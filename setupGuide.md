# Setup inicial

* Clonar los [repositorios de la organización](https://github.com/orgs/tp-taller-3/repositories)
* Instalar nvm, docker y docker-compose
* Pararse en cada repositorio salvo `documentation` y correr `nvm use`. Si la versión requerida de node no está instalada, va a dar instrucciones para instalarlo. (Antes de ejecutar cualquier comando, es importante que `nvm current` coincida con el archivo `.nvmrc` para todos los repositorios)
* En repos `backend`, `deploy` y `frontend`: `yarn install`
* En repos `tslint-config` y `validations`: `npm install`
* Para iniciar la BD, en repo `back-end` correr:
    * `docker-compose up -d fiuba-course-admin-backend-database-postgres`
    * `yarn db:create`
    * `yarn db:test:create`
    * `yarn db:all:reboot`
* Para chequear que todo va bien, correr `git commit` en todos los repos (el hook corre build, linter y tests)
    * Debería decir `nothing to commit`, sin errores
* Para levantar los server
    * En `back-end`: `yarn dev`
    * En `front-end`: `yarn start`
    * Entrar a [localhost:3000](http://localhost:3000) en el browser
