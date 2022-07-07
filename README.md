# BicTree

BicTree je strom, ktorý zobrazuje kategórie kníh podľa dát aké dostane. 

Počiatočné dáta sa nachádzajú v súbore `/src/data/bic/init.json`:
```
hierarchy - sú hlavné kategórie jazykov
bicHierarchy - je strom podkategórií, ten je rovnaký pre každú kategóriu ale zobrazuje sa len určitá časť
```

Vstupné dáta sú v testovacích súboroch: 
```
ag-c-1.json - hierarchy id 1
ag-c-1-b-AFJ.json - hierarchy id 1 + bicHierarchy AFJ
ag-c-24-b-KF.json - hierarchy id 24 + bicHierarchy KF
```

Vstupné dáta obsahujú:
```
bic - konkrétna vetva bic stromu
category - konkrétna hlavná kategória
aggregations - agregácie, teda počet kníh v danej 'category' a 'bic'
```

Výstup je strom na základe počiatočných a vstupných dát, ktorý zobrazuje konkrétne zvolenú kategóriu (podkategóriu).
Zobrazujú sa IBA tie kategórie (podkategórie), ku ktorým je uvedený počet v `aggregations`.
Pri každom testovacom súbore je aj obrázok, ako by strom s danou konfiguráciou mal vyzerať.

## Dizajn
[Figma](https://www.figma.com/file/P6wtaoHANCH1LQw4jGH4f0/Zadanie)

## Instructions
We are fans of [BEM](http://getbem.com/), [Vue](https://vuejs.org/v2/style-guide/),
[Icomoon](https://icomoon.io/app/#/select), [normalize.css](https://github.com/necolas/normalize.css/).

Create GitHub account if you don't have one and send your account to [Zombi](mailto:tomas.zamba@odyzeo.com), he will give you access.

Push your assignment as branch `feature/{firstname.lastname}` to this repo and create pull request.

If you need help or have any questions ask [Zombi](mailto:tomas.zamba@odyzeo.com).

Keep it simple and GLHF.

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
