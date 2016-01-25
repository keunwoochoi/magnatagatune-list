# magnatagatune-list
List of automatic music tagging (using audio) research articles that are evaluated against MagnaTagATune Dataset

## Download
MagnaTagATune is hosted by MIRG of City University London, [here](http://mirg.city.ac.uk/codeapps/the-magnatagatune-dataset)

----------
# Papers
This list is based on google scholar, list of papers that cited the dataset, [google scholar search result](https://scholar.google.co.kr/scholar?hl=en&as_sdt=2005&sciodt=0,5&cites=10394255617419929029&scipsc=)

### 2016
not yet

### 2015
According to [this](https://scholar.google.co.kr/scholar?hl=en&as_sdt=2005&sciodt=0%2C5&cites=10394255617419929029&scipsc=&as_ylo=2015&as_yhi=2015),
 * U Sandouk et al., arxiv: text-processing.
 * U Sandouk et al., arxiv: text-processing.
 * E Colautti et al. : ...written in French but doesn't seem related to audio
(and,)
 * J Nam et al., arxiv: [pdf](http://arxiv.org/abs/1508.04999)
   * title: A deep bag-of-features model for music auto-tagging
   * TODO


### 2014
According to [this](https://scholar.google.co.kr/scholar?hl=en&as_sdt=2005&sciodt=0%2C5&cites=10394255617419929029&scipsc=&as_ylo=2014&as_yhi=2014),
 * D Lim at al., JMLR: about metrics
 * S Duan et al.: survey of tagging techniques
 * G Sageder et al.: not used. onlysubset of MagnaTagATune is used to verity the proposed feature selection that is based on ismir2014 DB.
(and,)
 * S Dieleman et al.:
   * title: End-to-end learning for music audio
   * TODO
 * A Oord et al.: [pdf](http://www.terasoft.com.tw/conf/ismir2014/proceedings/T007_118_Paper.pdf)
   * title: Transfer learning by supervised pre-training for audio-based music classification
   * TODO
 * SN Tran et al.: [pdf](http://mirg.city.ac.uk/blog/wp-content/uploads/2013/09/rbm-features-for-music-similarity.pdf)
   * title: feature preprocessing with RBMs for music similarity learning
 * F Gouton et al.: [pdf](http://arxiv.org/abs/1410.0001)
   * title: on evaluation validity in music autotagging

 
### 2013
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
(and,)
 * S Dieleman et al., ismir:
   * title: Multiscale Approaches To Music Audio Feature Learning
   (TODO)
 * J Stastny et al.: [pdf](http://www.researchgate.net/profile/Jii_Fejfar/publication/257563651_Audio_data_classification_by_means_of_new_algorithms/links/5432b2d00cf225bddcc7c68a.pdf)
   * title: audio data classification by means of new algorithms
   * TODO
 * R Piva: [pdf](http://tesi.cab.unipd.it/42723/)
   * TODO


### 2012
According to [this](https://scholar.google.co.kr/scholar?hl=en&as_sdt=2005&sciodt=0%2C5&cites=10394255617419929029&scipsc=&as_ylo=2012&as_yhi=2012),
 * D wolff et al.: just mentioning.
 * Y Li et al.: not about the DB
 * M Levy: can't get the pdf of it, seems like internal document in the school.
 * L Barrington, PhD thesis: probably not focusing on automatic tagging
 * P Hamel, PhD thesis: written in french. according to its list of contents it would be same results as in the author's ismir paper.
(and,)
 
 * J NAM et al.,: mirex 2012 submission
   * title: mirex 2012 submission: audio classification using sparse feature learning
   * algorithm: RBM + SVM
   * result
    * AROC (ranking): 0.7244,
    * F-measure (annotation): 0.1123

### 2011
According to [this](https://scholar.google.co.kr/scholar?hl=en&as_sdt=2005&sciodt=0%2C5&cites=10394255617419929029&scipsc=&as_ylo=2011&as_yhi=2011),
 * AJ Quinn et al., SIGCHI: a general survey on human computation
 * YH Yang et al. IEEE ASLP: just mentining. experiment was performed on smaller private dataset
 * P Hamel et al.:
   * title: temporal pooling and multiscale learning for automatic annotation and ranking of music audio
   * features: MFCC
   * set: 14600/1629/6499 for training/validation/test
   * tags: not specified, probably using all 160 tags.
   * comparison: against four algirithms [19][17][18][9] (see the references in the paper), all of which use MFCC or 'cepstral transform that is closely related to MFCCs' + spectral features (spectrao centroid, rolloff, flux). They also used GMM of tags, VQ, PAMIR, or individual SVM. 
   * features: 128 MFCC --> 120 principle components, which is called PMSC
     * then mean,var,max,min, 3rd and 4th centered moments -pooling
  * model 1: MLP with L2 regularisation and cross-entropy for loss function. 
  * model 2: multi-time-scale learning 
  * evaluation metric: AUC
  * result:
table 1. 
| algorithm        | AUC           | average training time  |
|:-------------:|:-------------:|:-----:|
| MFCC(20)      | 0.77+-0.04 | 5.9gh |
| MEL-spectrum(128)      | 0.853+-0.008 | 5.2h |
| PMSC(120)      | 0.876+-0.004 | 1.5h |

table 2.

| measure | Manzagol | Zhi | Mandel | Marsyas | mel-spec+PFC | PMSC+PFC | PSMC+MTSL |
| ------------- |:-------------:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
| average AUC-tag | 0.750 | 0.673 | 0.821 | 0.831 | 0.820 | 0.845 | 0.861 |
| average AUC-clip | 0.810 | 0.748 | 0.886 | 0.933 | 0.930 | 0.938 | 0.943 |
| precision@3 | 0.255 | 0.224 | 0.323 | 0.440 | 0.430 | 0.449 | 0.467 |
| precision@6 | 0.194 | 0.192 | 0.245 | 0.314 | 0.305 | 0.320 | 0.327 |
| precision@9 | 0.159 | 0.168 | 0.197 | 0.244 | 0.240 | 0.249 | 0.255 |
| precision@12 | 0.136 | 0.146 | 0.167 | 0.201 | 0.198 | 0.205 | 0.211 |
| precision@15 | 0.119 | 0.127 | 0.145 | 0.172 | 0.170 | 0.175 | 0.181 |
left four: rsults from MIREX 2009

 * J Weston et al., JNMR:
http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/37179.pdf
 * D Wolff, ismir: about similarity metric
 * J Weston et al., arXiv: same as above JNMR, but with tables at within text. 
http://arxiv.org/pdf/1105.5196.pdf
 * M Mann et al., ismir: mood predction in reduced dimensions.
 * D Wolff et al., : about similarity
 * T Aizenberg et al.: about melodic salience modelling
(and,)
 * S Dieleman et al., ismir 2011:
   * title: audio-based music classification with a pretrained convolutional network
   * 
### 2010
According to [this](https://scholar.google.co.kr/scholar?hl=en&as_sdt=2005&sciodt=0%2C5&cites=10394255617419929029&scipsc=&as_ylo=2010&as_yhi=2010),

 * E Law et al., MLKD: learning to tag from open voca labels
 * M Mandel et al.: learning tags that vary withnin a song
 * A Quinn et al.: not related.
 * E Law et al., ECML: learning to tag using noisy labels
 * Y Panagakis et al.: sparse multi-label linear embedding NNTF for automatic music tagging
 * F Maillet: about music recommendation
(and,)
 * K Seyerlehner et al.: [pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.227.6265&rep=rep1&type=pdf)
  * metric: f-score and G-mean (geometric mean of true negative rate and recall)
  * result:

| feature set | f-score | g-mean | f-score (S2) | g-mean(S20 |
| ------------- |:-------------:|:-----:|:-----:|:-----:|
| SAF | 0.3775 | 0.6101 | 0.3962 | 0.6252 |
| BLF-PCA | 0.4163 | 0.6410 | 0.4201 | 0.6439 |

| feature set | avg. f-score | avg. g-mean | avg. f-score (S2) | avg. g-mean(S20 |
| ------------- |:-------------:|:-----:|:-----:|:-----:|
| SAF | 0.1777 | 0.3573 | 0.1932 | 0.3784 |
| BLF-PCA | 0.2136 | 0.4019 | 0.2185 | 0.4081 |

 * J Bergstra et al., ismir 2010: [pdf](https://www.researchgate.net/profile/Michael_Mandel/publication/220723009_Scalable_Genre_and_Tag_Prediction_with_Spectral_Covariance/links/02e7e520c4c292aee4000000.pdf)
    * used few selected tags only

* SR Ness et al.: [pdf](Improving automatic music tag annotation using stacked generalization of probabilistic svm outputs)
  * audio features (+Affinity) + SVM
  * result

global average (table 2)
| algorithm | precision | recall | accuracy | F-score |
| ------------- |:-------------:|:-----:|:-----:|:-----:|
| Audio SVM | 0.307 | 0.315 | 0.969 | 0.311 |
| Affinity SVM | 0.351 | 0.354 | 0.971 | 0.353 |

affinity svm - per-tag evaluation (table 4) (table 3 is ommited as table 4 outperforms in overall)
| number of tags | precision | recall | accuracy | F-score |
| ------------- |:-------------:|:-----:|:-----:|:-----:|
| 20 | 0.418 | 0.691 | 0.856 | 0.518 |
| 30 | 0.346 | 0.671  | 0.862  | 0.453  |
| 40 | 0.394  | 0.397 | 0.914 | 0.395 |
| 50 | 0.369| 0.372 | 0.923 | 0.371 |
| 100 | 0.259 | 0.262 | 0.951 | 0.260 |
| all (188) | 0.184 | 0.186 | 0.971 | 0.185 |


### 2009
N/A



