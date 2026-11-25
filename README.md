# UWA Prognostics data library - Maintenance work order data

## Maintenance work orders on excavators for NLP - from the UWA PDL

In 2016 the UWA System Health Lab developed a web-based data management system [1] (the PDL) for use by researchers and industry around the world to access suitable datasets to support technical language processing and prognostics. Industry datasets are rarely shared and hardly ever published. By far the most used data sets have been the ones on maintenance work orders. Since the PDL was closed in 2022 we have received numerous requests for these data. We have created this github repo to facilitate distribution.

The data sets described below have been instrumental in developing a number of widely used state-of-the-art tools for dealing with normalisation and annotation of maintenance records. These tools are described below. All their repos contain training data sets.

## MaintNorm - A corpus and benchmark model for lexical normalisation and masking of industrial maintenance short text

​This repository contains the data, models, and code accompanying the paper titled "MaintNorm: A corpus and benchmark model for lexical normalisation and masking of industrial maintenance short text" published in WNUT 2024. [link](https://github.com/nlp-tlp/maintnorm)

## MaintIE -  A Fine-Grained Annotation Schema and Benchmark for Information Extraction from Low-Quality Maintenance Short Texts

This repository contains the data, models, and code accompanying the paper titled MaintIE: A Fine-Grained Annotation Schema and Benchmark for Information Extraction from Low-Quality Maintenance Short Texts published in LREC-Coling 2024. [link](https://github.com/nlp-tlp/maintie)

## MaintKG - Automated Maintenance Knowledge Graph Construction

MaintKG (Maintenance Knowledge Graph) is a framework for automatically constructing knowledge graphs from maintenance work order records. It processes CMMS (Computerized Maintenance Management System) records to create structured, graph-based knowledge representations. [link](https://github.com/nlp-tlp/MaintKG)

## PyPi mudlark library

This library [link](https://pypi.org/project/mudlark/) is designed to provide utilities for cleaning CSV datasets that contain technical language. Mudlark has three main purposes:

- Rapid and easy preprocessing of CSV datasets that have a text column. 
- Exporting a CSV dataset to a JSON file that can be readily imported into QuickGraph, so that you can annotate the textual portion of your CSV dataset.
- Normalising a single piece of text which involves replacing any words appearing in a predefined "corrections dictionary" with suitable replacements. 

The package also includes a useful standalone dictionary of wrong words and their correction.

# Raw data sets

## Excavator work order data set (5 assets, 5485 records)

One of the datasets, the "excavator data set" has been widely used and since the PDL web site was closed down in 2021 we make this data set openly available here in the Git repo. There are 5485 records.

The data set can be downloaded [5485_record_data](data\Excavator_2015_Raw_ForPDL.csv) and used under CC-BY-4.0 licence.

The data set is described in the Hodkiewicz and Batsioudis (2017) paper and represents the 5 units in Shovel Set A.

### Relevant citation 

Hodkiewicz, M.R., Batsioudis, Z., Radomiljac, T. and Ho, M.T., 2017, October. Why autonomous assets are good for reliability–the impact of ‘operator-related component’failures on heavy mobile equipment reliability. In Annual conference of the PHM Society (Vol. 9, No. 1).
[link](https://www.papers.phmsociety.org/index.php/phmconf/article/view/2449)

## Mobile Equipment work order data set (685 assetIDs, 600,000 records)

This large data set (>600k records) was described in the Hodkiewicz and Ho (2016) paper. It has been anonymised.

The data set can be downloaded [600k_data](data\wo-mobileequip-anon-600k.xlsx) and used under CC-BY-4.0 licence.

### Relevant citation
Hodkiewicz, M. and Ho, M.T.W., 2016. Cleaning historical maintenance work order data for reliability analysis. Journal of Quality in Maintenance Engineering, 22(2), pp.146-163.
[link](https://www.emerald.com/jqme/article/22/2/146/252589?casa_token=OHxig0faB3gAAAAA:F0DQ7nH35bfrXBVEMVNts1foEulIWC-M2A7RUei6e6205mjr27ozKUmhxHeSn00DKd4cPw1XyljwvRc)

## Mobile equipment work orders with annotation and KG schema

A 500 record subset of the 600k record set with annotations, train and test sets. Used to create the MWO2KG from annotated MWO data in 2022. This work was done in 2022 and paved the way for the MaintIE work published in 2024.
[code and data link](https://github.com/nlp-tlp/mwo2kg-and-echidna)
[paper link](https://journals.sagepub.com/doi/full/10.1177/1748006X221131128)


## Papers that have used these data sets include the following:

Woods, C., Selway, M., Bikaun, T., Stumptner, M. and Hodkiewicz, M., 2024. An ontology for maintenance activities and its application to data quality. Semantic Web, 15(2), pp.319-352.

Lau, A., Feng, J., Hodkiewicz, M., Woods, C., Stewart, M. and Polpo, A., 2025. Generating Authentic Grounded Synthetic Maintenance Work Orders. IEEE Access.

Bikaun, T.K., French, T., Stewart, M., Liu, W. and Hodkiewicz, M., 2024, May. MaintIE: A fine-grained annotation schema and benchmark for information extraction from maintenance short texts. In Proceedings of the 2024 Joint International Conference on Computational Linguistics, Language Resources and Evaluation (LREC-COLING 2024) (pp. 10939-10951).

Bikaun, T., Hodkiewicz, M. and Liu, W., 2024, March. MaintNorm: A corpus and benchmark model for lexical normalisation and masking of industrial maintenance short text. In Proceedings of the Ninth Workshop on Noisy and User-generated Text (W-NUT 2024) (pp. 68-78).

Bikaun, T., 2024. Automatic knowledge extraction from industrial maintenance short text using deep learning. PhD Thesis, University of Western Australia.

Bikaun, T. and Hodkiewicz, M., 2021, June. Semi-automated estimation of reliability measures from maintenancework order records. In PHM Society European Conference (Vol. 6, No. 1, pp. 9-9).

Bikaun, T., French, T., Hodkiewicz, M., Stewart, M. and Liu, W., 2021, November. LexiClean: An annotation tool for rapid multi-task lexical normalisation. In Proceedings of the 2021 conference on empirical methods in natural language processing: system demonstrations (pp. 212-219).

Yang, Z., Baraldi, P. and Zio, E., 2020. A novel method for maintenance record clustering and its application to a case study of maintenance optimization. Reliability Engineering & System Safety, 203, p.107103.

Payette, M., Abdul-Nour, G., Meango, T.J.M., Diago, M. and Côté, A., 2025. Leveraging failure modes and effect analysis for technical language processing. Machine Learning and Knowledge Extraction, 7(2), p.42.

Kulkarni, A., Terpenny, J. and Prabhu, V., 2023. Leveraging active learning for failure mode acquisition. Sensors, 23(5), p.2818.

Sexton, T. and Fuge, M., 2020. Organizing tagged knowledge: Similarity measures and semantic fluency in structure mining. Journal of Mechanical Design, 142(3), p.031111.

Naqvi, S.M.R., Ghufran, M., Varnier, C., Nicod, J.M., Javed, K. and Zerhouni, N., 2024. Unlocking maintenance insights in industrial text through semantic search. Computers in Industry, 157, p.104083.

Naqvi, S.M.R., Ghufran, M., Meraghni, S., Varnier, C., Nicod, J.M. and Zerhouni, N., 2022. Human knowledge centered maintenance decision support in digital twin environment. Journal of manufacturing systems, 65, pp.528-537.

Naqvi, S.M.R., Ghufran, M., Varnier, C., Nicod, J.M. and Zerhouni, N., 2025. Enhancing semantic search using ontologies: A hybrid information retrieval approach for industrial text. Journal of Industrial Information Integration, 45, p.100835.

Naqvi, S.M.R., Ghufran, M., Meraghni, S., Varnier, C., Nicod, J.M. and Zerhouni, N., 2022, June. Generating semantic matches between maintenance work orders for diagnostic decision support. In Annual Conference of the PHM Society (Vol. 14, No. 1).

Nandyala, A.V., Lukens, S., Rathod, S. and Agarwal, P., 2021, June. Evaluating word representations in a technical language processing pipeline. In Phm society european conference (Vol. 6, No. 1, pp. 17-17).


## Bibliography

1. Sikorska, J., Hodkiewicz, M., D’Cruz, A., Astfalck, L. and Keating, A., 2016, July. A collaborative data library for testing prognostic models. In PHM Society European Conference (Vol. 3, No. 1). [link](https://papers.phmsociety.org/index.php/phme/article/view/1579)

