## GOOGLE TRANSLATE SAUVAGE

## Instructions d'installation pour les développeurs

1) Clonez le référentiel vers \AppData\Local\FoundryVTT\Data\systems\AnimaBeyondFoundry. Dans Sourcetree, cela se fait dans File->Clone.

2) Installez node si vous ne l'avez pas : https://nodejs.org/en/download/

3) Dans VSCode, ajoutez le dossier du référentiel à l'espace de travail (clic droit sur le panneau de gauche et "Ajouter un dossier à l'espace de travail" par exemple). Faites ensuite un clic droit dessus et "Ouvrir dans le terminal intégré". Cela ouvre un terminal de commande Windows dans ce répertoire (...\FoundryVTT\Data\systems\AnimaBeyondFoundry). Dans ce terminal, exécutez la commande : 
`(? il manque la commande je pense)`

4) Dupliquez le fichier `foundryconfig.example.json` et renommez-le en `foundryconfig.json`, puis modifiez-le et remplissez le champ `destPath` avec le chemin où vous avez le dossier systèmes, par exemple :
   4.1. Windows : `C:/Users/<Nom d'utilisateur>/AppData/Local/FoundryVTT/Data/systems`
   4.2. Linux : `/home/<Nom d'utilisateur>/.local/share/FoundryVTT/Data/systems`
   4.3. Chez moi : `D:/Dev/FoundryVTT/Data/systems`

`installation npm`

4) Jusqu'à présent, ce dossier n'a aucun effet sur Foundry. Pour générer le dossier système réel, nous exécutons la commande :

`npm run-script build`, pour simplement le construire, ou

`npm run-script build:watch`, pour le générer et aussi pour le régénérer si nous apportons des modifications au dossier du référentiel.

5) Ouvrez la fonderie. Nous devrions voir Anima Beyond Fantasy parmi nos systèmes installés.

## Instructions de travail pour les développeurs

a) Pour commencer à travailler sur quelque chose qui n'est pas déjà en cours de travail :

1) Nous allons à la branche DEVELOP.
   -Dans Sourcetree, la première fois, il faut aller dans le panneau de gauche, dans >Remotes>background> et double-cliquer sur la branche dans laquelle on veut se placer. Ce faisant, nous verrons comment maintenant dans le panneau de gauche, dans >Branches, la branche dans laquelle nous venons de nous placer apparaît (les branches qui apparaissent dans >Branches sont celles que nous avons localement, et celles dans >Remote sont celles que nous ont). sont sur GitHub).
- Les fois suivantes, lorsque nous avons déjà Développer dans le menu déroulant >Branches, nous double-cliquons simplement dessus pour nous y placer.

2) Nous nous assurons que nous disposons de la version la plus à jour du référentiel : bouton FETCH, et si un changement est détecté, bouton PULL.

3) Nous créons une nouvelle branche à partir de develop. Dans Sourcetree, cela se fait sur le bouton Branches à côté de Fetch. Mettez un nom descriptif du travail qui va être fait dans cette branche, afin que nous comprenions tous ce qui est fait et ce qui ne l'est pas

4) On se place dans la branche dans laquelle on va travailler (celle que l'on vient de créer).

5) Planifier des trucs : dans VSCode, ouvrez le terminal dans le dossier du référentiel et exécutez la commande :

`npm run-script build:watch`

Tant que le terminal fonctionne avec cette commande, toute modification apportée au dossier du référentiel entraînera la recompilation et la mise à jour du dossier animabf par le projet.
- Pour voir les changements dans Foundry, il suffit généralement d'appuyer sur f5 à l'intérieur du monde une fois le projet compilé. Sinon, Options -> Revenir à la configuration et recharger le monde.

5) Lorsque votre travail est terminé, ou lorsque vous souhaitez enregistrer votre progression, validez la branche sur laquelle vous vous trouvez. Dans Sourcetree, cela se fait sur le bouton COMMIT en haut à gauche. En lui donnant, vous obtenez des fichiers mis en scène et des fichiers non mis en scène. Organisez les fichiers que vous souhaitez enregistrer, ajoutez un commentaire descriptif ci-dessous sur ce que vous avez fait et appuyez sur Valider dans le coin inférieur droit.

6) Si vous n'avez pas coché la case "Push Immediately..." lors de la validation, vous verrez le bouton Push s'allumer. Vérifiez que vous êtes bien dans la branche où vous devez vous trouver et appuyez sur le bouton PUSH.

7) Lorsque le travail sur une certaine fonctionnalité est complètement terminé, nous entrons dans Git et faisons une PULL REQUEST depuis notre branche pour développer, et marquons certains de nos collègues comme réviseurs afin qu'ils révisent notre code avant de l'accepter. Ceux d'entre vous qui ont des doutes demandent sur Discord.

8) De temps en temps, lorsque la branche Develop a eu suffisamment de changements, une MERGE sera effectuée de la branche develop à la branche master. Encore une fois, il vaut mieux que cela ne se fasse qu'avec un consensus entre plusieurs.

b) Pour continuer votre travail ou le travail d'un autre : Comme ci-dessus mais sans l'étape 1 ou 3.

## Liens utiles

- [Comment créer un nouveau type d'élément] (add-new-item.md)
- [Test Cyprès](cypress_integration_tests.md) 