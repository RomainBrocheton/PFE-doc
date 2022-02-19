# Utilisation

## Utilisation normale
Pour lancer l'application, il vous suffit de construire les images Docker et de lancer le container :
```
docker compose up --build
```

Une fois les images construites une première fois, vous pourrez uniquement lancer le container les fois suivantes :
```
docker compose up
```

Une fois lancé, l'interface utilisateur sera accessible à l'adresse http://localhost tandis que l'API sera accessible à l'adresse http://localhost:8080.

## Mode développeur
Le passage par Docker peut compliquer les tâches de devéloppement des entités. En effet, il faudrai reconstruire les images à chaque modification, ce qui peut prendre du temps. Pour éviter cela, vous pouvez lancer les entités une par une :

### Lancement du backend
```
cd ./server
npm start
```

Une fois lancée, l'API sera accessible à l'adresse http://localhost:8080.

### Lancement du frontend
```
cd ./front
ng serve --open
```

!> La variable d'environnement `MONGO_URL` ne sera pas pris en compte dans ce cas ! Il est nécessaire de recopier l'URL d'accès à la base de données dans le fichier `./server/database/mongo.js` dans la méthode `mongoose.connect()`. Par exemple :  `mongoose.connect('mongodb+srv://teamplay:mongodb-mongodb@teamplaycluster.quhje.mongodb.net/apinode' , function( error ){ })`

Une fois lancé, l'interface utilisateur sera accessible à l'adresse http://localhost:4200.