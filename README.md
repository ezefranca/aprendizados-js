# Aprendizados de JS

🐸 Eu sou meio burro, por isso estou fazendo anotações.

### Javascript Browser

#### DOM

```
document.body.addEventListener('click', function () {
     var myParent = document.getElementById("Banner"); 
     var myImage = document.createElement("img");
     myImage.src = 'https://thecatapi.com/api/images/get?format=src&type=gif';
     myParent.appendChild(myImage);
     myImage.style.marginLeft = "160px";
});
```


### Introdução

NodeJS é uma parada bem maneira. Dá pra usar pra quase tudo, IoT, fazer coisas sinistras no backend, enfim é bem maneiro. Entretanto carrega alguns problemas (vulgo "problemas", pois são problemas MEUS), o primeiro deles é o Javascript (🙃), sério, é uma linguagem marota, entretanto difícil, pois diferente de liguagens como C, C++, Objective-C, Swift, Javascript é interpretada, logo, NO FUCKING BREAKPOINTS... 

Essas anotações vão evoluir aos poucos conforme eu for aprendendo e entendendo coisas novas. Não tenho propósito de ser referência de nada, jamais, e não tenho nenhum compromisso e garantia com nada. São minhas anotações, você deveria fazer as suas, entretanto, contribuições e correções são bem vindas. 

### Hello World NodeJS

### Deploy da aplicação

### Adicionando Logs (FUCKING IMPORTANT)

```
console.log('Mensagem de Log aqui')
```

### Codigo bloqueante e codigo não bloqueante (FUCKING IMPORTANT)

O Node é especial justamente por rodar "código não bloqueante", para entender temos o exemplo:

```javascript
/* Blocking Code */

var getUserSync = require('./getUserSync')

var user1 = getUserSync('123');
console.log('user1', user1);

var user2 = getUserSync('321');
console.log('user2', user2);

var sum = 1 + 2;
console.log('the sum is' + sum);


/* Non-blocking Code */

var getUser = require('./getUser')

getUser('123', function (user1) {
	console.log('user1', user1);
});

getUser('321', function (user2) {
	console.log('user2', user2);
});

var sum = 1 + 2;
console.log('the sum is' + sum);
```


### Lendo os Logs quando deploy foi feito no heroku (FUCKING IMPORTANT)

```
heroku logs --tail
```
