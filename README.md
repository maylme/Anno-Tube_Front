# Anno-Tube_Front
Partie front de Anno'Tube. 

Pour lancer le front: 

	- bower install;
	- polymer serve --open
	
Vous trouverez en en-tête de chaque fichier, les élèves qui ont travaillés dessus. 
Pour plus de details, referez vous au flux git. 

Pour tout problème ou demande d'information suplémentaire, vous pouvez contacter maylme par git. 

# Routing et ajout de page

Allez dans annotube-app.html. C'est le fichier "mère". La base de toutes les pages polymer.
Reperer le tag : 
``` html
<iron-pages></iron-pages>
```
Dedans vous avez déjà les deux pages home et 404. Rajouter votre page à ce niveau **EN GARDANT 404 EN DERNIER** du genre si j'ajoute la page poney : 
``` html
<annotube-home name="home"></annotube-home>
<annotube-poney name="poney"></annotube-poney>
<annotube-view404 name="view404"></annotube-view404>
```

Pour ce qui est du nom de la page elle doit être préfixer de "annotube-" sinon ca marhce pas.
Normalement tu n'as rien d'autre à faire.

Ta page doit s'appeler annotube-XXXX.html.

Si je fait une page poney : annotube-poney.html a ce squellette: 
``` html
<!--
Poney page
By: Mayl
-->
<!-- toujours mettre ca -->
<link rel="import" href="../../bower_components/polymer/polymer.html">

<dom-module id="annotube-home">
  <template>
    <style>
    	/* Whatever mon poulet ça c'est un exemple */
      :host {
        display: block;
        padding: 10px 20px;
      }
    </style>
    PONEYYYYYY <!-- enfin ton html quoi...-->
  </template>

  <script>
    Polymer({
      is: 'annotube-poney', /* oublie pas le prefixe "annotube-" */
    });
  </script>
</dom-module>

```
