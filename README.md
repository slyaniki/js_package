# js_package
petite présentation de quelques packages js et comment les utiliser


`AXIOS`

Axios est un client HTTP basé sur des promesses pour le navigateur et Node.js. Axios facilite l'envoi de requêtes HTTP asynchrones aux points de terminaison REST et l'exécution d'opérations CRUD.

installation

`$ npm install axios` ou voir d'autre manière d'installation

## Effectuer une requette GET ##

` const axios = require('axios');

axios.get('http://webcode.me').then(resp => {

    console.log(resp.data);
});`
  
    
    

  ## Axios requette GET async/await ##

`const axios = require('axios');

async function makeGetRequest() {
  
  let res = await axios.get('http://webcode.me');

  let data = res.data;
  console.log(data);
}
GetRequest(); `  
  
  
 ## Axios  API consommation ##
 get(), post(), ou  delete() 

basic_api.js

`const axios = require('axios');

async function makeRequest() {

    const config = {
        method: 'get',
        url: 'http://webcode.me'
    }

    let res = await axios(config)

    console.log(res.status)
}

Request();`  
  
  
## Effectuer une POSTdemande##
 
 `const axios = require('axios');
async function makePostRequest() {
    let res = await axios.post('https://jsonplaceholder.typicode.com/posts');
    console.log(`Status code: ${res.status}`);
    console.log(`Status text: ${res.statusText}`);
    console.log(`Request method: ${res.request.method}`);
    console.log(`Path: ${res.request.path}`);

    console.log(`Date: ${res.headers.date}`);
    console.log(`Data: ${res.data}`);
}

makePostRequest();`
  
  
  
  ##socket io##
  
  etablie une connection en temps réel entre client et serveur
  
  
 ##installation##
 
 ` npm install socket.io `
 
 ##initialisation##
 
 `<script> 
  let socket = io();
  socket.emit('message');
  socket.on('message,(data)=>{
  console.log(data);
  });
  
 
 </script>`
 
 
 ##express session##
 
 ## installation 
 
 `npm install --save express-session `
 
 ##initialiser 
 
 `  router.route("/actu")
   .get((req,res)=>{
       if(req.session.enligne)
            res.render('actu.ejs')
        else
            res.status(404).send("err")
     })
      
module.exports = router; `
 
  ## annyang js 
  
  un package utiliser pour l'activation des commandes vocaux.
  
  ` <script src="//cdnjs.cloudflare.com/ajax/libs/annyang/2.6.1/annyang.min.js"></script>
<script>
if (annyang) {
  // Let's define a command.
  var commands = {
    'hello': function() { alert('Hello world!'); }
  };

  // Add our commands to annyang
  annyang.addCommands(commands);

  // Start listening.
  annyang.start();
}
</script> ` 


## validator js
   un outils de validation de données
## Installation et utilisation
Utilisation côté serveur
Installez la bibliothèque avec `npm install validator`

` var validator =  require ( ' validator ' ); validateur . isEmail ( ' foo@bar.com ' ); // => true  `  

## Utilisation côté client
La bibliothèque peut être chargée en tant que script autonome ou via un chargeur compatible avec AMD.

< script  type = " text / javascript "  src = " validator.min.js " > </ script > 
< script  type = " text / javascript " >
  validateur . isEmail ( ' foo@bar.com ' ); // => true
</ script > `
