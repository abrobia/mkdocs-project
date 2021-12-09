# Projecte MkDocs

Projecte de test usant [Mkdocs](https://www.mkdocs.org/) com a eina de documentació i [GitHub Pages](https://pages.github.com/) com a eina de publicació. 

https://abrobia.github.io/mkdocs-project/  


## 1. Instal·lació Mkdocs

Instal·lem Mkdocs al nostre ordinador.

```
pip install mkdocs
```  


## 2. Creació inicial del projecte

Creem una carpeta en qualsevol directori del nostre ordinador on emmagtzemarem tots els arxius del projecte. En aquest cas el projecte s'anomena "mkdocs-project".

```
mkdocs new mkdocs-project
cd mkdocs-project
```  


## 3. Inicialització del servidor virtual

Iniciem el servidor Mkdocs a partir de la següent comanda:

```
mkdocs serve
```

Accedim a http://127.0.0.1:8000 per veure el nostre projecte local des del navegador.    


## 3. Configuració del projecte

Creem les pàgines .md de contingut.

Escollim un [theme](https://www.mkdocs.org/user-guide/choosing-your-theme/).

Afegim els [pluguins](https://www.mkdocs.org/dev-guide/plugins/) que desitgem.  


## 4. Publicació de la web amb GitHub pages

Des de GitHub, creem un nou repositori on pujarem el nostre projecte emmagatzemat a l'ordinador fent servir Git.  

Mitjançant el terminal, ens situem dins de la carpeta local ("mkdocs-project") que conté els arxius i a continuació executem:

```
python -m mkdocs build
```

Inicialitzem el repositori local i fem el nostre primer commit usant les següents ordres habituals:

```
git init
site/ > .gitignore
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/abrobia/mkdocs-project.git
git push -u origin main
$ mkdocs gh-deploy

```  

Si tot ha anat bé, la consola mostrarà el següent missatge final:

_Your documentation should shortly be available at:_ https://abrobia.github.io/mkdocs-project/  


## Actualització del projecte

Si es volen fer canvis (modificar, afegir contingut, etc):

* Creem una nova branch i la clonem des del nostre ordinador (usem SourceTree)
* Fem els canvis que vulguem des de l'editor (usem Visual Studio Code)
* Pujem els canvis a partir de les següents ordres:   
```
git add commit "NOM_DEL_COMMIT"
git push -u origin update
mkdocs gh-deploy
```  
De nou, si tot ha anat bé, la consola mostrarà el següent missatge final:

_Your documentation should shortly be available at:_ https://abrobia.github.io/mkdocs-project/  
