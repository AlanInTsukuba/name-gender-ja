# Gender classification of given names for Japanese text

<p class="author"><a href="https://orcid.org/0000-0003-0070-2347" target="_blank">Alan Engel</a><br>Last update: 24 September 2021</p>

## Table of Contents
<ul>
    <li><a href="#Introduction">Introduction</a></li>
    <li><a href="#Ethics">Ethics and privacy</a></li>
    <li><a href="#Background">Background</a>
        <ul>
        <li><a href="#NameMatchingEuropean">Name-matching using European alphabets</a></li>
        <li><a href="#GenderAttributionEastAsian">Gender attribution for East Asian names</a></li></ul></li>
    <li><a href="#Datasets">Datasets</a>
        <ul>
        <li><a href="#IndividualSearches">Individually searched given names (not released)</a></li>
        <li><a href="#JapaneseCelebs">Japanese celebrities</a></li>
        <li><a href="#GivenNamesGenderDataset">Gender-specific given names</a></li>
        <li><a href="#EndCharGenderDataset">Gender-specific end characters</a></li>
        </ul></li>
    <li><a href="#CreatorNamesComparison">Applying datasets to creator names</a></li>
    <li><a href="#Notes">Notes</a></li>
    <li><a href="#References">References</a></li>
 </ul>

## <a id="Introduction">Introduction</a>

There is a compelling need for estimating gender based on given names that are written in Kanji and in Japanese text. Tools for estimating gender would enable research of gender disparities among authors, inventors, designers, politicians, government-certified bidders, licensed professionals and a wide range of other socioeconomic participants. 

Three types of data resources are in development:

#### 1. Individually searched given names selected from persons listed in Japanese registered designs

Registered designs published by the Japan Patent and Trademark Office (JPO) list persons in three roles: 1) examiners, 2) agents, and 3) creators. One approach to identifying genders of given names is to search for actual persons with those names and record names and either disclosed or perceived binary genders. While this can provide maximal coverage of names listed in registered designs, it is not clear whether or not this data can be subjected to statistical tests and can be applied to other name collections. (Dataset not released)

#### 2. Collections of given names obtained from internet sources

So far, two kinds of internet sources have been indentified that can be used for statistical estimation of gender based on given names. Being more general population samples, they should lend themselves to statistical testing and application to other name collections. The first kind is gender-specific Wikipedia categories (dataset to be released). The second kind is gender-specific sports rosters, particularly marathon rosters. (Release of dataset under consideration.)

#### 3. Gender estimator based on ending characters

The given names collections are used to generate classification rules using the ending characters similar to those used by <a href="#LariviereEtal2013">Larivière et al (2013)</a> but with Japanese Kanji characters. (Release of dataset under consideration.)

## <a id="Ethics">Ethics and privacy</a>

For individually searched given names, binary genders were assigned based on declared or revealed genders in Facebook profiles, Wikipedia biographies, or gender-specific sports rosters; inferred genders from obituaries and the like; or perceived genders from labeled photographs. Facebook profiles for which genders were hidden were excluded even if gender could be perceived from the profile photograph as hiding gender can be treated as explicitly prohibiting use of the profile for gender identification.

## <a id="Background">Background</a>

Research into gender disparities requires the ability to code the genders of persons in sample sets. This section reviews studies that code or classify gender based on given names. These studies are listed here chronologically by date of first publication.

### <a id="NameMatchingEuropean">Name-matching using European alphabets</a>

<a href="#ButtonsToBiotech1999">United States Patent and Trademark Office (1999)</a>, in its Buttons to Biotech report, matches the given names of inventors against a file of female-only given names. Patents having an inventor with a matching given name were classified as woman-inventor patents. Patents having inventors with given names that are male-only or ambiguous are assumed to be male.

<a href="#WhittingtonSmithDoerr2008">Whittington and Smith-Doerr (2008)</a> code subjects using their given names based on common name lists and background searching. Beyond noting that the percentage of women in their sample is proprotionate to other comparable samples, they provide no detail or validation of their coding.

<a href="#DelixusNWBC2012">Delixus, Inc. and National Women’s Business Council (2012)</a> use a popular names web site, http://www.20000-names.com/, to classify Japanese, Korean and Chinese names. They use popular names data books authored by Nancy Man for American names. These latter books were formerly available at https://www.smashwords.com/.

