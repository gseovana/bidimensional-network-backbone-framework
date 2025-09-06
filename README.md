# A Network-Driven Framework for Bidimensional Analysis of Information Dissemination on Social Media Platforms

This repository provides the code and data to reproduce the results presented in the paper:

**"A Network-Driven Framework for Bidimensional Analysis of Information Dissemination on Social Media Platforms"**<br>
Geovana S. Oliveira, João Pedro Lobo, Otávio Venâncio, Vinícius da F. Vieira, Jussara M. Almeida, Ana P. C. Silva, Ronan S. Ferreira and Carlos H. G. Ferreira<br> 
**DOI: 0.5753/jis.2025.5526**<br><br>
Accepted and published in Journal on Interactive Systems, 2025.


## Description

This repository enables full reproducibility of our study by providing:

1. **Well-documented source code** that implements all major steps of the analysis pipeline:
   - Data preprocessing  
   - Backbone extraction  
   - Edge classification  
   - Community detection  
   - Topic modeling  

2. **Ready-to-run Jupyter notebooks** with step-by-step instructions for each stage of the workflow
3. **External access to all required data artifacts**, including backbone structures and interaction networks for both case studies, available through a shared Google Drive folder

## Repository Structure
This repository contains only the Jupyter notebooks used in our experiments. Due to storage limitations, the datasets and intermediate outputs are hosted externally.
The notebooks are organized into two main case studies: **Telegram** and **Twitter**

Each case study has its own subdirectory containing the corresponding notebooks:
```bash
├── Telegram/
│├── 1 - Network Generator.ipynb  
│├── 2 - Edge Classifier and Characterization.ipynb  
│├── 3 - Community Detection.ipynb  
│├── 4 - Topic Analysis.ipynb 
│
├──Twitter/
│├── 1 - Network Generator.ipynb  
│├── 2 - Edge Classifier and Analysis.ipynb  
│├── 3 - Community Detection.ipynb  
│├── 4 - Topic Analysis.ipynb  
│├── topology.ipynb
```
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

## Datasets and Intermediate Outputs
> ⚠️ Due to ethical and legal constraints, we do **not** include raw textual data. However, all intermediate outputs needed for replication (e.g., structural features, backbones, community labels, topic distributions) are included, and the entire modeling pipeline can be executed from these.

All required datasets and intermediate outputs — including backbone graphs, interaction networks, structural features, community assignments, and topic distributions — are hosted externally on Google Drive. 

➤ Download link: Google Drive - https://drive.google.com/drive/folders/1ZkhXcBparNYiJVNT91FM6o53PakmFLzT?usp=sharing

 ### How to use the data
To run the notebooks properly:

1. Download the contents of the Telegram/ and Twitter/ folders from the Google Drive link above.
2. Place each folder (Telegram and Twitter) in the same directory as this repository, alongside the corresponding notebook folders.
3. The folder structure should look like this:
```bash
├── /Telegram/
│ ├── /communities/
│ ├── /edgelist/
│ ├── /topic_analysis/
│ ├── 1 - Network Generator.ipynb 
│ ├── 2 - Edge Classifier and Characterization.ipynb
│ ├── 3 - Community Detection.ipynb
│ ├── 4 - Topic Analysis.ipynb
│
├── /Twitter/ 
│ ├── /communities/
│ ├── /dataset/ 
│ ├── /networks/ 
│ ├── 1 - Network Generator.ipynb
│ ├── 2 - Edge Classifier and Analysis.ipynb
│ ├── 3 - Community Detection.ipynb
│ ├── 4 - Topic Analysis.ipynb
│ └── topology.ipynb
```
No further configuration or reorganization is required.

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
