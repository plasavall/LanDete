# NOTE :bangbang:
This is a temporarily empty repository. The database will be made publicly available once the article for which it was developed is accepted.

## Welcome to the LanDete Database
LanDete is a database generated for Landmark Detection within regions or cities. It contains 6 diverse locations in Spain, ranging from small villages to large regions containing several population cores.

Included regions are:
* [Tapia de Casariego]\: small coastal village in Asturias.
* [Getafe]\: medium-sized industrial city located 13 km south of Madrid.
* [Jerez de la Frontera]\: medium-sized touristic city in Andalucia.
* [Valencia]\: large touristic coastal city in the east of Spain.
* [Guadalajara]\: small region including various villages with Black Architecture.
* [Euskadi]\: region between rivers Lea and Oria, with several coastal touristic villages.

[Tapia de Casariego]: https://en.wikipedia.org/wiki/Tapia_de_Casariego
[Getafe]: https://en.wikipedia.org/wiki/Getafe
[Jerez de la Frontera]: https://en.wikipedia.org/wiki/Jerez_de_la_Frontera
[Valencia]: https://en.wikipedia.org/wiki/Valencia
[Guadalajara]: https://www.recordrentacar.com/blog/en/road-trip-through-the-black-villages-of-guadalajara/
[Euskadi]: https://en.wikipedia.org/wiki/Oria_(river)

The database was generated from the web platform [Flickr], which allows for downloading geo-located images uploaded by users, along with lists of descriptive tags regarding each image.

[Flickr]: https://www.flickr.com/

The data for each region is stored in a diferent directory. Each directory contains 3 files:
* dictionary: csv file of size *_D_* x 2. *_D_* is the size of the dictionary, this is, the number of different tags present in the region. The first of the 2 columns contains the set of string representing each tag, while the second represents the frequency of said tag within the region.
* features: csv file of size *_N_* x (*_D_* + 3). *_N_* is the number of samples extracted from Flickr, this is, the number of uploaded images within the corresponding region. The first 3 entries of the columns represent latitude, longitude and a unique user ID, respectively, whereas the last *_D_* entries correspond to the dictionary entries. If a certain position *i* is activated (set to 1), the sample contains the *i*th tag in the dictionary.
* GT: text file containing the ground-truth points for each location, i.e., the most important touristic landmarks within the region. The file is structured as follows:<br/>
> latitude1 longitude1 relevance1 identifier1<br/>
> latitude2 longitude2 relevance2 identifier2<br/>
> latitude3 longitude3 relevance3 identifier3<br/>
> ...
<br/>
This database was developed by [Eduardo Pla Sacristán] at University Carlos III of Madrid.

[Eduardo Pla Sacristán]: https://orcid.org/0000-0001-5764-880X
