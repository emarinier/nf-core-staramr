# phac-nml/staramrnf: Changelog

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## Development

### `Changed`

- Modified the template for input csv file to include a `sample_name` column in addition to `sample` in-line with changes to [IRIDA-Next update] as seen with the [speciesabundance pipeline]
  - `sample_name` special characters will be replaced with `"-"`
  - If no `sample_name` is supplied in the column `sample` will be used
  - To avoid repeat values for `sample_name` all `sample_name` values will be suffixed with the index of the `input` samplesheet.csv

[IRIDA-Next update]: https://github.com/phac-nml/irida-next/pull/678
[speciesabundance pipeline]: https://github.com/phac-nml/speciesabundance/pull/24

## [0.1.0] - 2024-08-14

Initial release of staramrnf, or staramr nextflow pipeline, is a nextflow wrapper of [staramr](https://github.com/phac-nml/staramr/).

`staramr` (AMR) scans bacterial genome contigs against the [ResFinder][resfinder-db], [PointFinder][pointfinder-db], and [PlasmidFinder][plasmidfinder-db] databases (used by the [ResFinder webservice][resfinder-web] and other webservices offered by the Center for Genomic Epidemiology) and compiles a summary report of detected antimicrobial resistance genes. The `star|_`in`staramr` indicates that it can handle all of the ResFinder, PointFinder, and PlasmidFinder databases.

staramrnf follows the `nf-core` pipeline file structure and used the nf-core [template](https://nf-co.re/docs/contributing/pipelines/pipeline_file_structure)

[resfinder-db]: https://bitbucket.org/genomicepidemiology/resfinder_db
[pointfinder-db]: https://bitbucket.org/genomicepidemiology/pointfinder_db
[plasmidfinder-db]: https://bitbucket.org/genomicepidemiology/plasmidfinder_db
[resfinder-web]: http://genepi.food.dtu.dk/resfinder
[0.1.0]: https://github.com/phac-nml/staramrnf/releases/tag/0.1.0
