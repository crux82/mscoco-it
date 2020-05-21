# MSCOCO-it Dataset
## A large scale dataset for Image Captioning in Italian

[MSCOCO](http://cocodataset.org) is a large scale dataset for training of image captioning systems.
It contains(2014 version) more than 600,000 image-caption pairs. It contains training and validation subsets, made respectively of 82, 783 and 40, 504 images, where
every image has 5 human-written annotations in English.

**MSCOCO-it** is derived from the MSCOCO dataset and it is obtained through semi-automatic translation of the dataset 
into Italian. It represents a large-scale dataset for image captioning in Italian. 
**The dataset contains more than 600,000 image-caption pairs derived from the original English dataset.** 
In the paper from (Vinyals et al., 2014), all the image-caption pairs (training+validation / five captions for each image) have been used to train the system, except for a development set of about 2000 images and a test set of about 4000 images that were held out from validation subsets for evaluation. In the following guide to the MSCOCO-it resource, we are going to refer to them as the MSCOCO2K development set and the MSCOCO4K test set.
In the MSCOCO-it resource, two subsets of images along with their annotations taken from, respectively, the MSCOCO2K development set and MSCOCO4K test set and
given that each image has five caption, all the captions (automatically translated from English to Italian) have been manually validated.


The MSCOCO-it dataset is composed of 6 files:

**TRAINING SET**
* `captions_ita_trainingset_train2014.json`: it consists of the annotations for the images
from the original full MSCOCO training set annotations file, except from the ones in the MSCOCO2K
development set and MSCOCO4K test set. All these images and their captions can be used to train a
model.. 
* `captions_ita_trainingset_val2014.json`: it consists of the annotations for the images from
the original full MSCOCO validation set annotations file, except from the ones in the MSCOCO2K
development set and MSCOCO4K test set. All these images and their captions can be used to train a
model. 

**DEVELOPMENT SET**
* `captions_ita_devset_unvalidated.json`:contains the annotations for all the images from
the MSCOCO2K original development set (2000 images held out from the full MSCOCO validation set)
whose Italian captions, translated with Bing, are all NOT manually validated.
* `captions_ita_devset_validated.json`: contains all the validated annotations for a subset of the images from the MSCOCO2K original development set (2000 images held out from the full
MSCOCO validation set). 

**TEST SET:**
* `captions_ita_testset_unvalidated.json`,
* `captions_ita_testset_validated.json`: same file organization as the
development set, referred to a subset of the original MSCOCO4K test set (4000 images held out for
testing from the full MSCOCO validation set).


More details about MSCOCO-it can be found in JCOL??????. Note that this release it is different from the document as regards the partially validated captions that are now validated.


**IMAGES**

Please refear to : http://cocodataset.org/#download
* 2014 Train images [83K/13GB] 
* 2014 Val images [41K/6GB]
### How to cite MSCOCO-it


If you find MSCOCO-it useful for your research, please cite the following paper:

~~~~


DEFINIRE

~~~~


## Download

To download the MSCOCO-it dataset, please refer to [this folder](https://github.com/crux82/mscoco-it/tree/master/mscoco-it)

The resource is developed by the [Semantic Analytics Group](http://sag.art.uniroma2.it) of
the [University of Roma Tor Vergata](http://web.uniroma2.it/home). 
You can download a copy of the dataset (distributed under the CC BY-SA 4.0 license).

DEFINIRE

## Release format

The same format used in the MSCOCO dataset is adopted:

```
{
"info": info, 
"images": [image], 
"annotations": [annotation],
"licenses": [license],
}

info{
"year": int,
"version": str, 
"description": str, 
"contributor": str,
"url": str,
"date_created": datetime,
}

image{
"id": int,
"width": int,
"height": int,
"file_name": str,
"license": int, 
"flickr_url": str,
"coco_url": str,
"date_captured": datetime,
}

license{
"id": int,
"name": str,
"url": str,
}
annotation{
"id": int, 
"image_id": int,
"caption": str,
}

```


## Size of MSCOCO-it

The original MSCOCO dataset contains the following elements:

| Element | Training Set | Validation set |
| -------------- | --------------: | --------------: |
| Images | 82 783 | 40 504 |
| Captions| ~414 000| ~202 000 |


The final MSCOCO-it contains the following elements:
unvalidated (u.) and validated (v.)

|  | #images	| #captions	| #words | 
| --------- | :---------: | :-----: |:---------:  |
|	training u.	|   116 195 | 581 286 | ~6 900 000 | 
|	development	v.| 308 | 1 541 |17 913 |
|	development	u.| 1 696 | 8 486  |~102 000 |
|	test v. | 596 | 2 982   |34 657 |
|	test u. | 3 422  | 17 120 | ~202 000 |
					


## References
T. Lin, M. Maire, S. J. Belongie, L. D. Bourdev, R. B. Girshick, J. Hays,P. Perona, D. Ramanan, P. Doll ́ar, and C. L. Zitnick, “Microsoft COCO:common  objects  in  context,”CoRR,  vol.  abs/1405.0312,  2014.  [Online].Available:  http://arxiv.org/abs/1405.0312

O. Vinyals, A. Toshev, S. Bengio, and D. Erhan, "Show and tell: A neural image caption generator," in 2015 IEEE Conference on Computer Vision and Pattern Recognition (CVPR), June 2015, pp. 3156-3164. [Online]. Available: https://arxiv.org/abs/1411.4555



## Contacts

For any questions or suggestions, you can send an e-mail to <croce@info.uniroma2.it>

More details will be also added to
