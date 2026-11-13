# CV en ligne

Site de CV en français construit avec Jekyll et le thème [Jekyll Professional Resume](https://github.com/byanko55/jekyll-professional-resume), chargé depuis sa branche `master`.

## Personnaliser le CV

Modifiez les informations personnelles et les liens dans `_config.yml`. Les sections du CV se définissent dans des fichiers YAML placés dans `_data/`, un fichier par section :

* `experiences.yml` : expériences professionnelles
* `formation.yml` : formation
* `competences.yml` : compétences
* `langues.yml` : langues
* `profil.yml` : profil professionnel

Chaque fichier suit cette structure. Ajoutez un élément par expérience, diplôme, compétence ou langue dans `contents` :

```yml
subject: Expériences professionnelles
listing-order: 1
icon: "/assets/img/briefcase.svg"
contents:
  - title: "Intitulé du poste"
    role: "Votre rôle"
    date: "2023–2025"
    description:
      - "Responsabilité ou réalisation."
```

Les champs propres à un élément peuvent varier selon la section : utilisez par exemple `level` pour le niveau d'une langue ou `grade` pour un diplôme. Les fichiers actuels reprennent les informations de `raw.txt`. La page `index.html` utilise la mise en page `home` du thème, qui lit automatiquement les fichiers de `_data/` et trie les sections avec `listing-order`.

## Prévisualiser localement

Installez une version de Ruby compatible avec Jekyll 3.9 et Bundler, puis lancez :

```sh
bundle install
bundle exec jekyll serve
```

Ouvrez ensuite <http://localhost:4000/cv-en-ligne/>.

## Publier avec GitHub Pages

Dans les paramètres du dépôt, ouvrez **Pages**, choisissez **Deploy from a branch**, puis sélectionnez la branche `main` et le dossier `/ (root)`. GitHub Pages construira le site avec la configuration Jekyll. L'adresse configurée est `https://esthertchangani.github.io/cv-en-ligne/`; modifiez `url` et `baseurl` dans `_config.yml` si vous publiez sous une autre adresse.

Le thème amont est distribué sous licence MIT : [licence et code source](https://github.com/byanko55/jekyll-professional-resume).
