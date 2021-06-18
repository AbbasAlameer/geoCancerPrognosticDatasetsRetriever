# GEO_CPDR - Gene Expression Omnibus (GEO): Cancer Prognostic Datasets Retriever
Gene Expression Omnibus (GEO): Cancer Prognostic Datasets Retriever (or geo_CPDR) is a Bioinformatics tool for cancer prognostic dataset retrieval from the GEO database.
## Summary
Gene Expression Omnibus (GEO): Cancer Prognostic Datasets Retriever (or geo_CPDR) is a Bioinformatics tool for cancer prognostic dataset retrieval from the GEO database. It requires a GeoDatasets input file listing all GSE dataset entries for a specific cancer (ex. Bladder cancer), obtained as a download from the GEO database.  geo_CPDR functions by applying two heuristic filters to examine individual GSE dataset entries listed in a GEO DataSets input file. The first filter (Prognostic title/abstract filter) flags for prognostic keywords (ex. “prognosis” or “survival”) used by clinical science researchers and present in the title/abstract entries of a GSE dataset. If found, geo_CPDR retrieves those flagged datasets. The second filter (Prognostic Signature filter) filters these datasets further by applying prognostic signature pattern matching (Perl regular expression signatures) to identify if the GSE dataset is a likely prognostic dataset.
## Installation
geo_CPDR can be used on any Linux or macOS machines. To run geo_CPDR, you need to have the following programs installed on your computer:

<p><ul><li>Perl (version 5.30.0 or later)</li></ul></p>
<p><ul><li>cURL (version 7.68.0 or later)</li></ul></p>

By default, Perl is installed on all Linux or macOS operating systems. Likewise, cURL is installed on all macOS versions. cURL may not be installed on Linux and would need to be manually installed through a Linux distribution’s software centre. However, geo_CPDR will install it automatically on Ubuntu linux.
## Data file
The required input file is a GEO DataSets file obtainable as a download, upon querying for any particular cancer (ex. “Bladder cancer”), from the <a href="https://www.ncbi.nlm.nih.gov/geo/">GEO database</a>. 
## Execution instructions
Obtain a GeoDatasets input file for a specific cancer (for example using the search query “Bladder cancer”) and save it in a particular directory in which geo_CPDR is present. Next run geo_CPDR with the following command:

<p><ul>geo_Cancer_Prognostic_Datasets_Retriever -f [INPUT_GEO_FILE] -c [CANCER_TYPE] -o [OUTPUT_FILE]</ul></p>

The output file of geo_CPDR will be found in the ./CANCER_TYPE directory. Help information can be read by typing the following command:  

<p><ul>geo_Cancer_Prognostic_Datasets_Retriever --help</ul></p>

## License
All the code is licensed under the <a href="http://www.gnu.org/licenses/gpl-2.0-standalone.html">GNU General Public License, version 2 (GPLv2).</a> 
## Contact
geo_CPDR was developed by <a href="http://kuweb.ku.edu.kw/biosc/People/AcademicStaff/Dr.AbbasAlameer/index.htm">Abbas Alameer</a> (abbas.alameer(AT)ku.edu.kw) at the Bioinformatics and Molecular Modelling Group of <a href="http://kuweb.ku.edu.kw/ku/index.htm">Kuwait University</a>.

## Support
<address>For support of geo_CPDR, please email <a href="mailto:abbas.alameer@ku.edu.kw">Abbas Alameer.</a></address>
