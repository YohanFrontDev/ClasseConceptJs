

<!-- Preview = Ctrl + Maj + V -->


# Concept Classe JS
#### Utiliser l'héritage pour ajouter des fonctionnalités.
### Partie 1: Définir deux classes Film et Série.


*L’héritage est un paradigme de programmation: c'est une façon de programmer en suivant un ensemble de théories, concepts et principes. (ex: programmation orientée objet -> paradigme)*

```bash
##  Utilisation du this pour définir le paramètre de MON OBJET
class Film {
   constructor(title, releasedDate, duration) {
       this.title = title                  # param 1 -> console.log(this.title)
       this.releasedDate = releasedDate    # param 2 -> console.log(this.releaseDate)
       this.duration = duration            # param 3 -> console.log(this.duration)
   }
}

class Série {
   constructor(title, numberOfEpisodePerSeason, numberOfSeasons) {
       this.title = title
       this.numberOfEpisodePerSeason = numberOfEpisodePerSeason
       this.numberOfSeasons = numberOfSeasons
   }
}

# Instanciation de 3 films. (param1, param2, param3)
const FilmPredator = new Movie("Predator", 1987, 107)
const FilmTerminator = new Movie("Terminator", 1984, 107)
const FilmAlien = new Movie("Alien", 1979, 117)

# Instanciation de 3 séries. (param1, param2, param3)
const SerieFriends = new TvShow("Friends", 23, 10)
const SerieScrubs = new TvShow("Scrubs", 20, 9)
const SerieSupernatural = new TvShow("Supernatural", 24, 15)
```

*********
* ##### Partie 2: Création d'une classe Media. 

```bash
class Media {
   constructor(url) {
       this.url = url # param 1
   }
    #Création d'une fonction de ma classe Media.
   jouer() {
       #Afficher mon url dans la console.
       console.log(this.url)
   }
}
```


*********
* #### Partie 3: Utiliser un paramètre de ma classe Media dans mes autre classes. 
    ######   Utiliser l'héritage pour ajouter des fonctionnalités.

Nous allons faire appel au mot clé Extends afin de permettre aux classes Film et Série d'utiliser la fonction jouer.Nous ajouterons bien évidemment en paramètre notre "url".
```bash
 class Media {
    constructor(url) {
        this._url = url
    }
 
    jouer() {
        console.log(PredatorMovie._url)
    }
 }
 class Film extends Media{
   constructor(url,title, releasedDate, duration) {
       this.title = title                  # param 1 -> console.log(this.title)
       this.releasedDate = releasedDate    # param 2 -> console.log(this.releaseDate)
       this.duration = duration            # param 3 -> console.log(this.duration)
   }
}

class Série extends Media{
   constructor(url,title, numberOfEpisodePerSeason, numberOfSeasons) {
       this.title = title
       this.numberOfEpisodePerSeason = numberOfEpisodePerSeason
       this.numberOfSeasons = numberOfSeasons
   }
}

 const FilmPredator = new Film("https//www.youtube/hvfdvikhbi3kjnfre34.com", "Predator", 1987, 107)
 FilmPredator.play() #fonctionnera grâce à notre extends.

```

