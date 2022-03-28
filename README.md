[![funding](https://img.shields.io/static/v1?label=published+through&message=LIFE+RIPARIAS&labelColor=00a58d&color=ffffff)](https://www.riparias.be/)

# List of Invasive Alien Species of Union concern

## Rationale

This repository contains the functionality to standardize the data of [List of Invasive Alien Species of Union concern](https://ec.europa.eu/environment/nature/invasivealien/list/index_en.htm) to a [Darwin Core checklist](https://www.gbif.org/dataset-classes) that can be harvested by [GBIF](http://www.gbif.org).

## Workflow

[source data](data/raw) → Darwin Core [mapping script](src/dwc_mapping.Rmd) → generated [Darwin Core files](data/processed)

The source data are manually created from:

- [2019 consolidated version pdf](https://ec.europa.eu/environment/nature/invasivealien/docs/R_2016_1141_Union-list-2019-consolidation.pdf): scientific names with authors, synonym names (in parenthesis) with authors
- [web page](https://ec.europa.eu/environment/nature/invasivealien/list/index_en.htm): English name, entry into force, kingdom (table headers)

## Published dataset

<!-- This section provides links to the published dataset. Obviously, you'll only be able to add those links once you have published your dataset. 😋 -->

* [Dataset on the IPT](<!-- Add the URL of the dataset on the IPT here -->)
* [Dataset on GBIF](<!-- Add the DOI of the dataset on GBIF here -->)

## Repo structure

The repository structure is based on [Cookiecutter Data Science](http://drivendata.github.io/cookiecutter-data-science/) and the [Checklist recipe](https://github.com/trias-project/checklist-recipe). Files and directories indicated with `GENERATED` should not be edited manually.

```
├── README.md              : Description of this repository
├── LICENSE                : Repository license
├── union-list.Rproj       : RStudio project file
├── .gitignore             : Files and directories to be ignored by git
│
├── data
│   ├── raw                : Source data, input for mapping script
│   └── processed          : Darwin Core output of mapping script GENERATED
│
└── src
    └── dwc_mapping.Rmd    : Darwin Core mapping script, core functionality of this repository
```

## Installation

1. Clone this repository to your computer
2. Open the RStudio project file
3. Open the `dwc_mapping.Rmd` [R Markdown file](https://rmarkdown.rstudio.com/) in RStudio
4. Install any required packages
5. Click `Run > Run All` to generate the processed data

## License

[MIT License](LICENSE) for the code and documentation in this repository. The included data is released under another license.
