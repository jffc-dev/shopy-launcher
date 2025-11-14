### Dev
1. Clone repo
2. Create .env file based on .env.template
3. Run `docker compose up --build`


### Steps to create Git Submodules


1. Create new GitHub repo
2. Clone repo locally
3. Add the submodule, where `repository_url` is the url of the repo and `directory_name` is the name of the folder where the submodule will be stored (it shouldn't exist in the project)
```
git submodule add <repository_url> <directory_name>
```
4. Add the chages (git add, git commit, git push)
Ex:
```
git add .
git commit -m "Add submodule"
git push
```
5. Inicializar y actualizar Sub-módulos, cuando alguien clona el repositorio por primera vez, debe de ejecutar el siguiente comando para inicializar y actualizar los sub-módulos
```
git submodule update --init --recursive
```
6. Para actualizar las referencias de los sub-módulos
```
git submodule update --remote
```


## Importante
Si se trabaja en el repositorio que tiene los sub-módulos, **primero actualizar y hacer push** en el sub-módulo y **después** en el repositorio principal. 

Si se hace al revés, se perderán las referencias de los sub-módulos en el repositorio principal y tendremos que resolver conflictos.
