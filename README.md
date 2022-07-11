# BSc-Project-Endothelial-development-in-mouse-embryo
## Can somites give rise to endothelia in the developing moue emrbyo?

### Background
Cell lineage describes the developmental history of a cell - studying this framework allows us to understand the causes and mechanisms of cellular diversity, both in healthy and diseased organisms.
According to the previous research on avian embryos, the somites can give rise to endothelium, but the evidence is questionable (Pardanaud et al., 1996).
Recent mouse grafting experiments shown no contribution of somites to Dorsal Aorta (Wilson et al., unpublished).

### Aim
To investigate if somites can make endothelia in the developing mouse embryo by computational analysis, using scRNA-seq data of E8.0-E8.5 stage cells from Mouse Gastrulation Atlas (Pijuan-Sala et al, 2019; Griffiths and Lun, 2020).

### Project Description
To explore the relationship between somites and enodthelia series of analysis was performed. Those included Mouse Gastrulation data selection and preparation, entropy calculation for cell fate probability analysis, RNA velocity and trajectory analysis and Waddington analysis.

#### Cell fate probability analysis
Palantir (Python) allows analysis of scRNA-seq by pseudotime modelling in terms of each lineage probability of reaching assigned terminal state and by measurment of plasticity of cells localised along this trajectory (Setty et al., 2019).
Pseudotime is decribed as localisation of cells on traectory leading from one cell state to another and is modelled by calculation of entropy, based on cell transcriptome (Setty et al., 2019). Analysis was performed jointly in R and Python.

#### RNA velocity analysis
RNA velocity considers transcription as a dynamic process and bases the analysis on transcription, splicing and degradation rates for each gene in a cell (Amezquita et al., 2019; Bergen et al., 2020; La Manno et al., 2018; Rue-Albrecht, Lun and Soneson, 2020). Analysis was performed in R and involved selected cells of interest as well as entire data.

#### Trajectory analysis
Transcriptome data of each cell in the lineages can be very variable, Slingshot (Street et al., 2018) characterizes those lineages to draw "a path through high-dimmentional expression space". Initially, trajectory analysis invovles use of minimum spanning tree, which is based on cell clusters and identifies the most important parts of the global lineage structure in a stable manner. Similar cells are connected within the trajectory, which can also be branched (Amezquita et al., 2019; Street et al., 2018). 

#### Waddington - Optimal Transport
Waddington-OT - a methematical model of Optimal Transport, uses temporal coupling of cells to minimize kinetic energy in gene expression space and is based on Waddington metaphor of marbeles rolling over the landscape, which represents the development. Waddington-OT is based on inference of probability of cells possessing particular origin and fate, by analysing the distribution of this porbablitie at selected times (Schiebinger et al., 2019, Wagner and Klein, 2020). Entire analysis was perormed using R.

### Credit
This BSC Hons Project was performed under guidance and supervision of Val Wilson Research Groupy - Centre for Regenerative Medicine, Edinburgh, Scotland.

### References
Amezquita, R. A., Lun, A. T. L., Becht, E., Carey, V. J., Carpp, L. N., Geistlinger, L., Marini, F., Rue-Albrecht, K., Risso, D., Soneson, C., Waldron, L., Pagѐs, H., Smitch, M. L., Huber, W., Morgan, M., Gottardo, R. and Hicks, S. C. 2019. Orchestrating single-cell analysis with Bioconductor. Nature methods, 17, 137-145.

Bergen, V., Lange, M., Peidli, S., Wolf, F. A. and Theis, F. J. 2020. Generalizing RNA velocity to transient cell states through dynamic modelling. Nature Biotechnology, 38, 1408-1414.

Griffiths, J. and Lun, A. 2020. MouseGastrulationData: Single-Cell Transcriptomics Data across Mouse Gastrulation and Early Organogenesis. R package version 1.4.0, https://github.com/MarioniLab/MouseGastrulationData.

La Manno, G., Soldatov, R., Zeisel, A., Braun, E., Hochgerner, H., Petukhov, V., Lidschreiber, K., Kastriti, M. E., Lönnerberg, P. Furlan, A., Fan, J., Borm, L. E., Liu, Z., van Bruggen, D., Guo, J, He, X., Barker, R., Sundström, E., Castelo-Branco, G., Cramer, P., Adameyko, I., Linnarsson, S. and Kharchenko, P. V. 2018. RNA velocity of single cells. Nature, 560, 494-498.

Pardanaud, L., Luton D., Prigent, M., Bourcheix, L-M., Catala, M. and Dierelen-Liѐvre, F. 1996. Two distinct endothelial lineages in ontogeny, one of them related to hematopoiesis. Development 122, 1363-1371.

Pijuan-Sala, B., Griffiths, A., Guibentif, C., Hiscock, T. W., Jawaid, W., Calero-Nieto, F. J., Mulas, C., Ibarra-Soria, X., Tyser, R. C. V., Lee Lian Ho., D., Reik, W., Srinivas, S., Simons, B. D., Nichols, J., Marioni, J. C. and Göttgens, B. 2019. A single-cell molecula map of mouse gastrulation and early organogenesis. Nature 566, 490-495. 

Rue-Albrecht K., Lun A. and Soneson C. 2020. velociraptor: Toolkit for Single-Cell Velocity. R package version 1.0.0, https://github.com/kevinrue/velociraptor.

Schiebinger, G., Shu, J., Tabaka, M., Cleary, B., Subramanian, V., Solomon, A., Gould, J., Liu, S., Lin, S., Berube, P., Lee, L., Chen, J., Brumbaugh, J., Rigollet, P., Hochedlinger, K., Jaenisch, R., Regev, A. and Lander, E. S. 2019. Optimal-Transport Analysis of Single-Cell Gene Expression Identitifies Developmental Trajectories in Reprogramming. Cell, 176(4), 928-943.

Setty, M., Kiseliovas, V., Levine, J., Gayoso, A., Mazutis, L. and Pe’er, D. 2019. Characterization of cell fate probabilities in single-cell data with Palantir. Nature Biotechnology, 37, 451-460.

Street, K., Risso, D., Fletcher,  R. B., Das, D., Ngai, J., Yosef, N., Purdom, E. and Dudoit, S. 2018. Slingshot: cell lineage and pseudotime inference for single-cell transcriptomics. BMC Genomics, 19, 477. https://doi.org/10.1186/s12864-018-4772-0
Wagner, D. E. and Klein, A. M. 2020. Lineage tracing meets single-cell omics: opportunities and challenges. Nature reviews genetics, 21, 410-427.


