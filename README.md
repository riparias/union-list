[![funding](https://img.shields.io/static/v1?label=published+through&message=LIFE+RIPARIAS&labelColor=00a58d&color=ffffff)](https://www.riparias.be/)

# List of Invasive Alien Species of Union concern

## Rationale

This repository contains the functionality to standardize the data of the [List of Invasive Alien Species of Union concern](https://ec.europa.eu/environment/nature/invasivealien/list/index_en.htm) to a [Darwin Core Archive](https://www.gbif.org/darwin-core) that can be harvested by [GBIF](https://www.gbif.org/).

## Workflow

[source data](https://github.com/riparias/union-list/tree/main/data/raw) → Darwin Core [mapping script](https://riparias.github.io/union-list/dwc_mapping.html) → generated [Darwin Core files](https://github.com/riparias/union-list/tree/main/data/processed)

The source data are manually created from:

- [2022 consolidated version pdf](https://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:02016R1141-20220802&from=EN): scientific names with authors, synonym names (in parenthesis) with authors
- spreadsheets containing common names: [first version](https://circabc.europa.eu/ui/group/4cd6cb36-b0f1-4db4-915e-65cd29067f49/library/2ed2ee2a-730f-4583-a3ac-bb2a1815ad6a/details) (January 2018) and later additions ([April 2020](https://circabc.europa.eu/ui/group/4cd6cb36-b0f1-4db4-915e-65cd29067f49/library/1ac00d12-613b-447c-ab91-3016af071bcf/details) and [January 2022](https://circabc.europa.eu/ui/group/4cd6cb36-b0f1-4db4-915e-65cd29067f49/library/fad036d3-e2df-4adb-9c7a-7b9593a4c2f8/details))

## Published dataset

<!-- This section provides links to the published dataset. Obviously, you'll only be able to add those links once you have published your dataset. 😋 -->

- [Dataset on the IPT](https://ipt.inbo.be/resource?r=union-list)
- [Dataset on GBIF](https://doi.org/10.15468/97aucj)

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
