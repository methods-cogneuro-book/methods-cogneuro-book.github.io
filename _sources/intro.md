---
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.10.3
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# Introduction

Ce livre, "Méthodes en neurosciences cognitives", présente les principales techniques de neuroimagerie utilisées pour étudier la cognition chez l'humain (et l'animal) et disposant d'une bonne résolution spatiale:
 * résonance magnétique (anatomique, fonctionnelle, et de diffusion),
 * tomographie par émission de positrons,
 * imagerie optique.

Ce livre est une entrée en matière et est destiné à des lecteurs qui découvrent ces méthodes pour la première fois. Ce livre vous fournira des connaissances théoriques sur les bases physiques et physiologiques de ces techniques de neuroimagerie. De plus, il propose une introduction aux principales techniques de traitement d’image et d’analyse statistique qui leur sont associées. Chaque chapitre comporte une série d'exercices qui incluent des exemples d'applications dans le cadre de projets de recherche en neurosciences cognitives.

```{warning}
L'objectif de cet ouvrage n'est pas d'être un outil de référence de type "ouvrage spécialiste" qui explique tous les détails spécifiques liés à une technique donnée. Le but de ce livre est plutôt de présenter un survol de l'ensemble des techniques les plus conventionnelles en neuroscience cognitive de manière concise, pour que les lecteurs puissent en apprécier les forces et faiblesses, ainsi que comprendre comment choisir la technique la plus adaptée à un type de recherche spécifique.
```

## Contribuer
Ce projet est développé de manière collaborative. Toute suggestion est la bienvenue! Vous pouvez utiliser la page "[issue](https://github.com/PSY3018/psy3018.github.io/issues)" de Github pour faire une demande à l'équipe, ou décrire un problème. Vous pouvez également proposer directement un changement en effectuant une "pull request" sur la [page Github](https://github.com/PSY3018/psy3018.github.io) du livre.

## Contributeurs

Le développement de ce livre a démarré afin de servir d'outil de référence pour le cours PSY3018, donné au baccalauréat en neurosciences cognitives de l'Université de Montréal. Le cours est donné principalement par le Dr Pierre Bellec, avec la contribution des auxiliaires d'enseignement ainsi que de multiples intervenants supplémentaires. Ce livre bénéficie également du retour constructif des étudiants ayant suivi le cours PSY3018 depuis sa création en 2018. Les contributions générales sont présentées ci-dessous. Des contributions spécifiques sont listées au sein de chaque chapitre.

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/pbellec">
        <img src="https://avatars.githubusercontent.com/u/1670887?v=4?s=100" width="100px;" alt=""/>
        <br /><sub><b>Pierre bellec</b></sub>
      </a>
      <br />
        <a title="Contenu">🤔</a>
        <a title="Code">💻</a>
        <a title="Quizz">⚠️</a>
        <a title="Révision du texte">👀</a>
    </td>
    <td align="center">
      <a href="https://github.com/eddyfortier">
        <img src="https://avatars.githubusercontent.com/u/72314243?v=4?s=100" width="100px;" alt=""/>
        <br /><sub><b>Eddy Fortier</b></sub>
      </a>
      <br />
        <a title="Contenu">🤔</a>
        <a title="Révision du texte">👀</a>
    </td>
    <td align="center">
      <a href="https://github.com/danjgale">
        <img src="https://avatars.githubusercontent.com/u/14634382?v=4?s=100" width="100px;" alt=""/>
        <br /><sub><b>Dan J Gale</b></sub>
      </a>
      <br />
        <a title="Figure">🎨</a>
    </td>
    <td align="center">
      <a href="https://github.com/SamGuay">
        <img src="https://avatars.githubusercontent.com/u/30598330?v=4?s=100" width="100px;" alt=""/>
        <br /><sub><b>Samuel Guay</b></sub>
      </a>
      <br />
        <a title="Révision du texte">👀</a>
    </td>  
    <td align="center">
      <a href="https://github.com/Xanthylajoie">
        <img src="https://avatars.githubusercontent.com/u/90349544?v=4?s=100" width="100px;" alt=""/>
        <br /><sub><b>Xanthy Lajoie</b></sub>
      </a>
      <br />
        <a title="Contenu">🤔</a>
        <a title="Révision du texte">👀</a>
    </td>
  </tr>
  <tr>
    <td align="center">
      <a href="https://github.com/elisabethloranger">
        <img src="https://avatars.githubusercontent.com/u/90270981?v=4?s=100" width="100px;" alt=""/>
        <br /><sub><b>Élisabeth Loranger</b></sub>
      </a>
      <br />
        <a title="Contenu">🤔</a>
    </td>
    <td align="center">
      <a href="https://github.com/sangfrois">
        <img src="https://avatars.githubusercontent.com/u/38385719?v=4?s=100" width="100px;" alt=""/>
        <br /><sub><b>François Lespinasse</b></sub>
      </a>
      <br />
        <a title="Contenu">🤔</a>
        <a title="Révision du texte">👀</a>
    </td>
    <td align="center">
      <a href="https://github.com/me-pic">
        <img src="https://avatars.githubusercontent.com/u/77584086?v=4?s=100" width="100px;" alt=""/>
        <br /><sub><b>Marie-Eve Picard</b></sub>
      </a>
      <br />
        <a title="Contenu">🤔</a>
        <a title="Révision du texte">👀</a>
    </td>
    <td align="center">
      <a href="https://github.com/anproulx">
        <img src="https://avatars.githubusercontent.com/u/65092948?v=4?s=100" width="100px;" alt=""/>
        <br /><sub><b>Andréanne Proulx</b></sub>
      </a>
      <br />
        <a title="Contenu">🤔</a>
    </td>
  </tr>
</table>

## Remerciements
Ce livre est dans une large mesure "reproductible": de nombreuses figures sont générées à l'aide de données ouvertes, avec du code accessible à même le livre. Cette technologie est rendue possible grâce aux projets suivants:
 * [jupyter book](https://jupyterbook.org) est l'outil utilisé pour générer le livre. Ce projet repose lui-même sur l'outil de documentation [sphinx](https://www.sphinx-doc.org).
 * La librairie [nilearn](https://nilearn.github.io/) en [python](https://www.python.org/), notamment pour la partie sur l'IRM structurelle, l'IRM fonctionnelle et les modèles statistiques.
 * La librairie [Dipy](https://dipy.org), notamment pour la partie sur l'IRM de diffusion.
 * La librairie [MNE python](https://mne.tools/stable/index.html) est utilisée dans le chapitre portant sur l'imagerie optique.
 * Les visualisations d'images cérébrales utilisées dans le cours proviennent en partie de jeux de données publiques. L'origine des données est précisée dans la description de chacune des figures.
 * Le logo provient du site <a href="https://www.vecteezy.com/free-vector/brain">Brain Vectors by Vecteezy</a>
 * Certaines images du livre ont été obtenues sous droits illimités pour diffusion web et limités pour impression (500k copies) via [shutterstock](https://www.shutterstock.com) par P. Bellec.

 Les auteurs sont très reconnaissants pour l'énorme travail et la générosité des communautés qui créent et maintiennent tous ces projets!

 ## Statistiques
 La génération des figures pour les différents chapitres du livre a requis les temps suivants:
 ```{nb-exec-table}
```
