# Decouverte de nouvelles proprietés CSS et sélecteurs
## Clip-path
"La propriété CSS clip-path empêche une portion d'un élément d'être affichée en définissant une région de rognage. Seule la zone spécifique de l'élément à l'intérieur de la région sera affichée, le reste sera masqué". Nous pouvons utiliser cette proprieté por donner de nouvelles formes aux éléments.
Example:
Avec le code CSS `clip-path: polygon(50% 0%, 0% 100%, 100% 100%);` nous avons ce resultat ci: [Example clip-path](http://www.cepegra-labs.be/webdesign/fed2023/alexandra/html+css/Untitled.png)

Example 2:
Avec le code CSS `…img{
        width: 900px;
        clip-path: circle(30%);
    }…
    ….polly{
        clip-path: polygon(0% 0%, 75% 0%, 100% 100%, 25% 100%);
    }…`nous avons ce resultat ci: [Example 2 clip-path](http://cepegra-labs.be/webdesign/fed2023/diego/html-css/exo-marckdown/index.html)

## Scroll-snap-type
[Example scroll-snap-type](https://discordapp.com/channels/1160117567336222770/1163802451313438803/1185195125173919824)


## :has & :is

### :has
Le sélecteur :has permet de sélectionner un élément qui contient quelque chose de spécifique, par exemple sélectionner uniquement les div qui contiennent un <p>

Example:
`div:has(p) {
  background: red;
}`

### :is
"Le sélecteur :is() nous propose de sélectionner plusieurs éléments à cibler sans devoir préciser à chaque fois les éléments parents"

Example:

Au lieu d'écrire:

`section h1, section h2, section h3, section h4, section h5, section h6, 
article h1, article h2, article h3, article h4, article h5, article h6, 
aside h1, aside h2, aside h3, aside h4, aside h5, aside h6, 
nav h1, nav h2, nav h3, nav h4, nav h5, nav h6 {
  color: #BADA55;
}`

On mettrais plutôt:

`:is(section, article, aside, nav) :is(h1, h2, h3, h4, h5, h6) {
  color: #BADA55;
}`
