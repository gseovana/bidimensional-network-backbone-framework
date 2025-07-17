# A Network-Driven Framework for Bidimensional Analysis of Information Dissemination on Social Media Platforms

This repository provides the code and data to reproduce the results presented in the paper:

**"A Network-Driven Framework for Bidimensional Analysis of Information Dissemination on Social Media Platforms"**<br>
Geovana S. Oliveira, João Pedro Lobo, Otávio Venâncio, Vinícius da F. Vieira, Jussara M. Almeida, Ana P. C. Silva, Ronan S. Ferreira and Carlos H. G. Ferreira<br>
To appear in Journal of Systems Information, 2025.


## Description

This repository supports full reproducibility of the study by providing:

1. Fully documented source code covering:
   - Data preprocessing  
   - Backbone extraction  
   - Edges classification  
   - Community detection  
   - Topic modeling  
2. Ready-to-run Jupyter notebooks with step-by-step guidance  
3. The backbone structures and interaction networks used in both case studies

## Repository Structure

All scripts for executing the experiments are organized in subdirectories of this repository. The entire pipeline is implemented using Jupyter notebooks, which are structured to reflect the main stages of our framework: data preprocessing, backbone extraction, classification, community detection, and topic modeling.

We provide preprocessed versions of the datasets used in the study — including backbone graphs, interaction networks, structural features, and community assignments — organized in dedicated folders for each case study.

📁 The structure is organized into two main case studies:

├── /Telegram/<br>
│ ├── /communities/<br>
│ ├── /edgelist/<br>
│ ├── /figs/<br>
│ ├── /topic_analysis/<br>
│ ├── 1 - Network Generator.ipynb <br>
│ ├── 2 - Edge Classifier and Characterization.ipynb <br>
│ ├── 3 - Community Detection.ipynb <br>
│ ├── 4 - Topic Analysis.ipynb <br>
│<br>
├── /Twitter/ <br>
│ ├── /communities/ <br>
│ ├── /dataset/ <br>
│ ├── /figs/ <br>
│ ├── /networks/ <br>
│ ├── 1 - Network Generator.ipynb<br>
│ ├── 2 - Edge Classifier and Analysis.ipynb<br>
│ ├── 3 - Community Detection.ipynb<br>
│ ├── 4 - Topic Analysis.ipynb<br>
│ └── topology.ipynb <br>

## System Configuration

The experiments presented in this repository involve the processing of large-scale interaction networks and derived graph structures. Given the size and complexity of the datasets — including multi-million edge graphs — certain stages of the pipeline (e.g., backbone extraction, community detection, topic modeling) require substantial computational resources.

All results reported in the paper were obtained using the following hardware setup:

- **Processor type**: 2x Intel Xeon Gold 6130 CPU @ 2.10 GHz (16 cores per socket)
- **RAM**: 384 GB DDR-4 Dual Rank 2666 MHz
- **Storage**: 8x HD 1 TB, SAS 12 Gb/s, 2.5”, 7.200 rpm 2x SSD 480 GB, SATA 6 Gb/s, 2.5”
- **GPU Accelerator**: 2x NVIDIA Tesla V100 PCIe 16 GB

> Several steps involve loading large graphs entirely into memory or performing costly matrix operations (e.g., during topic modeling). Attempting to run the full pipeline on machines with limited RAM or CPU threads may result in memory errors or long processing times.

Although most post-processing and classification stages can be executed on a standard workstation, we recommend using a machine with at least **128 GB of RAM** to ensure smooth replication of all components in both case studies.

To facilitate reproducibility under constrained hardware, we provide precomputed intermediate results (e.g., backbone graphs, community assignments, extracted topics), which can be directly loaded in the Jupyter notebooks.

## Datasets and Code

> ⚠️ Due to ethical and legal constraints, we do **not** include raw textual data. However, all intermediate outputs needed for replication (e.g., structural features, backbones, community labels, topic distributions) are included, and the entire modeling pipeline can be executed from these.

Because of storage limitations on GitHub, the full datasets and precomputed intermediate files used in this study are hosted externally on Google Drive.

**➤ Download link**: Google Drive - https://drive.google.com/drive/folders/1ZkhXcBparNYiJVNT91FM6o53PakmFLzT?usp=sharing

The data folders in the Google Drive are already structured correctly. After downloading, no additional reorganization is needed — the files will work with the provided notebooks as-is.

## References

The following publications support or inspired key components of this work. Please cite them if you use this repository or build upon its methodology:

**Backbone Extraction Algorithm**
- Marcaccioli, R., & Livan, G. (2019). *A Pólya urn approach to information filtering in complex networks*. Nature Communications, 10, 745. https://doi.org/10.1038/s41467-019-08667-3 <br>
➤ Link to download: https://www.mathworks.com/matlabcentral/fileexchange/69501-pf

**Telegram Dataset**
- Venâncio, O. R., Ferreira, C. H. G., Almeida, J. M., & da Silva, A. P. C. (2024). *Unraveling User Coordination on Telegram: A Comprehensive Analysis of Political Mobilization during the 2022 Brazilian Presidential Election*. Proceedings of the International AAAI Conference on Web and Social Media, 18(1), 1545–1556. https://doi.org/10.1609/icwsm.v18i1.31408

**Twitter Dataset**
- Fonseca, L. G. G. da, Ferreira, C. H. G., & Reis, J. C. S. dos. (2024). *The Role of News Source Certification in Shaping Tweet Content: Textual and Dissemination Patterns in Brazil's 2022 Elections*. In: Proceedings of the 20th Brazilian Symposium on Information Systems (SBSI), Juiz de Fora, MG. Sociedade Brasileira de Computação.

## Contact

For questions, feedback, or collaboration inquiries, please contact:

**Geovana Silva de Oliveira**  
<geovana.so@aluno.ufop.edu.br> | <gsoliveira2406@gmail.com>

**Carlos H. G. Ferreira**  
<chgferreira@ufop.edu.br>
