# phac-nml/staramrnf: Changelog

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## 0.1.0 - [TBD]

Initial release of staramrnf, or staramr nextflow pipeline, is a nextflow wrapper of [staramr](https://github.com/phac-nml/staramr/).

`staramr` (*AMR) scans bacterial genome contigs against the [ResFinder][resfinder-db], [PointFinder][pointfinder-db], and [PlasmidFinder][plasmidfinder-db] databases (used by the [ResFinder webservice][resfinder-web] and other webservices offered by the Center for Genomic Epidemiology) and compiles a summary report of detected antimicrobial resistance genes. The `star|*` in `staramr` indicates that it can handle all of the ResFinder, PointFinder, and PlasmidFinder databases.

staramrnf follows the `nf-core` pipeline file structure and used the nf-core [template](https://nf-co.re/docs/contributing/pipelines/pipeline_file_structure)
