# Datasets

Below are two large scale datasets: TR-News (Turkish) and HU-News (Hungarian). These datasets are intended for the abstractive text summarization task but also contain other fields which can be used in tasks such as topic classification, key phrase extraction and author detection. The datasets contain news URLs but sometimes news content can be copied across other sites causing deduplications. Hence, deduplicated versions (deduplication is performed based on the abstract and content fields) for both datasets are also provided. 

## TR-News

* [Version 1.0.0](https://drive.google.com/file/d/14MESFZp65H3TMvbh8QGoMfXDENdhizn9/view?usp=sharing)

* [Deduplicated](https://drive.google.com/file/d/1QzDQGkVOqsV4VyVryWdQ6Me5BDuwPCP5/view?usp=sharing)

## HU-News

* [Version 1.0.0](https://drive.google.com/file/d/1oiVRY9Nf5USIBpJS3TK7D-hF29Er1xH1/view?usp=sharing)

* [Deduplicated](https://drive.google.com/file/d/1lSVO7g-30Fgax6l3-LPoVRhAy0B2y3eM/view?usp=sharing)

The files can be loaded with pandas

```python
import pandas as pd

train = pd.read_csv("train.tsv","\t")
validation = pd.read_csv("validation.tsv","\t")
test = pd.read_csv("test.tsv","\t")
```
or you can use them over Huggingface Dataset

```python
from datasets import load_dataset
tr_dataset = load_dataset("batubayk/TR-News")
hu_dataset = load_dataset("batubayk/HU-News")
```
# Citation
If you use these datasets, please cite the paper:
    
    @article{10.1007/s10579-021-09568-y, 
    year = {2022}, 
    title = {{Abstractive text summarization and new large-scale datasets for agglutinative languages Turkish and Hungarian}}, 
    author = {Baykara, Batuhan and Güngör, Tunga}, 
    journal = {Language Resources and Evaluation}, 
    issn = {1574-020X}, 
    doi = {10.1007/s10579-021-09568-y},
    pages = {1--35}}
