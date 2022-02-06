# Cypress Integration Tests

Cypress est un outil qui permet de tester intégralement un site web ou une application web. Autrement dit : il émule les actions qu'on lui raconte sur différents éléments et on lui dit à quoi s'attendre, par exemple : 

```js
// cy est la façon dont nous devons interagir avec cypress 

cy.visit('http://localhost:30000') // Le pedimos a Cypress que visite esa URL, la cual contiene la interfaz Foundry

cy.get('button[type="submit"]').click(); // Nous demandons à Cypress de visiter cette URL, qui contient l'interface Foundry 

cy.get('h3').should('have.text', 'Anima Beyond Foundry'); // Enfin il vérifie qu'un H3 contient un nom donné 
```

Le but des tests d'intégration est de s'assurer que l'ensemble du module fonctionne correctement.

## Lancer des tests 

**TL;DR**

- Nous copions `cypress.env.example.json` dans `cypress.env.json` et configurons les champs 
- `npm run cypress:open`

**Note importante : Le lancement des tests de cyprès créera des mondes avec des noms aléatoires, vous devrez les supprimer manuellement après avoir lancé les tests **

### fichier de configuration

Pour lancer les tests, nous devons d'abord copier le fichier `cypress.env.example.json` et le renommer en `cypress.env.json`. Dans le fichier `cypress.env.json`, nous remplissons les champs suivants :

- `foundryAdminPassword` : c'est le mot de passe administrateur que vous utilisez dans Foundry pour pouvoir revenir à la liste des mondes ou vous connecter en tant qu'administrateur 

Remarque : Le fichier `cypress.env.json` est ignoré dans le `.gitignore` donc ne vous inquiétez pas, vos informations d'identification ne seront jamais téléchargées dans le référentiel par inadvertance 

### Ouvrir Cypress

Si nous faisons `npm run cypress:open` nous ouvrirons l'interface Cypress, nous y verrons tous les tests disponibles à lancer. Nous cliquons sur celui que nous voulons et c'est tout. 

