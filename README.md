# api-filmaffinity
API REST no oficial de Filmaffinity en castellano

Desarrollada por Carlos Ramos


# API Filmaffinity

* [Introducción](#introduccion)
* [Ejemplos de uso](#ejemplos-de-uso)

## Introducción

Se ha implementado una API REST para extraer información de Filmaffinity.
Se trata de una API no oficial, por lo que blablabla...

### Ejemplos de uso
* Búsqueda de id de películas que coincidan con los términos de búsqueda introducidos:
    * GET https://pelisdatosapi.herokuapp.com/api/busqueda/lo+que+el+viento+se+llevo
```json
    [
        {
            titulo: "Lo que el viento se llevó (1939) - Filmaffinity",
            id: "470268",
            poster: "https://pics.filmaffinity.com/Lo_que_el_viento_se_llev-432251527-large.jpg"
        }
    ]
```

   * GET https://pelisdatosapi.herokuapp.com/api/busqueda/la+amenaza+fantasma
```json
    [
        {
            titulo: "La guerra de las galaxias. Episodio I: La amenaza fantasma (1999 ...",
            id: "267008",
            poster: "https://pics.filmaffinity.com/La_guerra_de_las_galaxias_Episodio_I_La_amenaza_fantasma-434398792-large.jpg"
        },
        {
            titulo: "Stealth: La amenaza invisible (2005) - Filmaffinity",
            id: "553558",
            poster: "https://pics.filmaffinity.com/Stealth_La_amenaza_invisible-730759310-large.jpg"
        }
    ]
```

* Búsqueda de una película a través de su id :
    * GET https://pelisdatosapi.herokuapp.com/api/pelicula/470268
```json
    {
        titulo: "Lo que el viento se llevó",
        anio: "1939",
        direccion: "Victor Fleming, George Cukor, Sam Wood",
        reparto: "Vivien Leigh, Clark Gable, Olivia de Havilland, Leslie Howard, Hattie McDaniel,
            Thomas Mitchell, Barbara O'Neil, Butterfly McQueen, Ona Munson, Ann Rutherford, Evelyn
            Keyes, Mickey Kuhn, Ward Bond",
        sinopsis: "Georgia, 1861. En la elegante mansión sureña de Tara, vive Scarlett O'Hara
            (Vivien Leigh), la joven más bella, caprichosa y egoísta de la región. Ella suspira
            por el amor de Ashley (Leslie Howard), pero él está prometido con su prima, la dulce y
            bondadosa Melanie (Olivia de Havilland). En la última fiesta antes del estallido de la
            Guerra de Secesión (1861-1865), Scarlett conoce al cínico y apuesto Rhett Butler
            (Clark Gable), un vividor arrogante y aventurero, que sólo piensa en sí mismo y que no
            tiene ninguna intención de participar en la contienda. Lo único que él desea es hacerse
            rico y conquistar el corazón de la hermosa Scarlett."
    }
```

   * GET https://pelisdatosapi.herokuapp.com/api/pelicula/267008
```json
    {
        titulo: "La guerra delas galaxias. Episodio I: La amenaza fantasma",
        anio: "1999",
        direccion: "George Lucas",
        reparto: "Liam Neeson, Ewan McGregor, Natalie Portman, Jake Lloyd, Samuel L. Jackson,
            Ian McDiarmid, Ray Park, Anthony Daniels, Kenny Baker, Pernilla August, Hugh Quarshie,
            Ahmed Best, Andy Secombe, Frank Oz, Terence Stamp, Keira Knightley, Oliver Ford
            Davies, Ralph Brown, Warwick Davis, Sofia Coppola, Dominic West, Silas Carson",
        sinopsis: "Ambientada treinta años antes que 'La guerra de las galaxias' (1977),
            muestra la infancia de Darth Vader, el pasado de Obi-Wan Kenobi y el resurgimiento
            de los Sith, los caballeros Jedi dominados por el Lado Oscuro. La Federación de
            Comercio ha bloqueado el pequeño planeta de Naboo, gobernado por la joven Reina
            Amidala; se trata de un plan ideado por Sith Darth Sidious, que, manteniéndose en
            el anonimato, dirige a los neimoidianos, que están al mando de la Federación.
            El Jedi Qui-Gon Jinn y su aprendiz Obi-Wan Kenobi convencen a Amidala para que vaya
            a Coruscant, la capital de la República y sede del Consejo Jedi, y trate de
            neutralizar esta amenaza. Pero, al intentar esquivar el bloqueo, la nave real
            resulta averiada, viéndose así obligada la tripulación a aterrizar en el desértico
            y remoto planeta de Tatooine..."
    }
```