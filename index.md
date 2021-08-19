# Gender classification of given names for Japanese text

## Introduction

According to the Japan National Census, more than 40% of repondents who give their occupation as designer are women. This has been true since the 1990 census. On the other hand, the share of creators listed on Japanese registered designs who are women is unknown, perhaps around 10%. This project aims to quantify this share by developing name-gender data resources for estimating the genders of creators.

Three types of data resources are in development:

#### 1. Individually searched given names selected from persons listed in Japanese registered designs

Registered designs published by the Japan Patent and Trademark Office (JPO) list persons in three roles: 1) examiners, 2) agents, and 3) creators. One approach to identifying genders of given names is to search for actual persons with those names and record names and either disclosed or perceived binary genders. While this can provide maximal coverage of names listed in registered designs, it is not clear whether or not this data can be subjected to statistical tests and can be applied to other name collections. (Dataset not released)

#### 2. Collections of given names obtained from internet sources

So far, two kinds of internet sources have been indentified that can be used for statistical estimation of gender based on given names. Being more general population samples, they should lend themselves to statistical testing and application to other name collections. The first kind is gender-specific Wikipedia categories (dataset to be released). The second kind is gender-specific sports rosters, particularly marathon rosters. (Release of dataset under consideration.)

#### 3. Gender estimator based on ending characters

The given names collections are used to generate classification rules using the ending characters similar to those used by <a href="#LariviereEtal2013">Larivière et al (2013)</a> but with Japanese Kanji characters. (Release of dataset under consideration.)

## Ethics and privacy

For individually searched given names, binary genders were assigned based on declared or revealed genders in Facebook profiles, Wikipedia biographies, or gender-specific sports rosters; inferred genders from obituaries and the like; or perceived genders from labeled photographs. Facebook profiles for which genders were hidden were excluded even if gender could be perceived from the profile photograph as hiding gender can be treated as explicitly prohibiting use of the profile for gender identification.

## Background

Research into gender disparities requires the ability to code the genders of persons in sample sets. This section reviews studies that code or classify gender based on given names. These studies are listed here chronologically by date of first publication.

### Name-matching using European alphabets

<a href="#ButtonsToBiotech1999">United States Patent and Trademark Office (1999)</a>, in its Buttons to Biotech report, matches the given names of inventors against a file of female-only given names. Patents having an inventor with a matching given name were classified as woman-inventor patents. Patents having inventors with given names that are male-only or ambiguous are assumed to be male.

<a href="#WhittingtonSmithDoerr2008">Whittington and Smith-Doerr (2008)</a> code subjects using their given names based on common name lists and background searching. Beyond noting that the percentage of women in their sample is proprotionate to other comparable samples, they provide no detail or validation of their coding.

<a href="#DelixusNWBC2012">Delixus, Inc. and National Women’s Business Council (2012)</a> use a popular names web site, http://www.20000-names.com/, to classify Japanese, Korean and Chinese names. They use popular names data books authored by Nancy Man for American names. These latter books were formerly available at https://www.smashwords.com/.

