# footer

## blocs de liens (link widget)

Le footer est composé de plusieures colonnes : informations de la boutique et deux ou trois colonnes supplémentaires.

Pour modificer ces colonnes:

* Menu latéral
* Personnaliser -> Apparence -> Link Widget

L'écran permet de:  

* modifier l'ordre des éléments 
* supprimer un bloc
* ajouter un bloc  

Les blocs sont des composés d'un titre et de liens.  Lors de l'ajout ou d'une modification il est possible de spécifier:

* un titre
* un point d'accroche 
* des contenus personalisé (traductions) pour les langues
* un choix entre les divers liens disponibles dans la boutique avec la possibilité d'en créer.

## copyright

Le copyright est la petite ligne en bas de l'écran, elle indique que celui-ci a été réalisé à l'aide de prestashop.  Il est possible de modifier.

Deux choses sont à modifier.

### Le texte du copyright

* Dans le menu latéral je choisi  Personnaliser -> International -> traductions
* Dans écran je sélectionne:

  * Type de traduction -> traduction du thème
  * Sélectionnez votre thème -> classic
  * Choisissez votre langue -> français
  * Bouton 'Modifier'

* Dans l'écran suivant je peux accéder directement à mon élément à modifier:
  * Dans le champs de recherche je tape soit
    * 'copyright' ou
    * 'ecommerce software by'
* Par naviguation je clique:
  * shop -> themes -> global -> page 3
* les deux méthodes mènent au même élément à modifier.
* la chaîne ```%copyright% %year% - site e-commerce (example) par %prestashop%```  est le texte à modifier les élément entre % sont des %variable%. De base il y a trois variables qui se retrouvent dans le code. Il doit y avoir le même nombre dans la traduction et dans le code.
  * copyright
  * année
  * prestashop
* Le copyright est un lien pour qu'il ne renvoie plus vers le site de prestashop il aller modifier dans le code.

### L'url du copyright
* la page se trouve à **templates/_partials/footer.tpl** 
* tout en bas de la page se trouve le code du copyright, c'est la que je peux modifier l'url et aussi les variables du bloc
```smarty 
{block name='copyright_link'}
    <a class="_blank" href="http://www.jphnovitz.be" target="_blank">
        {l s='%copyright% %year% - Ecommerce software by %prestashop%' sprintf=['%prestashop%' => 'jphNovitz™', '%year%' => 'Y'|date, '%copyright%' => '©'] d='Shop.Theme.Global'} 
    </a> 
{/block}
 ```

[<< retour à l'index](index.md)