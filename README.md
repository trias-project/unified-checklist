# Global Register of Introduced and Invasive Species - Belgium

[![Build Status](https://travis-ci.org/trias-project/unified-checklist.svg?branch=master)](https://travis-ci.org/trias-project/unified-checklist)

## Rationale

This repository contains the functionality to create and standardize the _Global Register of Introduced and Invasive Species - Belgium_ to a [Darwin Core checklist](https://www.gbif.org/dataset-classes) that can be harvested by [GBIF](http://www.gbif.org).

This unified checklist is the result of an open and reproducible data publication and data processing pipeline developed for the [TrIAS project](http://trias-project.be). The data publication pipeline is based on the [Checklist recipe](https://github.com/trias-project/checklist-recipe/wiki) and consists of the publication of a selection of authoritative (inter)national checklists as standardized Darwin Core Archives to [GBIF](https://www.gbif.org/dataset/search?type=CHECKLIST&project_id=trias). These are:

1. [Verloove et al. (2018)](https://doi.org/10.15468/wtda1m) based on Verloove (2018) for plants
2. [Boets et al. (2018)](https://doi.org/10.15468/yxcq07) based on Boets et al. (2016) for macroinvertebrates
3. [Verreycken et al. (2018a)](https://doi.org/10.15468/xvuzfh) based on Verreycken et al. (2018b) for fishes
4. [Vanderweyen et al. (2018)](https://doi.org/10.15468/2dboyn) based on Vanderweyen & Fraiture (2007, 2008, 2011) for rust fungi
5. [Reyserhove et al. (2018)](https://doi.org/10.15468/3pmlxs) for various species
6. [Zieritz et al. (2018)](https://doi.org/10.15468/guejza) based on Zieritz et al. (2017) for pathways.

Predominantly, these checklists record the presence of alien species in Belgium for a specific taxon group or habitat and are maintained by their respective authors. The data processing consists of the extraction of all Belgian non-native taxa from these checklists and the unification of their taxonomy (using the [GBIF Backbone Taxonomy](https://doi.org/10.15468/39omei)) and related information. This automated process is implemented and documented at https://trias-project.github.io/unified-checklist/

## Workflow

See https://trias-project.github.io/unified-checklist/

## Published dataset

* [Dataset on the IPT](https://ipt.inbo.be/resource?r=unified-checklist)
* [Dataset on GBIF](https://doi.org/10.15468/xoidmd)

## Repo structure

The repository structure is based on [Cookiecutter Data Science](http://drivendata.github.io/cookiecutter-data-science/) and the [Checklist recipe](https://github.com/trias-project/checklist-recipe). Files and directories indicated with `GENERATED` should not be edited manually.

```
├── README.md              : Description of this repository
├── LICENSE                : Repository license
├── unified-checklist.Rproj : RStudio project file
├── .gitignore             : Files and directories to be ignored by git
│
├── data
│   ├── raw                : Source data as downloaded from GBIF GENERATED
│   ├── interim            : Unified data GENERATED
│   └── processed          : Darwin Core output of mapping script GENERATED
│
├── docs                   : Repository website GENERATED
│
├── index.Rmd              : Website homepage
├── _bookdown.yml          : Settings to build website in docs/
│
└── src
    ├── 1_get_taxa.Rmd     : Script to get taxa from checklists
    ├── 2_get_information.Rmd : Script to get related information
    ├── 3_verify_taxa.Rmd  : Script to verify taxa
    ├── 4_unify_taxa.Rmd   : Script to unify taxa
    ├── 5_unify_information.Rmd : Script to unify related information
    └── 6_dwc_mapping.Rmd  : Script to map to Darwin Core
```

## Installation

1. Clone this repository to your computer
2. Open the RStudio project file
3. Open the `index.Rmd` [R Markdown file](https://rmarkdown.rstudio.com/) in RStudio
4. Install any required packages
6. Click `Build > Build Book` to generate the processed data and build the website in `docs/`

## Contributors

[List of contributors](https://github.com/trias-project/unified-checklist/contributors)

## License

[MIT License](https://github.com/trias-project/unified-checklist/blob/master/LICENSE) for the code and documentation in this repository. The included data is released under another license.
