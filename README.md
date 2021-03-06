# Multimodal Entity Linking Datasets Benchmark

## 1. Abstract

Multimodal entity linking (MEL) aims to utilize multimodal information to map mentions to corresponding entities defined in knowledge bases. We release three MEL datasets: Weibo-MEL, Wikidata-MEL and Richpedia-MEL, containing 25,602, 18,880 and 17,806 samples from social media, encyclopedia and multimodal knowledge graphs respectively. A MEL dataset construction approach is proposed, including five stages: multimodal information extraction, mention extraction, entity extraction, triple construction and dataset construction. Experiment results demonstrate the usability of the datasets and the distinguishability between baseline models.

## 2. Introduction

Multimodal entity linking (MEL) aims to utilize multimodal information to map mentions to corresponding entities defined in knowledge bases. We release three MEL datasets: Weibo-MEL, Wikidata-MEL and Richpedia-MEL, containing 25,602, 18,880 and 17,806 samples from social media, encyclopedia and multimodal knowledge graphs respectively. A MEL dataset construction approach is proposed, including five stages: multimodal information extraction, mention extraction, entity extraction, triple construction and dataset construction. Experiment results demonstrate the usability of the datasets and the distinguishability between baseline models.

To construct large-scale MEL datasets, we propose a MEL dataset construction approach, including five stages. In **Multimodal Information Extraction**, we select multimodal data sources and extract textual and visual information. In **Mention Extraction**, we extract mentions from textual information and keep the mentions which corresponding entities may exist. In **Entity Extraction**, we query the knowledge bases with the filtered mentions, gather the entity lists, and save the correct entities. In **Triple Construction**, we merge the corresponding mentions and entities into mention-entity (M-E) pairs, and combine them into triples with textual and visual information. Then, we keep the correct triples as the samples of the MEL dataset. Finally, in **Dataset  Construction** stage, we partition the dataset into training set (70%), validation set (10%) and testing set (20%). The overview of the approach is illustrated in figure below.

  ![image-20210704105704949](https://markdown-bluestragglers.oss-cn-beijing.aliyuncs.com/image-20210704105704949.png)

## 3. Visual Information and Knowledge Graph Resources

Due to the large size of the visual information and knowledge graph resources, we deposited these resources in the Baidu Cloud Disk.

Visual information download addresses:
* [Weibo-MEL Visual Information](https://pan.baidu.com/s/1VTzzKXpORziookJiHKwWKw)
* [Wikidata-MEL Visual Information](https://pan.baidu.com/s/1FbhgMZ-w2DdAPLgCBDvKtQ)
* [Richpedia-MEL Visual Information](https://pan.baidu.com/s/1lt-SmWUX5GAmLRNWggDkXQ?from=init#list/path=%2Fsharelink653312845-459959024382112%2Fimage&parentPath=%2Fsharelink653312845-459959024382112)

Knowledge graph download addresses:
* [Wikidata Knowledge Graph for Weibo-MEL and Wikidata-MEL](https://dumps.wikimedia.org/wikidatawiki/entities/latest-all.json.bz2)
* [Richpedia Knowledge Graph for Richpedia-MEL](https://pan.baidu.com/s/1FTEwSV6CystQHT_wgdjYEA)

The extraction codes are 2021.

## 4. Samples of the MEL datasets

### 4.1 Weibo-MEL dataset

**Visual information:**

* ![image-20210703210612299](https://markdown-bluestragglers.oss-cn-beijing.aliyuncs.com/image-20210703210612299.png)

**Textual information:**

* ?????????30???????????????#????????????????????????????????????# ???????????????????????????????????????????????????????????????????????????????????????????????????1990???12?????????????????????????????????????????????????????????????????????1?????????????????????1???????????????4????????????30????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????#????????????????????????# [?????????9???] ??????

**Mention-entity pairs:**

* "?????????": "?????????"
* "??????": "??????????????????????????????????????????"
* "?????????": "????????????????????????????????????"

### 4.2 Wikidata-MEL dataset

**Visual information:**

* ![image-20210703212658556](https://markdown-bluestragglers.oss-cn-beijing.aliyuncs.com/image-20210703212658556.png)

**Textual information:**

* Seattle Mayor Charles L. Smith (left) with Will Rogers, circa 1935.

**Mention-entity pairs:**

* "Charles L. Smith": "Charles L. Smith (Seattle politician)"
* "Will Rogers": "Will Rogers"

### 4.3 Richpedia-MEL dataset

**Visual information:**

* ![image-20210703212710693](https://markdown-bluestragglers.oss-cn-beijing.aliyuncs.com/image-20210703212710693.png)

**Textual information:**

* Washington resigned his commission after the Treaty of Paris in 1783.

**Mention-entity pairs:**

* "Washington": "George Washington"