<a href="#LariviereEtal2013">Larivière et al (2013)</a> classify Romanized Korean and Japanese given names based on US Census lists (https://www.census.gov/genealogy/www/data/1990surnames/names_files.html, currently https://www.census.gov/topics/population/genealogy/data/1990_census/1990_census_namefiles.html) Wikipedia lists and categories: http://en.wikipedia.org/wiki/List_of_Korean_given_names and http://en.wikipedia.org/wiki/Category:Korean_given_names for Korean, and http://en.wikipedia.org/wiki/Category:Japanese_given_names and http://en.wikipedia.org/wiki/Japanese_name for Japanese. Korean and Japanese names not matched in universal lists are classified using series of rules, notably name endings. Genders for Chinese names are manually coded by native speakers from China who used personal knowledge of Chinese names supplemented by web searches on Google Images and Facebook. <a href="#LariviereEtal2013">Larivière et al (2013)</a> apply this classification methodology to gender disparities in science; <a href="#SugimotoEtal2015">Larivière et al (2013)</a> apply it to gender disparities in patenting.

<a href="#MartinezEtal2016">Martinez, Gema Lax, Julio Raffo, Kaori Saito (2016)</a> review the methodological approaches to attributing gender and develop a gender-name dictionary with worldwide coverage. Relevent to the current research, in addition to making use of popular name lists on Wikipedia, they use an ad-hoc list of Chinese, Indian, Japanese and Korean names that was created by WIPO staff native speakers.

<a href="#JensenKovacsSorenson2018">Jensen, Kyle, Balázs Kovács, and Olav Sorenson (2018)</a> determine the probable gender of inventors in US utility patent applications using given name gender distributions available from the US Social Security Administration and from two commercial databases, GenderAPI and genderize.io. They associated a given name with a single gender if the name was associated at least 95% of the time with that gender.

<a href="#MullerEtAl2019">Müller, Jain, and Te (2019)</a> use a dataset provided by a Swiss automobile insurance company that contains 1.88 million women's and 2.18 million men's names from 172 nationalities. These names contain 99,000 (5.3%) uniquely female and 111,000 (5.1%) uniquely male given names. (In this research, gender-specific Japanese marathon rosters contain about 40% unique names for both women and men.) They define unisex as names found for both genders with the probably of each being less than 95%.

### <a id="GenderAttributionEastAsian">Gender attribution for East Asian names</a>

Gender attribution for Asian names using European alphabets suffers from limitiations. The USPTO's <a href="#ProgressAndPotential2019">2019 Progress and Potential</a> profile of women inventors used a baseline attribution method based on IBM's Global Name Recognition system and WIPO7s worldwide gender-name dictionary (WGND). This baseline method was unable to classify gender for 54,400 cases from Japan, 34,600 cases from China and 28,300 cases from the Republic of Korea. These unclassified cases comprised 62% of the inventors residing in China and 31% of those residing in the Republic of Korea.

#### Existing resources for Japanese given names written in Kanji

Since the 1970s, Japanese parents have placed emphasis on finding unique names for their children (<a href="#Baresova2020">Baresova, 2020</a> and <a href="#Baresova2021">Baresova, 2021</a>). This popularity has given rise to a wide range of websites that provide lists of possible names with comments on meaning, phonology and numerology. The sources of names and rankings are unclear and names may not actually exist (see, for example, <a href="#douseidoumei_com">douseidoumei.com</a>). Two sites that specify their sources of data are <a href="#douseidoumei_net" >Dousei Doumei Jiten</a> and <a href="#namaejiten_com">Heisei Namae Jiten.</a> The former sources its data from a 2002 national telephone directory that was issued on CD-ROM and whose names are 90% male. The latter sources its data from an unnamed commercial database company and contains a more balanced mix of male and female names. The current project uses neither of these resources.

#### Characteristics of Japanese given names

##### 1. Given names may have multiple readings

In contrast to South Korea, where <i>hanja</i> in names each have only one associated phonetic Hangul (<a href="#YasuokaYasuoka2016">Yasuoka and Yasuoka (2016)</a>), <i>kanji</i> names in Japan can have multiple readings. Among the 10 most popular girls and boys names in Japan in 2020, shown in the tables below, <i>kanji</i> names have up to 5 readings, and some readings are applied to multiple <i>kanji</i> names, even unisex.

<table>
<caption><b>Readings of top 10 names of girls born in 2020 
(<a href="#MeijiyasudaReadingsGirls2020">Meiji Yasuda Life Insurance Company</a>)</b></caption>
<thead><tr><th>Rank</th><th><i>Kanji</i></th><th>Readings (Number of girls)</th></tr></thead>
<tbody>
<tr><td>1</td><td>陽葵</td><td>Himari (24), Hinata (15), Hina (3), Hiyori (2)</td></tr>
<tr><td>2</td><td>凛</td><td>Rin (41)</td></tr>
<tr><td>3</td><td>詩</td><td>Uta (40)</td></tr>
<tr><td>4</td><td>結菜</td><td>Yuna (20), Yuina (17), Yuuna (3)</td></tr>
<tr><td>5</td><td>結愛</td><td>Yua (22), Yui (4), Yume (3), Yuna (2), Yura (2)</td></tr>
<tr><td>6</td><td>莉子</td><td>Riko (36)</td></tr>
<tr><td>7</td><td>結月</td><td>Yudziki (27), Yuzuki (5), Yutsuki (2)</td></tr>
<tr><td>8</td><td>紬</td><td>Tsumugi (33)</td></tr>
<tr><td>8</td><td>澪</td><td>Mio (25), Rei (4)</td></tr>
<tr><td>10</td><td>結衣</td><td>Yui (32)</td></tr>
</tbody>
</table>
<table>
<caption><b>Readings of top 10 names of boys born in 2020 
(<a href="#MeijiyasudaReadingsBoys2020">Meiji Yasuda Life Insurance Company</a>)</b></caption>
<thead><tr><th>Rank</th><th><i>Kanji</i></th><th>Readings (Number of boys)</th></tr></thead>
<tbody>
<tr><td>1</td><td>蒼</td><td>Aoi (31), Sou (8), Ao (7), Sora (2)</td></tr>
<tr><td>2</td><td>樹</td><td>Itsuki (43), Tatsuki (2)</td></tr>
<tr><td>2</td><td>蓮</td><td>Ren (47)</td></tr>
<tr><td>4</td><td>陽翔</td><td>Haruto (31), Hinato (3), Hinata (2)</td></tr>
<tr><td>5</td><td>律</td><td>Ritsu (38)</td></tr>
<tr><td>6</td><td>朝陽</td><td>Asahi (36)</td></tr>
<tr><td>7</td><td>湊</td><td>Minato (33)</td></tr>
<tr><td>8</td><td>新</td><td>Arata (31), Shin (2)</td></tr>
<tr><td>9</td><td>大和</td><td>Yamato (32)</td></tr>
<tr><td>10</td><td>大翔</td><td>Hiroto (12), Taiga (7), Haruto (5), Yamato (4), Taishi (2)</td></tr>
</tbody>
</table>

##### 2. Given names commonly have gender-specific end characters

TBA

#### Characteristics of Chinese, Korean, Taiwanese and other Asian given names as they occur in Japanese text and databases

TBA

## <a id="TargetData">Target data</a>

TBA

## <a id="Datasets">Datasets</a>

### <a id="IndividualSearches">Individually searched given names (not released)</a>

<table>
<caption><b>Individually searched given names of persons listed on Japanese registered designs 2000-2018</b></caption>
<thead>
<tr><th>Category</th><th>Female</th><th>Male</th><th>Both</th><th>Undetermined</th><th>Total</th></tr>
</thead>
<tbody>
<tr><td>Examiners</td><td>42</td><td>97</td><td>3</td><td>0</td><td>145</td></tr>
<tr><td>Agents*</td><td>466</td><td>2894</td><td>65</td><td>8</td><td>3433</td></tr>
<tr><td>Creators</td><td>430</td><td>4103</td><td>152</td><td>270</td><td>4955</td></tr>
<tr><td>Total<br>(uniqued)</td><td>917</td><td>7030</td><td>217</td><td>249</td><td>8413</td></tr>
<tr><td colspan=6>*Excludes firms and companies listed as agents.</td></tr>
</tbody>
</table>

### <a id="JapaneseCelebs">Japanese celebrities</a>

<a href="https://github.com/AlanInTsukuba/name-gender-ja/blob/main/datasets/JapaneseCelebs.csv">JapaneseCelebs.csv</a> contains the given names, genders, full names and Wikipedia URL for 12397 Japanese celebrities scraped from the Wikipedia categories <a href="https://ja.wikipedia.org/wiki/Category:日本の女優">日本の女優 (Japanese female actors)</a> and <a href="https://ja.wikipedia.org/wiki/Category:日本の男優">日本の男優 (Japanese male actors)</a>; 5445 of these are women and 6952 are men. Uniquing on given name-gender tuples yielded 2701 unique female names and 4060 unique male names; 131 names were in both female and male uniqued sets. During clean up, original names were given precedence over stage names expect when the entry indicated transgender, in which case the first name after gender change was selected.

### <a id="GivenNamesGenderDataset">Gender-specific given names</a>

Runner lists were obtained from nine geographically separated marathons. Cleaned of foreign names entered in either roman characters or katakana, these lists yielded 96,087 surname-given name-gender tuples, which were uniqued to produce 88,079 tuples. Uniquing makes the operating assumption that each unique tuple corresponds to a single runner who ran in multiple marathons. Women made up 21.2% of the list. This list was aggregated on given name to give counts of surnames, women and men for each given name. Using a threshold surname count of 23 (expectation value of 5 / share of women), Chi-square good-of-fit tests were run for names with surname counts greater than the threshold and Fisher exact test were run for names with surname counts greater than or equal to 2 and less than or equal to the threshold. With a female expectation share of 0.211889 and p-value cutoff of 0.05, this yielded the 2744 gender-specific (1718 female, 1026 male) given names in GivenNameGender.csv.

<table>
<caption><b>Sample rows from GivenNameGender.csv</b></caption>
<thead><tr><th>GivenName</th><th>SurnameCount</th>
<th>Female</th><th>Male</th><th>Gender</th><th>pVal</th></tr></thead>
<tbody>
<tr><td>真奈</td><td>10</td><td>10</td><td>0</td><td>f</td><td>1.824277E-07</td></tr>
<tr><td>真奈美</td><td>22</td><td>22</td><td>0</td><td>f</td><td>1.494169E-15</td></tr>
<tr><td>真二</td><td>38</td><td>0</td><td>38</td><td>m</td><td>0.002</td></tr>
<tr><td>真之</td><td>14</td><td>0</td><td>14</td><td>m</td><td>0.03566325</td></tr>
</tbody>
</table>

### <a id="EndCharGenderDataset">Gender-specific end characters</a>

The same process for GivenNameGender.csv was followed except for further aggregating the given name aggregate list on the given names' end characters. With a female expectation share of 0.211889 and p-value cutoff of 0.05, this yielded the 445 gender-specific (185 female, 260 male) end characters in EndCharGender.csv.

<table>
<caption><b>Sample rows from EndCharGender.csv</b></caption>
<thead><tr><th>EndChar</th><th>SurnameCount</th>
<th>Female</th><th>Male</th><th>Gender</th><th>pVal</th></tr></thead>
<tbody>
<tr><td>映</td><td>7</td><td>6</td><td>1</td><td>f</td><td>0.0005184512</td></tr>
<tr><td>栄</td><td>74</td><td>27</td><td>47</td><td>f</td><td>0.002</td></tr>
<tr><td>英</td><td>166</td><td>17</td><td>149</td><td>m</td><td>0.001</td></tr>
<tr><td>衛</td><td>34</td><td>0</td><td>34</td><td>m</td><td>0.003</td></tr>
</tbody>
</table>

## <a id="CreatorNamesComparison">Applying datasets to creator names</a>

To compare gender assignments using the 4 datasets above, I applied them to the names of creators listed on Japanese designs registered between 2000 and 2018. The creators were restricted to those with Japanese addresses and those designs applied for directly at the Japanese patent office. This excludes creators with Japanese addresses whose registrations were applied for via the Hague Convention.
<table>
<caption><b>Gender matches between datasets and set of 145689 creator names</b></caption>
<tr height=18 style='height:13.5pt'>
  <td rowspan=2 height=18 width=97 style='height:13.5pt;width:73pt'></td>
  <td rowspan=2 colspan=2 width=144 style='width:108pt'>Matches vs name set</td>
  <td colspan=2 width=144 style='width:108pt'>Female</td>
  <td colspan=2 width=144 style='width:108pt'>Male</td>
  <td colspan=2 width=144 style='width:108pt'>Both</td>
 </tr>
<tr height=18 style='height:13.5pt'>
  <td colspan=6 width=432 style='width:324pt'>(Percent vs dataset matches)</td>
 </tr>
<tr height=18 style='height:13.5pt'>
  <td height=18 width=97 style='height:13.5pt;width:73pt'>Individually searched</td>
  <td width=72 style='width:54pt'>88227</td>
  <td width=72 style='width:54pt'>60.6%</td>
  <td width=72 style='width:54pt'>8809</td>
  <td width=72 style='width:54pt'>10.0%</td>
  <td width=72 style='width:54pt'>78858</td>
  <td width=72 style='width:54pt'>89.4%</td>
  <td width=72 style='width:54pt'>560</td>
  <td width=72 style='width:54pt'>0.6%</td>
 </tr>
<tr height=18 style='height:13.5pt'>
  <td height=18 width=97 style='height:13.5pt;width:73pt'>Japanese celebrities (Wikipedia)</td>
  <td width=72 style='width:54pt'>85424</td>
  <td width=72 style='width:54pt'>58.6%</td>
  <td width=72 style='width:54pt'>11427</td>
  <td width=72 style='width:54pt'>13.4%</td>
  <td width=72 style='width:54pt'>70699</td>
  <td width=72 style='width:54pt'>82.8%</td>
  <td width=72 style='width:54pt'>3298</td>
  <td width=72 style='width:54pt'>3.9%</td>
 </tr>
<tr height=18 style='height:13.5pt'>
  <td height=18 width=97 style='height:13.5pt;width:73pt'>Marathon rosters (given names)</td>
  <td width=72 style='width:54pt'>77959</td>
  <td width=72 style='width:54pt'>53.5%</td>
  <td width=72 style='width:54pt'>13280</td>
  <td width=72 style='width:54pt'>17.0%</td>
  <td width=72 style='width:54pt'>64679</td>
  <td width=72 style='width:54pt'>83.0%</td>
  <td colspan=2 width=144 style='width:108pt'>NA</td>
 </tr>
<tr height=18 style='height:13.5pt'>
  <td height=18 width=97 style='height:13.5pt;width:73pt'>Marathon rosters (end characters)</td>
  <td width=72 style='width:54pt'>139981</td>
  <td width=72 style='width:54pt'>96.1%</td>
  <td width=72 style='width:54pt'>19692</td>
  <td width=72 style='width:54pt'>14.1%</td>
  <td width=72 style='width:54pt'>120289</td>
  <td width=72 style='width:54pt'>85.9%</td>
  <td colspan=2 width=144 style='width:108pt'>NA</td>
 </tr>
<tr height=18 style='height:13.5pt'>
  <td height=18 width=97 style='height:13.5pt;width:73pt'>Not matched by any dataset</td>
  <td width=72 style='width:54pt'>472</td>
  <td width=72 style='width:54pt'>0.3%</td>
 </tr>
 </table>

The following table looks at consistency between datasets.

<table>
<caption><b>Agreement between datasets</b></caption>
<tr height=18 style='height:13.5pt'>
  <td height=18 width=97 style='height:13.5pt;width:73pt'></td>
  <td width=93 style='width:70pt'></td>
  <td width=72 style='width:54pt'></td>
  <td colspan=2 width=144 style='width:108pt'></td>
  <td colspan=2 width=144 style='width:108pt'></td>
  <td width=72 style='width:54pt'></td>
  <td colspan=2 width=144 style='width:108pt'></td>
  <td colspan=2 width=144 style='width:108pt'></td>
  <td colspan=6 class=xl65 width=432 style='width:324pt'>Marathon rosters</td>
 </tr>
   <tr height=25 style='height:18.75pt'>
  <td height=25 style='height:18.75pt'></td>
  <td colspan=7 class=xl66 width=288 style='width:216pt'>Japanese celebrities
  (Wikipedia)</td>
  <td colspan=5 class=xl66 width=216 style='width:162pt'>Given names</td>
  <td colspan=5 class=xl66 width=216 style='width:162pt'>End characters</td>
 </tr>
<tr height=19 style='height:14.25pt'>
  <td height=19 style='height:14.25pt'></td>
  <td></td>
  <td>Subtotal</td>
  <td colspan=2>Female</td>
  <td colspan=2>Male</td>
  <td colspan=2>Both</td>
   <td>Subtotal</td>
  <td colspan=2>Female</td>
  <td colspan=2>Male</td>
  <td>Subtotal</td>
  <td colspan=2>Female</td>
  <td colspan=2>Male</td>
 </tr>
</table>
<!--
<table>
<caption><b>Datasets applied to creators creators listed on Japanese designs registered between 2000 and 2018</b></caption>
<tr height=18 style='height:13.5pt'>
  <td height=18 width=97 style='height:13.5pt;width:73pt'></td>
  <td width=93 style='width:70pt'></td>
  <td width=72 style='width:54pt'></td>
  <td width=72 style='width:54pt'></td>
  <td width=72 style='width:54pt'></td>
  <td width=72 style='width:54pt'></td>
  <td width=72 style='width:54pt'></td>
  <td width=72 style='width:54pt'></td>
  <td width=72 style='width:54pt'></td>
  <td width=72 style='width:54pt'></td>
  <td width=72 style='width:54pt'></td>
  <td colspan=6 class=xl65 width=432 style='width:324pt'>Marathon rosters</td>
  <td width=99 style='width:74pt'></td>
 </tr>
  <tr height=25 style='height:18.75pt'>
  <td height=25 colspan=3 style='height:18.75pt'></td>
  <td colspan=4 class=xl65>Individually searched</td>
  <td colspan=4 class=xl66 width=288 style='width:216pt'>Japanese celebrities
  (Wikipedia)</td>
  <td colspan=3 class=xl66 width=216 style='width:162pt'>Given names</td>
  <td colspan=3 class=xl66 width=216 style='width:162pt'>End characters</td>
  <td>Undetermined</td>
 </tr>
 <tr height=19 style='height:14.25pt'>
  <td height=19 style='height:14.25pt'></td>
  <td>Names</td>
  <td>Total</td>
  <td>Female</td>
  <td>Male</td>
  <td>Both</td>
  <td>Subtotal</td>
  <td>Female</td>
  <td>Male</td>
  <td>Both</td>
  <td>Subtotal</td>
  <td>Female</td>
  <td>Male</td>
  <td>Subtotal</td>
  <td>Female</td>
  <td>Male</td>
  <td>Subtotal</td>
  <td></td>
 </tr>
  <tr height=20 style='height:15.0pt'>
  <td height=20 style='height:15.0pt'></td>
  <td>Total</td>
  <td class=xl86 align=right>145689</td>
  <td colspan=15 ></td>
 </tr>
 <tr height=19 style='height:14.25pt'>
  <td rowspan=4 height=74 class=xl66 width=97 style='height:55.5pt;width:73pt'>Individually
  searched</td>
  <td>Female</td>
  <td></td>
  <td class=xl68 align=right>8809</td>
  <td class=xl69> </td>
  <td class=xl69> </td>
  <td class=xl70> </td>
  <td class=xl76 align=right style='border-left:none'>7019</td>
  <td class=xl77 align=right>96</td>
  <td class=xl77 align=right>776</td>
  <td class=xl78> </td>
  <td class=xl81 align=right style='border-left:none'>8031</td>
  <td class=xl77 align=right>0</td>
  <td class=xl77> </td>
  <td class=xl81 align=right>7985</td>
  <td class=xl77 align=right>363</td>
  <td class=xl78> </td>
  <td></td>
 </tr>
 <tr height=18 style='height:13.5pt'>
  <td height=18 style='height:13.5pt'>Male</td>
  <td></td>
  <td class=xl71> </td>
  <td align=right>78858</td>
  <td></td>
  <td class=xl72> </td>
  <td class=xl71 align=right style='border-left:none'>50</td>
  <td align=right>57282</td>
  <td align=right>1992</td>
  <td class=xl79> </td>
  <td class=xl82 align=right style='border-left:none'>163</td>
  <td align=right>58011</td>
  <td></td>
  <td class=xl82 align=right>1571</td>
  <td align=right>73161</td>
  <td class=xl79> </td>
  <td></td>
 </tr>
 <tr height=18 style='height:13.5pt'>
  <td height=18 style='height:13.5pt'>Both</td>
  <td></td>
  <td class=xl71> </td>
  <td></td>
  <td align=right>560</td>
  <td class=xl72> </td>
  <td class=xl71 align=right style='border-left:none'>73</td>
  <td align=right>50</td>
  <td align=right>132</td>
  <td class=xl79> </td>
  <td class=xl82 align=right style='border-left:none'>109</td>
  <td align=right>45</td>
  <td></td>
  <td class=xl82 align=right>262</td>
  <td align=right>127</td>
  <td class=xl79> </td>
  <td></td>
 </tr>
 <tr height=19 style='height:14.25pt'>
  <td height=19 style='height:14.25pt'>Subtotal</td>
  <td></td>
  <td class=xl73> </td>
  <td class=xl74> </td>
  <td class=xl74> </td>
  <td class=xl75 align=right>88227</td>
  <td class=xl73 style='border-left:none'> </td>
  <td class=xl74> </td>
  <td class=xl74> </td>
  <td class=xl80 align=right>67470</td>
  <td class=xl83 style='border-left:none'> </td>
  <td class=xl84> </td>
  <td class=xl84 align=right>66359</td>
  <td class=xl83> </td>
  <td class=xl84> </td>
  <td class=xl85 align=right>83469</td>
  <td></td>
 </tr>
 <tr height=19 style='height:14.25pt'>
  <td rowspan=4 height=74 class=xl66 width=97 style='height:55.5pt;width:73pt'>Japanese
  celebrities (Wikipedia)</td>
  <td>Female</td>
  <td colspan=5 style='mso-ignore:colspan'></td>
  <td class=xl68 align=right style='border-top:none'>11427</td>
  <td class=xl69 style='border-top:none'> </td>
  <td class=xl69 style='border-top:none'> </td>
  <td class=xl70 style='border-top:none'> </td>
  <td align=right>10562</td>
  <td align=right>0</td>
  <td></td>
  <td class=xl81 align=right style='border-top:none'>10853</td>
  <td class=xl77 align=right style='border-top:none'>411</td>
  <td class=xl78 style='border-top:none'> </td>
  <td></td>
 </tr>
 <tr height=18 style='height:13.5pt'>
  <td height=18 style='height:13.5pt'>Male</td>
  <td colspan=5 style='mso-ignore:colspan'></td>
  <td class=xl71> </td>
  <td align=right>70699</td>
  <td></td>
  <td class=xl72> </td>
  <td align=right>144</td>
  <td align=right>55482</td>
  <td></td>
  <td class=xl82 align=right>981</td>
  <td align=right>68736</td>
  <td class=xl79> </td>
  <td></td>
 </tr>
 <tr height=18 style='height:13.5pt'>
  <td height=18 style='height:13.5pt'>Both</td>
  <td colspan=5 style='mso-ignore:colspan'></td>
  <td class=xl71> </td>
  <td></td>
  <td align=right>3298</td>
  <td class=xl72> </td>
  <td align=right>918</td>
  <td align=right>1720</td>
  <td></td>
  <td class=xl82 align=right>1124</td>
  <td align=right>1810</td>
  <td class=xl79> </td>
  <td></td>
 </tr>
 <tr height=19 style='height:14.25pt'>
  <td height=19 style='height:14.25pt'>Subtotal</td>
  <td colspan=5 style='mso-ignore:colspan'></td>
  <td class=xl73> </td>
  <td class=xl74> </td>
  <td class=xl74> </td>
  <td class=xl75 align=right>85424</td>
  <td colspan=2 style='mso-ignore:colspan'></td>
  <td align=right>68826</td>
  <td class=xl83> </td>
  <td class=xl84> </td>
  <td class=xl85 align=right>83915</td>
  <td></td>
 </tr>
 <tr height=19 style='height:14.25pt'>
  <td rowspan=3 height=56 class=xl66 width=97 style='height:42.0pt;width:73pt'>Marathon
  rosters (given names)</td>
  <td>Female</td>
  <td colspan=9 style='mso-ignore:colspan'></td>
  <td class=xl68 align=right>13280</td>
  <td class=xl69> </td>
  <td class=xl70> </td>
  <td class=xl76 align=right style='border-top:none;border-left:none'>12848</td>
  <td class=xl77 align=right style='border-top:none'>306</td>
  <td class=xl78 style='border-top:none'> </td>
  <td></td>
 </tr>
 <tr height=18 style='height:13.5pt'>
  <td height=18 style='height:13.5pt'>Male</td>
  <td colspan=9 style='mso-ignore:colspan'></td>
  <td class=xl71> </td>
  <td align=right>64679</td>
  <td class=xl72> </td>
  <td class=xl71 align=right style='border-left:none'>604</td>
  <td align=right>63893</td>
  <td class=xl79> </td>
  <td></td>
 </tr>
 <tr height=19 style='height:14.25pt'>
  <td height=19 style='height:14.25pt'>Subtotal</td>
  <td colspan=9 style='mso-ignore:colspan'></td>
  <td class=xl73> </td>
  <td class=xl74> </td>
  <td class=xl75 align=right>77959</td>
  <td class=xl73 style='border-left:none'> </td>
  <td class=xl74> </td>
  <td class=xl80 align=right>77651</td>
  <td></td>
 </tr>
 <tr height=19 style='height:14.25pt'>
  <td rowspan=3 height=56 class=xl66 width=97 style='height:42.0pt;width:73pt'>Marathon
  rosters (end characters)</td>
  <td>Female</td>
  <td colspan=12 style='mso-ignore:colspan'></td>
  <td class=xl68 align=right style='border-top:none'>19692</td>
  <td class=xl69 style='border-top:none'> </td>
  <td class=xl70 style='border-top:none'> </td>
  <td></td>
 </tr>
  <tr height=18 style='height:13.5pt'>
  <td height=18 style='height:13.5pt'>Male</td>
  <td colspan=12 style='mso-ignore:colspan'></td>
  <td class=xl71> </td>
  <td align=right>120289</td>
  <td class=xl72> </td>
  <td></td>
 </tr>
 <tr height=19 style='height:14.25pt'>
  <td height=19 style='height:14.25pt'>Subtotal</td>
  <td colspan=12 style='mso-ignore:colspan'></td>
  <td class=xl73> </td>
  <td class=xl74> </td>
  <td class=xl75 align=right>139981</td>
  <td></td>
 </tr>
 <tr height=20 style='height:15.0pt'>
  <td height=20 style='height:15.0pt'>Undetermined</td>
  <td colspan=16 style='mso-ignore:colspan'></td>
  <td class=xl86 align=right>472</td>
 </tr>
 <tr height=19 style='height:14.25pt'>
  <td height=19 colspan=18 style='height:14.25pt;mso-ignore:colspan'></td>
 </tr>
</table>
-->

## <a id="Notes">Notes</a>

<a id="MeijiyasudaReadingsGirls2020" href="https://www.meijiyasuda.co.jp/enjoy/ranking/read_best10/girl.html">名前ベスト10の読み方、女の子 [Readings of the top 10 names, girls]</a>[accessed 21 August 2021]

<a id="MeijiyasudaReadingsBoyss2020" href="https://www.meijiyasuda.co.jp/enjoy/ranking/read_best10/index.html">名前ベスト10の読み方、男の子[Readings of the top 10 names, boys]</a>[accessed 21 August 2021]

<a id="douseidoumei_com" href="http://douseidoumei.com/heisei/" target=_blank>平成同姓同名名前ランキング (Heisei same surname, same name ranking)</a> [accessed 31 August 2021] http://douseidoumei.com/heisei/

<a id="douseidoumei_net" href="http://www.douseidoumei.net/motodata.html"  target=_blank>Dousei Doumei Jiten (Same Surname, Same Name Dictionary)</a> [accessed 31 August 2021] http://www.douseidoumei.net/motodata.html

<a id="namaejiten_com" href="http://www.namaejiten.com/motodata.html"  target=_blank>Heisei Namae Jiten (Heisei Names Dictionary)</a> [accessed 31 August 2021] http://www.namaejiten.com/motodata.html

## <a id="References">References</a>

<a id="Baresova2021">Barešová, Ivona (2021)</a> "Boy Or Girl? the Rise of Non-Gender-Specific Names in Japan." Silva Iaponicarum, no. 56-59, 2021, pp. 26. [accessed 22 August 2021] http://silvajp.home.amu.edu.pl/Silva%2056575859.pdf#page=26

<a id="Baresova2020">Baresova, Ivona (2020)</a> "Hiroko, Sachiko, Yoko : The Phenomenon of Female "-Ko" Names in Modern Japan." The Gakushuin Journal of International Studies, vol. 6, 2020, pp. 23-38. [accessed 31 August 2021] https://glim-re.repo.nii.ac.jp/?action=repository_uri&item_id=4831&file_id=22&file_no=1

<a id="DelixusNWBC2012">Delixus, Inc. and National Women’s Business Council (2012)</a> Intellectual Property and Women Entrepreneurs. <https://cdn.www.nwbc.gov/wp-content/uploads/2018/02/27192725/Qualitative-Analysis-Intellectual-Property-Women-Entrepreneurs-Part-1.pdf> (accessed 16 August 2021)

<a id="JensenEtAl2018">Jensen K, Kovács B, Sorenson O. (2018)</a> Gender differences in obtaining and maintaining patent rights. Nat Biotechnol. 2018 Apr 5;36(4):307-309. doi: 10.1038/nbt.4120. PMID: 29621210.

<a id="JensenKovacsSorenson2018">Jensen, Kyle, Balázs Kovács, and Olav Sorenson (2018)</a> "Gender Differences in Obtaining and Maintaining Patent Rights." Nature Biotechnology, vol. 36, no. 4, 2018, pp. 307-309. [accessed 9 December 2020] https://www-proquest-com.ezproxy.tulips.tsukuba.ac.jp/docview/2021770129?pq-origsite=summon

<a id="LariviereEtal2013">Larivière, Vincent, Chaoqun Ni, Blaise Cronin, and Cassidy R. Sugimoto (2013).</a> "Global Gender Disparities in Science." Nature (London), 504(7479), pp. 211-213, doi:10.1038/504211a. Supplementary information.

<a id="Kawagishi2013">Kawagishi, Katsumi (2013)</a> Changes in the use of Kanji for names and the motivation behind such change (in Japanese). Journal of Yasuda Women's University, 41, 1-14, 2013. [accessed 20 August 2021] https://yasuda-u.repo.nii.ac.jp/?action=repository_uri&item_id=97

<a id="KnowlesEtal2016">Knowles, Rebecca, Josh Carroll, Mark Dredze (2016)</a>. Demographer: Extremely simple name demographics. Proceedings of 2016 EMNLP Workshop on Natural Language Processing and Computational Social Science. Association for Computational Linguistics. November 2016. pp 108-113. [accessed 28 August 2021] https://doi.org/10.18653/v1/W16-5614

<a id="MartinezEtal2016">Martinez, Gema Lax, Julio Raffo, Kaori Saito (2016)</a> Identifying the gender of PCT inventors. Economic Research Working Paper No. 33. World Intelectual Property Organization. [accessed 19 August 2021] https://www.wipo.int/publications/en/details.jsp?id=4125&plang=EN

<a id="MartinezEtal2021">Martinez, Gema Lax, Helena Saenz de Juano-i-Ribes, Deyun Yin, Bruno Le Feuvre, Intan Hamdan-Livramento, Kaori Saito, Julio Raffo (2021)</a> Expanding the World Gender-Name Dictionary: WGND 2.0. Economic Research Working Paper No. 64. World Intelectual Property Organization. [accessed 19 August 2021] https://www.wipo.int/edocs/pubdocs/en/wipo_pub_econstat_wp_64.pdf

<a id="MullerEtAl2019">Müller, Daniel, Pratiksha Jain, and Yieh-Funk Te. (2019)</a> "Augmenting data quality through high-precision gender categorization." Journal of Data and Information Quality (JDIQ) 11(2):1-18. doi:10.1145/3297720

<a id="ParkYoon2007">Park, Seong-Bae, and Hee-Geun Yoon (2007)</a>"Determining the Gender of Korean Names for Pronoun Generation." International Journal of Computer Science and Engineering 1.4 (2007): 226-30. [accessed 20 August 2021] https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.192.8977&rep=rep1&type=pdf

<a id="SugimotoEtal2015">Sugimoto, Cassidy R., Chaoqun Ni, Jevin D. West, Vincent Larivière (2015)</a> The Academic Advantage: Gender Disparities in Patenting. PLoS ONE 10(5): e0128000. doi:10.1371/journal.pone.0128000

<a id="TangEtal2011">Tang, Cong, Keith Ross, Nitesh Saxena, Ruichuan Xu (2011)</a> What's in a Name: A Study of Names, Gender Inference, and Gender Behavior in Facebook. In Jianliang Xu, Ge Yu, Shuigeng Zhou, and Rainer Unland (Eds.), Database Systems for Adanced Applications. DASFAA 2011. Lecture Notes in Computer Science, vol 6637. (pp. 344–356). Springer Berlin Heidelberg. [accessed 19 August 2021] https://doi-org.ezproxy.tulips.tsukuba.ac.jp/10.1007/978-3-642-20244-5_33

<a id="ButtonsToBiotech1999">United States Patent and Trademark Office (1999)</a>. Buttons to Biotech. 1996 Update Report with supplemental data through 1998. https://www.uspto.gov/web/offices/ac/ido/oeip/taf/wom_98.pdf (accessed 17 August 2021)

<a id="ProgressAndPotential2019">United States Patent and Trademark Office (2019)</a>. Progress and Potential: A profile of women inventors on U.S. patents. Office of the Chief Economist, IP Data Highlights, No. 2, February 2019, https://www.uspto.gov/sites/default/files/documents/OCE-DH-Progress-Potential-2020.pdf (accessed 17 August 2021)

<a id="WhittingtonSmithDoerr2008">Whittington, Kjersten Bunker, and Laurel Smith-Doerr (2008)</a> “WOMEN INVENTORS IN CONTEXT: Disparities in Patenting across Academia and Industry.” Gender and Society, 22(2):194–218. JSTOR, www.jstor.org/stable/27821633. Accessed 13 August 2021.

<a id="YasuokaYasuoka2016">Yasuoka, Koichi, and Motoko Yasuoka (2016)</a> Nichikan Nijukokuseki no Ko no Na ni tsukaeru ninmeiyo kanji (Japanese). Kosekijiho, no. 744, September 2016 [accessed 20 August 2021 ] http://hdl.handle.net/2433/219442