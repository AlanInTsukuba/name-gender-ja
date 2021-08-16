# Gender classification of given names for Japanese text

## Introduction

According to the Japan National Census, more than 40% of repondents who give their occupation as designer are women. This has been true since the 1990 census. On the other hand, the share of creators listed on Japanese registered designs who are women is unknown, perhaps around 10%. This project aims to quantify this share by developing name-gender data resources for estimating the genders of creators.

Three types of data resources are in development:

#### 1. Individually searched given names selected from persons listed in Japanese registered designs

Registered designs published by the Japan Patent and Trademark Office (JPO) list persons in three roles: 1) examiners, 2) agents, and 3) creators. One approach to identifying genders of given names is to search for actual persons with those names and record names and either disclosed or perceived binary genders. While this can provide maximal coverage of names listed in registered designs, it is not clear whether or not this data can be subjected to statistical tests and can be applied to other name collections.

#### 2. Collections of given names obtained from internet sources

So far, two kinds of internet sources have been indentified that can be used for statistical estimation of gender based on given names. The first kind is gender-specific Wikipedia categories. The second kind is gender-specific sports rosters, particularly marathon rosters. Being more general population samples, they should lend themselves to statistical testing and application to other name collections

#### 3. Gender estimator based on ending characters

The given names collections are used to generate classification rules using the ending characters similar to those used by <a href="#LariviereEtal2013">Larivière et al (2013)</a> but with Japanese Kanji characters.

## Ethics and privacy

## Background

Research into gender disparities requires the ability to code the genders of persons in sample sets. Several studies have used gender specificity of given names to estimate these persons.

<a href="#WhittingtonSmithDoerr2008">Whittington and Smith-Doerr (2008)</a> code subjects using their given names based on common name lists and background searching. Beyond noting that the percentage of women in their sample is proprotionate to other comparable samples, they provide no detail or validation of their coding.

<a href="#LariviereEtal2013">Larivière et al (2013)</a> classify Romanized Korean and Japanese given names based on US Census lists (https://www.census.gov/genealogy/www/data/1990surnames/names_files.html, currently https://www.census.gov/topics/population/genealogy/data/1990_census/1990_census_namefiles.html) Wikipedia lists and categories: http://en.wikipedia.org/wiki/List_of_Korean_given_names and http://en.wikipedia.org/wiki/Category:Korean_given_names for Korean, and http://en.wikipedia.org/wiki/Category:Japanese_given_names and http://en.wikipedia.org/wiki/Japanese_name for Japanese. Korean and Japanese names not matched in universal lists are classified using series of rules, notably name endings. Genders for Chinese names are manually coded by native speakers from China who used personal knowledge of Chinese names supplemented by web searches on Google Images and Facebook. <a href="#LariviereEtal2013">Larivière et al (2013)</a> apply this classification methodology to gender disparities in science; <a href="#SugimotoEtal2015">Larivière et al (2013)</a> apply it to gender disparities in patenting.

<a href="#DelixusNWBC2012">Delixus, Inc. and National Women’s Business Council (2012)</a> use a popular names web site, http://www.20000-names.com/, to classify Japanese, Korean and Chinese names. They use popular names data books authored by Nancy Man for American names. These latter books were formerly available at https://www.smashwords.com/.

## References
<a id="DelixusNWBC2012">Delixus, Inc. and National Women’s Business Council (2012)</a> Intellectual Property and Women Entrepreneurs. <https://cdn.www.nwbc.gov/wp-content/uploads/2018/02/27192725/Qualitative-Analysis-Intellectual-Property-Women-Entrepreneurs-Part-1.pdf> (accessed 16 August 2021)

<a id="LariviereEtal2013">Larivière, Vincent, Chaoqun Ni, Blaise Cronin, and Cassidy R. Sugimoto (2013).</a> "Global Gender Disparities in Science." Nature (London), 504(7479), pp. 211-213, doi:10.1038/504211a. Supplementary information.

<a id="MullerEtAl2019">Müller, Daniel, Pratiksha Jain, and Yieh-Funk Te. (2019)</a> "Augmenting data quality through high-precision gender categorization." Journal of Data and Information Quality (JDIQ) 11(2):1-18. doi:10.1145/3297720

<a id="SugimotoEtal2015">Sugimoto, Cassidy R., Chaoqun Ni, Jevin D. West, Vincent Larivière (2015)</a> The Academic Advantage: Gender Disparities in Patenting. PLoS ONE 10(5): e0128000. doi:10.1371/journal.pone.0128000

<a id="WhittingtonSmithDoerr2008">Whittington, Kjersten Bunker, and Laurel Smith-Doerr (2008)</a> “WOMEN INVENTORS IN CONTEXT: Disparities in Patenting across Academia and Industry.” Gender and Society, 22(2):194–218. JSTOR, www.jstor.org/stable/27821633. Accessed 13 Aug. 2021.