<a href="#LariviereEtal2013">Larivière et al (2013)</a> classify Romanized Korean and Japanese given names based on US Census lists (https://www.census.gov/genealogy/www/data/1990surnames/names_files.html, currently https://www.census.gov/topics/population/genealogy/data/1990_census/1990_census_namefiles.html) Wikipedia lists and categories: http://en.wikipedia.org/wiki/List_of_Korean_given_names and http://en.wikipedia.org/wiki/Category:Korean_given_names for Korean, and http://en.wikipedia.org/wiki/Category:Japanese_given_names and http://en.wikipedia.org/wiki/Japanese_name for Japanese. Korean and Japanese names not matched in universal lists are classified using series of rules, notably name endings. Genders for Chinese names are manually coded by native speakers from China who used personal knowledge of Chinese names supplemented by web searches on Google Images and Facebook. <a href="#LariviereEtal2013">Larivière et al (2013)</a> apply this classification methodology to gender disparities in science; <a href="#SugimotoEtal2015">Larivière et al (2013)</a> apply it to gender disparities in patenting.

<a href="#MartinezEtal2016">Martinez, Gema Lax, Julio Raffo, Kaori Saito (2016)</a> review the methodological approaches to attributing gender and develop a gender-name dictionary with worldwide coverage. Relevent to the current research, in addition to making use of popular name lists on Wikipedia, they use an ad-hoc list of Chinese, Indian, Japanese and Korean names that was created by WIPO staff native speakers.

<a href="#JensenKovacsSorenson2018">Jensen, Kyle, Balázs Kovács, and Olav Sorenson (2018)</a> determine the probable gender of inventors in US utility patent applications using given name gender distributions available from the US Social Security Administration and from two commercial databases, GenderAPI and genderize.io. They associated a given name with a single gender if the name was associated at least 95% of the time with that gender.

<a href="#MullerEtAl2019">Müller, Jain, and Te (2019)</a> use a dataset provided by a Swiss automobile insurance company that contains 1.88 million women's and 2.18 million men's names from 172 nationalities. These names contain 99,000 (5.3%) uniquely female and 111,000 (5.1%) uniquely male given names. (In this research, gender-specific Japanese marathon rosters contain about 40% unique names for both women and men.) They define unisex as names found for both genders with the probably of each being less than 95%.



## References
<a id="DelixusNWBC2012">Delixus, Inc. and National Women’s Business Council (2012)</a> Intellectual Property and Women Entrepreneurs. <https://cdn.www.nwbc.gov/wp-content/uploads/2018/02/27192725/Qualitative-Analysis-Intellectual-Property-Women-Entrepreneurs-Part-1.pdf> (accessed 16 August 2021)

<a id="JensenEtAl2018">Jensen K, Kovács B, Sorenson O. (2018)</a> Gender differences in obtaining and maintaining patent rights. Nat Biotechnol. 2018 Apr 5;36(4):307-309. doi: 10.1038/nbt.4120. PMID: 29621210.

<a id="JensenKovacsSorenson2018">Jensen, Kyle, Balázs Kovács, and Olav Sorenson (2018)</a> "Gender Differences in Obtaining and Maintaining Patent Rights." Nature Biotechnology, vol. 36, no. 4, 2018, pp. 307-309. [accessed 9 December 2020] https://www-proquest-com.ezproxy.tulips.tsukuba.ac.jp/docview/2021770129?pq-origsite=summon

<a id="LariviereEtal2013">Larivière, Vincent, Chaoqun Ni, Blaise Cronin, and Cassidy R. Sugimoto (2013).</a> "Global Gender Disparities in Science." Nature (London), 504(7479), pp. 211-213, doi:10.1038/504211a. Supplementary information.

<a id="MartinezEtal2016">Martinez, Gema Lax, Julio Raffo, Kaori Saito (2016)</a> Identifying the gender of PCT inventors. Economic Research Working Paper No. 33. World Intelectual Property Organization. [accessed 19 August 2021] https://www.wipo.int/publications/en/details.jsp?id=4125&plang=EN

<a id="MartinezEtal2021">Martinez, Gema Lax, Helena Saenz de Juano-i-Ribes, Deyun Yin, Bruno Le Feuvre, Intan Hamdan-Livramento, Kaori Saito, Julio Raffo (2021)</a> Expanding the World Gender-Name Dictionary: WGND 2.0. Economic Research Working Paper No. 64. World Intelectual Property Organization. [accessed 19 August 2021] https://www.wipo.int/edocs/pubdocs/en/wipo_pub_econstat_wp_64.pdf

<a id="MullerEtAl2019">Müller, Daniel, Pratiksha Jain, and Yieh-Funk Te. (2019)</a> "Augmenting data quality through high-precision gender categorization." Journal of Data and Information Quality (JDIQ) 11(2):1-18. doi:10.1145/3297720

<a id="SugimotoEtal2015">Sugimoto, Cassidy R., Chaoqun Ni, Jevin D. West, Vincent Larivière (2015)</a> The Academic Advantage: Gender Disparities in Patenting. PLoS ONE 10(5): e0128000. doi:10.1371/journal.pone.0128000

<a id="TangEtal2011">Tang, Cong, Keith Ross, Nitesh Saxena, Ruichuan Xu (2011)</a> What's in a Name: A Study of Names, Gender Inference, and Gender Behavior in Facebook. In Jianliang Xu, Ge Yu, Shuigeng Zhou, and Rainer Unland (Eds.), Database Systems for Adanced Applications. DASFAA 2011. Lecture Notes in Computer Science, vol 6637. (pp. 344–356). Springer Berlin Heidelberg. [accessed 19 August 2021] https://doi-org.ezproxy.tulips.tsukuba.ac.jp/10.1007/978-3-642-20244-5_33

<a id="ButtonsToBiotech1999">United States Patent and Trademark Office (1999)</a>. Buttons to Biotech. 1996 Update Report with supplemental data through 1998. https://www.uspto.gov/web/offices/ac/ido/oeip/taf/wom_98.pdf (accessed 17 August 2021)

<a id="WhittingtonSmithDoerr2008">Whittington, Kjersten Bunker, and Laurel Smith-Doerr (2008)</a> “WOMEN INVENTORS IN CONTEXT: Disparities in Patenting across Academia and Industry.” Gender and Society, 22(2):194–218. JSTOR, www.jstor.org/stable/27821633. Accessed 13 August 2021.