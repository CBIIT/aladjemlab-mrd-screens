# aladjemlab-mrd-screens

### General Information

This is a repo containing the R code used to generate the RNAi screen results included in the Nature Manuscript 2023-12-22155B from the Aladjem Lab at the National Cancer Institute/NIH. The R code heavily uses the [cellHTS2 package](https://bioconductor.riken.jp/packages/3.13/bioc/html/cellHTS2.html).

**Title:** Mechanism for local attenuation of DNA replication at double-strand breaks

**Authors:** Robin Sebastian, Eric Sun, Michael Fedkenheuer, Haiqing Fu, SeolKyoung Jung, Bhushan Thakur, Christophe Redon, Gianluca Pegoraro, Andy Tran, Lőrinc Pongor, Jacob Gross, Sara Mosavarpour, Nana Kusi, Rafael Casellas, Anagh Ray, Anjali Dhall, Mirit Aladjem.

**DOI:** TBD

The code for the analysis of the primary RNAi screens is contained in two self-contained subfolders: `DDR` containing the RNAi screen data generated using the DNA Damage Response library, and `Kinome`, containing the RNAi screen data generated using the Kinome library, respectively. 

### DNA Damage Response (DDR) Screen

The `DDR` folder contains:

- An `HTS2_Dataprep.Rmd` script that includes the R and `cellHTS2` code used to prepare the data for the actual `cellHTS2` analysis. This script needs to be run before the `HTS2_Analysis.Rmd` script.
- An `HTS2_Analysis.Rmd` script that runs the `cellHTS2` analysis separately on each cellular feature calculated by Columbus.
- The well level results obtained from the Columbus image analysis server, which is contained in the `measurement_data` subfolder. 
- The `reformatting` subfolder contains library reformatting metadata output by the liquid handler and is used by the `HTS2_Dataprep.Rmd` script to generate the siRNA oligos layouts for the imaging plates used in the screen. 
- A `Description.txt` file that contains details about the screen according to the `cellHTS2`
- A series of subfolders whose name starts with `cellHTS2_output` containing the results of the `cellHTS2` analysis. Each of these subfolder contains data relative to one of the cellular features analyzed and output by Columbus.

The subfolder containing primary RNAi DDR screen results relevant for this manuscript is:

- `spots_edu_pos_median_ratio`: These are data relative to ratio of EdU intensity between the outside and the inside of the pH2AX spots in EdU positive cells.

### Kinome Screen

The `Kinome` folder contains:

- An `01_hts2_dataprep.Rmd` script that includes the R and `cellHTS2` code used to prepare the data for the actual `cellHTS2` analysis. This script needs to be run before the `02_hts2_analysis.Rmd` script.
- An `02_hts2_analysis.Rmd` script that runs the `cellHTS2` analysis separately on each cellular feature calculated by Columbus.
- The well level results obtained from the Columbus image analysis server, which is contained in the `columbus_input` subfolder. 
- The `reformat_metadata` subfolder contains library reformatting metadata output by the liquid handler and is used by the `HTS2_Dataprep.Rmd` script to generate the siRNA oligos layouts for the imaging plates used in the screen. 
- A `Description.txt` file that contains details about the screen according to the `cellHTS2`
- A series of subfolders whose name starts with `cellHTS2_output` containing the results of the `cellHTS2` analysis. Each of these subfolder contains data relative to one of the cellular features analyzed and output by Columbus. 

The subfolder containing primary RNAi Kinome screen results relevant for this manuscript is:

- `spots_edu_pos_median_ratio`: These are data relative to ratio of EdU intensity between the outside and the inside of the pH2AX spots in EdU positive cells.

For information about this repo, please contact [Mirit Aladjem](mailto:mirit.aladjem@nih.gov) or [Gianluca Pegoraro](mailto:gianluca.pegoraro@nih.gov).
