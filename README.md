# magnatagatune-list
List of automatic music tagging (using audio) research articles that are evaluated against MagnaTagATune Dataset

# Information
## Download
MagnaTagATune is hosted by MIRG of City University London, [here](http://mirg.city.ac.uk/codeapps/the-magnatagatune-dataset)

# Papers
This list is based on google scholar, list of papers that cited the dataset, [google scholar search result](https://scholar.google.co.kr/scholar?hl=en&as_sdt=2005&sciodt=0,5&cites=10394255617419929029&scipsc=)

## 2016
not yet

## 2015
According to [this](https://scholar.google.co.kr/scholar?hl=en&as_sdt=2005&sciodt=0%2C5&cites=10394255617419929029&scipsc=&as_ylo=2015&as_yhi=2015),
 * U Sandouk et al., arxiv: text-processing.
 * U Sandouk et al., arxiv: text-processing.
 * E Colautti et al. : ...written in French but doesn't seem related to audio

## 2014
According to [this](https://scholar.google.co.kr/scholar?hl=en&as_sdt=2005&sciodt=0%2C5&cites=10394255617419929029&scipsc=&as_ylo=2014&as_yhi=2014),
 * D Lim at al., JMLR: about metrics
 * S Duan et al.: survey of tagging techniques
 * G Sageder et al.: not used. onlysubset of MagnaTagATune is used to verity the proposed feature selection that is based on ismir2014 DB.

## 2013
According to [this](https://scholar.google.co.kr/scholar?hl=en&as_sdt=2005&sciodt=0%2C5&cites=10394255617419929029&scipsc=&as_ylo=2013&as_yhi=2013),
 * D Wolff et al. : similarity
 * J Watson et al., arxiv: proposing an algorithm for ranking prediction.
   * set: 16k for training, 160 tags (probably top-160 popular tags)
   * feature: 104-dim MFCC, 100-dim embedding dimension
   * result

| algorithm        | precision@1           | precision@3  |
| ------------- |:-------------:| -----:|
| k-nn      | 39.4% | 28.6% |
| k-nn (Wsabie space)      | 45.2% | 31.9% |
| Wsabie      | 48.7% | 37.5% |
| Affinity Weighted Embedding      | 52.7% | 39.2% |

 * JA Burgoyne et al., ismir: just mentioning.

## 2012
According to [this](https://scholar.google.co.kr/scholar?hl=en&as_sdt=2005&sciodt=0%2C5&cites=10394255617419929029&scipsc=&as_ylo=2012&as_yhi=2012),
 * D wolff et al.: just mentioning.
 * Y Li et al.: not about the DB
 * M Levy: can't get the pdf of it, seems like internal document in the school.
 * L Barrington, PhD thesis: probably not focusing on automatic tagging
 * P Hamel, PhD thesis: written in french. according to its list of contents it would be same results as in the author's ismir paper.
 


