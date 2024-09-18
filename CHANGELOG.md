# phac-nml/staramrnf: Changelog

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## Development

## [0.1.1] - 2024-09-19

The pipeline has been modified to accept an input (samplesheet) with an optional `sample_name` column. The goal of the `sample_name` is to allow for IRIDA-Next users to modify their output filenames and sample names. Previously, all files and samples were named using the IRIDA-Next ID (for which users do not chose). This modification will not impact the running locally of `staramrnf` because if `sample_name` column is absent (as was the case prior to the release) then the `sample` column will behave as it had previously.

- `sample_name` special characters will be replaced with `"_"`
- If no `sample_name` is supplied in the column `sample` will be used
- To avoid repeat values for `sample_name` all `sample_name` values will be suffixed with the `sample` value. Which is a unique value.

## [0.1.0] - 2024-08-14

Initial release of staramrnf, or staramr nextflow pipeline, is a nextflow wrapper of [staramr](https://github.com/phac-nml/staramr/).

`staramr` (AMR) scans bacterial genome contigs against the [ResFinder][resfinder-db], [PointFinder][pointfinder-db], and [PlasmidFinder][plasmidfinder-db] databases (used by the [ResFinder webservice][resfinder-web] and other webservices offered by the Center for Genomic Epidemiology) and compiles a summary report of detected antimicrobial resistance genes. The `star|_`in`staramr` indicates that it can handle all of the ResFinder, PointFinder, and PlasmidFinder databases.

staramrnf follows the `nf-core` pipeline file structure and used the nf-core [template](https://nf-co.re/docs/contributing/pipelines/pipeline_file_structure)

[resfinder-db]: https://bitbucket.org/genomicepidemiology/resfinder_db
[pointfinder-db]: https://bitbucket.org/genomicepidemiology/pointfinder_db
[plasmidfinder-db]: https://bitbucket.org/genomicepidemiology/plasmidfinder_db
[resfinder-web]: http://genepi.food.dtu.dk/resfinder
[0.1.0]: https://github.com/phac-nml/staramrnf/releases/tag/0.1.0
