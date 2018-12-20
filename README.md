
# Importar o DataSet Titanic


```python
#importar o arquivo para uma variavel
titanic_csv = open('titanic.csv','r')
```


```python
# o metodo readlines identifica cada linha atravez do \n 
titanic_csv.readlines()
```




    ['PassengerId,Survived,Pclass,Name,Sex,Age,SibSp,Parch,Ticket,Fare,Cabin,Embarked\n',
     '1,0,3,"Braund, Mr. Owen Harris",male,22,1,0,A/5 21171,7.25,,S\n',
     '2,1,1,"Cumings, Mrs. John Bradley (Florence Briggs Thayer)",female,38,1,0,PC 17599,71.2833,C85,C\n',
     '3,1,3,"Heikkinen, Miss. Laina",female,26,0,0,STON/O2. 3101282,7.925,,S\n',
     '4,1,1,"Futrelle, Mrs. Jacques Heath (Lily May Peel)",female,35,1,0,113803,53.1,C123,S\n',
     '5,0,3,"Allen, Mr. William Henry",male,35,0,0,373450,8.05,,S\n',
     '6,0,3,"Moran, Mr. James",male,,0,0,330877,8.4583,,Q\n',
     '7,0,1,"McCarthy, Mr. Timothy J",male,54,0,0,17463,51.8625,E46,S\n',
     '8,0,3,"Palsson, Master. Gosta Leonard",male,2,3,1,349909,21.075,,S\n',
     '9,1,3,"Johnson, Mrs. Oscar W (Elisabeth Vilhelmina Berg)",female,27,0,2,347742,11.1333,,S\n',
     '10,1,2,"Nasser, Mrs. Nicholas (Adele Achem)",female,14,1,0,237736,30.0708,,C\n',
     '11,1,3,"Sandstrom, Miss. Marguerite Rut",female,4,1,1,PP 9549,16.7,G6,S\n',
     '12,1,1,"Bonnell, Miss. Elizabeth",female,58,0,0,113783,26.55,C103,S\n',
     '13,0,3,"Saundercock, Mr. William Henry",male,20,0,0,A/5. 2151,8.05,,S\n',
     '14,0,3,"Andersson, Mr. Anders Johan",male,39,1,5,347082,31.275,,S\n',
     '15,0,3,"Vestrom, Miss. Hulda Amanda Adolfina",female,14,0,0,350406,7.8542,,S\n',
     '16,1,2,"Hewlett, Mrs. (Mary D Kingcome) ",female,55,0,0,248706,16,,S\n',
     '17,0,3,"Rice, Master. Eugene",male,2,4,1,382652,29.125,,Q\n',
     '18,1,2,"Williams, Mr. Charles Eugene",male,,0,0,244373,13,,S\n',
     '19,0,3,"Vander Planke, Mrs. Julius (Emelia Maria Vandemoortele)",female,31,1,0,345763,18,,S\n',
     '20,1,3,"Masselmani, Mrs. Fatima",female,,0,0,2649,7.225,,C\n',
     '21,0,2,"Fynney, Mr. Joseph J",male,35,0,0,239865,26,,S\n',
     '22,1,2,"Beesley, Mr. Lawrence",male,34,0,0,248698,13,D56,S\n',
     '23,1,3,"McGowan, Miss. Anna ""Annie""",female,15,0,0,330923,8.0292,,Q\n',
     '24,1,1,"Sloper, Mr. William Thompson",male,28,0,0,113788,35.5,A6,S\n',
     '25,0,3,"Palsson, Miss. Torborg Danira",female,8,3,1,349909,21.075,,S\n',
     '26,1,3,"Asplund, Mrs. Carl Oscar (Selma Augusta Emilia Johansson)",female,38,1,5,347077,31.3875,,S\n',
     '27,0,3,"Emir, Mr. Farred Chehab",male,,0,0,2631,7.225,,C\n',
     '28,0,1,"Fortune, Mr. Charles Alexander",male,19,3,2,19950,263,C23 C25 C27,S\n',
     '29,1,3,"O\'Dwyer, Miss. Ellen ""Nellie""",female,,0,0,330959,7.8792,,Q\n',
     '30,0,3,"Todoroff, Mr. Lalio",male,,0,0,349216,7.8958,,S\n',
     '31,0,1,"Uruchurtu, Don. Manuel E",male,40,0,0,PC 17601,27.7208,,C\n',
     '32,1,1,"Spencer, Mrs. William Augustus (Marie Eugenie)",female,,1,0,PC 17569,146.5208,B78,C\n',
     '33,1,3,"Glynn, Miss. Mary Agatha",female,,0,0,335677,7.75,,Q\n',
     '34,0,2,"Wheadon, Mr. Edward H",male,66,0,0,C.A. 24579,10.5,,S\n',
     '35,0,1,"Meyer, Mr. Edgar Joseph",male,28,1,0,PC 17604,82.1708,,C\n',
     '36,0,1,"Holverson, Mr. Alexander Oskar",male,42,1,0,113789,52,,S\n',
     '37,1,3,"Mamee, Mr. Hanna",male,,0,0,2677,7.2292,,C\n',
     '38,0,3,"Cann, Mr. Ernest Charles",male,21,0,0,A./5. 2152,8.05,,S\n',
     '39,0,3,"Vander Planke, Miss. Augusta Maria",female,18,2,0,345764,18,,S\n',
     '40,1,3,"Nicola-Yarred, Miss. Jamila",female,14,1,0,2651,11.2417,,C\n',
     '41,0,3,"Ahlin, Mrs. Johan (Johanna Persdotter Larsson)",female,40,1,0,7546,9.475,,S\n',
     '42,0,2,"Turpin, Mrs. William John Robert (Dorothy Ann Wonnacott)",female,27,1,0,11668,21,,S\n',
     '43,0,3,"Kraeff, Mr. Theodor",male,,0,0,349253,7.8958,,C\n',
     '44,1,2,"Laroche, Miss. Simonne Marie Anne Andree",female,3,1,2,SC/Paris 2123,41.5792,,C\n',
     '45,1,3,"Devaney, Miss. Margaret Delia",female,19,0,0,330958,7.8792,,Q\n',
     '46,0,3,"Rogers, Mr. William John",male,,0,0,S.C./A.4. 23567,8.05,,S\n',
     '47,0,3,"Lennon, Mr. Denis",male,,1,0,370371,15.5,,Q\n',
     '48,1,3,"O\'Driscoll, Miss. Bridget",female,,0,0,14311,7.75,,Q\n',
     '49,0,3,"Samaan, Mr. Youssef",male,,2,0,2662,21.6792,,C\n',
     '50,0,3,"Arnold-Franchi, Mrs. Josef (Josefine Franchi)",female,18,1,0,349237,17.8,,S\n',
     '51,0,3,"Panula, Master. Juha Niilo",male,7,4,1,3101295,39.6875,,S\n',
     '52,0,3,"Nosworthy, Mr. Richard Cater",male,21,0,0,A/4. 39886,7.8,,S\n',
     '53,1,1,"Harper, Mrs. Henry Sleeper (Myna Haxtun)",female,49,1,0,PC 17572,76.7292,D33,C\n',
     '54,1,2,"Faunthorpe, Mrs. Lizzie (Elizabeth Anne Wilkinson)",female,29,1,0,2926,26,,S\n',
     '55,0,1,"Ostby, Mr. Engelhart Cornelius",male,65,0,1,113509,61.9792,B30,C\n',
     '56,1,1,"Woolner, Mr. Hugh",male,,0,0,19947,35.5,C52,S\n',
     '57,1,2,"Rugg, Miss. Emily",female,21,0,0,C.A. 31026,10.5,,S\n',
     '58,0,3,"Novel, Mr. Mansouer",male,28.5,0,0,2697,7.2292,,C\n',
     '59,1,2,"West, Miss. Constance Mirium",female,5,1,2,C.A. 34651,27.75,,S\n',
     '60,0,3,"Goodwin, Master. William Frederick",male,11,5,2,CA 2144,46.9,,S\n',
     '61,0,3,"Sirayanian, Mr. Orsen",male,22,0,0,2669,7.2292,,C\n',
     '62,1,1,"Icard, Miss. Amelie",female,38,0,0,113572,80,B28,\n',
     '63,0,1,"Harris, Mr. Henry Birkhardt",male,45,1,0,36973,83.475,C83,S\n',
     '64,0,3,"Skoog, Master. Harald",male,4,3,2,347088,27.9,,S\n',
     '65,0,1,"Stewart, Mr. Albert A",male,,0,0,PC 17605,27.7208,,C\n',
     '66,1,3,"Moubarek, Master. Gerios",male,,1,1,2661,15.2458,,C\n',
     '67,1,2,"Nye, Mrs. (Elizabeth Ramell)",female,29,0,0,C.A. 29395,10.5,F33,S\n',
     '68,0,3,"Crease, Mr. Ernest James",male,19,0,0,S.P. 3464,8.1583,,S\n',
     '69,1,3,"Andersson, Miss. Erna Alexandra",female,17,4,2,3101281,7.925,,S\n',
     '70,0,3,"Kink, Mr. Vincenz",male,26,2,0,315151,8.6625,,S\n',
     '71,0,2,"Jenkin, Mr. Stephen Curnow",male,32,0,0,C.A. 33111,10.5,,S\n',
     '72,0,3,"Goodwin, Miss. Lillian Amy",female,16,5,2,CA 2144,46.9,,S\n',
     '73,0,2,"Hood, Mr. Ambrose Jr",male,21,0,0,S.O.C. 14879,73.5,,S\n',
     '74,0,3,"Chronopoulos, Mr. Apostolos",male,26,1,0,2680,14.4542,,C\n',
     '75,1,3,"Bing, Mr. Lee",male,32,0,0,1601,56.4958,,S\n',
     '76,0,3,"Moen, Mr. Sigurd Hansen",male,25,0,0,348123,7.65,F G73,S\n',
     '77,0,3,"Staneff, Mr. Ivan",male,,0,0,349208,7.8958,,S\n',
     '78,0,3,"Moutal, Mr. Rahamin Haim",male,,0,0,374746,8.05,,S\n',
     '79,1,2,"Caldwell, Master. Alden Gates",male,0.83,0,2,248738,29,,S\n',
     '80,1,3,"Dowdell, Miss. Elizabeth",female,30,0,0,364516,12.475,,S\n',
     '81,0,3,"Waelens, Mr. Achille",male,22,0,0,345767,9,,S\n',
     '82,1,3,"Sheerlinck, Mr. Jan Baptist",male,29,0,0,345779,9.5,,S\n',
     '83,1,3,"McDermott, Miss. Brigdet Delia",female,,0,0,330932,7.7875,,Q\n',
     '84,0,1,"Carrau, Mr. Francisco M",male,28,0,0,113059,47.1,,S\n',
     '85,1,2,"Ilett, Miss. Bertha",female,17,0,0,SO/C 14885,10.5,,S\n',
     '86,1,3,"Backstrom, Mrs. Karl Alfred (Maria Mathilda Gustafsson)",female,33,3,0,3101278,15.85,,S\n',
     '87,0,3,"Ford, Mr. William Neal",male,16,1,3,W./C. 6608,34.375,,S\n',
     '88,0,3,"Slocovski, Mr. Selman Francis",male,,0,0,SOTON/OQ 392086,8.05,,S\n',
     '89,1,1,"Fortune, Miss. Mabel Helen",female,23,3,2,19950,263,C23 C25 C27,S\n',
     '90,0,3,"Celotti, Mr. Francesco",male,24,0,0,343275,8.05,,S\n',
     '91,0,3,"Christmann, Mr. Emil",male,29,0,0,343276,8.05,,S\n',
     '92,0,3,"Andreasson, Mr. Paul Edvin",male,20,0,0,347466,7.8542,,S\n',
     '93,0,1,"Chaffee, Mr. Herbert Fuller",male,46,1,0,W.E.P. 5734,61.175,E31,S\n',
     '94,0,3,"Dean, Mr. Bertram Frank",male,26,1,2,C.A. 2315,20.575,,S\n',
     '95,0,3,"Coxon, Mr. Daniel",male,59,0,0,364500,7.25,,S\n',
     '96,0,3,"Shorney, Mr. Charles Joseph",male,,0,0,374910,8.05,,S\n',
     '97,0,1,"Goldschmidt, Mr. George B",male,71,0,0,PC 17754,34.6542,A5,C\n',
     '98,1,1,"Greenfield, Mr. William Bertram",male,23,0,1,PC 17759,63.3583,D10 D12,C\n',
     '99,1,2,"Doling, Mrs. John T (Ada Julia Bone)",female,34,0,1,231919,23,,S\n',
     '100,0,2,"Kantor, Mr. Sinai",male,34,1,0,244367,26,,S\n',
     '101,0,3,"Petranec, Miss. Matilda",female,28,0,0,349245,7.8958,,S\n',
     '102,0,3,"Petroff, Mr. Pastcho (""Pentcho"")",male,,0,0,349215,7.8958,,S\n',
     '103,0,1,"White, Mr. Richard Frasar",male,21,0,1,35281,77.2875,D26,S\n',
     '104,0,3,"Johansson, Mr. Gustaf Joel",male,33,0,0,7540,8.6542,,S\n',
     '105,0,3,"Gustafsson, Mr. Anders Vilhelm",male,37,2,0,3101276,7.925,,S\n',
     '106,0,3,"Mionoff, Mr. Stoytcho",male,28,0,0,349207,7.8958,,S\n',
     '107,1,3,"Salkjelsvik, Miss. Anna Kristine",female,21,0,0,343120,7.65,,S\n',
     '108,1,3,"Moss, Mr. Albert Johan",male,,0,0,312991,7.775,,S\n',
     '109,0,3,"Rekic, Mr. Tido",male,38,0,0,349249,7.8958,,S\n',
     '110,1,3,"Moran, Miss. Bertha",female,,1,0,371110,24.15,,Q\n',
     '111,0,1,"Porter, Mr. Walter Chamberlain",male,47,0,0,110465,52,C110,S\n',
     '112,0,3,"Zabour, Miss. Hileni",female,14.5,1,0,2665,14.4542,,C\n',
     '113,0,3,"Barton, Mr. David John",male,22,0,0,324669,8.05,,S\n',
     '114,0,3,"Jussila, Miss. Katriina",female,20,1,0,4136,9.825,,S\n',
     '115,0,3,"Attalah, Miss. Malake",female,17,0,0,2627,14.4583,,C\n',
     '116,0,3,"Pekoniemi, Mr. Edvard",male,21,0,0,STON/O 2. 3101294,7.925,,S\n',
     '117,0,3,"Connors, Mr. Patrick",male,70.5,0,0,370369,7.75,,Q\n',
     '118,0,2,"Turpin, Mr. William John Robert",male,29,1,0,11668,21,,S\n',
     '119,0,1,"Baxter, Mr. Quigg Edmond",male,24,0,1,PC 17558,247.5208,B58 B60,C\n',
     '120,0,3,"Andersson, Miss. Ellis Anna Maria",female,2,4,2,347082,31.275,,S\n',
     '121,0,2,"Hickman, Mr. Stanley George",male,21,2,0,S.O.C. 14879,73.5,,S\n',
     '122,0,3,"Moore, Mr. Leonard Charles",male,,0,0,A4. 54510,8.05,,S\n',
     '123,0,2,"Nasser, Mr. Nicholas",male,32.5,1,0,237736,30.0708,,C\n',
     '124,1,2,"Webber, Miss. Susan",female,32.5,0,0,27267,13,E101,S\n',
     '125,0,1,"White, Mr. Percival Wayland",male,54,0,1,35281,77.2875,D26,S\n',
     '126,1,3,"Nicola-Yarred, Master. Elias",male,12,1,0,2651,11.2417,,C\n',
     '127,0,3,"McMahon, Mr. Martin",male,,0,0,370372,7.75,,Q\n',
     '128,1,3,"Madsen, Mr. Fridtjof Arne",male,24,0,0,C 17369,7.1417,,S\n',
     '129,1,3,"Peter, Miss. Anna",female,,1,1,2668,22.3583,F E69,C\n',
     '130,0,3,"Ekstrom, Mr. Johan",male,45,0,0,347061,6.975,,S\n',
     '131,0,3,"Drazenoic, Mr. Jozef",male,33,0,0,349241,7.8958,,C\n',
     '132,0,3,"Coelho, Mr. Domingos Fernandeo",male,20,0,0,SOTON/O.Q. 3101307,7.05,,S\n',
     '133,0,3,"Robins, Mrs. Alexander A (Grace Charity Laury)",female,47,1,0,A/5. 3337,14.5,,S\n',
     '134,1,2,"Weisz, Mrs. Leopold (Mathilde Francoise Pede)",female,29,1,0,228414,26,,S\n',
     '135,0,2,"Sobey, Mr. Samuel James Hayden",male,25,0,0,C.A. 29178,13,,S\n',
     '136,0,2,"Richard, Mr. Emile",male,23,0,0,SC/PARIS 2133,15.0458,,C\n',
     '137,1,1,"Newsom, Miss. Helen Monypeny",female,19,0,2,11752,26.2833,D47,S\n',
     '138,0,1,"Futrelle, Mr. Jacques Heath",male,37,1,0,113803,53.1,C123,S\n',
     '139,0,3,"Osen, Mr. Olaf Elon",male,16,0,0,7534,9.2167,,S\n',
     '140,0,1,"Giglio, Mr. Victor",male,24,0,0,PC 17593,79.2,B86,C\n',
     '141,0,3,"Boulos, Mrs. Joseph (Sultana)",female,,0,2,2678,15.2458,,C\n',
     '142,1,3,"Nysten, Miss. Anna Sofia",female,22,0,0,347081,7.75,,S\n',
     '143,1,3,"Hakkarainen, Mrs. Pekka Pietari (Elin Matilda Dolck)",female,24,1,0,STON/O2. 3101279,15.85,,S\n',
     '144,0,3,"Burke, Mr. Jeremiah",male,19,0,0,365222,6.75,,Q\n',
     '145,0,2,"Andrew, Mr. Edgardo Samuel",male,18,0,0,231945,11.5,,S\n',
     '146,0,2,"Nicholls, Mr. Joseph Charles",male,19,1,1,C.A. 33112,36.75,,S\n',
     '147,1,3,"Andersson, Mr. August Edvard (""Wennerstrom"")",male,27,0,0,350043,7.7958,,S\n',
     '148,0,3,"Ford, Miss. Robina Maggie ""Ruby""",female,9,2,2,W./C. 6608,34.375,,S\n',
     '149,0,2,"Navratil, Mr. Michel (""Louis M Hoffman"")",male,36.5,0,2,230080,26,F2,S\n',
     '150,0,2,"Byles, Rev. Thomas Roussel Davids",male,42,0,0,244310,13,,S\n',
     '151,0,2,"Bateman, Rev. Robert James",male,51,0,0,S.O.P. 1166,12.525,,S\n',
     '152,1,1,"Pears, Mrs. Thomas (Edith Wearne)",female,22,1,0,113776,66.6,C2,S\n',
     '153,0,3,"Meo, Mr. Alfonzo",male,55.5,0,0,A.5. 11206,8.05,,S\n',
     '154,0,3,"van Billiard, Mr. Austin Blyler",male,40.5,0,2,A/5. 851,14.5,,S\n',
     '155,0,3,"Olsen, Mr. Ole Martin",male,,0,0,Fa 265302,7.3125,,S\n',
     '156,0,1,"Williams, Mr. Charles Duane",male,51,0,1,PC 17597,61.3792,,C\n',
     '157,1,3,"Gilnagh, Miss. Katherine ""Katie""",female,16,0,0,35851,7.7333,,Q\n',
     '158,0,3,"Corn, Mr. Harry",male,30,0,0,SOTON/OQ 392090,8.05,,S\n',
     '159,0,3,"Smiljanic, Mr. Mile",male,,0,0,315037,8.6625,,S\n',
     '160,0,3,"Sage, Master. Thomas Henry",male,,8,2,CA. 2343,69.55,,S\n',
     '161,0,3,"Cribb, Mr. John Hatfield",male,44,0,1,371362,16.1,,S\n',
     '162,1,2,"Watt, Mrs. James (Elizabeth ""Bessie"" Inglis Milne)",female,40,0,0,C.A. 33595,15.75,,S\n',
     '163,0,3,"Bengtsson, Mr. John Viktor",male,26,0,0,347068,7.775,,S\n',
     '164,0,3,"Calic, Mr. Jovo",male,17,0,0,315093,8.6625,,S\n',
     '165,0,3,"Panula, Master. Eino Viljami",male,1,4,1,3101295,39.6875,,S\n',
     '166,1,3,"Goldsmith, Master. Frank John William ""Frankie""",male,9,0,2,363291,20.525,,S\n',
     '167,1,1,"Chibnall, Mrs. (Edith Martha Bowerman)",female,,0,1,113505,55,E33,S\n',
     '168,0,3,"Skoog, Mrs. William (Anna Bernhardina Karlsson)",female,45,1,4,347088,27.9,,S\n',
     '169,0,1,"Baumann, Mr. John D",male,,0,0,PC 17318,25.925,,S\n',
     '170,0,3,"Ling, Mr. Lee",male,28,0,0,1601,56.4958,,S\n',
     '171,0,1,"Van der hoef, Mr. Wyckoff",male,61,0,0,111240,33.5,B19,S\n',
     '172,0,3,"Rice, Master. Arthur",male,4,4,1,382652,29.125,,Q\n',
     '173,1,3,"Johnson, Miss. Eleanor Ileen",female,1,1,1,347742,11.1333,,S\n',
     '174,0,3,"Sivola, Mr. Antti Wilhelm",male,21,0,0,STON/O 2. 3101280,7.925,,S\n',
     '175,0,1,"Smith, Mr. James Clinch",male,56,0,0,17764,30.6958,A7,C\n',
     '176,0,3,"Klasen, Mr. Klas Albin",male,18,1,1,350404,7.8542,,S\n',
     '177,0,3,"Lefebre, Master. Henry Forbes",male,,3,1,4133,25.4667,,S\n',
     '178,0,1,"Isham, Miss. Ann Elizabeth",female,50,0,0,PC 17595,28.7125,C49,C\n',
     '179,0,2,"Hale, Mr. Reginald",male,30,0,0,250653,13,,S\n',
     '180,0,3,"Leonard, Mr. Lionel",male,36,0,0,LINE,0,,S\n',
     '181,0,3,"Sage, Miss. Constance Gladys",female,,8,2,CA. 2343,69.55,,S\n',
     '182,0,2,"Pernot, Mr. Rene",male,,0,0,SC/PARIS 2131,15.05,,C\n',
     '183,0,3,"Asplund, Master. Clarence Gustaf Hugo",male,9,4,2,347077,31.3875,,S\n',
     '184,1,2,"Becker, Master. Richard F",male,1,2,1,230136,39,F4,S\n',
     '185,1,3,"Kink-Heilmann, Miss. Luise Gretchen",female,4,0,2,315153,22.025,,S\n',
     '186,0,1,"Rood, Mr. Hugh Roscoe",male,,0,0,113767,50,A32,S\n',
     '187,1,3,"O\'Brien, Mrs. Thomas (Johanna ""Hannah"" Godfrey)",female,,1,0,370365,15.5,,Q\n',
     '188,1,1,"Romaine, Mr. Charles Hallace (""Mr C Rolmane"")",male,45,0,0,111428,26.55,,S\n',
     '189,0,3,"Bourke, Mr. John",male,40,1,1,364849,15.5,,Q\n',
     '190,0,3,"Turcin, Mr. Stjepan",male,36,0,0,349247,7.8958,,S\n',
     '191,1,2,"Pinsky, Mrs. (Rosa)",female,32,0,0,234604,13,,S\n',
     '192,0,2,"Carbines, Mr. William",male,19,0,0,28424,13,,S\n',
     '193,1,3,"Andersen-Jensen, Miss. Carla Christine Nielsine",female,19,1,0,350046,7.8542,,S\n',
     '194,1,2,"Navratil, Master. Michel M",male,3,1,1,230080,26,F2,S\n',
     '195,1,1,"Brown, Mrs. James Joseph (Margaret Tobin)",female,44,0,0,PC 17610,27.7208,B4,C\n',
     '196,1,1,"Lurette, Miss. Elise",female,58,0,0,PC 17569,146.5208,B80,C\n',
     '197,0,3,"Mernagh, Mr. Robert",male,,0,0,368703,7.75,,Q\n',
     '198,0,3,"Olsen, Mr. Karl Siegwart Andreas",male,42,0,1,4579,8.4042,,S\n',
     '199,1,3,"Madigan, Miss. Margaret ""Maggie""",female,,0,0,370370,7.75,,Q\n',
     '200,0,2,"Yrois, Miss. Henriette (""Mrs Harbeck"")",female,24,0,0,248747,13,,S\n',
     '201,0,3,"Vande Walle, Mr. Nestor Cyriel",male,28,0,0,345770,9.5,,S\n',
     '202,0,3,"Sage, Mr. Frederick",male,,8,2,CA. 2343,69.55,,S\n',
     '203,0,3,"Johanson, Mr. Jakob Alfred",male,34,0,0,3101264,6.4958,,S\n',
     '204,0,3,"Youseff, Mr. Gerious",male,45.5,0,0,2628,7.225,,C\n',
     '205,1,3,"Cohen, Mr. Gurshon ""Gus""",male,18,0,0,A/5 3540,8.05,,S\n',
     '206,0,3,"Strom, Miss. Telma Matilda",female,2,0,1,347054,10.4625,G6,S\n',
     '207,0,3,"Backstrom, Mr. Karl Alfred",male,32,1,0,3101278,15.85,,S\n',
     '208,1,3,"Albimona, Mr. Nassef Cassem",male,26,0,0,2699,18.7875,,C\n',
     '209,1,3,"Carr, Miss. Helen ""Ellen""",female,16,0,0,367231,7.75,,Q\n',
     '210,1,1,"Blank, Mr. Henry",male,40,0,0,112277,31,A31,C\n',
     '211,0,3,"Ali, Mr. Ahmed",male,24,0,0,SOTON/O.Q. 3101311,7.05,,S\n',
     '212,1,2,"Cameron, Miss. Clear Annie",female,35,0,0,F.C.C. 13528,21,,S\n',
     '213,0,3,"Perkin, Mr. John Henry",male,22,0,0,A/5 21174,7.25,,S\n',
     '214,0,2,"Givard, Mr. Hans Kristensen",male,30,0,0,250646,13,,S\n',
     '215,0,3,"Kiernan, Mr. Philip",male,,1,0,367229,7.75,,Q\n',
     '216,1,1,"Newell, Miss. Madeleine",female,31,1,0,35273,113.275,D36,C\n',
     '217,1,3,"Honkanen, Miss. Eliina",female,27,0,0,STON/O2. 3101283,7.925,,S\n',
     '218,0,2,"Jacobsohn, Mr. Sidney Samuel",male,42,1,0,243847,27,,S\n',
     '219,1,1,"Bazzani, Miss. Albina",female,32,0,0,11813,76.2917,D15,C\n',
     '220,0,2,"Harris, Mr. Walter",male,30,0,0,W/C 14208,10.5,,S\n',
     '221,1,3,"Sunderland, Mr. Victor Francis",male,16,0,0,SOTON/OQ 392089,8.05,,S\n',
     '222,0,2,"Bracken, Mr. James H",male,27,0,0,220367,13,,S\n',
     '223,0,3,"Green, Mr. George Henry",male,51,0,0,21440,8.05,,S\n',
     '224,0,3,"Nenkoff, Mr. Christo",male,,0,0,349234,7.8958,,S\n',
     '225,1,1,"Hoyt, Mr. Frederick Maxfield",male,38,1,0,19943,90,C93,S\n',
     '226,0,3,"Berglund, Mr. Karl Ivar Sven",male,22,0,0,PP 4348,9.35,,S\n',
     '227,1,2,"Mellors, Mr. William John",male,19,0,0,SW/PP 751,10.5,,S\n',
     '228,0,3,"Lovell, Mr. John Hall (""Henry"")",male,20.5,0,0,A/5 21173,7.25,,S\n',
     '229,0,2,"Fahlstrom, Mr. Arne Jonas",male,18,0,0,236171,13,,S\n',
     '230,0,3,"Lefebre, Miss. Mathilde",female,,3,1,4133,25.4667,,S\n',
     '231,1,1,"Harris, Mrs. Henry Birkhardt (Irene Wallach)",female,35,1,0,36973,83.475,C83,S\n',
     '232,0,3,"Larsson, Mr. Bengt Edvin",male,29,0,0,347067,7.775,,S\n',
     '233,0,2,"Sjostedt, Mr. Ernst Adolf",male,59,0,0,237442,13.5,,S\n',
     '234,1,3,"Asplund, Miss. Lillian Gertrud",female,5,4,2,347077,31.3875,,S\n',
     '235,0,2,"Leyson, Mr. Robert William Norman",male,24,0,0,C.A. 29566,10.5,,S\n',
     '236,0,3,"Harknett, Miss. Alice Phoebe",female,,0,0,W./C. 6609,7.55,,S\n',
     '237,0,2,"Hold, Mr. Stephen",male,44,1,0,26707,26,,S\n',
     '238,1,2,"Collyer, Miss. Marjorie ""Lottie""",female,8,0,2,C.A. 31921,26.25,,S\n',
     '239,0,2,"Pengelly, Mr. Frederick William",male,19,0,0,28665,10.5,,S\n',
     '240,0,2,"Hunt, Mr. George Henry",male,33,0,0,SCO/W 1585,12.275,,S\n',
     '241,0,3,"Zabour, Miss. Thamine",female,,1,0,2665,14.4542,,C\n',
     '242,1,3,"Murphy, Miss. Katherine ""Kate""",female,,1,0,367230,15.5,,Q\n',
     '243,0,2,"Coleridge, Mr. Reginald Charles",male,29,0,0,W./C. 14263,10.5,,S\n',
     '244,0,3,"Maenpaa, Mr. Matti Alexanteri",male,22,0,0,STON/O 2. 3101275,7.125,,S\n',
     '245,0,3,"Attalah, Mr. Sleiman",male,30,0,0,2694,7.225,,C\n',
     '246,0,1,"Minahan, Dr. William Edward",male,44,2,0,19928,90,C78,Q\n',
     '247,0,3,"Lindahl, Miss. Agda Thorilda Viktoria",female,25,0,0,347071,7.775,,S\n',
     '248,1,2,"Hamalainen, Mrs. William (Anna)",female,24,0,2,250649,14.5,,S\n',
     '249,1,1,"Beckwith, Mr. Richard Leonard",male,37,1,1,11751,52.5542,D35,S\n',
     '250,0,2,"Carter, Rev. Ernest Courtenay",male,54,1,0,244252,26,,S\n',
     '251,0,3,"Reed, Mr. James George",male,,0,0,362316,7.25,,S\n',
     '252,0,3,"Strom, Mrs. Wilhelm (Elna Matilda Persson)",female,29,1,1,347054,10.4625,G6,S\n',
     '253,0,1,"Stead, Mr. William Thomas",male,62,0,0,113514,26.55,C87,S\n',
     '254,0,3,"Lobb, Mr. William Arthur",male,30,1,0,A/5. 3336,16.1,,S\n',
     '255,0,3,"Rosblom, Mrs. Viktor (Helena Wilhelmina)",female,41,0,2,370129,20.2125,,S\n',
     '256,1,3,"Touma, Mrs. Darwis (Hanne Youssef Razi)",female,29,0,2,2650,15.2458,,C\n',
     '257,1,1,"Thorne, Mrs. Gertrude Maybelle",female,,0,0,PC 17585,79.2,,C\n',
     '258,1,1,"Cherry, Miss. Gladys",female,30,0,0,110152,86.5,B77,S\n',
     '259,1,1,"Ward, Miss. Anna",female,35,0,0,PC 17755,512.3292,,C\n',
     '260,1,2,"Parrish, Mrs. (Lutie Davis)",female,50,0,1,230433,26,,S\n',
     '261,0,3,"Smith, Mr. Thomas",male,,0,0,384461,7.75,,Q\n',
     '262,1,3,"Asplund, Master. Edvin Rojj Felix",male,3,4,2,347077,31.3875,,S\n',
     '263,0,1,"Taussig, Mr. Emil",male,52,1,1,110413,79.65,E67,S\n',
     '264,0,1,"Harrison, Mr. William",male,40,0,0,112059,0,B94,S\n',
     '265,0,3,"Henry, Miss. Delia",female,,0,0,382649,7.75,,Q\n',
     '266,0,2,"Reeves, Mr. David",male,36,0,0,C.A. 17248,10.5,,S\n',
     '267,0,3,"Panula, Mr. Ernesti Arvid",male,16,4,1,3101295,39.6875,,S\n',
     '268,1,3,"Persson, Mr. Ernst Ulrik",male,25,1,0,347083,7.775,,S\n',
     '269,1,1,"Graham, Mrs. William Thompson (Edith Junkins)",female,58,0,1,PC 17582,153.4625,C125,S\n',
     '270,1,1,"Bissette, Miss. Amelia",female,35,0,0,PC 17760,135.6333,C99,S\n',
     '271,0,1,"Cairns, Mr. Alexander",male,,0,0,113798,31,,S\n',
     '272,1,3,"Tornquist, Mr. William Henry",male,25,0,0,LINE,0,,S\n',
     '273,1,2,"Mellinger, Mrs. (Elizabeth Anne Maidment)",female,41,0,1,250644,19.5,,S\n',
     '274,0,1,"Natsch, Mr. Charles H",male,37,0,1,PC 17596,29.7,C118,C\n',
     '275,1,3,"Healy, Miss. Hanora ""Nora""",female,,0,0,370375,7.75,,Q\n',
     '276,1,1,"Andrews, Miss. Kornelia Theodosia",female,63,1,0,13502,77.9583,D7,S\n',
     '277,0,3,"Lindblom, Miss. Augusta Charlotta",female,45,0,0,347073,7.75,,S\n',
     '278,0,2,"Parkes, Mr. Francis ""Frank""",male,,0,0,239853,0,,S\n',
     '279,0,3,"Rice, Master. Eric",male,7,4,1,382652,29.125,,Q\n',
     '280,1,3,"Abbott, Mrs. Stanton (Rosa Hunt)",female,35,1,1,C.A. 2673,20.25,,S\n',
     '281,0,3,"Duane, Mr. Frank",male,65,0,0,336439,7.75,,Q\n',
     '282,0,3,"Olsson, Mr. Nils Johan Goransson",male,28,0,0,347464,7.8542,,S\n',
     '283,0,3,"de Pelsmaeker, Mr. Alfons",male,16,0,0,345778,9.5,,S\n',
     '284,1,3,"Dorking, Mr. Edward Arthur",male,19,0,0,A/5. 10482,8.05,,S\n',
     '285,0,1,"Smith, Mr. Richard William",male,,0,0,113056,26,A19,S\n',
     '286,0,3,"Stankovic, Mr. Ivan",male,33,0,0,349239,8.6625,,C\n',
     '287,1,3,"de Mulder, Mr. Theodore",male,30,0,0,345774,9.5,,S\n',
     '288,0,3,"Naidenoff, Mr. Penko",male,22,0,0,349206,7.8958,,S\n',
     '289,1,2,"Hosono, Mr. Masabumi",male,42,0,0,237798,13,,S\n',
     '290,1,3,"Connolly, Miss. Kate",female,22,0,0,370373,7.75,,Q\n',
     '291,1,1,"Barber, Miss. Ellen ""Nellie""",female,26,0,0,19877,78.85,,S\n',
     '292,1,1,"Bishop, Mrs. Dickinson H (Helen Walton)",female,19,1,0,11967,91.0792,B49,C\n',
     '293,0,2,"Levy, Mr. Rene Jacques",male,36,0,0,SC/Paris 2163,12.875,D,C\n',
     '294,0,3,"Haas, Miss. Aloisia",female,24,0,0,349236,8.85,,S\n',
     '295,0,3,"Mineff, Mr. Ivan",male,24,0,0,349233,7.8958,,S\n',
     '296,0,1,"Lewy, Mr. Ervin G",male,,0,0,PC 17612,27.7208,,C\n',
     '297,0,3,"Hanna, Mr. Mansour",male,23.5,0,0,2693,7.2292,,C\n',
     '298,0,1,"Allison, Miss. Helen Loraine",female,2,1,2,113781,151.55,C22 C26,S\n',
     '299,1,1,"Saalfeld, Mr. Adolphe",male,,0,0,19988,30.5,C106,S\n',
     '300,1,1,"Baxter, Mrs. James (Helene DeLaudeniere Chaput)",female,50,0,1,PC 17558,247.5208,B58 B60,C\n',
     '301,1,3,"Kelly, Miss. Anna Katherine ""Annie Kate""",female,,0,0,9234,7.75,,Q\n',
     '302,1,3,"McCoy, Mr. Bernard",male,,2,0,367226,23.25,,Q\n',
     '303,0,3,"Johnson, Mr. William Cahoone Jr",male,19,0,0,LINE,0,,S\n',
     '304,1,2,"Keane, Miss. Nora A",female,,0,0,226593,12.35,E101,Q\n',
     '305,0,3,"Williams, Mr. Howard Hugh ""Harry""",male,,0,0,A/5 2466,8.05,,S\n',
     '306,1,1,"Allison, Master. Hudson Trevor",male,0.92,1,2,113781,151.55,C22 C26,S\n',
     '307,1,1,"Fleming, Miss. Margaret",female,,0,0,17421,110.8833,,C\n',
     '308,1,1,"Penasco y Castellana, Mrs. Victor de Satode (Maria Josefa Perez de Soto y Vallejo)",female,17,1,0,PC 17758,108.9,C65,C\n',
     '309,0,2,"Abelson, Mr. Samuel",male,30,1,0,P/PP 3381,24,,C\n',
     '310,1,1,"Francatelli, Miss. Laura Mabel",female,30,0,0,PC 17485,56.9292,E36,C\n',
     '311,1,1,"Hays, Miss. Margaret Bechstein",female,24,0,0,11767,83.1583,C54,C\n',
     '312,1,1,"Ryerson, Miss. Emily Borie",female,18,2,2,PC 17608,262.375,B57 B59 B63 B66,C\n',
     '313,0,2,"Lahtinen, Mrs. William (Anna Sylfven)",female,26,1,1,250651,26,,S\n',
     '314,0,3,"Hendekovic, Mr. Ignjac",male,28,0,0,349243,7.8958,,S\n',
     '315,0,2,"Hart, Mr. Benjamin",male,43,1,1,F.C.C. 13529,26.25,,S\n',
     '316,1,3,"Nilsson, Miss. Helmina Josefina",female,26,0,0,347470,7.8542,,S\n',
     '317,1,2,"Kantor, Mrs. Sinai (Miriam Sternin)",female,24,1,0,244367,26,,S\n',
     '318,0,2,"Moraweck, Dr. Ernest",male,54,0,0,29011,14,,S\n',
     '319,1,1,"Wick, Miss. Mary Natalie",female,31,0,2,36928,164.8667,C7,S\n',
     '320,1,1,"Spedden, Mrs. Frederic Oakley (Margaretta Corning Stone)",female,40,1,1,16966,134.5,E34,C\n',
     '321,0,3,"Dennis, Mr. Samuel",male,22,0,0,A/5 21172,7.25,,S\n',
     '322,0,3,"Danoff, Mr. Yoto",male,27,0,0,349219,7.8958,,S\n',
     '323,1,2,"Slayter, Miss. Hilda Mary",female,30,0,0,234818,12.35,,Q\n',
     '324,1,2,"Caldwell, Mrs. Albert Francis (Sylvia Mae Harbaugh)",female,22,1,1,248738,29,,S\n',
     '325,0,3,"Sage, Mr. George John Jr",male,,8,2,CA. 2343,69.55,,S\n',
     '326,1,1,"Young, Miss. Marie Grice",female,36,0,0,PC 17760,135.6333,C32,C\n',
     '327,0,3,"Nysveen, Mr. Johan Hansen",male,61,0,0,345364,6.2375,,S\n',
     '328,1,2,"Ball, Mrs. (Ada E Hall)",female,36,0,0,28551,13,D,S\n',
     '329,1,3,"Goldsmith, Mrs. Frank John (Emily Alice Brown)",female,31,1,1,363291,20.525,,S\n',
     '330,1,1,"Hippach, Miss. Jean Gertrude",female,16,0,1,111361,57.9792,B18,C\n',
     '331,1,3,"McCoy, Miss. Agnes",female,,2,0,367226,23.25,,Q\n',
     '332,0,1,"Partner, Mr. Austen",male,45.5,0,0,113043,28.5,C124,S\n',
     '333,0,1,"Graham, Mr. George Edward",male,38,0,1,PC 17582,153.4625,C91,S\n',
     '334,0,3,"Vander Planke, Mr. Leo Edmondus",male,16,2,0,345764,18,,S\n',
     '335,1,1,"Frauenthal, Mrs. Henry William (Clara Heinsheimer)",female,,1,0,PC 17611,133.65,,S\n',
     '336,0,3,"Denkoff, Mr. Mitto",male,,0,0,349225,7.8958,,S\n',
     '337,0,1,"Pears, Mr. Thomas Clinton",male,29,1,0,113776,66.6,C2,S\n',
     '338,1,1,"Burns, Miss. Elizabeth Margaret",female,41,0,0,16966,134.5,E40,C\n',
     '339,1,3,"Dahl, Mr. Karl Edwart",male,45,0,0,7598,8.05,,S\n',
     '340,0,1,"Blackwell, Mr. Stephen Weart",male,45,0,0,113784,35.5,T,S\n',
     '341,1,2,"Navratil, Master. Edmond Roger",male,2,1,1,230080,26,F2,S\n',
     '342,1,1,"Fortune, Miss. Alice Elizabeth",female,24,3,2,19950,263,C23 C25 C27,S\n',
     '343,0,2,"Collander, Mr. Erik Gustaf",male,28,0,0,248740,13,,S\n',
     '344,0,2,"Sedgwick, Mr. Charles Frederick Waddington",male,25,0,0,244361,13,,S\n',
     '345,0,2,"Fox, Mr. Stanley Hubert",male,36,0,0,229236,13,,S\n',
     '346,1,2,"Brown, Miss. Amelia ""Mildred""",female,24,0,0,248733,13,F33,S\n',
     '347,1,2,"Smith, Miss. Marion Elsie",female,40,0,0,31418,13,,S\n',
     '348,1,3,"Davison, Mrs. Thomas Henry (Mary E Finck)",female,,1,0,386525,16.1,,S\n',
     '349,1,3,"Coutts, Master. William Loch ""William""",male,3,1,1,C.A. 37671,15.9,,S\n',
     '350,0,3,"Dimic, Mr. Jovan",male,42,0,0,315088,8.6625,,S\n',
     '351,0,3,"Odahl, Mr. Nils Martin",male,23,0,0,7267,9.225,,S\n',
     '352,0,1,"Williams-Lambert, Mr. Fletcher Fellows",male,,0,0,113510,35,C128,S\n',
     '353,0,3,"Elias, Mr. Tannous",male,15,1,1,2695,7.2292,,C\n',
     '354,0,3,"Arnold-Franchi, Mr. Josef",male,25,1,0,349237,17.8,,S\n',
     '355,0,3,"Yousif, Mr. Wazli",male,,0,0,2647,7.225,,C\n',
     '356,0,3,"Vanden Steen, Mr. Leo Peter",male,28,0,0,345783,9.5,,S\n',
     '357,1,1,"Bowerman, Miss. Elsie Edith",female,22,0,1,113505,55,E33,S\n',
     '358,0,2,"Funk, Miss. Annie Clemmer",female,38,0,0,237671,13,,S\n',
     '359,1,3,"McGovern, Miss. Mary",female,,0,0,330931,7.8792,,Q\n',
     '360,1,3,"Mockler, Miss. Helen Mary ""Ellie""",female,,0,0,330980,7.8792,,Q\n',
     '361,0,3,"Skoog, Mr. Wilhelm",male,40,1,4,347088,27.9,,S\n',
     '362,0,2,"del Carlo, Mr. Sebastiano",male,29,1,0,SC/PARIS 2167,27.7208,,C\n',
     '363,0,3,"Barbara, Mrs. (Catherine David)",female,45,0,1,2691,14.4542,,C\n',
     '364,0,3,"Asim, Mr. Adola",male,35,0,0,SOTON/O.Q. 3101310,7.05,,S\n',
     '365,0,3,"O\'Brien, Mr. Thomas",male,,1,0,370365,15.5,,Q\n',
     '366,0,3,"Adahl, Mr. Mauritz Nils Martin",male,30,0,0,C 7076,7.25,,S\n',
     '367,1,1,"Warren, Mrs. Frank Manley (Anna Sophia Atkinson)",female,60,1,0,110813,75.25,D37,C\n',
     '368,1,3,"Moussa, Mrs. (Mantoura Boulos)",female,,0,0,2626,7.2292,,C\n',
     '369,1,3,"Jermyn, Miss. Annie",female,,0,0,14313,7.75,,Q\n',
     '370,1,1,"Aubart, Mme. Leontine Pauline",female,24,0,0,PC 17477,69.3,B35,C\n',
     '371,1,1,"Harder, Mr. George Achilles",male,25,1,0,11765,55.4417,E50,C\n',
     '372,0,3,"Wiklund, Mr. Jakob Alfred",male,18,1,0,3101267,6.4958,,S\n',
     '373,0,3,"Beavan, Mr. William Thomas",male,19,0,0,323951,8.05,,S\n',
     '374,0,1,"Ringhini, Mr. Sante",male,22,0,0,PC 17760,135.6333,,C\n',
     '375,0,3,"Palsson, Miss. Stina Viola",female,3,3,1,349909,21.075,,S\n',
     '376,1,1,"Meyer, Mrs. Edgar Joseph (Leila Saks)",female,,1,0,PC 17604,82.1708,,C\n',
     '377,1,3,"Landergren, Miss. Aurora Adelia",female,22,0,0,C 7077,7.25,,S\n',
     '378,0,1,"Widener, Mr. Harry Elkins",male,27,0,2,113503,211.5,C82,C\n',
     '379,0,3,"Betros, Mr. Tannous",male,20,0,0,2648,4.0125,,C\n',
     '380,0,3,"Gustafsson, Mr. Karl Gideon",male,19,0,0,347069,7.775,,S\n',
     '381,1,1,"Bidois, Miss. Rosalie",female,42,0,0,PC 17757,227.525,,C\n',
     '382,1,3,"Nakid, Miss. Maria (""Mary"")",female,1,0,2,2653,15.7417,,C\n',
     '383,0,3,"Tikkanen, Mr. Juho",male,32,0,0,STON/O 2. 3101293,7.925,,S\n',
     '384,1,1,"Holverson, Mrs. Alexander Oskar (Mary Aline Towner)",female,35,1,0,113789,52,,S\n',
     '385,0,3,"Plotcharsky, Mr. Vasil",male,,0,0,349227,7.8958,,S\n',
     '386,0,2,"Davies, Mr. Charles Henry",male,18,0,0,S.O.C. 14879,73.5,,S\n',
     '387,0,3,"Goodwin, Master. Sidney Leonard",male,1,5,2,CA 2144,46.9,,S\n',
     '388,1,2,"Buss, Miss. Kate",female,36,0,0,27849,13,,S\n',
     '389,0,3,"Sadlier, Mr. Matthew",male,,0,0,367655,7.7292,,Q\n',
     '390,1,2,"Lehmann, Miss. Bertha",female,17,0,0,SC 1748,12,,C\n',
     '391,1,1,"Carter, Mr. William Ernest",male,36,1,2,113760,120,B96 B98,S\n',
     '392,1,3,"Jansson, Mr. Carl Olof",male,21,0,0,350034,7.7958,,S\n',
     '393,0,3,"Gustafsson, Mr. Johan Birger",male,28,2,0,3101277,7.925,,S\n',
     '394,1,1,"Newell, Miss. Marjorie",female,23,1,0,35273,113.275,D36,C\n',
     '395,1,3,"Sandstrom, Mrs. Hjalmar (Agnes Charlotta Bengtsson)",female,24,0,2,PP 9549,16.7,G6,S\n',
     '396,0,3,"Johansson, Mr. Erik",male,22,0,0,350052,7.7958,,S\n',
     '397,0,3,"Olsson, Miss. Elina",female,31,0,0,350407,7.8542,,S\n',
     '398,0,2,"McKane, Mr. Peter David",male,46,0,0,28403,26,,S\n',
     '399,0,2,"Pain, Dr. Alfred",male,23,0,0,244278,10.5,,S\n',
     '400,1,2,"Trout, Mrs. William H (Jessie L)",female,28,0,0,240929,12.65,,S\n',
     '401,1,3,"Niskanen, Mr. Juha",male,39,0,0,STON/O 2. 3101289,7.925,,S\n',
     '402,0,3,"Adams, Mr. John",male,26,0,0,341826,8.05,,S\n',
     '403,0,3,"Jussila, Miss. Mari Aina",female,21,1,0,4137,9.825,,S\n',
     '404,0,3,"Hakkarainen, Mr. Pekka Pietari",male,28,1,0,STON/O2. 3101279,15.85,,S\n',
     '405,0,3,"Oreskovic, Miss. Marija",female,20,0,0,315096,8.6625,,S\n',
     '406,0,2,"Gale, Mr. Shadrach",male,34,1,0,28664,21,,S\n',
     '407,0,3,"Widegren, Mr. Carl/Charles Peter",male,51,0,0,347064,7.75,,S\n',
     '408,1,2,"Richards, Master. William Rowe",male,3,1,1,29106,18.75,,S\n',
     '409,0,3,"Birkeland, Mr. Hans Martin Monsen",male,21,0,0,312992,7.775,,S\n',
     '410,0,3,"Lefebre, Miss. Ida",female,,3,1,4133,25.4667,,S\n',
     '411,0,3,"Sdycoff, Mr. Todor",male,,0,0,349222,7.8958,,S\n',
     '412,0,3,"Hart, Mr. Henry",male,,0,0,394140,6.8583,,Q\n',
     '413,1,1,"Minahan, Miss. Daisy E",female,33,1,0,19928,90,C78,Q\n',
     '414,0,2,"Cunningham, Mr. Alfred Fleming",male,,0,0,239853,0,,S\n',
     '415,1,3,"Sundman, Mr. Johan Julian",male,44,0,0,STON/O 2. 3101269,7.925,,S\n',
     '416,0,3,"Meek, Mrs. Thomas (Annie Louise Rowley)",female,,0,0,343095,8.05,,S\n',
     '417,1,2,"Drew, Mrs. James Vivian (Lulu Thorne Christian)",female,34,1,1,28220,32.5,,S\n',
     '418,1,2,"Silven, Miss. Lyyli Karoliina",female,18,0,2,250652,13,,S\n',
     '419,0,2,"Matthews, Mr. William John",male,30,0,0,28228,13,,S\n',
     '420,0,3,"Van Impe, Miss. Catharina",female,10,0,2,345773,24.15,,S\n',
     '421,0,3,"Gheorgheff, Mr. Stanio",male,,0,0,349254,7.8958,,C\n',
     '422,0,3,"Charters, Mr. David",male,21,0,0,A/5. 13032,7.7333,,Q\n',
     '423,0,3,"Zimmerman, Mr. Leo",male,29,0,0,315082,7.875,,S\n',
     '424,0,3,"Danbom, Mrs. Ernst Gilbert (Anna Sigrid Maria Brogren)",female,28,1,1,347080,14.4,,S\n',
     '425,0,3,"Rosblom, Mr. Viktor Richard",male,18,1,1,370129,20.2125,,S\n',
     '426,0,3,"Wiseman, Mr. Phillippe",male,,0,0,A/4. 34244,7.25,,S\n',
     '427,1,2,"Clarke, Mrs. Charles V (Ada Maria Winfield)",female,28,1,0,2003,26,,S\n',
     '428,1,2,"Phillips, Miss. Kate Florence (""Mrs Kate Louise Phillips Marshall"")",female,19,0,0,250655,26,,S\n',
     '429,0,3,"Flynn, Mr. James",male,,0,0,364851,7.75,,Q\n',
     '430,1,3,"Pickard, Mr. Berk (Berk Trembisky)",male,32,0,0,SOTON/O.Q. 392078,8.05,E10,S\n',
     '431,1,1,"Bjornstrom-Steffansson, Mr. Mauritz Hakan",male,28,0,0,110564,26.55,C52,S\n',
     '432,1,3,"Thorneycroft, Mrs. Percival (Florence Kate White)",female,,1,0,376564,16.1,,S\n',
     '433,1,2,"Louch, Mrs. Charles Alexander (Alice Adelaide Slow)",female,42,1,0,SC/AH 3085,26,,S\n',
     '434,0,3,"Kallio, Mr. Nikolai Erland",male,17,0,0,STON/O 2. 3101274,7.125,,S\n',
     '435,0,1,"Silvey, Mr. William Baird",male,50,1,0,13507,55.9,E44,S\n',
     '436,1,1,"Carter, Miss. Lucile Polk",female,14,1,2,113760,120,B96 B98,S\n',
     '437,0,3,"Ford, Miss. Doolina Margaret ""Daisy""",female,21,2,2,W./C. 6608,34.375,,S\n',
     '438,1,2,"Richards, Mrs. Sidney (Emily Hocking)",female,24,2,3,29106,18.75,,S\n',
     '439,0,1,"Fortune, Mr. Mark",male,64,1,4,19950,263,C23 C25 C27,S\n',
     '440,0,2,"Kvillner, Mr. Johan Henrik Johannesson",male,31,0,0,C.A. 18723,10.5,,S\n',
     '441,1,2,"Hart, Mrs. Benjamin (Esther Ada Bloomfield)",female,45,1,1,F.C.C. 13529,26.25,,S\n',
     '442,0,3,"Hampe, Mr. Leon",male,20,0,0,345769,9.5,,S\n',
     '443,0,3,"Petterson, Mr. Johan Emil",male,25,1,0,347076,7.775,,S\n',
     '444,1,2,"Reynaldo, Ms. Encarnacion",female,28,0,0,230434,13,,S\n',
     '445,1,3,"Johannesen-Bratthammer, Mr. Bernt",male,,0,0,65306,8.1125,,S\n',
     '446,1,1,"Dodge, Master. Washington",male,4,0,2,33638,81.8583,A34,S\n',
     '447,1,2,"Mellinger, Miss. Madeleine Violet",female,13,0,1,250644,19.5,,S\n',
     '448,1,1,"Seward, Mr. Frederic Kimber",male,34,0,0,113794,26.55,,S\n',
     '449,1,3,"Baclini, Miss. Marie Catherine",female,5,2,1,2666,19.2583,,C\n',
     '450,1,1,"Peuchen, Major. Arthur Godfrey",male,52,0,0,113786,30.5,C104,S\n',
     '451,0,2,"West, Mr. Edwy Arthur",male,36,1,2,C.A. 34651,27.75,,S\n',
     '452,0,3,"Hagland, Mr. Ingvald Olai Olsen",male,,1,0,65303,19.9667,,S\n',
     '453,0,1,"Foreman, Mr. Benjamin Laventall",male,30,0,0,113051,27.75,C111,C\n',
     '454,1,1,"Goldenberg, Mr. Samuel L",male,49,1,0,17453,89.1042,C92,C\n',
     '455,0,3,"Peduzzi, Mr. Joseph",male,,0,0,A/5 2817,8.05,,S\n',
     '456,1,3,"Jalsevac, Mr. Ivan",male,29,0,0,349240,7.8958,,C\n',
     '457,0,1,"Millet, Mr. Francis Davis",male,65,0,0,13509,26.55,E38,S\n',
     '458,1,1,"Kenyon, Mrs. Frederick R (Marion)",female,,1,0,17464,51.8625,D21,S\n',
     '459,1,2,"Toomey, Miss. Ellen",female,50,0,0,F.C.C. 13531,10.5,,S\n',
     '460,0,3,"O\'Connor, Mr. Maurice",male,,0,0,371060,7.75,,Q\n',
     '461,1,1,"Anderson, Mr. Harry",male,48,0,0,19952,26.55,E12,S\n',
     '462,0,3,"Morley, Mr. William",male,34,0,0,364506,8.05,,S\n',
     '463,0,1,"Gee, Mr. Arthur H",male,47,0,0,111320,38.5,E63,S\n',
     '464,0,2,"Milling, Mr. Jacob Christian",male,48,0,0,234360,13,,S\n',
     '465,0,3,"Maisner, Mr. Simon",male,,0,0,A/S 2816,8.05,,S\n',
     '466,0,3,"Goncalves, Mr. Manuel Estanslas",male,38,0,0,SOTON/O.Q. 3101306,7.05,,S\n',
     '467,0,2,"Campbell, Mr. William",male,,0,0,239853,0,,S\n',
     '468,0,1,"Smart, Mr. John Montgomery",male,56,0,0,113792,26.55,,S\n',
     '469,0,3,"Scanlan, Mr. James",male,,0,0,36209,7.725,,Q\n',
     '470,1,3,"Baclini, Miss. Helene Barbara",female,0.75,2,1,2666,19.2583,,C\n',
     '471,0,3,"Keefe, Mr. Arthur",male,,0,0,323592,7.25,,S\n',
     '472,0,3,"Cacic, Mr. Luka",male,38,0,0,315089,8.6625,,S\n',
     '473,1,2,"West, Mrs. Edwy Arthur (Ada Mary Worth)",female,33,1,2,C.A. 34651,27.75,,S\n',
     '474,1,2,"Jerwan, Mrs. Amin S (Marie Marthe Thuillard)",female,23,0,0,SC/AH Basle 541,13.7917,D,C\n',
     '475,0,3,"Strandberg, Miss. Ida Sofia",female,22,0,0,7553,9.8375,,S\n',
     '476,0,1,"Clifford, Mr. George Quincy",male,,0,0,110465,52,A14,S\n',
     '477,0,2,"Renouf, Mr. Peter Henry",male,34,1,0,31027,21,,S\n',
     '478,0,3,"Braund, Mr. Lewis Richard",male,29,1,0,3460,7.0458,,S\n',
     '479,0,3,"Karlsson, Mr. Nils August",male,22,0,0,350060,7.5208,,S\n',
     '480,1,3,"Hirvonen, Miss. Hildur E",female,2,0,1,3101298,12.2875,,S\n',
     '481,0,3,"Goodwin, Master. Harold Victor",male,9,5,2,CA 2144,46.9,,S\n',
     '482,0,2,"Frost, Mr. Anthony Wood ""Archie""",male,,0,0,239854,0,,S\n',
     '483,0,3,"Rouse, Mr. Richard Henry",male,50,0,0,A/5 3594,8.05,,S\n',
     '484,1,3,"Turkula, Mrs. (Hedwig)",female,63,0,0,4134,9.5875,,S\n',
     '485,1,1,"Bishop, Mr. Dickinson H",male,25,1,0,11967,91.0792,B49,C\n',
     '486,0,3,"Lefebre, Miss. Jeannie",female,,3,1,4133,25.4667,,S\n',
     '487,1,1,"Hoyt, Mrs. Frederick Maxfield (Jane Anne Forby)",female,35,1,0,19943,90,C93,S\n',
     '488,0,1,"Kent, Mr. Edward Austin",male,58,0,0,11771,29.7,B37,C\n',
     '489,0,3,"Somerton, Mr. Francis William",male,30,0,0,A.5. 18509,8.05,,S\n',
     '490,1,3,"Coutts, Master. Eden Leslie ""Neville""",male,9,1,1,C.A. 37671,15.9,,S\n',
     '491,0,3,"Hagland, Mr. Konrad Mathias Reiersen",male,,1,0,65304,19.9667,,S\n',
     '492,0,3,"Windelov, Mr. Einar",male,21,0,0,SOTON/OQ 3101317,7.25,,S\n',
     '493,0,1,"Molson, Mr. Harry Markland",male,55,0,0,113787,30.5,C30,S\n',
     '494,0,1,"Artagaveytia, Mr. Ramon",male,71,0,0,PC 17609,49.5042,,C\n',
     '495,0,3,"Stanley, Mr. Edward Roland",male,21,0,0,A/4 45380,8.05,,S\n',
     '496,0,3,"Yousseff, Mr. Gerious",male,,0,0,2627,14.4583,,C\n',
     '497,1,1,"Eustis, Miss. Elizabeth Mussey",female,54,1,0,36947,78.2667,D20,C\n',
     '498,0,3,"Shellard, Mr. Frederick William",male,,0,0,C.A. 6212,15.1,,S\n',
     '499,0,1,"Allison, Mrs. Hudson J C (Bessie Waldo Daniels)",female,25,1,2,113781,151.55,C22 C26,S\n',
     '500,0,3,"Svensson, Mr. Olof",male,24,0,0,350035,7.7958,,S\n',
     '501,0,3,"Calic, Mr. Petar",male,17,0,0,315086,8.6625,,S\n',
     '502,0,3,"Canavan, Miss. Mary",female,21,0,0,364846,7.75,,Q\n',
     '503,0,3,"O\'Sullivan, Miss. Bridget Mary",female,,0,0,330909,7.6292,,Q\n',
     '504,0,3,"Laitinen, Miss. Kristina Sofia",female,37,0,0,4135,9.5875,,S\n',
     '505,1,1,"Maioni, Miss. Roberta",female,16,0,0,110152,86.5,B79,S\n',
     '506,0,1,"Penasco y Castellana, Mr. Victor de Satode",male,18,1,0,PC 17758,108.9,C65,C\n',
     '507,1,2,"Quick, Mrs. Frederick Charles (Jane Richards)",female,33,0,2,26360,26,,S\n',
     '508,1,1,"Bradley, Mr. George (""George Arthur Brayton"")",male,,0,0,111427,26.55,,S\n',
     '509,0,3,"Olsen, Mr. Henry Margido",male,28,0,0,C 4001,22.525,,S\n',
     '510,1,3,"Lang, Mr. Fang",male,26,0,0,1601,56.4958,,S\n',
     '511,1,3,"Daly, Mr. Eugene Patrick",male,29,0,0,382651,7.75,,Q\n',
     '512,0,3,"Webber, Mr. James",male,,0,0,SOTON/OQ 3101316,8.05,,S\n',
     '513,1,1,"McGough, Mr. James Robert",male,36,0,0,PC 17473,26.2875,E25,S\n',
     '514,1,1,"Rothschild, Mrs. Martin (Elizabeth L. Barrett)",female,54,1,0,PC 17603,59.4,,C\n',
     '515,0,3,"Coleff, Mr. Satio",male,24,0,0,349209,7.4958,,S\n',
     '516,0,1,"Walker, Mr. William Anderson",male,47,0,0,36967,34.0208,D46,S\n',
     '517,1,2,"Lemore, Mrs. (Amelia Milley)",female,34,0,0,C.A. 34260,10.5,F33,S\n',
     '518,0,3,"Ryan, Mr. Patrick",male,,0,0,371110,24.15,,Q\n',
     '519,1,2,"Angle, Mrs. William A (Florence ""Mary"" Agnes Hughes)",female,36,1,0,226875,26,,S\n',
     '520,0,3,"Pavlovic, Mr. Stefo",male,32,0,0,349242,7.8958,,S\n',
     '521,1,1,"Perreault, Miss. Anne",female,30,0,0,12749,93.5,B73,S\n',
     '522,0,3,"Vovk, Mr. Janko",male,22,0,0,349252,7.8958,,S\n',
     '523,0,3,"Lahoud, Mr. Sarkis",male,,0,0,2624,7.225,,C\n',
     '524,1,1,"Hippach, Mrs. Louis Albert (Ida Sophia Fischer)",female,44,0,1,111361,57.9792,B18,C\n',
     '525,0,3,"Kassem, Mr. Fared",male,,0,0,2700,7.2292,,C\n',
     '526,0,3,"Farrell, Mr. James",male,40.5,0,0,367232,7.75,,Q\n',
     '527,1,2,"Ridsdale, Miss. Lucy",female,50,0,0,W./C. 14258,10.5,,S\n',
     '528,0,1,"Farthing, Mr. John",male,,0,0,PC 17483,221.7792,C95,S\n',
     '529,0,3,"Salonen, Mr. Johan Werner",male,39,0,0,3101296,7.925,,S\n',
     '530,0,2,"Hocking, Mr. Richard George",male,23,2,1,29104,11.5,,S\n',
     '531,1,2,"Quick, Miss. Phyllis May",female,2,1,1,26360,26,,S\n',
     '532,0,3,"Toufik, Mr. Nakli",male,,0,0,2641,7.2292,,C\n',
     '533,0,3,"Elias, Mr. Joseph Jr",male,17,1,1,2690,7.2292,,C\n',
     '534,1,3,"Peter, Mrs. Catherine (Catherine Rizk)",female,,0,2,2668,22.3583,,C\n',
     '535,0,3,"Cacic, Miss. Marija",female,30,0,0,315084,8.6625,,S\n',
     '536,1,2,"Hart, Miss. Eva Miriam",female,7,0,2,F.C.C. 13529,26.25,,S\n',
     '537,0,1,"Butt, Major. Archibald Willingham",male,45,0,0,113050,26.55,B38,S\n',
     '538,1,1,"LeRoy, Miss. Bertha",female,30,0,0,PC 17761,106.425,,C\n',
     '539,0,3,"Risien, Mr. Samuel Beard",male,,0,0,364498,14.5,,S\n',
     '540,1,1,"Frolicher, Miss. Hedwig Margaritha",female,22,0,2,13568,49.5,B39,C\n',
     '541,1,1,"Crosby, Miss. Harriet R",female,36,0,2,WE/P 5735,71,B22,S\n',
     '542,0,3,"Andersson, Miss. Ingeborg Constanzia",female,9,4,2,347082,31.275,,S\n',
     '543,0,3,"Andersson, Miss. Sigrid Elisabeth",female,11,4,2,347082,31.275,,S\n',
     '544,1,2,"Beane, Mr. Edward",male,32,1,0,2908,26,,S\n',
     '545,0,1,"Douglas, Mr. Walter Donald",male,50,1,0,PC 17761,106.425,C86,C\n',
     '546,0,1,"Nicholson, Mr. Arthur Ernest",male,64,0,0,693,26,,S\n',
     '547,1,2,"Beane, Mrs. Edward (Ethel Clarke)",female,19,1,0,2908,26,,S\n',
     '548,1,2,"Padro y Manent, Mr. Julian",male,,0,0,SC/PARIS 2146,13.8625,,C\n',
     '549,0,3,"Goldsmith, Mr. Frank John",male,33,1,1,363291,20.525,,S\n',
     '550,1,2,"Davies, Master. John Morgan Jr",male,8,1,1,C.A. 33112,36.75,,S\n',
     '551,1,1,"Thayer, Mr. John Borland Jr",male,17,0,2,17421,110.8833,C70,C\n',
     '552,0,2,"Sharp, Mr. Percival James R",male,27,0,0,244358,26,,S\n',
     '553,0,3,"O\'Brien, Mr. Timothy",male,,0,0,330979,7.8292,,Q\n',
     '554,1,3,"Leeni, Mr. Fahim (""Philip Zenni"")",male,22,0,0,2620,7.225,,C\n',
     '555,1,3,"Ohman, Miss. Velin",female,22,0,0,347085,7.775,,S\n',
     '556,0,1,"Wright, Mr. George",male,62,0,0,113807,26.55,,S\n',
     '557,1,1,"Duff Gordon, Lady. (Lucille Christiana Sutherland) (""Mrs Morgan"")",female,48,1,0,11755,39.6,A16,C\n',
     '558,0,1,"Robbins, Mr. Victor",male,,0,0,PC 17757,227.525,,C\n',
     '559,1,1,"Taussig, Mrs. Emil (Tillie Mandelbaum)",female,39,1,1,110413,79.65,E67,S\n',
     '560,1,3,"de Messemaeker, Mrs. Guillaume Joseph (Emma)",female,36,1,0,345572,17.4,,S\n',
     '561,0,3,"Morrow, Mr. Thomas Rowan",male,,0,0,372622,7.75,,Q\n',
     '562,0,3,"Sivic, Mr. Husein",male,40,0,0,349251,7.8958,,S\n',
     '563,0,2,"Norman, Mr. Robert Douglas",male,28,0,0,218629,13.5,,S\n',
     '564,0,3,"Simmons, Mr. John",male,,0,0,SOTON/OQ 392082,8.05,,S\n',
     '565,0,3,"Meanwell, Miss. (Marion Ogden)",female,,0,0,SOTON/O.Q. 392087,8.05,,S\n',
     '566,0,3,"Davies, Mr. Alfred J",male,24,2,0,A/4 48871,24.15,,S\n',
     '567,0,3,"Stoytcheff, Mr. Ilia",male,19,0,0,349205,7.8958,,S\n',
     '568,0,3,"Palsson, Mrs. Nils (Alma Cornelia Berglund)",female,29,0,4,349909,21.075,,S\n',
     '569,0,3,"Doharr, Mr. Tannous",male,,0,0,2686,7.2292,,C\n',
     '570,1,3,"Jonsson, Mr. Carl",male,32,0,0,350417,7.8542,,S\n',
     '571,1,2,"Harris, Mr. George",male,62,0,0,S.W./PP 752,10.5,,S\n',
     '572,1,1,"Appleton, Mrs. Edward Dale (Charlotte Lamson)",female,53,2,0,11769,51.4792,C101,S\n',
     '573,1,1,"Flynn, Mr. John Irwin (""Irving"")",male,36,0,0,PC 17474,26.3875,E25,S\n',
     '574,1,3,"Kelly, Miss. Mary",female,,0,0,14312,7.75,,Q\n',
     '575,0,3,"Rush, Mr. Alfred George John",male,16,0,0,A/4. 20589,8.05,,S\n',
     '576,0,3,"Patchett, Mr. George",male,19,0,0,358585,14.5,,S\n',
     '577,1,2,"Garside, Miss. Ethel",female,34,0,0,243880,13,,S\n',
     '578,1,1,"Silvey, Mrs. William Baird (Alice Munger)",female,39,1,0,13507,55.9,E44,S\n',
     '579,0,3,"Caram, Mrs. Joseph (Maria Elias)",female,,1,0,2689,14.4583,,C\n',
     '580,1,3,"Jussila, Mr. Eiriik",male,32,0,0,STON/O 2. 3101286,7.925,,S\n',
     '581,1,2,"Christy, Miss. Julie Rachel",female,25,1,1,237789,30,,S\n',
     '582,1,1,"Thayer, Mrs. John Borland (Marian Longstreth Morris)",female,39,1,1,17421,110.8833,C68,C\n',
     '583,0,2,"Downton, Mr. William James",male,54,0,0,28403,26,,S\n',
     '584,0,1,"Ross, Mr. John Hugo",male,36,0,0,13049,40.125,A10,C\n',
     '585,0,3,"Paulner, Mr. Uscher",male,,0,0,3411,8.7125,,C\n',
     '586,1,1,"Taussig, Miss. Ruth",female,18,0,2,110413,79.65,E68,S\n',
     '587,0,2,"Jarvis, Mr. John Denzil",male,47,0,0,237565,15,,S\n',
     '588,1,1,"Frolicher-Stehli, Mr. Maxmillian",male,60,1,1,13567,79.2,B41,C\n',
     '589,0,3,"Gilinski, Mr. Eliezer",male,22,0,0,14973,8.05,,S\n',
     '590,0,3,"Murdlin, Mr. Joseph",male,,0,0,A./5. 3235,8.05,,S\n',
     '591,0,3,"Rintamaki, Mr. Matti",male,35,0,0,STON/O 2. 3101273,7.125,,S\n',
     '592,1,1,"Stephenson, Mrs. Walter Bertram (Martha Eustis)",female,52,1,0,36947,78.2667,D20,C\n',
     '593,0,3,"Elsbury, Mr. William James",male,47,0,0,A/5 3902,7.25,,S\n',
     '594,0,3,"Bourke, Miss. Mary",female,,0,2,364848,7.75,,Q\n',
     '595,0,2,"Chapman, Mr. John Henry",male,37,1,0,SC/AH 29037,26,,S\n',
     '596,0,3,"Van Impe, Mr. Jean Baptiste",male,36,1,1,345773,24.15,,S\n',
     '597,1,2,"Leitch, Miss. Jessie Wills",female,,0,0,248727,33,,S\n',
     '598,0,3,"Johnson, Mr. Alfred",male,49,0,0,LINE,0,,S\n',
     '599,0,3,"Boulos, Mr. Hanna",male,,0,0,2664,7.225,,C\n',
     '600,1,1,"Duff Gordon, Sir. Cosmo Edmund (""Mr Morgan"")",male,49,1,0,PC 17485,56.9292,A20,C\n',
     '601,1,2,"Jacobsohn, Mrs. Sidney Samuel (Amy Frances Christy)",female,24,2,1,243847,27,,S\n',
     '602,0,3,"Slabenoff, Mr. Petco",male,,0,0,349214,7.8958,,S\n',
     '603,0,1,"Harrington, Mr. Charles H",male,,0,0,113796,42.4,,S\n',
     '604,0,3,"Torber, Mr. Ernst William",male,44,0,0,364511,8.05,,S\n',
     '605,1,1,"Homer, Mr. Harry (""Mr E Haven"")",male,35,0,0,111426,26.55,,C\n',
     '606,0,3,"Lindell, Mr. Edvard Bengtsson",male,36,1,0,349910,15.55,,S\n',
     '607,0,3,"Karaic, Mr. Milan",male,30,0,0,349246,7.8958,,S\n',
     '608,1,1,"Daniel, Mr. Robert Williams",male,27,0,0,113804,30.5,,S\n',
     '609,1,2,"Laroche, Mrs. Joseph (Juliette Marie Louise Lafargue)",female,22,1,2,SC/Paris 2123,41.5792,,C\n',
     '610,1,1,"Shutes, Miss. Elizabeth W",female,40,0,0,PC 17582,153.4625,C125,S\n',
     '611,0,3,"Andersson, Mrs. Anders Johan (Alfrida Konstantia Brogren)",female,39,1,5,347082,31.275,,S\n',
     '612,0,3,"Jardin, Mr. Jose Neto",male,,0,0,SOTON/O.Q. 3101305,7.05,,S\n',
     '613,1,3,"Murphy, Miss. Margaret Jane",female,,1,0,367230,15.5,,Q\n',
     '614,0,3,"Horgan, Mr. John",male,,0,0,370377,7.75,,Q\n',
     '615,0,3,"Brocklebank, Mr. William Alfred",male,35,0,0,364512,8.05,,S\n',
     '616,1,2,"Herman, Miss. Alice",female,24,1,2,220845,65,,S\n',
     '617,0,3,"Danbom, Mr. Ernst Gilbert",male,34,1,1,347080,14.4,,S\n',
     '618,0,3,"Lobb, Mrs. William Arthur (Cordelia K Stanlick)",female,26,1,0,A/5. 3336,16.1,,S\n',
     '619,1,2,"Becker, Miss. Marion Louise",female,4,2,1,230136,39,F4,S\n',
     '620,0,2,"Gavey, Mr. Lawrence",male,26,0,0,31028,10.5,,S\n',
     '621,0,3,"Yasbeck, Mr. Antoni",male,27,1,0,2659,14.4542,,C\n',
     '622,1,1,"Kimball, Mr. Edwin Nelson Jr",male,42,1,0,11753,52.5542,D19,S\n',
     '623,1,3,"Nakid, Mr. Sahid",male,20,1,1,2653,15.7417,,C\n',
     '624,0,3,"Hansen, Mr. Henry Damsgaard",male,21,0,0,350029,7.8542,,S\n',
     '625,0,3,"Bowen, Mr. David John ""Dai""",male,21,0,0,54636,16.1,,S\n',
     '626,0,1,"Sutton, Mr. Frederick",male,61,0,0,36963,32.3208,D50,S\n',
     '627,0,2,"Kirkland, Rev. Charles Leonard",male,57,0,0,219533,12.35,,Q\n',
     '628,1,1,"Longley, Miss. Gretchen Fiske",female,21,0,0,13502,77.9583,D9,S\n',
     '629,0,3,"Bostandyeff, Mr. Guentcho",male,26,0,0,349224,7.8958,,S\n',
     '630,0,3,"O\'Connell, Mr. Patrick D",male,,0,0,334912,7.7333,,Q\n',
     '631,1,1,"Barkworth, Mr. Algernon Henry Wilson",male,80,0,0,27042,30,A23,S\n',
     '632,0,3,"Lundahl, Mr. Johan Svensson",male,51,0,0,347743,7.0542,,S\n',
     '633,1,1,"Stahelin-Maeglin, Dr. Max",male,32,0,0,13214,30.5,B50,C\n',
     '634,0,1,"Parr, Mr. William Henry Marsh",male,,0,0,112052,0,,S\n',
     '635,0,3,"Skoog, Miss. Mabel",female,9,3,2,347088,27.9,,S\n',
     '636,1,2,"Davis, Miss. Mary",female,28,0,0,237668,13,,S\n',
     '637,0,3,"Leinonen, Mr. Antti Gustaf",male,32,0,0,STON/O 2. 3101292,7.925,,S\n',
     '638,0,2,"Collyer, Mr. Harvey",male,31,1,1,C.A. 31921,26.25,,S\n',
     '639,0,3,"Panula, Mrs. Juha (Maria Emilia Ojala)",female,41,0,5,3101295,39.6875,,S\n',
     '640,0,3,"Thorneycroft, Mr. Percival",male,,1,0,376564,16.1,,S\n',
     '641,0,3,"Jensen, Mr. Hans Peder",male,20,0,0,350050,7.8542,,S\n',
     '642,1,1,"Sagesser, Mlle. Emma",female,24,0,0,PC 17477,69.3,B35,C\n',
     '643,0,3,"Skoog, Miss. Margit Elizabeth",female,2,3,2,347088,27.9,,S\n',
     '644,1,3,"Foo, Mr. Choong",male,,0,0,1601,56.4958,,S\n',
     '645,1,3,"Baclini, Miss. Eugenie",female,0.75,2,1,2666,19.2583,,C\n',
     '646,1,1,"Harper, Mr. Henry Sleeper",male,48,1,0,PC 17572,76.7292,D33,C\n',
     '647,0,3,"Cor, Mr. Liudevit",male,19,0,0,349231,7.8958,,S\n',
     '648,1,1,"Simonius-Blumer, Col. Oberst Alfons",male,56,0,0,13213,35.5,A26,C\n',
     '649,0,3,"Willey, Mr. Edward",male,,0,0,S.O./P.P. 751,7.55,,S\n',
     '650,1,3,"Stanley, Miss. Amy Zillah Elsie",female,23,0,0,CA. 2314,7.55,,S\n',
     '651,0,3,"Mitkoff, Mr. Mito",male,,0,0,349221,7.8958,,S\n',
     '652,1,2,"Doling, Miss. Elsie",female,18,0,1,231919,23,,S\n',
     '653,0,3,"Kalvik, Mr. Johannes Halvorsen",male,21,0,0,8475,8.4333,,S\n',
     '654,1,3,"O\'Leary, Miss. Hanora ""Norah""",female,,0,0,330919,7.8292,,Q\n',
     '655,0,3,"Hegarty, Miss. Hanora ""Nora""",female,18,0,0,365226,6.75,,Q\n',
     '656,0,2,"Hickman, Mr. Leonard Mark",male,24,2,0,S.O.C. 14879,73.5,,S\n',
     '657,0,3,"Radeff, Mr. Alexander",male,,0,0,349223,7.8958,,S\n',
     '658,0,3,"Bourke, Mrs. John (Catherine)",female,32,1,1,364849,15.5,,Q\n',
     '659,0,2,"Eitemiller, Mr. George Floyd",male,23,0,0,29751,13,,S\n',
     '660,0,1,"Newell, Mr. Arthur Webster",male,58,0,2,35273,113.275,D48,C\n',
     '661,1,1,"Frauenthal, Dr. Henry William",male,50,2,0,PC 17611,133.65,,S\n',
     '662,0,3,"Badt, Mr. Mohamed",male,40,0,0,2623,7.225,,C\n',
     '663,0,1,"Colley, Mr. Edward Pomeroy",male,47,0,0,5727,25.5875,E58,S\n',
     '664,0,3,"Coleff, Mr. Peju",male,36,0,0,349210,7.4958,,S\n',
     '665,1,3,"Lindqvist, Mr. Eino William",male,20,1,0,STON/O 2. 3101285,7.925,,S\n',
     '666,0,2,"Hickman, Mr. Lewis",male,32,2,0,S.O.C. 14879,73.5,,S\n',
     '667,0,2,"Butler, Mr. Reginald Fenton",male,25,0,0,234686,13,,S\n',
     '668,0,3,"Rommetvedt, Mr. Knud Paust",male,,0,0,312993,7.775,,S\n',
     '669,0,3,"Cook, Mr. Jacob",male,43,0,0,A/5 3536,8.05,,S\n',
     '670,1,1,"Taylor, Mrs. Elmer Zebley (Juliet Cummins Wright)",female,,1,0,19996,52,C126,S\n',
     '671,1,2,"Brown, Mrs. Thomas William Solomon (Elizabeth Catherine Ford)",female,40,1,1,29750,39,,S\n',
     '672,0,1,"Davidson, Mr. Thornton",male,31,1,0,F.C. 12750,52,B71,S\n',
     '673,0,2,"Mitchell, Mr. Henry Michael",male,70,0,0,C.A. 24580,10.5,,S\n',
     '674,1,2,"Wilhelms, Mr. Charles",male,31,0,0,244270,13,,S\n',
     '675,0,2,"Watson, Mr. Ennis Hastings",male,,0,0,239856,0,,S\n',
     '676,0,3,"Edvardsson, Mr. Gustaf Hjalmar",male,18,0,0,349912,7.775,,S\n',
     '677,0,3,"Sawyer, Mr. Frederick Charles",male,24.5,0,0,342826,8.05,,S\n',
     '678,1,3,"Turja, Miss. Anna Sofia",female,18,0,0,4138,9.8417,,S\n',
     '679,0,3,"Goodwin, Mrs. Frederick (Augusta Tyler)",female,43,1,6,CA 2144,46.9,,S\n',
     '680,1,1,"Cardeza, Mr. Thomas Drake Martinez",male,36,0,1,PC 17755,512.3292,B51 B53 B55,C\n',
     '681,0,3,"Peters, Miss. Katie",female,,0,0,330935,8.1375,,Q\n',
     '682,1,1,"Hassab, Mr. Hammad",male,27,0,0,PC 17572,76.7292,D49,C\n',
     '683,0,3,"Olsvigen, Mr. Thor Anderson",male,20,0,0,6563,9.225,,S\n',
     '684,0,3,"Goodwin, Mr. Charles Edward",male,14,5,2,CA 2144,46.9,,S\n',
     '685,0,2,"Brown, Mr. Thomas William Solomon",male,60,1,1,29750,39,,S\n',
     '686,0,2,"Laroche, Mr. Joseph Philippe Lemercier",male,25,1,2,SC/Paris 2123,41.5792,,C\n',
     '687,0,3,"Panula, Mr. Jaako Arnold",male,14,4,1,3101295,39.6875,,S\n',
     '688,0,3,"Dakic, Mr. Branko",male,19,0,0,349228,10.1708,,S\n',
     '689,0,3,"Fischer, Mr. Eberhard Thelander",male,18,0,0,350036,7.7958,,S\n',
     '690,1,1,"Madill, Miss. Georgette Alexandra",female,15,0,1,24160,211.3375,B5,S\n',
     '691,1,1,"Dick, Mr. Albert Adrian",male,31,1,0,17474,57,B20,S\n',
     '692,1,3,"Karun, Miss. Manca",female,4,0,1,349256,13.4167,,C\n',
     '693,1,3,"Lam, Mr. Ali",male,,0,0,1601,56.4958,,S\n',
     '694,0,3,"Saad, Mr. Khalil",male,25,0,0,2672,7.225,,C\n',
     '695,0,1,"Weir, Col. John",male,60,0,0,113800,26.55,,S\n',
     '696,0,2,"Chapman, Mr. Charles Henry",male,52,0,0,248731,13.5,,S\n',
     '697,0,3,"Kelly, Mr. James",male,44,0,0,363592,8.05,,S\n',
     '698,1,3,"Mullens, Miss. Katherine ""Katie""",female,,0,0,35852,7.7333,,Q\n',
     '699,0,1,"Thayer, Mr. John Borland",male,49,1,1,17421,110.8833,C68,C\n',
     '700,0,3,"Humblen, Mr. Adolf Mathias Nicolai Olsen",male,42,0,0,348121,7.65,F G63,S\n',
     '701,1,1,"Astor, Mrs. John Jacob (Madeleine Talmadge Force)",female,18,1,0,PC 17757,227.525,C62 C64,C\n',
     '702,1,1,"Silverthorne, Mr. Spencer Victor",male,35,0,0,PC 17475,26.2875,E24,S\n',
     '703,0,3,"Barbara, Miss. Saiide",female,18,0,1,2691,14.4542,,C\n',
     '704,0,3,"Gallagher, Mr. Martin",male,25,0,0,36864,7.7417,,Q\n',
     '705,0,3,"Hansen, Mr. Henrik Juul",male,26,1,0,350025,7.8542,,S\n',
     '706,0,2,"Morley, Mr. Henry Samuel (""Mr Henry Marshall"")",male,39,0,0,250655,26,,S\n',
     '707,1,2,"Kelly, Mrs. Florence ""Fannie""",female,45,0,0,223596,13.5,,S\n',
     '708,1,1,"Calderhead, Mr. Edward Pennington",male,42,0,0,PC 17476,26.2875,E24,S\n',
     '709,1,1,"Cleaver, Miss. Alice",female,22,0,0,113781,151.55,,S\n',
     '710,1,3,"Moubarek, Master. Halim Gonios (""William George"")",male,,1,1,2661,15.2458,,C\n',
     '711,1,1,"Mayne, Mlle. Berthe Antonine (""Mrs de Villiers"")",female,24,0,0,PC 17482,49.5042,C90,C\n',
     '712,0,1,"Klaber, Mr. Herman",male,,0,0,113028,26.55,C124,S\n',
     '713,1,1,"Taylor, Mr. Elmer Zebley",male,48,1,0,19996,52,C126,S\n',
     '714,0,3,"Larsson, Mr. August Viktor",male,29,0,0,7545,9.4833,,S\n',
     '715,0,2,"Greenberg, Mr. Samuel",male,52,0,0,250647,13,,S\n',
     '716,0,3,"Soholt, Mr. Peter Andreas Lauritz Andersen",male,19,0,0,348124,7.65,F G73,S\n',
     '717,1,1,"Endres, Miss. Caroline Louise",female,38,0,0,PC 17757,227.525,C45,C\n',
     '718,1,2,"Troutt, Miss. Edwina Celia ""Winnie""",female,27,0,0,34218,10.5,E101,S\n',
     '719,0,3,"McEvoy, Mr. Michael",male,,0,0,36568,15.5,,Q\n',
     '720,0,3,"Johnson, Mr. Malkolm Joackim",male,33,0,0,347062,7.775,,S\n',
     '721,1,2,"Harper, Miss. Annie Jessie ""Nina""",female,6,0,1,248727,33,,S\n',
     '722,0,3,"Jensen, Mr. Svend Lauritz",male,17,1,0,350048,7.0542,,S\n',
     '723,0,2,"Gillespie, Mr. William Henry",male,34,0,0,12233,13,,S\n',
     '724,0,2,"Hodges, Mr. Henry Price",male,50,0,0,250643,13,,S\n',
     '725,1,1,"Chambers, Mr. Norman Campbell",male,27,1,0,113806,53.1,E8,S\n',
     '726,0,3,"Oreskovic, Mr. Luka",male,20,0,0,315094,8.6625,,S\n',
     '727,1,2,"Renouf, Mrs. Peter Henry (Lillian Jefferys)",female,30,3,0,31027,21,,S\n',
     '728,1,3,"Mannion, Miss. Margareth",female,,0,0,36866,7.7375,,Q\n',
     '729,0,2,"Bryhl, Mr. Kurt Arnold Gottfrid",male,25,1,0,236853,26,,S\n',
     '730,0,3,"Ilmakangas, Miss. Pieta Sofia",female,25,1,0,STON/O2. 3101271,7.925,,S\n',
     '731,1,1,"Allen, Miss. Elisabeth Walton",female,29,0,0,24160,211.3375,B5,S\n',
     '732,0,3,"Hassan, Mr. Houssein G N",male,11,0,0,2699,18.7875,,C\n',
     '733,0,2,"Knight, Mr. Robert J",male,,0,0,239855,0,,S\n',
     '734,0,2,"Berriman, Mr. William John",male,23,0,0,28425,13,,S\n',
     '735,0,2,"Troupiansky, Mr. Moses Aaron",male,23,0,0,233639,13,,S\n',
     '736,0,3,"Williams, Mr. Leslie",male,28.5,0,0,54636,16.1,,S\n',
     '737,0,3,"Ford, Mrs. Edward (Margaret Ann Watson)",female,48,1,3,W./C. 6608,34.375,,S\n',
     '738,1,1,"Lesurer, Mr. Gustave J",male,35,0,0,PC 17755,512.3292,B101,C\n',
     '739,0,3,"Ivanoff, Mr. Kanio",male,,0,0,349201,7.8958,,S\n',
     '740,0,3,"Nankoff, Mr. Minko",male,,0,0,349218,7.8958,,S\n',
     '741,1,1,"Hawksford, Mr. Walter James",male,,0,0,16988,30,D45,S\n',
     '742,0,1,"Cavendish, Mr. Tyrell William",male,36,1,0,19877,78.85,C46,S\n',
     '743,1,1,"Ryerson, Miss. Susan Parker ""Suzette""",female,21,2,2,PC 17608,262.375,B57 B59 B63 B66,C\n',
     '744,0,3,"McNamee, Mr. Neal",male,24,1,0,376566,16.1,,S\n',
     '745,1,3,"Stranden, Mr. Juho",male,31,0,0,STON/O 2. 3101288,7.925,,S\n',
     '746,0,1,"Crosby, Capt. Edward Gifford",male,70,1,1,WE/P 5735,71,B22,S\n',
     '747,0,3,"Abbott, Mr. Rossmore Edward",male,16,1,1,C.A. 2673,20.25,,S\n',
     '748,1,2,"Sinkkonen, Miss. Anna",female,30,0,0,250648,13,,S\n',
     '749,0,1,"Marvin, Mr. Daniel Warner",male,19,1,0,113773,53.1,D30,S\n',
     '750,0,3,"Connaghton, Mr. Michael",male,31,0,0,335097,7.75,,Q\n',
     '751,1,2,"Wells, Miss. Joan",female,4,1,1,29103,23,,S\n',
     '752,1,3,"Moor, Master. Meier",male,6,0,1,392096,12.475,E121,S\n',
     '753,0,3,"Vande Velde, Mr. Johannes Joseph",male,33,0,0,345780,9.5,,S\n',
     '754,0,3,"Jonkoff, Mr. Lalio",male,23,0,0,349204,7.8958,,S\n',
     '755,1,2,"Herman, Mrs. Samuel (Jane Laver)",female,48,1,2,220845,65,,S\n',
     '756,1,2,"Hamalainen, Master. Viljo",male,0.67,1,1,250649,14.5,,S\n',
     '757,0,3,"Carlsson, Mr. August Sigfrid",male,28,0,0,350042,7.7958,,S\n',
     '758,0,2,"Bailey, Mr. Percy Andrew",male,18,0,0,29108,11.5,,S\n',
     '759,0,3,"Theobald, Mr. Thomas Leonard",male,34,0,0,363294,8.05,,S\n',
     '760,1,1,"Rothes, the Countess. of (Lucy Noel Martha Dyer-Edwards)",female,33,0,0,110152,86.5,B77,S\n',
     '761,0,3,"Garfirth, Mr. John",male,,0,0,358585,14.5,,S\n',
     '762,0,3,"Nirva, Mr. Iisakki Antino Aijo",male,41,0,0,SOTON/O2 3101272,7.125,,S\n',
     '763,1,3,"Barah, Mr. Hanna Assi",male,20,0,0,2663,7.2292,,C\n',
     '764,1,1,"Carter, Mrs. William Ernest (Lucile Polk)",female,36,1,2,113760,120,B96 B98,S\n',
     '765,0,3,"Eklund, Mr. Hans Linus",male,16,0,0,347074,7.775,,S\n',
     '766,1,1,"Hogeboom, Mrs. John C (Anna Andrews)",female,51,1,0,13502,77.9583,D11,S\n',
     '767,0,1,"Brewe, Dr. Arthur Jackson",male,,0,0,112379,39.6,,C\n',
     '768,0,3,"Mangan, Miss. Mary",female,30.5,0,0,364850,7.75,,Q\n',
     '769,0,3,"Moran, Mr. Daniel J",male,,1,0,371110,24.15,,Q\n',
     '770,0,3,"Gronnestad, Mr. Daniel Danielsen",male,32,0,0,8471,8.3625,,S\n',
     '771,0,3,"Lievens, Mr. Rene Aime",male,24,0,0,345781,9.5,,S\n',
     '772,0,3,"Jensen, Mr. Niels Peder",male,48,0,0,350047,7.8542,,S\n',
     '773,0,2,"Mack, Mrs. (Mary)",female,57,0,0,S.O./P.P. 3,10.5,E77,S\n',
     '774,0,3,"Elias, Mr. Dibo",male,,0,0,2674,7.225,,C\n',
     '775,1,2,"Hocking, Mrs. Elizabeth (Eliza Needs)",female,54,1,3,29105,23,,S\n',
     '776,0,3,"Myhrman, Mr. Pehr Fabian Oliver Malkolm",male,18,0,0,347078,7.75,,S\n',
     '777,0,3,"Tobin, Mr. Roger",male,,0,0,383121,7.75,F38,Q\n',
     '778,1,3,"Emanuel, Miss. Virginia Ethel",female,5,0,0,364516,12.475,,S\n',
     '779,0,3,"Kilgannon, Mr. Thomas J",male,,0,0,36865,7.7375,,Q\n',
     '780,1,1,"Robert, Mrs. Edward Scott (Elisabeth Walton McMillan)",female,43,0,1,24160,211.3375,B3,S\n',
     '781,1,3,"Ayoub, Miss. Banoura",female,13,0,0,2687,7.2292,,C\n',
     '782,1,1,"Dick, Mrs. Albert Adrian (Vera Gillespie)",female,17,1,0,17474,57,B20,S\n',
     '783,0,1,"Long, Mr. Milton Clyde",male,29,0,0,113501,30,D6,S\n',
     '784,0,3,"Johnston, Mr. Andrew G",male,,1,2,W./C. 6607,23.45,,S\n',
     '785,0,3,"Ali, Mr. William",male,25,0,0,SOTON/O.Q. 3101312,7.05,,S\n',
     '786,0,3,"Harmer, Mr. Abraham (David Lishin)",male,25,0,0,374887,7.25,,S\n',
     '787,1,3,"Sjoblom, Miss. Anna Sofia",female,18,0,0,3101265,7.4958,,S\n',
     '788,0,3,"Rice, Master. George Hugh",male,8,4,1,382652,29.125,,Q\n',
     '789,1,3,"Dean, Master. Bertram Vere",male,1,1,2,C.A. 2315,20.575,,S\n',
     '790,0,1,"Guggenheim, Mr. Benjamin",male,46,0,0,PC 17593,79.2,B82 B84,C\n',
     '791,0,3,"Keane, Mr. Andrew ""Andy""",male,,0,0,12460,7.75,,Q\n',
     '792,0,2,"Gaskell, Mr. Alfred",male,16,0,0,239865,26,,S\n',
     '793,0,3,"Sage, Miss. Stella Anna",female,,8,2,CA. 2343,69.55,,S\n',
     '794,0,1,"Hoyt, Mr. William Fisher",male,,0,0,PC 17600,30.6958,,C\n',
     '795,0,3,"Dantcheff, Mr. Ristiu",male,25,0,0,349203,7.8958,,S\n',
     '796,0,2,"Otter, Mr. Richard",male,39,0,0,28213,13,,S\n',
     '797,1,1,"Leader, Dr. Alice (Farnham)",female,49,0,0,17465,25.9292,D17,S\n',
     '798,1,3,"Osman, Mrs. Mara",female,31,0,0,349244,8.6833,,S\n',
     '799,0,3,"Ibrahim Shawah, Mr. Yousseff",male,30,0,0,2685,7.2292,,C\n',
     '800,0,3,"Van Impe, Mrs. Jean Baptiste (Rosalie Paula Govaert)",female,30,1,1,345773,24.15,,S\n',
     '801,0,2,"Ponesell, Mr. Martin",male,34,0,0,250647,13,,S\n',
     '802,1,2,"Collyer, Mrs. Harvey (Charlotte Annie Tate)",female,31,1,1,C.A. 31921,26.25,,S\n',
     '803,1,1,"Carter, Master. William Thornton II",male,11,1,2,113760,120,B96 B98,S\n',
     '804,1,3,"Thomas, Master. Assad Alexander",male,0.42,0,1,2625,8.5167,,C\n',
     '805,1,3,"Hedman, Mr. Oskar Arvid",male,27,0,0,347089,6.975,,S\n',
     '806,0,3,"Johansson, Mr. Karl Johan",male,31,0,0,347063,7.775,,S\n',
     '807,0,1,"Andrews, Mr. Thomas Jr",male,39,0,0,112050,0,A36,S\n',
     '808,0,3,"Pettersson, Miss. Ellen Natalia",female,18,0,0,347087,7.775,,S\n',
     '809,0,2,"Meyer, Mr. August",male,39,0,0,248723,13,,S\n',
     '810,1,1,"Chambers, Mrs. Norman Campbell (Bertha Griggs)",female,33,1,0,113806,53.1,E8,S\n',
     '811,0,3,"Alexander, Mr. William",male,26,0,0,3474,7.8875,,S\n',
     '812,0,3,"Lester, Mr. James",male,39,0,0,A/4 48871,24.15,,S\n',
     '813,0,2,"Slemen, Mr. Richard James",male,35,0,0,28206,10.5,,S\n',
     '814,0,3,"Andersson, Miss. Ebba Iris Alfrida",female,6,4,2,347082,31.275,,S\n',
     '815,0,3,"Tomlin, Mr. Ernest Portage",male,30.5,0,0,364499,8.05,,S\n',
     '816,0,1,"Fry, Mr. Richard",male,,0,0,112058,0,B102,S\n',
     '817,0,3,"Heininen, Miss. Wendla Maria",female,23,0,0,STON/O2. 3101290,7.925,,S\n',
     '818,0,2,"Mallet, Mr. Albert",male,31,1,1,S.C./PARIS 2079,37.0042,,C\n',
     '819,0,3,"Holm, Mr. John Fredrik Alexander",male,43,0,0,C 7075,6.45,,S\n',
     '820,0,3,"Skoog, Master. Karl Thorsten",male,10,3,2,347088,27.9,,S\n',
     '821,1,1,"Hays, Mrs. Charles Melville (Clara Jennings Gregg)",female,52,1,1,12749,93.5,B69,S\n',
     '822,1,3,"Lulic, Mr. Nikola",male,27,0,0,315098,8.6625,,S\n',
     '823,0,1,"Reuchlin, Jonkheer. John George",male,38,0,0,19972,0,,S\n',
     '824,1,3,"Moor, Mrs. (Beila)",female,27,0,1,392096,12.475,E121,S\n',
     '825,0,3,"Panula, Master. Urho Abraham",male,2,4,1,3101295,39.6875,,S\n',
     '826,0,3,"Flynn, Mr. John",male,,0,0,368323,6.95,,Q\n',
     '827,0,3,"Lam, Mr. Len",male,,0,0,1601,56.4958,,S\n',
     '828,1,2,"Mallet, Master. Andre",male,1,0,2,S.C./PARIS 2079,37.0042,,C\n',
     '829,1,3,"McCormack, Mr. Thomas Joseph",male,,0,0,367228,7.75,,Q\n',
     '830,1,1,"Stone, Mrs. George Nelson (Martha Evelyn)",female,62,0,0,113572,80,B28,\n',
     '831,1,3,"Yasbeck, Mrs. Antoni (Selini Alexander)",female,15,1,0,2659,14.4542,,C\n',
     '832,1,2,"Richards, Master. George Sibley",male,0.83,1,1,29106,18.75,,S\n',
     '833,0,3,"Saad, Mr. Amin",male,,0,0,2671,7.2292,,C\n',
     '834,0,3,"Augustsson, Mr. Albert",male,23,0,0,347468,7.8542,,S\n',
     '835,0,3,"Allum, Mr. Owen George",male,18,0,0,2223,8.3,,S\n',
     '836,1,1,"Compton, Miss. Sara Rebecca",female,39,1,1,PC 17756,83.1583,E49,C\n',
     '837,0,3,"Pasic, Mr. Jakob",male,21,0,0,315097,8.6625,,S\n',
     '838,0,3,"Sirota, Mr. Maurice",male,,0,0,392092,8.05,,S\n',
     '839,1,3,"Chip, Mr. Chang",male,32,0,0,1601,56.4958,,S\n',
     '840,1,1,"Marechal, Mr. Pierre",male,,0,0,11774,29.7,C47,C\n',
     '841,0,3,"Alhomaki, Mr. Ilmari Rudolf",male,20,0,0,SOTON/O2 3101287,7.925,,S\n',
     '842,0,2,"Mudd, Mr. Thomas Charles",male,16,0,0,S.O./P.P. 3,10.5,,S\n',
     '843,1,1,"Serepeca, Miss. Augusta",female,30,0,0,113798,31,,C\n',
     '844,0,3,"Lemberopolous, Mr. Peter L",male,34.5,0,0,2683,6.4375,,C\n',
     '845,0,3,"Culumovic, Mr. Jeso",male,17,0,0,315090,8.6625,,S\n',
     '846,0,3,"Abbing, Mr. Anthony",male,42,0,0,C.A. 5547,7.55,,S\n',
     '847,0,3,"Sage, Mr. Douglas Bullen",male,,8,2,CA. 2343,69.55,,S\n',
     '848,0,3,"Markoff, Mr. Marin",male,35,0,0,349213,7.8958,,C\n',
     '849,0,2,"Harper, Rev. John",male,28,0,1,248727,33,,S\n',
     '850,1,1,"Goldenberg, Mrs. Samuel L (Edwiga Grabowska)",female,,1,0,17453,89.1042,C92,C\n',
     '851,0,3,"Andersson, Master. Sigvard Harald Elias",male,4,4,2,347082,31.275,,S\n',
     '852,0,3,"Svensson, Mr. Johan",male,74,0,0,347060,7.775,,S\n',
     '853,0,3,"Boulos, Miss. Nourelain",female,9,1,1,2678,15.2458,,C\n',
     '854,1,1,"Lines, Miss. Mary Conover",female,16,0,1,PC 17592,39.4,D28,S\n',
     '855,0,2,"Carter, Mrs. Ernest Courtenay (Lilian Hughes)",female,44,1,0,244252,26,,S\n',
     '856,1,3,"Aks, Mrs. Sam (Leah Rosen)",female,18,0,1,392091,9.35,,S\n',
     '857,1,1,"Wick, Mrs. George Dennick (Mary Hitchcock)",female,45,1,1,36928,164.8667,,S\n',
     '858,1,1,"Daly, Mr. Peter Denis ",male,51,0,0,113055,26.55,E17,S\n',
     '859,1,3,"Baclini, Mrs. Solomon (Latifa Qurban)",female,24,0,3,2666,19.2583,,C\n',
     '860,0,3,"Razi, Mr. Raihed",male,,0,0,2629,7.2292,,C\n',
     '861,0,3,"Hansen, Mr. Claus Peter",male,41,2,0,350026,14.1083,,S\n',
     '862,0,2,"Giles, Mr. Frederick Edward",male,21,1,0,28134,11.5,,S\n',
     '863,1,1,"Swift, Mrs. Frederick Joel (Margaret Welles Barron)",female,48,0,0,17466,25.9292,D17,S\n',
     '864,0,3,"Sage, Miss. Dorothy Edith ""Dolly""",female,,8,2,CA. 2343,69.55,,S\n',
     '865,0,2,"Gill, Mr. John William",male,24,0,0,233866,13,,S\n',
     '866,1,2,"Bystrom, Mrs. (Karolina)",female,42,0,0,236852,13,,S\n',
     '867,1,2,"Duran y More, Miss. Asuncion",female,27,1,0,SC/PARIS 2149,13.8583,,C\n',
     '868,0,1,"Roebling, Mr. Washington Augustus II",male,31,0,0,PC 17590,50.4958,A24,S\n',
     '869,0,3,"van Melkebeke, Mr. Philemon",male,,0,0,345777,9.5,,S\n',
     '870,1,3,"Johnson, Master. Harold Theodor",male,4,1,1,347742,11.1333,,S\n',
     '871,0,3,"Balkic, Mr. Cerin",male,26,0,0,349248,7.8958,,S\n',
     '872,1,1,"Beckwith, Mrs. Richard Leonard (Sallie Monypeny)",female,47,1,1,11751,52.5542,D35,S\n',
     '873,0,1,"Carlsson, Mr. Frans Olof",male,33,0,0,695,5,B51 B53 B55,S\n',
     '874,0,3,"Vander Cruyssen, Mr. Victor",male,47,0,0,345765,9,,S\n',
     '875,1,2,"Abelson, Mrs. Samuel (Hannah Wizosky)",female,28,1,0,P/PP 3381,24,,C\n',
     '876,1,3,"Najib, Miss. Adele Kiamie ""Jane""",female,15,0,0,2667,7.225,,C\n',
     '877,0,3,"Gustafsson, Mr. Alfred Ossian",male,20,0,0,7534,9.8458,,S\n',
     '878,0,3,"Petroff, Mr. Nedelio",male,19,0,0,349212,7.8958,,S\n',
     '879,0,3,"Laleff, Mr. Kristo",male,,0,0,349217,7.8958,,S\n',
     '880,1,1,"Potter, Mrs. Thomas Jr (Lily Alexenia Wilson)",female,56,0,1,11767,83.1583,C50,C\n',
     '881,1,2,"Shelley, Mrs. William (Imanita Parrish Hall)",female,25,0,1,230433,26,,S\n',
     '882,0,3,"Markun, Mr. Johann",male,33,0,0,349257,7.8958,,S\n',
     '883,0,3,"Dahlberg, Miss. Gerda Ulrika",female,22,0,0,7552,10.5167,,S\n',
     '884,0,2,"Banfield, Mr. Frederick James",male,28,0,0,C.A./SOTON 34068,10.5,,S\n',
     '885,0,3,"Sutehall, Mr. Henry Jr",male,25,0,0,SOTON/OQ 392076,7.05,,S\n',
     '886,0,3,"Rice, Mrs. William (Margaret Norton)",female,39,0,5,382652,29.125,,Q\n',
     '887,0,2,"Montvila, Rev. Juozas",male,27,0,0,211536,13,,S\n',
     '888,1,1,"Graham, Miss. Margaret Edith",female,19,0,0,112053,30,B42,S\n',
     '889,0,3,"Johnston, Miss. Catherine Helen ""Carrie""",female,,1,2,W./C. 6607,23.45,,S\n',
     '890,1,1,"Behr, Mr. Karl Howell",male,26,0,0,111369,30,C148,C\n',
     '891,0,3,"Dooley, Mr. Patrick",male,32,0,0,370376,7.75,,Q\n']




```python
#posicionar o cursor na linha 0
titanic_csv.seek(0)
```




    0




```python
#lendo o arquivo e jogando na variavel
linhas = titanic_csv.readlines()
```


```python
linhas
```




    ['PassengerId,Survived,Pclass,Name,Sex,Age,SibSp,Parch,Ticket,Fare,Cabin,Embarked\n',
     '1,0,3,"Braund, Mr. Owen Harris",male,22,1,0,A/5 21171,7.25,,S\n',
     '2,1,1,"Cumings, Mrs. John Bradley (Florence Briggs Thayer)",female,38,1,0,PC 17599,71.2833,C85,C\n',
     '3,1,3,"Heikkinen, Miss. Laina",female,26,0,0,STON/O2. 3101282,7.925,,S\n',
     '4,1,1,"Futrelle, Mrs. Jacques Heath (Lily May Peel)",female,35,1,0,113803,53.1,C123,S\n',
     '5,0,3,"Allen, Mr. William Henry",male,35,0,0,373450,8.05,,S\n',
     '6,0,3,"Moran, Mr. James",male,,0,0,330877,8.4583,,Q\n',
     '7,0,1,"McCarthy, Mr. Timothy J",male,54,0,0,17463,51.8625,E46,S\n',
     '8,0,3,"Palsson, Master. Gosta Leonard",male,2,3,1,349909,21.075,,S\n',
     '9,1,3,"Johnson, Mrs. Oscar W (Elisabeth Vilhelmina Berg)",female,27,0,2,347742,11.1333,,S\n',
     '10,1,2,"Nasser, Mrs. Nicholas (Adele Achem)",female,14,1,0,237736,30.0708,,C\n',
     '11,1,3,"Sandstrom, Miss. Marguerite Rut",female,4,1,1,PP 9549,16.7,G6,S\n',
     '12,1,1,"Bonnell, Miss. Elizabeth",female,58,0,0,113783,26.55,C103,S\n',
     '13,0,3,"Saundercock, Mr. William Henry",male,20,0,0,A/5. 2151,8.05,,S\n',
     '14,0,3,"Andersson, Mr. Anders Johan",male,39,1,5,347082,31.275,,S\n',
     '15,0,3,"Vestrom, Miss. Hulda Amanda Adolfina",female,14,0,0,350406,7.8542,,S\n',
     '16,1,2,"Hewlett, Mrs. (Mary D Kingcome) ",female,55,0,0,248706,16,,S\n',
     '17,0,3,"Rice, Master. Eugene",male,2,4,1,382652,29.125,,Q\n',
     '18,1,2,"Williams, Mr. Charles Eugene",male,,0,0,244373,13,,S\n',
     '19,0,3,"Vander Planke, Mrs. Julius (Emelia Maria Vandemoortele)",female,31,1,0,345763,18,,S\n',
     '20,1,3,"Masselmani, Mrs. Fatima",female,,0,0,2649,7.225,,C\n',
     '21,0,2,"Fynney, Mr. Joseph J",male,35,0,0,239865,26,,S\n',
     '22,1,2,"Beesley, Mr. Lawrence",male,34,0,0,248698,13,D56,S\n',
     '23,1,3,"McGowan, Miss. Anna ""Annie""",female,15,0,0,330923,8.0292,,Q\n',
     '24,1,1,"Sloper, Mr. William Thompson",male,28,0,0,113788,35.5,A6,S\n',
     '25,0,3,"Palsson, Miss. Torborg Danira",female,8,3,1,349909,21.075,,S\n',
     '26,1,3,"Asplund, Mrs. Carl Oscar (Selma Augusta Emilia Johansson)",female,38,1,5,347077,31.3875,,S\n',
     '27,0,3,"Emir, Mr. Farred Chehab",male,,0,0,2631,7.225,,C\n',
     '28,0,1,"Fortune, Mr. Charles Alexander",male,19,3,2,19950,263,C23 C25 C27,S\n',
     '29,1,3,"O\'Dwyer, Miss. Ellen ""Nellie""",female,,0,0,330959,7.8792,,Q\n',
     '30,0,3,"Todoroff, Mr. Lalio",male,,0,0,349216,7.8958,,S\n',
     '31,0,1,"Uruchurtu, Don. Manuel E",male,40,0,0,PC 17601,27.7208,,C\n',
     '32,1,1,"Spencer, Mrs. William Augustus (Marie Eugenie)",female,,1,0,PC 17569,146.5208,B78,C\n',
     '33,1,3,"Glynn, Miss. Mary Agatha",female,,0,0,335677,7.75,,Q\n',
     '34,0,2,"Wheadon, Mr. Edward H",male,66,0,0,C.A. 24579,10.5,,S\n',
     '35,0,1,"Meyer, Mr. Edgar Joseph",male,28,1,0,PC 17604,82.1708,,C\n',
     '36,0,1,"Holverson, Mr. Alexander Oskar",male,42,1,0,113789,52,,S\n',
     '37,1,3,"Mamee, Mr. Hanna",male,,0,0,2677,7.2292,,C\n',
     '38,0,3,"Cann, Mr. Ernest Charles",male,21,0,0,A./5. 2152,8.05,,S\n',
     '39,0,3,"Vander Planke, Miss. Augusta Maria",female,18,2,0,345764,18,,S\n',
     '40,1,3,"Nicola-Yarred, Miss. Jamila",female,14,1,0,2651,11.2417,,C\n',
     '41,0,3,"Ahlin, Mrs. Johan (Johanna Persdotter Larsson)",female,40,1,0,7546,9.475,,S\n',
     '42,0,2,"Turpin, Mrs. William John Robert (Dorothy Ann Wonnacott)",female,27,1,0,11668,21,,S\n',
     '43,0,3,"Kraeff, Mr. Theodor",male,,0,0,349253,7.8958,,C\n',
     '44,1,2,"Laroche, Miss. Simonne Marie Anne Andree",female,3,1,2,SC/Paris 2123,41.5792,,C\n',
     '45,1,3,"Devaney, Miss. Margaret Delia",female,19,0,0,330958,7.8792,,Q\n',
     '46,0,3,"Rogers, Mr. William John",male,,0,0,S.C./A.4. 23567,8.05,,S\n',
     '47,0,3,"Lennon, Mr. Denis",male,,1,0,370371,15.5,,Q\n',
     '48,1,3,"O\'Driscoll, Miss. Bridget",female,,0,0,14311,7.75,,Q\n',
     '49,0,3,"Samaan, Mr. Youssef",male,,2,0,2662,21.6792,,C\n',
     '50,0,3,"Arnold-Franchi, Mrs. Josef (Josefine Franchi)",female,18,1,0,349237,17.8,,S\n',
     '51,0,3,"Panula, Master. Juha Niilo",male,7,4,1,3101295,39.6875,,S\n',
     '52,0,3,"Nosworthy, Mr. Richard Cater",male,21,0,0,A/4. 39886,7.8,,S\n',
     '53,1,1,"Harper, Mrs. Henry Sleeper (Myna Haxtun)",female,49,1,0,PC 17572,76.7292,D33,C\n',
     '54,1,2,"Faunthorpe, Mrs. Lizzie (Elizabeth Anne Wilkinson)",female,29,1,0,2926,26,,S\n',
     '55,0,1,"Ostby, Mr. Engelhart Cornelius",male,65,0,1,113509,61.9792,B30,C\n',
     '56,1,1,"Woolner, Mr. Hugh",male,,0,0,19947,35.5,C52,S\n',
     '57,1,2,"Rugg, Miss. Emily",female,21,0,0,C.A. 31026,10.5,,S\n',
     '58,0,3,"Novel, Mr. Mansouer",male,28.5,0,0,2697,7.2292,,C\n',
     '59,1,2,"West, Miss. Constance Mirium",female,5,1,2,C.A. 34651,27.75,,S\n',
     '60,0,3,"Goodwin, Master. William Frederick",male,11,5,2,CA 2144,46.9,,S\n',
     '61,0,3,"Sirayanian, Mr. Orsen",male,22,0,0,2669,7.2292,,C\n',
     '62,1,1,"Icard, Miss. Amelie",female,38,0,0,113572,80,B28,\n',
     '63,0,1,"Harris, Mr. Henry Birkhardt",male,45,1,0,36973,83.475,C83,S\n',
     '64,0,3,"Skoog, Master. Harald",male,4,3,2,347088,27.9,,S\n',
     '65,0,1,"Stewart, Mr. Albert A",male,,0,0,PC 17605,27.7208,,C\n',
     '66,1,3,"Moubarek, Master. Gerios",male,,1,1,2661,15.2458,,C\n',
     '67,1,2,"Nye, Mrs. (Elizabeth Ramell)",female,29,0,0,C.A. 29395,10.5,F33,S\n',
     '68,0,3,"Crease, Mr. Ernest James",male,19,0,0,S.P. 3464,8.1583,,S\n',
     '69,1,3,"Andersson, Miss. Erna Alexandra",female,17,4,2,3101281,7.925,,S\n',
     '70,0,3,"Kink, Mr. Vincenz",male,26,2,0,315151,8.6625,,S\n',
     '71,0,2,"Jenkin, Mr. Stephen Curnow",male,32,0,0,C.A. 33111,10.5,,S\n',
     '72,0,3,"Goodwin, Miss. Lillian Amy",female,16,5,2,CA 2144,46.9,,S\n',
     '73,0,2,"Hood, Mr. Ambrose Jr",male,21,0,0,S.O.C. 14879,73.5,,S\n',
     '74,0,3,"Chronopoulos, Mr. Apostolos",male,26,1,0,2680,14.4542,,C\n',
     '75,1,3,"Bing, Mr. Lee",male,32,0,0,1601,56.4958,,S\n',
     '76,0,3,"Moen, Mr. Sigurd Hansen",male,25,0,0,348123,7.65,F G73,S\n',
     '77,0,3,"Staneff, Mr. Ivan",male,,0,0,349208,7.8958,,S\n',
     '78,0,3,"Moutal, Mr. Rahamin Haim",male,,0,0,374746,8.05,,S\n',
     '79,1,2,"Caldwell, Master. Alden Gates",male,0.83,0,2,248738,29,,S\n',
     '80,1,3,"Dowdell, Miss. Elizabeth",female,30,0,0,364516,12.475,,S\n',
     '81,0,3,"Waelens, Mr. Achille",male,22,0,0,345767,9,,S\n',
     '82,1,3,"Sheerlinck, Mr. Jan Baptist",male,29,0,0,345779,9.5,,S\n',
     '83,1,3,"McDermott, Miss. Brigdet Delia",female,,0,0,330932,7.7875,,Q\n',
     '84,0,1,"Carrau, Mr. Francisco M",male,28,0,0,113059,47.1,,S\n',
     '85,1,2,"Ilett, Miss. Bertha",female,17,0,0,SO/C 14885,10.5,,S\n',
     '86,1,3,"Backstrom, Mrs. Karl Alfred (Maria Mathilda Gustafsson)",female,33,3,0,3101278,15.85,,S\n',
     '87,0,3,"Ford, Mr. William Neal",male,16,1,3,W./C. 6608,34.375,,S\n',
     '88,0,3,"Slocovski, Mr. Selman Francis",male,,0,0,SOTON/OQ 392086,8.05,,S\n',
     '89,1,1,"Fortune, Miss. Mabel Helen",female,23,3,2,19950,263,C23 C25 C27,S\n',
     '90,0,3,"Celotti, Mr. Francesco",male,24,0,0,343275,8.05,,S\n',
     '91,0,3,"Christmann, Mr. Emil",male,29,0,0,343276,8.05,,S\n',
     '92,0,3,"Andreasson, Mr. Paul Edvin",male,20,0,0,347466,7.8542,,S\n',
     '93,0,1,"Chaffee, Mr. Herbert Fuller",male,46,1,0,W.E.P. 5734,61.175,E31,S\n',
     '94,0,3,"Dean, Mr. Bertram Frank",male,26,1,2,C.A. 2315,20.575,,S\n',
     '95,0,3,"Coxon, Mr. Daniel",male,59,0,0,364500,7.25,,S\n',
     '96,0,3,"Shorney, Mr. Charles Joseph",male,,0,0,374910,8.05,,S\n',
     '97,0,1,"Goldschmidt, Mr. George B",male,71,0,0,PC 17754,34.6542,A5,C\n',
     '98,1,1,"Greenfield, Mr. William Bertram",male,23,0,1,PC 17759,63.3583,D10 D12,C\n',
     '99,1,2,"Doling, Mrs. John T (Ada Julia Bone)",female,34,0,1,231919,23,,S\n',
     '100,0,2,"Kantor, Mr. Sinai",male,34,1,0,244367,26,,S\n',
     '101,0,3,"Petranec, Miss. Matilda",female,28,0,0,349245,7.8958,,S\n',
     '102,0,3,"Petroff, Mr. Pastcho (""Pentcho"")",male,,0,0,349215,7.8958,,S\n',
     '103,0,1,"White, Mr. Richard Frasar",male,21,0,1,35281,77.2875,D26,S\n',
     '104,0,3,"Johansson, Mr. Gustaf Joel",male,33,0,0,7540,8.6542,,S\n',
     '105,0,3,"Gustafsson, Mr. Anders Vilhelm",male,37,2,0,3101276,7.925,,S\n',
     '106,0,3,"Mionoff, Mr. Stoytcho",male,28,0,0,349207,7.8958,,S\n',
     '107,1,3,"Salkjelsvik, Miss. Anna Kristine",female,21,0,0,343120,7.65,,S\n',
     '108,1,3,"Moss, Mr. Albert Johan",male,,0,0,312991,7.775,,S\n',
     '109,0,3,"Rekic, Mr. Tido",male,38,0,0,349249,7.8958,,S\n',
     '110,1,3,"Moran, Miss. Bertha",female,,1,0,371110,24.15,,Q\n',
     '111,0,1,"Porter, Mr. Walter Chamberlain",male,47,0,0,110465,52,C110,S\n',
     '112,0,3,"Zabour, Miss. Hileni",female,14.5,1,0,2665,14.4542,,C\n',
     '113,0,3,"Barton, Mr. David John",male,22,0,0,324669,8.05,,S\n',
     '114,0,3,"Jussila, Miss. Katriina",female,20,1,0,4136,9.825,,S\n',
     '115,0,3,"Attalah, Miss. Malake",female,17,0,0,2627,14.4583,,C\n',
     '116,0,3,"Pekoniemi, Mr. Edvard",male,21,0,0,STON/O 2. 3101294,7.925,,S\n',
     '117,0,3,"Connors, Mr. Patrick",male,70.5,0,0,370369,7.75,,Q\n',
     '118,0,2,"Turpin, Mr. William John Robert",male,29,1,0,11668,21,,S\n',
     '119,0,1,"Baxter, Mr. Quigg Edmond",male,24,0,1,PC 17558,247.5208,B58 B60,C\n',
     '120,0,3,"Andersson, Miss. Ellis Anna Maria",female,2,4,2,347082,31.275,,S\n',
     '121,0,2,"Hickman, Mr. Stanley George",male,21,2,0,S.O.C. 14879,73.5,,S\n',
     '122,0,3,"Moore, Mr. Leonard Charles",male,,0,0,A4. 54510,8.05,,S\n',
     '123,0,2,"Nasser, Mr. Nicholas",male,32.5,1,0,237736,30.0708,,C\n',
     '124,1,2,"Webber, Miss. Susan",female,32.5,0,0,27267,13,E101,S\n',
     '125,0,1,"White, Mr. Percival Wayland",male,54,0,1,35281,77.2875,D26,S\n',
     '126,1,3,"Nicola-Yarred, Master. Elias",male,12,1,0,2651,11.2417,,C\n',
     '127,0,3,"McMahon, Mr. Martin",male,,0,0,370372,7.75,,Q\n',
     '128,1,3,"Madsen, Mr. Fridtjof Arne",male,24,0,0,C 17369,7.1417,,S\n',
     '129,1,3,"Peter, Miss. Anna",female,,1,1,2668,22.3583,F E69,C\n',
     '130,0,3,"Ekstrom, Mr. Johan",male,45,0,0,347061,6.975,,S\n',
     '131,0,3,"Drazenoic, Mr. Jozef",male,33,0,0,349241,7.8958,,C\n',
     '132,0,3,"Coelho, Mr. Domingos Fernandeo",male,20,0,0,SOTON/O.Q. 3101307,7.05,,S\n',
     '133,0,3,"Robins, Mrs. Alexander A (Grace Charity Laury)",female,47,1,0,A/5. 3337,14.5,,S\n',
     '134,1,2,"Weisz, Mrs. Leopold (Mathilde Francoise Pede)",female,29,1,0,228414,26,,S\n',
     '135,0,2,"Sobey, Mr. Samuel James Hayden",male,25,0,0,C.A. 29178,13,,S\n',
     '136,0,2,"Richard, Mr. Emile",male,23,0,0,SC/PARIS 2133,15.0458,,C\n',
     '137,1,1,"Newsom, Miss. Helen Monypeny",female,19,0,2,11752,26.2833,D47,S\n',
     '138,0,1,"Futrelle, Mr. Jacques Heath",male,37,1,0,113803,53.1,C123,S\n',
     '139,0,3,"Osen, Mr. Olaf Elon",male,16,0,0,7534,9.2167,,S\n',
     '140,0,1,"Giglio, Mr. Victor",male,24,0,0,PC 17593,79.2,B86,C\n',
     '141,0,3,"Boulos, Mrs. Joseph (Sultana)",female,,0,2,2678,15.2458,,C\n',
     '142,1,3,"Nysten, Miss. Anna Sofia",female,22,0,0,347081,7.75,,S\n',
     '143,1,3,"Hakkarainen, Mrs. Pekka Pietari (Elin Matilda Dolck)",female,24,1,0,STON/O2. 3101279,15.85,,S\n',
     '144,0,3,"Burke, Mr. Jeremiah",male,19,0,0,365222,6.75,,Q\n',
     '145,0,2,"Andrew, Mr. Edgardo Samuel",male,18,0,0,231945,11.5,,S\n',
     '146,0,2,"Nicholls, Mr. Joseph Charles",male,19,1,1,C.A. 33112,36.75,,S\n',
     '147,1,3,"Andersson, Mr. August Edvard (""Wennerstrom"")",male,27,0,0,350043,7.7958,,S\n',
     '148,0,3,"Ford, Miss. Robina Maggie ""Ruby""",female,9,2,2,W./C. 6608,34.375,,S\n',
     '149,0,2,"Navratil, Mr. Michel (""Louis M Hoffman"")",male,36.5,0,2,230080,26,F2,S\n',
     '150,0,2,"Byles, Rev. Thomas Roussel Davids",male,42,0,0,244310,13,,S\n',
     '151,0,2,"Bateman, Rev. Robert James",male,51,0,0,S.O.P. 1166,12.525,,S\n',
     '152,1,1,"Pears, Mrs. Thomas (Edith Wearne)",female,22,1,0,113776,66.6,C2,S\n',
     '153,0,3,"Meo, Mr. Alfonzo",male,55.5,0,0,A.5. 11206,8.05,,S\n',
     '154,0,3,"van Billiard, Mr. Austin Blyler",male,40.5,0,2,A/5. 851,14.5,,S\n',
     '155,0,3,"Olsen, Mr. Ole Martin",male,,0,0,Fa 265302,7.3125,,S\n',
     '156,0,1,"Williams, Mr. Charles Duane",male,51,0,1,PC 17597,61.3792,,C\n',
     '157,1,3,"Gilnagh, Miss. Katherine ""Katie""",female,16,0,0,35851,7.7333,,Q\n',
     '158,0,3,"Corn, Mr. Harry",male,30,0,0,SOTON/OQ 392090,8.05,,S\n',
     '159,0,3,"Smiljanic, Mr. Mile",male,,0,0,315037,8.6625,,S\n',
     '160,0,3,"Sage, Master. Thomas Henry",male,,8,2,CA. 2343,69.55,,S\n',
     '161,0,3,"Cribb, Mr. John Hatfield",male,44,0,1,371362,16.1,,S\n',
     '162,1,2,"Watt, Mrs. James (Elizabeth ""Bessie"" Inglis Milne)",female,40,0,0,C.A. 33595,15.75,,S\n',
     '163,0,3,"Bengtsson, Mr. John Viktor",male,26,0,0,347068,7.775,,S\n',
     '164,0,3,"Calic, Mr. Jovo",male,17,0,0,315093,8.6625,,S\n',
     '165,0,3,"Panula, Master. Eino Viljami",male,1,4,1,3101295,39.6875,,S\n',
     '166,1,3,"Goldsmith, Master. Frank John William ""Frankie""",male,9,0,2,363291,20.525,,S\n',
     '167,1,1,"Chibnall, Mrs. (Edith Martha Bowerman)",female,,0,1,113505,55,E33,S\n',
     '168,0,3,"Skoog, Mrs. William (Anna Bernhardina Karlsson)",female,45,1,4,347088,27.9,,S\n',
     '169,0,1,"Baumann, Mr. John D",male,,0,0,PC 17318,25.925,,S\n',
     '170,0,3,"Ling, Mr. Lee",male,28,0,0,1601,56.4958,,S\n',
     '171,0,1,"Van der hoef, Mr. Wyckoff",male,61,0,0,111240,33.5,B19,S\n',
     '172,0,3,"Rice, Master. Arthur",male,4,4,1,382652,29.125,,Q\n',
     '173,1,3,"Johnson, Miss. Eleanor Ileen",female,1,1,1,347742,11.1333,,S\n',
     '174,0,3,"Sivola, Mr. Antti Wilhelm",male,21,0,0,STON/O 2. 3101280,7.925,,S\n',
     '175,0,1,"Smith, Mr. James Clinch",male,56,0,0,17764,30.6958,A7,C\n',
     '176,0,3,"Klasen, Mr. Klas Albin",male,18,1,1,350404,7.8542,,S\n',
     '177,0,3,"Lefebre, Master. Henry Forbes",male,,3,1,4133,25.4667,,S\n',
     '178,0,1,"Isham, Miss. Ann Elizabeth",female,50,0,0,PC 17595,28.7125,C49,C\n',
     '179,0,2,"Hale, Mr. Reginald",male,30,0,0,250653,13,,S\n',
     '180,0,3,"Leonard, Mr. Lionel",male,36,0,0,LINE,0,,S\n',
     '181,0,3,"Sage, Miss. Constance Gladys",female,,8,2,CA. 2343,69.55,,S\n',
     '182,0,2,"Pernot, Mr. Rene",male,,0,0,SC/PARIS 2131,15.05,,C\n',
     '183,0,3,"Asplund, Master. Clarence Gustaf Hugo",male,9,4,2,347077,31.3875,,S\n',
     '184,1,2,"Becker, Master. Richard F",male,1,2,1,230136,39,F4,S\n',
     '185,1,3,"Kink-Heilmann, Miss. Luise Gretchen",female,4,0,2,315153,22.025,,S\n',
     '186,0,1,"Rood, Mr. Hugh Roscoe",male,,0,0,113767,50,A32,S\n',
     '187,1,3,"O\'Brien, Mrs. Thomas (Johanna ""Hannah"" Godfrey)",female,,1,0,370365,15.5,,Q\n',
     '188,1,1,"Romaine, Mr. Charles Hallace (""Mr C Rolmane"")",male,45,0,0,111428,26.55,,S\n',
     '189,0,3,"Bourke, Mr. John",male,40,1,1,364849,15.5,,Q\n',
     '190,0,3,"Turcin, Mr. Stjepan",male,36,0,0,349247,7.8958,,S\n',
     '191,1,2,"Pinsky, Mrs. (Rosa)",female,32,0,0,234604,13,,S\n',
     '192,0,2,"Carbines, Mr. William",male,19,0,0,28424,13,,S\n',
     '193,1,3,"Andersen-Jensen, Miss. Carla Christine Nielsine",female,19,1,0,350046,7.8542,,S\n',
     '194,1,2,"Navratil, Master. Michel M",male,3,1,1,230080,26,F2,S\n',
     '195,1,1,"Brown, Mrs. James Joseph (Margaret Tobin)",female,44,0,0,PC 17610,27.7208,B4,C\n',
     '196,1,1,"Lurette, Miss. Elise",female,58,0,0,PC 17569,146.5208,B80,C\n',
     '197,0,3,"Mernagh, Mr. Robert",male,,0,0,368703,7.75,,Q\n',
     '198,0,3,"Olsen, Mr. Karl Siegwart Andreas",male,42,0,1,4579,8.4042,,S\n',
     '199,1,3,"Madigan, Miss. Margaret ""Maggie""",female,,0,0,370370,7.75,,Q\n',
     '200,0,2,"Yrois, Miss. Henriette (""Mrs Harbeck"")",female,24,0,0,248747,13,,S\n',
     '201,0,3,"Vande Walle, Mr. Nestor Cyriel",male,28,0,0,345770,9.5,,S\n',
     '202,0,3,"Sage, Mr. Frederick",male,,8,2,CA. 2343,69.55,,S\n',
     '203,0,3,"Johanson, Mr. Jakob Alfred",male,34,0,0,3101264,6.4958,,S\n',
     '204,0,3,"Youseff, Mr. Gerious",male,45.5,0,0,2628,7.225,,C\n',
     '205,1,3,"Cohen, Mr. Gurshon ""Gus""",male,18,0,0,A/5 3540,8.05,,S\n',
     '206,0,3,"Strom, Miss. Telma Matilda",female,2,0,1,347054,10.4625,G6,S\n',
     '207,0,3,"Backstrom, Mr. Karl Alfred",male,32,1,0,3101278,15.85,,S\n',
     '208,1,3,"Albimona, Mr. Nassef Cassem",male,26,0,0,2699,18.7875,,C\n',
     '209,1,3,"Carr, Miss. Helen ""Ellen""",female,16,0,0,367231,7.75,,Q\n',
     '210,1,1,"Blank, Mr. Henry",male,40,0,0,112277,31,A31,C\n',
     '211,0,3,"Ali, Mr. Ahmed",male,24,0,0,SOTON/O.Q. 3101311,7.05,,S\n',
     '212,1,2,"Cameron, Miss. Clear Annie",female,35,0,0,F.C.C. 13528,21,,S\n',
     '213,0,3,"Perkin, Mr. John Henry",male,22,0,0,A/5 21174,7.25,,S\n',
     '214,0,2,"Givard, Mr. Hans Kristensen",male,30,0,0,250646,13,,S\n',
     '215,0,3,"Kiernan, Mr. Philip",male,,1,0,367229,7.75,,Q\n',
     '216,1,1,"Newell, Miss. Madeleine",female,31,1,0,35273,113.275,D36,C\n',
     '217,1,3,"Honkanen, Miss. Eliina",female,27,0,0,STON/O2. 3101283,7.925,,S\n',
     '218,0,2,"Jacobsohn, Mr. Sidney Samuel",male,42,1,0,243847,27,,S\n',
     '219,1,1,"Bazzani, Miss. Albina",female,32,0,0,11813,76.2917,D15,C\n',
     '220,0,2,"Harris, Mr. Walter",male,30,0,0,W/C 14208,10.5,,S\n',
     '221,1,3,"Sunderland, Mr. Victor Francis",male,16,0,0,SOTON/OQ 392089,8.05,,S\n',
     '222,0,2,"Bracken, Mr. James H",male,27,0,0,220367,13,,S\n',
     '223,0,3,"Green, Mr. George Henry",male,51,0,0,21440,8.05,,S\n',
     '224,0,3,"Nenkoff, Mr. Christo",male,,0,0,349234,7.8958,,S\n',
     '225,1,1,"Hoyt, Mr. Frederick Maxfield",male,38,1,0,19943,90,C93,S\n',
     '226,0,3,"Berglund, Mr. Karl Ivar Sven",male,22,0,0,PP 4348,9.35,,S\n',
     '227,1,2,"Mellors, Mr. William John",male,19,0,0,SW/PP 751,10.5,,S\n',
     '228,0,3,"Lovell, Mr. John Hall (""Henry"")",male,20.5,0,0,A/5 21173,7.25,,S\n',
     '229,0,2,"Fahlstrom, Mr. Arne Jonas",male,18,0,0,236171,13,,S\n',
     '230,0,3,"Lefebre, Miss. Mathilde",female,,3,1,4133,25.4667,,S\n',
     '231,1,1,"Harris, Mrs. Henry Birkhardt (Irene Wallach)",female,35,1,0,36973,83.475,C83,S\n',
     '232,0,3,"Larsson, Mr. Bengt Edvin",male,29,0,0,347067,7.775,,S\n',
     '233,0,2,"Sjostedt, Mr. Ernst Adolf",male,59,0,0,237442,13.5,,S\n',
     '234,1,3,"Asplund, Miss. Lillian Gertrud",female,5,4,2,347077,31.3875,,S\n',
     '235,0,2,"Leyson, Mr. Robert William Norman",male,24,0,0,C.A. 29566,10.5,,S\n',
     '236,0,3,"Harknett, Miss. Alice Phoebe",female,,0,0,W./C. 6609,7.55,,S\n',
     '237,0,2,"Hold, Mr. Stephen",male,44,1,0,26707,26,,S\n',
     '238,1,2,"Collyer, Miss. Marjorie ""Lottie""",female,8,0,2,C.A. 31921,26.25,,S\n',
     '239,0,2,"Pengelly, Mr. Frederick William",male,19,0,0,28665,10.5,,S\n',
     '240,0,2,"Hunt, Mr. George Henry",male,33,0,0,SCO/W 1585,12.275,,S\n',
     '241,0,3,"Zabour, Miss. Thamine",female,,1,0,2665,14.4542,,C\n',
     '242,1,3,"Murphy, Miss. Katherine ""Kate""",female,,1,0,367230,15.5,,Q\n',
     '243,0,2,"Coleridge, Mr. Reginald Charles",male,29,0,0,W./C. 14263,10.5,,S\n',
     '244,0,3,"Maenpaa, Mr. Matti Alexanteri",male,22,0,0,STON/O 2. 3101275,7.125,,S\n',
     '245,0,3,"Attalah, Mr. Sleiman",male,30,0,0,2694,7.225,,C\n',
     '246,0,1,"Minahan, Dr. William Edward",male,44,2,0,19928,90,C78,Q\n',
     '247,0,3,"Lindahl, Miss. Agda Thorilda Viktoria",female,25,0,0,347071,7.775,,S\n',
     '248,1,2,"Hamalainen, Mrs. William (Anna)",female,24,0,2,250649,14.5,,S\n',
     '249,1,1,"Beckwith, Mr. Richard Leonard",male,37,1,1,11751,52.5542,D35,S\n',
     '250,0,2,"Carter, Rev. Ernest Courtenay",male,54,1,0,244252,26,,S\n',
     '251,0,3,"Reed, Mr. James George",male,,0,0,362316,7.25,,S\n',
     '252,0,3,"Strom, Mrs. Wilhelm (Elna Matilda Persson)",female,29,1,1,347054,10.4625,G6,S\n',
     '253,0,1,"Stead, Mr. William Thomas",male,62,0,0,113514,26.55,C87,S\n',
     '254,0,3,"Lobb, Mr. William Arthur",male,30,1,0,A/5. 3336,16.1,,S\n',
     '255,0,3,"Rosblom, Mrs. Viktor (Helena Wilhelmina)",female,41,0,2,370129,20.2125,,S\n',
     '256,1,3,"Touma, Mrs. Darwis (Hanne Youssef Razi)",female,29,0,2,2650,15.2458,,C\n',
     '257,1,1,"Thorne, Mrs. Gertrude Maybelle",female,,0,0,PC 17585,79.2,,C\n',
     '258,1,1,"Cherry, Miss. Gladys",female,30,0,0,110152,86.5,B77,S\n',
     '259,1,1,"Ward, Miss. Anna",female,35,0,0,PC 17755,512.3292,,C\n',
     '260,1,2,"Parrish, Mrs. (Lutie Davis)",female,50,0,1,230433,26,,S\n',
     '261,0,3,"Smith, Mr. Thomas",male,,0,0,384461,7.75,,Q\n',
     '262,1,3,"Asplund, Master. Edvin Rojj Felix",male,3,4,2,347077,31.3875,,S\n',
     '263,0,1,"Taussig, Mr. Emil",male,52,1,1,110413,79.65,E67,S\n',
     '264,0,1,"Harrison, Mr. William",male,40,0,0,112059,0,B94,S\n',
     '265,0,3,"Henry, Miss. Delia",female,,0,0,382649,7.75,,Q\n',
     '266,0,2,"Reeves, Mr. David",male,36,0,0,C.A. 17248,10.5,,S\n',
     '267,0,3,"Panula, Mr. Ernesti Arvid",male,16,4,1,3101295,39.6875,,S\n',
     '268,1,3,"Persson, Mr. Ernst Ulrik",male,25,1,0,347083,7.775,,S\n',
     '269,1,1,"Graham, Mrs. William Thompson (Edith Junkins)",female,58,0,1,PC 17582,153.4625,C125,S\n',
     '270,1,1,"Bissette, Miss. Amelia",female,35,0,0,PC 17760,135.6333,C99,S\n',
     '271,0,1,"Cairns, Mr. Alexander",male,,0,0,113798,31,,S\n',
     '272,1,3,"Tornquist, Mr. William Henry",male,25,0,0,LINE,0,,S\n',
     '273,1,2,"Mellinger, Mrs. (Elizabeth Anne Maidment)",female,41,0,1,250644,19.5,,S\n',
     '274,0,1,"Natsch, Mr. Charles H",male,37,0,1,PC 17596,29.7,C118,C\n',
     '275,1,3,"Healy, Miss. Hanora ""Nora""",female,,0,0,370375,7.75,,Q\n',
     '276,1,1,"Andrews, Miss. Kornelia Theodosia",female,63,1,0,13502,77.9583,D7,S\n',
     '277,0,3,"Lindblom, Miss. Augusta Charlotta",female,45,0,0,347073,7.75,,S\n',
     '278,0,2,"Parkes, Mr. Francis ""Frank""",male,,0,0,239853,0,,S\n',
     '279,0,3,"Rice, Master. Eric",male,7,4,1,382652,29.125,,Q\n',
     '280,1,3,"Abbott, Mrs. Stanton (Rosa Hunt)",female,35,1,1,C.A. 2673,20.25,,S\n',
     '281,0,3,"Duane, Mr. Frank",male,65,0,0,336439,7.75,,Q\n',
     '282,0,3,"Olsson, Mr. Nils Johan Goransson",male,28,0,0,347464,7.8542,,S\n',
     '283,0,3,"de Pelsmaeker, Mr. Alfons",male,16,0,0,345778,9.5,,S\n',
     '284,1,3,"Dorking, Mr. Edward Arthur",male,19,0,0,A/5. 10482,8.05,,S\n',
     '285,0,1,"Smith, Mr. Richard William",male,,0,0,113056,26,A19,S\n',
     '286,0,3,"Stankovic, Mr. Ivan",male,33,0,0,349239,8.6625,,C\n',
     '287,1,3,"de Mulder, Mr. Theodore",male,30,0,0,345774,9.5,,S\n',
     '288,0,3,"Naidenoff, Mr. Penko",male,22,0,0,349206,7.8958,,S\n',
     '289,1,2,"Hosono, Mr. Masabumi",male,42,0,0,237798,13,,S\n',
     '290,1,3,"Connolly, Miss. Kate",female,22,0,0,370373,7.75,,Q\n',
     '291,1,1,"Barber, Miss. Ellen ""Nellie""",female,26,0,0,19877,78.85,,S\n',
     '292,1,1,"Bishop, Mrs. Dickinson H (Helen Walton)",female,19,1,0,11967,91.0792,B49,C\n',
     '293,0,2,"Levy, Mr. Rene Jacques",male,36,0,0,SC/Paris 2163,12.875,D,C\n',
     '294,0,3,"Haas, Miss. Aloisia",female,24,0,0,349236,8.85,,S\n',
     '295,0,3,"Mineff, Mr. Ivan",male,24,0,0,349233,7.8958,,S\n',
     '296,0,1,"Lewy, Mr. Ervin G",male,,0,0,PC 17612,27.7208,,C\n',
     '297,0,3,"Hanna, Mr. Mansour",male,23.5,0,0,2693,7.2292,,C\n',
     '298,0,1,"Allison, Miss. Helen Loraine",female,2,1,2,113781,151.55,C22 C26,S\n',
     '299,1,1,"Saalfeld, Mr. Adolphe",male,,0,0,19988,30.5,C106,S\n',
     '300,1,1,"Baxter, Mrs. James (Helene DeLaudeniere Chaput)",female,50,0,1,PC 17558,247.5208,B58 B60,C\n',
     '301,1,3,"Kelly, Miss. Anna Katherine ""Annie Kate""",female,,0,0,9234,7.75,,Q\n',
     '302,1,3,"McCoy, Mr. Bernard",male,,2,0,367226,23.25,,Q\n',
     '303,0,3,"Johnson, Mr. William Cahoone Jr",male,19,0,0,LINE,0,,S\n',
     '304,1,2,"Keane, Miss. Nora A",female,,0,0,226593,12.35,E101,Q\n',
     '305,0,3,"Williams, Mr. Howard Hugh ""Harry""",male,,0,0,A/5 2466,8.05,,S\n',
     '306,1,1,"Allison, Master. Hudson Trevor",male,0.92,1,2,113781,151.55,C22 C26,S\n',
     '307,1,1,"Fleming, Miss. Margaret",female,,0,0,17421,110.8833,,C\n',
     '308,1,1,"Penasco y Castellana, Mrs. Victor de Satode (Maria Josefa Perez de Soto y Vallejo)",female,17,1,0,PC 17758,108.9,C65,C\n',
     '309,0,2,"Abelson, Mr. Samuel",male,30,1,0,P/PP 3381,24,,C\n',
     '310,1,1,"Francatelli, Miss. Laura Mabel",female,30,0,0,PC 17485,56.9292,E36,C\n',
     '311,1,1,"Hays, Miss. Margaret Bechstein",female,24,0,0,11767,83.1583,C54,C\n',
     '312,1,1,"Ryerson, Miss. Emily Borie",female,18,2,2,PC 17608,262.375,B57 B59 B63 B66,C\n',
     '313,0,2,"Lahtinen, Mrs. William (Anna Sylfven)",female,26,1,1,250651,26,,S\n',
     '314,0,3,"Hendekovic, Mr. Ignjac",male,28,0,0,349243,7.8958,,S\n',
     '315,0,2,"Hart, Mr. Benjamin",male,43,1,1,F.C.C. 13529,26.25,,S\n',
     '316,1,3,"Nilsson, Miss. Helmina Josefina",female,26,0,0,347470,7.8542,,S\n',
     '317,1,2,"Kantor, Mrs. Sinai (Miriam Sternin)",female,24,1,0,244367,26,,S\n',
     '318,0,2,"Moraweck, Dr. Ernest",male,54,0,0,29011,14,,S\n',
     '319,1,1,"Wick, Miss. Mary Natalie",female,31,0,2,36928,164.8667,C7,S\n',
     '320,1,1,"Spedden, Mrs. Frederic Oakley (Margaretta Corning Stone)",female,40,1,1,16966,134.5,E34,C\n',
     '321,0,3,"Dennis, Mr. Samuel",male,22,0,0,A/5 21172,7.25,,S\n',
     '322,0,3,"Danoff, Mr. Yoto",male,27,0,0,349219,7.8958,,S\n',
     '323,1,2,"Slayter, Miss. Hilda Mary",female,30,0,0,234818,12.35,,Q\n',
     '324,1,2,"Caldwell, Mrs. Albert Francis (Sylvia Mae Harbaugh)",female,22,1,1,248738,29,,S\n',
     '325,0,3,"Sage, Mr. George John Jr",male,,8,2,CA. 2343,69.55,,S\n',
     '326,1,1,"Young, Miss. Marie Grice",female,36,0,0,PC 17760,135.6333,C32,C\n',
     '327,0,3,"Nysveen, Mr. Johan Hansen",male,61,0,0,345364,6.2375,,S\n',
     '328,1,2,"Ball, Mrs. (Ada E Hall)",female,36,0,0,28551,13,D,S\n',
     '329,1,3,"Goldsmith, Mrs. Frank John (Emily Alice Brown)",female,31,1,1,363291,20.525,,S\n',
     '330,1,1,"Hippach, Miss. Jean Gertrude",female,16,0,1,111361,57.9792,B18,C\n',
     '331,1,3,"McCoy, Miss. Agnes",female,,2,0,367226,23.25,,Q\n',
     '332,0,1,"Partner, Mr. Austen",male,45.5,0,0,113043,28.5,C124,S\n',
     '333,0,1,"Graham, Mr. George Edward",male,38,0,1,PC 17582,153.4625,C91,S\n',
     '334,0,3,"Vander Planke, Mr. Leo Edmondus",male,16,2,0,345764,18,,S\n',
     '335,1,1,"Frauenthal, Mrs. Henry William (Clara Heinsheimer)",female,,1,0,PC 17611,133.65,,S\n',
     '336,0,3,"Denkoff, Mr. Mitto",male,,0,0,349225,7.8958,,S\n',
     '337,0,1,"Pears, Mr. Thomas Clinton",male,29,1,0,113776,66.6,C2,S\n',
     '338,1,1,"Burns, Miss. Elizabeth Margaret",female,41,0,0,16966,134.5,E40,C\n',
     '339,1,3,"Dahl, Mr. Karl Edwart",male,45,0,0,7598,8.05,,S\n',
     '340,0,1,"Blackwell, Mr. Stephen Weart",male,45,0,0,113784,35.5,T,S\n',
     '341,1,2,"Navratil, Master. Edmond Roger",male,2,1,1,230080,26,F2,S\n',
     '342,1,1,"Fortune, Miss. Alice Elizabeth",female,24,3,2,19950,263,C23 C25 C27,S\n',
     '343,0,2,"Collander, Mr. Erik Gustaf",male,28,0,0,248740,13,,S\n',
     '344,0,2,"Sedgwick, Mr. Charles Frederick Waddington",male,25,0,0,244361,13,,S\n',
     '345,0,2,"Fox, Mr. Stanley Hubert",male,36,0,0,229236,13,,S\n',
     '346,1,2,"Brown, Miss. Amelia ""Mildred""",female,24,0,0,248733,13,F33,S\n',
     '347,1,2,"Smith, Miss. Marion Elsie",female,40,0,0,31418,13,,S\n',
     '348,1,3,"Davison, Mrs. Thomas Henry (Mary E Finck)",female,,1,0,386525,16.1,,S\n',
     '349,1,3,"Coutts, Master. William Loch ""William""",male,3,1,1,C.A. 37671,15.9,,S\n',
     '350,0,3,"Dimic, Mr. Jovan",male,42,0,0,315088,8.6625,,S\n',
     '351,0,3,"Odahl, Mr. Nils Martin",male,23,0,0,7267,9.225,,S\n',
     '352,0,1,"Williams-Lambert, Mr. Fletcher Fellows",male,,0,0,113510,35,C128,S\n',
     '353,0,3,"Elias, Mr. Tannous",male,15,1,1,2695,7.2292,,C\n',
     '354,0,3,"Arnold-Franchi, Mr. Josef",male,25,1,0,349237,17.8,,S\n',
     '355,0,3,"Yousif, Mr. Wazli",male,,0,0,2647,7.225,,C\n',
     '356,0,3,"Vanden Steen, Mr. Leo Peter",male,28,0,0,345783,9.5,,S\n',
     '357,1,1,"Bowerman, Miss. Elsie Edith",female,22,0,1,113505,55,E33,S\n',
     '358,0,2,"Funk, Miss. Annie Clemmer",female,38,0,0,237671,13,,S\n',
     '359,1,3,"McGovern, Miss. Mary",female,,0,0,330931,7.8792,,Q\n',
     '360,1,3,"Mockler, Miss. Helen Mary ""Ellie""",female,,0,0,330980,7.8792,,Q\n',
     '361,0,3,"Skoog, Mr. Wilhelm",male,40,1,4,347088,27.9,,S\n',
     '362,0,2,"del Carlo, Mr. Sebastiano",male,29,1,0,SC/PARIS 2167,27.7208,,C\n',
     '363,0,3,"Barbara, Mrs. (Catherine David)",female,45,0,1,2691,14.4542,,C\n',
     '364,0,3,"Asim, Mr. Adola",male,35,0,0,SOTON/O.Q. 3101310,7.05,,S\n',
     '365,0,3,"O\'Brien, Mr. Thomas",male,,1,0,370365,15.5,,Q\n',
     '366,0,3,"Adahl, Mr. Mauritz Nils Martin",male,30,0,0,C 7076,7.25,,S\n',
     '367,1,1,"Warren, Mrs. Frank Manley (Anna Sophia Atkinson)",female,60,1,0,110813,75.25,D37,C\n',
     '368,1,3,"Moussa, Mrs. (Mantoura Boulos)",female,,0,0,2626,7.2292,,C\n',
     '369,1,3,"Jermyn, Miss. Annie",female,,0,0,14313,7.75,,Q\n',
     '370,1,1,"Aubart, Mme. Leontine Pauline",female,24,0,0,PC 17477,69.3,B35,C\n',
     '371,1,1,"Harder, Mr. George Achilles",male,25,1,0,11765,55.4417,E50,C\n',
     '372,0,3,"Wiklund, Mr. Jakob Alfred",male,18,1,0,3101267,6.4958,,S\n',
     '373,0,3,"Beavan, Mr. William Thomas",male,19,0,0,323951,8.05,,S\n',
     '374,0,1,"Ringhini, Mr. Sante",male,22,0,0,PC 17760,135.6333,,C\n',
     '375,0,3,"Palsson, Miss. Stina Viola",female,3,3,1,349909,21.075,,S\n',
     '376,1,1,"Meyer, Mrs. Edgar Joseph (Leila Saks)",female,,1,0,PC 17604,82.1708,,C\n',
     '377,1,3,"Landergren, Miss. Aurora Adelia",female,22,0,0,C 7077,7.25,,S\n',
     '378,0,1,"Widener, Mr. Harry Elkins",male,27,0,2,113503,211.5,C82,C\n',
     '379,0,3,"Betros, Mr. Tannous",male,20,0,0,2648,4.0125,,C\n',
     '380,0,3,"Gustafsson, Mr. Karl Gideon",male,19,0,0,347069,7.775,,S\n',
     '381,1,1,"Bidois, Miss. Rosalie",female,42,0,0,PC 17757,227.525,,C\n',
     '382,1,3,"Nakid, Miss. Maria (""Mary"")",female,1,0,2,2653,15.7417,,C\n',
     '383,0,3,"Tikkanen, Mr. Juho",male,32,0,0,STON/O 2. 3101293,7.925,,S\n',
     '384,1,1,"Holverson, Mrs. Alexander Oskar (Mary Aline Towner)",female,35,1,0,113789,52,,S\n',
     '385,0,3,"Plotcharsky, Mr. Vasil",male,,0,0,349227,7.8958,,S\n',
     '386,0,2,"Davies, Mr. Charles Henry",male,18,0,0,S.O.C. 14879,73.5,,S\n',
     '387,0,3,"Goodwin, Master. Sidney Leonard",male,1,5,2,CA 2144,46.9,,S\n',
     '388,1,2,"Buss, Miss. Kate",female,36,0,0,27849,13,,S\n',
     '389,0,3,"Sadlier, Mr. Matthew",male,,0,0,367655,7.7292,,Q\n',
     '390,1,2,"Lehmann, Miss. Bertha",female,17,0,0,SC 1748,12,,C\n',
     '391,1,1,"Carter, Mr. William Ernest",male,36,1,2,113760,120,B96 B98,S\n',
     '392,1,3,"Jansson, Mr. Carl Olof",male,21,0,0,350034,7.7958,,S\n',
     '393,0,3,"Gustafsson, Mr. Johan Birger",male,28,2,0,3101277,7.925,,S\n',
     '394,1,1,"Newell, Miss. Marjorie",female,23,1,0,35273,113.275,D36,C\n',
     '395,1,3,"Sandstrom, Mrs. Hjalmar (Agnes Charlotta Bengtsson)",female,24,0,2,PP 9549,16.7,G6,S\n',
     '396,0,3,"Johansson, Mr. Erik",male,22,0,0,350052,7.7958,,S\n',
     '397,0,3,"Olsson, Miss. Elina",female,31,0,0,350407,7.8542,,S\n',
     '398,0,2,"McKane, Mr. Peter David",male,46,0,0,28403,26,,S\n',
     '399,0,2,"Pain, Dr. Alfred",male,23,0,0,244278,10.5,,S\n',
     '400,1,2,"Trout, Mrs. William H (Jessie L)",female,28,0,0,240929,12.65,,S\n',
     '401,1,3,"Niskanen, Mr. Juha",male,39,0,0,STON/O 2. 3101289,7.925,,S\n',
     '402,0,3,"Adams, Mr. John",male,26,0,0,341826,8.05,,S\n',
     '403,0,3,"Jussila, Miss. Mari Aina",female,21,1,0,4137,9.825,,S\n',
     '404,0,3,"Hakkarainen, Mr. Pekka Pietari",male,28,1,0,STON/O2. 3101279,15.85,,S\n',
     '405,0,3,"Oreskovic, Miss. Marija",female,20,0,0,315096,8.6625,,S\n',
     '406,0,2,"Gale, Mr. Shadrach",male,34,1,0,28664,21,,S\n',
     '407,0,3,"Widegren, Mr. Carl/Charles Peter",male,51,0,0,347064,7.75,,S\n',
     '408,1,2,"Richards, Master. William Rowe",male,3,1,1,29106,18.75,,S\n',
     '409,0,3,"Birkeland, Mr. Hans Martin Monsen",male,21,0,0,312992,7.775,,S\n',
     '410,0,3,"Lefebre, Miss. Ida",female,,3,1,4133,25.4667,,S\n',
     '411,0,3,"Sdycoff, Mr. Todor",male,,0,0,349222,7.8958,,S\n',
     '412,0,3,"Hart, Mr. Henry",male,,0,0,394140,6.8583,,Q\n',
     '413,1,1,"Minahan, Miss. Daisy E",female,33,1,0,19928,90,C78,Q\n',
     '414,0,2,"Cunningham, Mr. Alfred Fleming",male,,0,0,239853,0,,S\n',
     '415,1,3,"Sundman, Mr. Johan Julian",male,44,0,0,STON/O 2. 3101269,7.925,,S\n',
     '416,0,3,"Meek, Mrs. Thomas (Annie Louise Rowley)",female,,0,0,343095,8.05,,S\n',
     '417,1,2,"Drew, Mrs. James Vivian (Lulu Thorne Christian)",female,34,1,1,28220,32.5,,S\n',
     '418,1,2,"Silven, Miss. Lyyli Karoliina",female,18,0,2,250652,13,,S\n',
     '419,0,2,"Matthews, Mr. William John",male,30,0,0,28228,13,,S\n',
     '420,0,3,"Van Impe, Miss. Catharina",female,10,0,2,345773,24.15,,S\n',
     '421,0,3,"Gheorgheff, Mr. Stanio",male,,0,0,349254,7.8958,,C\n',
     '422,0,3,"Charters, Mr. David",male,21,0,0,A/5. 13032,7.7333,,Q\n',
     '423,0,3,"Zimmerman, Mr. Leo",male,29,0,0,315082,7.875,,S\n',
     '424,0,3,"Danbom, Mrs. Ernst Gilbert (Anna Sigrid Maria Brogren)",female,28,1,1,347080,14.4,,S\n',
     '425,0,3,"Rosblom, Mr. Viktor Richard",male,18,1,1,370129,20.2125,,S\n',
     '426,0,3,"Wiseman, Mr. Phillippe",male,,0,0,A/4. 34244,7.25,,S\n',
     '427,1,2,"Clarke, Mrs. Charles V (Ada Maria Winfield)",female,28,1,0,2003,26,,S\n',
     '428,1,2,"Phillips, Miss. Kate Florence (""Mrs Kate Louise Phillips Marshall"")",female,19,0,0,250655,26,,S\n',
     '429,0,3,"Flynn, Mr. James",male,,0,0,364851,7.75,,Q\n',
     '430,1,3,"Pickard, Mr. Berk (Berk Trembisky)",male,32,0,0,SOTON/O.Q. 392078,8.05,E10,S\n',
     '431,1,1,"Bjornstrom-Steffansson, Mr. Mauritz Hakan",male,28,0,0,110564,26.55,C52,S\n',
     '432,1,3,"Thorneycroft, Mrs. Percival (Florence Kate White)",female,,1,0,376564,16.1,,S\n',
     '433,1,2,"Louch, Mrs. Charles Alexander (Alice Adelaide Slow)",female,42,1,0,SC/AH 3085,26,,S\n',
     '434,0,3,"Kallio, Mr. Nikolai Erland",male,17,0,0,STON/O 2. 3101274,7.125,,S\n',
     '435,0,1,"Silvey, Mr. William Baird",male,50,1,0,13507,55.9,E44,S\n',
     '436,1,1,"Carter, Miss. Lucile Polk",female,14,1,2,113760,120,B96 B98,S\n',
     '437,0,3,"Ford, Miss. Doolina Margaret ""Daisy""",female,21,2,2,W./C. 6608,34.375,,S\n',
     '438,1,2,"Richards, Mrs. Sidney (Emily Hocking)",female,24,2,3,29106,18.75,,S\n',
     '439,0,1,"Fortune, Mr. Mark",male,64,1,4,19950,263,C23 C25 C27,S\n',
     '440,0,2,"Kvillner, Mr. Johan Henrik Johannesson",male,31,0,0,C.A. 18723,10.5,,S\n',
     '441,1,2,"Hart, Mrs. Benjamin (Esther Ada Bloomfield)",female,45,1,1,F.C.C. 13529,26.25,,S\n',
     '442,0,3,"Hampe, Mr. Leon",male,20,0,0,345769,9.5,,S\n',
     '443,0,3,"Petterson, Mr. Johan Emil",male,25,1,0,347076,7.775,,S\n',
     '444,1,2,"Reynaldo, Ms. Encarnacion",female,28,0,0,230434,13,,S\n',
     '445,1,3,"Johannesen-Bratthammer, Mr. Bernt",male,,0,0,65306,8.1125,,S\n',
     '446,1,1,"Dodge, Master. Washington",male,4,0,2,33638,81.8583,A34,S\n',
     '447,1,2,"Mellinger, Miss. Madeleine Violet",female,13,0,1,250644,19.5,,S\n',
     '448,1,1,"Seward, Mr. Frederic Kimber",male,34,0,0,113794,26.55,,S\n',
     '449,1,3,"Baclini, Miss. Marie Catherine",female,5,2,1,2666,19.2583,,C\n',
     '450,1,1,"Peuchen, Major. Arthur Godfrey",male,52,0,0,113786,30.5,C104,S\n',
     '451,0,2,"West, Mr. Edwy Arthur",male,36,1,2,C.A. 34651,27.75,,S\n',
     '452,0,3,"Hagland, Mr. Ingvald Olai Olsen",male,,1,0,65303,19.9667,,S\n',
     '453,0,1,"Foreman, Mr. Benjamin Laventall",male,30,0,0,113051,27.75,C111,C\n',
     '454,1,1,"Goldenberg, Mr. Samuel L",male,49,1,0,17453,89.1042,C92,C\n',
     '455,0,3,"Peduzzi, Mr. Joseph",male,,0,0,A/5 2817,8.05,,S\n',
     '456,1,3,"Jalsevac, Mr. Ivan",male,29,0,0,349240,7.8958,,C\n',
     '457,0,1,"Millet, Mr. Francis Davis",male,65,0,0,13509,26.55,E38,S\n',
     '458,1,1,"Kenyon, Mrs. Frederick R (Marion)",female,,1,0,17464,51.8625,D21,S\n',
     '459,1,2,"Toomey, Miss. Ellen",female,50,0,0,F.C.C. 13531,10.5,,S\n',
     '460,0,3,"O\'Connor, Mr. Maurice",male,,0,0,371060,7.75,,Q\n',
     '461,1,1,"Anderson, Mr. Harry",male,48,0,0,19952,26.55,E12,S\n',
     '462,0,3,"Morley, Mr. William",male,34,0,0,364506,8.05,,S\n',
     '463,0,1,"Gee, Mr. Arthur H",male,47,0,0,111320,38.5,E63,S\n',
     '464,0,2,"Milling, Mr. Jacob Christian",male,48,0,0,234360,13,,S\n',
     '465,0,3,"Maisner, Mr. Simon",male,,0,0,A/S 2816,8.05,,S\n',
     '466,0,3,"Goncalves, Mr. Manuel Estanslas",male,38,0,0,SOTON/O.Q. 3101306,7.05,,S\n',
     '467,0,2,"Campbell, Mr. William",male,,0,0,239853,0,,S\n',
     '468,0,1,"Smart, Mr. John Montgomery",male,56,0,0,113792,26.55,,S\n',
     '469,0,3,"Scanlan, Mr. James",male,,0,0,36209,7.725,,Q\n',
     '470,1,3,"Baclini, Miss. Helene Barbara",female,0.75,2,1,2666,19.2583,,C\n',
     '471,0,3,"Keefe, Mr. Arthur",male,,0,0,323592,7.25,,S\n',
     '472,0,3,"Cacic, Mr. Luka",male,38,0,0,315089,8.6625,,S\n',
     '473,1,2,"West, Mrs. Edwy Arthur (Ada Mary Worth)",female,33,1,2,C.A. 34651,27.75,,S\n',
     '474,1,2,"Jerwan, Mrs. Amin S (Marie Marthe Thuillard)",female,23,0,0,SC/AH Basle 541,13.7917,D,C\n',
     '475,0,3,"Strandberg, Miss. Ida Sofia",female,22,0,0,7553,9.8375,,S\n',
     '476,0,1,"Clifford, Mr. George Quincy",male,,0,0,110465,52,A14,S\n',
     '477,0,2,"Renouf, Mr. Peter Henry",male,34,1,0,31027,21,,S\n',
     '478,0,3,"Braund, Mr. Lewis Richard",male,29,1,0,3460,7.0458,,S\n',
     '479,0,3,"Karlsson, Mr. Nils August",male,22,0,0,350060,7.5208,,S\n',
     '480,1,3,"Hirvonen, Miss. Hildur E",female,2,0,1,3101298,12.2875,,S\n',
     '481,0,3,"Goodwin, Master. Harold Victor",male,9,5,2,CA 2144,46.9,,S\n',
     '482,0,2,"Frost, Mr. Anthony Wood ""Archie""",male,,0,0,239854,0,,S\n',
     '483,0,3,"Rouse, Mr. Richard Henry",male,50,0,0,A/5 3594,8.05,,S\n',
     '484,1,3,"Turkula, Mrs. (Hedwig)",female,63,0,0,4134,9.5875,,S\n',
     '485,1,1,"Bishop, Mr. Dickinson H",male,25,1,0,11967,91.0792,B49,C\n',
     '486,0,3,"Lefebre, Miss. Jeannie",female,,3,1,4133,25.4667,,S\n',
     '487,1,1,"Hoyt, Mrs. Frederick Maxfield (Jane Anne Forby)",female,35,1,0,19943,90,C93,S\n',
     '488,0,1,"Kent, Mr. Edward Austin",male,58,0,0,11771,29.7,B37,C\n',
     '489,0,3,"Somerton, Mr. Francis William",male,30,0,0,A.5. 18509,8.05,,S\n',
     '490,1,3,"Coutts, Master. Eden Leslie ""Neville""",male,9,1,1,C.A. 37671,15.9,,S\n',
     '491,0,3,"Hagland, Mr. Konrad Mathias Reiersen",male,,1,0,65304,19.9667,,S\n',
     '492,0,3,"Windelov, Mr. Einar",male,21,0,0,SOTON/OQ 3101317,7.25,,S\n',
     '493,0,1,"Molson, Mr. Harry Markland",male,55,0,0,113787,30.5,C30,S\n',
     '494,0,1,"Artagaveytia, Mr. Ramon",male,71,0,0,PC 17609,49.5042,,C\n',
     '495,0,3,"Stanley, Mr. Edward Roland",male,21,0,0,A/4 45380,8.05,,S\n',
     '496,0,3,"Yousseff, Mr. Gerious",male,,0,0,2627,14.4583,,C\n',
     '497,1,1,"Eustis, Miss. Elizabeth Mussey",female,54,1,0,36947,78.2667,D20,C\n',
     '498,0,3,"Shellard, Mr. Frederick William",male,,0,0,C.A. 6212,15.1,,S\n',
     '499,0,1,"Allison, Mrs. Hudson J C (Bessie Waldo Daniels)",female,25,1,2,113781,151.55,C22 C26,S\n',
     '500,0,3,"Svensson, Mr. Olof",male,24,0,0,350035,7.7958,,S\n',
     '501,0,3,"Calic, Mr. Petar",male,17,0,0,315086,8.6625,,S\n',
     '502,0,3,"Canavan, Miss. Mary",female,21,0,0,364846,7.75,,Q\n',
     '503,0,3,"O\'Sullivan, Miss. Bridget Mary",female,,0,0,330909,7.6292,,Q\n',
     '504,0,3,"Laitinen, Miss. Kristina Sofia",female,37,0,0,4135,9.5875,,S\n',
     '505,1,1,"Maioni, Miss. Roberta",female,16,0,0,110152,86.5,B79,S\n',
     '506,0,1,"Penasco y Castellana, Mr. Victor de Satode",male,18,1,0,PC 17758,108.9,C65,C\n',
     '507,1,2,"Quick, Mrs. Frederick Charles (Jane Richards)",female,33,0,2,26360,26,,S\n',
     '508,1,1,"Bradley, Mr. George (""George Arthur Brayton"")",male,,0,0,111427,26.55,,S\n',
     '509,0,3,"Olsen, Mr. Henry Margido",male,28,0,0,C 4001,22.525,,S\n',
     '510,1,3,"Lang, Mr. Fang",male,26,0,0,1601,56.4958,,S\n',
     '511,1,3,"Daly, Mr. Eugene Patrick",male,29,0,0,382651,7.75,,Q\n',
     '512,0,3,"Webber, Mr. James",male,,0,0,SOTON/OQ 3101316,8.05,,S\n',
     '513,1,1,"McGough, Mr. James Robert",male,36,0,0,PC 17473,26.2875,E25,S\n',
     '514,1,1,"Rothschild, Mrs. Martin (Elizabeth L. Barrett)",female,54,1,0,PC 17603,59.4,,C\n',
     '515,0,3,"Coleff, Mr. Satio",male,24,0,0,349209,7.4958,,S\n',
     '516,0,1,"Walker, Mr. William Anderson",male,47,0,0,36967,34.0208,D46,S\n',
     '517,1,2,"Lemore, Mrs. (Amelia Milley)",female,34,0,0,C.A. 34260,10.5,F33,S\n',
     '518,0,3,"Ryan, Mr. Patrick",male,,0,0,371110,24.15,,Q\n',
     '519,1,2,"Angle, Mrs. William A (Florence ""Mary"" Agnes Hughes)",female,36,1,0,226875,26,,S\n',
     '520,0,3,"Pavlovic, Mr. Stefo",male,32,0,0,349242,7.8958,,S\n',
     '521,1,1,"Perreault, Miss. Anne",female,30,0,0,12749,93.5,B73,S\n',
     '522,0,3,"Vovk, Mr. Janko",male,22,0,0,349252,7.8958,,S\n',
     '523,0,3,"Lahoud, Mr. Sarkis",male,,0,0,2624,7.225,,C\n',
     '524,1,1,"Hippach, Mrs. Louis Albert (Ida Sophia Fischer)",female,44,0,1,111361,57.9792,B18,C\n',
     '525,0,3,"Kassem, Mr. Fared",male,,0,0,2700,7.2292,,C\n',
     '526,0,3,"Farrell, Mr. James",male,40.5,0,0,367232,7.75,,Q\n',
     '527,1,2,"Ridsdale, Miss. Lucy",female,50,0,0,W./C. 14258,10.5,,S\n',
     '528,0,1,"Farthing, Mr. John",male,,0,0,PC 17483,221.7792,C95,S\n',
     '529,0,3,"Salonen, Mr. Johan Werner",male,39,0,0,3101296,7.925,,S\n',
     '530,0,2,"Hocking, Mr. Richard George",male,23,2,1,29104,11.5,,S\n',
     '531,1,2,"Quick, Miss. Phyllis May",female,2,1,1,26360,26,,S\n',
     '532,0,3,"Toufik, Mr. Nakli",male,,0,0,2641,7.2292,,C\n',
     '533,0,3,"Elias, Mr. Joseph Jr",male,17,1,1,2690,7.2292,,C\n',
     '534,1,3,"Peter, Mrs. Catherine (Catherine Rizk)",female,,0,2,2668,22.3583,,C\n',
     '535,0,3,"Cacic, Miss. Marija",female,30,0,0,315084,8.6625,,S\n',
     '536,1,2,"Hart, Miss. Eva Miriam",female,7,0,2,F.C.C. 13529,26.25,,S\n',
     '537,0,1,"Butt, Major. Archibald Willingham",male,45,0,0,113050,26.55,B38,S\n',
     '538,1,1,"LeRoy, Miss. Bertha",female,30,0,0,PC 17761,106.425,,C\n',
     '539,0,3,"Risien, Mr. Samuel Beard",male,,0,0,364498,14.5,,S\n',
     '540,1,1,"Frolicher, Miss. Hedwig Margaritha",female,22,0,2,13568,49.5,B39,C\n',
     '541,1,1,"Crosby, Miss. Harriet R",female,36,0,2,WE/P 5735,71,B22,S\n',
     '542,0,3,"Andersson, Miss. Ingeborg Constanzia",female,9,4,2,347082,31.275,,S\n',
     '543,0,3,"Andersson, Miss. Sigrid Elisabeth",female,11,4,2,347082,31.275,,S\n',
     '544,1,2,"Beane, Mr. Edward",male,32,1,0,2908,26,,S\n',
     '545,0,1,"Douglas, Mr. Walter Donald",male,50,1,0,PC 17761,106.425,C86,C\n',
     '546,0,1,"Nicholson, Mr. Arthur Ernest",male,64,0,0,693,26,,S\n',
     '547,1,2,"Beane, Mrs. Edward (Ethel Clarke)",female,19,1,0,2908,26,,S\n',
     '548,1,2,"Padro y Manent, Mr. Julian",male,,0,0,SC/PARIS 2146,13.8625,,C\n',
     '549,0,3,"Goldsmith, Mr. Frank John",male,33,1,1,363291,20.525,,S\n',
     '550,1,2,"Davies, Master. John Morgan Jr",male,8,1,1,C.A. 33112,36.75,,S\n',
     '551,1,1,"Thayer, Mr. John Borland Jr",male,17,0,2,17421,110.8833,C70,C\n',
     '552,0,2,"Sharp, Mr. Percival James R",male,27,0,0,244358,26,,S\n',
     '553,0,3,"O\'Brien, Mr. Timothy",male,,0,0,330979,7.8292,,Q\n',
     '554,1,3,"Leeni, Mr. Fahim (""Philip Zenni"")",male,22,0,0,2620,7.225,,C\n',
     '555,1,3,"Ohman, Miss. Velin",female,22,0,0,347085,7.775,,S\n',
     '556,0,1,"Wright, Mr. George",male,62,0,0,113807,26.55,,S\n',
     '557,1,1,"Duff Gordon, Lady. (Lucille Christiana Sutherland) (""Mrs Morgan"")",female,48,1,0,11755,39.6,A16,C\n',
     '558,0,1,"Robbins, Mr. Victor",male,,0,0,PC 17757,227.525,,C\n',
     '559,1,1,"Taussig, Mrs. Emil (Tillie Mandelbaum)",female,39,1,1,110413,79.65,E67,S\n',
     '560,1,3,"de Messemaeker, Mrs. Guillaume Joseph (Emma)",female,36,1,0,345572,17.4,,S\n',
     '561,0,3,"Morrow, Mr. Thomas Rowan",male,,0,0,372622,7.75,,Q\n',
     '562,0,3,"Sivic, Mr. Husein",male,40,0,0,349251,7.8958,,S\n',
     '563,0,2,"Norman, Mr. Robert Douglas",male,28,0,0,218629,13.5,,S\n',
     '564,0,3,"Simmons, Mr. John",male,,0,0,SOTON/OQ 392082,8.05,,S\n',
     '565,0,3,"Meanwell, Miss. (Marion Ogden)",female,,0,0,SOTON/O.Q. 392087,8.05,,S\n',
     '566,0,3,"Davies, Mr. Alfred J",male,24,2,0,A/4 48871,24.15,,S\n',
     '567,0,3,"Stoytcheff, Mr. Ilia",male,19,0,0,349205,7.8958,,S\n',
     '568,0,3,"Palsson, Mrs. Nils (Alma Cornelia Berglund)",female,29,0,4,349909,21.075,,S\n',
     '569,0,3,"Doharr, Mr. Tannous",male,,0,0,2686,7.2292,,C\n',
     '570,1,3,"Jonsson, Mr. Carl",male,32,0,0,350417,7.8542,,S\n',
     '571,1,2,"Harris, Mr. George",male,62,0,0,S.W./PP 752,10.5,,S\n',
     '572,1,1,"Appleton, Mrs. Edward Dale (Charlotte Lamson)",female,53,2,0,11769,51.4792,C101,S\n',
     '573,1,1,"Flynn, Mr. John Irwin (""Irving"")",male,36,0,0,PC 17474,26.3875,E25,S\n',
     '574,1,3,"Kelly, Miss. Mary",female,,0,0,14312,7.75,,Q\n',
     '575,0,3,"Rush, Mr. Alfred George John",male,16,0,0,A/4. 20589,8.05,,S\n',
     '576,0,3,"Patchett, Mr. George",male,19,0,0,358585,14.5,,S\n',
     '577,1,2,"Garside, Miss. Ethel",female,34,0,0,243880,13,,S\n',
     '578,1,1,"Silvey, Mrs. William Baird (Alice Munger)",female,39,1,0,13507,55.9,E44,S\n',
     '579,0,3,"Caram, Mrs. Joseph (Maria Elias)",female,,1,0,2689,14.4583,,C\n',
     '580,1,3,"Jussila, Mr. Eiriik",male,32,0,0,STON/O 2. 3101286,7.925,,S\n',
     '581,1,2,"Christy, Miss. Julie Rachel",female,25,1,1,237789,30,,S\n',
     '582,1,1,"Thayer, Mrs. John Borland (Marian Longstreth Morris)",female,39,1,1,17421,110.8833,C68,C\n',
     '583,0,2,"Downton, Mr. William James",male,54,0,0,28403,26,,S\n',
     '584,0,1,"Ross, Mr. John Hugo",male,36,0,0,13049,40.125,A10,C\n',
     '585,0,3,"Paulner, Mr. Uscher",male,,0,0,3411,8.7125,,C\n',
     '586,1,1,"Taussig, Miss. Ruth",female,18,0,2,110413,79.65,E68,S\n',
     '587,0,2,"Jarvis, Mr. John Denzil",male,47,0,0,237565,15,,S\n',
     '588,1,1,"Frolicher-Stehli, Mr. Maxmillian",male,60,1,1,13567,79.2,B41,C\n',
     '589,0,3,"Gilinski, Mr. Eliezer",male,22,0,0,14973,8.05,,S\n',
     '590,0,3,"Murdlin, Mr. Joseph",male,,0,0,A./5. 3235,8.05,,S\n',
     '591,0,3,"Rintamaki, Mr. Matti",male,35,0,0,STON/O 2. 3101273,7.125,,S\n',
     '592,1,1,"Stephenson, Mrs. Walter Bertram (Martha Eustis)",female,52,1,0,36947,78.2667,D20,C\n',
     '593,0,3,"Elsbury, Mr. William James",male,47,0,0,A/5 3902,7.25,,S\n',
     '594,0,3,"Bourke, Miss. Mary",female,,0,2,364848,7.75,,Q\n',
     '595,0,2,"Chapman, Mr. John Henry",male,37,1,0,SC/AH 29037,26,,S\n',
     '596,0,3,"Van Impe, Mr. Jean Baptiste",male,36,1,1,345773,24.15,,S\n',
     '597,1,2,"Leitch, Miss. Jessie Wills",female,,0,0,248727,33,,S\n',
     '598,0,3,"Johnson, Mr. Alfred",male,49,0,0,LINE,0,,S\n',
     '599,0,3,"Boulos, Mr. Hanna",male,,0,0,2664,7.225,,C\n',
     '600,1,1,"Duff Gordon, Sir. Cosmo Edmund (""Mr Morgan"")",male,49,1,0,PC 17485,56.9292,A20,C\n',
     '601,1,2,"Jacobsohn, Mrs. Sidney Samuel (Amy Frances Christy)",female,24,2,1,243847,27,,S\n',
     '602,0,3,"Slabenoff, Mr. Petco",male,,0,0,349214,7.8958,,S\n',
     '603,0,1,"Harrington, Mr. Charles H",male,,0,0,113796,42.4,,S\n',
     '604,0,3,"Torber, Mr. Ernst William",male,44,0,0,364511,8.05,,S\n',
     '605,1,1,"Homer, Mr. Harry (""Mr E Haven"")",male,35,0,0,111426,26.55,,C\n',
     '606,0,3,"Lindell, Mr. Edvard Bengtsson",male,36,1,0,349910,15.55,,S\n',
     '607,0,3,"Karaic, Mr. Milan",male,30,0,0,349246,7.8958,,S\n',
     '608,1,1,"Daniel, Mr. Robert Williams",male,27,0,0,113804,30.5,,S\n',
     '609,1,2,"Laroche, Mrs. Joseph (Juliette Marie Louise Lafargue)",female,22,1,2,SC/Paris 2123,41.5792,,C\n',
     '610,1,1,"Shutes, Miss. Elizabeth W",female,40,0,0,PC 17582,153.4625,C125,S\n',
     '611,0,3,"Andersson, Mrs. Anders Johan (Alfrida Konstantia Brogren)",female,39,1,5,347082,31.275,,S\n',
     '612,0,3,"Jardin, Mr. Jose Neto",male,,0,0,SOTON/O.Q. 3101305,7.05,,S\n',
     '613,1,3,"Murphy, Miss. Margaret Jane",female,,1,0,367230,15.5,,Q\n',
     '614,0,3,"Horgan, Mr. John",male,,0,0,370377,7.75,,Q\n',
     '615,0,3,"Brocklebank, Mr. William Alfred",male,35,0,0,364512,8.05,,S\n',
     '616,1,2,"Herman, Miss. Alice",female,24,1,2,220845,65,,S\n',
     '617,0,3,"Danbom, Mr. Ernst Gilbert",male,34,1,1,347080,14.4,,S\n',
     '618,0,3,"Lobb, Mrs. William Arthur (Cordelia K Stanlick)",female,26,1,0,A/5. 3336,16.1,,S\n',
     '619,1,2,"Becker, Miss. Marion Louise",female,4,2,1,230136,39,F4,S\n',
     '620,0,2,"Gavey, Mr. Lawrence",male,26,0,0,31028,10.5,,S\n',
     '621,0,3,"Yasbeck, Mr. Antoni",male,27,1,0,2659,14.4542,,C\n',
     '622,1,1,"Kimball, Mr. Edwin Nelson Jr",male,42,1,0,11753,52.5542,D19,S\n',
     '623,1,3,"Nakid, Mr. Sahid",male,20,1,1,2653,15.7417,,C\n',
     '624,0,3,"Hansen, Mr. Henry Damsgaard",male,21,0,0,350029,7.8542,,S\n',
     '625,0,3,"Bowen, Mr. David John ""Dai""",male,21,0,0,54636,16.1,,S\n',
     '626,0,1,"Sutton, Mr. Frederick",male,61,0,0,36963,32.3208,D50,S\n',
     '627,0,2,"Kirkland, Rev. Charles Leonard",male,57,0,0,219533,12.35,,Q\n',
     '628,1,1,"Longley, Miss. Gretchen Fiske",female,21,0,0,13502,77.9583,D9,S\n',
     '629,0,3,"Bostandyeff, Mr. Guentcho",male,26,0,0,349224,7.8958,,S\n',
     '630,0,3,"O\'Connell, Mr. Patrick D",male,,0,0,334912,7.7333,,Q\n',
     '631,1,1,"Barkworth, Mr. Algernon Henry Wilson",male,80,0,0,27042,30,A23,S\n',
     '632,0,3,"Lundahl, Mr. Johan Svensson",male,51,0,0,347743,7.0542,,S\n',
     '633,1,1,"Stahelin-Maeglin, Dr. Max",male,32,0,0,13214,30.5,B50,C\n',
     '634,0,1,"Parr, Mr. William Henry Marsh",male,,0,0,112052,0,,S\n',
     '635,0,3,"Skoog, Miss. Mabel",female,9,3,2,347088,27.9,,S\n',
     '636,1,2,"Davis, Miss. Mary",female,28,0,0,237668,13,,S\n',
     '637,0,3,"Leinonen, Mr. Antti Gustaf",male,32,0,0,STON/O 2. 3101292,7.925,,S\n',
     '638,0,2,"Collyer, Mr. Harvey",male,31,1,1,C.A. 31921,26.25,,S\n',
     '639,0,3,"Panula, Mrs. Juha (Maria Emilia Ojala)",female,41,0,5,3101295,39.6875,,S\n',
     '640,0,3,"Thorneycroft, Mr. Percival",male,,1,0,376564,16.1,,S\n',
     '641,0,3,"Jensen, Mr. Hans Peder",male,20,0,0,350050,7.8542,,S\n',
     '642,1,1,"Sagesser, Mlle. Emma",female,24,0,0,PC 17477,69.3,B35,C\n',
     '643,0,3,"Skoog, Miss. Margit Elizabeth",female,2,3,2,347088,27.9,,S\n',
     '644,1,3,"Foo, Mr. Choong",male,,0,0,1601,56.4958,,S\n',
     '645,1,3,"Baclini, Miss. Eugenie",female,0.75,2,1,2666,19.2583,,C\n',
     '646,1,1,"Harper, Mr. Henry Sleeper",male,48,1,0,PC 17572,76.7292,D33,C\n',
     '647,0,3,"Cor, Mr. Liudevit",male,19,0,0,349231,7.8958,,S\n',
     '648,1,1,"Simonius-Blumer, Col. Oberst Alfons",male,56,0,0,13213,35.5,A26,C\n',
     '649,0,3,"Willey, Mr. Edward",male,,0,0,S.O./P.P. 751,7.55,,S\n',
     '650,1,3,"Stanley, Miss. Amy Zillah Elsie",female,23,0,0,CA. 2314,7.55,,S\n',
     '651,0,3,"Mitkoff, Mr. Mito",male,,0,0,349221,7.8958,,S\n',
     '652,1,2,"Doling, Miss. Elsie",female,18,0,1,231919,23,,S\n',
     '653,0,3,"Kalvik, Mr. Johannes Halvorsen",male,21,0,0,8475,8.4333,,S\n',
     '654,1,3,"O\'Leary, Miss. Hanora ""Norah""",female,,0,0,330919,7.8292,,Q\n',
     '655,0,3,"Hegarty, Miss. Hanora ""Nora""",female,18,0,0,365226,6.75,,Q\n',
     '656,0,2,"Hickman, Mr. Leonard Mark",male,24,2,0,S.O.C. 14879,73.5,,S\n',
     '657,0,3,"Radeff, Mr. Alexander",male,,0,0,349223,7.8958,,S\n',
     '658,0,3,"Bourke, Mrs. John (Catherine)",female,32,1,1,364849,15.5,,Q\n',
     '659,0,2,"Eitemiller, Mr. George Floyd",male,23,0,0,29751,13,,S\n',
     '660,0,1,"Newell, Mr. Arthur Webster",male,58,0,2,35273,113.275,D48,C\n',
     '661,1,1,"Frauenthal, Dr. Henry William",male,50,2,0,PC 17611,133.65,,S\n',
     '662,0,3,"Badt, Mr. Mohamed",male,40,0,0,2623,7.225,,C\n',
     '663,0,1,"Colley, Mr. Edward Pomeroy",male,47,0,0,5727,25.5875,E58,S\n',
     '664,0,3,"Coleff, Mr. Peju",male,36,0,0,349210,7.4958,,S\n',
     '665,1,3,"Lindqvist, Mr. Eino William",male,20,1,0,STON/O 2. 3101285,7.925,,S\n',
     '666,0,2,"Hickman, Mr. Lewis",male,32,2,0,S.O.C. 14879,73.5,,S\n',
     '667,0,2,"Butler, Mr. Reginald Fenton",male,25,0,0,234686,13,,S\n',
     '668,0,3,"Rommetvedt, Mr. Knud Paust",male,,0,0,312993,7.775,,S\n',
     '669,0,3,"Cook, Mr. Jacob",male,43,0,0,A/5 3536,8.05,,S\n',
     '670,1,1,"Taylor, Mrs. Elmer Zebley (Juliet Cummins Wright)",female,,1,0,19996,52,C126,S\n',
     '671,1,2,"Brown, Mrs. Thomas William Solomon (Elizabeth Catherine Ford)",female,40,1,1,29750,39,,S\n',
     '672,0,1,"Davidson, Mr. Thornton",male,31,1,0,F.C. 12750,52,B71,S\n',
     '673,0,2,"Mitchell, Mr. Henry Michael",male,70,0,0,C.A. 24580,10.5,,S\n',
     '674,1,2,"Wilhelms, Mr. Charles",male,31,0,0,244270,13,,S\n',
     '675,0,2,"Watson, Mr. Ennis Hastings",male,,0,0,239856,0,,S\n',
     '676,0,3,"Edvardsson, Mr. Gustaf Hjalmar",male,18,0,0,349912,7.775,,S\n',
     '677,0,3,"Sawyer, Mr. Frederick Charles",male,24.5,0,0,342826,8.05,,S\n',
     '678,1,3,"Turja, Miss. Anna Sofia",female,18,0,0,4138,9.8417,,S\n',
     '679,0,3,"Goodwin, Mrs. Frederick (Augusta Tyler)",female,43,1,6,CA 2144,46.9,,S\n',
     '680,1,1,"Cardeza, Mr. Thomas Drake Martinez",male,36,0,1,PC 17755,512.3292,B51 B53 B55,C\n',
     '681,0,3,"Peters, Miss. Katie",female,,0,0,330935,8.1375,,Q\n',
     '682,1,1,"Hassab, Mr. Hammad",male,27,0,0,PC 17572,76.7292,D49,C\n',
     '683,0,3,"Olsvigen, Mr. Thor Anderson",male,20,0,0,6563,9.225,,S\n',
     '684,0,3,"Goodwin, Mr. Charles Edward",male,14,5,2,CA 2144,46.9,,S\n',
     '685,0,2,"Brown, Mr. Thomas William Solomon",male,60,1,1,29750,39,,S\n',
     '686,0,2,"Laroche, Mr. Joseph Philippe Lemercier",male,25,1,2,SC/Paris 2123,41.5792,,C\n',
     '687,0,3,"Panula, Mr. Jaako Arnold",male,14,4,1,3101295,39.6875,,S\n',
     '688,0,3,"Dakic, Mr. Branko",male,19,0,0,349228,10.1708,,S\n',
     '689,0,3,"Fischer, Mr. Eberhard Thelander",male,18,0,0,350036,7.7958,,S\n',
     '690,1,1,"Madill, Miss. Georgette Alexandra",female,15,0,1,24160,211.3375,B5,S\n',
     '691,1,1,"Dick, Mr. Albert Adrian",male,31,1,0,17474,57,B20,S\n',
     '692,1,3,"Karun, Miss. Manca",female,4,0,1,349256,13.4167,,C\n',
     '693,1,3,"Lam, Mr. Ali",male,,0,0,1601,56.4958,,S\n',
     '694,0,3,"Saad, Mr. Khalil",male,25,0,0,2672,7.225,,C\n',
     '695,0,1,"Weir, Col. John",male,60,0,0,113800,26.55,,S\n',
     '696,0,2,"Chapman, Mr. Charles Henry",male,52,0,0,248731,13.5,,S\n',
     '697,0,3,"Kelly, Mr. James",male,44,0,0,363592,8.05,,S\n',
     '698,1,3,"Mullens, Miss. Katherine ""Katie""",female,,0,0,35852,7.7333,,Q\n',
     '699,0,1,"Thayer, Mr. John Borland",male,49,1,1,17421,110.8833,C68,C\n',
     '700,0,3,"Humblen, Mr. Adolf Mathias Nicolai Olsen",male,42,0,0,348121,7.65,F G63,S\n',
     '701,1,1,"Astor, Mrs. John Jacob (Madeleine Talmadge Force)",female,18,1,0,PC 17757,227.525,C62 C64,C\n',
     '702,1,1,"Silverthorne, Mr. Spencer Victor",male,35,0,0,PC 17475,26.2875,E24,S\n',
     '703,0,3,"Barbara, Miss. Saiide",female,18,0,1,2691,14.4542,,C\n',
     '704,0,3,"Gallagher, Mr. Martin",male,25,0,0,36864,7.7417,,Q\n',
     '705,0,3,"Hansen, Mr. Henrik Juul",male,26,1,0,350025,7.8542,,S\n',
     '706,0,2,"Morley, Mr. Henry Samuel (""Mr Henry Marshall"")",male,39,0,0,250655,26,,S\n',
     '707,1,2,"Kelly, Mrs. Florence ""Fannie""",female,45,0,0,223596,13.5,,S\n',
     '708,1,1,"Calderhead, Mr. Edward Pennington",male,42,0,0,PC 17476,26.2875,E24,S\n',
     '709,1,1,"Cleaver, Miss. Alice",female,22,0,0,113781,151.55,,S\n',
     '710,1,3,"Moubarek, Master. Halim Gonios (""William George"")",male,,1,1,2661,15.2458,,C\n',
     '711,1,1,"Mayne, Mlle. Berthe Antonine (""Mrs de Villiers"")",female,24,0,0,PC 17482,49.5042,C90,C\n',
     '712,0,1,"Klaber, Mr. Herman",male,,0,0,113028,26.55,C124,S\n',
     '713,1,1,"Taylor, Mr. Elmer Zebley",male,48,1,0,19996,52,C126,S\n',
     '714,0,3,"Larsson, Mr. August Viktor",male,29,0,0,7545,9.4833,,S\n',
     '715,0,2,"Greenberg, Mr. Samuel",male,52,0,0,250647,13,,S\n',
     '716,0,3,"Soholt, Mr. Peter Andreas Lauritz Andersen",male,19,0,0,348124,7.65,F G73,S\n',
     '717,1,1,"Endres, Miss. Caroline Louise",female,38,0,0,PC 17757,227.525,C45,C\n',
     '718,1,2,"Troutt, Miss. Edwina Celia ""Winnie""",female,27,0,0,34218,10.5,E101,S\n',
     '719,0,3,"McEvoy, Mr. Michael",male,,0,0,36568,15.5,,Q\n',
     '720,0,3,"Johnson, Mr. Malkolm Joackim",male,33,0,0,347062,7.775,,S\n',
     '721,1,2,"Harper, Miss. Annie Jessie ""Nina""",female,6,0,1,248727,33,,S\n',
     '722,0,3,"Jensen, Mr. Svend Lauritz",male,17,1,0,350048,7.0542,,S\n',
     '723,0,2,"Gillespie, Mr. William Henry",male,34,0,0,12233,13,,S\n',
     '724,0,2,"Hodges, Mr. Henry Price",male,50,0,0,250643,13,,S\n',
     '725,1,1,"Chambers, Mr. Norman Campbell",male,27,1,0,113806,53.1,E8,S\n',
     '726,0,3,"Oreskovic, Mr. Luka",male,20,0,0,315094,8.6625,,S\n',
     '727,1,2,"Renouf, Mrs. Peter Henry (Lillian Jefferys)",female,30,3,0,31027,21,,S\n',
     '728,1,3,"Mannion, Miss. Margareth",female,,0,0,36866,7.7375,,Q\n',
     '729,0,2,"Bryhl, Mr. Kurt Arnold Gottfrid",male,25,1,0,236853,26,,S\n',
     '730,0,3,"Ilmakangas, Miss. Pieta Sofia",female,25,1,0,STON/O2. 3101271,7.925,,S\n',
     '731,1,1,"Allen, Miss. Elisabeth Walton",female,29,0,0,24160,211.3375,B5,S\n',
     '732,0,3,"Hassan, Mr. Houssein G N",male,11,0,0,2699,18.7875,,C\n',
     '733,0,2,"Knight, Mr. Robert J",male,,0,0,239855,0,,S\n',
     '734,0,2,"Berriman, Mr. William John",male,23,0,0,28425,13,,S\n',
     '735,0,2,"Troupiansky, Mr. Moses Aaron",male,23,0,0,233639,13,,S\n',
     '736,0,3,"Williams, Mr. Leslie",male,28.5,0,0,54636,16.1,,S\n',
     '737,0,3,"Ford, Mrs. Edward (Margaret Ann Watson)",female,48,1,3,W./C. 6608,34.375,,S\n',
     '738,1,1,"Lesurer, Mr. Gustave J",male,35,0,0,PC 17755,512.3292,B101,C\n',
     '739,0,3,"Ivanoff, Mr. Kanio",male,,0,0,349201,7.8958,,S\n',
     '740,0,3,"Nankoff, Mr. Minko",male,,0,0,349218,7.8958,,S\n',
     '741,1,1,"Hawksford, Mr. Walter James",male,,0,0,16988,30,D45,S\n',
     '742,0,1,"Cavendish, Mr. Tyrell William",male,36,1,0,19877,78.85,C46,S\n',
     '743,1,1,"Ryerson, Miss. Susan Parker ""Suzette""",female,21,2,2,PC 17608,262.375,B57 B59 B63 B66,C\n',
     '744,0,3,"McNamee, Mr. Neal",male,24,1,0,376566,16.1,,S\n',
     '745,1,3,"Stranden, Mr. Juho",male,31,0,0,STON/O 2. 3101288,7.925,,S\n',
     '746,0,1,"Crosby, Capt. Edward Gifford",male,70,1,1,WE/P 5735,71,B22,S\n',
     '747,0,3,"Abbott, Mr. Rossmore Edward",male,16,1,1,C.A. 2673,20.25,,S\n',
     '748,1,2,"Sinkkonen, Miss. Anna",female,30,0,0,250648,13,,S\n',
     '749,0,1,"Marvin, Mr. Daniel Warner",male,19,1,0,113773,53.1,D30,S\n',
     '750,0,3,"Connaghton, Mr. Michael",male,31,0,0,335097,7.75,,Q\n',
     '751,1,2,"Wells, Miss. Joan",female,4,1,1,29103,23,,S\n',
     '752,1,3,"Moor, Master. Meier",male,6,0,1,392096,12.475,E121,S\n',
     '753,0,3,"Vande Velde, Mr. Johannes Joseph",male,33,0,0,345780,9.5,,S\n',
     '754,0,3,"Jonkoff, Mr. Lalio",male,23,0,0,349204,7.8958,,S\n',
     '755,1,2,"Herman, Mrs. Samuel (Jane Laver)",female,48,1,2,220845,65,,S\n',
     '756,1,2,"Hamalainen, Master. Viljo",male,0.67,1,1,250649,14.5,,S\n',
     '757,0,3,"Carlsson, Mr. August Sigfrid",male,28,0,0,350042,7.7958,,S\n',
     '758,0,2,"Bailey, Mr. Percy Andrew",male,18,0,0,29108,11.5,,S\n',
     '759,0,3,"Theobald, Mr. Thomas Leonard",male,34,0,0,363294,8.05,,S\n',
     '760,1,1,"Rothes, the Countess. of (Lucy Noel Martha Dyer-Edwards)",female,33,0,0,110152,86.5,B77,S\n',
     '761,0,3,"Garfirth, Mr. John",male,,0,0,358585,14.5,,S\n',
     '762,0,3,"Nirva, Mr. Iisakki Antino Aijo",male,41,0,0,SOTON/O2 3101272,7.125,,S\n',
     '763,1,3,"Barah, Mr. Hanna Assi",male,20,0,0,2663,7.2292,,C\n',
     '764,1,1,"Carter, Mrs. William Ernest (Lucile Polk)",female,36,1,2,113760,120,B96 B98,S\n',
     '765,0,3,"Eklund, Mr. Hans Linus",male,16,0,0,347074,7.775,,S\n',
     '766,1,1,"Hogeboom, Mrs. John C (Anna Andrews)",female,51,1,0,13502,77.9583,D11,S\n',
     '767,0,1,"Brewe, Dr. Arthur Jackson",male,,0,0,112379,39.6,,C\n',
     '768,0,3,"Mangan, Miss. Mary",female,30.5,0,0,364850,7.75,,Q\n',
     '769,0,3,"Moran, Mr. Daniel J",male,,1,0,371110,24.15,,Q\n',
     '770,0,3,"Gronnestad, Mr. Daniel Danielsen",male,32,0,0,8471,8.3625,,S\n',
     '771,0,3,"Lievens, Mr. Rene Aime",male,24,0,0,345781,9.5,,S\n',
     '772,0,3,"Jensen, Mr. Niels Peder",male,48,0,0,350047,7.8542,,S\n',
     '773,0,2,"Mack, Mrs. (Mary)",female,57,0,0,S.O./P.P. 3,10.5,E77,S\n',
     '774,0,3,"Elias, Mr. Dibo",male,,0,0,2674,7.225,,C\n',
     '775,1,2,"Hocking, Mrs. Elizabeth (Eliza Needs)",female,54,1,3,29105,23,,S\n',
     '776,0,3,"Myhrman, Mr. Pehr Fabian Oliver Malkolm",male,18,0,0,347078,7.75,,S\n',
     '777,0,3,"Tobin, Mr. Roger",male,,0,0,383121,7.75,F38,Q\n',
     '778,1,3,"Emanuel, Miss. Virginia Ethel",female,5,0,0,364516,12.475,,S\n',
     '779,0,3,"Kilgannon, Mr. Thomas J",male,,0,0,36865,7.7375,,Q\n',
     '780,1,1,"Robert, Mrs. Edward Scott (Elisabeth Walton McMillan)",female,43,0,1,24160,211.3375,B3,S\n',
     '781,1,3,"Ayoub, Miss. Banoura",female,13,0,0,2687,7.2292,,C\n',
     '782,1,1,"Dick, Mrs. Albert Adrian (Vera Gillespie)",female,17,1,0,17474,57,B20,S\n',
     '783,0,1,"Long, Mr. Milton Clyde",male,29,0,0,113501,30,D6,S\n',
     '784,0,3,"Johnston, Mr. Andrew G",male,,1,2,W./C. 6607,23.45,,S\n',
     '785,0,3,"Ali, Mr. William",male,25,0,0,SOTON/O.Q. 3101312,7.05,,S\n',
     '786,0,3,"Harmer, Mr. Abraham (David Lishin)",male,25,0,0,374887,7.25,,S\n',
     '787,1,3,"Sjoblom, Miss. Anna Sofia",female,18,0,0,3101265,7.4958,,S\n',
     '788,0,3,"Rice, Master. George Hugh",male,8,4,1,382652,29.125,,Q\n',
     '789,1,3,"Dean, Master. Bertram Vere",male,1,1,2,C.A. 2315,20.575,,S\n',
     '790,0,1,"Guggenheim, Mr. Benjamin",male,46,0,0,PC 17593,79.2,B82 B84,C\n',
     '791,0,3,"Keane, Mr. Andrew ""Andy""",male,,0,0,12460,7.75,,Q\n',
     '792,0,2,"Gaskell, Mr. Alfred",male,16,0,0,239865,26,,S\n',
     '793,0,3,"Sage, Miss. Stella Anna",female,,8,2,CA. 2343,69.55,,S\n',
     '794,0,1,"Hoyt, Mr. William Fisher",male,,0,0,PC 17600,30.6958,,C\n',
     '795,0,3,"Dantcheff, Mr. Ristiu",male,25,0,0,349203,7.8958,,S\n',
     '796,0,2,"Otter, Mr. Richard",male,39,0,0,28213,13,,S\n',
     '797,1,1,"Leader, Dr. Alice (Farnham)",female,49,0,0,17465,25.9292,D17,S\n',
     '798,1,3,"Osman, Mrs. Mara",female,31,0,0,349244,8.6833,,S\n',
     '799,0,3,"Ibrahim Shawah, Mr. Yousseff",male,30,0,0,2685,7.2292,,C\n',
     '800,0,3,"Van Impe, Mrs. Jean Baptiste (Rosalie Paula Govaert)",female,30,1,1,345773,24.15,,S\n',
     '801,0,2,"Ponesell, Mr. Martin",male,34,0,0,250647,13,,S\n',
     '802,1,2,"Collyer, Mrs. Harvey (Charlotte Annie Tate)",female,31,1,1,C.A. 31921,26.25,,S\n',
     '803,1,1,"Carter, Master. William Thornton II",male,11,1,2,113760,120,B96 B98,S\n',
     '804,1,3,"Thomas, Master. Assad Alexander",male,0.42,0,1,2625,8.5167,,C\n',
     '805,1,3,"Hedman, Mr. Oskar Arvid",male,27,0,0,347089,6.975,,S\n',
     '806,0,3,"Johansson, Mr. Karl Johan",male,31,0,0,347063,7.775,,S\n',
     '807,0,1,"Andrews, Mr. Thomas Jr",male,39,0,0,112050,0,A36,S\n',
     '808,0,3,"Pettersson, Miss. Ellen Natalia",female,18,0,0,347087,7.775,,S\n',
     '809,0,2,"Meyer, Mr. August",male,39,0,0,248723,13,,S\n',
     '810,1,1,"Chambers, Mrs. Norman Campbell (Bertha Griggs)",female,33,1,0,113806,53.1,E8,S\n',
     '811,0,3,"Alexander, Mr. William",male,26,0,0,3474,7.8875,,S\n',
     '812,0,3,"Lester, Mr. James",male,39,0,0,A/4 48871,24.15,,S\n',
     '813,0,2,"Slemen, Mr. Richard James",male,35,0,0,28206,10.5,,S\n',
     '814,0,3,"Andersson, Miss. Ebba Iris Alfrida",female,6,4,2,347082,31.275,,S\n',
     '815,0,3,"Tomlin, Mr. Ernest Portage",male,30.5,0,0,364499,8.05,,S\n',
     '816,0,1,"Fry, Mr. Richard",male,,0,0,112058,0,B102,S\n',
     '817,0,3,"Heininen, Miss. Wendla Maria",female,23,0,0,STON/O2. 3101290,7.925,,S\n',
     '818,0,2,"Mallet, Mr. Albert",male,31,1,1,S.C./PARIS 2079,37.0042,,C\n',
     '819,0,3,"Holm, Mr. John Fredrik Alexander",male,43,0,0,C 7075,6.45,,S\n',
     '820,0,3,"Skoog, Master. Karl Thorsten",male,10,3,2,347088,27.9,,S\n',
     '821,1,1,"Hays, Mrs. Charles Melville (Clara Jennings Gregg)",female,52,1,1,12749,93.5,B69,S\n',
     '822,1,3,"Lulic, Mr. Nikola",male,27,0,0,315098,8.6625,,S\n',
     '823,0,1,"Reuchlin, Jonkheer. John George",male,38,0,0,19972,0,,S\n',
     '824,1,3,"Moor, Mrs. (Beila)",female,27,0,1,392096,12.475,E121,S\n',
     '825,0,3,"Panula, Master. Urho Abraham",male,2,4,1,3101295,39.6875,,S\n',
     '826,0,3,"Flynn, Mr. John",male,,0,0,368323,6.95,,Q\n',
     '827,0,3,"Lam, Mr. Len",male,,0,0,1601,56.4958,,S\n',
     '828,1,2,"Mallet, Master. Andre",male,1,0,2,S.C./PARIS 2079,37.0042,,C\n',
     '829,1,3,"McCormack, Mr. Thomas Joseph",male,,0,0,367228,7.75,,Q\n',
     '830,1,1,"Stone, Mrs. George Nelson (Martha Evelyn)",female,62,0,0,113572,80,B28,\n',
     '831,1,3,"Yasbeck, Mrs. Antoni (Selini Alexander)",female,15,1,0,2659,14.4542,,C\n',
     '832,1,2,"Richards, Master. George Sibley",male,0.83,1,1,29106,18.75,,S\n',
     '833,0,3,"Saad, Mr. Amin",male,,0,0,2671,7.2292,,C\n',
     '834,0,3,"Augustsson, Mr. Albert",male,23,0,0,347468,7.8542,,S\n',
     '835,0,3,"Allum, Mr. Owen George",male,18,0,0,2223,8.3,,S\n',
     '836,1,1,"Compton, Miss. Sara Rebecca",female,39,1,1,PC 17756,83.1583,E49,C\n',
     '837,0,3,"Pasic, Mr. Jakob",male,21,0,0,315097,8.6625,,S\n',
     '838,0,3,"Sirota, Mr. Maurice",male,,0,0,392092,8.05,,S\n',
     '839,1,3,"Chip, Mr. Chang",male,32,0,0,1601,56.4958,,S\n',
     '840,1,1,"Marechal, Mr. Pierre",male,,0,0,11774,29.7,C47,C\n',
     '841,0,3,"Alhomaki, Mr. Ilmari Rudolf",male,20,0,0,SOTON/O2 3101287,7.925,,S\n',
     '842,0,2,"Mudd, Mr. Thomas Charles",male,16,0,0,S.O./P.P. 3,10.5,,S\n',
     '843,1,1,"Serepeca, Miss. Augusta",female,30,0,0,113798,31,,C\n',
     '844,0,3,"Lemberopolous, Mr. Peter L",male,34.5,0,0,2683,6.4375,,C\n',
     '845,0,3,"Culumovic, Mr. Jeso",male,17,0,0,315090,8.6625,,S\n',
     '846,0,3,"Abbing, Mr. Anthony",male,42,0,0,C.A. 5547,7.55,,S\n',
     '847,0,3,"Sage, Mr. Douglas Bullen",male,,8,2,CA. 2343,69.55,,S\n',
     '848,0,3,"Markoff, Mr. Marin",male,35,0,0,349213,7.8958,,C\n',
     '849,0,2,"Harper, Rev. John",male,28,0,1,248727,33,,S\n',
     '850,1,1,"Goldenberg, Mrs. Samuel L (Edwiga Grabowska)",female,,1,0,17453,89.1042,C92,C\n',
     '851,0,3,"Andersson, Master. Sigvard Harald Elias",male,4,4,2,347082,31.275,,S\n',
     '852,0,3,"Svensson, Mr. Johan",male,74,0,0,347060,7.775,,S\n',
     '853,0,3,"Boulos, Miss. Nourelain",female,9,1,1,2678,15.2458,,C\n',
     '854,1,1,"Lines, Miss. Mary Conover",female,16,0,1,PC 17592,39.4,D28,S\n',
     '855,0,2,"Carter, Mrs. Ernest Courtenay (Lilian Hughes)",female,44,1,0,244252,26,,S\n',
     '856,1,3,"Aks, Mrs. Sam (Leah Rosen)",female,18,0,1,392091,9.35,,S\n',
     '857,1,1,"Wick, Mrs. George Dennick (Mary Hitchcock)",female,45,1,1,36928,164.8667,,S\n',
     '858,1,1,"Daly, Mr. Peter Denis ",male,51,0,0,113055,26.55,E17,S\n',
     '859,1,3,"Baclini, Mrs. Solomon (Latifa Qurban)",female,24,0,3,2666,19.2583,,C\n',
     '860,0,3,"Razi, Mr. Raihed",male,,0,0,2629,7.2292,,C\n',
     '861,0,3,"Hansen, Mr. Claus Peter",male,41,2,0,350026,14.1083,,S\n',
     '862,0,2,"Giles, Mr. Frederick Edward",male,21,1,0,28134,11.5,,S\n',
     '863,1,1,"Swift, Mrs. Frederick Joel (Margaret Welles Barron)",female,48,0,0,17466,25.9292,D17,S\n',
     '864,0,3,"Sage, Miss. Dorothy Edith ""Dolly""",female,,8,2,CA. 2343,69.55,,S\n',
     '865,0,2,"Gill, Mr. John William",male,24,0,0,233866,13,,S\n',
     '866,1,2,"Bystrom, Mrs. (Karolina)",female,42,0,0,236852,13,,S\n',
     '867,1,2,"Duran y More, Miss. Asuncion",female,27,1,0,SC/PARIS 2149,13.8583,,C\n',
     '868,0,1,"Roebling, Mr. Washington Augustus II",male,31,0,0,PC 17590,50.4958,A24,S\n',
     '869,0,3,"van Melkebeke, Mr. Philemon",male,,0,0,345777,9.5,,S\n',
     '870,1,3,"Johnson, Master. Harold Theodor",male,4,1,1,347742,11.1333,,S\n',
     '871,0,3,"Balkic, Mr. Cerin",male,26,0,0,349248,7.8958,,S\n',
     '872,1,1,"Beckwith, Mrs. Richard Leonard (Sallie Monypeny)",female,47,1,1,11751,52.5542,D35,S\n',
     '873,0,1,"Carlsson, Mr. Frans Olof",male,33,0,0,695,5,B51 B53 B55,S\n',
     '874,0,3,"Vander Cruyssen, Mr. Victor",male,47,0,0,345765,9,,S\n',
     '875,1,2,"Abelson, Mrs. Samuel (Hannah Wizosky)",female,28,1,0,P/PP 3381,24,,C\n',
     '876,1,3,"Najib, Miss. Adele Kiamie ""Jane""",female,15,0,0,2667,7.225,,C\n',
     '877,0,3,"Gustafsson, Mr. Alfred Ossian",male,20,0,0,7534,9.8458,,S\n',
     '878,0,3,"Petroff, Mr. Nedelio",male,19,0,0,349212,7.8958,,S\n',
     '879,0,3,"Laleff, Mr. Kristo",male,,0,0,349217,7.8958,,S\n',
     '880,1,1,"Potter, Mrs. Thomas Jr (Lily Alexenia Wilson)",female,56,0,1,11767,83.1583,C50,C\n',
     '881,1,2,"Shelley, Mrs. William (Imanita Parrish Hall)",female,25,0,1,230433,26,,S\n',
     '882,0,3,"Markun, Mr. Johann",male,33,0,0,349257,7.8958,,S\n',
     '883,0,3,"Dahlberg, Miss. Gerda Ulrika",female,22,0,0,7552,10.5167,,S\n',
     '884,0,2,"Banfield, Mr. Frederick James",male,28,0,0,C.A./SOTON 34068,10.5,,S\n',
     '885,0,3,"Sutehall, Mr. Henry Jr",male,25,0,0,SOTON/OQ 392076,7.05,,S\n',
     '886,0,3,"Rice, Mrs. William (Margaret Norton)",female,39,0,5,382652,29.125,,Q\n',
     '887,0,2,"Montvila, Rev. Juozas",male,27,0,0,211536,13,,S\n',
     '888,1,1,"Graham, Miss. Margaret Edith",female,19,0,0,112053,30,B42,S\n',
     '889,0,3,"Johnston, Miss. Catherine Helen ""Carrie""",female,,1,2,W./C. 6607,23.45,,S\n',
     '890,1,1,"Behr, Mr. Karl Howell",male,26,0,0,111369,30,C148,C\n',
     '891,0,3,"Dooley, Mr. Patrick",male,32,0,0,370376,7.75,,Q\n']




```python
linhas[0]
```




    'PassengerId,Survived,Pclass,Name,Sex,Age,SibSp,Parch,Ticket,Fare,Cabin,Embarked\n'




```python
linhas[1]
```




    '1,0,3,"Braund, Mr. Owen Harris",male,22,1,0,A/5 21171,7.25,,S\n'




```python
linhas[3]
```




    '3,1,3,"Heikkinen, Miss. Laina",female,26,0,0,STON/O2. 3101282,7.925,,S\n'




```python
linhas[4]
```




    '4,1,1,"Futrelle, Mrs. Jacques Heath (Lily May Peel)",female,35,1,0,113803,53.1,C123,S\n'




```python
titanic_csv.close()
```


```python
linhas[0].split(',')
```




    ['PassengerId',
     'Survived',
     'Pclass',
     'Name',
     'Sex',
     'Age',
     'SibSp',
     'Parch',
     'Ticket',
     'Fare',
     'Cabin',
     'Embarked\n']




```python
colunas = linhas[0].split(',') #vira uma lista de str
```


```python
colunas
```




    ['PassengerId',
     'Survived',
     'Pclass',
     'Name',
     'Sex',
     'Age',
     'SibSp',
     'Parch',
     'Ticket',
     'Fare',
     'Cabin',
     'Embarked\n']




```python
colunas[0]
```




    'PassengerId'




```python
colunas[1]
```




    'Survived'




```python
colunas[2]
```




    'Pclass'




```python
#cada coluna será um chave e os valores uma lista do dicionario
dados = linhas[1].split(',')
```


```python
print(colunas)
print(dados)
```

    ['PassengerId', 'Survived', 'Pclass', 'Name', 'Sex', 'Age', 'SibSp', 'Parch', 'Ticket', 'Fare', 'Cabin', 'Embarked\n']
    ['1', '0', '3', '"Braund', ' Mr. Owen Harris"', 'male', '22', '1', '0', 'A/5 21171', '7.25', '', 'S\n']
    


```python
i = 4
print(colunas[i])
print(dados[i])
```

    Sex
     Mr. Owen Harris"
    


```python
#deu ruim
print(len(colunas), len(dados))
```

    12 13
    

### Expressão Regular, vamos tirar a virgula e inverter o nome.


```python
def tratar_nome(linha):
    import re 
    match = re.compile(r'"(.*)(,)(\s.*)"')
    return match.sub(r'"\3 \1"', linha)   
```


```python
tratar_nome(linhas[1])
```




    '1,0,3," Mr. Owen Harris Braund",male,22,1,0,A/5 21171,7.25,,S\n'




```python
linha1_tratada = tratar_nome(linhas[1])
linha1_separada = linha1_tratada.split(",")
print(colunas)
print(linha1_tratada)
print(linha1_separada)
```

    ['PassengerId', 'Survived', 'Pclass', 'Name', 'Sex', 'Age', 'SibSp', 'Parch', 'Ticket', 'Fare', 'Cabin', 'Embarked\n']
    1,0,3," Mr. Owen Harris Braund",male,22,1,0,A/5 21171,7.25,,S
    
    ['1', '0', '3', '" Mr. Owen Harris Braund"', 'male', '22', '1', '0', 'A/5 21171', '7.25', '', 'S\n']
    


```python
titanic_dados = {}

for coluna in colunas:
    titanic_dados[coluna] = []
titanic_dados
```




    {'PassengerId': [],
     'Survived': [],
     'Pclass': [],
     'Name': [],
     'Sex': [],
     'Age': [],
     'SibSp': [],
     'Parch': [],
     'Ticket': [],
     'Fare': [],
     'Cabin': [],
     'Embarked\n': []}




```python
linhas[6]
```




    '6,0,3,"Moran, Mr. James",male,,0,0,330877,8.4583,,Q\n'




```python
#Tratando todas as linhas do data set

for dado in linhas[1:]:
    dado_tratado = tratar_nome(dado)
    print(dado_tratado)
```

    1,0,3," Mr. Owen Harris Braund",male,22,1,0,A/5 21171,7.25,,S
    
    2,1,1," Mrs. John Bradley (Florence Briggs Thayer) Cumings",female,38,1,0,PC 17599,71.2833,C85,C
    
    3,1,3," Miss. Laina Heikkinen",female,26,0,0,STON/O2. 3101282,7.925,,S
    
    4,1,1," Mrs. Jacques Heath (Lily May Peel) Futrelle",female,35,1,0,113803,53.1,C123,S
    
    5,0,3," Mr. William Henry Allen",male,35,0,0,373450,8.05,,S
    
    6,0,3," Mr. James Moran",male,,0,0,330877,8.4583,,Q
    
    7,0,1," Mr. Timothy J McCarthy",male,54,0,0,17463,51.8625,E46,S
    
    8,0,3," Master. Gosta Leonard Palsson",male,2,3,1,349909,21.075,,S
    
    9,1,3," Mrs. Oscar W (Elisabeth Vilhelmina Berg) Johnson",female,27,0,2,347742,11.1333,,S
    
    10,1,2," Mrs. Nicholas (Adele Achem) Nasser",female,14,1,0,237736,30.0708,,C
    
    11,1,3," Miss. Marguerite Rut Sandstrom",female,4,1,1,PP 9549,16.7,G6,S
    
    12,1,1," Miss. Elizabeth Bonnell",female,58,0,0,113783,26.55,C103,S
    
    13,0,3," Mr. William Henry Saundercock",male,20,0,0,A/5. 2151,8.05,,S
    
    14,0,3," Mr. Anders Johan Andersson",male,39,1,5,347082,31.275,,S
    
    15,0,3," Miss. Hulda Amanda Adolfina Vestrom",female,14,0,0,350406,7.8542,,S
    
    16,1,2," Mrs. (Mary D Kingcome)  Hewlett",female,55,0,0,248706,16,,S
    
    17,0,3," Master. Eugene Rice",male,2,4,1,382652,29.125,,Q
    
    18,1,2," Mr. Charles Eugene Williams",male,,0,0,244373,13,,S
    
    19,0,3," Mrs. Julius (Emelia Maria Vandemoortele) Vander Planke",female,31,1,0,345763,18,,S
    
    20,1,3," Mrs. Fatima Masselmani",female,,0,0,2649,7.225,,C
    
    21,0,2," Mr. Joseph J Fynney",male,35,0,0,239865,26,,S
    
    22,1,2," Mr. Lawrence Beesley",male,34,0,0,248698,13,D56,S
    
    23,1,3," Miss. Anna ""Annie"" McGowan",female,15,0,0,330923,8.0292,,Q
    
    24,1,1," Mr. William Thompson Sloper",male,28,0,0,113788,35.5,A6,S
    
    25,0,3," Miss. Torborg Danira Palsson",female,8,3,1,349909,21.075,,S
    
    26,1,3," Mrs. Carl Oscar (Selma Augusta Emilia Johansson) Asplund",female,38,1,5,347077,31.3875,,S
    
    27,0,3," Mr. Farred Chehab Emir",male,,0,0,2631,7.225,,C
    
    28,0,1," Mr. Charles Alexander Fortune",male,19,3,2,19950,263,C23 C25 C27,S
    
    29,1,3," Miss. Ellen ""Nellie"" O'Dwyer",female,,0,0,330959,7.8792,,Q
    
    30,0,3," Mr. Lalio Todoroff",male,,0,0,349216,7.8958,,S
    
    31,0,1," Don. Manuel E Uruchurtu",male,40,0,0,PC 17601,27.7208,,C
    
    32,1,1," Mrs. William Augustus (Marie Eugenie) Spencer",female,,1,0,PC 17569,146.5208,B78,C
    
    33,1,3," Miss. Mary Agatha Glynn",female,,0,0,335677,7.75,,Q
    
    34,0,2," Mr. Edward H Wheadon",male,66,0,0,C.A. 24579,10.5,,S
    
    35,0,1," Mr. Edgar Joseph Meyer",male,28,1,0,PC 17604,82.1708,,C
    
    36,0,1," Mr. Alexander Oskar Holverson",male,42,1,0,113789,52,,S
    
    37,1,3," Mr. Hanna Mamee",male,,0,0,2677,7.2292,,C
    
    38,0,3," Mr. Ernest Charles Cann",male,21,0,0,A./5. 2152,8.05,,S
    
    39,0,3," Miss. Augusta Maria Vander Planke",female,18,2,0,345764,18,,S
    
    40,1,3," Miss. Jamila Nicola-Yarred",female,14,1,0,2651,11.2417,,C
    
    41,0,3," Mrs. Johan (Johanna Persdotter Larsson) Ahlin",female,40,1,0,7546,9.475,,S
    
    42,0,2," Mrs. William John Robert (Dorothy Ann Wonnacott) Turpin",female,27,1,0,11668,21,,S
    
    43,0,3," Mr. Theodor Kraeff",male,,0,0,349253,7.8958,,C
    
    44,1,2," Miss. Simonne Marie Anne Andree Laroche",female,3,1,2,SC/Paris 2123,41.5792,,C
    
    45,1,3," Miss. Margaret Delia Devaney",female,19,0,0,330958,7.8792,,Q
    
    46,0,3," Mr. William John Rogers",male,,0,0,S.C./A.4. 23567,8.05,,S
    
    47,0,3," Mr. Denis Lennon",male,,1,0,370371,15.5,,Q
    
    48,1,3," Miss. Bridget O'Driscoll",female,,0,0,14311,7.75,,Q
    
    49,0,3," Mr. Youssef Samaan",male,,2,0,2662,21.6792,,C
    
    50,0,3," Mrs. Josef (Josefine Franchi) Arnold-Franchi",female,18,1,0,349237,17.8,,S
    
    51,0,3," Master. Juha Niilo Panula",male,7,4,1,3101295,39.6875,,S
    
    52,0,3," Mr. Richard Cater Nosworthy",male,21,0,0,A/4. 39886,7.8,,S
    
    53,1,1," Mrs. Henry Sleeper (Myna Haxtun) Harper",female,49,1,0,PC 17572,76.7292,D33,C
    
    54,1,2," Mrs. Lizzie (Elizabeth Anne Wilkinson) Faunthorpe",female,29,1,0,2926,26,,S
    
    55,0,1," Mr. Engelhart Cornelius Ostby",male,65,0,1,113509,61.9792,B30,C
    
    56,1,1," Mr. Hugh Woolner",male,,0,0,19947,35.5,C52,S
    
    57,1,2," Miss. Emily Rugg",female,21,0,0,C.A. 31026,10.5,,S
    
    58,0,3," Mr. Mansouer Novel",male,28.5,0,0,2697,7.2292,,C
    
    59,1,2," Miss. Constance Mirium West",female,5,1,2,C.A. 34651,27.75,,S
    
    60,0,3," Master. William Frederick Goodwin",male,11,5,2,CA 2144,46.9,,S
    
    61,0,3," Mr. Orsen Sirayanian",male,22,0,0,2669,7.2292,,C
    
    62,1,1," Miss. Amelie Icard",female,38,0,0,113572,80,B28,
    
    63,0,1," Mr. Henry Birkhardt Harris",male,45,1,0,36973,83.475,C83,S
    
    64,0,3," Master. Harald Skoog",male,4,3,2,347088,27.9,,S
    
    65,0,1," Mr. Albert A Stewart",male,,0,0,PC 17605,27.7208,,C
    
    66,1,3," Master. Gerios Moubarek",male,,1,1,2661,15.2458,,C
    
    67,1,2," Mrs. (Elizabeth Ramell) Nye",female,29,0,0,C.A. 29395,10.5,F33,S
    
    68,0,3," Mr. Ernest James Crease",male,19,0,0,S.P. 3464,8.1583,,S
    
    69,1,3," Miss. Erna Alexandra Andersson",female,17,4,2,3101281,7.925,,S
    
    70,0,3," Mr. Vincenz Kink",male,26,2,0,315151,8.6625,,S
    
    71,0,2," Mr. Stephen Curnow Jenkin",male,32,0,0,C.A. 33111,10.5,,S
    
    72,0,3," Miss. Lillian Amy Goodwin",female,16,5,2,CA 2144,46.9,,S
    
    73,0,2," Mr. Ambrose Jr Hood",male,21,0,0,S.O.C. 14879,73.5,,S
    
    74,0,3," Mr. Apostolos Chronopoulos",male,26,1,0,2680,14.4542,,C
    
    75,1,3," Mr. Lee Bing",male,32,0,0,1601,56.4958,,S
    
    76,0,3," Mr. Sigurd Hansen Moen",male,25,0,0,348123,7.65,F G73,S
    
    77,0,3," Mr. Ivan Staneff",male,,0,0,349208,7.8958,,S
    
    78,0,3," Mr. Rahamin Haim Moutal",male,,0,0,374746,8.05,,S
    
    79,1,2," Master. Alden Gates Caldwell",male,0.83,0,2,248738,29,,S
    
    80,1,3," Miss. Elizabeth Dowdell",female,30,0,0,364516,12.475,,S
    
    81,0,3," Mr. Achille Waelens",male,22,0,0,345767,9,,S
    
    82,1,3," Mr. Jan Baptist Sheerlinck",male,29,0,0,345779,9.5,,S
    
    83,1,3," Miss. Brigdet Delia McDermott",female,,0,0,330932,7.7875,,Q
    
    84,0,1," Mr. Francisco M Carrau",male,28,0,0,113059,47.1,,S
    
    85,1,2," Miss. Bertha Ilett",female,17,0,0,SO/C 14885,10.5,,S
    
    86,1,3," Mrs. Karl Alfred (Maria Mathilda Gustafsson) Backstrom",female,33,3,0,3101278,15.85,,S
    
    87,0,3," Mr. William Neal Ford",male,16,1,3,W./C. 6608,34.375,,S
    
    88,0,3," Mr. Selman Francis Slocovski",male,,0,0,SOTON/OQ 392086,8.05,,S
    
    89,1,1," Miss. Mabel Helen Fortune",female,23,3,2,19950,263,C23 C25 C27,S
    
    90,0,3," Mr. Francesco Celotti",male,24,0,0,343275,8.05,,S
    
    91,0,3," Mr. Emil Christmann",male,29,0,0,343276,8.05,,S
    
    92,0,3," Mr. Paul Edvin Andreasson",male,20,0,0,347466,7.8542,,S
    
    93,0,1," Mr. Herbert Fuller Chaffee",male,46,1,0,W.E.P. 5734,61.175,E31,S
    
    94,0,3," Mr. Bertram Frank Dean",male,26,1,2,C.A. 2315,20.575,,S
    
    95,0,3," Mr. Daniel Coxon",male,59,0,0,364500,7.25,,S
    
    96,0,3," Mr. Charles Joseph Shorney",male,,0,0,374910,8.05,,S
    
    97,0,1," Mr. George B Goldschmidt",male,71,0,0,PC 17754,34.6542,A5,C
    
    98,1,1," Mr. William Bertram Greenfield",male,23,0,1,PC 17759,63.3583,D10 D12,C
    
    99,1,2," Mrs. John T (Ada Julia Bone) Doling",female,34,0,1,231919,23,,S
    
    100,0,2," Mr. Sinai Kantor",male,34,1,0,244367,26,,S
    
    101,0,3," Miss. Matilda Petranec",female,28,0,0,349245,7.8958,,S
    
    102,0,3," Mr. Pastcho (""Pentcho"") Petroff",male,,0,0,349215,7.8958,,S
    
    103,0,1," Mr. Richard Frasar White",male,21,0,1,35281,77.2875,D26,S
    
    104,0,3," Mr. Gustaf Joel Johansson",male,33,0,0,7540,8.6542,,S
    
    105,0,3," Mr. Anders Vilhelm Gustafsson",male,37,2,0,3101276,7.925,,S
    
    106,0,3," Mr. Stoytcho Mionoff",male,28,0,0,349207,7.8958,,S
    
    107,1,3," Miss. Anna Kristine Salkjelsvik",female,21,0,0,343120,7.65,,S
    
    108,1,3," Mr. Albert Johan Moss",male,,0,0,312991,7.775,,S
    
    109,0,3," Mr. Tido Rekic",male,38,0,0,349249,7.8958,,S
    
    110,1,3," Miss. Bertha Moran",female,,1,0,371110,24.15,,Q
    
    111,0,1," Mr. Walter Chamberlain Porter",male,47,0,0,110465,52,C110,S
    
    112,0,3," Miss. Hileni Zabour",female,14.5,1,0,2665,14.4542,,C
    
    113,0,3," Mr. David John Barton",male,22,0,0,324669,8.05,,S
    
    114,0,3," Miss. Katriina Jussila",female,20,1,0,4136,9.825,,S
    
    115,0,3," Miss. Malake Attalah",female,17,0,0,2627,14.4583,,C
    
    116,0,3," Mr. Edvard Pekoniemi",male,21,0,0,STON/O 2. 3101294,7.925,,S
    
    117,0,3," Mr. Patrick Connors",male,70.5,0,0,370369,7.75,,Q
    
    118,0,2," Mr. William John Robert Turpin",male,29,1,0,11668,21,,S
    
    119,0,1," Mr. Quigg Edmond Baxter",male,24,0,1,PC 17558,247.5208,B58 B60,C
    
    120,0,3," Miss. Ellis Anna Maria Andersson",female,2,4,2,347082,31.275,,S
    
    121,0,2," Mr. Stanley George Hickman",male,21,2,0,S.O.C. 14879,73.5,,S
    
    122,0,3," Mr. Leonard Charles Moore",male,,0,0,A4. 54510,8.05,,S
    
    123,0,2," Mr. Nicholas Nasser",male,32.5,1,0,237736,30.0708,,C
    
    124,1,2," Miss. Susan Webber",female,32.5,0,0,27267,13,E101,S
    
    125,0,1," Mr. Percival Wayland White",male,54,0,1,35281,77.2875,D26,S
    
    126,1,3," Master. Elias Nicola-Yarred",male,12,1,0,2651,11.2417,,C
    
    127,0,3," Mr. Martin McMahon",male,,0,0,370372,7.75,,Q
    
    128,1,3," Mr. Fridtjof Arne Madsen",male,24,0,0,C 17369,7.1417,,S
    
    129,1,3," Miss. Anna Peter",female,,1,1,2668,22.3583,F E69,C
    
    130,0,3," Mr. Johan Ekstrom",male,45,0,0,347061,6.975,,S
    
    131,0,3," Mr. Jozef Drazenoic",male,33,0,0,349241,7.8958,,C
    
    132,0,3," Mr. Domingos Fernandeo Coelho",male,20,0,0,SOTON/O.Q. 3101307,7.05,,S
    
    133,0,3," Mrs. Alexander A (Grace Charity Laury) Robins",female,47,1,0,A/5. 3337,14.5,,S
    
    134,1,2," Mrs. Leopold (Mathilde Francoise Pede) Weisz",female,29,1,0,228414,26,,S
    
    135,0,2," Mr. Samuel James Hayden Sobey",male,25,0,0,C.A. 29178,13,,S
    
    136,0,2," Mr. Emile Richard",male,23,0,0,SC/PARIS 2133,15.0458,,C
    
    137,1,1," Miss. Helen Monypeny Newsom",female,19,0,2,11752,26.2833,D47,S
    
    138,0,1," Mr. Jacques Heath Futrelle",male,37,1,0,113803,53.1,C123,S
    
    139,0,3," Mr. Olaf Elon Osen",male,16,0,0,7534,9.2167,,S
    
    140,0,1," Mr. Victor Giglio",male,24,0,0,PC 17593,79.2,B86,C
    
    141,0,3," Mrs. Joseph (Sultana) Boulos",female,,0,2,2678,15.2458,,C
    
    142,1,3," Miss. Anna Sofia Nysten",female,22,0,0,347081,7.75,,S
    
    143,1,3," Mrs. Pekka Pietari (Elin Matilda Dolck) Hakkarainen",female,24,1,0,STON/O2. 3101279,15.85,,S
    
    144,0,3," Mr. Jeremiah Burke",male,19,0,0,365222,6.75,,Q
    
    145,0,2," Mr. Edgardo Samuel Andrew",male,18,0,0,231945,11.5,,S
    
    146,0,2," Mr. Joseph Charles Nicholls",male,19,1,1,C.A. 33112,36.75,,S
    
    147,1,3," Mr. August Edvard (""Wennerstrom"") Andersson",male,27,0,0,350043,7.7958,,S
    
    148,0,3," Miss. Robina Maggie ""Ruby"" Ford",female,9,2,2,W./C. 6608,34.375,,S
    
    149,0,2," Mr. Michel (""Louis M Hoffman"") Navratil",male,36.5,0,2,230080,26,F2,S
    
    150,0,2," Rev. Thomas Roussel Davids Byles",male,42,0,0,244310,13,,S
    
    151,0,2," Rev. Robert James Bateman",male,51,0,0,S.O.P. 1166,12.525,,S
    
    152,1,1," Mrs. Thomas (Edith Wearne) Pears",female,22,1,0,113776,66.6,C2,S
    
    153,0,3," Mr. Alfonzo Meo",male,55.5,0,0,A.5. 11206,8.05,,S
    
    154,0,3," Mr. Austin Blyler van Billiard",male,40.5,0,2,A/5. 851,14.5,,S
    
    155,0,3," Mr. Ole Martin Olsen",male,,0,0,Fa 265302,7.3125,,S
    
    156,0,1," Mr. Charles Duane Williams",male,51,0,1,PC 17597,61.3792,,C
    
    157,1,3," Miss. Katherine ""Katie"" Gilnagh",female,16,0,0,35851,7.7333,,Q
    
    158,0,3," Mr. Harry Corn",male,30,0,0,SOTON/OQ 392090,8.05,,S
    
    159,0,3," Mr. Mile Smiljanic",male,,0,0,315037,8.6625,,S
    
    160,0,3," Master. Thomas Henry Sage",male,,8,2,CA. 2343,69.55,,S
    
    161,0,3," Mr. John Hatfield Cribb",male,44,0,1,371362,16.1,,S
    
    162,1,2," Mrs. James (Elizabeth ""Bessie"" Inglis Milne) Watt",female,40,0,0,C.A. 33595,15.75,,S
    
    163,0,3," Mr. John Viktor Bengtsson",male,26,0,0,347068,7.775,,S
    
    164,0,3," Mr. Jovo Calic",male,17,0,0,315093,8.6625,,S
    
    165,0,3," Master. Eino Viljami Panula",male,1,4,1,3101295,39.6875,,S
    
    166,1,3," Master. Frank John William ""Frankie"" Goldsmith",male,9,0,2,363291,20.525,,S
    
    167,1,1," Mrs. (Edith Martha Bowerman) Chibnall",female,,0,1,113505,55,E33,S
    
    168,0,3," Mrs. William (Anna Bernhardina Karlsson) Skoog",female,45,1,4,347088,27.9,,S
    
    169,0,1," Mr. John D Baumann",male,,0,0,PC 17318,25.925,,S
    
    170,0,3," Mr. Lee Ling",male,28,0,0,1601,56.4958,,S
    
    171,0,1," Mr. Wyckoff Van der hoef",male,61,0,0,111240,33.5,B19,S
    
    172,0,3," Master. Arthur Rice",male,4,4,1,382652,29.125,,Q
    
    173,1,3," Miss. Eleanor Ileen Johnson",female,1,1,1,347742,11.1333,,S
    
    174,0,3," Mr. Antti Wilhelm Sivola",male,21,0,0,STON/O 2. 3101280,7.925,,S
    
    175,0,1," Mr. James Clinch Smith",male,56,0,0,17764,30.6958,A7,C
    
    176,0,3," Mr. Klas Albin Klasen",male,18,1,1,350404,7.8542,,S
    
    177,0,3," Master. Henry Forbes Lefebre",male,,3,1,4133,25.4667,,S
    
    178,0,1," Miss. Ann Elizabeth Isham",female,50,0,0,PC 17595,28.7125,C49,C
    
    179,0,2," Mr. Reginald Hale",male,30,0,0,250653,13,,S
    
    180,0,3," Mr. Lionel Leonard",male,36,0,0,LINE,0,,S
    
    181,0,3," Miss. Constance Gladys Sage",female,,8,2,CA. 2343,69.55,,S
    
    182,0,2," Mr. Rene Pernot",male,,0,0,SC/PARIS 2131,15.05,,C
    
    183,0,3," Master. Clarence Gustaf Hugo Asplund",male,9,4,2,347077,31.3875,,S
    
    184,1,2," Master. Richard F Becker",male,1,2,1,230136,39,F4,S
    
    185,1,3," Miss. Luise Gretchen Kink-Heilmann",female,4,0,2,315153,22.025,,S
    
    186,0,1," Mr. Hugh Roscoe Rood",male,,0,0,113767,50,A32,S
    
    187,1,3," Mrs. Thomas (Johanna ""Hannah"" Godfrey) O'Brien",female,,1,0,370365,15.5,,Q
    
    188,1,1," Mr. Charles Hallace (""Mr C Rolmane"") Romaine",male,45,0,0,111428,26.55,,S
    
    189,0,3," Mr. John Bourke",male,40,1,1,364849,15.5,,Q
    
    190,0,3," Mr. Stjepan Turcin",male,36,0,0,349247,7.8958,,S
    
    191,1,2," Mrs. (Rosa) Pinsky",female,32,0,0,234604,13,,S
    
    192,0,2," Mr. William Carbines",male,19,0,0,28424,13,,S
    
    193,1,3," Miss. Carla Christine Nielsine Andersen-Jensen",female,19,1,0,350046,7.8542,,S
    
    194,1,2," Master. Michel M Navratil",male,3,1,1,230080,26,F2,S
    
    195,1,1," Mrs. James Joseph (Margaret Tobin) Brown",female,44,0,0,PC 17610,27.7208,B4,C
    
    196,1,1," Miss. Elise Lurette",female,58,0,0,PC 17569,146.5208,B80,C
    
    197,0,3," Mr. Robert Mernagh",male,,0,0,368703,7.75,,Q
    
    198,0,3," Mr. Karl Siegwart Andreas Olsen",male,42,0,1,4579,8.4042,,S
    
    199,1,3," Miss. Margaret ""Maggie"" Madigan",female,,0,0,370370,7.75,,Q
    
    200,0,2," Miss. Henriette (""Mrs Harbeck"") Yrois",female,24,0,0,248747,13,,S
    
    201,0,3," Mr. Nestor Cyriel Vande Walle",male,28,0,0,345770,9.5,,S
    
    202,0,3," Mr. Frederick Sage",male,,8,2,CA. 2343,69.55,,S
    
    203,0,3," Mr. Jakob Alfred Johanson",male,34,0,0,3101264,6.4958,,S
    
    204,0,3," Mr. Gerious Youseff",male,45.5,0,0,2628,7.225,,C
    
    205,1,3," Mr. Gurshon ""Gus"" Cohen",male,18,0,0,A/5 3540,8.05,,S
    
    206,0,3," Miss. Telma Matilda Strom",female,2,0,1,347054,10.4625,G6,S
    
    207,0,3," Mr. Karl Alfred Backstrom",male,32,1,0,3101278,15.85,,S
    
    208,1,3," Mr. Nassef Cassem Albimona",male,26,0,0,2699,18.7875,,C
    
    209,1,3," Miss. Helen ""Ellen"" Carr",female,16,0,0,367231,7.75,,Q
    
    210,1,1," Mr. Henry Blank",male,40,0,0,112277,31,A31,C
    
    211,0,3," Mr. Ahmed Ali",male,24,0,0,SOTON/O.Q. 3101311,7.05,,S
    
    212,1,2," Miss. Clear Annie Cameron",female,35,0,0,F.C.C. 13528,21,,S
    
    213,0,3," Mr. John Henry Perkin",male,22,0,0,A/5 21174,7.25,,S
    
    214,0,2," Mr. Hans Kristensen Givard",male,30,0,0,250646,13,,S
    
    215,0,3," Mr. Philip Kiernan",male,,1,0,367229,7.75,,Q
    
    216,1,1," Miss. Madeleine Newell",female,31,1,0,35273,113.275,D36,C
    
    217,1,3," Miss. Eliina Honkanen",female,27,0,0,STON/O2. 3101283,7.925,,S
    
    218,0,2," Mr. Sidney Samuel Jacobsohn",male,42,1,0,243847,27,,S
    
    219,1,1," Miss. Albina Bazzani",female,32,0,0,11813,76.2917,D15,C
    
    220,0,2," Mr. Walter Harris",male,30,0,0,W/C 14208,10.5,,S
    
    221,1,3," Mr. Victor Francis Sunderland",male,16,0,0,SOTON/OQ 392089,8.05,,S
    
    222,0,2," Mr. James H Bracken",male,27,0,0,220367,13,,S
    
    223,0,3," Mr. George Henry Green",male,51,0,0,21440,8.05,,S
    
    224,0,3," Mr. Christo Nenkoff",male,,0,0,349234,7.8958,,S
    
    225,1,1," Mr. Frederick Maxfield Hoyt",male,38,1,0,19943,90,C93,S
    
    226,0,3," Mr. Karl Ivar Sven Berglund",male,22,0,0,PP 4348,9.35,,S
    
    227,1,2," Mr. William John Mellors",male,19,0,0,SW/PP 751,10.5,,S
    
    228,0,3," Mr. John Hall (""Henry"") Lovell",male,20.5,0,0,A/5 21173,7.25,,S
    
    229,0,2," Mr. Arne Jonas Fahlstrom",male,18,0,0,236171,13,,S
    
    230,0,3," Miss. Mathilde Lefebre",female,,3,1,4133,25.4667,,S
    
    231,1,1," Mrs. Henry Birkhardt (Irene Wallach) Harris",female,35,1,0,36973,83.475,C83,S
    
    232,0,3," Mr. Bengt Edvin Larsson",male,29,0,0,347067,7.775,,S
    
    233,0,2," Mr. Ernst Adolf Sjostedt",male,59,0,0,237442,13.5,,S
    
    234,1,3," Miss. Lillian Gertrud Asplund",female,5,4,2,347077,31.3875,,S
    
    235,0,2," Mr. Robert William Norman Leyson",male,24,0,0,C.A. 29566,10.5,,S
    
    236,0,3," Miss. Alice Phoebe Harknett",female,,0,0,W./C. 6609,7.55,,S
    
    237,0,2," Mr. Stephen Hold",male,44,1,0,26707,26,,S
    
    238,1,2," Miss. Marjorie ""Lottie"" Collyer",female,8,0,2,C.A. 31921,26.25,,S
    
    239,0,2," Mr. Frederick William Pengelly",male,19,0,0,28665,10.5,,S
    
    240,0,2," Mr. George Henry Hunt",male,33,0,0,SCO/W 1585,12.275,,S
    
    241,0,3," Miss. Thamine Zabour",female,,1,0,2665,14.4542,,C
    
    242,1,3," Miss. Katherine ""Kate"" Murphy",female,,1,0,367230,15.5,,Q
    
    243,0,2," Mr. Reginald Charles Coleridge",male,29,0,0,W./C. 14263,10.5,,S
    
    244,0,3," Mr. Matti Alexanteri Maenpaa",male,22,0,0,STON/O 2. 3101275,7.125,,S
    
    245,0,3," Mr. Sleiman Attalah",male,30,0,0,2694,7.225,,C
    
    246,0,1," Dr. William Edward Minahan",male,44,2,0,19928,90,C78,Q
    
    247,0,3," Miss. Agda Thorilda Viktoria Lindahl",female,25,0,0,347071,7.775,,S
    
    248,1,2," Mrs. William (Anna) Hamalainen",female,24,0,2,250649,14.5,,S
    
    249,1,1," Mr. Richard Leonard Beckwith",male,37,1,1,11751,52.5542,D35,S
    
    250,0,2," Rev. Ernest Courtenay Carter",male,54,1,0,244252,26,,S
    
    251,0,3," Mr. James George Reed",male,,0,0,362316,7.25,,S
    
    252,0,3," Mrs. Wilhelm (Elna Matilda Persson) Strom",female,29,1,1,347054,10.4625,G6,S
    
    253,0,1," Mr. William Thomas Stead",male,62,0,0,113514,26.55,C87,S
    
    254,0,3," Mr. William Arthur Lobb",male,30,1,0,A/5. 3336,16.1,,S
    
    255,0,3," Mrs. Viktor (Helena Wilhelmina) Rosblom",female,41,0,2,370129,20.2125,,S
    
    256,1,3," Mrs. Darwis (Hanne Youssef Razi) Touma",female,29,0,2,2650,15.2458,,C
    
    257,1,1," Mrs. Gertrude Maybelle Thorne",female,,0,0,PC 17585,79.2,,C
    
    258,1,1," Miss. Gladys Cherry",female,30,0,0,110152,86.5,B77,S
    
    259,1,1," Miss. Anna Ward",female,35,0,0,PC 17755,512.3292,,C
    
    260,1,2," Mrs. (Lutie Davis) Parrish",female,50,0,1,230433,26,,S
    
    261,0,3," Mr. Thomas Smith",male,,0,0,384461,7.75,,Q
    
    262,1,3," Master. Edvin Rojj Felix Asplund",male,3,4,2,347077,31.3875,,S
    
    263,0,1," Mr. Emil Taussig",male,52,1,1,110413,79.65,E67,S
    
    264,0,1," Mr. William Harrison",male,40,0,0,112059,0,B94,S
    
    265,0,3," Miss. Delia Henry",female,,0,0,382649,7.75,,Q
    
    266,0,2," Mr. David Reeves",male,36,0,0,C.A. 17248,10.5,,S
    
    267,0,3," Mr. Ernesti Arvid Panula",male,16,4,1,3101295,39.6875,,S
    
    268,1,3," Mr. Ernst Ulrik Persson",male,25,1,0,347083,7.775,,S
    
    269,1,1," Mrs. William Thompson (Edith Junkins) Graham",female,58,0,1,PC 17582,153.4625,C125,S
    
    270,1,1," Miss. Amelia Bissette",female,35,0,0,PC 17760,135.6333,C99,S
    
    271,0,1," Mr. Alexander Cairns",male,,0,0,113798,31,,S
    
    272,1,3," Mr. William Henry Tornquist",male,25,0,0,LINE,0,,S
    
    273,1,2," Mrs. (Elizabeth Anne Maidment) Mellinger",female,41,0,1,250644,19.5,,S
    
    274,0,1," Mr. Charles H Natsch",male,37,0,1,PC 17596,29.7,C118,C
    
    275,1,3," Miss. Hanora ""Nora"" Healy",female,,0,0,370375,7.75,,Q
    
    276,1,1," Miss. Kornelia Theodosia Andrews",female,63,1,0,13502,77.9583,D7,S
    
    277,0,3," Miss. Augusta Charlotta Lindblom",female,45,0,0,347073,7.75,,S
    
    278,0,2," Mr. Francis ""Frank"" Parkes",male,,0,0,239853,0,,S
    
    279,0,3," Master. Eric Rice",male,7,4,1,382652,29.125,,Q
    
    280,1,3," Mrs. Stanton (Rosa Hunt) Abbott",female,35,1,1,C.A. 2673,20.25,,S
    
    281,0,3," Mr. Frank Duane",male,65,0,0,336439,7.75,,Q
    
    282,0,3," Mr. Nils Johan Goransson Olsson",male,28,0,0,347464,7.8542,,S
    
    283,0,3," Mr. Alfons de Pelsmaeker",male,16,0,0,345778,9.5,,S
    
    284,1,3," Mr. Edward Arthur Dorking",male,19,0,0,A/5. 10482,8.05,,S
    
    285,0,1," Mr. Richard William Smith",male,,0,0,113056,26,A19,S
    
    286,0,3," Mr. Ivan Stankovic",male,33,0,0,349239,8.6625,,C
    
    287,1,3," Mr. Theodore de Mulder",male,30,0,0,345774,9.5,,S
    
    288,0,3," Mr. Penko Naidenoff",male,22,0,0,349206,7.8958,,S
    
    289,1,2," Mr. Masabumi Hosono",male,42,0,0,237798,13,,S
    
    290,1,3," Miss. Kate Connolly",female,22,0,0,370373,7.75,,Q
    
    291,1,1," Miss. Ellen ""Nellie"" Barber",female,26,0,0,19877,78.85,,S
    
    292,1,1," Mrs. Dickinson H (Helen Walton) Bishop",female,19,1,0,11967,91.0792,B49,C
    
    293,0,2," Mr. Rene Jacques Levy",male,36,0,0,SC/Paris 2163,12.875,D,C
    
    294,0,3," Miss. Aloisia Haas",female,24,0,0,349236,8.85,,S
    
    295,0,3," Mr. Ivan Mineff",male,24,0,0,349233,7.8958,,S
    
    296,0,1," Mr. Ervin G Lewy",male,,0,0,PC 17612,27.7208,,C
    
    297,0,3," Mr. Mansour Hanna",male,23.5,0,0,2693,7.2292,,C
    
    298,0,1," Miss. Helen Loraine Allison",female,2,1,2,113781,151.55,C22 C26,S
    
    299,1,1," Mr. Adolphe Saalfeld",male,,0,0,19988,30.5,C106,S
    
    300,1,1," Mrs. James (Helene DeLaudeniere Chaput) Baxter",female,50,0,1,PC 17558,247.5208,B58 B60,C
    
    301,1,3," Miss. Anna Katherine ""Annie Kate"" Kelly",female,,0,0,9234,7.75,,Q
    
    302,1,3," Mr. Bernard McCoy",male,,2,0,367226,23.25,,Q
    
    303,0,3," Mr. William Cahoone Jr Johnson",male,19,0,0,LINE,0,,S
    
    304,1,2," Miss. Nora A Keane",female,,0,0,226593,12.35,E101,Q
    
    305,0,3," Mr. Howard Hugh ""Harry"" Williams",male,,0,0,A/5 2466,8.05,,S
    
    306,1,1," Master. Hudson Trevor Allison",male,0.92,1,2,113781,151.55,C22 C26,S
    
    307,1,1," Miss. Margaret Fleming",female,,0,0,17421,110.8833,,C
    
    308,1,1," Mrs. Victor de Satode (Maria Josefa Perez de Soto y Vallejo) Penasco y Castellana",female,17,1,0,PC 17758,108.9,C65,C
    
    309,0,2," Mr. Samuel Abelson",male,30,1,0,P/PP 3381,24,,C
    
    310,1,1," Miss. Laura Mabel Francatelli",female,30,0,0,PC 17485,56.9292,E36,C
    
    311,1,1," Miss. Margaret Bechstein Hays",female,24,0,0,11767,83.1583,C54,C
    
    312,1,1," Miss. Emily Borie Ryerson",female,18,2,2,PC 17608,262.375,B57 B59 B63 B66,C
    
    313,0,2," Mrs. William (Anna Sylfven) Lahtinen",female,26,1,1,250651,26,,S
    
    314,0,3," Mr. Ignjac Hendekovic",male,28,0,0,349243,7.8958,,S
    
    315,0,2," Mr. Benjamin Hart",male,43,1,1,F.C.C. 13529,26.25,,S
    
    316,1,3," Miss. Helmina Josefina Nilsson",female,26,0,0,347470,7.8542,,S
    
    317,1,2," Mrs. Sinai (Miriam Sternin) Kantor",female,24,1,0,244367,26,,S
    
    318,0,2," Dr. Ernest Moraweck",male,54,0,0,29011,14,,S
    
    319,1,1," Miss. Mary Natalie Wick",female,31,0,2,36928,164.8667,C7,S
    
    320,1,1," Mrs. Frederic Oakley (Margaretta Corning Stone) Spedden",female,40,1,1,16966,134.5,E34,C
    
    321,0,3," Mr. Samuel Dennis",male,22,0,0,A/5 21172,7.25,,S
    
    322,0,3," Mr. Yoto Danoff",male,27,0,0,349219,7.8958,,S
    
    323,1,2," Miss. Hilda Mary Slayter",female,30,0,0,234818,12.35,,Q
    
    324,1,2," Mrs. Albert Francis (Sylvia Mae Harbaugh) Caldwell",female,22,1,1,248738,29,,S
    
    325,0,3," Mr. George John Jr Sage",male,,8,2,CA. 2343,69.55,,S
    
    326,1,1," Miss. Marie Grice Young",female,36,0,0,PC 17760,135.6333,C32,C
    
    327,0,3," Mr. Johan Hansen Nysveen",male,61,0,0,345364,6.2375,,S
    
    328,1,2," Mrs. (Ada E Hall) Ball",female,36,0,0,28551,13,D,S
    
    329,1,3," Mrs. Frank John (Emily Alice Brown) Goldsmith",female,31,1,1,363291,20.525,,S
    
    330,1,1," Miss. Jean Gertrude Hippach",female,16,0,1,111361,57.9792,B18,C
    
    331,1,3," Miss. Agnes McCoy",female,,2,0,367226,23.25,,Q
    
    332,0,1," Mr. Austen Partner",male,45.5,0,0,113043,28.5,C124,S
    
    333,0,1," Mr. George Edward Graham",male,38,0,1,PC 17582,153.4625,C91,S
    
    334,0,3," Mr. Leo Edmondus Vander Planke",male,16,2,0,345764,18,,S
    
    335,1,1," Mrs. Henry William (Clara Heinsheimer) Frauenthal",female,,1,0,PC 17611,133.65,,S
    
    336,0,3," Mr. Mitto Denkoff",male,,0,0,349225,7.8958,,S
    
    337,0,1," Mr. Thomas Clinton Pears",male,29,1,0,113776,66.6,C2,S
    
    338,1,1," Miss. Elizabeth Margaret Burns",female,41,0,0,16966,134.5,E40,C
    
    339,1,3," Mr. Karl Edwart Dahl",male,45,0,0,7598,8.05,,S
    
    340,0,1," Mr. Stephen Weart Blackwell",male,45,0,0,113784,35.5,T,S
    
    341,1,2," Master. Edmond Roger Navratil",male,2,1,1,230080,26,F2,S
    
    342,1,1," Miss. Alice Elizabeth Fortune",female,24,3,2,19950,263,C23 C25 C27,S
    
    343,0,2," Mr. Erik Gustaf Collander",male,28,0,0,248740,13,,S
    
    344,0,2," Mr. Charles Frederick Waddington Sedgwick",male,25,0,0,244361,13,,S
    
    345,0,2," Mr. Stanley Hubert Fox",male,36,0,0,229236,13,,S
    
    346,1,2," Miss. Amelia ""Mildred"" Brown",female,24,0,0,248733,13,F33,S
    
    347,1,2," Miss. Marion Elsie Smith",female,40,0,0,31418,13,,S
    
    348,1,3," Mrs. Thomas Henry (Mary E Finck) Davison",female,,1,0,386525,16.1,,S
    
    349,1,3," Master. William Loch ""William"" Coutts",male,3,1,1,C.A. 37671,15.9,,S
    
    350,0,3," Mr. Jovan Dimic",male,42,0,0,315088,8.6625,,S
    
    351,0,3," Mr. Nils Martin Odahl",male,23,0,0,7267,9.225,,S
    
    352,0,1," Mr. Fletcher Fellows Williams-Lambert",male,,0,0,113510,35,C128,S
    
    353,0,3," Mr. Tannous Elias",male,15,1,1,2695,7.2292,,C
    
    354,0,3," Mr. Josef Arnold-Franchi",male,25,1,0,349237,17.8,,S
    
    355,0,3," Mr. Wazli Yousif",male,,0,0,2647,7.225,,C
    
    356,0,3," Mr. Leo Peter Vanden Steen",male,28,0,0,345783,9.5,,S
    
    357,1,1," Miss. Elsie Edith Bowerman",female,22,0,1,113505,55,E33,S
    
    358,0,2," Miss. Annie Clemmer Funk",female,38,0,0,237671,13,,S
    
    359,1,3," Miss. Mary McGovern",female,,0,0,330931,7.8792,,Q
    
    360,1,3," Miss. Helen Mary ""Ellie"" Mockler",female,,0,0,330980,7.8792,,Q
    
    361,0,3," Mr. Wilhelm Skoog",male,40,1,4,347088,27.9,,S
    
    362,0,2," Mr. Sebastiano del Carlo",male,29,1,0,SC/PARIS 2167,27.7208,,C
    
    363,0,3," Mrs. (Catherine David) Barbara",female,45,0,1,2691,14.4542,,C
    
    364,0,3," Mr. Adola Asim",male,35,0,0,SOTON/O.Q. 3101310,7.05,,S
    
    365,0,3," Mr. Thomas O'Brien",male,,1,0,370365,15.5,,Q
    
    366,0,3," Mr. Mauritz Nils Martin Adahl",male,30,0,0,C 7076,7.25,,S
    
    367,1,1," Mrs. Frank Manley (Anna Sophia Atkinson) Warren",female,60,1,0,110813,75.25,D37,C
    
    368,1,3," Mrs. (Mantoura Boulos) Moussa",female,,0,0,2626,7.2292,,C
    
    369,1,3," Miss. Annie Jermyn",female,,0,0,14313,7.75,,Q
    
    370,1,1," Mme. Leontine Pauline Aubart",female,24,0,0,PC 17477,69.3,B35,C
    
    371,1,1," Mr. George Achilles Harder",male,25,1,0,11765,55.4417,E50,C
    
    372,0,3," Mr. Jakob Alfred Wiklund",male,18,1,0,3101267,6.4958,,S
    
    373,0,3," Mr. William Thomas Beavan",male,19,0,0,323951,8.05,,S
    
    374,0,1," Mr. Sante Ringhini",male,22,0,0,PC 17760,135.6333,,C
    
    375,0,3," Miss. Stina Viola Palsson",female,3,3,1,349909,21.075,,S
    
    376,1,1," Mrs. Edgar Joseph (Leila Saks) Meyer",female,,1,0,PC 17604,82.1708,,C
    
    377,1,3," Miss. Aurora Adelia Landergren",female,22,0,0,C 7077,7.25,,S
    
    378,0,1," Mr. Harry Elkins Widener",male,27,0,2,113503,211.5,C82,C
    
    379,0,3," Mr. Tannous Betros",male,20,0,0,2648,4.0125,,C
    
    380,0,3," Mr. Karl Gideon Gustafsson",male,19,0,0,347069,7.775,,S
    
    381,1,1," Miss. Rosalie Bidois",female,42,0,0,PC 17757,227.525,,C
    
    382,1,3," Miss. Maria (""Mary"") Nakid",female,1,0,2,2653,15.7417,,C
    
    383,0,3," Mr. Juho Tikkanen",male,32,0,0,STON/O 2. 3101293,7.925,,S
    
    384,1,1," Mrs. Alexander Oskar (Mary Aline Towner) Holverson",female,35,1,0,113789,52,,S
    
    385,0,3," Mr. Vasil Plotcharsky",male,,0,0,349227,7.8958,,S
    
    386,0,2," Mr. Charles Henry Davies",male,18,0,0,S.O.C. 14879,73.5,,S
    
    387,0,3," Master. Sidney Leonard Goodwin",male,1,5,2,CA 2144,46.9,,S
    
    388,1,2," Miss. Kate Buss",female,36,0,0,27849,13,,S
    
    389,0,3," Mr. Matthew Sadlier",male,,0,0,367655,7.7292,,Q
    
    390,1,2," Miss. Bertha Lehmann",female,17,0,0,SC 1748,12,,C
    
    391,1,1," Mr. William Ernest Carter",male,36,1,2,113760,120,B96 B98,S
    
    392,1,3," Mr. Carl Olof Jansson",male,21,0,0,350034,7.7958,,S
    
    393,0,3," Mr. Johan Birger Gustafsson",male,28,2,0,3101277,7.925,,S
    
    394,1,1," Miss. Marjorie Newell",female,23,1,0,35273,113.275,D36,C
    
    395,1,3," Mrs. Hjalmar (Agnes Charlotta Bengtsson) Sandstrom",female,24,0,2,PP 9549,16.7,G6,S
    
    396,0,3," Mr. Erik Johansson",male,22,0,0,350052,7.7958,,S
    
    397,0,3," Miss. Elina Olsson",female,31,0,0,350407,7.8542,,S
    
    398,0,2," Mr. Peter David McKane",male,46,0,0,28403,26,,S
    
    399,0,2," Dr. Alfred Pain",male,23,0,0,244278,10.5,,S
    
    400,1,2," Mrs. William H (Jessie L) Trout",female,28,0,0,240929,12.65,,S
    
    401,1,3," Mr. Juha Niskanen",male,39,0,0,STON/O 2. 3101289,7.925,,S
    
    402,0,3," Mr. John Adams",male,26,0,0,341826,8.05,,S
    
    403,0,3," Miss. Mari Aina Jussila",female,21,1,0,4137,9.825,,S
    
    404,0,3," Mr. Pekka Pietari Hakkarainen",male,28,1,0,STON/O2. 3101279,15.85,,S
    
    405,0,3," Miss. Marija Oreskovic",female,20,0,0,315096,8.6625,,S
    
    406,0,2," Mr. Shadrach Gale",male,34,1,0,28664,21,,S
    
    407,0,3," Mr. Carl/Charles Peter Widegren",male,51,0,0,347064,7.75,,S
    
    408,1,2," Master. William Rowe Richards",male,3,1,1,29106,18.75,,S
    
    409,0,3," Mr. Hans Martin Monsen Birkeland",male,21,0,0,312992,7.775,,S
    
    410,0,3," Miss. Ida Lefebre",female,,3,1,4133,25.4667,,S
    
    411,0,3," Mr. Todor Sdycoff",male,,0,0,349222,7.8958,,S
    
    412,0,3," Mr. Henry Hart",male,,0,0,394140,6.8583,,Q
    
    413,1,1," Miss. Daisy E Minahan",female,33,1,0,19928,90,C78,Q
    
    414,0,2," Mr. Alfred Fleming Cunningham",male,,0,0,239853,0,,S
    
    415,1,3," Mr. Johan Julian Sundman",male,44,0,0,STON/O 2. 3101269,7.925,,S
    
    416,0,3," Mrs. Thomas (Annie Louise Rowley) Meek",female,,0,0,343095,8.05,,S
    
    417,1,2," Mrs. James Vivian (Lulu Thorne Christian) Drew",female,34,1,1,28220,32.5,,S
    
    418,1,2," Miss. Lyyli Karoliina Silven",female,18,0,2,250652,13,,S
    
    419,0,2," Mr. William John Matthews",male,30,0,0,28228,13,,S
    
    420,0,3," Miss. Catharina Van Impe",female,10,0,2,345773,24.15,,S
    
    421,0,3," Mr. Stanio Gheorgheff",male,,0,0,349254,7.8958,,C
    
    422,0,3," Mr. David Charters",male,21,0,0,A/5. 13032,7.7333,,Q
    
    423,0,3," Mr. Leo Zimmerman",male,29,0,0,315082,7.875,,S
    
    424,0,3," Mrs. Ernst Gilbert (Anna Sigrid Maria Brogren) Danbom",female,28,1,1,347080,14.4,,S
    
    425,0,3," Mr. Viktor Richard Rosblom",male,18,1,1,370129,20.2125,,S
    
    426,0,3," Mr. Phillippe Wiseman",male,,0,0,A/4. 34244,7.25,,S
    
    427,1,2," Mrs. Charles V (Ada Maria Winfield) Clarke",female,28,1,0,2003,26,,S
    
    428,1,2," Miss. Kate Florence (""Mrs Kate Louise Phillips Marshall"") Phillips",female,19,0,0,250655,26,,S
    
    429,0,3," Mr. James Flynn",male,,0,0,364851,7.75,,Q
    
    430,1,3," Mr. Berk (Berk Trembisky) Pickard",male,32,0,0,SOTON/O.Q. 392078,8.05,E10,S
    
    431,1,1," Mr. Mauritz Hakan Bjornstrom-Steffansson",male,28,0,0,110564,26.55,C52,S
    
    432,1,3," Mrs. Percival (Florence Kate White) Thorneycroft",female,,1,0,376564,16.1,,S
    
    433,1,2," Mrs. Charles Alexander (Alice Adelaide Slow) Louch",female,42,1,0,SC/AH 3085,26,,S
    
    434,0,3," Mr. Nikolai Erland Kallio",male,17,0,0,STON/O 2. 3101274,7.125,,S
    
    435,0,1," Mr. William Baird Silvey",male,50,1,0,13507,55.9,E44,S
    
    436,1,1," Miss. Lucile Polk Carter",female,14,1,2,113760,120,B96 B98,S
    
    437,0,3," Miss. Doolina Margaret ""Daisy"" Ford",female,21,2,2,W./C. 6608,34.375,,S
    
    438,1,2," Mrs. Sidney (Emily Hocking) Richards",female,24,2,3,29106,18.75,,S
    
    439,0,1," Mr. Mark Fortune",male,64,1,4,19950,263,C23 C25 C27,S
    
    440,0,2," Mr. Johan Henrik Johannesson Kvillner",male,31,0,0,C.A. 18723,10.5,,S
    
    441,1,2," Mrs. Benjamin (Esther Ada Bloomfield) Hart",female,45,1,1,F.C.C. 13529,26.25,,S
    
    442,0,3," Mr. Leon Hampe",male,20,0,0,345769,9.5,,S
    
    443,0,3," Mr. Johan Emil Petterson",male,25,1,0,347076,7.775,,S
    
    444,1,2," Ms. Encarnacion Reynaldo",female,28,0,0,230434,13,,S
    
    445,1,3," Mr. Bernt Johannesen-Bratthammer",male,,0,0,65306,8.1125,,S
    
    446,1,1," Master. Washington Dodge",male,4,0,2,33638,81.8583,A34,S
    
    447,1,2," Miss. Madeleine Violet Mellinger",female,13,0,1,250644,19.5,,S
    
    448,1,1," Mr. Frederic Kimber Seward",male,34,0,0,113794,26.55,,S
    
    449,1,3," Miss. Marie Catherine Baclini",female,5,2,1,2666,19.2583,,C
    
    450,1,1," Major. Arthur Godfrey Peuchen",male,52,0,0,113786,30.5,C104,S
    
    451,0,2," Mr. Edwy Arthur West",male,36,1,2,C.A. 34651,27.75,,S
    
    452,0,3," Mr. Ingvald Olai Olsen Hagland",male,,1,0,65303,19.9667,,S
    
    453,0,1," Mr. Benjamin Laventall Foreman",male,30,0,0,113051,27.75,C111,C
    
    454,1,1," Mr. Samuel L Goldenberg",male,49,1,0,17453,89.1042,C92,C
    
    455,0,3," Mr. Joseph Peduzzi",male,,0,0,A/5 2817,8.05,,S
    
    456,1,3," Mr. Ivan Jalsevac",male,29,0,0,349240,7.8958,,C
    
    457,0,1," Mr. Francis Davis Millet",male,65,0,0,13509,26.55,E38,S
    
    458,1,1," Mrs. Frederick R (Marion) Kenyon",female,,1,0,17464,51.8625,D21,S
    
    459,1,2," Miss. Ellen Toomey",female,50,0,0,F.C.C. 13531,10.5,,S
    
    460,0,3," Mr. Maurice O'Connor",male,,0,0,371060,7.75,,Q
    
    461,1,1," Mr. Harry Anderson",male,48,0,0,19952,26.55,E12,S
    
    462,0,3," Mr. William Morley",male,34,0,0,364506,8.05,,S
    
    463,0,1," Mr. Arthur H Gee",male,47,0,0,111320,38.5,E63,S
    
    464,0,2," Mr. Jacob Christian Milling",male,48,0,0,234360,13,,S
    
    465,0,3," Mr. Simon Maisner",male,,0,0,A/S 2816,8.05,,S
    
    466,0,3," Mr. Manuel Estanslas Goncalves",male,38,0,0,SOTON/O.Q. 3101306,7.05,,S
    
    467,0,2," Mr. William Campbell",male,,0,0,239853,0,,S
    
    468,0,1," Mr. John Montgomery Smart",male,56,0,0,113792,26.55,,S
    
    469,0,3," Mr. James Scanlan",male,,0,0,36209,7.725,,Q
    
    470,1,3," Miss. Helene Barbara Baclini",female,0.75,2,1,2666,19.2583,,C
    
    471,0,3," Mr. Arthur Keefe",male,,0,0,323592,7.25,,S
    
    472,0,3," Mr. Luka Cacic",male,38,0,0,315089,8.6625,,S
    
    473,1,2," Mrs. Edwy Arthur (Ada Mary Worth) West",female,33,1,2,C.A. 34651,27.75,,S
    
    474,1,2," Mrs. Amin S (Marie Marthe Thuillard) Jerwan",female,23,0,0,SC/AH Basle 541,13.7917,D,C
    
    475,0,3," Miss. Ida Sofia Strandberg",female,22,0,0,7553,9.8375,,S
    
    476,0,1," Mr. George Quincy Clifford",male,,0,0,110465,52,A14,S
    
    477,0,2," Mr. Peter Henry Renouf",male,34,1,0,31027,21,,S
    
    478,0,3," Mr. Lewis Richard Braund",male,29,1,0,3460,7.0458,,S
    
    479,0,3," Mr. Nils August Karlsson",male,22,0,0,350060,7.5208,,S
    
    480,1,3," Miss. Hildur E Hirvonen",female,2,0,1,3101298,12.2875,,S
    
    481,0,3," Master. Harold Victor Goodwin",male,9,5,2,CA 2144,46.9,,S
    
    482,0,2," Mr. Anthony Wood ""Archie"" Frost",male,,0,0,239854,0,,S
    
    483,0,3," Mr. Richard Henry Rouse",male,50,0,0,A/5 3594,8.05,,S
    
    484,1,3," Mrs. (Hedwig) Turkula",female,63,0,0,4134,9.5875,,S
    
    485,1,1," Mr. Dickinson H Bishop",male,25,1,0,11967,91.0792,B49,C
    
    486,0,3," Miss. Jeannie Lefebre",female,,3,1,4133,25.4667,,S
    
    487,1,1," Mrs. Frederick Maxfield (Jane Anne Forby) Hoyt",female,35,1,0,19943,90,C93,S
    
    488,0,1," Mr. Edward Austin Kent",male,58,0,0,11771,29.7,B37,C
    
    489,0,3," Mr. Francis William Somerton",male,30,0,0,A.5. 18509,8.05,,S
    
    490,1,3," Master. Eden Leslie ""Neville"" Coutts",male,9,1,1,C.A. 37671,15.9,,S
    
    491,0,3," Mr. Konrad Mathias Reiersen Hagland",male,,1,0,65304,19.9667,,S
    
    492,0,3," Mr. Einar Windelov",male,21,0,0,SOTON/OQ 3101317,7.25,,S
    
    493,0,1," Mr. Harry Markland Molson",male,55,0,0,113787,30.5,C30,S
    
    494,0,1," Mr. Ramon Artagaveytia",male,71,0,0,PC 17609,49.5042,,C
    
    495,0,3," Mr. Edward Roland Stanley",male,21,0,0,A/4 45380,8.05,,S
    
    496,0,3," Mr. Gerious Yousseff",male,,0,0,2627,14.4583,,C
    
    497,1,1," Miss. Elizabeth Mussey Eustis",female,54,1,0,36947,78.2667,D20,C
    
    498,0,3," Mr. Frederick William Shellard",male,,0,0,C.A. 6212,15.1,,S
    
    499,0,1," Mrs. Hudson J C (Bessie Waldo Daniels) Allison",female,25,1,2,113781,151.55,C22 C26,S
    
    500,0,3," Mr. Olof Svensson",male,24,0,0,350035,7.7958,,S
    
    501,0,3," Mr. Petar Calic",male,17,0,0,315086,8.6625,,S
    
    502,0,3," Miss. Mary Canavan",female,21,0,0,364846,7.75,,Q
    
    503,0,3," Miss. Bridget Mary O'Sullivan",female,,0,0,330909,7.6292,,Q
    
    504,0,3," Miss. Kristina Sofia Laitinen",female,37,0,0,4135,9.5875,,S
    
    505,1,1," Miss. Roberta Maioni",female,16,0,0,110152,86.5,B79,S
    
    506,0,1," Mr. Victor de Satode Penasco y Castellana",male,18,1,0,PC 17758,108.9,C65,C
    
    507,1,2," Mrs. Frederick Charles (Jane Richards) Quick",female,33,0,2,26360,26,,S
    
    508,1,1," Mr. George (""George Arthur Brayton"") Bradley",male,,0,0,111427,26.55,,S
    
    509,0,3," Mr. Henry Margido Olsen",male,28,0,0,C 4001,22.525,,S
    
    510,1,3," Mr. Fang Lang",male,26,0,0,1601,56.4958,,S
    
    511,1,3," Mr. Eugene Patrick Daly",male,29,0,0,382651,7.75,,Q
    
    512,0,3," Mr. James Webber",male,,0,0,SOTON/OQ 3101316,8.05,,S
    
    513,1,1," Mr. James Robert McGough",male,36,0,0,PC 17473,26.2875,E25,S
    
    514,1,1," Mrs. Martin (Elizabeth L. Barrett) Rothschild",female,54,1,0,PC 17603,59.4,,C
    
    515,0,3," Mr. Satio Coleff",male,24,0,0,349209,7.4958,,S
    
    516,0,1," Mr. William Anderson Walker",male,47,0,0,36967,34.0208,D46,S
    
    517,1,2," Mrs. (Amelia Milley) Lemore",female,34,0,0,C.A. 34260,10.5,F33,S
    
    518,0,3," Mr. Patrick Ryan",male,,0,0,371110,24.15,,Q
    
    519,1,2," Mrs. William A (Florence ""Mary"" Agnes Hughes) Angle",female,36,1,0,226875,26,,S
    
    520,0,3," Mr. Stefo Pavlovic",male,32,0,0,349242,7.8958,,S
    
    521,1,1," Miss. Anne Perreault",female,30,0,0,12749,93.5,B73,S
    
    522,0,3," Mr. Janko Vovk",male,22,0,0,349252,7.8958,,S
    
    523,0,3," Mr. Sarkis Lahoud",male,,0,0,2624,7.225,,C
    
    524,1,1," Mrs. Louis Albert (Ida Sophia Fischer) Hippach",female,44,0,1,111361,57.9792,B18,C
    
    525,0,3," Mr. Fared Kassem",male,,0,0,2700,7.2292,,C
    
    526,0,3," Mr. James Farrell",male,40.5,0,0,367232,7.75,,Q
    
    527,1,2," Miss. Lucy Ridsdale",female,50,0,0,W./C. 14258,10.5,,S
    
    528,0,1," Mr. John Farthing",male,,0,0,PC 17483,221.7792,C95,S
    
    529,0,3," Mr. Johan Werner Salonen",male,39,0,0,3101296,7.925,,S
    
    530,0,2," Mr. Richard George Hocking",male,23,2,1,29104,11.5,,S
    
    531,1,2," Miss. Phyllis May Quick",female,2,1,1,26360,26,,S
    
    532,0,3," Mr. Nakli Toufik",male,,0,0,2641,7.2292,,C
    
    533,0,3," Mr. Joseph Jr Elias",male,17,1,1,2690,7.2292,,C
    
    534,1,3," Mrs. Catherine (Catherine Rizk) Peter",female,,0,2,2668,22.3583,,C
    
    535,0,3," Miss. Marija Cacic",female,30,0,0,315084,8.6625,,S
    
    536,1,2," Miss. Eva Miriam Hart",female,7,0,2,F.C.C. 13529,26.25,,S
    
    537,0,1," Major. Archibald Willingham Butt",male,45,0,0,113050,26.55,B38,S
    
    538,1,1," Miss. Bertha LeRoy",female,30,0,0,PC 17761,106.425,,C
    
    539,0,3," Mr. Samuel Beard Risien",male,,0,0,364498,14.5,,S
    
    540,1,1," Miss. Hedwig Margaritha Frolicher",female,22,0,2,13568,49.5,B39,C
    
    541,1,1," Miss. Harriet R Crosby",female,36,0,2,WE/P 5735,71,B22,S
    
    542,0,3," Miss. Ingeborg Constanzia Andersson",female,9,4,2,347082,31.275,,S
    
    543,0,3," Miss. Sigrid Elisabeth Andersson",female,11,4,2,347082,31.275,,S
    
    544,1,2," Mr. Edward Beane",male,32,1,0,2908,26,,S
    
    545,0,1," Mr. Walter Donald Douglas",male,50,1,0,PC 17761,106.425,C86,C
    
    546,0,1," Mr. Arthur Ernest Nicholson",male,64,0,0,693,26,,S
    
    547,1,2," Mrs. Edward (Ethel Clarke) Beane",female,19,1,0,2908,26,,S
    
    548,1,2," Mr. Julian Padro y Manent",male,,0,0,SC/PARIS 2146,13.8625,,C
    
    549,0,3," Mr. Frank John Goldsmith",male,33,1,1,363291,20.525,,S
    
    550,1,2," Master. John Morgan Jr Davies",male,8,1,1,C.A. 33112,36.75,,S
    
    551,1,1," Mr. John Borland Jr Thayer",male,17,0,2,17421,110.8833,C70,C
    
    552,0,2," Mr. Percival James R Sharp",male,27,0,0,244358,26,,S
    
    553,0,3," Mr. Timothy O'Brien",male,,0,0,330979,7.8292,,Q
    
    554,1,3," Mr. Fahim (""Philip Zenni"") Leeni",male,22,0,0,2620,7.225,,C
    
    555,1,3," Miss. Velin Ohman",female,22,0,0,347085,7.775,,S
    
    556,0,1," Mr. George Wright",male,62,0,0,113807,26.55,,S
    
    557,1,1," Lady. (Lucille Christiana Sutherland) (""Mrs Morgan"") Duff Gordon",female,48,1,0,11755,39.6,A16,C
    
    558,0,1," Mr. Victor Robbins",male,,0,0,PC 17757,227.525,,C
    
    559,1,1," Mrs. Emil (Tillie Mandelbaum) Taussig",female,39,1,1,110413,79.65,E67,S
    
    560,1,3," Mrs. Guillaume Joseph (Emma) de Messemaeker",female,36,1,0,345572,17.4,,S
    
    561,0,3," Mr. Thomas Rowan Morrow",male,,0,0,372622,7.75,,Q
    
    562,0,3," Mr. Husein Sivic",male,40,0,0,349251,7.8958,,S
    
    563,0,2," Mr. Robert Douglas Norman",male,28,0,0,218629,13.5,,S
    
    564,0,3," Mr. John Simmons",male,,0,0,SOTON/OQ 392082,8.05,,S
    
    565,0,3," Miss. (Marion Ogden) Meanwell",female,,0,0,SOTON/O.Q. 392087,8.05,,S
    
    566,0,3," Mr. Alfred J Davies",male,24,2,0,A/4 48871,24.15,,S
    
    567,0,3," Mr. Ilia Stoytcheff",male,19,0,0,349205,7.8958,,S
    
    568,0,3," Mrs. Nils (Alma Cornelia Berglund) Palsson",female,29,0,4,349909,21.075,,S
    
    569,0,3," Mr. Tannous Doharr",male,,0,0,2686,7.2292,,C
    
    570,1,3," Mr. Carl Jonsson",male,32,0,0,350417,7.8542,,S
    
    571,1,2," Mr. George Harris",male,62,0,0,S.W./PP 752,10.5,,S
    
    572,1,1," Mrs. Edward Dale (Charlotte Lamson) Appleton",female,53,2,0,11769,51.4792,C101,S
    
    573,1,1," Mr. John Irwin (""Irving"") Flynn",male,36,0,0,PC 17474,26.3875,E25,S
    
    574,1,3," Miss. Mary Kelly",female,,0,0,14312,7.75,,Q
    
    575,0,3," Mr. Alfred George John Rush",male,16,0,0,A/4. 20589,8.05,,S
    
    576,0,3," Mr. George Patchett",male,19,0,0,358585,14.5,,S
    
    577,1,2," Miss. Ethel Garside",female,34,0,0,243880,13,,S
    
    578,1,1," Mrs. William Baird (Alice Munger) Silvey",female,39,1,0,13507,55.9,E44,S
    
    579,0,3," Mrs. Joseph (Maria Elias) Caram",female,,1,0,2689,14.4583,,C
    
    580,1,3," Mr. Eiriik Jussila",male,32,0,0,STON/O 2. 3101286,7.925,,S
    
    581,1,2," Miss. Julie Rachel Christy",female,25,1,1,237789,30,,S
    
    582,1,1," Mrs. John Borland (Marian Longstreth Morris) Thayer",female,39,1,1,17421,110.8833,C68,C
    
    583,0,2," Mr. William James Downton",male,54,0,0,28403,26,,S
    
    584,0,1," Mr. John Hugo Ross",male,36,0,0,13049,40.125,A10,C
    
    585,0,3," Mr. Uscher Paulner",male,,0,0,3411,8.7125,,C
    
    586,1,1," Miss. Ruth Taussig",female,18,0,2,110413,79.65,E68,S
    
    587,0,2," Mr. John Denzil Jarvis",male,47,0,0,237565,15,,S
    
    588,1,1," Mr. Maxmillian Frolicher-Stehli",male,60,1,1,13567,79.2,B41,C
    
    589,0,3," Mr. Eliezer Gilinski",male,22,0,0,14973,8.05,,S
    
    590,0,3," Mr. Joseph Murdlin",male,,0,0,A./5. 3235,8.05,,S
    
    591,0,3," Mr. Matti Rintamaki",male,35,0,0,STON/O 2. 3101273,7.125,,S
    
    592,1,1," Mrs. Walter Bertram (Martha Eustis) Stephenson",female,52,1,0,36947,78.2667,D20,C
    
    593,0,3," Mr. William James Elsbury",male,47,0,0,A/5 3902,7.25,,S
    
    594,0,3," Miss. Mary Bourke",female,,0,2,364848,7.75,,Q
    
    595,0,2," Mr. John Henry Chapman",male,37,1,0,SC/AH 29037,26,,S
    
    596,0,3," Mr. Jean Baptiste Van Impe",male,36,1,1,345773,24.15,,S
    
    597,1,2," Miss. Jessie Wills Leitch",female,,0,0,248727,33,,S
    
    598,0,3," Mr. Alfred Johnson",male,49,0,0,LINE,0,,S
    
    599,0,3," Mr. Hanna Boulos",male,,0,0,2664,7.225,,C
    
    600,1,1," Sir. Cosmo Edmund (""Mr Morgan"") Duff Gordon",male,49,1,0,PC 17485,56.9292,A20,C
    
    601,1,2," Mrs. Sidney Samuel (Amy Frances Christy) Jacobsohn",female,24,2,1,243847,27,,S
    
    602,0,3," Mr. Petco Slabenoff",male,,0,0,349214,7.8958,,S
    
    603,0,1," Mr. Charles H Harrington",male,,0,0,113796,42.4,,S
    
    604,0,3," Mr. Ernst William Torber",male,44,0,0,364511,8.05,,S
    
    605,1,1," Mr. Harry (""Mr E Haven"") Homer",male,35,0,0,111426,26.55,,C
    
    606,0,3," Mr. Edvard Bengtsson Lindell",male,36,1,0,349910,15.55,,S
    
    607,0,3," Mr. Milan Karaic",male,30,0,0,349246,7.8958,,S
    
    608,1,1," Mr. Robert Williams Daniel",male,27,0,0,113804,30.5,,S
    
    609,1,2," Mrs. Joseph (Juliette Marie Louise Lafargue) Laroche",female,22,1,2,SC/Paris 2123,41.5792,,C
    
    610,1,1," Miss. Elizabeth W Shutes",female,40,0,0,PC 17582,153.4625,C125,S
    
    611,0,3," Mrs. Anders Johan (Alfrida Konstantia Brogren) Andersson",female,39,1,5,347082,31.275,,S
    
    612,0,3," Mr. Jose Neto Jardin",male,,0,0,SOTON/O.Q. 3101305,7.05,,S
    
    613,1,3," Miss. Margaret Jane Murphy",female,,1,0,367230,15.5,,Q
    
    614,0,3," Mr. John Horgan",male,,0,0,370377,7.75,,Q
    
    615,0,3," Mr. William Alfred Brocklebank",male,35,0,0,364512,8.05,,S
    
    616,1,2," Miss. Alice Herman",female,24,1,2,220845,65,,S
    
    617,0,3," Mr. Ernst Gilbert Danbom",male,34,1,1,347080,14.4,,S
    
    618,0,3," Mrs. William Arthur (Cordelia K Stanlick) Lobb",female,26,1,0,A/5. 3336,16.1,,S
    
    619,1,2," Miss. Marion Louise Becker",female,4,2,1,230136,39,F4,S
    
    620,0,2," Mr. Lawrence Gavey",male,26,0,0,31028,10.5,,S
    
    621,0,3," Mr. Antoni Yasbeck",male,27,1,0,2659,14.4542,,C
    
    622,1,1," Mr. Edwin Nelson Jr Kimball",male,42,1,0,11753,52.5542,D19,S
    
    623,1,3," Mr. Sahid Nakid",male,20,1,1,2653,15.7417,,C
    
    624,0,3," Mr. Henry Damsgaard Hansen",male,21,0,0,350029,7.8542,,S
    
    625,0,3," Mr. David John ""Dai"" Bowen",male,21,0,0,54636,16.1,,S
    
    626,0,1," Mr. Frederick Sutton",male,61,0,0,36963,32.3208,D50,S
    
    627,0,2," Rev. Charles Leonard Kirkland",male,57,0,0,219533,12.35,,Q
    
    628,1,1," Miss. Gretchen Fiske Longley",female,21,0,0,13502,77.9583,D9,S
    
    629,0,3," Mr. Guentcho Bostandyeff",male,26,0,0,349224,7.8958,,S
    
    630,0,3," Mr. Patrick D O'Connell",male,,0,0,334912,7.7333,,Q
    
    631,1,1," Mr. Algernon Henry Wilson Barkworth",male,80,0,0,27042,30,A23,S
    
    632,0,3," Mr. Johan Svensson Lundahl",male,51,0,0,347743,7.0542,,S
    
    633,1,1," Dr. Max Stahelin-Maeglin",male,32,0,0,13214,30.5,B50,C
    
    634,0,1," Mr. William Henry Marsh Parr",male,,0,0,112052,0,,S
    
    635,0,3," Miss. Mabel Skoog",female,9,3,2,347088,27.9,,S
    
    636,1,2," Miss. Mary Davis",female,28,0,0,237668,13,,S
    
    637,0,3," Mr. Antti Gustaf Leinonen",male,32,0,0,STON/O 2. 3101292,7.925,,S
    
    638,0,2," Mr. Harvey Collyer",male,31,1,1,C.A. 31921,26.25,,S
    
    639,0,3," Mrs. Juha (Maria Emilia Ojala) Panula",female,41,0,5,3101295,39.6875,,S
    
    640,0,3," Mr. Percival Thorneycroft",male,,1,0,376564,16.1,,S
    
    641,0,3," Mr. Hans Peder Jensen",male,20,0,0,350050,7.8542,,S
    
    642,1,1," Mlle. Emma Sagesser",female,24,0,0,PC 17477,69.3,B35,C
    
    643,0,3," Miss. Margit Elizabeth Skoog",female,2,3,2,347088,27.9,,S
    
    644,1,3," Mr. Choong Foo",male,,0,0,1601,56.4958,,S
    
    645,1,3," Miss. Eugenie Baclini",female,0.75,2,1,2666,19.2583,,C
    
    646,1,1," Mr. Henry Sleeper Harper",male,48,1,0,PC 17572,76.7292,D33,C
    
    647,0,3," Mr. Liudevit Cor",male,19,0,0,349231,7.8958,,S
    
    648,1,1," Col. Oberst Alfons Simonius-Blumer",male,56,0,0,13213,35.5,A26,C
    
    649,0,3," Mr. Edward Willey",male,,0,0,S.O./P.P. 751,7.55,,S
    
    650,1,3," Miss. Amy Zillah Elsie Stanley",female,23,0,0,CA. 2314,7.55,,S
    
    651,0,3," Mr. Mito Mitkoff",male,,0,0,349221,7.8958,,S
    
    652,1,2," Miss. Elsie Doling",female,18,0,1,231919,23,,S
    
    653,0,3," Mr. Johannes Halvorsen Kalvik",male,21,0,0,8475,8.4333,,S
    
    654,1,3," Miss. Hanora ""Norah"" O'Leary",female,,0,0,330919,7.8292,,Q
    
    655,0,3," Miss. Hanora ""Nora"" Hegarty",female,18,0,0,365226,6.75,,Q
    
    656,0,2," Mr. Leonard Mark Hickman",male,24,2,0,S.O.C. 14879,73.5,,S
    
    657,0,3," Mr. Alexander Radeff",male,,0,0,349223,7.8958,,S
    
    658,0,3," Mrs. John (Catherine) Bourke",female,32,1,1,364849,15.5,,Q
    
    659,0,2," Mr. George Floyd Eitemiller",male,23,0,0,29751,13,,S
    
    660,0,1," Mr. Arthur Webster Newell",male,58,0,2,35273,113.275,D48,C
    
    661,1,1," Dr. Henry William Frauenthal",male,50,2,0,PC 17611,133.65,,S
    
    662,0,3," Mr. Mohamed Badt",male,40,0,0,2623,7.225,,C
    
    663,0,1," Mr. Edward Pomeroy Colley",male,47,0,0,5727,25.5875,E58,S
    
    664,0,3," Mr. Peju Coleff",male,36,0,0,349210,7.4958,,S
    
    665,1,3," Mr. Eino William Lindqvist",male,20,1,0,STON/O 2. 3101285,7.925,,S
    
    666,0,2," Mr. Lewis Hickman",male,32,2,0,S.O.C. 14879,73.5,,S
    
    667,0,2," Mr. Reginald Fenton Butler",male,25,0,0,234686,13,,S
    
    668,0,3," Mr. Knud Paust Rommetvedt",male,,0,0,312993,7.775,,S
    
    669,0,3," Mr. Jacob Cook",male,43,0,0,A/5 3536,8.05,,S
    
    670,1,1," Mrs. Elmer Zebley (Juliet Cummins Wright) Taylor",female,,1,0,19996,52,C126,S
    
    671,1,2," Mrs. Thomas William Solomon (Elizabeth Catherine Ford) Brown",female,40,1,1,29750,39,,S
    
    672,0,1," Mr. Thornton Davidson",male,31,1,0,F.C. 12750,52,B71,S
    
    673,0,2," Mr. Henry Michael Mitchell",male,70,0,0,C.A. 24580,10.5,,S
    
    674,1,2," Mr. Charles Wilhelms",male,31,0,0,244270,13,,S
    
    675,0,2," Mr. Ennis Hastings Watson",male,,0,0,239856,0,,S
    
    676,0,3," Mr. Gustaf Hjalmar Edvardsson",male,18,0,0,349912,7.775,,S
    
    677,0,3," Mr. Frederick Charles Sawyer",male,24.5,0,0,342826,8.05,,S
    
    678,1,3," Miss. Anna Sofia Turja",female,18,0,0,4138,9.8417,,S
    
    679,0,3," Mrs. Frederick (Augusta Tyler) Goodwin",female,43,1,6,CA 2144,46.9,,S
    
    680,1,1," Mr. Thomas Drake Martinez Cardeza",male,36,0,1,PC 17755,512.3292,B51 B53 B55,C
    
    681,0,3," Miss. Katie Peters",female,,0,0,330935,8.1375,,Q
    
    682,1,1," Mr. Hammad Hassab",male,27,0,0,PC 17572,76.7292,D49,C
    
    683,0,3," Mr. Thor Anderson Olsvigen",male,20,0,0,6563,9.225,,S
    
    684,0,3," Mr. Charles Edward Goodwin",male,14,5,2,CA 2144,46.9,,S
    
    685,0,2," Mr. Thomas William Solomon Brown",male,60,1,1,29750,39,,S
    
    686,0,2," Mr. Joseph Philippe Lemercier Laroche",male,25,1,2,SC/Paris 2123,41.5792,,C
    
    687,0,3," Mr. Jaako Arnold Panula",male,14,4,1,3101295,39.6875,,S
    
    688,0,3," Mr. Branko Dakic",male,19,0,0,349228,10.1708,,S
    
    689,0,3," Mr. Eberhard Thelander Fischer",male,18,0,0,350036,7.7958,,S
    
    690,1,1," Miss. Georgette Alexandra Madill",female,15,0,1,24160,211.3375,B5,S
    
    691,1,1," Mr. Albert Adrian Dick",male,31,1,0,17474,57,B20,S
    
    692,1,3," Miss. Manca Karun",female,4,0,1,349256,13.4167,,C
    
    693,1,3," Mr. Ali Lam",male,,0,0,1601,56.4958,,S
    
    694,0,3," Mr. Khalil Saad",male,25,0,0,2672,7.225,,C
    
    695,0,1," Col. John Weir",male,60,0,0,113800,26.55,,S
    
    696,0,2," Mr. Charles Henry Chapman",male,52,0,0,248731,13.5,,S
    
    697,0,3," Mr. James Kelly",male,44,0,0,363592,8.05,,S
    
    698,1,3," Miss. Katherine ""Katie"" Mullens",female,,0,0,35852,7.7333,,Q
    
    699,0,1," Mr. John Borland Thayer",male,49,1,1,17421,110.8833,C68,C
    
    700,0,3," Mr. Adolf Mathias Nicolai Olsen Humblen",male,42,0,0,348121,7.65,F G63,S
    
    701,1,1," Mrs. John Jacob (Madeleine Talmadge Force) Astor",female,18,1,0,PC 17757,227.525,C62 C64,C
    
    702,1,1," Mr. Spencer Victor Silverthorne",male,35,0,0,PC 17475,26.2875,E24,S
    
    703,0,3," Miss. Saiide Barbara",female,18,0,1,2691,14.4542,,C
    
    704,0,3," Mr. Martin Gallagher",male,25,0,0,36864,7.7417,,Q
    
    705,0,3," Mr. Henrik Juul Hansen",male,26,1,0,350025,7.8542,,S
    
    706,0,2," Mr. Henry Samuel (""Mr Henry Marshall"") Morley",male,39,0,0,250655,26,,S
    
    707,1,2," Mrs. Florence ""Fannie"" Kelly",female,45,0,0,223596,13.5,,S
    
    708,1,1," Mr. Edward Pennington Calderhead",male,42,0,0,PC 17476,26.2875,E24,S
    
    709,1,1," Miss. Alice Cleaver",female,22,0,0,113781,151.55,,S
    
    710,1,3," Master. Halim Gonios (""William George"") Moubarek",male,,1,1,2661,15.2458,,C
    
    711,1,1," Mlle. Berthe Antonine (""Mrs de Villiers"") Mayne",female,24,0,0,PC 17482,49.5042,C90,C
    
    712,0,1," Mr. Herman Klaber",male,,0,0,113028,26.55,C124,S
    
    713,1,1," Mr. Elmer Zebley Taylor",male,48,1,0,19996,52,C126,S
    
    714,0,3," Mr. August Viktor Larsson",male,29,0,0,7545,9.4833,,S
    
    715,0,2," Mr. Samuel Greenberg",male,52,0,0,250647,13,,S
    
    716,0,3," Mr. Peter Andreas Lauritz Andersen Soholt",male,19,0,0,348124,7.65,F G73,S
    
    717,1,1," Miss. Caroline Louise Endres",female,38,0,0,PC 17757,227.525,C45,C
    
    718,1,2," Miss. Edwina Celia ""Winnie"" Troutt",female,27,0,0,34218,10.5,E101,S
    
    719,0,3," Mr. Michael McEvoy",male,,0,0,36568,15.5,,Q
    
    720,0,3," Mr. Malkolm Joackim Johnson",male,33,0,0,347062,7.775,,S
    
    721,1,2," Miss. Annie Jessie ""Nina"" Harper",female,6,0,1,248727,33,,S
    
    722,0,3," Mr. Svend Lauritz Jensen",male,17,1,0,350048,7.0542,,S
    
    723,0,2," Mr. William Henry Gillespie",male,34,0,0,12233,13,,S
    
    724,0,2," Mr. Henry Price Hodges",male,50,0,0,250643,13,,S
    
    725,1,1," Mr. Norman Campbell Chambers",male,27,1,0,113806,53.1,E8,S
    
    726,0,3," Mr. Luka Oreskovic",male,20,0,0,315094,8.6625,,S
    
    727,1,2," Mrs. Peter Henry (Lillian Jefferys) Renouf",female,30,3,0,31027,21,,S
    
    728,1,3," Miss. Margareth Mannion",female,,0,0,36866,7.7375,,Q
    
    729,0,2," Mr. Kurt Arnold Gottfrid Bryhl",male,25,1,0,236853,26,,S
    
    730,0,3," Miss. Pieta Sofia Ilmakangas",female,25,1,0,STON/O2. 3101271,7.925,,S
    
    731,1,1," Miss. Elisabeth Walton Allen",female,29,0,0,24160,211.3375,B5,S
    
    732,0,3," Mr. Houssein G N Hassan",male,11,0,0,2699,18.7875,,C
    
    733,0,2," Mr. Robert J Knight",male,,0,0,239855,0,,S
    
    734,0,2," Mr. William John Berriman",male,23,0,0,28425,13,,S
    
    735,0,2," Mr. Moses Aaron Troupiansky",male,23,0,0,233639,13,,S
    
    736,0,3," Mr. Leslie Williams",male,28.5,0,0,54636,16.1,,S
    
    737,0,3," Mrs. Edward (Margaret Ann Watson) Ford",female,48,1,3,W./C. 6608,34.375,,S
    
    738,1,1," Mr. Gustave J Lesurer",male,35,0,0,PC 17755,512.3292,B101,C
    
    739,0,3," Mr. Kanio Ivanoff",male,,0,0,349201,7.8958,,S
    
    740,0,3," Mr. Minko Nankoff",male,,0,0,349218,7.8958,,S
    
    741,1,1," Mr. Walter James Hawksford",male,,0,0,16988,30,D45,S
    
    742,0,1," Mr. Tyrell William Cavendish",male,36,1,0,19877,78.85,C46,S
    
    743,1,1," Miss. Susan Parker ""Suzette"" Ryerson",female,21,2,2,PC 17608,262.375,B57 B59 B63 B66,C
    
    744,0,3," Mr. Neal McNamee",male,24,1,0,376566,16.1,,S
    
    745,1,3," Mr. Juho Stranden",male,31,0,0,STON/O 2. 3101288,7.925,,S
    
    746,0,1," Capt. Edward Gifford Crosby",male,70,1,1,WE/P 5735,71,B22,S
    
    747,0,3," Mr. Rossmore Edward Abbott",male,16,1,1,C.A. 2673,20.25,,S
    
    748,1,2," Miss. Anna Sinkkonen",female,30,0,0,250648,13,,S
    
    749,0,1," Mr. Daniel Warner Marvin",male,19,1,0,113773,53.1,D30,S
    
    750,0,3," Mr. Michael Connaghton",male,31,0,0,335097,7.75,,Q
    
    751,1,2," Miss. Joan Wells",female,4,1,1,29103,23,,S
    
    752,1,3," Master. Meier Moor",male,6,0,1,392096,12.475,E121,S
    
    753,0,3," Mr. Johannes Joseph Vande Velde",male,33,0,0,345780,9.5,,S
    
    754,0,3," Mr. Lalio Jonkoff",male,23,0,0,349204,7.8958,,S
    
    755,1,2," Mrs. Samuel (Jane Laver) Herman",female,48,1,2,220845,65,,S
    
    756,1,2," Master. Viljo Hamalainen",male,0.67,1,1,250649,14.5,,S
    
    757,0,3," Mr. August Sigfrid Carlsson",male,28,0,0,350042,7.7958,,S
    
    758,0,2," Mr. Percy Andrew Bailey",male,18,0,0,29108,11.5,,S
    
    759,0,3," Mr. Thomas Leonard Theobald",male,34,0,0,363294,8.05,,S
    
    760,1,1," the Countess. of (Lucy Noel Martha Dyer-Edwards) Rothes",female,33,0,0,110152,86.5,B77,S
    
    761,0,3," Mr. John Garfirth",male,,0,0,358585,14.5,,S
    
    762,0,3," Mr. Iisakki Antino Aijo Nirva",male,41,0,0,SOTON/O2 3101272,7.125,,S
    
    763,1,3," Mr. Hanna Assi Barah",male,20,0,0,2663,7.2292,,C
    
    764,1,1," Mrs. William Ernest (Lucile Polk) Carter",female,36,1,2,113760,120,B96 B98,S
    
    765,0,3," Mr. Hans Linus Eklund",male,16,0,0,347074,7.775,,S
    
    766,1,1," Mrs. John C (Anna Andrews) Hogeboom",female,51,1,0,13502,77.9583,D11,S
    
    767,0,1," Dr. Arthur Jackson Brewe",male,,0,0,112379,39.6,,C
    
    768,0,3," Miss. Mary Mangan",female,30.5,0,0,364850,7.75,,Q
    
    769,0,3," Mr. Daniel J Moran",male,,1,0,371110,24.15,,Q
    
    770,0,3," Mr. Daniel Danielsen Gronnestad",male,32,0,0,8471,8.3625,,S
    
    771,0,3," Mr. Rene Aime Lievens",male,24,0,0,345781,9.5,,S
    
    772,0,3," Mr. Niels Peder Jensen",male,48,0,0,350047,7.8542,,S
    
    773,0,2," Mrs. (Mary) Mack",female,57,0,0,S.O./P.P. 3,10.5,E77,S
    
    774,0,3," Mr. Dibo Elias",male,,0,0,2674,7.225,,C
    
    775,1,2," Mrs. Elizabeth (Eliza Needs) Hocking",female,54,1,3,29105,23,,S
    
    776,0,3," Mr. Pehr Fabian Oliver Malkolm Myhrman",male,18,0,0,347078,7.75,,S
    
    777,0,3," Mr. Roger Tobin",male,,0,0,383121,7.75,F38,Q
    
    778,1,3," Miss. Virginia Ethel Emanuel",female,5,0,0,364516,12.475,,S
    
    779,0,3," Mr. Thomas J Kilgannon",male,,0,0,36865,7.7375,,Q
    
    780,1,1," Mrs. Edward Scott (Elisabeth Walton McMillan) Robert",female,43,0,1,24160,211.3375,B3,S
    
    781,1,3," Miss. Banoura Ayoub",female,13,0,0,2687,7.2292,,C
    
    782,1,1," Mrs. Albert Adrian (Vera Gillespie) Dick",female,17,1,0,17474,57,B20,S
    
    783,0,1," Mr. Milton Clyde Long",male,29,0,0,113501,30,D6,S
    
    784,0,3," Mr. Andrew G Johnston",male,,1,2,W./C. 6607,23.45,,S
    
    785,0,3," Mr. William Ali",male,25,0,0,SOTON/O.Q. 3101312,7.05,,S
    
    786,0,3," Mr. Abraham (David Lishin) Harmer",male,25,0,0,374887,7.25,,S
    
    787,1,3," Miss. Anna Sofia Sjoblom",female,18,0,0,3101265,7.4958,,S
    
    788,0,3," Master. George Hugh Rice",male,8,4,1,382652,29.125,,Q
    
    789,1,3," Master. Bertram Vere Dean",male,1,1,2,C.A. 2315,20.575,,S
    
    790,0,1," Mr. Benjamin Guggenheim",male,46,0,0,PC 17593,79.2,B82 B84,C
    
    791,0,3," Mr. Andrew ""Andy"" Keane",male,,0,0,12460,7.75,,Q
    
    792,0,2," Mr. Alfred Gaskell",male,16,0,0,239865,26,,S
    
    793,0,3," Miss. Stella Anna Sage",female,,8,2,CA. 2343,69.55,,S
    
    794,0,1," Mr. William Fisher Hoyt",male,,0,0,PC 17600,30.6958,,C
    
    795,0,3," Mr. Ristiu Dantcheff",male,25,0,0,349203,7.8958,,S
    
    796,0,2," Mr. Richard Otter",male,39,0,0,28213,13,,S
    
    797,1,1," Dr. Alice (Farnham) Leader",female,49,0,0,17465,25.9292,D17,S
    
    798,1,3," Mrs. Mara Osman",female,31,0,0,349244,8.6833,,S
    
    799,0,3," Mr. Yousseff Ibrahim Shawah",male,30,0,0,2685,7.2292,,C
    
    800,0,3," Mrs. Jean Baptiste (Rosalie Paula Govaert) Van Impe",female,30,1,1,345773,24.15,,S
    
    801,0,2," Mr. Martin Ponesell",male,34,0,0,250647,13,,S
    
    802,1,2," Mrs. Harvey (Charlotte Annie Tate) Collyer",female,31,1,1,C.A. 31921,26.25,,S
    
    803,1,1," Master. William Thornton II Carter",male,11,1,2,113760,120,B96 B98,S
    
    804,1,3," Master. Assad Alexander Thomas",male,0.42,0,1,2625,8.5167,,C
    
    805,1,3," Mr. Oskar Arvid Hedman",male,27,0,0,347089,6.975,,S
    
    806,0,3," Mr. Karl Johan Johansson",male,31,0,0,347063,7.775,,S
    
    807,0,1," Mr. Thomas Jr Andrews",male,39,0,0,112050,0,A36,S
    
    808,0,3," Miss. Ellen Natalia Pettersson",female,18,0,0,347087,7.775,,S
    
    809,0,2," Mr. August Meyer",male,39,0,0,248723,13,,S
    
    810,1,1," Mrs. Norman Campbell (Bertha Griggs) Chambers",female,33,1,0,113806,53.1,E8,S
    
    811,0,3," Mr. William Alexander",male,26,0,0,3474,7.8875,,S
    
    812,0,3," Mr. James Lester",male,39,0,0,A/4 48871,24.15,,S
    
    813,0,2," Mr. Richard James Slemen",male,35,0,0,28206,10.5,,S
    
    814,0,3," Miss. Ebba Iris Alfrida Andersson",female,6,4,2,347082,31.275,,S
    
    815,0,3," Mr. Ernest Portage Tomlin",male,30.5,0,0,364499,8.05,,S
    
    816,0,1," Mr. Richard Fry",male,,0,0,112058,0,B102,S
    
    817,0,3," Miss. Wendla Maria Heininen",female,23,0,0,STON/O2. 3101290,7.925,,S
    
    818,0,2," Mr. Albert Mallet",male,31,1,1,S.C./PARIS 2079,37.0042,,C
    
    819,0,3," Mr. John Fredrik Alexander Holm",male,43,0,0,C 7075,6.45,,S
    
    820,0,3," Master. Karl Thorsten Skoog",male,10,3,2,347088,27.9,,S
    
    821,1,1," Mrs. Charles Melville (Clara Jennings Gregg) Hays",female,52,1,1,12749,93.5,B69,S
    
    822,1,3," Mr. Nikola Lulic",male,27,0,0,315098,8.6625,,S
    
    823,0,1," Jonkheer. John George Reuchlin",male,38,0,0,19972,0,,S
    
    824,1,3," Mrs. (Beila) Moor",female,27,0,1,392096,12.475,E121,S
    
    825,0,3," Master. Urho Abraham Panula",male,2,4,1,3101295,39.6875,,S
    
    826,0,3," Mr. John Flynn",male,,0,0,368323,6.95,,Q
    
    827,0,3," Mr. Len Lam",male,,0,0,1601,56.4958,,S
    
    828,1,2," Master. Andre Mallet",male,1,0,2,S.C./PARIS 2079,37.0042,,C
    
    829,1,3," Mr. Thomas Joseph McCormack",male,,0,0,367228,7.75,,Q
    
    830,1,1," Mrs. George Nelson (Martha Evelyn) Stone",female,62,0,0,113572,80,B28,
    
    831,1,3," Mrs. Antoni (Selini Alexander) Yasbeck",female,15,1,0,2659,14.4542,,C
    
    832,1,2," Master. George Sibley Richards",male,0.83,1,1,29106,18.75,,S
    
    833,0,3," Mr. Amin Saad",male,,0,0,2671,7.2292,,C
    
    834,0,3," Mr. Albert Augustsson",male,23,0,0,347468,7.8542,,S
    
    835,0,3," Mr. Owen George Allum",male,18,0,0,2223,8.3,,S
    
    836,1,1," Miss. Sara Rebecca Compton",female,39,1,1,PC 17756,83.1583,E49,C
    
    837,0,3," Mr. Jakob Pasic",male,21,0,0,315097,8.6625,,S
    
    838,0,3," Mr. Maurice Sirota",male,,0,0,392092,8.05,,S
    
    839,1,3," Mr. Chang Chip",male,32,0,0,1601,56.4958,,S
    
    840,1,1," Mr. Pierre Marechal",male,,0,0,11774,29.7,C47,C
    
    841,0,3," Mr. Ilmari Rudolf Alhomaki",male,20,0,0,SOTON/O2 3101287,7.925,,S
    
    842,0,2," Mr. Thomas Charles Mudd",male,16,0,0,S.O./P.P. 3,10.5,,S
    
    843,1,1," Miss. Augusta Serepeca",female,30,0,0,113798,31,,C
    
    844,0,3," Mr. Peter L Lemberopolous",male,34.5,0,0,2683,6.4375,,C
    
    845,0,3," Mr. Jeso Culumovic",male,17,0,0,315090,8.6625,,S
    
    846,0,3," Mr. Anthony Abbing",male,42,0,0,C.A. 5547,7.55,,S
    
    847,0,3," Mr. Douglas Bullen Sage",male,,8,2,CA. 2343,69.55,,S
    
    848,0,3," Mr. Marin Markoff",male,35,0,0,349213,7.8958,,C
    
    849,0,2," Rev. John Harper",male,28,0,1,248727,33,,S
    
    850,1,1," Mrs. Samuel L (Edwiga Grabowska) Goldenberg",female,,1,0,17453,89.1042,C92,C
    
    851,0,3," Master. Sigvard Harald Elias Andersson",male,4,4,2,347082,31.275,,S
    
    852,0,3," Mr. Johan Svensson",male,74,0,0,347060,7.775,,S
    
    853,0,3," Miss. Nourelain Boulos",female,9,1,1,2678,15.2458,,C
    
    854,1,1," Miss. Mary Conover Lines",female,16,0,1,PC 17592,39.4,D28,S
    
    855,0,2," Mrs. Ernest Courtenay (Lilian Hughes) Carter",female,44,1,0,244252,26,,S
    
    856,1,3," Mrs. Sam (Leah Rosen) Aks",female,18,0,1,392091,9.35,,S
    
    857,1,1," Mrs. George Dennick (Mary Hitchcock) Wick",female,45,1,1,36928,164.8667,,S
    
    858,1,1," Mr. Peter Denis  Daly",male,51,0,0,113055,26.55,E17,S
    
    859,1,3," Mrs. Solomon (Latifa Qurban) Baclini",female,24,0,3,2666,19.2583,,C
    
    860,0,3," Mr. Raihed Razi",male,,0,0,2629,7.2292,,C
    
    861,0,3," Mr. Claus Peter Hansen",male,41,2,0,350026,14.1083,,S
    
    862,0,2," Mr. Frederick Edward Giles",male,21,1,0,28134,11.5,,S
    
    863,1,1," Mrs. Frederick Joel (Margaret Welles Barron) Swift",female,48,0,0,17466,25.9292,D17,S
    
    864,0,3," Miss. Dorothy Edith ""Dolly"" Sage",female,,8,2,CA. 2343,69.55,,S
    
    865,0,2," Mr. John William Gill",male,24,0,0,233866,13,,S
    
    866,1,2," Mrs. (Karolina) Bystrom",female,42,0,0,236852,13,,S
    
    867,1,2," Miss. Asuncion Duran y More",female,27,1,0,SC/PARIS 2149,13.8583,,C
    
    868,0,1," Mr. Washington Augustus II Roebling",male,31,0,0,PC 17590,50.4958,A24,S
    
    869,0,3," Mr. Philemon van Melkebeke",male,,0,0,345777,9.5,,S
    
    870,1,3," Master. Harold Theodor Johnson",male,4,1,1,347742,11.1333,,S
    
    871,0,3," Mr. Cerin Balkic",male,26,0,0,349248,7.8958,,S
    
    872,1,1," Mrs. Richard Leonard (Sallie Monypeny) Beckwith",female,47,1,1,11751,52.5542,D35,S
    
    873,0,1," Mr. Frans Olof Carlsson",male,33,0,0,695,5,B51 B53 B55,S
    
    874,0,3," Mr. Victor Vander Cruyssen",male,47,0,0,345765,9,,S
    
    875,1,2," Mrs. Samuel (Hannah Wizosky) Abelson",female,28,1,0,P/PP 3381,24,,C
    
    876,1,3," Miss. Adele Kiamie ""Jane"" Najib",female,15,0,0,2667,7.225,,C
    
    877,0,3," Mr. Alfred Ossian Gustafsson",male,20,0,0,7534,9.8458,,S
    
    878,0,3," Mr. Nedelio Petroff",male,19,0,0,349212,7.8958,,S
    
    879,0,3," Mr. Kristo Laleff",male,,0,0,349217,7.8958,,S
    
    880,1,1," Mrs. Thomas Jr (Lily Alexenia Wilson) Potter",female,56,0,1,11767,83.1583,C50,C
    
    881,1,2," Mrs. William (Imanita Parrish Hall) Shelley",female,25,0,1,230433,26,,S
    
    882,0,3," Mr. Johann Markun",male,33,0,0,349257,7.8958,,S
    
    883,0,3," Miss. Gerda Ulrika Dahlberg",female,22,0,0,7552,10.5167,,S
    
    884,0,2," Mr. Frederick James Banfield",male,28,0,0,C.A./SOTON 34068,10.5,,S
    
    885,0,3," Mr. Henry Jr Sutehall",male,25,0,0,SOTON/OQ 392076,7.05,,S
    
    886,0,3," Mrs. William (Margaret Norton) Rice",female,39,0,5,382652,29.125,,Q
    
    887,0,2," Rev. Juozas Montvila",male,27,0,0,211536,13,,S
    
    888,1,1," Miss. Margaret Edith Graham",female,19,0,0,112053,30,B42,S
    
    889,0,3," Miss. Catherine Helen ""Carrie"" Johnston",female,,1,2,W./C. 6607,23.45,,S
    
    890,1,1," Mr. Karl Howell Behr",male,26,0,0,111369,30,C148,C
    
    891,0,3," Mr. Patrick Dooley",male,32,0,0,370376,7.75,,Q
    
    


```python
#criando uma lista
for dado in linhas[1:]:
    dado_tratado = tratar_nome(dado)
    dado_como_lista = dado_tratado.split(',')
    print(dado_como_lista)
```

    ['1', '0', '3', '" Mr. Owen Harris Braund"', 'male', '22', '1', '0', 'A/5 21171', '7.25', '', 'S\n']
    ['2', '1', '1', '" Mrs. John Bradley (Florence Briggs Thayer) Cumings"', 'female', '38', '1', '0', 'PC 17599', '71.2833', 'C85', 'C\n']
    ['3', '1', '3', '" Miss. Laina Heikkinen"', 'female', '26', '0', '0', 'STON/O2. 3101282', '7.925', '', 'S\n']
    ['4', '1', '1', '" Mrs. Jacques Heath (Lily May Peel) Futrelle"', 'female', '35', '1', '0', '113803', '53.1', 'C123', 'S\n']
    ['5', '0', '3', '" Mr. William Henry Allen"', 'male', '35', '0', '0', '373450', '8.05', '', 'S\n']
    ['6', '0', '3', '" Mr. James Moran"', 'male', '', '0', '0', '330877', '8.4583', '', 'Q\n']
    ['7', '0', '1', '" Mr. Timothy J McCarthy"', 'male', '54', '0', '0', '17463', '51.8625', 'E46', 'S\n']
    ['8', '0', '3', '" Master. Gosta Leonard Palsson"', 'male', '2', '3', '1', '349909', '21.075', '', 'S\n']
    ['9', '1', '3', '" Mrs. Oscar W (Elisabeth Vilhelmina Berg) Johnson"', 'female', '27', '0', '2', '347742', '11.1333', '', 'S\n']
    ['10', '1', '2', '" Mrs. Nicholas (Adele Achem) Nasser"', 'female', '14', '1', '0', '237736', '30.0708', '', 'C\n']
    ['11', '1', '3', '" Miss. Marguerite Rut Sandstrom"', 'female', '4', '1', '1', 'PP 9549', '16.7', 'G6', 'S\n']
    ['12', '1', '1', '" Miss. Elizabeth Bonnell"', 'female', '58', '0', '0', '113783', '26.55', 'C103', 'S\n']
    ['13', '0', '3', '" Mr. William Henry Saundercock"', 'male', '20', '0', '0', 'A/5. 2151', '8.05', '', 'S\n']
    ['14', '0', '3', '" Mr. Anders Johan Andersson"', 'male', '39', '1', '5', '347082', '31.275', '', 'S\n']
    ['15', '0', '3', '" Miss. Hulda Amanda Adolfina Vestrom"', 'female', '14', '0', '0', '350406', '7.8542', '', 'S\n']
    ['16', '1', '2', '" Mrs. (Mary D Kingcome)  Hewlett"', 'female', '55', '0', '0', '248706', '16', '', 'S\n']
    ['17', '0', '3', '" Master. Eugene Rice"', 'male', '2', '4', '1', '382652', '29.125', '', 'Q\n']
    ['18', '1', '2', '" Mr. Charles Eugene Williams"', 'male', '', '0', '0', '244373', '13', '', 'S\n']
    ['19', '0', '3', '" Mrs. Julius (Emelia Maria Vandemoortele) Vander Planke"', 'female', '31', '1', '0', '345763', '18', '', 'S\n']
    ['20', '1', '3', '" Mrs. Fatima Masselmani"', 'female', '', '0', '0', '2649', '7.225', '', 'C\n']
    ['21', '0', '2', '" Mr. Joseph J Fynney"', 'male', '35', '0', '0', '239865', '26', '', 'S\n']
    ['22', '1', '2', '" Mr. Lawrence Beesley"', 'male', '34', '0', '0', '248698', '13', 'D56', 'S\n']
    ['23', '1', '3', '" Miss. Anna ""Annie"" McGowan"', 'female', '15', '0', '0', '330923', '8.0292', '', 'Q\n']
    ['24', '1', '1', '" Mr. William Thompson Sloper"', 'male', '28', '0', '0', '113788', '35.5', 'A6', 'S\n']
    ['25', '0', '3', '" Miss. Torborg Danira Palsson"', 'female', '8', '3', '1', '349909', '21.075', '', 'S\n']
    ['26', '1', '3', '" Mrs. Carl Oscar (Selma Augusta Emilia Johansson) Asplund"', 'female', '38', '1', '5', '347077', '31.3875', '', 'S\n']
    ['27', '0', '3', '" Mr. Farred Chehab Emir"', 'male', '', '0', '0', '2631', '7.225', '', 'C\n']
    ['28', '0', '1', '" Mr. Charles Alexander Fortune"', 'male', '19', '3', '2', '19950', '263', 'C23 C25 C27', 'S\n']
    ['29', '1', '3', '" Miss. Ellen ""Nellie"" O\'Dwyer"', 'female', '', '0', '0', '330959', '7.8792', '', 'Q\n']
    ['30', '0', '3', '" Mr. Lalio Todoroff"', 'male', '', '0', '0', '349216', '7.8958', '', 'S\n']
    ['31', '0', '1', '" Don. Manuel E Uruchurtu"', 'male', '40', '0', '0', 'PC 17601', '27.7208', '', 'C\n']
    ['32', '1', '1', '" Mrs. William Augustus (Marie Eugenie) Spencer"', 'female', '', '1', '0', 'PC 17569', '146.5208', 'B78', 'C\n']
    ['33', '1', '3', '" Miss. Mary Agatha Glynn"', 'female', '', '0', '0', '335677', '7.75', '', 'Q\n']
    ['34', '0', '2', '" Mr. Edward H Wheadon"', 'male', '66', '0', '0', 'C.A. 24579', '10.5', '', 'S\n']
    ['35', '0', '1', '" Mr. Edgar Joseph Meyer"', 'male', '28', '1', '0', 'PC 17604', '82.1708', '', 'C\n']
    ['36', '0', '1', '" Mr. Alexander Oskar Holverson"', 'male', '42', '1', '0', '113789', '52', '', 'S\n']
    ['37', '1', '3', '" Mr. Hanna Mamee"', 'male', '', '0', '0', '2677', '7.2292', '', 'C\n']
    ['38', '0', '3', '" Mr. Ernest Charles Cann"', 'male', '21', '0', '0', 'A./5. 2152', '8.05', '', 'S\n']
    ['39', '0', '3', '" Miss. Augusta Maria Vander Planke"', 'female', '18', '2', '0', '345764', '18', '', 'S\n']
    ['40', '1', '3', '" Miss. Jamila Nicola-Yarred"', 'female', '14', '1', '0', '2651', '11.2417', '', 'C\n']
    ['41', '0', '3', '" Mrs. Johan (Johanna Persdotter Larsson) Ahlin"', 'female', '40', '1', '0', '7546', '9.475', '', 'S\n']
    ['42', '0', '2', '" Mrs. William John Robert (Dorothy Ann Wonnacott) Turpin"', 'female', '27', '1', '0', '11668', '21', '', 'S\n']
    ['43', '0', '3', '" Mr. Theodor Kraeff"', 'male', '', '0', '0', '349253', '7.8958', '', 'C\n']
    ['44', '1', '2', '" Miss. Simonne Marie Anne Andree Laroche"', 'female', '3', '1', '2', 'SC/Paris 2123', '41.5792', '', 'C\n']
    ['45', '1', '3', '" Miss. Margaret Delia Devaney"', 'female', '19', '0', '0', '330958', '7.8792', '', 'Q\n']
    ['46', '0', '3', '" Mr. William John Rogers"', 'male', '', '0', '0', 'S.C./A.4. 23567', '8.05', '', 'S\n']
    ['47', '0', '3', '" Mr. Denis Lennon"', 'male', '', '1', '0', '370371', '15.5', '', 'Q\n']
    ['48', '1', '3', '" Miss. Bridget O\'Driscoll"', 'female', '', '0', '0', '14311', '7.75', '', 'Q\n']
    ['49', '0', '3', '" Mr. Youssef Samaan"', 'male', '', '2', '0', '2662', '21.6792', '', 'C\n']
    ['50', '0', '3', '" Mrs. Josef (Josefine Franchi) Arnold-Franchi"', 'female', '18', '1', '0', '349237', '17.8', '', 'S\n']
    ['51', '0', '3', '" Master. Juha Niilo Panula"', 'male', '7', '4', '1', '3101295', '39.6875', '', 'S\n']
    ['52', '0', '3', '" Mr. Richard Cater Nosworthy"', 'male', '21', '0', '0', 'A/4. 39886', '7.8', '', 'S\n']
    ['53', '1', '1', '" Mrs. Henry Sleeper (Myna Haxtun) Harper"', 'female', '49', '1', '0', 'PC 17572', '76.7292', 'D33', 'C\n']
    ['54', '1', '2', '" Mrs. Lizzie (Elizabeth Anne Wilkinson) Faunthorpe"', 'female', '29', '1', '0', '2926', '26', '', 'S\n']
    ['55', '0', '1', '" Mr. Engelhart Cornelius Ostby"', 'male', '65', '0', '1', '113509', '61.9792', 'B30', 'C\n']
    ['56', '1', '1', '" Mr. Hugh Woolner"', 'male', '', '0', '0', '19947', '35.5', 'C52', 'S\n']
    ['57', '1', '2', '" Miss. Emily Rugg"', 'female', '21', '0', '0', 'C.A. 31026', '10.5', '', 'S\n']
    ['58', '0', '3', '" Mr. Mansouer Novel"', 'male', '28.5', '0', '0', '2697', '7.2292', '', 'C\n']
    ['59', '1', '2', '" Miss. Constance Mirium West"', 'female', '5', '1', '2', 'C.A. 34651', '27.75', '', 'S\n']
    ['60', '0', '3', '" Master. William Frederick Goodwin"', 'male', '11', '5', '2', 'CA 2144', '46.9', '', 'S\n']
    ['61', '0', '3', '" Mr. Orsen Sirayanian"', 'male', '22', '0', '0', '2669', '7.2292', '', 'C\n']
    ['62', '1', '1', '" Miss. Amelie Icard"', 'female', '38', '0', '0', '113572', '80', 'B28', '\n']
    ['63', '0', '1', '" Mr. Henry Birkhardt Harris"', 'male', '45', '1', '0', '36973', '83.475', 'C83', 'S\n']
    ['64', '0', '3', '" Master. Harald Skoog"', 'male', '4', '3', '2', '347088', '27.9', '', 'S\n']
    ['65', '0', '1', '" Mr. Albert A Stewart"', 'male', '', '0', '0', 'PC 17605', '27.7208', '', 'C\n']
    ['66', '1', '3', '" Master. Gerios Moubarek"', 'male', '', '1', '1', '2661', '15.2458', '', 'C\n']
    ['67', '1', '2', '" Mrs. (Elizabeth Ramell) Nye"', 'female', '29', '0', '0', 'C.A. 29395', '10.5', 'F33', 'S\n']
    ['68', '0', '3', '" Mr. Ernest James Crease"', 'male', '19', '0', '0', 'S.P. 3464', '8.1583', '', 'S\n']
    ['69', '1', '3', '" Miss. Erna Alexandra Andersson"', 'female', '17', '4', '2', '3101281', '7.925', '', 'S\n']
    ['70', '0', '3', '" Mr. Vincenz Kink"', 'male', '26', '2', '0', '315151', '8.6625', '', 'S\n']
    ['71', '0', '2', '" Mr. Stephen Curnow Jenkin"', 'male', '32', '0', '0', 'C.A. 33111', '10.5', '', 'S\n']
    ['72', '0', '3', '" Miss. Lillian Amy Goodwin"', 'female', '16', '5', '2', 'CA 2144', '46.9', '', 'S\n']
    ['73', '0', '2', '" Mr. Ambrose Jr Hood"', 'male', '21', '0', '0', 'S.O.C. 14879', '73.5', '', 'S\n']
    ['74', '0', '3', '" Mr. Apostolos Chronopoulos"', 'male', '26', '1', '0', '2680', '14.4542', '', 'C\n']
    ['75', '1', '3', '" Mr. Lee Bing"', 'male', '32', '0', '0', '1601', '56.4958', '', 'S\n']
    ['76', '0', '3', '" Mr. Sigurd Hansen Moen"', 'male', '25', '0', '0', '348123', '7.65', 'F G73', 'S\n']
    ['77', '0', '3', '" Mr. Ivan Staneff"', 'male', '', '0', '0', '349208', '7.8958', '', 'S\n']
    ['78', '0', '3', '" Mr. Rahamin Haim Moutal"', 'male', '', '0', '0', '374746', '8.05', '', 'S\n']
    ['79', '1', '2', '" Master. Alden Gates Caldwell"', 'male', '0.83', '0', '2', '248738', '29', '', 'S\n']
    ['80', '1', '3', '" Miss. Elizabeth Dowdell"', 'female', '30', '0', '0', '364516', '12.475', '', 'S\n']
    ['81', '0', '3', '" Mr. Achille Waelens"', 'male', '22', '0', '0', '345767', '9', '', 'S\n']
    ['82', '1', '3', '" Mr. Jan Baptist Sheerlinck"', 'male', '29', '0', '0', '345779', '9.5', '', 'S\n']
    ['83', '1', '3', '" Miss. Brigdet Delia McDermott"', 'female', '', '0', '0', '330932', '7.7875', '', 'Q\n']
    ['84', '0', '1', '" Mr. Francisco M Carrau"', 'male', '28', '0', '0', '113059', '47.1', '', 'S\n']
    ['85', '1', '2', '" Miss. Bertha Ilett"', 'female', '17', '0', '0', 'SO/C 14885', '10.5', '', 'S\n']
    ['86', '1', '3', '" Mrs. Karl Alfred (Maria Mathilda Gustafsson) Backstrom"', 'female', '33', '3', '0', '3101278', '15.85', '', 'S\n']
    ['87', '0', '3', '" Mr. William Neal Ford"', 'male', '16', '1', '3', 'W./C. 6608', '34.375', '', 'S\n']
    ['88', '0', '3', '" Mr. Selman Francis Slocovski"', 'male', '', '0', '0', 'SOTON/OQ 392086', '8.05', '', 'S\n']
    ['89', '1', '1', '" Miss. Mabel Helen Fortune"', 'female', '23', '3', '2', '19950', '263', 'C23 C25 C27', 'S\n']
    ['90', '0', '3', '" Mr. Francesco Celotti"', 'male', '24', '0', '0', '343275', '8.05', '', 'S\n']
    ['91', '0', '3', '" Mr. Emil Christmann"', 'male', '29', '0', '0', '343276', '8.05', '', 'S\n']
    ['92', '0', '3', '" Mr. Paul Edvin Andreasson"', 'male', '20', '0', '0', '347466', '7.8542', '', 'S\n']
    ['93', '0', '1', '" Mr. Herbert Fuller Chaffee"', 'male', '46', '1', '0', 'W.E.P. 5734', '61.175', 'E31', 'S\n']
    ['94', '0', '3', '" Mr. Bertram Frank Dean"', 'male', '26', '1', '2', 'C.A. 2315', '20.575', '', 'S\n']
    ['95', '0', '3', '" Mr. Daniel Coxon"', 'male', '59', '0', '0', '364500', '7.25', '', 'S\n']
    ['96', '0', '3', '" Mr. Charles Joseph Shorney"', 'male', '', '0', '0', '374910', '8.05', '', 'S\n']
    ['97', '0', '1', '" Mr. George B Goldschmidt"', 'male', '71', '0', '0', 'PC 17754', '34.6542', 'A5', 'C\n']
    ['98', '1', '1', '" Mr. William Bertram Greenfield"', 'male', '23', '0', '1', 'PC 17759', '63.3583', 'D10 D12', 'C\n']
    ['99', '1', '2', '" Mrs. John T (Ada Julia Bone) Doling"', 'female', '34', '0', '1', '231919', '23', '', 'S\n']
    ['100', '0', '2', '" Mr. Sinai Kantor"', 'male', '34', '1', '0', '244367', '26', '', 'S\n']
    ['101', '0', '3', '" Miss. Matilda Petranec"', 'female', '28', '0', '0', '349245', '7.8958', '', 'S\n']
    ['102', '0', '3', '" Mr. Pastcho (""Pentcho"") Petroff"', 'male', '', '0', '0', '349215', '7.8958', '', 'S\n']
    ['103', '0', '1', '" Mr. Richard Frasar White"', 'male', '21', '0', '1', '35281', '77.2875', 'D26', 'S\n']
    ['104', '0', '3', '" Mr. Gustaf Joel Johansson"', 'male', '33', '0', '0', '7540', '8.6542', '', 'S\n']
    ['105', '0', '3', '" Mr. Anders Vilhelm Gustafsson"', 'male', '37', '2', '0', '3101276', '7.925', '', 'S\n']
    ['106', '0', '3', '" Mr. Stoytcho Mionoff"', 'male', '28', '0', '0', '349207', '7.8958', '', 'S\n']
    ['107', '1', '3', '" Miss. Anna Kristine Salkjelsvik"', 'female', '21', '0', '0', '343120', '7.65', '', 'S\n']
    ['108', '1', '3', '" Mr. Albert Johan Moss"', 'male', '', '0', '0', '312991', '7.775', '', 'S\n']
    ['109', '0', '3', '" Mr. Tido Rekic"', 'male', '38', '0', '0', '349249', '7.8958', '', 'S\n']
    ['110', '1', '3', '" Miss. Bertha Moran"', 'female', '', '1', '0', '371110', '24.15', '', 'Q\n']
    ['111', '0', '1', '" Mr. Walter Chamberlain Porter"', 'male', '47', '0', '0', '110465', '52', 'C110', 'S\n']
    ['112', '0', '3', '" Miss. Hileni Zabour"', 'female', '14.5', '1', '0', '2665', '14.4542', '', 'C\n']
    ['113', '0', '3', '" Mr. David John Barton"', 'male', '22', '0', '0', '324669', '8.05', '', 'S\n']
    ['114', '0', '3', '" Miss. Katriina Jussila"', 'female', '20', '1', '0', '4136', '9.825', '', 'S\n']
    ['115', '0', '3', '" Miss. Malake Attalah"', 'female', '17', '0', '0', '2627', '14.4583', '', 'C\n']
    ['116', '0', '3', '" Mr. Edvard Pekoniemi"', 'male', '21', '0', '0', 'STON/O 2. 3101294', '7.925', '', 'S\n']
    ['117', '0', '3', '" Mr. Patrick Connors"', 'male', '70.5', '0', '0', '370369', '7.75', '', 'Q\n']
    ['118', '0', '2', '" Mr. William John Robert Turpin"', 'male', '29', '1', '0', '11668', '21', '', 'S\n']
    ['119', '0', '1', '" Mr. Quigg Edmond Baxter"', 'male', '24', '0', '1', 'PC 17558', '247.5208', 'B58 B60', 'C\n']
    ['120', '0', '3', '" Miss. Ellis Anna Maria Andersson"', 'female', '2', '4', '2', '347082', '31.275', '', 'S\n']
    ['121', '0', '2', '" Mr. Stanley George Hickman"', 'male', '21', '2', '0', 'S.O.C. 14879', '73.5', '', 'S\n']
    ['122', '0', '3', '" Mr. Leonard Charles Moore"', 'male', '', '0', '0', 'A4. 54510', '8.05', '', 'S\n']
    ['123', '0', '2', '" Mr. Nicholas Nasser"', 'male', '32.5', '1', '0', '237736', '30.0708', '', 'C\n']
    ['124', '1', '2', '" Miss. Susan Webber"', 'female', '32.5', '0', '0', '27267', '13', 'E101', 'S\n']
    ['125', '0', '1', '" Mr. Percival Wayland White"', 'male', '54', '0', '1', '35281', '77.2875', 'D26', 'S\n']
    ['126', '1', '3', '" Master. Elias Nicola-Yarred"', 'male', '12', '1', '0', '2651', '11.2417', '', 'C\n']
    ['127', '0', '3', '" Mr. Martin McMahon"', 'male', '', '0', '0', '370372', '7.75', '', 'Q\n']
    ['128', '1', '3', '" Mr. Fridtjof Arne Madsen"', 'male', '24', '0', '0', 'C 17369', '7.1417', '', 'S\n']
    ['129', '1', '3', '" Miss. Anna Peter"', 'female', '', '1', '1', '2668', '22.3583', 'F E69', 'C\n']
    ['130', '0', '3', '" Mr. Johan Ekstrom"', 'male', '45', '0', '0', '347061', '6.975', '', 'S\n']
    ['131', '0', '3', '" Mr. Jozef Drazenoic"', 'male', '33', '0', '0', '349241', '7.8958', '', 'C\n']
    ['132', '0', '3', '" Mr. Domingos Fernandeo Coelho"', 'male', '20', '0', '0', 'SOTON/O.Q. 3101307', '7.05', '', 'S\n']
    ['133', '0', '3', '" Mrs. Alexander A (Grace Charity Laury) Robins"', 'female', '47', '1', '0', 'A/5. 3337', '14.5', '', 'S\n']
    ['134', '1', '2', '" Mrs. Leopold (Mathilde Francoise Pede) Weisz"', 'female', '29', '1', '0', '228414', '26', '', 'S\n']
    ['135', '0', '2', '" Mr. Samuel James Hayden Sobey"', 'male', '25', '0', '0', 'C.A. 29178', '13', '', 'S\n']
    ['136', '0', '2', '" Mr. Emile Richard"', 'male', '23', '0', '0', 'SC/PARIS 2133', '15.0458', '', 'C\n']
    ['137', '1', '1', '" Miss. Helen Monypeny Newsom"', 'female', '19', '0', '2', '11752', '26.2833', 'D47', 'S\n']
    ['138', '0', '1', '" Mr. Jacques Heath Futrelle"', 'male', '37', '1', '0', '113803', '53.1', 'C123', 'S\n']
    ['139', '0', '3', '" Mr. Olaf Elon Osen"', 'male', '16', '0', '0', '7534', '9.2167', '', 'S\n']
    ['140', '0', '1', '" Mr. Victor Giglio"', 'male', '24', '0', '0', 'PC 17593', '79.2', 'B86', 'C\n']
    ['141', '0', '3', '" Mrs. Joseph (Sultana) Boulos"', 'female', '', '0', '2', '2678', '15.2458', '', 'C\n']
    ['142', '1', '3', '" Miss. Anna Sofia Nysten"', 'female', '22', '0', '0', '347081', '7.75', '', 'S\n']
    ['143', '1', '3', '" Mrs. Pekka Pietari (Elin Matilda Dolck) Hakkarainen"', 'female', '24', '1', '0', 'STON/O2. 3101279', '15.85', '', 'S\n']
    ['144', '0', '3', '" Mr. Jeremiah Burke"', 'male', '19', '0', '0', '365222', '6.75', '', 'Q\n']
    ['145', '0', '2', '" Mr. Edgardo Samuel Andrew"', 'male', '18', '0', '0', '231945', '11.5', '', 'S\n']
    ['146', '0', '2', '" Mr. Joseph Charles Nicholls"', 'male', '19', '1', '1', 'C.A. 33112', '36.75', '', 'S\n']
    ['147', '1', '3', '" Mr. August Edvard (""Wennerstrom"") Andersson"', 'male', '27', '0', '0', '350043', '7.7958', '', 'S\n']
    ['148', '0', '3', '" Miss. Robina Maggie ""Ruby"" Ford"', 'female', '9', '2', '2', 'W./C. 6608', '34.375', '', 'S\n']
    ['149', '0', '2', '" Mr. Michel (""Louis M Hoffman"") Navratil"', 'male', '36.5', '0', '2', '230080', '26', 'F2', 'S\n']
    ['150', '0', '2', '" Rev. Thomas Roussel Davids Byles"', 'male', '42', '0', '0', '244310', '13', '', 'S\n']
    ['151', '0', '2', '" Rev. Robert James Bateman"', 'male', '51', '0', '0', 'S.O.P. 1166', '12.525', '', 'S\n']
    ['152', '1', '1', '" Mrs. Thomas (Edith Wearne) Pears"', 'female', '22', '1', '0', '113776', '66.6', 'C2', 'S\n']
    ['153', '0', '3', '" Mr. Alfonzo Meo"', 'male', '55.5', '0', '0', 'A.5. 11206', '8.05', '', 'S\n']
    ['154', '0', '3', '" Mr. Austin Blyler van Billiard"', 'male', '40.5', '0', '2', 'A/5. 851', '14.5', '', 'S\n']
    ['155', '0', '3', '" Mr. Ole Martin Olsen"', 'male', '', '0', '0', 'Fa 265302', '7.3125', '', 'S\n']
    ['156', '0', '1', '" Mr. Charles Duane Williams"', 'male', '51', '0', '1', 'PC 17597', '61.3792', '', 'C\n']
    ['157', '1', '3', '" Miss. Katherine ""Katie"" Gilnagh"', 'female', '16', '0', '0', '35851', '7.7333', '', 'Q\n']
    ['158', '0', '3', '" Mr. Harry Corn"', 'male', '30', '0', '0', 'SOTON/OQ 392090', '8.05', '', 'S\n']
    ['159', '0', '3', '" Mr. Mile Smiljanic"', 'male', '', '0', '0', '315037', '8.6625', '', 'S\n']
    ['160', '0', '3', '" Master. Thomas Henry Sage"', 'male', '', '8', '2', 'CA. 2343', '69.55', '', 'S\n']
    ['161', '0', '3', '" Mr. John Hatfield Cribb"', 'male', '44', '0', '1', '371362', '16.1', '', 'S\n']
    ['162', '1', '2', '" Mrs. James (Elizabeth ""Bessie"" Inglis Milne) Watt"', 'female', '40', '0', '0', 'C.A. 33595', '15.75', '', 'S\n']
    ['163', '0', '3', '" Mr. John Viktor Bengtsson"', 'male', '26', '0', '0', '347068', '7.775', '', 'S\n']
    ['164', '0', '3', '" Mr. Jovo Calic"', 'male', '17', '0', '0', '315093', '8.6625', '', 'S\n']
    ['165', '0', '3', '" Master. Eino Viljami Panula"', 'male', '1', '4', '1', '3101295', '39.6875', '', 'S\n']
    ['166', '1', '3', '" Master. Frank John William ""Frankie"" Goldsmith"', 'male', '9', '0', '2', '363291', '20.525', '', 'S\n']
    ['167', '1', '1', '" Mrs. (Edith Martha Bowerman) Chibnall"', 'female', '', '0', '1', '113505', '55', 'E33', 'S\n']
    ['168', '0', '3', '" Mrs. William (Anna Bernhardina Karlsson) Skoog"', 'female', '45', '1', '4', '347088', '27.9', '', 'S\n']
    ['169', '0', '1', '" Mr. John D Baumann"', 'male', '', '0', '0', 'PC 17318', '25.925', '', 'S\n']
    ['170', '0', '3', '" Mr. Lee Ling"', 'male', '28', '0', '0', '1601', '56.4958', '', 'S\n']
    ['171', '0', '1', '" Mr. Wyckoff Van der hoef"', 'male', '61', '0', '0', '111240', '33.5', 'B19', 'S\n']
    ['172', '0', '3', '" Master. Arthur Rice"', 'male', '4', '4', '1', '382652', '29.125', '', 'Q\n']
    ['173', '1', '3', '" Miss. Eleanor Ileen Johnson"', 'female', '1', '1', '1', '347742', '11.1333', '', 'S\n']
    ['174', '0', '3', '" Mr. Antti Wilhelm Sivola"', 'male', '21', '0', '0', 'STON/O 2. 3101280', '7.925', '', 'S\n']
    ['175', '0', '1', '" Mr. James Clinch Smith"', 'male', '56', '0', '0', '17764', '30.6958', 'A7', 'C\n']
    ['176', '0', '3', '" Mr. Klas Albin Klasen"', 'male', '18', '1', '1', '350404', '7.8542', '', 'S\n']
    ['177', '0', '3', '" Master. Henry Forbes Lefebre"', 'male', '', '3', '1', '4133', '25.4667', '', 'S\n']
    ['178', '0', '1', '" Miss. Ann Elizabeth Isham"', 'female', '50', '0', '0', 'PC 17595', '28.7125', 'C49', 'C\n']
    ['179', '0', '2', '" Mr. Reginald Hale"', 'male', '30', '0', '0', '250653', '13', '', 'S\n']
    ['180', '0', '3', '" Mr. Lionel Leonard"', 'male', '36', '0', '0', 'LINE', '0', '', 'S\n']
    ['181', '0', '3', '" Miss. Constance Gladys Sage"', 'female', '', '8', '2', 'CA. 2343', '69.55', '', 'S\n']
    ['182', '0', '2', '" Mr. Rene Pernot"', 'male', '', '0', '0', 'SC/PARIS 2131', '15.05', '', 'C\n']
    ['183', '0', '3', '" Master. Clarence Gustaf Hugo Asplund"', 'male', '9', '4', '2', '347077', '31.3875', '', 'S\n']
    ['184', '1', '2', '" Master. Richard F Becker"', 'male', '1', '2', '1', '230136', '39', 'F4', 'S\n']
    ['185', '1', '3', '" Miss. Luise Gretchen Kink-Heilmann"', 'female', '4', '0', '2', '315153', '22.025', '', 'S\n']
    ['186', '0', '1', '" Mr. Hugh Roscoe Rood"', 'male', '', '0', '0', '113767', '50', 'A32', 'S\n']
    ['187', '1', '3', '" Mrs. Thomas (Johanna ""Hannah"" Godfrey) O\'Brien"', 'female', '', '1', '0', '370365', '15.5', '', 'Q\n']
    ['188', '1', '1', '" Mr. Charles Hallace (""Mr C Rolmane"") Romaine"', 'male', '45', '0', '0', '111428', '26.55', '', 'S\n']
    ['189', '0', '3', '" Mr. John Bourke"', 'male', '40', '1', '1', '364849', '15.5', '', 'Q\n']
    ['190', '0', '3', '" Mr. Stjepan Turcin"', 'male', '36', '0', '0', '349247', '7.8958', '', 'S\n']
    ['191', '1', '2', '" Mrs. (Rosa) Pinsky"', 'female', '32', '0', '0', '234604', '13', '', 'S\n']
    ['192', '0', '2', '" Mr. William Carbines"', 'male', '19', '0', '0', '28424', '13', '', 'S\n']
    ['193', '1', '3', '" Miss. Carla Christine Nielsine Andersen-Jensen"', 'female', '19', '1', '0', '350046', '7.8542', '', 'S\n']
    ['194', '1', '2', '" Master. Michel M Navratil"', 'male', '3', '1', '1', '230080', '26', 'F2', 'S\n']
    ['195', '1', '1', '" Mrs. James Joseph (Margaret Tobin) Brown"', 'female', '44', '0', '0', 'PC 17610', '27.7208', 'B4', 'C\n']
    ['196', '1', '1', '" Miss. Elise Lurette"', 'female', '58', '0', '0', 'PC 17569', '146.5208', 'B80', 'C\n']
    ['197', '0', '3', '" Mr. Robert Mernagh"', 'male', '', '0', '0', '368703', '7.75', '', 'Q\n']
    ['198', '0', '3', '" Mr. Karl Siegwart Andreas Olsen"', 'male', '42', '0', '1', '4579', '8.4042', '', 'S\n']
    ['199', '1', '3', '" Miss. Margaret ""Maggie"" Madigan"', 'female', '', '0', '0', '370370', '7.75', '', 'Q\n']
    ['200', '0', '2', '" Miss. Henriette (""Mrs Harbeck"") Yrois"', 'female', '24', '0', '0', '248747', '13', '', 'S\n']
    ['201', '0', '3', '" Mr. Nestor Cyriel Vande Walle"', 'male', '28', '0', '0', '345770', '9.5', '', 'S\n']
    ['202', '0', '3', '" Mr. Frederick Sage"', 'male', '', '8', '2', 'CA. 2343', '69.55', '', 'S\n']
    ['203', '0', '3', '" Mr. Jakob Alfred Johanson"', 'male', '34', '0', '0', '3101264', '6.4958', '', 'S\n']
    ['204', '0', '3', '" Mr. Gerious Youseff"', 'male', '45.5', '0', '0', '2628', '7.225', '', 'C\n']
    ['205', '1', '3', '" Mr. Gurshon ""Gus"" Cohen"', 'male', '18', '0', '0', 'A/5 3540', '8.05', '', 'S\n']
    ['206', '0', '3', '" Miss. Telma Matilda Strom"', 'female', '2', '0', '1', '347054', '10.4625', 'G6', 'S\n']
    ['207', '0', '3', '" Mr. Karl Alfred Backstrom"', 'male', '32', '1', '0', '3101278', '15.85', '', 'S\n']
    ['208', '1', '3', '" Mr. Nassef Cassem Albimona"', 'male', '26', '0', '0', '2699', '18.7875', '', 'C\n']
    ['209', '1', '3', '" Miss. Helen ""Ellen"" Carr"', 'female', '16', '0', '0', '367231', '7.75', '', 'Q\n']
    ['210', '1', '1', '" Mr. Henry Blank"', 'male', '40', '0', '0', '112277', '31', 'A31', 'C\n']
    ['211', '0', '3', '" Mr. Ahmed Ali"', 'male', '24', '0', '0', 'SOTON/O.Q. 3101311', '7.05', '', 'S\n']
    ['212', '1', '2', '" Miss. Clear Annie Cameron"', 'female', '35', '0', '0', 'F.C.C. 13528', '21', '', 'S\n']
    ['213', '0', '3', '" Mr. John Henry Perkin"', 'male', '22', '0', '0', 'A/5 21174', '7.25', '', 'S\n']
    ['214', '0', '2', '" Mr. Hans Kristensen Givard"', 'male', '30', '0', '0', '250646', '13', '', 'S\n']
    ['215', '0', '3', '" Mr. Philip Kiernan"', 'male', '', '1', '0', '367229', '7.75', '', 'Q\n']
    ['216', '1', '1', '" Miss. Madeleine Newell"', 'female', '31', '1', '0', '35273', '113.275', 'D36', 'C\n']
    ['217', '1', '3', '" Miss. Eliina Honkanen"', 'female', '27', '0', '0', 'STON/O2. 3101283', '7.925', '', 'S\n']
    ['218', '0', '2', '" Mr. Sidney Samuel Jacobsohn"', 'male', '42', '1', '0', '243847', '27', '', 'S\n']
    ['219', '1', '1', '" Miss. Albina Bazzani"', 'female', '32', '0', '0', '11813', '76.2917', 'D15', 'C\n']
    ['220', '0', '2', '" Mr. Walter Harris"', 'male', '30', '0', '0', 'W/C 14208', '10.5', '', 'S\n']
    ['221', '1', '3', '" Mr. Victor Francis Sunderland"', 'male', '16', '0', '0', 'SOTON/OQ 392089', '8.05', '', 'S\n']
    ['222', '0', '2', '" Mr. James H Bracken"', 'male', '27', '0', '0', '220367', '13', '', 'S\n']
    ['223', '0', '3', '" Mr. George Henry Green"', 'male', '51', '0', '0', '21440', '8.05', '', 'S\n']
    ['224', '0', '3', '" Mr. Christo Nenkoff"', 'male', '', '0', '0', '349234', '7.8958', '', 'S\n']
    ['225', '1', '1', '" Mr. Frederick Maxfield Hoyt"', 'male', '38', '1', '0', '19943', '90', 'C93', 'S\n']
    ['226', '0', '3', '" Mr. Karl Ivar Sven Berglund"', 'male', '22', '0', '0', 'PP 4348', '9.35', '', 'S\n']
    ['227', '1', '2', '" Mr. William John Mellors"', 'male', '19', '0', '0', 'SW/PP 751', '10.5', '', 'S\n']
    ['228', '0', '3', '" Mr. John Hall (""Henry"") Lovell"', 'male', '20.5', '0', '0', 'A/5 21173', '7.25', '', 'S\n']
    ['229', '0', '2', '" Mr. Arne Jonas Fahlstrom"', 'male', '18', '0', '0', '236171', '13', '', 'S\n']
    ['230', '0', '3', '" Miss. Mathilde Lefebre"', 'female', '', '3', '1', '4133', '25.4667', '', 'S\n']
    ['231', '1', '1', '" Mrs. Henry Birkhardt (Irene Wallach) Harris"', 'female', '35', '1', '0', '36973', '83.475', 'C83', 'S\n']
    ['232', '0', '3', '" Mr. Bengt Edvin Larsson"', 'male', '29', '0', '0', '347067', '7.775', '', 'S\n']
    ['233', '0', '2', '" Mr. Ernst Adolf Sjostedt"', 'male', '59', '0', '0', '237442', '13.5', '', 'S\n']
    ['234', '1', '3', '" Miss. Lillian Gertrud Asplund"', 'female', '5', '4', '2', '347077', '31.3875', '', 'S\n']
    ['235', '0', '2', '" Mr. Robert William Norman Leyson"', 'male', '24', '0', '0', 'C.A. 29566', '10.5', '', 'S\n']
    ['236', '0', '3', '" Miss. Alice Phoebe Harknett"', 'female', '', '0', '0', 'W./C. 6609', '7.55', '', 'S\n']
    ['237', '0', '2', '" Mr. Stephen Hold"', 'male', '44', '1', '0', '26707', '26', '', 'S\n']
    ['238', '1', '2', '" Miss. Marjorie ""Lottie"" Collyer"', 'female', '8', '0', '2', 'C.A. 31921', '26.25', '', 'S\n']
    ['239', '0', '2', '" Mr. Frederick William Pengelly"', 'male', '19', '0', '0', '28665', '10.5', '', 'S\n']
    ['240', '0', '2', '" Mr. George Henry Hunt"', 'male', '33', '0', '0', 'SCO/W 1585', '12.275', '', 'S\n']
    ['241', '0', '3', '" Miss. Thamine Zabour"', 'female', '', '1', '0', '2665', '14.4542', '', 'C\n']
    ['242', '1', '3', '" Miss. Katherine ""Kate"" Murphy"', 'female', '', '1', '0', '367230', '15.5', '', 'Q\n']
    ['243', '0', '2', '" Mr. Reginald Charles Coleridge"', 'male', '29', '0', '0', 'W./C. 14263', '10.5', '', 'S\n']
    ['244', '0', '3', '" Mr. Matti Alexanteri Maenpaa"', 'male', '22', '0', '0', 'STON/O 2. 3101275', '7.125', '', 'S\n']
    ['245', '0', '3', '" Mr. Sleiman Attalah"', 'male', '30', '0', '0', '2694', '7.225', '', 'C\n']
    ['246', '0', '1', '" Dr. William Edward Minahan"', 'male', '44', '2', '0', '19928', '90', 'C78', 'Q\n']
    ['247', '0', '3', '" Miss. Agda Thorilda Viktoria Lindahl"', 'female', '25', '0', '0', '347071', '7.775', '', 'S\n']
    ['248', '1', '2', '" Mrs. William (Anna) Hamalainen"', 'female', '24', '0', '2', '250649', '14.5', '', 'S\n']
    ['249', '1', '1', '" Mr. Richard Leonard Beckwith"', 'male', '37', '1', '1', '11751', '52.5542', 'D35', 'S\n']
    ['250', '0', '2', '" Rev. Ernest Courtenay Carter"', 'male', '54', '1', '0', '244252', '26', '', 'S\n']
    ['251', '0', '3', '" Mr. James George Reed"', 'male', '', '0', '0', '362316', '7.25', '', 'S\n']
    ['252', '0', '3', '" Mrs. Wilhelm (Elna Matilda Persson) Strom"', 'female', '29', '1', '1', '347054', '10.4625', 'G6', 'S\n']
    ['253', '0', '1', '" Mr. William Thomas Stead"', 'male', '62', '0', '0', '113514', '26.55', 'C87', 'S\n']
    ['254', '0', '3', '" Mr. William Arthur Lobb"', 'male', '30', '1', '0', 'A/5. 3336', '16.1', '', 'S\n']
    ['255', '0', '3', '" Mrs. Viktor (Helena Wilhelmina) Rosblom"', 'female', '41', '0', '2', '370129', '20.2125', '', 'S\n']
    ['256', '1', '3', '" Mrs. Darwis (Hanne Youssef Razi) Touma"', 'female', '29', '0', '2', '2650', '15.2458', '', 'C\n']
    ['257', '1', '1', '" Mrs. Gertrude Maybelle Thorne"', 'female', '', '0', '0', 'PC 17585', '79.2', '', 'C\n']
    ['258', '1', '1', '" Miss. Gladys Cherry"', 'female', '30', '0', '0', '110152', '86.5', 'B77', 'S\n']
    ['259', '1', '1', '" Miss. Anna Ward"', 'female', '35', '0', '0', 'PC 17755', '512.3292', '', 'C\n']
    ['260', '1', '2', '" Mrs. (Lutie Davis) Parrish"', 'female', '50', '0', '1', '230433', '26', '', 'S\n']
    ['261', '0', '3', '" Mr. Thomas Smith"', 'male', '', '0', '0', '384461', '7.75', '', 'Q\n']
    ['262', '1', '3', '" Master. Edvin Rojj Felix Asplund"', 'male', '3', '4', '2', '347077', '31.3875', '', 'S\n']
    ['263', '0', '1', '" Mr. Emil Taussig"', 'male', '52', '1', '1', '110413', '79.65', 'E67', 'S\n']
    ['264', '0', '1', '" Mr. William Harrison"', 'male', '40', '0', '0', '112059', '0', 'B94', 'S\n']
    ['265', '0', '3', '" Miss. Delia Henry"', 'female', '', '0', '0', '382649', '7.75', '', 'Q\n']
    ['266', '0', '2', '" Mr. David Reeves"', 'male', '36', '0', '0', 'C.A. 17248', '10.5', '', 'S\n']
    ['267', '0', '3', '" Mr. Ernesti Arvid Panula"', 'male', '16', '4', '1', '3101295', '39.6875', '', 'S\n']
    ['268', '1', '3', '" Mr. Ernst Ulrik Persson"', 'male', '25', '1', '0', '347083', '7.775', '', 'S\n']
    ['269', '1', '1', '" Mrs. William Thompson (Edith Junkins) Graham"', 'female', '58', '0', '1', 'PC 17582', '153.4625', 'C125', 'S\n']
    ['270', '1', '1', '" Miss. Amelia Bissette"', 'female', '35', '0', '0', 'PC 17760', '135.6333', 'C99', 'S\n']
    ['271', '0', '1', '" Mr. Alexander Cairns"', 'male', '', '0', '0', '113798', '31', '', 'S\n']
    ['272', '1', '3', '" Mr. William Henry Tornquist"', 'male', '25', '0', '0', 'LINE', '0', '', 'S\n']
    ['273', '1', '2', '" Mrs. (Elizabeth Anne Maidment) Mellinger"', 'female', '41', '0', '1', '250644', '19.5', '', 'S\n']
    ['274', '0', '1', '" Mr. Charles H Natsch"', 'male', '37', '0', '1', 'PC 17596', '29.7', 'C118', 'C\n']
    ['275', '1', '3', '" Miss. Hanora ""Nora"" Healy"', 'female', '', '0', '0', '370375', '7.75', '', 'Q\n']
    ['276', '1', '1', '" Miss. Kornelia Theodosia Andrews"', 'female', '63', '1', '0', '13502', '77.9583', 'D7', 'S\n']
    ['277', '0', '3', '" Miss. Augusta Charlotta Lindblom"', 'female', '45', '0', '0', '347073', '7.75', '', 'S\n']
    ['278', '0', '2', '" Mr. Francis ""Frank"" Parkes"', 'male', '', '0', '0', '239853', '0', '', 'S\n']
    ['279', '0', '3', '" Master. Eric Rice"', 'male', '7', '4', '1', '382652', '29.125', '', 'Q\n']
    ['280', '1', '3', '" Mrs. Stanton (Rosa Hunt) Abbott"', 'female', '35', '1', '1', 'C.A. 2673', '20.25', '', 'S\n']
    ['281', '0', '3', '" Mr. Frank Duane"', 'male', '65', '0', '0', '336439', '7.75', '', 'Q\n']
    ['282', '0', '3', '" Mr. Nils Johan Goransson Olsson"', 'male', '28', '0', '0', '347464', '7.8542', '', 'S\n']
    ['283', '0', '3', '" Mr. Alfons de Pelsmaeker"', 'male', '16', '0', '0', '345778', '9.5', '', 'S\n']
    ['284', '1', '3', '" Mr. Edward Arthur Dorking"', 'male', '19', '0', '0', 'A/5. 10482', '8.05', '', 'S\n']
    ['285', '0', '1', '" Mr. Richard William Smith"', 'male', '', '0', '0', '113056', '26', 'A19', 'S\n']
    ['286', '0', '3', '" Mr. Ivan Stankovic"', 'male', '33', '0', '0', '349239', '8.6625', '', 'C\n']
    ['287', '1', '3', '" Mr. Theodore de Mulder"', 'male', '30', '0', '0', '345774', '9.5', '', 'S\n']
    ['288', '0', '3', '" Mr. Penko Naidenoff"', 'male', '22', '0', '0', '349206', '7.8958', '', 'S\n']
    ['289', '1', '2', '" Mr. Masabumi Hosono"', 'male', '42', '0', '0', '237798', '13', '', 'S\n']
    ['290', '1', '3', '" Miss. Kate Connolly"', 'female', '22', '0', '0', '370373', '7.75', '', 'Q\n']
    ['291', '1', '1', '" Miss. Ellen ""Nellie"" Barber"', 'female', '26', '0', '0', '19877', '78.85', '', 'S\n']
    ['292', '1', '1', '" Mrs. Dickinson H (Helen Walton) Bishop"', 'female', '19', '1', '0', '11967', '91.0792', 'B49', 'C\n']
    ['293', '0', '2', '" Mr. Rene Jacques Levy"', 'male', '36', '0', '0', 'SC/Paris 2163', '12.875', 'D', 'C\n']
    ['294', '0', '3', '" Miss. Aloisia Haas"', 'female', '24', '0', '0', '349236', '8.85', '', 'S\n']
    ['295', '0', '3', '" Mr. Ivan Mineff"', 'male', '24', '0', '0', '349233', '7.8958', '', 'S\n']
    ['296', '0', '1', '" Mr. Ervin G Lewy"', 'male', '', '0', '0', 'PC 17612', '27.7208', '', 'C\n']
    ['297', '0', '3', '" Mr. Mansour Hanna"', 'male', '23.5', '0', '0', '2693', '7.2292', '', 'C\n']
    ['298', '0', '1', '" Miss. Helen Loraine Allison"', 'female', '2', '1', '2', '113781', '151.55', 'C22 C26', 'S\n']
    ['299', '1', '1', '" Mr. Adolphe Saalfeld"', 'male', '', '0', '0', '19988', '30.5', 'C106', 'S\n']
    ['300', '1', '1', '" Mrs. James (Helene DeLaudeniere Chaput) Baxter"', 'female', '50', '0', '1', 'PC 17558', '247.5208', 'B58 B60', 'C\n']
    ['301', '1', '3', '" Miss. Anna Katherine ""Annie Kate"" Kelly"', 'female', '', '0', '0', '9234', '7.75', '', 'Q\n']
    ['302', '1', '3', '" Mr. Bernard McCoy"', 'male', '', '2', '0', '367226', '23.25', '', 'Q\n']
    ['303', '0', '3', '" Mr. William Cahoone Jr Johnson"', 'male', '19', '0', '0', 'LINE', '0', '', 'S\n']
    ['304', '1', '2', '" Miss. Nora A Keane"', 'female', '', '0', '0', '226593', '12.35', 'E101', 'Q\n']
    ['305', '0', '3', '" Mr. Howard Hugh ""Harry"" Williams"', 'male', '', '0', '0', 'A/5 2466', '8.05', '', 'S\n']
    ['306', '1', '1', '" Master. Hudson Trevor Allison"', 'male', '0.92', '1', '2', '113781', '151.55', 'C22 C26', 'S\n']
    ['307', '1', '1', '" Miss. Margaret Fleming"', 'female', '', '0', '0', '17421', '110.8833', '', 'C\n']
    ['308', '1', '1', '" Mrs. Victor de Satode (Maria Josefa Perez de Soto y Vallejo) Penasco y Castellana"', 'female', '17', '1', '0', 'PC 17758', '108.9', 'C65', 'C\n']
    ['309', '0', '2', '" Mr. Samuel Abelson"', 'male', '30', '1', '0', 'P/PP 3381', '24', '', 'C\n']
    ['310', '1', '1', '" Miss. Laura Mabel Francatelli"', 'female', '30', '0', '0', 'PC 17485', '56.9292', 'E36', 'C\n']
    ['311', '1', '1', '" Miss. Margaret Bechstein Hays"', 'female', '24', '0', '0', '11767', '83.1583', 'C54', 'C\n']
    ['312', '1', '1', '" Miss. Emily Borie Ryerson"', 'female', '18', '2', '2', 'PC 17608', '262.375', 'B57 B59 B63 B66', 'C\n']
    ['313', '0', '2', '" Mrs. William (Anna Sylfven) Lahtinen"', 'female', '26', '1', '1', '250651', '26', '', 'S\n']
    ['314', '0', '3', '" Mr. Ignjac Hendekovic"', 'male', '28', '0', '0', '349243', '7.8958', '', 'S\n']
    ['315', '0', '2', '" Mr. Benjamin Hart"', 'male', '43', '1', '1', 'F.C.C. 13529', '26.25', '', 'S\n']
    ['316', '1', '3', '" Miss. Helmina Josefina Nilsson"', 'female', '26', '0', '0', '347470', '7.8542', '', 'S\n']
    ['317', '1', '2', '" Mrs. Sinai (Miriam Sternin) Kantor"', 'female', '24', '1', '0', '244367', '26', '', 'S\n']
    ['318', '0', '2', '" Dr. Ernest Moraweck"', 'male', '54', '0', '0', '29011', '14', '', 'S\n']
    ['319', '1', '1', '" Miss. Mary Natalie Wick"', 'female', '31', '0', '2', '36928', '164.8667', 'C7', 'S\n']
    ['320', '1', '1', '" Mrs. Frederic Oakley (Margaretta Corning Stone) Spedden"', 'female', '40', '1', '1', '16966', '134.5', 'E34', 'C\n']
    ['321', '0', '3', '" Mr. Samuel Dennis"', 'male', '22', '0', '0', 'A/5 21172', '7.25', '', 'S\n']
    ['322', '0', '3', '" Mr. Yoto Danoff"', 'male', '27', '0', '0', '349219', '7.8958', '', 'S\n']
    ['323', '1', '2', '" Miss. Hilda Mary Slayter"', 'female', '30', '0', '0', '234818', '12.35', '', 'Q\n']
    ['324', '1', '2', '" Mrs. Albert Francis (Sylvia Mae Harbaugh) Caldwell"', 'female', '22', '1', '1', '248738', '29', '', 'S\n']
    ['325', '0', '3', '" Mr. George John Jr Sage"', 'male', '', '8', '2', 'CA. 2343', '69.55', '', 'S\n']
    ['326', '1', '1', '" Miss. Marie Grice Young"', 'female', '36', '0', '0', 'PC 17760', '135.6333', 'C32', 'C\n']
    ['327', '0', '3', '" Mr. Johan Hansen Nysveen"', 'male', '61', '0', '0', '345364', '6.2375', '', 'S\n']
    ['328', '1', '2', '" Mrs. (Ada E Hall) Ball"', 'female', '36', '0', '0', '28551', '13', 'D', 'S\n']
    ['329', '1', '3', '" Mrs. Frank John (Emily Alice Brown) Goldsmith"', 'female', '31', '1', '1', '363291', '20.525', '', 'S\n']
    ['330', '1', '1', '" Miss. Jean Gertrude Hippach"', 'female', '16', '0', '1', '111361', '57.9792', 'B18', 'C\n']
    ['331', '1', '3', '" Miss. Agnes McCoy"', 'female', '', '2', '0', '367226', '23.25', '', 'Q\n']
    ['332', '0', '1', '" Mr. Austen Partner"', 'male', '45.5', '0', '0', '113043', '28.5', 'C124', 'S\n']
    ['333', '0', '1', '" Mr. George Edward Graham"', 'male', '38', '0', '1', 'PC 17582', '153.4625', 'C91', 'S\n']
    ['334', '0', '3', '" Mr. Leo Edmondus Vander Planke"', 'male', '16', '2', '0', '345764', '18', '', 'S\n']
    ['335', '1', '1', '" Mrs. Henry William (Clara Heinsheimer) Frauenthal"', 'female', '', '1', '0', 'PC 17611', '133.65', '', 'S\n']
    ['336', '0', '3', '" Mr. Mitto Denkoff"', 'male', '', '0', '0', '349225', '7.8958', '', 'S\n']
    ['337', '0', '1', '" Mr. Thomas Clinton Pears"', 'male', '29', '1', '0', '113776', '66.6', 'C2', 'S\n']
    ['338', '1', '1', '" Miss. Elizabeth Margaret Burns"', 'female', '41', '0', '0', '16966', '134.5', 'E40', 'C\n']
    ['339', '1', '3', '" Mr. Karl Edwart Dahl"', 'male', '45', '0', '0', '7598', '8.05', '', 'S\n']
    ['340', '0', '1', '" Mr. Stephen Weart Blackwell"', 'male', '45', '0', '0', '113784', '35.5', 'T', 'S\n']
    ['341', '1', '2', '" Master. Edmond Roger Navratil"', 'male', '2', '1', '1', '230080', '26', 'F2', 'S\n']
    ['342', '1', '1', '" Miss. Alice Elizabeth Fortune"', 'female', '24', '3', '2', '19950', '263', 'C23 C25 C27', 'S\n']
    ['343', '0', '2', '" Mr. Erik Gustaf Collander"', 'male', '28', '0', '0', '248740', '13', '', 'S\n']
    ['344', '0', '2', '" Mr. Charles Frederick Waddington Sedgwick"', 'male', '25', '0', '0', '244361', '13', '', 'S\n']
    ['345', '0', '2', '" Mr. Stanley Hubert Fox"', 'male', '36', '0', '0', '229236', '13', '', 'S\n']
    ['346', '1', '2', '" Miss. Amelia ""Mildred"" Brown"', 'female', '24', '0', '0', '248733', '13', 'F33', 'S\n']
    ['347', '1', '2', '" Miss. Marion Elsie Smith"', 'female', '40', '0', '0', '31418', '13', '', 'S\n']
    ['348', '1', '3', '" Mrs. Thomas Henry (Mary E Finck) Davison"', 'female', '', '1', '0', '386525', '16.1', '', 'S\n']
    ['349', '1', '3', '" Master. William Loch ""William"" Coutts"', 'male', '3', '1', '1', 'C.A. 37671', '15.9', '', 'S\n']
    ['350', '0', '3', '" Mr. Jovan Dimic"', 'male', '42', '0', '0', '315088', '8.6625', '', 'S\n']
    ['351', '0', '3', '" Mr. Nils Martin Odahl"', 'male', '23', '0', '0', '7267', '9.225', '', 'S\n']
    ['352', '0', '1', '" Mr. Fletcher Fellows Williams-Lambert"', 'male', '', '0', '0', '113510', '35', 'C128', 'S\n']
    ['353', '0', '3', '" Mr. Tannous Elias"', 'male', '15', '1', '1', '2695', '7.2292', '', 'C\n']
    ['354', '0', '3', '" Mr. Josef Arnold-Franchi"', 'male', '25', '1', '0', '349237', '17.8', '', 'S\n']
    ['355', '0', '3', '" Mr. Wazli Yousif"', 'male', '', '0', '0', '2647', '7.225', '', 'C\n']
    ['356', '0', '3', '" Mr. Leo Peter Vanden Steen"', 'male', '28', '0', '0', '345783', '9.5', '', 'S\n']
    ['357', '1', '1', '" Miss. Elsie Edith Bowerman"', 'female', '22', '0', '1', '113505', '55', 'E33', 'S\n']
    ['358', '0', '2', '" Miss. Annie Clemmer Funk"', 'female', '38', '0', '0', '237671', '13', '', 'S\n']
    ['359', '1', '3', '" Miss. Mary McGovern"', 'female', '', '0', '0', '330931', '7.8792', '', 'Q\n']
    ['360', '1', '3', '" Miss. Helen Mary ""Ellie"" Mockler"', 'female', '', '0', '0', '330980', '7.8792', '', 'Q\n']
    ['361', '0', '3', '" Mr. Wilhelm Skoog"', 'male', '40', '1', '4', '347088', '27.9', '', 'S\n']
    ['362', '0', '2', '" Mr. Sebastiano del Carlo"', 'male', '29', '1', '0', 'SC/PARIS 2167', '27.7208', '', 'C\n']
    ['363', '0', '3', '" Mrs. (Catherine David) Barbara"', 'female', '45', '0', '1', '2691', '14.4542', '', 'C\n']
    ['364', '0', '3', '" Mr. Adola Asim"', 'male', '35', '0', '0', 'SOTON/O.Q. 3101310', '7.05', '', 'S\n']
    ['365', '0', '3', '" Mr. Thomas O\'Brien"', 'male', '', '1', '0', '370365', '15.5', '', 'Q\n']
    ['366', '0', '3', '" Mr. Mauritz Nils Martin Adahl"', 'male', '30', '0', '0', 'C 7076', '7.25', '', 'S\n']
    ['367', '1', '1', '" Mrs. Frank Manley (Anna Sophia Atkinson) Warren"', 'female', '60', '1', '0', '110813', '75.25', 'D37', 'C\n']
    ['368', '1', '3', '" Mrs. (Mantoura Boulos) Moussa"', 'female', '', '0', '0', '2626', '7.2292', '', 'C\n']
    ['369', '1', '3', '" Miss. Annie Jermyn"', 'female', '', '0', '0', '14313', '7.75', '', 'Q\n']
    ['370', '1', '1', '" Mme. Leontine Pauline Aubart"', 'female', '24', '0', '0', 'PC 17477', '69.3', 'B35', 'C\n']
    ['371', '1', '1', '" Mr. George Achilles Harder"', 'male', '25', '1', '0', '11765', '55.4417', 'E50', 'C\n']
    ['372', '0', '3', '" Mr. Jakob Alfred Wiklund"', 'male', '18', '1', '0', '3101267', '6.4958', '', 'S\n']
    ['373', '0', '3', '" Mr. William Thomas Beavan"', 'male', '19', '0', '0', '323951', '8.05', '', 'S\n']
    ['374', '0', '1', '" Mr. Sante Ringhini"', 'male', '22', '0', '0', 'PC 17760', '135.6333', '', 'C\n']
    ['375', '0', '3', '" Miss. Stina Viola Palsson"', 'female', '3', '3', '1', '349909', '21.075', '', 'S\n']
    ['376', '1', '1', '" Mrs. Edgar Joseph (Leila Saks) Meyer"', 'female', '', '1', '0', 'PC 17604', '82.1708', '', 'C\n']
    ['377', '1', '3', '" Miss. Aurora Adelia Landergren"', 'female', '22', '0', '0', 'C 7077', '7.25', '', 'S\n']
    ['378', '0', '1', '" Mr. Harry Elkins Widener"', 'male', '27', '0', '2', '113503', '211.5', 'C82', 'C\n']
    ['379', '0', '3', '" Mr. Tannous Betros"', 'male', '20', '0', '0', '2648', '4.0125', '', 'C\n']
    ['380', '0', '3', '" Mr. Karl Gideon Gustafsson"', 'male', '19', '0', '0', '347069', '7.775', '', 'S\n']
    ['381', '1', '1', '" Miss. Rosalie Bidois"', 'female', '42', '0', '0', 'PC 17757', '227.525', '', 'C\n']
    ['382', '1', '3', '" Miss. Maria (""Mary"") Nakid"', 'female', '1', '0', '2', '2653', '15.7417', '', 'C\n']
    ['383', '0', '3', '" Mr. Juho Tikkanen"', 'male', '32', '0', '0', 'STON/O 2. 3101293', '7.925', '', 'S\n']
    ['384', '1', '1', '" Mrs. Alexander Oskar (Mary Aline Towner) Holverson"', 'female', '35', '1', '0', '113789', '52', '', 'S\n']
    ['385', '0', '3', '" Mr. Vasil Plotcharsky"', 'male', '', '0', '0', '349227', '7.8958', '', 'S\n']
    ['386', '0', '2', '" Mr. Charles Henry Davies"', 'male', '18', '0', '0', 'S.O.C. 14879', '73.5', '', 'S\n']
    ['387', '0', '3', '" Master. Sidney Leonard Goodwin"', 'male', '1', '5', '2', 'CA 2144', '46.9', '', 'S\n']
    ['388', '1', '2', '" Miss. Kate Buss"', 'female', '36', '0', '0', '27849', '13', '', 'S\n']
    ['389', '0', '3', '" Mr. Matthew Sadlier"', 'male', '', '0', '0', '367655', '7.7292', '', 'Q\n']
    ['390', '1', '2', '" Miss. Bertha Lehmann"', 'female', '17', '0', '0', 'SC 1748', '12', '', 'C\n']
    ['391', '1', '1', '" Mr. William Ernest Carter"', 'male', '36', '1', '2', '113760', '120', 'B96 B98', 'S\n']
    ['392', '1', '3', '" Mr. Carl Olof Jansson"', 'male', '21', '0', '0', '350034', '7.7958', '', 'S\n']
    ['393', '0', '3', '" Mr. Johan Birger Gustafsson"', 'male', '28', '2', '0', '3101277', '7.925', '', 'S\n']
    ['394', '1', '1', '" Miss. Marjorie Newell"', 'female', '23', '1', '0', '35273', '113.275', 'D36', 'C\n']
    ['395', '1', '3', '" Mrs. Hjalmar (Agnes Charlotta Bengtsson) Sandstrom"', 'female', '24', '0', '2', 'PP 9549', '16.7', 'G6', 'S\n']
    ['396', '0', '3', '" Mr. Erik Johansson"', 'male', '22', '0', '0', '350052', '7.7958', '', 'S\n']
    ['397', '0', '3', '" Miss. Elina Olsson"', 'female', '31', '0', '0', '350407', '7.8542', '', 'S\n']
    ['398', '0', '2', '" Mr. Peter David McKane"', 'male', '46', '0', '0', '28403', '26', '', 'S\n']
    ['399', '0', '2', '" Dr. Alfred Pain"', 'male', '23', '0', '0', '244278', '10.5', '', 'S\n']
    ['400', '1', '2', '" Mrs. William H (Jessie L) Trout"', 'female', '28', '0', '0', '240929', '12.65', '', 'S\n']
    ['401', '1', '3', '" Mr. Juha Niskanen"', 'male', '39', '0', '0', 'STON/O 2. 3101289', '7.925', '', 'S\n']
    ['402', '0', '3', '" Mr. John Adams"', 'male', '26', '0', '0', '341826', '8.05', '', 'S\n']
    ['403', '0', '3', '" Miss. Mari Aina Jussila"', 'female', '21', '1', '0', '4137', '9.825', '', 'S\n']
    ['404', '0', '3', '" Mr. Pekka Pietari Hakkarainen"', 'male', '28', '1', '0', 'STON/O2. 3101279', '15.85', '', 'S\n']
    ['405', '0', '3', '" Miss. Marija Oreskovic"', 'female', '20', '0', '0', '315096', '8.6625', '', 'S\n']
    ['406', '0', '2', '" Mr. Shadrach Gale"', 'male', '34', '1', '0', '28664', '21', '', 'S\n']
    ['407', '0', '3', '" Mr. Carl/Charles Peter Widegren"', 'male', '51', '0', '0', '347064', '7.75', '', 'S\n']
    ['408', '1', '2', '" Master. William Rowe Richards"', 'male', '3', '1', '1', '29106', '18.75', '', 'S\n']
    ['409', '0', '3', '" Mr. Hans Martin Monsen Birkeland"', 'male', '21', '0', '0', '312992', '7.775', '', 'S\n']
    ['410', '0', '3', '" Miss. Ida Lefebre"', 'female', '', '3', '1', '4133', '25.4667', '', 'S\n']
    ['411', '0', '3', '" Mr. Todor Sdycoff"', 'male', '', '0', '0', '349222', '7.8958', '', 'S\n']
    ['412', '0', '3', '" Mr. Henry Hart"', 'male', '', '0', '0', '394140', '6.8583', '', 'Q\n']
    ['413', '1', '1', '" Miss. Daisy E Minahan"', 'female', '33', '1', '0', '19928', '90', 'C78', 'Q\n']
    ['414', '0', '2', '" Mr. Alfred Fleming Cunningham"', 'male', '', '0', '0', '239853', '0', '', 'S\n']
    ['415', '1', '3', '" Mr. Johan Julian Sundman"', 'male', '44', '0', '0', 'STON/O 2. 3101269', '7.925', '', 'S\n']
    ['416', '0', '3', '" Mrs. Thomas (Annie Louise Rowley) Meek"', 'female', '', '0', '0', '343095', '8.05', '', 'S\n']
    ['417', '1', '2', '" Mrs. James Vivian (Lulu Thorne Christian) Drew"', 'female', '34', '1', '1', '28220', '32.5', '', 'S\n']
    ['418', '1', '2', '" Miss. Lyyli Karoliina Silven"', 'female', '18', '0', '2', '250652', '13', '', 'S\n']
    ['419', '0', '2', '" Mr. William John Matthews"', 'male', '30', '0', '0', '28228', '13', '', 'S\n']
    ['420', '0', '3', '" Miss. Catharina Van Impe"', 'female', '10', '0', '2', '345773', '24.15', '', 'S\n']
    ['421', '0', '3', '" Mr. Stanio Gheorgheff"', 'male', '', '0', '0', '349254', '7.8958', '', 'C\n']
    ['422', '0', '3', '" Mr. David Charters"', 'male', '21', '0', '0', 'A/5. 13032', '7.7333', '', 'Q\n']
    ['423', '0', '3', '" Mr. Leo Zimmerman"', 'male', '29', '0', '0', '315082', '7.875', '', 'S\n']
    ['424', '0', '3', '" Mrs. Ernst Gilbert (Anna Sigrid Maria Brogren) Danbom"', 'female', '28', '1', '1', '347080', '14.4', '', 'S\n']
    ['425', '0', '3', '" Mr. Viktor Richard Rosblom"', 'male', '18', '1', '1', '370129', '20.2125', '', 'S\n']
    ['426', '0', '3', '" Mr. Phillippe Wiseman"', 'male', '', '0', '0', 'A/4. 34244', '7.25', '', 'S\n']
    ['427', '1', '2', '" Mrs. Charles V (Ada Maria Winfield) Clarke"', 'female', '28', '1', '0', '2003', '26', '', 'S\n']
    ['428', '1', '2', '" Miss. Kate Florence (""Mrs Kate Louise Phillips Marshall"") Phillips"', 'female', '19', '0', '0', '250655', '26', '', 'S\n']
    ['429', '0', '3', '" Mr. James Flynn"', 'male', '', '0', '0', '364851', '7.75', '', 'Q\n']
    ['430', '1', '3', '" Mr. Berk (Berk Trembisky) Pickard"', 'male', '32', '0', '0', 'SOTON/O.Q. 392078', '8.05', 'E10', 'S\n']
    ['431', '1', '1', '" Mr. Mauritz Hakan Bjornstrom-Steffansson"', 'male', '28', '0', '0', '110564', '26.55', 'C52', 'S\n']
    ['432', '1', '3', '" Mrs. Percival (Florence Kate White) Thorneycroft"', 'female', '', '1', '0', '376564', '16.1', '', 'S\n']
    ['433', '1', '2', '" Mrs. Charles Alexander (Alice Adelaide Slow) Louch"', 'female', '42', '1', '0', 'SC/AH 3085', '26', '', 'S\n']
    ['434', '0', '3', '" Mr. Nikolai Erland Kallio"', 'male', '17', '0', '0', 'STON/O 2. 3101274', '7.125', '', 'S\n']
    ['435', '0', '1', '" Mr. William Baird Silvey"', 'male', '50', '1', '0', '13507', '55.9', 'E44', 'S\n']
    ['436', '1', '1', '" Miss. Lucile Polk Carter"', 'female', '14', '1', '2', '113760', '120', 'B96 B98', 'S\n']
    ['437', '0', '3', '" Miss. Doolina Margaret ""Daisy"" Ford"', 'female', '21', '2', '2', 'W./C. 6608', '34.375', '', 'S\n']
    ['438', '1', '2', '" Mrs. Sidney (Emily Hocking) Richards"', 'female', '24', '2', '3', '29106', '18.75', '', 'S\n']
    ['439', '0', '1', '" Mr. Mark Fortune"', 'male', '64', '1', '4', '19950', '263', 'C23 C25 C27', 'S\n']
    ['440', '0', '2', '" Mr. Johan Henrik Johannesson Kvillner"', 'male', '31', '0', '0', 'C.A. 18723', '10.5', '', 'S\n']
    ['441', '1', '2', '" Mrs. Benjamin (Esther Ada Bloomfield) Hart"', 'female', '45', '1', '1', 'F.C.C. 13529', '26.25', '', 'S\n']
    ['442', '0', '3', '" Mr. Leon Hampe"', 'male', '20', '0', '0', '345769', '9.5', '', 'S\n']
    ['443', '0', '3', '" Mr. Johan Emil Petterson"', 'male', '25', '1', '0', '347076', '7.775', '', 'S\n']
    ['444', '1', '2', '" Ms. Encarnacion Reynaldo"', 'female', '28', '0', '0', '230434', '13', '', 'S\n']
    ['445', '1', '3', '" Mr. Bernt Johannesen-Bratthammer"', 'male', '', '0', '0', '65306', '8.1125', '', 'S\n']
    ['446', '1', '1', '" Master. Washington Dodge"', 'male', '4', '0', '2', '33638', '81.8583', 'A34', 'S\n']
    ['447', '1', '2', '" Miss. Madeleine Violet Mellinger"', 'female', '13', '0', '1', '250644', '19.5', '', 'S\n']
    ['448', '1', '1', '" Mr. Frederic Kimber Seward"', 'male', '34', '0', '0', '113794', '26.55', '', 'S\n']
    ['449', '1', '3', '" Miss. Marie Catherine Baclini"', 'female', '5', '2', '1', '2666', '19.2583', '', 'C\n']
    ['450', '1', '1', '" Major. Arthur Godfrey Peuchen"', 'male', '52', '0', '0', '113786', '30.5', 'C104', 'S\n']
    ['451', '0', '2', '" Mr. Edwy Arthur West"', 'male', '36', '1', '2', 'C.A. 34651', '27.75', '', 'S\n']
    ['452', '0', '3', '" Mr. Ingvald Olai Olsen Hagland"', 'male', '', '1', '0', '65303', '19.9667', '', 'S\n']
    ['453', '0', '1', '" Mr. Benjamin Laventall Foreman"', 'male', '30', '0', '0', '113051', '27.75', 'C111', 'C\n']
    ['454', '1', '1', '" Mr. Samuel L Goldenberg"', 'male', '49', '1', '0', '17453', '89.1042', 'C92', 'C\n']
    ['455', '0', '3', '" Mr. Joseph Peduzzi"', 'male', '', '0', '0', 'A/5 2817', '8.05', '', 'S\n']
    ['456', '1', '3', '" Mr. Ivan Jalsevac"', 'male', '29', '0', '0', '349240', '7.8958', '', 'C\n']
    ['457', '0', '1', '" Mr. Francis Davis Millet"', 'male', '65', '0', '0', '13509', '26.55', 'E38', 'S\n']
    ['458', '1', '1', '" Mrs. Frederick R (Marion) Kenyon"', 'female', '', '1', '0', '17464', '51.8625', 'D21', 'S\n']
    ['459', '1', '2', '" Miss. Ellen Toomey"', 'female', '50', '0', '0', 'F.C.C. 13531', '10.5', '', 'S\n']
    ['460', '0', '3', '" Mr. Maurice O\'Connor"', 'male', '', '0', '0', '371060', '7.75', '', 'Q\n']
    ['461', '1', '1', '" Mr. Harry Anderson"', 'male', '48', '0', '0', '19952', '26.55', 'E12', 'S\n']
    ['462', '0', '3', '" Mr. William Morley"', 'male', '34', '0', '0', '364506', '8.05', '', 'S\n']
    ['463', '0', '1', '" Mr. Arthur H Gee"', 'male', '47', '0', '0', '111320', '38.5', 'E63', 'S\n']
    ['464', '0', '2', '" Mr. Jacob Christian Milling"', 'male', '48', '0', '0', '234360', '13', '', 'S\n']
    ['465', '0', '3', '" Mr. Simon Maisner"', 'male', '', '0', '0', 'A/S 2816', '8.05', '', 'S\n']
    ['466', '0', '3', '" Mr. Manuel Estanslas Goncalves"', 'male', '38', '0', '0', 'SOTON/O.Q. 3101306', '7.05', '', 'S\n']
    ['467', '0', '2', '" Mr. William Campbell"', 'male', '', '0', '0', '239853', '0', '', 'S\n']
    ['468', '0', '1', '" Mr. John Montgomery Smart"', 'male', '56', '0', '0', '113792', '26.55', '', 'S\n']
    ['469', '0', '3', '" Mr. James Scanlan"', 'male', '', '0', '0', '36209', '7.725', '', 'Q\n']
    ['470', '1', '3', '" Miss. Helene Barbara Baclini"', 'female', '0.75', '2', '1', '2666', '19.2583', '', 'C\n']
    ['471', '0', '3', '" Mr. Arthur Keefe"', 'male', '', '0', '0', '323592', '7.25', '', 'S\n']
    ['472', '0', '3', '" Mr. Luka Cacic"', 'male', '38', '0', '0', '315089', '8.6625', '', 'S\n']
    ['473', '1', '2', '" Mrs. Edwy Arthur (Ada Mary Worth) West"', 'female', '33', '1', '2', 'C.A. 34651', '27.75', '', 'S\n']
    ['474', '1', '2', '" Mrs. Amin S (Marie Marthe Thuillard) Jerwan"', 'female', '23', '0', '0', 'SC/AH Basle 541', '13.7917', 'D', 'C\n']
    ['475', '0', '3', '" Miss. Ida Sofia Strandberg"', 'female', '22', '0', '0', '7553', '9.8375', '', 'S\n']
    ['476', '0', '1', '" Mr. George Quincy Clifford"', 'male', '', '0', '0', '110465', '52', 'A14', 'S\n']
    ['477', '0', '2', '" Mr. Peter Henry Renouf"', 'male', '34', '1', '0', '31027', '21', '', 'S\n']
    ['478', '0', '3', '" Mr. Lewis Richard Braund"', 'male', '29', '1', '0', '3460', '7.0458', '', 'S\n']
    ['479', '0', '3', '" Mr. Nils August Karlsson"', 'male', '22', '0', '0', '350060', '7.5208', '', 'S\n']
    ['480', '1', '3', '" Miss. Hildur E Hirvonen"', 'female', '2', '0', '1', '3101298', '12.2875', '', 'S\n']
    ['481', '0', '3', '" Master. Harold Victor Goodwin"', 'male', '9', '5', '2', 'CA 2144', '46.9', '', 'S\n']
    ['482', '0', '2', '" Mr. Anthony Wood ""Archie"" Frost"', 'male', '', '0', '0', '239854', '0', '', 'S\n']
    ['483', '0', '3', '" Mr. Richard Henry Rouse"', 'male', '50', '0', '0', 'A/5 3594', '8.05', '', 'S\n']
    ['484', '1', '3', '" Mrs. (Hedwig) Turkula"', 'female', '63', '0', '0', '4134', '9.5875', '', 'S\n']
    ['485', '1', '1', '" Mr. Dickinson H Bishop"', 'male', '25', '1', '0', '11967', '91.0792', 'B49', 'C\n']
    ['486', '0', '3', '" Miss. Jeannie Lefebre"', 'female', '', '3', '1', '4133', '25.4667', '', 'S\n']
    ['487', '1', '1', '" Mrs. Frederick Maxfield (Jane Anne Forby) Hoyt"', 'female', '35', '1', '0', '19943', '90', 'C93', 'S\n']
    ['488', '0', '1', '" Mr. Edward Austin Kent"', 'male', '58', '0', '0', '11771', '29.7', 'B37', 'C\n']
    ['489', '0', '3', '" Mr. Francis William Somerton"', 'male', '30', '0', '0', 'A.5. 18509', '8.05', '', 'S\n']
    ['490', '1', '3', '" Master. Eden Leslie ""Neville"" Coutts"', 'male', '9', '1', '1', 'C.A. 37671', '15.9', '', 'S\n']
    ['491', '0', '3', '" Mr. Konrad Mathias Reiersen Hagland"', 'male', '', '1', '0', '65304', '19.9667', '', 'S\n']
    ['492', '0', '3', '" Mr. Einar Windelov"', 'male', '21', '0', '0', 'SOTON/OQ 3101317', '7.25', '', 'S\n']
    ['493', '0', '1', '" Mr. Harry Markland Molson"', 'male', '55', '0', '0', '113787', '30.5', 'C30', 'S\n']
    ['494', '0', '1', '" Mr. Ramon Artagaveytia"', 'male', '71', '0', '0', 'PC 17609', '49.5042', '', 'C\n']
    ['495', '0', '3', '" Mr. Edward Roland Stanley"', 'male', '21', '0', '0', 'A/4 45380', '8.05', '', 'S\n']
    ['496', '0', '3', '" Mr. Gerious Yousseff"', 'male', '', '0', '0', '2627', '14.4583', '', 'C\n']
    ['497', '1', '1', '" Miss. Elizabeth Mussey Eustis"', 'female', '54', '1', '0', '36947', '78.2667', 'D20', 'C\n']
    ['498', '0', '3', '" Mr. Frederick William Shellard"', 'male', '', '0', '0', 'C.A. 6212', '15.1', '', 'S\n']
    ['499', '0', '1', '" Mrs. Hudson J C (Bessie Waldo Daniels) Allison"', 'female', '25', '1', '2', '113781', '151.55', 'C22 C26', 'S\n']
    ['500', '0', '3', '" Mr. Olof Svensson"', 'male', '24', '0', '0', '350035', '7.7958', '', 'S\n']
    ['501', '0', '3', '" Mr. Petar Calic"', 'male', '17', '0', '0', '315086', '8.6625', '', 'S\n']
    ['502', '0', '3', '" Miss. Mary Canavan"', 'female', '21', '0', '0', '364846', '7.75', '', 'Q\n']
    ['503', '0', '3', '" Miss. Bridget Mary O\'Sullivan"', 'female', '', '0', '0', '330909', '7.6292', '', 'Q\n']
    ['504', '0', '3', '" Miss. Kristina Sofia Laitinen"', 'female', '37', '0', '0', '4135', '9.5875', '', 'S\n']
    ['505', '1', '1', '" Miss. Roberta Maioni"', 'female', '16', '0', '0', '110152', '86.5', 'B79', 'S\n']
    ['506', '0', '1', '" Mr. Victor de Satode Penasco y Castellana"', 'male', '18', '1', '0', 'PC 17758', '108.9', 'C65', 'C\n']
    ['507', '1', '2', '" Mrs. Frederick Charles (Jane Richards) Quick"', 'female', '33', '0', '2', '26360', '26', '', 'S\n']
    ['508', '1', '1', '" Mr. George (""George Arthur Brayton"") Bradley"', 'male', '', '0', '0', '111427', '26.55', '', 'S\n']
    ['509', '0', '3', '" Mr. Henry Margido Olsen"', 'male', '28', '0', '0', 'C 4001', '22.525', '', 'S\n']
    ['510', '1', '3', '" Mr. Fang Lang"', 'male', '26', '0', '0', '1601', '56.4958', '', 'S\n']
    ['511', '1', '3', '" Mr. Eugene Patrick Daly"', 'male', '29', '0', '0', '382651', '7.75', '', 'Q\n']
    ['512', '0', '3', '" Mr. James Webber"', 'male', '', '0', '0', 'SOTON/OQ 3101316', '8.05', '', 'S\n']
    ['513', '1', '1', '" Mr. James Robert McGough"', 'male', '36', '0', '0', 'PC 17473', '26.2875', 'E25', 'S\n']
    ['514', '1', '1', '" Mrs. Martin (Elizabeth L. Barrett) Rothschild"', 'female', '54', '1', '0', 'PC 17603', '59.4', '', 'C\n']
    ['515', '0', '3', '" Mr. Satio Coleff"', 'male', '24', '0', '0', '349209', '7.4958', '', 'S\n']
    ['516', '0', '1', '" Mr. William Anderson Walker"', 'male', '47', '0', '0', '36967', '34.0208', 'D46', 'S\n']
    ['517', '1', '2', '" Mrs. (Amelia Milley) Lemore"', 'female', '34', '0', '0', 'C.A. 34260', '10.5', 'F33', 'S\n']
    ['518', '0', '3', '" Mr. Patrick Ryan"', 'male', '', '0', '0', '371110', '24.15', '', 'Q\n']
    ['519', '1', '2', '" Mrs. William A (Florence ""Mary"" Agnes Hughes) Angle"', 'female', '36', '1', '0', '226875', '26', '', 'S\n']
    ['520', '0', '3', '" Mr. Stefo Pavlovic"', 'male', '32', '0', '0', '349242', '7.8958', '', 'S\n']
    ['521', '1', '1', '" Miss. Anne Perreault"', 'female', '30', '0', '0', '12749', '93.5', 'B73', 'S\n']
    ['522', '0', '3', '" Mr. Janko Vovk"', 'male', '22', '0', '0', '349252', '7.8958', '', 'S\n']
    ['523', '0', '3', '" Mr. Sarkis Lahoud"', 'male', '', '0', '0', '2624', '7.225', '', 'C\n']
    ['524', '1', '1', '" Mrs. Louis Albert (Ida Sophia Fischer) Hippach"', 'female', '44', '0', '1', '111361', '57.9792', 'B18', 'C\n']
    ['525', '0', '3', '" Mr. Fared Kassem"', 'male', '', '0', '0', '2700', '7.2292', '', 'C\n']
    ['526', '0', '3', '" Mr. James Farrell"', 'male', '40.5', '0', '0', '367232', '7.75', '', 'Q\n']
    ['527', '1', '2', '" Miss. Lucy Ridsdale"', 'female', '50', '0', '0', 'W./C. 14258', '10.5', '', 'S\n']
    ['528', '0', '1', '" Mr. John Farthing"', 'male', '', '0', '0', 'PC 17483', '221.7792', 'C95', 'S\n']
    ['529', '0', '3', '" Mr. Johan Werner Salonen"', 'male', '39', '0', '0', '3101296', '7.925', '', 'S\n']
    ['530', '0', '2', '" Mr. Richard George Hocking"', 'male', '23', '2', '1', '29104', '11.5', '', 'S\n']
    ['531', '1', '2', '" Miss. Phyllis May Quick"', 'female', '2', '1', '1', '26360', '26', '', 'S\n']
    ['532', '0', '3', '" Mr. Nakli Toufik"', 'male', '', '0', '0', '2641', '7.2292', '', 'C\n']
    ['533', '0', '3', '" Mr. Joseph Jr Elias"', 'male', '17', '1', '1', '2690', '7.2292', '', 'C\n']
    ['534', '1', '3', '" Mrs. Catherine (Catherine Rizk) Peter"', 'female', '', '0', '2', '2668', '22.3583', '', 'C\n']
    ['535', '0', '3', '" Miss. Marija Cacic"', 'female', '30', '0', '0', '315084', '8.6625', '', 'S\n']
    ['536', '1', '2', '" Miss. Eva Miriam Hart"', 'female', '7', '0', '2', 'F.C.C. 13529', '26.25', '', 'S\n']
    ['537', '0', '1', '" Major. Archibald Willingham Butt"', 'male', '45', '0', '0', '113050', '26.55', 'B38', 'S\n']
    ['538', '1', '1', '" Miss. Bertha LeRoy"', 'female', '30', '0', '0', 'PC 17761', '106.425', '', 'C\n']
    ['539', '0', '3', '" Mr. Samuel Beard Risien"', 'male', '', '0', '0', '364498', '14.5', '', 'S\n']
    ['540', '1', '1', '" Miss. Hedwig Margaritha Frolicher"', 'female', '22', '0', '2', '13568', '49.5', 'B39', 'C\n']
    ['541', '1', '1', '" Miss. Harriet R Crosby"', 'female', '36', '0', '2', 'WE/P 5735', '71', 'B22', 'S\n']
    ['542', '0', '3', '" Miss. Ingeborg Constanzia Andersson"', 'female', '9', '4', '2', '347082', '31.275', '', 'S\n']
    ['543', '0', '3', '" Miss. Sigrid Elisabeth Andersson"', 'female', '11', '4', '2', '347082', '31.275', '', 'S\n']
    ['544', '1', '2', '" Mr. Edward Beane"', 'male', '32', '1', '0', '2908', '26', '', 'S\n']
    ['545', '0', '1', '" Mr. Walter Donald Douglas"', 'male', '50', '1', '0', 'PC 17761', '106.425', 'C86', 'C\n']
    ['546', '0', '1', '" Mr. Arthur Ernest Nicholson"', 'male', '64', '0', '0', '693', '26', '', 'S\n']
    ['547', '1', '2', '" Mrs. Edward (Ethel Clarke) Beane"', 'female', '19', '1', '0', '2908', '26', '', 'S\n']
    ['548', '1', '2', '" Mr. Julian Padro y Manent"', 'male', '', '0', '0', 'SC/PARIS 2146', '13.8625', '', 'C\n']
    ['549', '0', '3', '" Mr. Frank John Goldsmith"', 'male', '33', '1', '1', '363291', '20.525', '', 'S\n']
    ['550', '1', '2', '" Master. John Morgan Jr Davies"', 'male', '8', '1', '1', 'C.A. 33112', '36.75', '', 'S\n']
    ['551', '1', '1', '" Mr. John Borland Jr Thayer"', 'male', '17', '0', '2', '17421', '110.8833', 'C70', 'C\n']
    ['552', '0', '2', '" Mr. Percival James R Sharp"', 'male', '27', '0', '0', '244358', '26', '', 'S\n']
    ['553', '0', '3', '" Mr. Timothy O\'Brien"', 'male', '', '0', '0', '330979', '7.8292', '', 'Q\n']
    ['554', '1', '3', '" Mr. Fahim (""Philip Zenni"") Leeni"', 'male', '22', '0', '0', '2620', '7.225', '', 'C\n']
    ['555', '1', '3', '" Miss. Velin Ohman"', 'female', '22', '0', '0', '347085', '7.775', '', 'S\n']
    ['556', '0', '1', '" Mr. George Wright"', 'male', '62', '0', '0', '113807', '26.55', '', 'S\n']
    ['557', '1', '1', '" Lady. (Lucille Christiana Sutherland) (""Mrs Morgan"") Duff Gordon"', 'female', '48', '1', '0', '11755', '39.6', 'A16', 'C\n']
    ['558', '0', '1', '" Mr. Victor Robbins"', 'male', '', '0', '0', 'PC 17757', '227.525', '', 'C\n']
    ['559', '1', '1', '" Mrs. Emil (Tillie Mandelbaum) Taussig"', 'female', '39', '1', '1', '110413', '79.65', 'E67', 'S\n']
    ['560', '1', '3', '" Mrs. Guillaume Joseph (Emma) de Messemaeker"', 'female', '36', '1', '0', '345572', '17.4', '', 'S\n']
    ['561', '0', '3', '" Mr. Thomas Rowan Morrow"', 'male', '', '0', '0', '372622', '7.75', '', 'Q\n']
    ['562', '0', '3', '" Mr. Husein Sivic"', 'male', '40', '0', '0', '349251', '7.8958', '', 'S\n']
    ['563', '0', '2', '" Mr. Robert Douglas Norman"', 'male', '28', '0', '0', '218629', '13.5', '', 'S\n']
    ['564', '0', '3', '" Mr. John Simmons"', 'male', '', '0', '0', 'SOTON/OQ 392082', '8.05', '', 'S\n']
    ['565', '0', '3', '" Miss. (Marion Ogden) Meanwell"', 'female', '', '0', '0', 'SOTON/O.Q. 392087', '8.05', '', 'S\n']
    ['566', '0', '3', '" Mr. Alfred J Davies"', 'male', '24', '2', '0', 'A/4 48871', '24.15', '', 'S\n']
    ['567', '0', '3', '" Mr. Ilia Stoytcheff"', 'male', '19', '0', '0', '349205', '7.8958', '', 'S\n']
    ['568', '0', '3', '" Mrs. Nils (Alma Cornelia Berglund) Palsson"', 'female', '29', '0', '4', '349909', '21.075', '', 'S\n']
    ['569', '0', '3', '" Mr. Tannous Doharr"', 'male', '', '0', '0', '2686', '7.2292', '', 'C\n']
    ['570', '1', '3', '" Mr. Carl Jonsson"', 'male', '32', '0', '0', '350417', '7.8542', '', 'S\n']
    ['571', '1', '2', '" Mr. George Harris"', 'male', '62', '0', '0', 'S.W./PP 752', '10.5', '', 'S\n']
    ['572', '1', '1', '" Mrs. Edward Dale (Charlotte Lamson) Appleton"', 'female', '53', '2', '0', '11769', '51.4792', 'C101', 'S\n']
    ['573', '1', '1', '" Mr. John Irwin (""Irving"") Flynn"', 'male', '36', '0', '0', 'PC 17474', '26.3875', 'E25', 'S\n']
    ['574', '1', '3', '" Miss. Mary Kelly"', 'female', '', '0', '0', '14312', '7.75', '', 'Q\n']
    ['575', '0', '3', '" Mr. Alfred George John Rush"', 'male', '16', '0', '0', 'A/4. 20589', '8.05', '', 'S\n']
    ['576', '0', '3', '" Mr. George Patchett"', 'male', '19', '0', '0', '358585', '14.5', '', 'S\n']
    ['577', '1', '2', '" Miss. Ethel Garside"', 'female', '34', '0', '0', '243880', '13', '', 'S\n']
    ['578', '1', '1', '" Mrs. William Baird (Alice Munger) Silvey"', 'female', '39', '1', '0', '13507', '55.9', 'E44', 'S\n']
    ['579', '0', '3', '" Mrs. Joseph (Maria Elias) Caram"', 'female', '', '1', '0', '2689', '14.4583', '', 'C\n']
    ['580', '1', '3', '" Mr. Eiriik Jussila"', 'male', '32', '0', '0', 'STON/O 2. 3101286', '7.925', '', 'S\n']
    ['581', '1', '2', '" Miss. Julie Rachel Christy"', 'female', '25', '1', '1', '237789', '30', '', 'S\n']
    ['582', '1', '1', '" Mrs. John Borland (Marian Longstreth Morris) Thayer"', 'female', '39', '1', '1', '17421', '110.8833', 'C68', 'C\n']
    ['583', '0', '2', '" Mr. William James Downton"', 'male', '54', '0', '0', '28403', '26', '', 'S\n']
    ['584', '0', '1', '" Mr. John Hugo Ross"', 'male', '36', '0', '0', '13049', '40.125', 'A10', 'C\n']
    ['585', '0', '3', '" Mr. Uscher Paulner"', 'male', '', '0', '0', '3411', '8.7125', '', 'C\n']
    ['586', '1', '1', '" Miss. Ruth Taussig"', 'female', '18', '0', '2', '110413', '79.65', 'E68', 'S\n']
    ['587', '0', '2', '" Mr. John Denzil Jarvis"', 'male', '47', '0', '0', '237565', '15', '', 'S\n']
    ['588', '1', '1', '" Mr. Maxmillian Frolicher-Stehli"', 'male', '60', '1', '1', '13567', '79.2', 'B41', 'C\n']
    ['589', '0', '3', '" Mr. Eliezer Gilinski"', 'male', '22', '0', '0', '14973', '8.05', '', 'S\n']
    ['590', '0', '3', '" Mr. Joseph Murdlin"', 'male', '', '0', '0', 'A./5. 3235', '8.05', '', 'S\n']
    ['591', '0', '3', '" Mr. Matti Rintamaki"', 'male', '35', '0', '0', 'STON/O 2. 3101273', '7.125', '', 'S\n']
    ['592', '1', '1', '" Mrs. Walter Bertram (Martha Eustis) Stephenson"', 'female', '52', '1', '0', '36947', '78.2667', 'D20', 'C\n']
    ['593', '0', '3', '" Mr. William James Elsbury"', 'male', '47', '0', '0', 'A/5 3902', '7.25', '', 'S\n']
    ['594', '0', '3', '" Miss. Mary Bourke"', 'female', '', '0', '2', '364848', '7.75', '', 'Q\n']
    ['595', '0', '2', '" Mr. John Henry Chapman"', 'male', '37', '1', '0', 'SC/AH 29037', '26', '', 'S\n']
    ['596', '0', '3', '" Mr. Jean Baptiste Van Impe"', 'male', '36', '1', '1', '345773', '24.15', '', 'S\n']
    ['597', '1', '2', '" Miss. Jessie Wills Leitch"', 'female', '', '0', '0', '248727', '33', '', 'S\n']
    ['598', '0', '3', '" Mr. Alfred Johnson"', 'male', '49', '0', '0', 'LINE', '0', '', 'S\n']
    ['599', '0', '3', '" Mr. Hanna Boulos"', 'male', '', '0', '0', '2664', '7.225', '', 'C\n']
    ['600', '1', '1', '" Sir. Cosmo Edmund (""Mr Morgan"") Duff Gordon"', 'male', '49', '1', '0', 'PC 17485', '56.9292', 'A20', 'C\n']
    ['601', '1', '2', '" Mrs. Sidney Samuel (Amy Frances Christy) Jacobsohn"', 'female', '24', '2', '1', '243847', '27', '', 'S\n']
    ['602', '0', '3', '" Mr. Petco Slabenoff"', 'male', '', '0', '0', '349214', '7.8958', '', 'S\n']
    ['603', '0', '1', '" Mr. Charles H Harrington"', 'male', '', '0', '0', '113796', '42.4', '', 'S\n']
    ['604', '0', '3', '" Mr. Ernst William Torber"', 'male', '44', '0', '0', '364511', '8.05', '', 'S\n']
    ['605', '1', '1', '" Mr. Harry (""Mr E Haven"") Homer"', 'male', '35', '0', '0', '111426', '26.55', '', 'C\n']
    ['606', '0', '3', '" Mr. Edvard Bengtsson Lindell"', 'male', '36', '1', '0', '349910', '15.55', '', 'S\n']
    ['607', '0', '3', '" Mr. Milan Karaic"', 'male', '30', '0', '0', '349246', '7.8958', '', 'S\n']
    ['608', '1', '1', '" Mr. Robert Williams Daniel"', 'male', '27', '0', '0', '113804', '30.5', '', 'S\n']
    ['609', '1', '2', '" Mrs. Joseph (Juliette Marie Louise Lafargue) Laroche"', 'female', '22', '1', '2', 'SC/Paris 2123', '41.5792', '', 'C\n']
    ['610', '1', '1', '" Miss. Elizabeth W Shutes"', 'female', '40', '0', '0', 'PC 17582', '153.4625', 'C125', 'S\n']
    ['611', '0', '3', '" Mrs. Anders Johan (Alfrida Konstantia Brogren) Andersson"', 'female', '39', '1', '5', '347082', '31.275', '', 'S\n']
    ['612', '0', '3', '" Mr. Jose Neto Jardin"', 'male', '', '0', '0', 'SOTON/O.Q. 3101305', '7.05', '', 'S\n']
    ['613', '1', '3', '" Miss. Margaret Jane Murphy"', 'female', '', '1', '0', '367230', '15.5', '', 'Q\n']
    ['614', '0', '3', '" Mr. John Horgan"', 'male', '', '0', '0', '370377', '7.75', '', 'Q\n']
    ['615', '0', '3', '" Mr. William Alfred Brocklebank"', 'male', '35', '0', '0', '364512', '8.05', '', 'S\n']
    ['616', '1', '2', '" Miss. Alice Herman"', 'female', '24', '1', '2', '220845', '65', '', 'S\n']
    ['617', '0', '3', '" Mr. Ernst Gilbert Danbom"', 'male', '34', '1', '1', '347080', '14.4', '', 'S\n']
    ['618', '0', '3', '" Mrs. William Arthur (Cordelia K Stanlick) Lobb"', 'female', '26', '1', '0', 'A/5. 3336', '16.1', '', 'S\n']
    ['619', '1', '2', '" Miss. Marion Louise Becker"', 'female', '4', '2', '1', '230136', '39', 'F4', 'S\n']
    ['620', '0', '2', '" Mr. Lawrence Gavey"', 'male', '26', '0', '0', '31028', '10.5', '', 'S\n']
    ['621', '0', '3', '" Mr. Antoni Yasbeck"', 'male', '27', '1', '0', '2659', '14.4542', '', 'C\n']
    ['622', '1', '1', '" Mr. Edwin Nelson Jr Kimball"', 'male', '42', '1', '0', '11753', '52.5542', 'D19', 'S\n']
    ['623', '1', '3', '" Mr. Sahid Nakid"', 'male', '20', '1', '1', '2653', '15.7417', '', 'C\n']
    ['624', '0', '3', '" Mr. Henry Damsgaard Hansen"', 'male', '21', '0', '0', '350029', '7.8542', '', 'S\n']
    ['625', '0', '3', '" Mr. David John ""Dai"" Bowen"', 'male', '21', '0', '0', '54636', '16.1', '', 'S\n']
    ['626', '0', '1', '" Mr. Frederick Sutton"', 'male', '61', '0', '0', '36963', '32.3208', 'D50', 'S\n']
    ['627', '0', '2', '" Rev. Charles Leonard Kirkland"', 'male', '57', '0', '0', '219533', '12.35', '', 'Q\n']
    ['628', '1', '1', '" Miss. Gretchen Fiske Longley"', 'female', '21', '0', '0', '13502', '77.9583', 'D9', 'S\n']
    ['629', '0', '3', '" Mr. Guentcho Bostandyeff"', 'male', '26', '0', '0', '349224', '7.8958', '', 'S\n']
    ['630', '0', '3', '" Mr. Patrick D O\'Connell"', 'male', '', '0', '0', '334912', '7.7333', '', 'Q\n']
    ['631', '1', '1', '" Mr. Algernon Henry Wilson Barkworth"', 'male', '80', '0', '0', '27042', '30', 'A23', 'S\n']
    ['632', '0', '3', '" Mr. Johan Svensson Lundahl"', 'male', '51', '0', '0', '347743', '7.0542', '', 'S\n']
    ['633', '1', '1', '" Dr. Max Stahelin-Maeglin"', 'male', '32', '0', '0', '13214', '30.5', 'B50', 'C\n']
    ['634', '0', '1', '" Mr. William Henry Marsh Parr"', 'male', '', '0', '0', '112052', '0', '', 'S\n']
    ['635', '0', '3', '" Miss. Mabel Skoog"', 'female', '9', '3', '2', '347088', '27.9', '', 'S\n']
    ['636', '1', '2', '" Miss. Mary Davis"', 'female', '28', '0', '0', '237668', '13', '', 'S\n']
    ['637', '0', '3', '" Mr. Antti Gustaf Leinonen"', 'male', '32', '0', '0', 'STON/O 2. 3101292', '7.925', '', 'S\n']
    ['638', '0', '2', '" Mr. Harvey Collyer"', 'male', '31', '1', '1', 'C.A. 31921', '26.25', '', 'S\n']
    ['639', '0', '3', '" Mrs. Juha (Maria Emilia Ojala) Panula"', 'female', '41', '0', '5', '3101295', '39.6875', '', 'S\n']
    ['640', '0', '3', '" Mr. Percival Thorneycroft"', 'male', '', '1', '0', '376564', '16.1', '', 'S\n']
    ['641', '0', '3', '" Mr. Hans Peder Jensen"', 'male', '20', '0', '0', '350050', '7.8542', '', 'S\n']
    ['642', '1', '1', '" Mlle. Emma Sagesser"', 'female', '24', '0', '0', 'PC 17477', '69.3', 'B35', 'C\n']
    ['643', '0', '3', '" Miss. Margit Elizabeth Skoog"', 'female', '2', '3', '2', '347088', '27.9', '', 'S\n']
    ['644', '1', '3', '" Mr. Choong Foo"', 'male', '', '0', '0', '1601', '56.4958', '', 'S\n']
    ['645', '1', '3', '" Miss. Eugenie Baclini"', 'female', '0.75', '2', '1', '2666', '19.2583', '', 'C\n']
    ['646', '1', '1', '" Mr. Henry Sleeper Harper"', 'male', '48', '1', '0', 'PC 17572', '76.7292', 'D33', 'C\n']
    ['647', '0', '3', '" Mr. Liudevit Cor"', 'male', '19', '0', '0', '349231', '7.8958', '', 'S\n']
    ['648', '1', '1', '" Col. Oberst Alfons Simonius-Blumer"', 'male', '56', '0', '0', '13213', '35.5', 'A26', 'C\n']
    ['649', '0', '3', '" Mr. Edward Willey"', 'male', '', '0', '0', 'S.O./P.P. 751', '7.55', '', 'S\n']
    ['650', '1', '3', '" Miss. Amy Zillah Elsie Stanley"', 'female', '23', '0', '0', 'CA. 2314', '7.55', '', 'S\n']
    ['651', '0', '3', '" Mr. Mito Mitkoff"', 'male', '', '0', '0', '349221', '7.8958', '', 'S\n']
    ['652', '1', '2', '" Miss. Elsie Doling"', 'female', '18', '0', '1', '231919', '23', '', 'S\n']
    ['653', '0', '3', '" Mr. Johannes Halvorsen Kalvik"', 'male', '21', '0', '0', '8475', '8.4333', '', 'S\n']
    ['654', '1', '3', '" Miss. Hanora ""Norah"" O\'Leary"', 'female', '', '0', '0', '330919', '7.8292', '', 'Q\n']
    ['655', '0', '3', '" Miss. Hanora ""Nora"" Hegarty"', 'female', '18', '0', '0', '365226', '6.75', '', 'Q\n']
    ['656', '0', '2', '" Mr. Leonard Mark Hickman"', 'male', '24', '2', '0', 'S.O.C. 14879', '73.5', '', 'S\n']
    ['657', '0', '3', '" Mr. Alexander Radeff"', 'male', '', '0', '0', '349223', '7.8958', '', 'S\n']
    ['658', '0', '3', '" Mrs. John (Catherine) Bourke"', 'female', '32', '1', '1', '364849', '15.5', '', 'Q\n']
    ['659', '0', '2', '" Mr. George Floyd Eitemiller"', 'male', '23', '0', '0', '29751', '13', '', 'S\n']
    ['660', '0', '1', '" Mr. Arthur Webster Newell"', 'male', '58', '0', '2', '35273', '113.275', 'D48', 'C\n']
    ['661', '1', '1', '" Dr. Henry William Frauenthal"', 'male', '50', '2', '0', 'PC 17611', '133.65', '', 'S\n']
    ['662', '0', '3', '" Mr. Mohamed Badt"', 'male', '40', '0', '0', '2623', '7.225', '', 'C\n']
    ['663', '0', '1', '" Mr. Edward Pomeroy Colley"', 'male', '47', '0', '0', '5727', '25.5875', 'E58', 'S\n']
    ['664', '0', '3', '" Mr. Peju Coleff"', 'male', '36', '0', '0', '349210', '7.4958', '', 'S\n']
    ['665', '1', '3', '" Mr. Eino William Lindqvist"', 'male', '20', '1', '0', 'STON/O 2. 3101285', '7.925', '', 'S\n']
    ['666', '0', '2', '" Mr. Lewis Hickman"', 'male', '32', '2', '0', 'S.O.C. 14879', '73.5', '', 'S\n']
    ['667', '0', '2', '" Mr. Reginald Fenton Butler"', 'male', '25', '0', '0', '234686', '13', '', 'S\n']
    ['668', '0', '3', '" Mr. Knud Paust Rommetvedt"', 'male', '', '0', '0', '312993', '7.775', '', 'S\n']
    ['669', '0', '3', '" Mr. Jacob Cook"', 'male', '43', '0', '0', 'A/5 3536', '8.05', '', 'S\n']
    ['670', '1', '1', '" Mrs. Elmer Zebley (Juliet Cummins Wright) Taylor"', 'female', '', '1', '0', '19996', '52', 'C126', 'S\n']
    ['671', '1', '2', '" Mrs. Thomas William Solomon (Elizabeth Catherine Ford) Brown"', 'female', '40', '1', '1', '29750', '39', '', 'S\n']
    ['672', '0', '1', '" Mr. Thornton Davidson"', 'male', '31', '1', '0', 'F.C. 12750', '52', 'B71', 'S\n']
    ['673', '0', '2', '" Mr. Henry Michael Mitchell"', 'male', '70', '0', '0', 'C.A. 24580', '10.5', '', 'S\n']
    ['674', '1', '2', '" Mr. Charles Wilhelms"', 'male', '31', '0', '0', '244270', '13', '', 'S\n']
    ['675', '0', '2', '" Mr. Ennis Hastings Watson"', 'male', '', '0', '0', '239856', '0', '', 'S\n']
    ['676', '0', '3', '" Mr. Gustaf Hjalmar Edvardsson"', 'male', '18', '0', '0', '349912', '7.775', '', 'S\n']
    ['677', '0', '3', '" Mr. Frederick Charles Sawyer"', 'male', '24.5', '0', '0', '342826', '8.05', '', 'S\n']
    ['678', '1', '3', '" Miss. Anna Sofia Turja"', 'female', '18', '0', '0', '4138', '9.8417', '', 'S\n']
    ['679', '0', '3', '" Mrs. Frederick (Augusta Tyler) Goodwin"', 'female', '43', '1', '6', 'CA 2144', '46.9', '', 'S\n']
    ['680', '1', '1', '" Mr. Thomas Drake Martinez Cardeza"', 'male', '36', '0', '1', 'PC 17755', '512.3292', 'B51 B53 B55', 'C\n']
    ['681', '0', '3', '" Miss. Katie Peters"', 'female', '', '0', '0', '330935', '8.1375', '', 'Q\n']
    ['682', '1', '1', '" Mr. Hammad Hassab"', 'male', '27', '0', '0', 'PC 17572', '76.7292', 'D49', 'C\n']
    ['683', '0', '3', '" Mr. Thor Anderson Olsvigen"', 'male', '20', '0', '0', '6563', '9.225', '', 'S\n']
    ['684', '0', '3', '" Mr. Charles Edward Goodwin"', 'male', '14', '5', '2', 'CA 2144', '46.9', '', 'S\n']
    ['685', '0', '2', '" Mr. Thomas William Solomon Brown"', 'male', '60', '1', '1', '29750', '39', '', 'S\n']
    ['686', '0', '2', '" Mr. Joseph Philippe Lemercier Laroche"', 'male', '25', '1', '2', 'SC/Paris 2123', '41.5792', '', 'C\n']
    ['687', '0', '3', '" Mr. Jaako Arnold Panula"', 'male', '14', '4', '1', '3101295', '39.6875', '', 'S\n']
    ['688', '0', '3', '" Mr. Branko Dakic"', 'male', '19', '0', '0', '349228', '10.1708', '', 'S\n']
    ['689', '0', '3', '" Mr. Eberhard Thelander Fischer"', 'male', '18', '0', '0', '350036', '7.7958', '', 'S\n']
    ['690', '1', '1', '" Miss. Georgette Alexandra Madill"', 'female', '15', '0', '1', '24160', '211.3375', 'B5', 'S\n']
    ['691', '1', '1', '" Mr. Albert Adrian Dick"', 'male', '31', '1', '0', '17474', '57', 'B20', 'S\n']
    ['692', '1', '3', '" Miss. Manca Karun"', 'female', '4', '0', '1', '349256', '13.4167', '', 'C\n']
    ['693', '1', '3', '" Mr. Ali Lam"', 'male', '', '0', '0', '1601', '56.4958', '', 'S\n']
    ['694', '0', '3', '" Mr. Khalil Saad"', 'male', '25', '0', '0', '2672', '7.225', '', 'C\n']
    ['695', '0', '1', '" Col. John Weir"', 'male', '60', '0', '0', '113800', '26.55', '', 'S\n']
    ['696', '0', '2', '" Mr. Charles Henry Chapman"', 'male', '52', '0', '0', '248731', '13.5', '', 'S\n']
    ['697', '0', '3', '" Mr. James Kelly"', 'male', '44', '0', '0', '363592', '8.05', '', 'S\n']
    ['698', '1', '3', '" Miss. Katherine ""Katie"" Mullens"', 'female', '', '0', '0', '35852', '7.7333', '', 'Q\n']
    ['699', '0', '1', '" Mr. John Borland Thayer"', 'male', '49', '1', '1', '17421', '110.8833', 'C68', 'C\n']
    ['700', '0', '3', '" Mr. Adolf Mathias Nicolai Olsen Humblen"', 'male', '42', '0', '0', '348121', '7.65', 'F G63', 'S\n']
    ['701', '1', '1', '" Mrs. John Jacob (Madeleine Talmadge Force) Astor"', 'female', '18', '1', '0', 'PC 17757', '227.525', 'C62 C64', 'C\n']
    ['702', '1', '1', '" Mr. Spencer Victor Silverthorne"', 'male', '35', '0', '0', 'PC 17475', '26.2875', 'E24', 'S\n']
    ['703', '0', '3', '" Miss. Saiide Barbara"', 'female', '18', '0', '1', '2691', '14.4542', '', 'C\n']
    ['704', '0', '3', '" Mr. Martin Gallagher"', 'male', '25', '0', '0', '36864', '7.7417', '', 'Q\n']
    ['705', '0', '3', '" Mr. Henrik Juul Hansen"', 'male', '26', '1', '0', '350025', '7.8542', '', 'S\n']
    ['706', '0', '2', '" Mr. Henry Samuel (""Mr Henry Marshall"") Morley"', 'male', '39', '0', '0', '250655', '26', '', 'S\n']
    ['707', '1', '2', '" Mrs. Florence ""Fannie"" Kelly"', 'female', '45', '0', '0', '223596', '13.5', '', 'S\n']
    ['708', '1', '1', '" Mr. Edward Pennington Calderhead"', 'male', '42', '0', '0', 'PC 17476', '26.2875', 'E24', 'S\n']
    ['709', '1', '1', '" Miss. Alice Cleaver"', 'female', '22', '0', '0', '113781', '151.55', '', 'S\n']
    ['710', '1', '3', '" Master. Halim Gonios (""William George"") Moubarek"', 'male', '', '1', '1', '2661', '15.2458', '', 'C\n']
    ['711', '1', '1', '" Mlle. Berthe Antonine (""Mrs de Villiers"") Mayne"', 'female', '24', '0', '0', 'PC 17482', '49.5042', 'C90', 'C\n']
    ['712', '0', '1', '" Mr. Herman Klaber"', 'male', '', '0', '0', '113028', '26.55', 'C124', 'S\n']
    ['713', '1', '1', '" Mr. Elmer Zebley Taylor"', 'male', '48', '1', '0', '19996', '52', 'C126', 'S\n']
    ['714', '0', '3', '" Mr. August Viktor Larsson"', 'male', '29', '0', '0', '7545', '9.4833', '', 'S\n']
    ['715', '0', '2', '" Mr. Samuel Greenberg"', 'male', '52', '0', '0', '250647', '13', '', 'S\n']
    ['716', '0', '3', '" Mr. Peter Andreas Lauritz Andersen Soholt"', 'male', '19', '0', '0', '348124', '7.65', 'F G73', 'S\n']
    ['717', '1', '1', '" Miss. Caroline Louise Endres"', 'female', '38', '0', '0', 'PC 17757', '227.525', 'C45', 'C\n']
    ['718', '1', '2', '" Miss. Edwina Celia ""Winnie"" Troutt"', 'female', '27', '0', '0', '34218', '10.5', 'E101', 'S\n']
    ['719', '0', '3', '" Mr. Michael McEvoy"', 'male', '', '0', '0', '36568', '15.5', '', 'Q\n']
    ['720', '0', '3', '" Mr. Malkolm Joackim Johnson"', 'male', '33', '0', '0', '347062', '7.775', '', 'S\n']
    ['721', '1', '2', '" Miss. Annie Jessie ""Nina"" Harper"', 'female', '6', '0', '1', '248727', '33', '', 'S\n']
    ['722', '0', '3', '" Mr. Svend Lauritz Jensen"', 'male', '17', '1', '0', '350048', '7.0542', '', 'S\n']
    ['723', '0', '2', '" Mr. William Henry Gillespie"', 'male', '34', '0', '0', '12233', '13', '', 'S\n']
    ['724', '0', '2', '" Mr. Henry Price Hodges"', 'male', '50', '0', '0', '250643', '13', '', 'S\n']
    ['725', '1', '1', '" Mr. Norman Campbell Chambers"', 'male', '27', '1', '0', '113806', '53.1', 'E8', 'S\n']
    ['726', '0', '3', '" Mr. Luka Oreskovic"', 'male', '20', '0', '0', '315094', '8.6625', '', 'S\n']
    ['727', '1', '2', '" Mrs. Peter Henry (Lillian Jefferys) Renouf"', 'female', '30', '3', '0', '31027', '21', '', 'S\n']
    ['728', '1', '3', '" Miss. Margareth Mannion"', 'female', '', '0', '0', '36866', '7.7375', '', 'Q\n']
    ['729', '0', '2', '" Mr. Kurt Arnold Gottfrid Bryhl"', 'male', '25', '1', '0', '236853', '26', '', 'S\n']
    ['730', '0', '3', '" Miss. Pieta Sofia Ilmakangas"', 'female', '25', '1', '0', 'STON/O2. 3101271', '7.925', '', 'S\n']
    ['731', '1', '1', '" Miss. Elisabeth Walton Allen"', 'female', '29', '0', '0', '24160', '211.3375', 'B5', 'S\n']
    ['732', '0', '3', '" Mr. Houssein G N Hassan"', 'male', '11', '0', '0', '2699', '18.7875', '', 'C\n']
    ['733', '0', '2', '" Mr. Robert J Knight"', 'male', '', '0', '0', '239855', '0', '', 'S\n']
    ['734', '0', '2', '" Mr. William John Berriman"', 'male', '23', '0', '0', '28425', '13', '', 'S\n']
    ['735', '0', '2', '" Mr. Moses Aaron Troupiansky"', 'male', '23', '0', '0', '233639', '13', '', 'S\n']
    ['736', '0', '3', '" Mr. Leslie Williams"', 'male', '28.5', '0', '0', '54636', '16.1', '', 'S\n']
    ['737', '0', '3', '" Mrs. Edward (Margaret Ann Watson) Ford"', 'female', '48', '1', '3', 'W./C. 6608', '34.375', '', 'S\n']
    ['738', '1', '1', '" Mr. Gustave J Lesurer"', 'male', '35', '0', '0', 'PC 17755', '512.3292', 'B101', 'C\n']
    ['739', '0', '3', '" Mr. Kanio Ivanoff"', 'male', '', '0', '0', '349201', '7.8958', '', 'S\n']
    ['740', '0', '3', '" Mr. Minko Nankoff"', 'male', '', '0', '0', '349218', '7.8958', '', 'S\n']
    ['741', '1', '1', '" Mr. Walter James Hawksford"', 'male', '', '0', '0', '16988', '30', 'D45', 'S\n']
    ['742', '0', '1', '" Mr. Tyrell William Cavendish"', 'male', '36', '1', '0', '19877', '78.85', 'C46', 'S\n']
    ['743', '1', '1', '" Miss. Susan Parker ""Suzette"" Ryerson"', 'female', '21', '2', '2', 'PC 17608', '262.375', 'B57 B59 B63 B66', 'C\n']
    ['744', '0', '3', '" Mr. Neal McNamee"', 'male', '24', '1', '0', '376566', '16.1', '', 'S\n']
    ['745', '1', '3', '" Mr. Juho Stranden"', 'male', '31', '0', '0', 'STON/O 2. 3101288', '7.925', '', 'S\n']
    ['746', '0', '1', '" Capt. Edward Gifford Crosby"', 'male', '70', '1', '1', 'WE/P 5735', '71', 'B22', 'S\n']
    ['747', '0', '3', '" Mr. Rossmore Edward Abbott"', 'male', '16', '1', '1', 'C.A. 2673', '20.25', '', 'S\n']
    ['748', '1', '2', '" Miss. Anna Sinkkonen"', 'female', '30', '0', '0', '250648', '13', '', 'S\n']
    ['749', '0', '1', '" Mr. Daniel Warner Marvin"', 'male', '19', '1', '0', '113773', '53.1', 'D30', 'S\n']
    ['750', '0', '3', '" Mr. Michael Connaghton"', 'male', '31', '0', '0', '335097', '7.75', '', 'Q\n']
    ['751', '1', '2', '" Miss. Joan Wells"', 'female', '4', '1', '1', '29103', '23', '', 'S\n']
    ['752', '1', '3', '" Master. Meier Moor"', 'male', '6', '0', '1', '392096', '12.475', 'E121', 'S\n']
    ['753', '0', '3', '" Mr. Johannes Joseph Vande Velde"', 'male', '33', '0', '0', '345780', '9.5', '', 'S\n']
    ['754', '0', '3', '" Mr. Lalio Jonkoff"', 'male', '23', '0', '0', '349204', '7.8958', '', 'S\n']
    ['755', '1', '2', '" Mrs. Samuel (Jane Laver) Herman"', 'female', '48', '1', '2', '220845', '65', '', 'S\n']
    ['756', '1', '2', '" Master. Viljo Hamalainen"', 'male', '0.67', '1', '1', '250649', '14.5', '', 'S\n']
    ['757', '0', '3', '" Mr. August Sigfrid Carlsson"', 'male', '28', '0', '0', '350042', '7.7958', '', 'S\n']
    ['758', '0', '2', '" Mr. Percy Andrew Bailey"', 'male', '18', '0', '0', '29108', '11.5', '', 'S\n']
    ['759', '0', '3', '" Mr. Thomas Leonard Theobald"', 'male', '34', '0', '0', '363294', '8.05', '', 'S\n']
    ['760', '1', '1', '" the Countess. of (Lucy Noel Martha Dyer-Edwards) Rothes"', 'female', '33', '0', '0', '110152', '86.5', 'B77', 'S\n']
    ['761', '0', '3', '" Mr. John Garfirth"', 'male', '', '0', '0', '358585', '14.5', '', 'S\n']
    ['762', '0', '3', '" Mr. Iisakki Antino Aijo Nirva"', 'male', '41', '0', '0', 'SOTON/O2 3101272', '7.125', '', 'S\n']
    ['763', '1', '3', '" Mr. Hanna Assi Barah"', 'male', '20', '0', '0', '2663', '7.2292', '', 'C\n']
    ['764', '1', '1', '" Mrs. William Ernest (Lucile Polk) Carter"', 'female', '36', '1', '2', '113760', '120', 'B96 B98', 'S\n']
    ['765', '0', '3', '" Mr. Hans Linus Eklund"', 'male', '16', '0', '0', '347074', '7.775', '', 'S\n']
    ['766', '1', '1', '" Mrs. John C (Anna Andrews) Hogeboom"', 'female', '51', '1', '0', '13502', '77.9583', 'D11', 'S\n']
    ['767', '0', '1', '" Dr. Arthur Jackson Brewe"', 'male', '', '0', '0', '112379', '39.6', '', 'C\n']
    ['768', '0', '3', '" Miss. Mary Mangan"', 'female', '30.5', '0', '0', '364850', '7.75', '', 'Q\n']
    ['769', '0', '3', '" Mr. Daniel J Moran"', 'male', '', '1', '0', '371110', '24.15', '', 'Q\n']
    ['770', '0', '3', '" Mr. Daniel Danielsen Gronnestad"', 'male', '32', '0', '0', '8471', '8.3625', '', 'S\n']
    ['771', '0', '3', '" Mr. Rene Aime Lievens"', 'male', '24', '0', '0', '345781', '9.5', '', 'S\n']
    ['772', '0', '3', '" Mr. Niels Peder Jensen"', 'male', '48', '0', '0', '350047', '7.8542', '', 'S\n']
    ['773', '0', '2', '" Mrs. (Mary) Mack"', 'female', '57', '0', '0', 'S.O./P.P. 3', '10.5', 'E77', 'S\n']
    ['774', '0', '3', '" Mr. Dibo Elias"', 'male', '', '0', '0', '2674', '7.225', '', 'C\n']
    ['775', '1', '2', '" Mrs. Elizabeth (Eliza Needs) Hocking"', 'female', '54', '1', '3', '29105', '23', '', 'S\n']
    ['776', '0', '3', '" Mr. Pehr Fabian Oliver Malkolm Myhrman"', 'male', '18', '0', '0', '347078', '7.75', '', 'S\n']
    ['777', '0', '3', '" Mr. Roger Tobin"', 'male', '', '0', '0', '383121', '7.75', 'F38', 'Q\n']
    ['778', '1', '3', '" Miss. Virginia Ethel Emanuel"', 'female', '5', '0', '0', '364516', '12.475', '', 'S\n']
    ['779', '0', '3', '" Mr. Thomas J Kilgannon"', 'male', '', '0', '0', '36865', '7.7375', '', 'Q\n']
    ['780', '1', '1', '" Mrs. Edward Scott (Elisabeth Walton McMillan) Robert"', 'female', '43', '0', '1', '24160', '211.3375', 'B3', 'S\n']
    ['781', '1', '3', '" Miss. Banoura Ayoub"', 'female', '13', '0', '0', '2687', '7.2292', '', 'C\n']
    ['782', '1', '1', '" Mrs. Albert Adrian (Vera Gillespie) Dick"', 'female', '17', '1', '0', '17474', '57', 'B20', 'S\n']
    ['783', '0', '1', '" Mr. Milton Clyde Long"', 'male', '29', '0', '0', '113501', '30', 'D6', 'S\n']
    ['784', '0', '3', '" Mr. Andrew G Johnston"', 'male', '', '1', '2', 'W./C. 6607', '23.45', '', 'S\n']
    ['785', '0', '3', '" Mr. William Ali"', 'male', '25', '0', '0', 'SOTON/O.Q. 3101312', '7.05', '', 'S\n']
    ['786', '0', '3', '" Mr. Abraham (David Lishin) Harmer"', 'male', '25', '0', '0', '374887', '7.25', '', 'S\n']
    ['787', '1', '3', '" Miss. Anna Sofia Sjoblom"', 'female', '18', '0', '0', '3101265', '7.4958', '', 'S\n']
    ['788', '0', '3', '" Master. George Hugh Rice"', 'male', '8', '4', '1', '382652', '29.125', '', 'Q\n']
    ['789', '1', '3', '" Master. Bertram Vere Dean"', 'male', '1', '1', '2', 'C.A. 2315', '20.575', '', 'S\n']
    ['790', '0', '1', '" Mr. Benjamin Guggenheim"', 'male', '46', '0', '0', 'PC 17593', '79.2', 'B82 B84', 'C\n']
    ['791', '0', '3', '" Mr. Andrew ""Andy"" Keane"', 'male', '', '0', '0', '12460', '7.75', '', 'Q\n']
    ['792', '0', '2', '" Mr. Alfred Gaskell"', 'male', '16', '0', '0', '239865', '26', '', 'S\n']
    ['793', '0', '3', '" Miss. Stella Anna Sage"', 'female', '', '8', '2', 'CA. 2343', '69.55', '', 'S\n']
    ['794', '0', '1', '" Mr. William Fisher Hoyt"', 'male', '', '0', '0', 'PC 17600', '30.6958', '', 'C\n']
    ['795', '0', '3', '" Mr. Ristiu Dantcheff"', 'male', '25', '0', '0', '349203', '7.8958', '', 'S\n']
    ['796', '0', '2', '" Mr. Richard Otter"', 'male', '39', '0', '0', '28213', '13', '', 'S\n']
    ['797', '1', '1', '" Dr. Alice (Farnham) Leader"', 'female', '49', '0', '0', '17465', '25.9292', 'D17', 'S\n']
    ['798', '1', '3', '" Mrs. Mara Osman"', 'female', '31', '0', '0', '349244', '8.6833', '', 'S\n']
    ['799', '0', '3', '" Mr. Yousseff Ibrahim Shawah"', 'male', '30', '0', '0', '2685', '7.2292', '', 'C\n']
    ['800', '0', '3', '" Mrs. Jean Baptiste (Rosalie Paula Govaert) Van Impe"', 'female', '30', '1', '1', '345773', '24.15', '', 'S\n']
    ['801', '0', '2', '" Mr. Martin Ponesell"', 'male', '34', '0', '0', '250647', '13', '', 'S\n']
    ['802', '1', '2', '" Mrs. Harvey (Charlotte Annie Tate) Collyer"', 'female', '31', '1', '1', 'C.A. 31921', '26.25', '', 'S\n']
    ['803', '1', '1', '" Master. William Thornton II Carter"', 'male', '11', '1', '2', '113760', '120', 'B96 B98', 'S\n']
    ['804', '1', '3', '" Master. Assad Alexander Thomas"', 'male', '0.42', '0', '1', '2625', '8.5167', '', 'C\n']
    ['805', '1', '3', '" Mr. Oskar Arvid Hedman"', 'male', '27', '0', '0', '347089', '6.975', '', 'S\n']
    ['806', '0', '3', '" Mr. Karl Johan Johansson"', 'male', '31', '0', '0', '347063', '7.775', '', 'S\n']
    ['807', '0', '1', '" Mr. Thomas Jr Andrews"', 'male', '39', '0', '0', '112050', '0', 'A36', 'S\n']
    ['808', '0', '3', '" Miss. Ellen Natalia Pettersson"', 'female', '18', '0', '0', '347087', '7.775', '', 'S\n']
    ['809', '0', '2', '" Mr. August Meyer"', 'male', '39', '0', '0', '248723', '13', '', 'S\n']
    ['810', '1', '1', '" Mrs. Norman Campbell (Bertha Griggs) Chambers"', 'female', '33', '1', '0', '113806', '53.1', 'E8', 'S\n']
    ['811', '0', '3', '" Mr. William Alexander"', 'male', '26', '0', '0', '3474', '7.8875', '', 'S\n']
    ['812', '0', '3', '" Mr. James Lester"', 'male', '39', '0', '0', 'A/4 48871', '24.15', '', 'S\n']
    ['813', '0', '2', '" Mr. Richard James Slemen"', 'male', '35', '0', '0', '28206', '10.5', '', 'S\n']
    ['814', '0', '3', '" Miss. Ebba Iris Alfrida Andersson"', 'female', '6', '4', '2', '347082', '31.275', '', 'S\n']
    ['815', '0', '3', '" Mr. Ernest Portage Tomlin"', 'male', '30.5', '0', '0', '364499', '8.05', '', 'S\n']
    ['816', '0', '1', '" Mr. Richard Fry"', 'male', '', '0', '0', '112058', '0', 'B102', 'S\n']
    ['817', '0', '3', '" Miss. Wendla Maria Heininen"', 'female', '23', '0', '0', 'STON/O2. 3101290', '7.925', '', 'S\n']
    ['818', '0', '2', '" Mr. Albert Mallet"', 'male', '31', '1', '1', 'S.C./PARIS 2079', '37.0042', '', 'C\n']
    ['819', '0', '3', '" Mr. John Fredrik Alexander Holm"', 'male', '43', '0', '0', 'C 7075', '6.45', '', 'S\n']
    ['820', '0', '3', '" Master. Karl Thorsten Skoog"', 'male', '10', '3', '2', '347088', '27.9', '', 'S\n']
    ['821', '1', '1', '" Mrs. Charles Melville (Clara Jennings Gregg) Hays"', 'female', '52', '1', '1', '12749', '93.5', 'B69', 'S\n']
    ['822', '1', '3', '" Mr. Nikola Lulic"', 'male', '27', '0', '0', '315098', '8.6625', '', 'S\n']
    ['823', '0', '1', '" Jonkheer. John George Reuchlin"', 'male', '38', '0', '0', '19972', '0', '', 'S\n']
    ['824', '1', '3', '" Mrs. (Beila) Moor"', 'female', '27', '0', '1', '392096', '12.475', 'E121', 'S\n']
    ['825', '0', '3', '" Master. Urho Abraham Panula"', 'male', '2', '4', '1', '3101295', '39.6875', '', 'S\n']
    ['826', '0', '3', '" Mr. John Flynn"', 'male', '', '0', '0', '368323', '6.95', '', 'Q\n']
    ['827', '0', '3', '" Mr. Len Lam"', 'male', '', '0', '0', '1601', '56.4958', '', 'S\n']
    ['828', '1', '2', '" Master. Andre Mallet"', 'male', '1', '0', '2', 'S.C./PARIS 2079', '37.0042', '', 'C\n']
    ['829', '1', '3', '" Mr. Thomas Joseph McCormack"', 'male', '', '0', '0', '367228', '7.75', '', 'Q\n']
    ['830', '1', '1', '" Mrs. George Nelson (Martha Evelyn) Stone"', 'female', '62', '0', '0', '113572', '80', 'B28', '\n']
    ['831', '1', '3', '" Mrs. Antoni (Selini Alexander) Yasbeck"', 'female', '15', '1', '0', '2659', '14.4542', '', 'C\n']
    ['832', '1', '2', '" Master. George Sibley Richards"', 'male', '0.83', '1', '1', '29106', '18.75', '', 'S\n']
    ['833', '0', '3', '" Mr. Amin Saad"', 'male', '', '0', '0', '2671', '7.2292', '', 'C\n']
    ['834', '0', '3', '" Mr. Albert Augustsson"', 'male', '23', '0', '0', '347468', '7.8542', '', 'S\n']
    ['835', '0', '3', '" Mr. Owen George Allum"', 'male', '18', '0', '0', '2223', '8.3', '', 'S\n']
    ['836', '1', '1', '" Miss. Sara Rebecca Compton"', 'female', '39', '1', '1', 'PC 17756', '83.1583', 'E49', 'C\n']
    ['837', '0', '3', '" Mr. Jakob Pasic"', 'male', '21', '0', '0', '315097', '8.6625', '', 'S\n']
    ['838', '0', '3', '" Mr. Maurice Sirota"', 'male', '', '0', '0', '392092', '8.05', '', 'S\n']
    ['839', '1', '3', '" Mr. Chang Chip"', 'male', '32', '0', '0', '1601', '56.4958', '', 'S\n']
    ['840', '1', '1', '" Mr. Pierre Marechal"', 'male', '', '0', '0', '11774', '29.7', 'C47', 'C\n']
    ['841', '0', '3', '" Mr. Ilmari Rudolf Alhomaki"', 'male', '20', '0', '0', 'SOTON/O2 3101287', '7.925', '', 'S\n']
    ['842', '0', '2', '" Mr. Thomas Charles Mudd"', 'male', '16', '0', '0', 'S.O./P.P. 3', '10.5', '', 'S\n']
    ['843', '1', '1', '" Miss. Augusta Serepeca"', 'female', '30', '0', '0', '113798', '31', '', 'C\n']
    ['844', '0', '3', '" Mr. Peter L Lemberopolous"', 'male', '34.5', '0', '0', '2683', '6.4375', '', 'C\n']
    ['845', '0', '3', '" Mr. Jeso Culumovic"', 'male', '17', '0', '0', '315090', '8.6625', '', 'S\n']
    ['846', '0', '3', '" Mr. Anthony Abbing"', 'male', '42', '0', '0', 'C.A. 5547', '7.55', '', 'S\n']
    ['847', '0', '3', '" Mr. Douglas Bullen Sage"', 'male', '', '8', '2', 'CA. 2343', '69.55', '', 'S\n']
    ['848', '0', '3', '" Mr. Marin Markoff"', 'male', '35', '0', '0', '349213', '7.8958', '', 'C\n']
    ['849', '0', '2', '" Rev. John Harper"', 'male', '28', '0', '1', '248727', '33', '', 'S\n']
    ['850', '1', '1', '" Mrs. Samuel L (Edwiga Grabowska) Goldenberg"', 'female', '', '1', '0', '17453', '89.1042', 'C92', 'C\n']
    ['851', '0', '3', '" Master. Sigvard Harald Elias Andersson"', 'male', '4', '4', '2', '347082', '31.275', '', 'S\n']
    ['852', '0', '3', '" Mr. Johan Svensson"', 'male', '74', '0', '0', '347060', '7.775', '', 'S\n']
    ['853', '0', '3', '" Miss. Nourelain Boulos"', 'female', '9', '1', '1', '2678', '15.2458', '', 'C\n']
    ['854', '1', '1', '" Miss. Mary Conover Lines"', 'female', '16', '0', '1', 'PC 17592', '39.4', 'D28', 'S\n']
    ['855', '0', '2', '" Mrs. Ernest Courtenay (Lilian Hughes) Carter"', 'female', '44', '1', '0', '244252', '26', '', 'S\n']
    ['856', '1', '3', '" Mrs. Sam (Leah Rosen) Aks"', 'female', '18', '0', '1', '392091', '9.35', '', 'S\n']
    ['857', '1', '1', '" Mrs. George Dennick (Mary Hitchcock) Wick"', 'female', '45', '1', '1', '36928', '164.8667', '', 'S\n']
    ['858', '1', '1', '" Mr. Peter Denis  Daly"', 'male', '51', '0', '0', '113055', '26.55', 'E17', 'S\n']
    ['859', '1', '3', '" Mrs. Solomon (Latifa Qurban) Baclini"', 'female', '24', '0', '3', '2666', '19.2583', '', 'C\n']
    ['860', '0', '3', '" Mr. Raihed Razi"', 'male', '', '0', '0', '2629', '7.2292', '', 'C\n']
    ['861', '0', '3', '" Mr. Claus Peter Hansen"', 'male', '41', '2', '0', '350026', '14.1083', '', 'S\n']
    ['862', '0', '2', '" Mr. Frederick Edward Giles"', 'male', '21', '1', '0', '28134', '11.5', '', 'S\n']
    ['863', '1', '1', '" Mrs. Frederick Joel (Margaret Welles Barron) Swift"', 'female', '48', '0', '0', '17466', '25.9292', 'D17', 'S\n']
    ['864', '0', '3', '" Miss. Dorothy Edith ""Dolly"" Sage"', 'female', '', '8', '2', 'CA. 2343', '69.55', '', 'S\n']
    ['865', '0', '2', '" Mr. John William Gill"', 'male', '24', '0', '0', '233866', '13', '', 'S\n']
    ['866', '1', '2', '" Mrs. (Karolina) Bystrom"', 'female', '42', '0', '0', '236852', '13', '', 'S\n']
    ['867', '1', '2', '" Miss. Asuncion Duran y More"', 'female', '27', '1', '0', 'SC/PARIS 2149', '13.8583', '', 'C\n']
    ['868', '0', '1', '" Mr. Washington Augustus II Roebling"', 'male', '31', '0', '0', 'PC 17590', '50.4958', 'A24', 'S\n']
    ['869', '0', '3', '" Mr. Philemon van Melkebeke"', 'male', '', '0', '0', '345777', '9.5', '', 'S\n']
    ['870', '1', '3', '" Master. Harold Theodor Johnson"', 'male', '4', '1', '1', '347742', '11.1333', '', 'S\n']
    ['871', '0', '3', '" Mr. Cerin Balkic"', 'male', '26', '0', '0', '349248', '7.8958', '', 'S\n']
    ['872', '1', '1', '" Mrs. Richard Leonard (Sallie Monypeny) Beckwith"', 'female', '47', '1', '1', '11751', '52.5542', 'D35', 'S\n']
    ['873', '0', '1', '" Mr. Frans Olof Carlsson"', 'male', '33', '0', '0', '695', '5', 'B51 B53 B55', 'S\n']
    ['874', '0', '3', '" Mr. Victor Vander Cruyssen"', 'male', '47', '0', '0', '345765', '9', '', 'S\n']
    ['875', '1', '2', '" Mrs. Samuel (Hannah Wizosky) Abelson"', 'female', '28', '1', '0', 'P/PP 3381', '24', '', 'C\n']
    ['876', '1', '3', '" Miss. Adele Kiamie ""Jane"" Najib"', 'female', '15', '0', '0', '2667', '7.225', '', 'C\n']
    ['877', '0', '3', '" Mr. Alfred Ossian Gustafsson"', 'male', '20', '0', '0', '7534', '9.8458', '', 'S\n']
    ['878', '0', '3', '" Mr. Nedelio Petroff"', 'male', '19', '0', '0', '349212', '7.8958', '', 'S\n']
    ['879', '0', '3', '" Mr. Kristo Laleff"', 'male', '', '0', '0', '349217', '7.8958', '', 'S\n']
    ['880', '1', '1', '" Mrs. Thomas Jr (Lily Alexenia Wilson) Potter"', 'female', '56', '0', '1', '11767', '83.1583', 'C50', 'C\n']
    ['881', '1', '2', '" Mrs. William (Imanita Parrish Hall) Shelley"', 'female', '25', '0', '1', '230433', '26', '', 'S\n']
    ['882', '0', '3', '" Mr. Johann Markun"', 'male', '33', '0', '0', '349257', '7.8958', '', 'S\n']
    ['883', '0', '3', '" Miss. Gerda Ulrika Dahlberg"', 'female', '22', '0', '0', '7552', '10.5167', '', 'S\n']
    ['884', '0', '2', '" Mr. Frederick James Banfield"', 'male', '28', '0', '0', 'C.A./SOTON 34068', '10.5', '', 'S\n']
    ['885', '0', '3', '" Mr. Henry Jr Sutehall"', 'male', '25', '0', '0', 'SOTON/OQ 392076', '7.05', '', 'S\n']
    ['886', '0', '3', '" Mrs. William (Margaret Norton) Rice"', 'female', '39', '0', '5', '382652', '29.125', '', 'Q\n']
    ['887', '0', '2', '" Rev. Juozas Montvila"', 'male', '27', '0', '0', '211536', '13', '', 'S\n']
    ['888', '1', '1', '" Miss. Margaret Edith Graham"', 'female', '19', '0', '0', '112053', '30', 'B42', 'S\n']
    ['889', '0', '3', '" Miss. Catherine Helen ""Carrie"" Johnston"', 'female', '', '1', '2', 'W./C. 6607', '23.45', '', 'S\n']
    ['890', '1', '1', '" Mr. Karl Howell Behr"', 'male', '26', '0', '0', '111369', '30', 'C148', 'C\n']
    ['891', '0', '3', '" Mr. Patrick Dooley"', 'male', '32', '0', '0', '370376', '7.75', '', 'Q\n']
    

### Tratanto Listas


```python
dados_tratados = []

for dado in linhas[1:]:
    dado_tratado = tratar_nome(dado)
    dado_como_lista = dado_tratado.split(',')
    dados_tratados.append(dado_como_lista)

```


```python
print(dados_tratados[0][3])
```

    " Mr. Owen Harris Braund"
    


```python
# 1 - Pego cada linha da variavel dados_tratados e coloco em passageiro
# 2 - faço um for em passageiro e pego o indice e o restante dos dados
# 3 - vou na variavel coluna e pego a coluna no respectivo indice
for passageiro in dados_tratados:
    print(passageiro)
    for indice, dado in enumerate(passageiro):
        print(indice,dado)
    print("----------------------------")
```

    ['1', '0', '3', '" Mr. Owen Harris Braund"', 'male', '22', '1', '0', 'A/5 21171', '7.25', '', 'S\n']
    0 1
    1 0
    2 3
    3 " Mr. Owen Harris Braund"
    4 male
    5 22
    6 1
    7 0
    8 A/5 21171
    9 7.25
    10 
    11 S
    
    ----------------------------
    ['2', '1', '1', '" Mrs. John Bradley (Florence Briggs Thayer) Cumings"', 'female', '38', '1', '0', 'PC 17599', '71.2833', 'C85', 'C\n']
    0 2
    1 1
    2 1
    3 " Mrs. John Bradley (Florence Briggs Thayer) Cumings"
    4 female
    5 38
    6 1
    7 0
    8 PC 17599
    9 71.2833
    10 C85
    11 C
    
    ----------------------------
    ['3', '1', '3', '" Miss. Laina Heikkinen"', 'female', '26', '0', '0', 'STON/O2. 3101282', '7.925', '', 'S\n']
    0 3
    1 1
    2 3
    3 " Miss. Laina Heikkinen"
    4 female
    5 26
    6 0
    7 0
    8 STON/O2. 3101282
    9 7.925
    10 
    11 S
    
    ----------------------------
    ['4', '1', '1', '" Mrs. Jacques Heath (Lily May Peel) Futrelle"', 'female', '35', '1', '0', '113803', '53.1', 'C123', 'S\n']
    0 4
    1 1
    2 1
    3 " Mrs. Jacques Heath (Lily May Peel) Futrelle"
    4 female
    5 35
    6 1
    7 0
    8 113803
    9 53.1
    10 C123
    11 S
    
    ----------------------------
    ['5', '0', '3', '" Mr. William Henry Allen"', 'male', '35', '0', '0', '373450', '8.05', '', 'S\n']
    0 5
    1 0
    2 3
    3 " Mr. William Henry Allen"
    4 male
    5 35
    6 0
    7 0
    8 373450
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['6', '0', '3', '" Mr. James Moran"', 'male', '', '0', '0', '330877', '8.4583', '', 'Q\n']
    0 6
    1 0
    2 3
    3 " Mr. James Moran"
    4 male
    5 
    6 0
    7 0
    8 330877
    9 8.4583
    10 
    11 Q
    
    ----------------------------
    ['7', '0', '1', '" Mr. Timothy J McCarthy"', 'male', '54', '0', '0', '17463', '51.8625', 'E46', 'S\n']
    0 7
    1 0
    2 1
    3 " Mr. Timothy J McCarthy"
    4 male
    5 54
    6 0
    7 0
    8 17463
    9 51.8625
    10 E46
    11 S
    
    ----------------------------
    ['8', '0', '3', '" Master. Gosta Leonard Palsson"', 'male', '2', '3', '1', '349909', '21.075', '', 'S\n']
    0 8
    1 0
    2 3
    3 " Master. Gosta Leonard Palsson"
    4 male
    5 2
    6 3
    7 1
    8 349909
    9 21.075
    10 
    11 S
    
    ----------------------------
    ['9', '1', '3', '" Mrs. Oscar W (Elisabeth Vilhelmina Berg) Johnson"', 'female', '27', '0', '2', '347742', '11.1333', '', 'S\n']
    0 9
    1 1
    2 3
    3 " Mrs. Oscar W (Elisabeth Vilhelmina Berg) Johnson"
    4 female
    5 27
    6 0
    7 2
    8 347742
    9 11.1333
    10 
    11 S
    
    ----------------------------
    ['10', '1', '2', '" Mrs. Nicholas (Adele Achem) Nasser"', 'female', '14', '1', '0', '237736', '30.0708', '', 'C\n']
    0 10
    1 1
    2 2
    3 " Mrs. Nicholas (Adele Achem) Nasser"
    4 female
    5 14
    6 1
    7 0
    8 237736
    9 30.0708
    10 
    11 C
    
    ----------------------------
    ['11', '1', '3', '" Miss. Marguerite Rut Sandstrom"', 'female', '4', '1', '1', 'PP 9549', '16.7', 'G6', 'S\n']
    0 11
    1 1
    2 3
    3 " Miss. Marguerite Rut Sandstrom"
    4 female
    5 4
    6 1
    7 1
    8 PP 9549
    9 16.7
    10 G6
    11 S
    
    ----------------------------
    ['12', '1', '1', '" Miss. Elizabeth Bonnell"', 'female', '58', '0', '0', '113783', '26.55', 'C103', 'S\n']
    0 12
    1 1
    2 1
    3 " Miss. Elizabeth Bonnell"
    4 female
    5 58
    6 0
    7 0
    8 113783
    9 26.55
    10 C103
    11 S
    
    ----------------------------
    ['13', '0', '3', '" Mr. William Henry Saundercock"', 'male', '20', '0', '0', 'A/5. 2151', '8.05', '', 'S\n']
    0 13
    1 0
    2 3
    3 " Mr. William Henry Saundercock"
    4 male
    5 20
    6 0
    7 0
    8 A/5. 2151
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['14', '0', '3', '" Mr. Anders Johan Andersson"', 'male', '39', '1', '5', '347082', '31.275', '', 'S\n']
    0 14
    1 0
    2 3
    3 " Mr. Anders Johan Andersson"
    4 male
    5 39
    6 1
    7 5
    8 347082
    9 31.275
    10 
    11 S
    
    ----------------------------
    ['15', '0', '3', '" Miss. Hulda Amanda Adolfina Vestrom"', 'female', '14', '0', '0', '350406', '7.8542', '', 'S\n']
    0 15
    1 0
    2 3
    3 " Miss. Hulda Amanda Adolfina Vestrom"
    4 female
    5 14
    6 0
    7 0
    8 350406
    9 7.8542
    10 
    11 S
    
    ----------------------------
    ['16', '1', '2', '" Mrs. (Mary D Kingcome)  Hewlett"', 'female', '55', '0', '0', '248706', '16', '', 'S\n']
    0 16
    1 1
    2 2
    3 " Mrs. (Mary D Kingcome)  Hewlett"
    4 female
    5 55
    6 0
    7 0
    8 248706
    9 16
    10 
    11 S
    
    ----------------------------
    ['17', '0', '3', '" Master. Eugene Rice"', 'male', '2', '4', '1', '382652', '29.125', '', 'Q\n']
    0 17
    1 0
    2 3
    3 " Master. Eugene Rice"
    4 male
    5 2
    6 4
    7 1
    8 382652
    9 29.125
    10 
    11 Q
    
    ----------------------------
    ['18', '1', '2', '" Mr. Charles Eugene Williams"', 'male', '', '0', '0', '244373', '13', '', 'S\n']
    0 18
    1 1
    2 2
    3 " Mr. Charles Eugene Williams"
    4 male
    5 
    6 0
    7 0
    8 244373
    9 13
    10 
    11 S
    
    ----------------------------
    ['19', '0', '3', '" Mrs. Julius (Emelia Maria Vandemoortele) Vander Planke"', 'female', '31', '1', '0', '345763', '18', '', 'S\n']
    0 19
    1 0
    2 3
    3 " Mrs. Julius (Emelia Maria Vandemoortele) Vander Planke"
    4 female
    5 31
    6 1
    7 0
    8 345763
    9 18
    10 
    11 S
    
    ----------------------------
    ['20', '1', '3', '" Mrs. Fatima Masselmani"', 'female', '', '0', '0', '2649', '7.225', '', 'C\n']
    0 20
    1 1
    2 3
    3 " Mrs. Fatima Masselmani"
    4 female
    5 
    6 0
    7 0
    8 2649
    9 7.225
    10 
    11 C
    
    ----------------------------
    ['21', '0', '2', '" Mr. Joseph J Fynney"', 'male', '35', '0', '0', '239865', '26', '', 'S\n']
    0 21
    1 0
    2 2
    3 " Mr. Joseph J Fynney"
    4 male
    5 35
    6 0
    7 0
    8 239865
    9 26
    10 
    11 S
    
    ----------------------------
    ['22', '1', '2', '" Mr. Lawrence Beesley"', 'male', '34', '0', '0', '248698', '13', 'D56', 'S\n']
    0 22
    1 1
    2 2
    3 " Mr. Lawrence Beesley"
    4 male
    5 34
    6 0
    7 0
    8 248698
    9 13
    10 D56
    11 S
    
    ----------------------------
    ['23', '1', '3', '" Miss. Anna ""Annie"" McGowan"', 'female', '15', '0', '0', '330923', '8.0292', '', 'Q\n']
    0 23
    1 1
    2 3
    3 " Miss. Anna ""Annie"" McGowan"
    4 female
    5 15
    6 0
    7 0
    8 330923
    9 8.0292
    10 
    11 Q
    
    ----------------------------
    ['24', '1', '1', '" Mr. William Thompson Sloper"', 'male', '28', '0', '0', '113788', '35.5', 'A6', 'S\n']
    0 24
    1 1
    2 1
    3 " Mr. William Thompson Sloper"
    4 male
    5 28
    6 0
    7 0
    8 113788
    9 35.5
    10 A6
    11 S
    
    ----------------------------
    ['25', '0', '3', '" Miss. Torborg Danira Palsson"', 'female', '8', '3', '1', '349909', '21.075', '', 'S\n']
    0 25
    1 0
    2 3
    3 " Miss. Torborg Danira Palsson"
    4 female
    5 8
    6 3
    7 1
    8 349909
    9 21.075
    10 
    11 S
    
    ----------------------------
    ['26', '1', '3', '" Mrs. Carl Oscar (Selma Augusta Emilia Johansson) Asplund"', 'female', '38', '1', '5', '347077', '31.3875', '', 'S\n']
    0 26
    1 1
    2 3
    3 " Mrs. Carl Oscar (Selma Augusta Emilia Johansson) Asplund"
    4 female
    5 38
    6 1
    7 5
    8 347077
    9 31.3875
    10 
    11 S
    
    ----------------------------
    ['27', '0', '3', '" Mr. Farred Chehab Emir"', 'male', '', '0', '0', '2631', '7.225', '', 'C\n']
    0 27
    1 0
    2 3
    3 " Mr. Farred Chehab Emir"
    4 male
    5 
    6 0
    7 0
    8 2631
    9 7.225
    10 
    11 C
    
    ----------------------------
    ['28', '0', '1', '" Mr. Charles Alexander Fortune"', 'male', '19', '3', '2', '19950', '263', 'C23 C25 C27', 'S\n']
    0 28
    1 0
    2 1
    3 " Mr. Charles Alexander Fortune"
    4 male
    5 19
    6 3
    7 2
    8 19950
    9 263
    10 C23 C25 C27
    11 S
    
    ----------------------------
    ['29', '1', '3', '" Miss. Ellen ""Nellie"" O\'Dwyer"', 'female', '', '0', '0', '330959', '7.8792', '', 'Q\n']
    0 29
    1 1
    2 3
    3 " Miss. Ellen ""Nellie"" O'Dwyer"
    4 female
    5 
    6 0
    7 0
    8 330959
    9 7.8792
    10 
    11 Q
    
    ----------------------------
    ['30', '0', '3', '" Mr. Lalio Todoroff"', 'male', '', '0', '0', '349216', '7.8958', '', 'S\n']
    0 30
    1 0
    2 3
    3 " Mr. Lalio Todoroff"
    4 male
    5 
    6 0
    7 0
    8 349216
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['31', '0', '1', '" Don. Manuel E Uruchurtu"', 'male', '40', '0', '0', 'PC 17601', '27.7208', '', 'C\n']
    0 31
    1 0
    2 1
    3 " Don. Manuel E Uruchurtu"
    4 male
    5 40
    6 0
    7 0
    8 PC 17601
    9 27.7208
    10 
    11 C
    
    ----------------------------
    ['32', '1', '1', '" Mrs. William Augustus (Marie Eugenie) Spencer"', 'female', '', '1', '0', 'PC 17569', '146.5208', 'B78', 'C\n']
    0 32
    1 1
    2 1
    3 " Mrs. William Augustus (Marie Eugenie) Spencer"
    4 female
    5 
    6 1
    7 0
    8 PC 17569
    9 146.5208
    10 B78
    11 C
    
    ----------------------------
    ['33', '1', '3', '" Miss. Mary Agatha Glynn"', 'female', '', '0', '0', '335677', '7.75', '', 'Q\n']
    0 33
    1 1
    2 3
    3 " Miss. Mary Agatha Glynn"
    4 female
    5 
    6 0
    7 0
    8 335677
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['34', '0', '2', '" Mr. Edward H Wheadon"', 'male', '66', '0', '0', 'C.A. 24579', '10.5', '', 'S\n']
    0 34
    1 0
    2 2
    3 " Mr. Edward H Wheadon"
    4 male
    5 66
    6 0
    7 0
    8 C.A. 24579
    9 10.5
    10 
    11 S
    
    ----------------------------
    ['35', '0', '1', '" Mr. Edgar Joseph Meyer"', 'male', '28', '1', '0', 'PC 17604', '82.1708', '', 'C\n']
    0 35
    1 0
    2 1
    3 " Mr. Edgar Joseph Meyer"
    4 male
    5 28
    6 1
    7 0
    8 PC 17604
    9 82.1708
    10 
    11 C
    
    ----------------------------
    ['36', '0', '1', '" Mr. Alexander Oskar Holverson"', 'male', '42', '1', '0', '113789', '52', '', 'S\n']
    0 36
    1 0
    2 1
    3 " Mr. Alexander Oskar Holverson"
    4 male
    5 42
    6 1
    7 0
    8 113789
    9 52
    10 
    11 S
    
    ----------------------------
    ['37', '1', '3', '" Mr. Hanna Mamee"', 'male', '', '0', '0', '2677', '7.2292', '', 'C\n']
    0 37
    1 1
    2 3
    3 " Mr. Hanna Mamee"
    4 male
    5 
    6 0
    7 0
    8 2677
    9 7.2292
    10 
    11 C
    
    ----------------------------
    ['38', '0', '3', '" Mr. Ernest Charles Cann"', 'male', '21', '0', '0', 'A./5. 2152', '8.05', '', 'S\n']
    0 38
    1 0
    2 3
    3 " Mr. Ernest Charles Cann"
    4 male
    5 21
    6 0
    7 0
    8 A./5. 2152
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['39', '0', '3', '" Miss. Augusta Maria Vander Planke"', 'female', '18', '2', '0', '345764', '18', '', 'S\n']
    0 39
    1 0
    2 3
    3 " Miss. Augusta Maria Vander Planke"
    4 female
    5 18
    6 2
    7 0
    8 345764
    9 18
    10 
    11 S
    
    ----------------------------
    ['40', '1', '3', '" Miss. Jamila Nicola-Yarred"', 'female', '14', '1', '0', '2651', '11.2417', '', 'C\n']
    0 40
    1 1
    2 3
    3 " Miss. Jamila Nicola-Yarred"
    4 female
    5 14
    6 1
    7 0
    8 2651
    9 11.2417
    10 
    11 C
    
    ----------------------------
    ['41', '0', '3', '" Mrs. Johan (Johanna Persdotter Larsson) Ahlin"', 'female', '40', '1', '0', '7546', '9.475', '', 'S\n']
    0 41
    1 0
    2 3
    3 " Mrs. Johan (Johanna Persdotter Larsson) Ahlin"
    4 female
    5 40
    6 1
    7 0
    8 7546
    9 9.475
    10 
    11 S
    
    ----------------------------
    ['42', '0', '2', '" Mrs. William John Robert (Dorothy Ann Wonnacott) Turpin"', 'female', '27', '1', '0', '11668', '21', '', 'S\n']
    0 42
    1 0
    2 2
    3 " Mrs. William John Robert (Dorothy Ann Wonnacott) Turpin"
    4 female
    5 27
    6 1
    7 0
    8 11668
    9 21
    10 
    11 S
    
    ----------------------------
    ['43', '0', '3', '" Mr. Theodor Kraeff"', 'male', '', '0', '0', '349253', '7.8958', '', 'C\n']
    0 43
    1 0
    2 3
    3 " Mr. Theodor Kraeff"
    4 male
    5 
    6 0
    7 0
    8 349253
    9 7.8958
    10 
    11 C
    
    ----------------------------
    ['44', '1', '2', '" Miss. Simonne Marie Anne Andree Laroche"', 'female', '3', '1', '2', 'SC/Paris 2123', '41.5792', '', 'C\n']
    0 44
    1 1
    2 2
    3 " Miss. Simonne Marie Anne Andree Laroche"
    4 female
    5 3
    6 1
    7 2
    8 SC/Paris 2123
    9 41.5792
    10 
    11 C
    
    ----------------------------
    ['45', '1', '3', '" Miss. Margaret Delia Devaney"', 'female', '19', '0', '0', '330958', '7.8792', '', 'Q\n']
    0 45
    1 1
    2 3
    3 " Miss. Margaret Delia Devaney"
    4 female
    5 19
    6 0
    7 0
    8 330958
    9 7.8792
    10 
    11 Q
    
    ----------------------------
    ['46', '0', '3', '" Mr. William John Rogers"', 'male', '', '0', '0', 'S.C./A.4. 23567', '8.05', '', 'S\n']
    0 46
    1 0
    2 3
    3 " Mr. William John Rogers"
    4 male
    5 
    6 0
    7 0
    8 S.C./A.4. 23567
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['47', '0', '3', '" Mr. Denis Lennon"', 'male', '', '1', '0', '370371', '15.5', '', 'Q\n']
    0 47
    1 0
    2 3
    3 " Mr. Denis Lennon"
    4 male
    5 
    6 1
    7 0
    8 370371
    9 15.5
    10 
    11 Q
    
    ----------------------------
    ['48', '1', '3', '" Miss. Bridget O\'Driscoll"', 'female', '', '0', '0', '14311', '7.75', '', 'Q\n']
    0 48
    1 1
    2 3
    3 " Miss. Bridget O'Driscoll"
    4 female
    5 
    6 0
    7 0
    8 14311
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['49', '0', '3', '" Mr. Youssef Samaan"', 'male', '', '2', '0', '2662', '21.6792', '', 'C\n']
    0 49
    1 0
    2 3
    3 " Mr. Youssef Samaan"
    4 male
    5 
    6 2
    7 0
    8 2662
    9 21.6792
    10 
    11 C
    
    ----------------------------
    ['50', '0', '3', '" Mrs. Josef (Josefine Franchi) Arnold-Franchi"', 'female', '18', '1', '0', '349237', '17.8', '', 'S\n']
    0 50
    1 0
    2 3
    3 " Mrs. Josef (Josefine Franchi) Arnold-Franchi"
    4 female
    5 18
    6 1
    7 0
    8 349237
    9 17.8
    10 
    11 S
    
    ----------------------------
    ['51', '0', '3', '" Master. Juha Niilo Panula"', 'male', '7', '4', '1', '3101295', '39.6875', '', 'S\n']
    0 51
    1 0
    2 3
    3 " Master. Juha Niilo Panula"
    4 male
    5 7
    6 4
    7 1
    8 3101295
    9 39.6875
    10 
    11 S
    
    ----------------------------
    ['52', '0', '3', '" Mr. Richard Cater Nosworthy"', 'male', '21', '0', '0', 'A/4. 39886', '7.8', '', 'S\n']
    0 52
    1 0
    2 3
    3 " Mr. Richard Cater Nosworthy"
    4 male
    5 21
    6 0
    7 0
    8 A/4. 39886
    9 7.8
    10 
    11 S
    
    ----------------------------
    ['53', '1', '1', '" Mrs. Henry Sleeper (Myna Haxtun) Harper"', 'female', '49', '1', '0', 'PC 17572', '76.7292', 'D33', 'C\n']
    0 53
    1 1
    2 1
    3 " Mrs. Henry Sleeper (Myna Haxtun) Harper"
    4 female
    5 49
    6 1
    7 0
    8 PC 17572
    9 76.7292
    10 D33
    11 C
    
    ----------------------------
    ['54', '1', '2', '" Mrs. Lizzie (Elizabeth Anne Wilkinson) Faunthorpe"', 'female', '29', '1', '0', '2926', '26', '', 'S\n']
    0 54
    1 1
    2 2
    3 " Mrs. Lizzie (Elizabeth Anne Wilkinson) Faunthorpe"
    4 female
    5 29
    6 1
    7 0
    8 2926
    9 26
    10 
    11 S
    
    ----------------------------
    ['55', '0', '1', '" Mr. Engelhart Cornelius Ostby"', 'male', '65', '0', '1', '113509', '61.9792', 'B30', 'C\n']
    0 55
    1 0
    2 1
    3 " Mr. Engelhart Cornelius Ostby"
    4 male
    5 65
    6 0
    7 1
    8 113509
    9 61.9792
    10 B30
    11 C
    
    ----------------------------
    ['56', '1', '1', '" Mr. Hugh Woolner"', 'male', '', '0', '0', '19947', '35.5', 'C52', 'S\n']
    0 56
    1 1
    2 1
    3 " Mr. Hugh Woolner"
    4 male
    5 
    6 0
    7 0
    8 19947
    9 35.5
    10 C52
    11 S
    
    ----------------------------
    ['57', '1', '2', '" Miss. Emily Rugg"', 'female', '21', '0', '0', 'C.A. 31026', '10.5', '', 'S\n']
    0 57
    1 1
    2 2
    3 " Miss. Emily Rugg"
    4 female
    5 21
    6 0
    7 0
    8 C.A. 31026
    9 10.5
    10 
    11 S
    
    ----------------------------
    ['58', '0', '3', '" Mr. Mansouer Novel"', 'male', '28.5', '0', '0', '2697', '7.2292', '', 'C\n']
    0 58
    1 0
    2 3
    3 " Mr. Mansouer Novel"
    4 male
    5 28.5
    6 0
    7 0
    8 2697
    9 7.2292
    10 
    11 C
    
    ----------------------------
    ['59', '1', '2', '" Miss. Constance Mirium West"', 'female', '5', '1', '2', 'C.A. 34651', '27.75', '', 'S\n']
    0 59
    1 1
    2 2
    3 " Miss. Constance Mirium West"
    4 female
    5 5
    6 1
    7 2
    8 C.A. 34651
    9 27.75
    10 
    11 S
    
    ----------------------------
    ['60', '0', '3', '" Master. William Frederick Goodwin"', 'male', '11', '5', '2', 'CA 2144', '46.9', '', 'S\n']
    0 60
    1 0
    2 3
    3 " Master. William Frederick Goodwin"
    4 male
    5 11
    6 5
    7 2
    8 CA 2144
    9 46.9
    10 
    11 S
    
    ----------------------------
    ['61', '0', '3', '" Mr. Orsen Sirayanian"', 'male', '22', '0', '0', '2669', '7.2292', '', 'C\n']
    0 61
    1 0
    2 3
    3 " Mr. Orsen Sirayanian"
    4 male
    5 22
    6 0
    7 0
    8 2669
    9 7.2292
    10 
    11 C
    
    ----------------------------
    ['62', '1', '1', '" Miss. Amelie Icard"', 'female', '38', '0', '0', '113572', '80', 'B28', '\n']
    0 62
    1 1
    2 1
    3 " Miss. Amelie Icard"
    4 female
    5 38
    6 0
    7 0
    8 113572
    9 80
    10 B28
    11 
    
    ----------------------------
    ['63', '0', '1', '" Mr. Henry Birkhardt Harris"', 'male', '45', '1', '0', '36973', '83.475', 'C83', 'S\n']
    0 63
    1 0
    2 1
    3 " Mr. Henry Birkhardt Harris"
    4 male
    5 45
    6 1
    7 0
    8 36973
    9 83.475
    10 C83
    11 S
    
    ----------------------------
    ['64', '0', '3', '" Master. Harald Skoog"', 'male', '4', '3', '2', '347088', '27.9', '', 'S\n']
    0 64
    1 0
    2 3
    3 " Master. Harald Skoog"
    4 male
    5 4
    6 3
    7 2
    8 347088
    9 27.9
    10 
    11 S
    
    ----------------------------
    ['65', '0', '1', '" Mr. Albert A Stewart"', 'male', '', '0', '0', 'PC 17605', '27.7208', '', 'C\n']
    0 65
    1 0
    2 1
    3 " Mr. Albert A Stewart"
    4 male
    5 
    6 0
    7 0
    8 PC 17605
    9 27.7208
    10 
    11 C
    
    ----------------------------
    ['66', '1', '3', '" Master. Gerios Moubarek"', 'male', '', '1', '1', '2661', '15.2458', '', 'C\n']
    0 66
    1 1
    2 3
    3 " Master. Gerios Moubarek"
    4 male
    5 
    6 1
    7 1
    8 2661
    9 15.2458
    10 
    11 C
    
    ----------------------------
    ['67', '1', '2', '" Mrs. (Elizabeth Ramell) Nye"', 'female', '29', '0', '0', 'C.A. 29395', '10.5', 'F33', 'S\n']
    0 67
    1 1
    2 2
    3 " Mrs. (Elizabeth Ramell) Nye"
    4 female
    5 29
    6 0
    7 0
    8 C.A. 29395
    9 10.5
    10 F33
    11 S
    
    ----------------------------
    ['68', '0', '3', '" Mr. Ernest James Crease"', 'male', '19', '0', '0', 'S.P. 3464', '8.1583', '', 'S\n']
    0 68
    1 0
    2 3
    3 " Mr. Ernest James Crease"
    4 male
    5 19
    6 0
    7 0
    8 S.P. 3464
    9 8.1583
    10 
    11 S
    
    ----------------------------
    ['69', '1', '3', '" Miss. Erna Alexandra Andersson"', 'female', '17', '4', '2', '3101281', '7.925', '', 'S\n']
    0 69
    1 1
    2 3
    3 " Miss. Erna Alexandra Andersson"
    4 female
    5 17
    6 4
    7 2
    8 3101281
    9 7.925
    10 
    11 S
    
    ----------------------------
    ['70', '0', '3', '" Mr. Vincenz Kink"', 'male', '26', '2', '0', '315151', '8.6625', '', 'S\n']
    0 70
    1 0
    2 3
    3 " Mr. Vincenz Kink"
    4 male
    5 26
    6 2
    7 0
    8 315151
    9 8.6625
    10 
    11 S
    
    ----------------------------
    ['71', '0', '2', '" Mr. Stephen Curnow Jenkin"', 'male', '32', '0', '0', 'C.A. 33111', '10.5', '', 'S\n']
    0 71
    1 0
    2 2
    3 " Mr. Stephen Curnow Jenkin"
    4 male
    5 32
    6 0
    7 0
    8 C.A. 33111
    9 10.5
    10 
    11 S
    
    ----------------------------
    ['72', '0', '3', '" Miss. Lillian Amy Goodwin"', 'female', '16', '5', '2', 'CA 2144', '46.9', '', 'S\n']
    0 72
    1 0
    2 3
    3 " Miss. Lillian Amy Goodwin"
    4 female
    5 16
    6 5
    7 2
    8 CA 2144
    9 46.9
    10 
    11 S
    
    ----------------------------
    ['73', '0', '2', '" Mr. Ambrose Jr Hood"', 'male', '21', '0', '0', 'S.O.C. 14879', '73.5', '', 'S\n']
    0 73
    1 0
    2 2
    3 " Mr. Ambrose Jr Hood"
    4 male
    5 21
    6 0
    7 0
    8 S.O.C. 14879
    9 73.5
    10 
    11 S
    
    ----------------------------
    ['74', '0', '3', '" Mr. Apostolos Chronopoulos"', 'male', '26', '1', '0', '2680', '14.4542', '', 'C\n']
    0 74
    1 0
    2 3
    3 " Mr. Apostolos Chronopoulos"
    4 male
    5 26
    6 1
    7 0
    8 2680
    9 14.4542
    10 
    11 C
    
    ----------------------------
    ['75', '1', '3', '" Mr. Lee Bing"', 'male', '32', '0', '0', '1601', '56.4958', '', 'S\n']
    0 75
    1 1
    2 3
    3 " Mr. Lee Bing"
    4 male
    5 32
    6 0
    7 0
    8 1601
    9 56.4958
    10 
    11 S
    
    ----------------------------
    ['76', '0', '3', '" Mr. Sigurd Hansen Moen"', 'male', '25', '0', '0', '348123', '7.65', 'F G73', 'S\n']
    0 76
    1 0
    2 3
    3 " Mr. Sigurd Hansen Moen"
    4 male
    5 25
    6 0
    7 0
    8 348123
    9 7.65
    10 F G73
    11 S
    
    ----------------------------
    ['77', '0', '3', '" Mr. Ivan Staneff"', 'male', '', '0', '0', '349208', '7.8958', '', 'S\n']
    0 77
    1 0
    2 3
    3 " Mr. Ivan Staneff"
    4 male
    5 
    6 0
    7 0
    8 349208
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['78', '0', '3', '" Mr. Rahamin Haim Moutal"', 'male', '', '0', '0', '374746', '8.05', '', 'S\n']
    0 78
    1 0
    2 3
    3 " Mr. Rahamin Haim Moutal"
    4 male
    5 
    6 0
    7 0
    8 374746
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['79', '1', '2', '" Master. Alden Gates Caldwell"', 'male', '0.83', '0', '2', '248738', '29', '', 'S\n']
    0 79
    1 1
    2 2
    3 " Master. Alden Gates Caldwell"
    4 male
    5 0.83
    6 0
    7 2
    8 248738
    9 29
    10 
    11 S
    
    ----------------------------
    ['80', '1', '3', '" Miss. Elizabeth Dowdell"', 'female', '30', '0', '0', '364516', '12.475', '', 'S\n']
    0 80
    1 1
    2 3
    3 " Miss. Elizabeth Dowdell"
    4 female
    5 30
    6 0
    7 0
    8 364516
    9 12.475
    10 
    11 S
    
    ----------------------------
    ['81', '0', '3', '" Mr. Achille Waelens"', 'male', '22', '0', '0', '345767', '9', '', 'S\n']
    0 81
    1 0
    2 3
    3 " Mr. Achille Waelens"
    4 male
    5 22
    6 0
    7 0
    8 345767
    9 9
    10 
    11 S
    
    ----------------------------
    ['82', '1', '3', '" Mr. Jan Baptist Sheerlinck"', 'male', '29', '0', '0', '345779', '9.5', '', 'S\n']
    0 82
    1 1
    2 3
    3 " Mr. Jan Baptist Sheerlinck"
    4 male
    5 29
    6 0
    7 0
    8 345779
    9 9.5
    10 
    11 S
    
    ----------------------------
    ['83', '1', '3', '" Miss. Brigdet Delia McDermott"', 'female', '', '0', '0', '330932', '7.7875', '', 'Q\n']
    0 83
    1 1
    2 3
    3 " Miss. Brigdet Delia McDermott"
    4 female
    5 
    6 0
    7 0
    8 330932
    9 7.7875
    10 
    11 Q
    
    ----------------------------
    ['84', '0', '1', '" Mr. Francisco M Carrau"', 'male', '28', '0', '0', '113059', '47.1', '', 'S\n']
    0 84
    1 0
    2 1
    3 " Mr. Francisco M Carrau"
    4 male
    5 28
    6 0
    7 0
    8 113059
    9 47.1
    10 
    11 S
    
    ----------------------------
    ['85', '1', '2', '" Miss. Bertha Ilett"', 'female', '17', '0', '0', 'SO/C 14885', '10.5', '', 'S\n']
    0 85
    1 1
    2 2
    3 " Miss. Bertha Ilett"
    4 female
    5 17
    6 0
    7 0
    8 SO/C 14885
    9 10.5
    10 
    11 S
    
    ----------------------------
    ['86', '1', '3', '" Mrs. Karl Alfred (Maria Mathilda Gustafsson) Backstrom"', 'female', '33', '3', '0', '3101278', '15.85', '', 'S\n']
    0 86
    1 1
    2 3
    3 " Mrs. Karl Alfred (Maria Mathilda Gustafsson) Backstrom"
    4 female
    5 33
    6 3
    7 0
    8 3101278
    9 15.85
    10 
    11 S
    
    ----------------------------
    ['87', '0', '3', '" Mr. William Neal Ford"', 'male', '16', '1', '3', 'W./C. 6608', '34.375', '', 'S\n']
    0 87
    1 0
    2 3
    3 " Mr. William Neal Ford"
    4 male
    5 16
    6 1
    7 3
    8 W./C. 6608
    9 34.375
    10 
    11 S
    
    ----------------------------
    ['88', '0', '3', '" Mr. Selman Francis Slocovski"', 'male', '', '0', '0', 'SOTON/OQ 392086', '8.05', '', 'S\n']
    0 88
    1 0
    2 3
    3 " Mr. Selman Francis Slocovski"
    4 male
    5 
    6 0
    7 0
    8 SOTON/OQ 392086
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['89', '1', '1', '" Miss. Mabel Helen Fortune"', 'female', '23', '3', '2', '19950', '263', 'C23 C25 C27', 'S\n']
    0 89
    1 1
    2 1
    3 " Miss. Mabel Helen Fortune"
    4 female
    5 23
    6 3
    7 2
    8 19950
    9 263
    10 C23 C25 C27
    11 S
    
    ----------------------------
    ['90', '0', '3', '" Mr. Francesco Celotti"', 'male', '24', '0', '0', '343275', '8.05', '', 'S\n']
    0 90
    1 0
    2 3
    3 " Mr. Francesco Celotti"
    4 male
    5 24
    6 0
    7 0
    8 343275
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['91', '0', '3', '" Mr. Emil Christmann"', 'male', '29', '0', '0', '343276', '8.05', '', 'S\n']
    0 91
    1 0
    2 3
    3 " Mr. Emil Christmann"
    4 male
    5 29
    6 0
    7 0
    8 343276
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['92', '0', '3', '" Mr. Paul Edvin Andreasson"', 'male', '20', '0', '0', '347466', '7.8542', '', 'S\n']
    0 92
    1 0
    2 3
    3 " Mr. Paul Edvin Andreasson"
    4 male
    5 20
    6 0
    7 0
    8 347466
    9 7.8542
    10 
    11 S
    
    ----------------------------
    ['93', '0', '1', '" Mr. Herbert Fuller Chaffee"', 'male', '46', '1', '0', 'W.E.P. 5734', '61.175', 'E31', 'S\n']
    0 93
    1 0
    2 1
    3 " Mr. Herbert Fuller Chaffee"
    4 male
    5 46
    6 1
    7 0
    8 W.E.P. 5734
    9 61.175
    10 E31
    11 S
    
    ----------------------------
    ['94', '0', '3', '" Mr. Bertram Frank Dean"', 'male', '26', '1', '2', 'C.A. 2315', '20.575', '', 'S\n']
    0 94
    1 0
    2 3
    3 " Mr. Bertram Frank Dean"
    4 male
    5 26
    6 1
    7 2
    8 C.A. 2315
    9 20.575
    10 
    11 S
    
    ----------------------------
    ['95', '0', '3', '" Mr. Daniel Coxon"', 'male', '59', '0', '0', '364500', '7.25', '', 'S\n']
    0 95
    1 0
    2 3
    3 " Mr. Daniel Coxon"
    4 male
    5 59
    6 0
    7 0
    8 364500
    9 7.25
    10 
    11 S
    
    ----------------------------
    ['96', '0', '3', '" Mr. Charles Joseph Shorney"', 'male', '', '0', '0', '374910', '8.05', '', 'S\n']
    0 96
    1 0
    2 3
    3 " Mr. Charles Joseph Shorney"
    4 male
    5 
    6 0
    7 0
    8 374910
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['97', '0', '1', '" Mr. George B Goldschmidt"', 'male', '71', '0', '0', 'PC 17754', '34.6542', 'A5', 'C\n']
    0 97
    1 0
    2 1
    3 " Mr. George B Goldschmidt"
    4 male
    5 71
    6 0
    7 0
    8 PC 17754
    9 34.6542
    10 A5
    11 C
    
    ----------------------------
    ['98', '1', '1', '" Mr. William Bertram Greenfield"', 'male', '23', '0', '1', 'PC 17759', '63.3583', 'D10 D12', 'C\n']
    0 98
    1 1
    2 1
    3 " Mr. William Bertram Greenfield"
    4 male
    5 23
    6 0
    7 1
    8 PC 17759
    9 63.3583
    10 D10 D12
    11 C
    
    ----------------------------
    ['99', '1', '2', '" Mrs. John T (Ada Julia Bone) Doling"', 'female', '34', '0', '1', '231919', '23', '', 'S\n']
    0 99
    1 1
    2 2
    3 " Mrs. John T (Ada Julia Bone) Doling"
    4 female
    5 34
    6 0
    7 1
    8 231919
    9 23
    10 
    11 S
    
    ----------------------------
    ['100', '0', '2', '" Mr. Sinai Kantor"', 'male', '34', '1', '0', '244367', '26', '', 'S\n']
    0 100
    1 0
    2 2
    3 " Mr. Sinai Kantor"
    4 male
    5 34
    6 1
    7 0
    8 244367
    9 26
    10 
    11 S
    
    ----------------------------
    ['101', '0', '3', '" Miss. Matilda Petranec"', 'female', '28', '0', '0', '349245', '7.8958', '', 'S\n']
    0 101
    1 0
    2 3
    3 " Miss. Matilda Petranec"
    4 female
    5 28
    6 0
    7 0
    8 349245
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['102', '0', '3', '" Mr. Pastcho (""Pentcho"") Petroff"', 'male', '', '0', '0', '349215', '7.8958', '', 'S\n']
    0 102
    1 0
    2 3
    3 " Mr. Pastcho (""Pentcho"") Petroff"
    4 male
    5 
    6 0
    7 0
    8 349215
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['103', '0', '1', '" Mr. Richard Frasar White"', 'male', '21', '0', '1', '35281', '77.2875', 'D26', 'S\n']
    0 103
    1 0
    2 1
    3 " Mr. Richard Frasar White"
    4 male
    5 21
    6 0
    7 1
    8 35281
    9 77.2875
    10 D26
    11 S
    
    ----------------------------
    ['104', '0', '3', '" Mr. Gustaf Joel Johansson"', 'male', '33', '0', '0', '7540', '8.6542', '', 'S\n']
    0 104
    1 0
    2 3
    3 " Mr. Gustaf Joel Johansson"
    4 male
    5 33
    6 0
    7 0
    8 7540
    9 8.6542
    10 
    11 S
    
    ----------------------------
    ['105', '0', '3', '" Mr. Anders Vilhelm Gustafsson"', 'male', '37', '2', '0', '3101276', '7.925', '', 'S\n']
    0 105
    1 0
    2 3
    3 " Mr. Anders Vilhelm Gustafsson"
    4 male
    5 37
    6 2
    7 0
    8 3101276
    9 7.925
    10 
    11 S
    
    ----------------------------
    ['106', '0', '3', '" Mr. Stoytcho Mionoff"', 'male', '28', '0', '0', '349207', '7.8958', '', 'S\n']
    0 106
    1 0
    2 3
    3 " Mr. Stoytcho Mionoff"
    4 male
    5 28
    6 0
    7 0
    8 349207
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['107', '1', '3', '" Miss. Anna Kristine Salkjelsvik"', 'female', '21', '0', '0', '343120', '7.65', '', 'S\n']
    0 107
    1 1
    2 3
    3 " Miss. Anna Kristine Salkjelsvik"
    4 female
    5 21
    6 0
    7 0
    8 343120
    9 7.65
    10 
    11 S
    
    ----------------------------
    ['108', '1', '3', '" Mr. Albert Johan Moss"', 'male', '', '0', '0', '312991', '7.775', '', 'S\n']
    0 108
    1 1
    2 3
    3 " Mr. Albert Johan Moss"
    4 male
    5 
    6 0
    7 0
    8 312991
    9 7.775
    10 
    11 S
    
    ----------------------------
    ['109', '0', '3', '" Mr. Tido Rekic"', 'male', '38', '0', '0', '349249', '7.8958', '', 'S\n']
    0 109
    1 0
    2 3
    3 " Mr. Tido Rekic"
    4 male
    5 38
    6 0
    7 0
    8 349249
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['110', '1', '3', '" Miss. Bertha Moran"', 'female', '', '1', '0', '371110', '24.15', '', 'Q\n']
    0 110
    1 1
    2 3
    3 " Miss. Bertha Moran"
    4 female
    5 
    6 1
    7 0
    8 371110
    9 24.15
    10 
    11 Q
    
    ----------------------------
    ['111', '0', '1', '" Mr. Walter Chamberlain Porter"', 'male', '47', '0', '0', '110465', '52', 'C110', 'S\n']
    0 111
    1 0
    2 1
    3 " Mr. Walter Chamberlain Porter"
    4 male
    5 47
    6 0
    7 0
    8 110465
    9 52
    10 C110
    11 S
    
    ----------------------------
    ['112', '0', '3', '" Miss. Hileni Zabour"', 'female', '14.5', '1', '0', '2665', '14.4542', '', 'C\n']
    0 112
    1 0
    2 3
    3 " Miss. Hileni Zabour"
    4 female
    5 14.5
    6 1
    7 0
    8 2665
    9 14.4542
    10 
    11 C
    
    ----------------------------
    ['113', '0', '3', '" Mr. David John Barton"', 'male', '22', '0', '0', '324669', '8.05', '', 'S\n']
    0 113
    1 0
    2 3
    3 " Mr. David John Barton"
    4 male
    5 22
    6 0
    7 0
    8 324669
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['114', '0', '3', '" Miss. Katriina Jussila"', 'female', '20', '1', '0', '4136', '9.825', '', 'S\n']
    0 114
    1 0
    2 3
    3 " Miss. Katriina Jussila"
    4 female
    5 20
    6 1
    7 0
    8 4136
    9 9.825
    10 
    11 S
    
    ----------------------------
    ['115', '0', '3', '" Miss. Malake Attalah"', 'female', '17', '0', '0', '2627', '14.4583', '', 'C\n']
    0 115
    1 0
    2 3
    3 " Miss. Malake Attalah"
    4 female
    5 17
    6 0
    7 0
    8 2627
    9 14.4583
    10 
    11 C
    
    ----------------------------
    ['116', '0', '3', '" Mr. Edvard Pekoniemi"', 'male', '21', '0', '0', 'STON/O 2. 3101294', '7.925', '', 'S\n']
    0 116
    1 0
    2 3
    3 " Mr. Edvard Pekoniemi"
    4 male
    5 21
    6 0
    7 0
    8 STON/O 2. 3101294
    9 7.925
    10 
    11 S
    
    ----------------------------
    ['117', '0', '3', '" Mr. Patrick Connors"', 'male', '70.5', '0', '0', '370369', '7.75', '', 'Q\n']
    0 117
    1 0
    2 3
    3 " Mr. Patrick Connors"
    4 male
    5 70.5
    6 0
    7 0
    8 370369
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['118', '0', '2', '" Mr. William John Robert Turpin"', 'male', '29', '1', '0', '11668', '21', '', 'S\n']
    0 118
    1 0
    2 2
    3 " Mr. William John Robert Turpin"
    4 male
    5 29
    6 1
    7 0
    8 11668
    9 21
    10 
    11 S
    
    ----------------------------
    ['119', '0', '1', '" Mr. Quigg Edmond Baxter"', 'male', '24', '0', '1', 'PC 17558', '247.5208', 'B58 B60', 'C\n']
    0 119
    1 0
    2 1
    3 " Mr. Quigg Edmond Baxter"
    4 male
    5 24
    6 0
    7 1
    8 PC 17558
    9 247.5208
    10 B58 B60
    11 C
    
    ----------------------------
    ['120', '0', '3', '" Miss. Ellis Anna Maria Andersson"', 'female', '2', '4', '2', '347082', '31.275', '', 'S\n']
    0 120
    1 0
    2 3
    3 " Miss. Ellis Anna Maria Andersson"
    4 female
    5 2
    6 4
    7 2
    8 347082
    9 31.275
    10 
    11 S
    
    ----------------------------
    ['121', '0', '2', '" Mr. Stanley George Hickman"', 'male', '21', '2', '0', 'S.O.C. 14879', '73.5', '', 'S\n']
    0 121
    1 0
    2 2
    3 " Mr. Stanley George Hickman"
    4 male
    5 21
    6 2
    7 0
    8 S.O.C. 14879
    9 73.5
    10 
    11 S
    
    ----------------------------
    ['122', '0', '3', '" Mr. Leonard Charles Moore"', 'male', '', '0', '0', 'A4. 54510', '8.05', '', 'S\n']
    0 122
    1 0
    2 3
    3 " Mr. Leonard Charles Moore"
    4 male
    5 
    6 0
    7 0
    8 A4. 54510
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['123', '0', '2', '" Mr. Nicholas Nasser"', 'male', '32.5', '1', '0', '237736', '30.0708', '', 'C\n']
    0 123
    1 0
    2 2
    3 " Mr. Nicholas Nasser"
    4 male
    5 32.5
    6 1
    7 0
    8 237736
    9 30.0708
    10 
    11 C
    
    ----------------------------
    ['124', '1', '2', '" Miss. Susan Webber"', 'female', '32.5', '0', '0', '27267', '13', 'E101', 'S\n']
    0 124
    1 1
    2 2
    3 " Miss. Susan Webber"
    4 female
    5 32.5
    6 0
    7 0
    8 27267
    9 13
    10 E101
    11 S
    
    ----------------------------
    ['125', '0', '1', '" Mr. Percival Wayland White"', 'male', '54', '0', '1', '35281', '77.2875', 'D26', 'S\n']
    0 125
    1 0
    2 1
    3 " Mr. Percival Wayland White"
    4 male
    5 54
    6 0
    7 1
    8 35281
    9 77.2875
    10 D26
    11 S
    
    ----------------------------
    ['126', '1', '3', '" Master. Elias Nicola-Yarred"', 'male', '12', '1', '0', '2651', '11.2417', '', 'C\n']
    0 126
    1 1
    2 3
    3 " Master. Elias Nicola-Yarred"
    4 male
    5 12
    6 1
    7 0
    8 2651
    9 11.2417
    10 
    11 C
    
    ----------------------------
    ['127', '0', '3', '" Mr. Martin McMahon"', 'male', '', '0', '0', '370372', '7.75', '', 'Q\n']
    0 127
    1 0
    2 3
    3 " Mr. Martin McMahon"
    4 male
    5 
    6 0
    7 0
    8 370372
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['128', '1', '3', '" Mr. Fridtjof Arne Madsen"', 'male', '24', '0', '0', 'C 17369', '7.1417', '', 'S\n']
    0 128
    1 1
    2 3
    3 " Mr. Fridtjof Arne Madsen"
    4 male
    5 24
    6 0
    7 0
    8 C 17369
    9 7.1417
    10 
    11 S
    
    ----------------------------
    ['129', '1', '3', '" Miss. Anna Peter"', 'female', '', '1', '1', '2668', '22.3583', 'F E69', 'C\n']
    0 129
    1 1
    2 3
    3 " Miss. Anna Peter"
    4 female
    5 
    6 1
    7 1
    8 2668
    9 22.3583
    10 F E69
    11 C
    
    ----------------------------
    ['130', '0', '3', '" Mr. Johan Ekstrom"', 'male', '45', '0', '0', '347061', '6.975', '', 'S\n']
    0 130
    1 0
    2 3
    3 " Mr. Johan Ekstrom"
    4 male
    5 45
    6 0
    7 0
    8 347061
    9 6.975
    10 
    11 S
    
    ----------------------------
    ['131', '0', '3', '" Mr. Jozef Drazenoic"', 'male', '33', '0', '0', '349241', '7.8958', '', 'C\n']
    0 131
    1 0
    2 3
    3 " Mr. Jozef Drazenoic"
    4 male
    5 33
    6 0
    7 0
    8 349241
    9 7.8958
    10 
    11 C
    
    ----------------------------
    ['132', '0', '3', '" Mr. Domingos Fernandeo Coelho"', 'male', '20', '0', '0', 'SOTON/O.Q. 3101307', '7.05', '', 'S\n']
    0 132
    1 0
    2 3
    3 " Mr. Domingos Fernandeo Coelho"
    4 male
    5 20
    6 0
    7 0
    8 SOTON/O.Q. 3101307
    9 7.05
    10 
    11 S
    
    ----------------------------
    ['133', '0', '3', '" Mrs. Alexander A (Grace Charity Laury) Robins"', 'female', '47', '1', '0', 'A/5. 3337', '14.5', '', 'S\n']
    0 133
    1 0
    2 3
    3 " Mrs. Alexander A (Grace Charity Laury) Robins"
    4 female
    5 47
    6 1
    7 0
    8 A/5. 3337
    9 14.5
    10 
    11 S
    
    ----------------------------
    ['134', '1', '2', '" Mrs. Leopold (Mathilde Francoise Pede) Weisz"', 'female', '29', '1', '0', '228414', '26', '', 'S\n']
    0 134
    1 1
    2 2
    3 " Mrs. Leopold (Mathilde Francoise Pede) Weisz"
    4 female
    5 29
    6 1
    7 0
    8 228414
    9 26
    10 
    11 S
    
    ----------------------------
    ['135', '0', '2', '" Mr. Samuel James Hayden Sobey"', 'male', '25', '0', '0', 'C.A. 29178', '13', '', 'S\n']
    0 135
    1 0
    2 2
    3 " Mr. Samuel James Hayden Sobey"
    4 male
    5 25
    6 0
    7 0
    8 C.A. 29178
    9 13
    10 
    11 S
    
    ----------------------------
    ['136', '0', '2', '" Mr. Emile Richard"', 'male', '23', '0', '0', 'SC/PARIS 2133', '15.0458', '', 'C\n']
    0 136
    1 0
    2 2
    3 " Mr. Emile Richard"
    4 male
    5 23
    6 0
    7 0
    8 SC/PARIS 2133
    9 15.0458
    10 
    11 C
    
    ----------------------------
    ['137', '1', '1', '" Miss. Helen Monypeny Newsom"', 'female', '19', '0', '2', '11752', '26.2833', 'D47', 'S\n']
    0 137
    1 1
    2 1
    3 " Miss. Helen Monypeny Newsom"
    4 female
    5 19
    6 0
    7 2
    8 11752
    9 26.2833
    10 D47
    11 S
    
    ----------------------------
    ['138', '0', '1', '" Mr. Jacques Heath Futrelle"', 'male', '37', '1', '0', '113803', '53.1', 'C123', 'S\n']
    0 138
    1 0
    2 1
    3 " Mr. Jacques Heath Futrelle"
    4 male
    5 37
    6 1
    7 0
    8 113803
    9 53.1
    10 C123
    11 S
    
    ----------------------------
    ['139', '0', '3', '" Mr. Olaf Elon Osen"', 'male', '16', '0', '0', '7534', '9.2167', '', 'S\n']
    0 139
    1 0
    2 3
    3 " Mr. Olaf Elon Osen"
    4 male
    5 16
    6 0
    7 0
    8 7534
    9 9.2167
    10 
    11 S
    
    ----------------------------
    ['140', '0', '1', '" Mr. Victor Giglio"', 'male', '24', '0', '0', 'PC 17593', '79.2', 'B86', 'C\n']
    0 140
    1 0
    2 1
    3 " Mr. Victor Giglio"
    4 male
    5 24
    6 0
    7 0
    8 PC 17593
    9 79.2
    10 B86
    11 C
    
    ----------------------------
    ['141', '0', '3', '" Mrs. Joseph (Sultana) Boulos"', 'female', '', '0', '2', '2678', '15.2458', '', 'C\n']
    0 141
    1 0
    2 3
    3 " Mrs. Joseph (Sultana) Boulos"
    4 female
    5 
    6 0
    7 2
    8 2678
    9 15.2458
    10 
    11 C
    
    ----------------------------
    ['142', '1', '3', '" Miss. Anna Sofia Nysten"', 'female', '22', '0', '0', '347081', '7.75', '', 'S\n']
    0 142
    1 1
    2 3
    3 " Miss. Anna Sofia Nysten"
    4 female
    5 22
    6 0
    7 0
    8 347081
    9 7.75
    10 
    11 S
    
    ----------------------------
    ['143', '1', '3', '" Mrs. Pekka Pietari (Elin Matilda Dolck) Hakkarainen"', 'female', '24', '1', '0', 'STON/O2. 3101279', '15.85', '', 'S\n']
    0 143
    1 1
    2 3
    3 " Mrs. Pekka Pietari (Elin Matilda Dolck) Hakkarainen"
    4 female
    5 24
    6 1
    7 0
    8 STON/O2. 3101279
    9 15.85
    10 
    11 S
    
    ----------------------------
    ['144', '0', '3', '" Mr. Jeremiah Burke"', 'male', '19', '0', '0', '365222', '6.75', '', 'Q\n']
    0 144
    1 0
    2 3
    3 " Mr. Jeremiah Burke"
    4 male
    5 19
    6 0
    7 0
    8 365222
    9 6.75
    10 
    11 Q
    
    ----------------------------
    ['145', '0', '2', '" Mr. Edgardo Samuel Andrew"', 'male', '18', '0', '0', '231945', '11.5', '', 'S\n']
    0 145
    1 0
    2 2
    3 " Mr. Edgardo Samuel Andrew"
    4 male
    5 18
    6 0
    7 0
    8 231945
    9 11.5
    10 
    11 S
    
    ----------------------------
    ['146', '0', '2', '" Mr. Joseph Charles Nicholls"', 'male', '19', '1', '1', 'C.A. 33112', '36.75', '', 'S\n']
    0 146
    1 0
    2 2
    3 " Mr. Joseph Charles Nicholls"
    4 male
    5 19
    6 1
    7 1
    8 C.A. 33112
    9 36.75
    10 
    11 S
    
    ----------------------------
    ['147', '1', '3', '" Mr. August Edvard (""Wennerstrom"") Andersson"', 'male', '27', '0', '0', '350043', '7.7958', '', 'S\n']
    0 147
    1 1
    2 3
    3 " Mr. August Edvard (""Wennerstrom"") Andersson"
    4 male
    5 27
    6 0
    7 0
    8 350043
    9 7.7958
    10 
    11 S
    
    ----------------------------
    ['148', '0', '3', '" Miss. Robina Maggie ""Ruby"" Ford"', 'female', '9', '2', '2', 'W./C. 6608', '34.375', '', 'S\n']
    0 148
    1 0
    2 3
    3 " Miss. Robina Maggie ""Ruby"" Ford"
    4 female
    5 9
    6 2
    7 2
    8 W./C. 6608
    9 34.375
    10 
    11 S
    
    ----------------------------
    ['149', '0', '2', '" Mr. Michel (""Louis M Hoffman"") Navratil"', 'male', '36.5', '0', '2', '230080', '26', 'F2', 'S\n']
    0 149
    1 0
    2 2
    3 " Mr. Michel (""Louis M Hoffman"") Navratil"
    4 male
    5 36.5
    6 0
    7 2
    8 230080
    9 26
    10 F2
    11 S
    
    ----------------------------
    ['150', '0', '2', '" Rev. Thomas Roussel Davids Byles"', 'male', '42', '0', '0', '244310', '13', '', 'S\n']
    0 150
    1 0
    2 2
    3 " Rev. Thomas Roussel Davids Byles"
    4 male
    5 42
    6 0
    7 0
    8 244310
    9 13
    10 
    11 S
    
    ----------------------------
    ['151', '0', '2', '" Rev. Robert James Bateman"', 'male', '51', '0', '0', 'S.O.P. 1166', '12.525', '', 'S\n']
    0 151
    1 0
    2 2
    3 " Rev. Robert James Bateman"
    4 male
    5 51
    6 0
    7 0
    8 S.O.P. 1166
    9 12.525
    10 
    11 S
    
    ----------------------------
    ['152', '1', '1', '" Mrs. Thomas (Edith Wearne) Pears"', 'female', '22', '1', '0', '113776', '66.6', 'C2', 'S\n']
    0 152
    1 1
    2 1
    3 " Mrs. Thomas (Edith Wearne) Pears"
    4 female
    5 22
    6 1
    7 0
    8 113776
    9 66.6
    10 C2
    11 S
    
    ----------------------------
    ['153', '0', '3', '" Mr. Alfonzo Meo"', 'male', '55.5', '0', '0', 'A.5. 11206', '8.05', '', 'S\n']
    0 153
    1 0
    2 3
    3 " Mr. Alfonzo Meo"
    4 male
    5 55.5
    6 0
    7 0
    8 A.5. 11206
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['154', '0', '3', '" Mr. Austin Blyler van Billiard"', 'male', '40.5', '0', '2', 'A/5. 851', '14.5', '', 'S\n']
    0 154
    1 0
    2 3
    3 " Mr. Austin Blyler van Billiard"
    4 male
    5 40.5
    6 0
    7 2
    8 A/5. 851
    9 14.5
    10 
    11 S
    
    ----------------------------
    ['155', '0', '3', '" Mr. Ole Martin Olsen"', 'male', '', '0', '0', 'Fa 265302', '7.3125', '', 'S\n']
    0 155
    1 0
    2 3
    3 " Mr. Ole Martin Olsen"
    4 male
    5 
    6 0
    7 0
    8 Fa 265302
    9 7.3125
    10 
    11 S
    
    ----------------------------
    ['156', '0', '1', '" Mr. Charles Duane Williams"', 'male', '51', '0', '1', 'PC 17597', '61.3792', '', 'C\n']
    0 156
    1 0
    2 1
    3 " Mr. Charles Duane Williams"
    4 male
    5 51
    6 0
    7 1
    8 PC 17597
    9 61.3792
    10 
    11 C
    
    ----------------------------
    ['157', '1', '3', '" Miss. Katherine ""Katie"" Gilnagh"', 'female', '16', '0', '0', '35851', '7.7333', '', 'Q\n']
    0 157
    1 1
    2 3
    3 " Miss. Katherine ""Katie"" Gilnagh"
    4 female
    5 16
    6 0
    7 0
    8 35851
    9 7.7333
    10 
    11 Q
    
    ----------------------------
    ['158', '0', '3', '" Mr. Harry Corn"', 'male', '30', '0', '0', 'SOTON/OQ 392090', '8.05', '', 'S\n']
    0 158
    1 0
    2 3
    3 " Mr. Harry Corn"
    4 male
    5 30
    6 0
    7 0
    8 SOTON/OQ 392090
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['159', '0', '3', '" Mr. Mile Smiljanic"', 'male', '', '0', '0', '315037', '8.6625', '', 'S\n']
    0 159
    1 0
    2 3
    3 " Mr. Mile Smiljanic"
    4 male
    5 
    6 0
    7 0
    8 315037
    9 8.6625
    10 
    11 S
    
    ----------------------------
    ['160', '0', '3', '" Master. Thomas Henry Sage"', 'male', '', '8', '2', 'CA. 2343', '69.55', '', 'S\n']
    0 160
    1 0
    2 3
    3 " Master. Thomas Henry Sage"
    4 male
    5 
    6 8
    7 2
    8 CA. 2343
    9 69.55
    10 
    11 S
    
    ----------------------------
    ['161', '0', '3', '" Mr. John Hatfield Cribb"', 'male', '44', '0', '1', '371362', '16.1', '', 'S\n']
    0 161
    1 0
    2 3
    3 " Mr. John Hatfield Cribb"
    4 male
    5 44
    6 0
    7 1
    8 371362
    9 16.1
    10 
    11 S
    
    ----------------------------
    ['162', '1', '2', '" Mrs. James (Elizabeth ""Bessie"" Inglis Milne) Watt"', 'female', '40', '0', '0', 'C.A. 33595', '15.75', '', 'S\n']
    0 162
    1 1
    2 2
    3 " Mrs. James (Elizabeth ""Bessie"" Inglis Milne) Watt"
    4 female
    5 40
    6 0
    7 0
    8 C.A. 33595
    9 15.75
    10 
    11 S
    
    ----------------------------
    ['163', '0', '3', '" Mr. John Viktor Bengtsson"', 'male', '26', '0', '0', '347068', '7.775', '', 'S\n']
    0 163
    1 0
    2 3
    3 " Mr. John Viktor Bengtsson"
    4 male
    5 26
    6 0
    7 0
    8 347068
    9 7.775
    10 
    11 S
    
    ----------------------------
    ['164', '0', '3', '" Mr. Jovo Calic"', 'male', '17', '0', '0', '315093', '8.6625', '', 'S\n']
    0 164
    1 0
    2 3
    3 " Mr. Jovo Calic"
    4 male
    5 17
    6 0
    7 0
    8 315093
    9 8.6625
    10 
    11 S
    
    ----------------------------
    ['165', '0', '3', '" Master. Eino Viljami Panula"', 'male', '1', '4', '1', '3101295', '39.6875', '', 'S\n']
    0 165
    1 0
    2 3
    3 " Master. Eino Viljami Panula"
    4 male
    5 1
    6 4
    7 1
    8 3101295
    9 39.6875
    10 
    11 S
    
    ----------------------------
    ['166', '1', '3', '" Master. Frank John William ""Frankie"" Goldsmith"', 'male', '9', '0', '2', '363291', '20.525', '', 'S\n']
    0 166
    1 1
    2 3
    3 " Master. Frank John William ""Frankie"" Goldsmith"
    4 male
    5 9
    6 0
    7 2
    8 363291
    9 20.525
    10 
    11 S
    
    ----------------------------
    ['167', '1', '1', '" Mrs. (Edith Martha Bowerman) Chibnall"', 'female', '', '0', '1', '113505', '55', 'E33', 'S\n']
    0 167
    1 1
    2 1
    3 " Mrs. (Edith Martha Bowerman) Chibnall"
    4 female
    5 
    6 0
    7 1
    8 113505
    9 55
    10 E33
    11 S
    
    ----------------------------
    ['168', '0', '3', '" Mrs. William (Anna Bernhardina Karlsson) Skoog"', 'female', '45', '1', '4', '347088', '27.9', '', 'S\n']
    0 168
    1 0
    2 3
    3 " Mrs. William (Anna Bernhardina Karlsson) Skoog"
    4 female
    5 45
    6 1
    7 4
    8 347088
    9 27.9
    10 
    11 S
    
    ----------------------------
    ['169', '0', '1', '" Mr. John D Baumann"', 'male', '', '0', '0', 'PC 17318', '25.925', '', 'S\n']
    0 169
    1 0
    2 1
    3 " Mr. John D Baumann"
    4 male
    5 
    6 0
    7 0
    8 PC 17318
    9 25.925
    10 
    11 S
    
    ----------------------------
    ['170', '0', '3', '" Mr. Lee Ling"', 'male', '28', '0', '0', '1601', '56.4958', '', 'S\n']
    0 170
    1 0
    2 3
    3 " Mr. Lee Ling"
    4 male
    5 28
    6 0
    7 0
    8 1601
    9 56.4958
    10 
    11 S
    
    ----------------------------
    ['171', '0', '1', '" Mr. Wyckoff Van der hoef"', 'male', '61', '0', '0', '111240', '33.5', 'B19', 'S\n']
    0 171
    1 0
    2 1
    3 " Mr. Wyckoff Van der hoef"
    4 male
    5 61
    6 0
    7 0
    8 111240
    9 33.5
    10 B19
    11 S
    
    ----------------------------
    ['172', '0', '3', '" Master. Arthur Rice"', 'male', '4', '4', '1', '382652', '29.125', '', 'Q\n']
    0 172
    1 0
    2 3
    3 " Master. Arthur Rice"
    4 male
    5 4
    6 4
    7 1
    8 382652
    9 29.125
    10 
    11 Q
    
    ----------------------------
    ['173', '1', '3', '" Miss. Eleanor Ileen Johnson"', 'female', '1', '1', '1', '347742', '11.1333', '', 'S\n']
    0 173
    1 1
    2 3
    3 " Miss. Eleanor Ileen Johnson"
    4 female
    5 1
    6 1
    7 1
    8 347742
    9 11.1333
    10 
    11 S
    
    ----------------------------
    ['174', '0', '3', '" Mr. Antti Wilhelm Sivola"', 'male', '21', '0', '0', 'STON/O 2. 3101280', '7.925', '', 'S\n']
    0 174
    1 0
    2 3
    3 " Mr. Antti Wilhelm Sivola"
    4 male
    5 21
    6 0
    7 0
    8 STON/O 2. 3101280
    9 7.925
    10 
    11 S
    
    ----------------------------
    ['175', '0', '1', '" Mr. James Clinch Smith"', 'male', '56', '0', '0', '17764', '30.6958', 'A7', 'C\n']
    0 175
    1 0
    2 1
    3 " Mr. James Clinch Smith"
    4 male
    5 56
    6 0
    7 0
    8 17764
    9 30.6958
    10 A7
    11 C
    
    ----------------------------
    ['176', '0', '3', '" Mr. Klas Albin Klasen"', 'male', '18', '1', '1', '350404', '7.8542', '', 'S\n']
    0 176
    1 0
    2 3
    3 " Mr. Klas Albin Klasen"
    4 male
    5 18
    6 1
    7 1
    8 350404
    9 7.8542
    10 
    11 S
    
    ----------------------------
    ['177', '0', '3', '" Master. Henry Forbes Lefebre"', 'male', '', '3', '1', '4133', '25.4667', '', 'S\n']
    0 177
    1 0
    2 3
    3 " Master. Henry Forbes Lefebre"
    4 male
    5 
    6 3
    7 1
    8 4133
    9 25.4667
    10 
    11 S
    
    ----------------------------
    ['178', '0', '1', '" Miss. Ann Elizabeth Isham"', 'female', '50', '0', '0', 'PC 17595', '28.7125', 'C49', 'C\n']
    0 178
    1 0
    2 1
    3 " Miss. Ann Elizabeth Isham"
    4 female
    5 50
    6 0
    7 0
    8 PC 17595
    9 28.7125
    10 C49
    11 C
    
    ----------------------------
    ['179', '0', '2', '" Mr. Reginald Hale"', 'male', '30', '0', '0', '250653', '13', '', 'S\n']
    0 179
    1 0
    2 2
    3 " Mr. Reginald Hale"
    4 male
    5 30
    6 0
    7 0
    8 250653
    9 13
    10 
    11 S
    
    ----------------------------
    ['180', '0', '3', '" Mr. Lionel Leonard"', 'male', '36', '0', '0', 'LINE', '0', '', 'S\n']
    0 180
    1 0
    2 3
    3 " Mr. Lionel Leonard"
    4 male
    5 36
    6 0
    7 0
    8 LINE
    9 0
    10 
    11 S
    
    ----------------------------
    ['181', '0', '3', '" Miss. Constance Gladys Sage"', 'female', '', '8', '2', 'CA. 2343', '69.55', '', 'S\n']
    0 181
    1 0
    2 3
    3 " Miss. Constance Gladys Sage"
    4 female
    5 
    6 8
    7 2
    8 CA. 2343
    9 69.55
    10 
    11 S
    
    ----------------------------
    ['182', '0', '2', '" Mr. Rene Pernot"', 'male', '', '0', '0', 'SC/PARIS 2131', '15.05', '', 'C\n']
    0 182
    1 0
    2 2
    3 " Mr. Rene Pernot"
    4 male
    5 
    6 0
    7 0
    8 SC/PARIS 2131
    9 15.05
    10 
    11 C
    
    ----------------------------
    ['183', '0', '3', '" Master. Clarence Gustaf Hugo Asplund"', 'male', '9', '4', '2', '347077', '31.3875', '', 'S\n']
    0 183
    1 0
    2 3
    3 " Master. Clarence Gustaf Hugo Asplund"
    4 male
    5 9
    6 4
    7 2
    8 347077
    9 31.3875
    10 
    11 S
    
    ----------------------------
    ['184', '1', '2', '" Master. Richard F Becker"', 'male', '1', '2', '1', '230136', '39', 'F4', 'S\n']
    0 184
    1 1
    2 2
    3 " Master. Richard F Becker"
    4 male
    5 1
    6 2
    7 1
    8 230136
    9 39
    10 F4
    11 S
    
    ----------------------------
    ['185', '1', '3', '" Miss. Luise Gretchen Kink-Heilmann"', 'female', '4', '0', '2', '315153', '22.025', '', 'S\n']
    0 185
    1 1
    2 3
    3 " Miss. Luise Gretchen Kink-Heilmann"
    4 female
    5 4
    6 0
    7 2
    8 315153
    9 22.025
    10 
    11 S
    
    ----------------------------
    ['186', '0', '1', '" Mr. Hugh Roscoe Rood"', 'male', '', '0', '0', '113767', '50', 'A32', 'S\n']
    0 186
    1 0
    2 1
    3 " Mr. Hugh Roscoe Rood"
    4 male
    5 
    6 0
    7 0
    8 113767
    9 50
    10 A32
    11 S
    
    ----------------------------
    ['187', '1', '3', '" Mrs. Thomas (Johanna ""Hannah"" Godfrey) O\'Brien"', 'female', '', '1', '0', '370365', '15.5', '', 'Q\n']
    0 187
    1 1
    2 3
    3 " Mrs. Thomas (Johanna ""Hannah"" Godfrey) O'Brien"
    4 female
    5 
    6 1
    7 0
    8 370365
    9 15.5
    10 
    11 Q
    
    ----------------------------
    ['188', '1', '1', '" Mr. Charles Hallace (""Mr C Rolmane"") Romaine"', 'male', '45', '0', '0', '111428', '26.55', '', 'S\n']
    0 188
    1 1
    2 1
    3 " Mr. Charles Hallace (""Mr C Rolmane"") Romaine"
    4 male
    5 45
    6 0
    7 0
    8 111428
    9 26.55
    10 
    11 S
    
    ----------------------------
    ['189', '0', '3', '" Mr. John Bourke"', 'male', '40', '1', '1', '364849', '15.5', '', 'Q\n']
    0 189
    1 0
    2 3
    3 " Mr. John Bourke"
    4 male
    5 40
    6 1
    7 1
    8 364849
    9 15.5
    10 
    11 Q
    
    ----------------------------
    ['190', '0', '3', '" Mr. Stjepan Turcin"', 'male', '36', '0', '0', '349247', '7.8958', '', 'S\n']
    0 190
    1 0
    2 3
    3 " Mr. Stjepan Turcin"
    4 male
    5 36
    6 0
    7 0
    8 349247
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['191', '1', '2', '" Mrs. (Rosa) Pinsky"', 'female', '32', '0', '0', '234604', '13', '', 'S\n']
    0 191
    1 1
    2 2
    3 " Mrs. (Rosa) Pinsky"
    4 female
    5 32
    6 0
    7 0
    8 234604
    9 13
    10 
    11 S
    
    ----------------------------
    ['192', '0', '2', '" Mr. William Carbines"', 'male', '19', '0', '0', '28424', '13', '', 'S\n']
    0 192
    1 0
    2 2
    3 " Mr. William Carbines"
    4 male
    5 19
    6 0
    7 0
    8 28424
    9 13
    10 
    11 S
    
    ----------------------------
    ['193', '1', '3', '" Miss. Carla Christine Nielsine Andersen-Jensen"', 'female', '19', '1', '0', '350046', '7.8542', '', 'S\n']
    0 193
    1 1
    2 3
    3 " Miss. Carla Christine Nielsine Andersen-Jensen"
    4 female
    5 19
    6 1
    7 0
    8 350046
    9 7.8542
    10 
    11 S
    
    ----------------------------
    ['194', '1', '2', '" Master. Michel M Navratil"', 'male', '3', '1', '1', '230080', '26', 'F2', 'S\n']
    0 194
    1 1
    2 2
    3 " Master. Michel M Navratil"
    4 male
    5 3
    6 1
    7 1
    8 230080
    9 26
    10 F2
    11 S
    
    ----------------------------
    ['195', '1', '1', '" Mrs. James Joseph (Margaret Tobin) Brown"', 'female', '44', '0', '0', 'PC 17610', '27.7208', 'B4', 'C\n']
    0 195
    1 1
    2 1
    3 " Mrs. James Joseph (Margaret Tobin) Brown"
    4 female
    5 44
    6 0
    7 0
    8 PC 17610
    9 27.7208
    10 B4
    11 C
    
    ----------------------------
    ['196', '1', '1', '" Miss. Elise Lurette"', 'female', '58', '0', '0', 'PC 17569', '146.5208', 'B80', 'C\n']
    0 196
    1 1
    2 1
    3 " Miss. Elise Lurette"
    4 female
    5 58
    6 0
    7 0
    8 PC 17569
    9 146.5208
    10 B80
    11 C
    
    ----------------------------
    ['197', '0', '3', '" Mr. Robert Mernagh"', 'male', '', '0', '0', '368703', '7.75', '', 'Q\n']
    0 197
    1 0
    2 3
    3 " Mr. Robert Mernagh"
    4 male
    5 
    6 0
    7 0
    8 368703
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['198', '0', '3', '" Mr. Karl Siegwart Andreas Olsen"', 'male', '42', '0', '1', '4579', '8.4042', '', 'S\n']
    0 198
    1 0
    2 3
    3 " Mr. Karl Siegwart Andreas Olsen"
    4 male
    5 42
    6 0
    7 1
    8 4579
    9 8.4042
    10 
    11 S
    
    ----------------------------
    ['199', '1', '3', '" Miss. Margaret ""Maggie"" Madigan"', 'female', '', '0', '0', '370370', '7.75', '', 'Q\n']
    0 199
    1 1
    2 3
    3 " Miss. Margaret ""Maggie"" Madigan"
    4 female
    5 
    6 0
    7 0
    8 370370
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['200', '0', '2', '" Miss. Henriette (""Mrs Harbeck"") Yrois"', 'female', '24', '0', '0', '248747', '13', '', 'S\n']
    0 200
    1 0
    2 2
    3 " Miss. Henriette (""Mrs Harbeck"") Yrois"
    4 female
    5 24
    6 0
    7 0
    8 248747
    9 13
    10 
    11 S
    
    ----------------------------
    ['201', '0', '3', '" Mr. Nestor Cyriel Vande Walle"', 'male', '28', '0', '0', '345770', '9.5', '', 'S\n']
    0 201
    1 0
    2 3
    3 " Mr. Nestor Cyriel Vande Walle"
    4 male
    5 28
    6 0
    7 0
    8 345770
    9 9.5
    10 
    11 S
    
    ----------------------------
    ['202', '0', '3', '" Mr. Frederick Sage"', 'male', '', '8', '2', 'CA. 2343', '69.55', '', 'S\n']
    0 202
    1 0
    2 3
    3 " Mr. Frederick Sage"
    4 male
    5 
    6 8
    7 2
    8 CA. 2343
    9 69.55
    10 
    11 S
    
    ----------------------------
    ['203', '0', '3', '" Mr. Jakob Alfred Johanson"', 'male', '34', '0', '0', '3101264', '6.4958', '', 'S\n']
    0 203
    1 0
    2 3
    3 " Mr. Jakob Alfred Johanson"
    4 male
    5 34
    6 0
    7 0
    8 3101264
    9 6.4958
    10 
    11 S
    
    ----------------------------
    ['204', '0', '3', '" Mr. Gerious Youseff"', 'male', '45.5', '0', '0', '2628', '7.225', '', 'C\n']
    0 204
    1 0
    2 3
    3 " Mr. Gerious Youseff"
    4 male
    5 45.5
    6 0
    7 0
    8 2628
    9 7.225
    10 
    11 C
    
    ----------------------------
    ['205', '1', '3', '" Mr. Gurshon ""Gus"" Cohen"', 'male', '18', '0', '0', 'A/5 3540', '8.05', '', 'S\n']
    0 205
    1 1
    2 3
    3 " Mr. Gurshon ""Gus"" Cohen"
    4 male
    5 18
    6 0
    7 0
    8 A/5 3540
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['206', '0', '3', '" Miss. Telma Matilda Strom"', 'female', '2', '0', '1', '347054', '10.4625', 'G6', 'S\n']
    0 206
    1 0
    2 3
    3 " Miss. Telma Matilda Strom"
    4 female
    5 2
    6 0
    7 1
    8 347054
    9 10.4625
    10 G6
    11 S
    
    ----------------------------
    ['207', '0', '3', '" Mr. Karl Alfred Backstrom"', 'male', '32', '1', '0', '3101278', '15.85', '', 'S\n']
    0 207
    1 0
    2 3
    3 " Mr. Karl Alfred Backstrom"
    4 male
    5 32
    6 1
    7 0
    8 3101278
    9 15.85
    10 
    11 S
    
    ----------------------------
    ['208', '1', '3', '" Mr. Nassef Cassem Albimona"', 'male', '26', '0', '0', '2699', '18.7875', '', 'C\n']
    0 208
    1 1
    2 3
    3 " Mr. Nassef Cassem Albimona"
    4 male
    5 26
    6 0
    7 0
    8 2699
    9 18.7875
    10 
    11 C
    
    ----------------------------
    ['209', '1', '3', '" Miss. Helen ""Ellen"" Carr"', 'female', '16', '0', '0', '367231', '7.75', '', 'Q\n']
    0 209
    1 1
    2 3
    3 " Miss. Helen ""Ellen"" Carr"
    4 female
    5 16
    6 0
    7 0
    8 367231
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['210', '1', '1', '" Mr. Henry Blank"', 'male', '40', '0', '0', '112277', '31', 'A31', 'C\n']
    0 210
    1 1
    2 1
    3 " Mr. Henry Blank"
    4 male
    5 40
    6 0
    7 0
    8 112277
    9 31
    10 A31
    11 C
    
    ----------------------------
    ['211', '0', '3', '" Mr. Ahmed Ali"', 'male', '24', '0', '0', 'SOTON/O.Q. 3101311', '7.05', '', 'S\n']
    0 211
    1 0
    2 3
    3 " Mr. Ahmed Ali"
    4 male
    5 24
    6 0
    7 0
    8 SOTON/O.Q. 3101311
    9 7.05
    10 
    11 S
    
    ----------------------------
    ['212', '1', '2', '" Miss. Clear Annie Cameron"', 'female', '35', '0', '0', 'F.C.C. 13528', '21', '', 'S\n']
    0 212
    1 1
    2 2
    3 " Miss. Clear Annie Cameron"
    4 female
    5 35
    6 0
    7 0
    8 F.C.C. 13528
    9 21
    10 
    11 S
    
    ----------------------------
    ['213', '0', '3', '" Mr. John Henry Perkin"', 'male', '22', '0', '0', 'A/5 21174', '7.25', '', 'S\n']
    0 213
    1 0
    2 3
    3 " Mr. John Henry Perkin"
    4 male
    5 22
    6 0
    7 0
    8 A/5 21174
    9 7.25
    10 
    11 S
    
    ----------------------------
    ['214', '0', '2', '" Mr. Hans Kristensen Givard"', 'male', '30', '0', '0', '250646', '13', '', 'S\n']
    0 214
    1 0
    2 2
    3 " Mr. Hans Kristensen Givard"
    4 male
    5 30
    6 0
    7 0
    8 250646
    9 13
    10 
    11 S
    
    ----------------------------
    ['215', '0', '3', '" Mr. Philip Kiernan"', 'male', '', '1', '0', '367229', '7.75', '', 'Q\n']
    0 215
    1 0
    2 3
    3 " Mr. Philip Kiernan"
    4 male
    5 
    6 1
    7 0
    8 367229
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['216', '1', '1', '" Miss. Madeleine Newell"', 'female', '31', '1', '0', '35273', '113.275', 'D36', 'C\n']
    0 216
    1 1
    2 1
    3 " Miss. Madeleine Newell"
    4 female
    5 31
    6 1
    7 0
    8 35273
    9 113.275
    10 D36
    11 C
    
    ----------------------------
    ['217', '1', '3', '" Miss. Eliina Honkanen"', 'female', '27', '0', '0', 'STON/O2. 3101283', '7.925', '', 'S\n']
    0 217
    1 1
    2 3
    3 " Miss. Eliina Honkanen"
    4 female
    5 27
    6 0
    7 0
    8 STON/O2. 3101283
    9 7.925
    10 
    11 S
    
    ----------------------------
    ['218', '0', '2', '" Mr. Sidney Samuel Jacobsohn"', 'male', '42', '1', '0', '243847', '27', '', 'S\n']
    0 218
    1 0
    2 2
    3 " Mr. Sidney Samuel Jacobsohn"
    4 male
    5 42
    6 1
    7 0
    8 243847
    9 27
    10 
    11 S
    
    ----------------------------
    ['219', '1', '1', '" Miss. Albina Bazzani"', 'female', '32', '0', '0', '11813', '76.2917', 'D15', 'C\n']
    0 219
    1 1
    2 1
    3 " Miss. Albina Bazzani"
    4 female
    5 32
    6 0
    7 0
    8 11813
    9 76.2917
    10 D15
    11 C
    
    ----------------------------
    ['220', '0', '2', '" Mr. Walter Harris"', 'male', '30', '0', '0', 'W/C 14208', '10.5', '', 'S\n']
    0 220
    1 0
    2 2
    3 " Mr. Walter Harris"
    4 male
    5 30
    6 0
    7 0
    8 W/C 14208
    9 10.5
    10 
    11 S
    
    ----------------------------
    ['221', '1', '3', '" Mr. Victor Francis Sunderland"', 'male', '16', '0', '0', 'SOTON/OQ 392089', '8.05', '', 'S\n']
    0 221
    1 1
    2 3
    3 " Mr. Victor Francis Sunderland"
    4 male
    5 16
    6 0
    7 0
    8 SOTON/OQ 392089
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['222', '0', '2', '" Mr. James H Bracken"', 'male', '27', '0', '0', '220367', '13', '', 'S\n']
    0 222
    1 0
    2 2
    3 " Mr. James H Bracken"
    4 male
    5 27
    6 0
    7 0
    8 220367
    9 13
    10 
    11 S
    
    ----------------------------
    ['223', '0', '3', '" Mr. George Henry Green"', 'male', '51', '0', '0', '21440', '8.05', '', 'S\n']
    0 223
    1 0
    2 3
    3 " Mr. George Henry Green"
    4 male
    5 51
    6 0
    7 0
    8 21440
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['224', '0', '3', '" Mr. Christo Nenkoff"', 'male', '', '0', '0', '349234', '7.8958', '', 'S\n']
    0 224
    1 0
    2 3
    3 " Mr. Christo Nenkoff"
    4 male
    5 
    6 0
    7 0
    8 349234
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['225', '1', '1', '" Mr. Frederick Maxfield Hoyt"', 'male', '38', '1', '0', '19943', '90', 'C93', 'S\n']
    0 225
    1 1
    2 1
    3 " Mr. Frederick Maxfield Hoyt"
    4 male
    5 38
    6 1
    7 0
    8 19943
    9 90
    10 C93
    11 S
    
    ----------------------------
    ['226', '0', '3', '" Mr. Karl Ivar Sven Berglund"', 'male', '22', '0', '0', 'PP 4348', '9.35', '', 'S\n']
    0 226
    1 0
    2 3
    3 " Mr. Karl Ivar Sven Berglund"
    4 male
    5 22
    6 0
    7 0
    8 PP 4348
    9 9.35
    10 
    11 S
    
    ----------------------------
    ['227', '1', '2', '" Mr. William John Mellors"', 'male', '19', '0', '0', 'SW/PP 751', '10.5', '', 'S\n']
    0 227
    1 1
    2 2
    3 " Mr. William John Mellors"
    4 male
    5 19
    6 0
    7 0
    8 SW/PP 751
    9 10.5
    10 
    11 S
    
    ----------------------------
    ['228', '0', '3', '" Mr. John Hall (""Henry"") Lovell"', 'male', '20.5', '0', '0', 'A/5 21173', '7.25', '', 'S\n']
    0 228
    1 0
    2 3
    3 " Mr. John Hall (""Henry"") Lovell"
    4 male
    5 20.5
    6 0
    7 0
    8 A/5 21173
    9 7.25
    10 
    11 S
    
    ----------------------------
    ['229', '0', '2', '" Mr. Arne Jonas Fahlstrom"', 'male', '18', '0', '0', '236171', '13', '', 'S\n']
    0 229
    1 0
    2 2
    3 " Mr. Arne Jonas Fahlstrom"
    4 male
    5 18
    6 0
    7 0
    8 236171
    9 13
    10 
    11 S
    
    ----------------------------
    ['230', '0', '3', '" Miss. Mathilde Lefebre"', 'female', '', '3', '1', '4133', '25.4667', '', 'S\n']
    0 230
    1 0
    2 3
    3 " Miss. Mathilde Lefebre"
    4 female
    5 
    6 3
    7 1
    8 4133
    9 25.4667
    10 
    11 S
    
    ----------------------------
    ['231', '1', '1', '" Mrs. Henry Birkhardt (Irene Wallach) Harris"', 'female', '35', '1', '0', '36973', '83.475', 'C83', 'S\n']
    0 231
    1 1
    2 1
    3 " Mrs. Henry Birkhardt (Irene Wallach) Harris"
    4 female
    5 35
    6 1
    7 0
    8 36973
    9 83.475
    10 C83
    11 S
    
    ----------------------------
    ['232', '0', '3', '" Mr. Bengt Edvin Larsson"', 'male', '29', '0', '0', '347067', '7.775', '', 'S\n']
    0 232
    1 0
    2 3
    3 " Mr. Bengt Edvin Larsson"
    4 male
    5 29
    6 0
    7 0
    8 347067
    9 7.775
    10 
    11 S
    
    ----------------------------
    ['233', '0', '2', '" Mr. Ernst Adolf Sjostedt"', 'male', '59', '0', '0', '237442', '13.5', '', 'S\n']
    0 233
    1 0
    2 2
    3 " Mr. Ernst Adolf Sjostedt"
    4 male
    5 59
    6 0
    7 0
    8 237442
    9 13.5
    10 
    11 S
    
    ----------------------------
    ['234', '1', '3', '" Miss. Lillian Gertrud Asplund"', 'female', '5', '4', '2', '347077', '31.3875', '', 'S\n']
    0 234
    1 1
    2 3
    3 " Miss. Lillian Gertrud Asplund"
    4 female
    5 5
    6 4
    7 2
    8 347077
    9 31.3875
    10 
    11 S
    
    ----------------------------
    ['235', '0', '2', '" Mr. Robert William Norman Leyson"', 'male', '24', '0', '0', 'C.A. 29566', '10.5', '', 'S\n']
    0 235
    1 0
    2 2
    3 " Mr. Robert William Norman Leyson"
    4 male
    5 24
    6 0
    7 0
    8 C.A. 29566
    9 10.5
    10 
    11 S
    
    ----------------------------
    ['236', '0', '3', '" Miss. Alice Phoebe Harknett"', 'female', '', '0', '0', 'W./C. 6609', '7.55', '', 'S\n']
    0 236
    1 0
    2 3
    3 " Miss. Alice Phoebe Harknett"
    4 female
    5 
    6 0
    7 0
    8 W./C. 6609
    9 7.55
    10 
    11 S
    
    ----------------------------
    ['237', '0', '2', '" Mr. Stephen Hold"', 'male', '44', '1', '0', '26707', '26', '', 'S\n']
    0 237
    1 0
    2 2
    3 " Mr. Stephen Hold"
    4 male
    5 44
    6 1
    7 0
    8 26707
    9 26
    10 
    11 S
    
    ----------------------------
    ['238', '1', '2', '" Miss. Marjorie ""Lottie"" Collyer"', 'female', '8', '0', '2', 'C.A. 31921', '26.25', '', 'S\n']
    0 238
    1 1
    2 2
    3 " Miss. Marjorie ""Lottie"" Collyer"
    4 female
    5 8
    6 0
    7 2
    8 C.A. 31921
    9 26.25
    10 
    11 S
    
    ----------------------------
    ['239', '0', '2', '" Mr. Frederick William Pengelly"', 'male', '19', '0', '0', '28665', '10.5', '', 'S\n']
    0 239
    1 0
    2 2
    3 " Mr. Frederick William Pengelly"
    4 male
    5 19
    6 0
    7 0
    8 28665
    9 10.5
    10 
    11 S
    
    ----------------------------
    ['240', '0', '2', '" Mr. George Henry Hunt"', 'male', '33', '0', '0', 'SCO/W 1585', '12.275', '', 'S\n']
    0 240
    1 0
    2 2
    3 " Mr. George Henry Hunt"
    4 male
    5 33
    6 0
    7 0
    8 SCO/W 1585
    9 12.275
    10 
    11 S
    
    ----------------------------
    ['241', '0', '3', '" Miss. Thamine Zabour"', 'female', '', '1', '0', '2665', '14.4542', '', 'C\n']
    0 241
    1 0
    2 3
    3 " Miss. Thamine Zabour"
    4 female
    5 
    6 1
    7 0
    8 2665
    9 14.4542
    10 
    11 C
    
    ----------------------------
    ['242', '1', '3', '" Miss. Katherine ""Kate"" Murphy"', 'female', '', '1', '0', '367230', '15.5', '', 'Q\n']
    0 242
    1 1
    2 3
    3 " Miss. Katherine ""Kate"" Murphy"
    4 female
    5 
    6 1
    7 0
    8 367230
    9 15.5
    10 
    11 Q
    
    ----------------------------
    ['243', '0', '2', '" Mr. Reginald Charles Coleridge"', 'male', '29', '0', '0', 'W./C. 14263', '10.5', '', 'S\n']
    0 243
    1 0
    2 2
    3 " Mr. Reginald Charles Coleridge"
    4 male
    5 29
    6 0
    7 0
    8 W./C. 14263
    9 10.5
    10 
    11 S
    
    ----------------------------
    ['244', '0', '3', '" Mr. Matti Alexanteri Maenpaa"', 'male', '22', '0', '0', 'STON/O 2. 3101275', '7.125', '', 'S\n']
    0 244
    1 0
    2 3
    3 " Mr. Matti Alexanteri Maenpaa"
    4 male
    5 22
    6 0
    7 0
    8 STON/O 2. 3101275
    9 7.125
    10 
    11 S
    
    ----------------------------
    ['245', '0', '3', '" Mr. Sleiman Attalah"', 'male', '30', '0', '0', '2694', '7.225', '', 'C\n']
    0 245
    1 0
    2 3
    3 " Mr. Sleiman Attalah"
    4 male
    5 30
    6 0
    7 0
    8 2694
    9 7.225
    10 
    11 C
    
    ----------------------------
    ['246', '0', '1', '" Dr. William Edward Minahan"', 'male', '44', '2', '0', '19928', '90', 'C78', 'Q\n']
    0 246
    1 0
    2 1
    3 " Dr. William Edward Minahan"
    4 male
    5 44
    6 2
    7 0
    8 19928
    9 90
    10 C78
    11 Q
    
    ----------------------------
    ['247', '0', '3', '" Miss. Agda Thorilda Viktoria Lindahl"', 'female', '25', '0', '0', '347071', '7.775', '', 'S\n']
    0 247
    1 0
    2 3
    3 " Miss. Agda Thorilda Viktoria Lindahl"
    4 female
    5 25
    6 0
    7 0
    8 347071
    9 7.775
    10 
    11 S
    
    ----------------------------
    ['248', '1', '2', '" Mrs. William (Anna) Hamalainen"', 'female', '24', '0', '2', '250649', '14.5', '', 'S\n']
    0 248
    1 1
    2 2
    3 " Mrs. William (Anna) Hamalainen"
    4 female
    5 24
    6 0
    7 2
    8 250649
    9 14.5
    10 
    11 S
    
    ----------------------------
    ['249', '1', '1', '" Mr. Richard Leonard Beckwith"', 'male', '37', '1', '1', '11751', '52.5542', 'D35', 'S\n']
    0 249
    1 1
    2 1
    3 " Mr. Richard Leonard Beckwith"
    4 male
    5 37
    6 1
    7 1
    8 11751
    9 52.5542
    10 D35
    11 S
    
    ----------------------------
    ['250', '0', '2', '" Rev. Ernest Courtenay Carter"', 'male', '54', '1', '0', '244252', '26', '', 'S\n']
    0 250
    1 0
    2 2
    3 " Rev. Ernest Courtenay Carter"
    4 male
    5 54
    6 1
    7 0
    8 244252
    9 26
    10 
    11 S
    
    ----------------------------
    ['251', '0', '3', '" Mr. James George Reed"', 'male', '', '0', '0', '362316', '7.25', '', 'S\n']
    0 251
    1 0
    2 3
    3 " Mr. James George Reed"
    4 male
    5 
    6 0
    7 0
    8 362316
    9 7.25
    10 
    11 S
    
    ----------------------------
    ['252', '0', '3', '" Mrs. Wilhelm (Elna Matilda Persson) Strom"', 'female', '29', '1', '1', '347054', '10.4625', 'G6', 'S\n']
    0 252
    1 0
    2 3
    3 " Mrs. Wilhelm (Elna Matilda Persson) Strom"
    4 female
    5 29
    6 1
    7 1
    8 347054
    9 10.4625
    10 G6
    11 S
    
    ----------------------------
    ['253', '0', '1', '" Mr. William Thomas Stead"', 'male', '62', '0', '0', '113514', '26.55', 'C87', 'S\n']
    0 253
    1 0
    2 1
    3 " Mr. William Thomas Stead"
    4 male
    5 62
    6 0
    7 0
    8 113514
    9 26.55
    10 C87
    11 S
    
    ----------------------------
    ['254', '0', '3', '" Mr. William Arthur Lobb"', 'male', '30', '1', '0', 'A/5. 3336', '16.1', '', 'S\n']
    0 254
    1 0
    2 3
    3 " Mr. William Arthur Lobb"
    4 male
    5 30
    6 1
    7 0
    8 A/5. 3336
    9 16.1
    10 
    11 S
    
    ----------------------------
    ['255', '0', '3', '" Mrs. Viktor (Helena Wilhelmina) Rosblom"', 'female', '41', '0', '2', '370129', '20.2125', '', 'S\n']
    0 255
    1 0
    2 3
    3 " Mrs. Viktor (Helena Wilhelmina) Rosblom"
    4 female
    5 41
    6 0
    7 2
    8 370129
    9 20.2125
    10 
    11 S
    
    ----------------------------
    ['256', '1', '3', '" Mrs. Darwis (Hanne Youssef Razi) Touma"', 'female', '29', '0', '2', '2650', '15.2458', '', 'C\n']
    0 256
    1 1
    2 3
    3 " Mrs. Darwis (Hanne Youssef Razi) Touma"
    4 female
    5 29
    6 0
    7 2
    8 2650
    9 15.2458
    10 
    11 C
    
    ----------------------------
    ['257', '1', '1', '" Mrs. Gertrude Maybelle Thorne"', 'female', '', '0', '0', 'PC 17585', '79.2', '', 'C\n']
    0 257
    1 1
    2 1
    3 " Mrs. Gertrude Maybelle Thorne"
    4 female
    5 
    6 0
    7 0
    8 PC 17585
    9 79.2
    10 
    11 C
    
    ----------------------------
    ['258', '1', '1', '" Miss. Gladys Cherry"', 'female', '30', '0', '0', '110152', '86.5', 'B77', 'S\n']
    0 258
    1 1
    2 1
    3 " Miss. Gladys Cherry"
    4 female
    5 30
    6 0
    7 0
    8 110152
    9 86.5
    10 B77
    11 S
    
    ----------------------------
    ['259', '1', '1', '" Miss. Anna Ward"', 'female', '35', '0', '0', 'PC 17755', '512.3292', '', 'C\n']
    0 259
    1 1
    2 1
    3 " Miss. Anna Ward"
    4 female
    5 35
    6 0
    7 0
    8 PC 17755
    9 512.3292
    10 
    11 C
    
    ----------------------------
    ['260', '1', '2', '" Mrs. (Lutie Davis) Parrish"', 'female', '50', '0', '1', '230433', '26', '', 'S\n']
    0 260
    1 1
    2 2
    3 " Mrs. (Lutie Davis) Parrish"
    4 female
    5 50
    6 0
    7 1
    8 230433
    9 26
    10 
    11 S
    
    ----------------------------
    ['261', '0', '3', '" Mr. Thomas Smith"', 'male', '', '0', '0', '384461', '7.75', '', 'Q\n']
    0 261
    1 0
    2 3
    3 " Mr. Thomas Smith"
    4 male
    5 
    6 0
    7 0
    8 384461
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['262', '1', '3', '" Master. Edvin Rojj Felix Asplund"', 'male', '3', '4', '2', '347077', '31.3875', '', 'S\n']
    0 262
    1 1
    2 3
    3 " Master. Edvin Rojj Felix Asplund"
    4 male
    5 3
    6 4
    7 2
    8 347077
    9 31.3875
    10 
    11 S
    
    ----------------------------
    ['263', '0', '1', '" Mr. Emil Taussig"', 'male', '52', '1', '1', '110413', '79.65', 'E67', 'S\n']
    0 263
    1 0
    2 1
    3 " Mr. Emil Taussig"
    4 male
    5 52
    6 1
    7 1
    8 110413
    9 79.65
    10 E67
    11 S
    
    ----------------------------
    ['264', '0', '1', '" Mr. William Harrison"', 'male', '40', '0', '0', '112059', '0', 'B94', 'S\n']
    0 264
    1 0
    2 1
    3 " Mr. William Harrison"
    4 male
    5 40
    6 0
    7 0
    8 112059
    9 0
    10 B94
    11 S
    
    ----------------------------
    ['265', '0', '3', '" Miss. Delia Henry"', 'female', '', '0', '0', '382649', '7.75', '', 'Q\n']
    0 265
    1 0
    2 3
    3 " Miss. Delia Henry"
    4 female
    5 
    6 0
    7 0
    8 382649
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['266', '0', '2', '" Mr. David Reeves"', 'male', '36', '0', '0', 'C.A. 17248', '10.5', '', 'S\n']
    0 266
    1 0
    2 2
    3 " Mr. David Reeves"
    4 male
    5 36
    6 0
    7 0
    8 C.A. 17248
    9 10.5
    10 
    11 S
    
    ----------------------------
    ['267', '0', '3', '" Mr. Ernesti Arvid Panula"', 'male', '16', '4', '1', '3101295', '39.6875', '', 'S\n']
    0 267
    1 0
    2 3
    3 " Mr. Ernesti Arvid Panula"
    4 male
    5 16
    6 4
    7 1
    8 3101295
    9 39.6875
    10 
    11 S
    
    ----------------------------
    ['268', '1', '3', '" Mr. Ernst Ulrik Persson"', 'male', '25', '1', '0', '347083', '7.775', '', 'S\n']
    0 268
    1 1
    2 3
    3 " Mr. Ernst Ulrik Persson"
    4 male
    5 25
    6 1
    7 0
    8 347083
    9 7.775
    10 
    11 S
    
    ----------------------------
    ['269', '1', '1', '" Mrs. William Thompson (Edith Junkins) Graham"', 'female', '58', '0', '1', 'PC 17582', '153.4625', 'C125', 'S\n']
    0 269
    1 1
    2 1
    3 " Mrs. William Thompson (Edith Junkins) Graham"
    4 female
    5 58
    6 0
    7 1
    8 PC 17582
    9 153.4625
    10 C125
    11 S
    
    ----------------------------
    ['270', '1', '1', '" Miss. Amelia Bissette"', 'female', '35', '0', '0', 'PC 17760', '135.6333', 'C99', 'S\n']
    0 270
    1 1
    2 1
    3 " Miss. Amelia Bissette"
    4 female
    5 35
    6 0
    7 0
    8 PC 17760
    9 135.6333
    10 C99
    11 S
    
    ----------------------------
    ['271', '0', '1', '" Mr. Alexander Cairns"', 'male', '', '0', '0', '113798', '31', '', 'S\n']
    0 271
    1 0
    2 1
    3 " Mr. Alexander Cairns"
    4 male
    5 
    6 0
    7 0
    8 113798
    9 31
    10 
    11 S
    
    ----------------------------
    ['272', '1', '3', '" Mr. William Henry Tornquist"', 'male', '25', '0', '0', 'LINE', '0', '', 'S\n']
    0 272
    1 1
    2 3
    3 " Mr. William Henry Tornquist"
    4 male
    5 25
    6 0
    7 0
    8 LINE
    9 0
    10 
    11 S
    
    ----------------------------
    ['273', '1', '2', '" Mrs. (Elizabeth Anne Maidment) Mellinger"', 'female', '41', '0', '1', '250644', '19.5', '', 'S\n']
    0 273
    1 1
    2 2
    3 " Mrs. (Elizabeth Anne Maidment) Mellinger"
    4 female
    5 41
    6 0
    7 1
    8 250644
    9 19.5
    10 
    11 S
    
    ----------------------------
    ['274', '0', '1', '" Mr. Charles H Natsch"', 'male', '37', '0', '1', 'PC 17596', '29.7', 'C118', 'C\n']
    0 274
    1 0
    2 1
    3 " Mr. Charles H Natsch"
    4 male
    5 37
    6 0
    7 1
    8 PC 17596
    9 29.7
    10 C118
    11 C
    
    ----------------------------
    ['275', '1', '3', '" Miss. Hanora ""Nora"" Healy"', 'female', '', '0', '0', '370375', '7.75', '', 'Q\n']
    0 275
    1 1
    2 3
    3 " Miss. Hanora ""Nora"" Healy"
    4 female
    5 
    6 0
    7 0
    8 370375
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['276', '1', '1', '" Miss. Kornelia Theodosia Andrews"', 'female', '63', '1', '0', '13502', '77.9583', 'D7', 'S\n']
    0 276
    1 1
    2 1
    3 " Miss. Kornelia Theodosia Andrews"
    4 female
    5 63
    6 1
    7 0
    8 13502
    9 77.9583
    10 D7
    11 S
    
    ----------------------------
    ['277', '0', '3', '" Miss. Augusta Charlotta Lindblom"', 'female', '45', '0', '0', '347073', '7.75', '', 'S\n']
    0 277
    1 0
    2 3
    3 " Miss. Augusta Charlotta Lindblom"
    4 female
    5 45
    6 0
    7 0
    8 347073
    9 7.75
    10 
    11 S
    
    ----------------------------
    ['278', '0', '2', '" Mr. Francis ""Frank"" Parkes"', 'male', '', '0', '0', '239853', '0', '', 'S\n']
    0 278
    1 0
    2 2
    3 " Mr. Francis ""Frank"" Parkes"
    4 male
    5 
    6 0
    7 0
    8 239853
    9 0
    10 
    11 S
    
    ----------------------------
    ['279', '0', '3', '" Master. Eric Rice"', 'male', '7', '4', '1', '382652', '29.125', '', 'Q\n']
    0 279
    1 0
    2 3
    3 " Master. Eric Rice"
    4 male
    5 7
    6 4
    7 1
    8 382652
    9 29.125
    10 
    11 Q
    
    ----------------------------
    ['280', '1', '3', '" Mrs. Stanton (Rosa Hunt) Abbott"', 'female', '35', '1', '1', 'C.A. 2673', '20.25', '', 'S\n']
    0 280
    1 1
    2 3
    3 " Mrs. Stanton (Rosa Hunt) Abbott"
    4 female
    5 35
    6 1
    7 1
    8 C.A. 2673
    9 20.25
    10 
    11 S
    
    ----------------------------
    ['281', '0', '3', '" Mr. Frank Duane"', 'male', '65', '0', '0', '336439', '7.75', '', 'Q\n']
    0 281
    1 0
    2 3
    3 " Mr. Frank Duane"
    4 male
    5 65
    6 0
    7 0
    8 336439
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['282', '0', '3', '" Mr. Nils Johan Goransson Olsson"', 'male', '28', '0', '0', '347464', '7.8542', '', 'S\n']
    0 282
    1 0
    2 3
    3 " Mr. Nils Johan Goransson Olsson"
    4 male
    5 28
    6 0
    7 0
    8 347464
    9 7.8542
    10 
    11 S
    
    ----------------------------
    ['283', '0', '3', '" Mr. Alfons de Pelsmaeker"', 'male', '16', '0', '0', '345778', '9.5', '', 'S\n']
    0 283
    1 0
    2 3
    3 " Mr. Alfons de Pelsmaeker"
    4 male
    5 16
    6 0
    7 0
    8 345778
    9 9.5
    10 
    11 S
    
    ----------------------------
    ['284', '1', '3', '" Mr. Edward Arthur Dorking"', 'male', '19', '0', '0', 'A/5. 10482', '8.05', '', 'S\n']
    0 284
    1 1
    2 3
    3 " Mr. Edward Arthur Dorking"
    4 male
    5 19
    6 0
    7 0
    8 A/5. 10482
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['285', '0', '1', '" Mr. Richard William Smith"', 'male', '', '0', '0', '113056', '26', 'A19', 'S\n']
    0 285
    1 0
    2 1
    3 " Mr. Richard William Smith"
    4 male
    5 
    6 0
    7 0
    8 113056
    9 26
    10 A19
    11 S
    
    ----------------------------
    ['286', '0', '3', '" Mr. Ivan Stankovic"', 'male', '33', '0', '0', '349239', '8.6625', '', 'C\n']
    0 286
    1 0
    2 3
    3 " Mr. Ivan Stankovic"
    4 male
    5 33
    6 0
    7 0
    8 349239
    9 8.6625
    10 
    11 C
    
    ----------------------------
    ['287', '1', '3', '" Mr. Theodore de Mulder"', 'male', '30', '0', '0', '345774', '9.5', '', 'S\n']
    0 287
    1 1
    2 3
    3 " Mr. Theodore de Mulder"
    4 male
    5 30
    6 0
    7 0
    8 345774
    9 9.5
    10 
    11 S
    
    ----------------------------
    ['288', '0', '3', '" Mr. Penko Naidenoff"', 'male', '22', '0', '0', '349206', '7.8958', '', 'S\n']
    0 288
    1 0
    2 3
    3 " Mr. Penko Naidenoff"
    4 male
    5 22
    6 0
    7 0
    8 349206
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['289', '1', '2', '" Mr. Masabumi Hosono"', 'male', '42', '0', '0', '237798', '13', '', 'S\n']
    0 289
    1 1
    2 2
    3 " Mr. Masabumi Hosono"
    4 male
    5 42
    6 0
    7 0
    8 237798
    9 13
    10 
    11 S
    
    ----------------------------
    ['290', '1', '3', '" Miss. Kate Connolly"', 'female', '22', '0', '0', '370373', '7.75', '', 'Q\n']
    0 290
    1 1
    2 3
    3 " Miss. Kate Connolly"
    4 female
    5 22
    6 0
    7 0
    8 370373
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['291', '1', '1', '" Miss. Ellen ""Nellie"" Barber"', 'female', '26', '0', '0', '19877', '78.85', '', 'S\n']
    0 291
    1 1
    2 1
    3 " Miss. Ellen ""Nellie"" Barber"
    4 female
    5 26
    6 0
    7 0
    8 19877
    9 78.85
    10 
    11 S
    
    ----------------------------
    ['292', '1', '1', '" Mrs. Dickinson H (Helen Walton) Bishop"', 'female', '19', '1', '0', '11967', '91.0792', 'B49', 'C\n']
    0 292
    1 1
    2 1
    3 " Mrs. Dickinson H (Helen Walton) Bishop"
    4 female
    5 19
    6 1
    7 0
    8 11967
    9 91.0792
    10 B49
    11 C
    
    ----------------------------
    ['293', '0', '2', '" Mr. Rene Jacques Levy"', 'male', '36', '0', '0', 'SC/Paris 2163', '12.875', 'D', 'C\n']
    0 293
    1 0
    2 2
    3 " Mr. Rene Jacques Levy"
    4 male
    5 36
    6 0
    7 0
    8 SC/Paris 2163
    9 12.875
    10 D
    11 C
    
    ----------------------------
    ['294', '0', '3', '" Miss. Aloisia Haas"', 'female', '24', '0', '0', '349236', '8.85', '', 'S\n']
    0 294
    1 0
    2 3
    3 " Miss. Aloisia Haas"
    4 female
    5 24
    6 0
    7 0
    8 349236
    9 8.85
    10 
    11 S
    
    ----------------------------
    ['295', '0', '3', '" Mr. Ivan Mineff"', 'male', '24', '0', '0', '349233', '7.8958', '', 'S\n']
    0 295
    1 0
    2 3
    3 " Mr. Ivan Mineff"
    4 male
    5 24
    6 0
    7 0
    8 349233
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['296', '0', '1', '" Mr. Ervin G Lewy"', 'male', '', '0', '0', 'PC 17612', '27.7208', '', 'C\n']
    0 296
    1 0
    2 1
    3 " Mr. Ervin G Lewy"
    4 male
    5 
    6 0
    7 0
    8 PC 17612
    9 27.7208
    10 
    11 C
    
    ----------------------------
    ['297', '0', '3', '" Mr. Mansour Hanna"', 'male', '23.5', '0', '0', '2693', '7.2292', '', 'C\n']
    0 297
    1 0
    2 3
    3 " Mr. Mansour Hanna"
    4 male
    5 23.5
    6 0
    7 0
    8 2693
    9 7.2292
    10 
    11 C
    
    ----------------------------
    ['298', '0', '1', '" Miss. Helen Loraine Allison"', 'female', '2', '1', '2', '113781', '151.55', 'C22 C26', 'S\n']
    0 298
    1 0
    2 1
    3 " Miss. Helen Loraine Allison"
    4 female
    5 2
    6 1
    7 2
    8 113781
    9 151.55
    10 C22 C26
    11 S
    
    ----------------------------
    ['299', '1', '1', '" Mr. Adolphe Saalfeld"', 'male', '', '0', '0', '19988', '30.5', 'C106', 'S\n']
    0 299
    1 1
    2 1
    3 " Mr. Adolphe Saalfeld"
    4 male
    5 
    6 0
    7 0
    8 19988
    9 30.5
    10 C106
    11 S
    
    ----------------------------
    ['300', '1', '1', '" Mrs. James (Helene DeLaudeniere Chaput) Baxter"', 'female', '50', '0', '1', 'PC 17558', '247.5208', 'B58 B60', 'C\n']
    0 300
    1 1
    2 1
    3 " Mrs. James (Helene DeLaudeniere Chaput) Baxter"
    4 female
    5 50
    6 0
    7 1
    8 PC 17558
    9 247.5208
    10 B58 B60
    11 C
    
    ----------------------------
    ['301', '1', '3', '" Miss. Anna Katherine ""Annie Kate"" Kelly"', 'female', '', '0', '0', '9234', '7.75', '', 'Q\n']
    0 301
    1 1
    2 3
    3 " Miss. Anna Katherine ""Annie Kate"" Kelly"
    4 female
    5 
    6 0
    7 0
    8 9234
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['302', '1', '3', '" Mr. Bernard McCoy"', 'male', '', '2', '0', '367226', '23.25', '', 'Q\n']
    0 302
    1 1
    2 3
    3 " Mr. Bernard McCoy"
    4 male
    5 
    6 2
    7 0
    8 367226
    9 23.25
    10 
    11 Q
    
    ----------------------------
    ['303', '0', '3', '" Mr. William Cahoone Jr Johnson"', 'male', '19', '0', '0', 'LINE', '0', '', 'S\n']
    0 303
    1 0
    2 3
    3 " Mr. William Cahoone Jr Johnson"
    4 male
    5 19
    6 0
    7 0
    8 LINE
    9 0
    10 
    11 S
    
    ----------------------------
    ['304', '1', '2', '" Miss. Nora A Keane"', 'female', '', '0', '0', '226593', '12.35', 'E101', 'Q\n']
    0 304
    1 1
    2 2
    3 " Miss. Nora A Keane"
    4 female
    5 
    6 0
    7 0
    8 226593
    9 12.35
    10 E101
    11 Q
    
    ----------------------------
    ['305', '0', '3', '" Mr. Howard Hugh ""Harry"" Williams"', 'male', '', '0', '0', 'A/5 2466', '8.05', '', 'S\n']
    0 305
    1 0
    2 3
    3 " Mr. Howard Hugh ""Harry"" Williams"
    4 male
    5 
    6 0
    7 0
    8 A/5 2466
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['306', '1', '1', '" Master. Hudson Trevor Allison"', 'male', '0.92', '1', '2', '113781', '151.55', 'C22 C26', 'S\n']
    0 306
    1 1
    2 1
    3 " Master. Hudson Trevor Allison"
    4 male
    5 0.92
    6 1
    7 2
    8 113781
    9 151.55
    10 C22 C26
    11 S
    
    ----------------------------
    ['307', '1', '1', '" Miss. Margaret Fleming"', 'female', '', '0', '0', '17421', '110.8833', '', 'C\n']
    0 307
    1 1
    2 1
    3 " Miss. Margaret Fleming"
    4 female
    5 
    6 0
    7 0
    8 17421
    9 110.8833
    10 
    11 C
    
    ----------------------------
    ['308', '1', '1', '" Mrs. Victor de Satode (Maria Josefa Perez de Soto y Vallejo) Penasco y Castellana"', 'female', '17', '1', '0', 'PC 17758', '108.9', 'C65', 'C\n']
    0 308
    1 1
    2 1
    3 " Mrs. Victor de Satode (Maria Josefa Perez de Soto y Vallejo) Penasco y Castellana"
    4 female
    5 17
    6 1
    7 0
    8 PC 17758
    9 108.9
    10 C65
    11 C
    
    ----------------------------
    ['309', '0', '2', '" Mr. Samuel Abelson"', 'male', '30', '1', '0', 'P/PP 3381', '24', '', 'C\n']
    0 309
    1 0
    2 2
    3 " Mr. Samuel Abelson"
    4 male
    5 30
    6 1
    7 0
    8 P/PP 3381
    9 24
    10 
    11 C
    
    ----------------------------
    ['310', '1', '1', '" Miss. Laura Mabel Francatelli"', 'female', '30', '0', '0', 'PC 17485', '56.9292', 'E36', 'C\n']
    0 310
    1 1
    2 1
    3 " Miss. Laura Mabel Francatelli"
    4 female
    5 30
    6 0
    7 0
    8 PC 17485
    9 56.9292
    10 E36
    11 C
    
    ----------------------------
    ['311', '1', '1', '" Miss. Margaret Bechstein Hays"', 'female', '24', '0', '0', '11767', '83.1583', 'C54', 'C\n']
    0 311
    1 1
    2 1
    3 " Miss. Margaret Bechstein Hays"
    4 female
    5 24
    6 0
    7 0
    8 11767
    9 83.1583
    10 C54
    11 C
    
    ----------------------------
    ['312', '1', '1', '" Miss. Emily Borie Ryerson"', 'female', '18', '2', '2', 'PC 17608', '262.375', 'B57 B59 B63 B66', 'C\n']
    0 312
    1 1
    2 1
    3 " Miss. Emily Borie Ryerson"
    4 female
    5 18
    6 2
    7 2
    8 PC 17608
    9 262.375
    10 B57 B59 B63 B66
    11 C
    
    ----------------------------
    ['313', '0', '2', '" Mrs. William (Anna Sylfven) Lahtinen"', 'female', '26', '1', '1', '250651', '26', '', 'S\n']
    0 313
    1 0
    2 2
    3 " Mrs. William (Anna Sylfven) Lahtinen"
    4 female
    5 26
    6 1
    7 1
    8 250651
    9 26
    10 
    11 S
    
    ----------------------------
    ['314', '0', '3', '" Mr. Ignjac Hendekovic"', 'male', '28', '0', '0', '349243', '7.8958', '', 'S\n']
    0 314
    1 0
    2 3
    3 " Mr. Ignjac Hendekovic"
    4 male
    5 28
    6 0
    7 0
    8 349243
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['315', '0', '2', '" Mr. Benjamin Hart"', 'male', '43', '1', '1', 'F.C.C. 13529', '26.25', '', 'S\n']
    0 315
    1 0
    2 2
    3 " Mr. Benjamin Hart"
    4 male
    5 43
    6 1
    7 1
    8 F.C.C. 13529
    9 26.25
    10 
    11 S
    
    ----------------------------
    ['316', '1', '3', '" Miss. Helmina Josefina Nilsson"', 'female', '26', '0', '0', '347470', '7.8542', '', 'S\n']
    0 316
    1 1
    2 3
    3 " Miss. Helmina Josefina Nilsson"
    4 female
    5 26
    6 0
    7 0
    8 347470
    9 7.8542
    10 
    11 S
    
    ----------------------------
    ['317', '1', '2', '" Mrs. Sinai (Miriam Sternin) Kantor"', 'female', '24', '1', '0', '244367', '26', '', 'S\n']
    0 317
    1 1
    2 2
    3 " Mrs. Sinai (Miriam Sternin) Kantor"
    4 female
    5 24
    6 1
    7 0
    8 244367
    9 26
    10 
    11 S
    
    ----------------------------
    ['318', '0', '2', '" Dr. Ernest Moraweck"', 'male', '54', '0', '0', '29011', '14', '', 'S\n']
    0 318
    1 0
    2 2
    3 " Dr. Ernest Moraweck"
    4 male
    5 54
    6 0
    7 0
    8 29011
    9 14
    10 
    11 S
    
    ----------------------------
    ['319', '1', '1', '" Miss. Mary Natalie Wick"', 'female', '31', '0', '2', '36928', '164.8667', 'C7', 'S\n']
    0 319
    1 1
    2 1
    3 " Miss. Mary Natalie Wick"
    4 female
    5 31
    6 0
    7 2
    8 36928
    9 164.8667
    10 C7
    11 S
    
    ----------------------------
    ['320', '1', '1', '" Mrs. Frederic Oakley (Margaretta Corning Stone) Spedden"', 'female', '40', '1', '1', '16966', '134.5', 'E34', 'C\n']
    0 320
    1 1
    2 1
    3 " Mrs. Frederic Oakley (Margaretta Corning Stone) Spedden"
    4 female
    5 40
    6 1
    7 1
    8 16966
    9 134.5
    10 E34
    11 C
    
    ----------------------------
    ['321', '0', '3', '" Mr. Samuel Dennis"', 'male', '22', '0', '0', 'A/5 21172', '7.25', '', 'S\n']
    0 321
    1 0
    2 3
    3 " Mr. Samuel Dennis"
    4 male
    5 22
    6 0
    7 0
    8 A/5 21172
    9 7.25
    10 
    11 S
    
    ----------------------------
    ['322', '0', '3', '" Mr. Yoto Danoff"', 'male', '27', '0', '0', '349219', '7.8958', '', 'S\n']
    0 322
    1 0
    2 3
    3 " Mr. Yoto Danoff"
    4 male
    5 27
    6 0
    7 0
    8 349219
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['323', '1', '2', '" Miss. Hilda Mary Slayter"', 'female', '30', '0', '0', '234818', '12.35', '', 'Q\n']
    0 323
    1 1
    2 2
    3 " Miss. Hilda Mary Slayter"
    4 female
    5 30
    6 0
    7 0
    8 234818
    9 12.35
    10 
    11 Q
    
    ----------------------------
    ['324', '1', '2', '" Mrs. Albert Francis (Sylvia Mae Harbaugh) Caldwell"', 'female', '22', '1', '1', '248738', '29', '', 'S\n']
    0 324
    1 1
    2 2
    3 " Mrs. Albert Francis (Sylvia Mae Harbaugh) Caldwell"
    4 female
    5 22
    6 1
    7 1
    8 248738
    9 29
    10 
    11 S
    
    ----------------------------
    ['325', '0', '3', '" Mr. George John Jr Sage"', 'male', '', '8', '2', 'CA. 2343', '69.55', '', 'S\n']
    0 325
    1 0
    2 3
    3 " Mr. George John Jr Sage"
    4 male
    5 
    6 8
    7 2
    8 CA. 2343
    9 69.55
    10 
    11 S
    
    ----------------------------
    ['326', '1', '1', '" Miss. Marie Grice Young"', 'female', '36', '0', '0', 'PC 17760', '135.6333', 'C32', 'C\n']
    0 326
    1 1
    2 1
    3 " Miss. Marie Grice Young"
    4 female
    5 36
    6 0
    7 0
    8 PC 17760
    9 135.6333
    10 C32
    11 C
    
    ----------------------------
    ['327', '0', '3', '" Mr. Johan Hansen Nysveen"', 'male', '61', '0', '0', '345364', '6.2375', '', 'S\n']
    0 327
    1 0
    2 3
    3 " Mr. Johan Hansen Nysveen"
    4 male
    5 61
    6 0
    7 0
    8 345364
    9 6.2375
    10 
    11 S
    
    ----------------------------
    ['328', '1', '2', '" Mrs. (Ada E Hall) Ball"', 'female', '36', '0', '0', '28551', '13', 'D', 'S\n']
    0 328
    1 1
    2 2
    3 " Mrs. (Ada E Hall) Ball"
    4 female
    5 36
    6 0
    7 0
    8 28551
    9 13
    10 D
    11 S
    
    ----------------------------
    ['329', '1', '3', '" Mrs. Frank John (Emily Alice Brown) Goldsmith"', 'female', '31', '1', '1', '363291', '20.525', '', 'S\n']
    0 329
    1 1
    2 3
    3 " Mrs. Frank John (Emily Alice Brown) Goldsmith"
    4 female
    5 31
    6 1
    7 1
    8 363291
    9 20.525
    10 
    11 S
    
    ----------------------------
    ['330', '1', '1', '" Miss. Jean Gertrude Hippach"', 'female', '16', '0', '1', '111361', '57.9792', 'B18', 'C\n']
    0 330
    1 1
    2 1
    3 " Miss. Jean Gertrude Hippach"
    4 female
    5 16
    6 0
    7 1
    8 111361
    9 57.9792
    10 B18
    11 C
    
    ----------------------------
    ['331', '1', '3', '" Miss. Agnes McCoy"', 'female', '', '2', '0', '367226', '23.25', '', 'Q\n']
    0 331
    1 1
    2 3
    3 " Miss. Agnes McCoy"
    4 female
    5 
    6 2
    7 0
    8 367226
    9 23.25
    10 
    11 Q
    
    ----------------------------
    ['332', '0', '1', '" Mr. Austen Partner"', 'male', '45.5', '0', '0', '113043', '28.5', 'C124', 'S\n']
    0 332
    1 0
    2 1
    3 " Mr. Austen Partner"
    4 male
    5 45.5
    6 0
    7 0
    8 113043
    9 28.5
    10 C124
    11 S
    
    ----------------------------
    ['333', '0', '1', '" Mr. George Edward Graham"', 'male', '38', '0', '1', 'PC 17582', '153.4625', 'C91', 'S\n']
    0 333
    1 0
    2 1
    3 " Mr. George Edward Graham"
    4 male
    5 38
    6 0
    7 1
    8 PC 17582
    9 153.4625
    10 C91
    11 S
    
    ----------------------------
    ['334', '0', '3', '" Mr. Leo Edmondus Vander Planke"', 'male', '16', '2', '0', '345764', '18', '', 'S\n']
    0 334
    1 0
    2 3
    3 " Mr. Leo Edmondus Vander Planke"
    4 male
    5 16
    6 2
    7 0
    8 345764
    9 18
    10 
    11 S
    
    ----------------------------
    ['335', '1', '1', '" Mrs. Henry William (Clara Heinsheimer) Frauenthal"', 'female', '', '1', '0', 'PC 17611', '133.65', '', 'S\n']
    0 335
    1 1
    2 1
    3 " Mrs. Henry William (Clara Heinsheimer) Frauenthal"
    4 female
    5 
    6 1
    7 0
    8 PC 17611
    9 133.65
    10 
    11 S
    
    ----------------------------
    ['336', '0', '3', '" Mr. Mitto Denkoff"', 'male', '', '0', '0', '349225', '7.8958', '', 'S\n']
    0 336
    1 0
    2 3
    3 " Mr. Mitto Denkoff"
    4 male
    5 
    6 0
    7 0
    8 349225
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['337', '0', '1', '" Mr. Thomas Clinton Pears"', 'male', '29', '1', '0', '113776', '66.6', 'C2', 'S\n']
    0 337
    1 0
    2 1
    3 " Mr. Thomas Clinton Pears"
    4 male
    5 29
    6 1
    7 0
    8 113776
    9 66.6
    10 C2
    11 S
    
    ----------------------------
    ['338', '1', '1', '" Miss. Elizabeth Margaret Burns"', 'female', '41', '0', '0', '16966', '134.5', 'E40', 'C\n']
    0 338
    1 1
    2 1
    3 " Miss. Elizabeth Margaret Burns"
    4 female
    5 41
    6 0
    7 0
    8 16966
    9 134.5
    10 E40
    11 C
    
    ----------------------------
    ['339', '1', '3', '" Mr. Karl Edwart Dahl"', 'male', '45', '0', '0', '7598', '8.05', '', 'S\n']
    0 339
    1 1
    2 3
    3 " Mr. Karl Edwart Dahl"
    4 male
    5 45
    6 0
    7 0
    8 7598
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['340', '0', '1', '" Mr. Stephen Weart Blackwell"', 'male', '45', '0', '0', '113784', '35.5', 'T', 'S\n']
    0 340
    1 0
    2 1
    3 " Mr. Stephen Weart Blackwell"
    4 male
    5 45
    6 0
    7 0
    8 113784
    9 35.5
    10 T
    11 S
    
    ----------------------------
    ['341', '1', '2', '" Master. Edmond Roger Navratil"', 'male', '2', '1', '1', '230080', '26', 'F2', 'S\n']
    0 341
    1 1
    2 2
    3 " Master. Edmond Roger Navratil"
    4 male
    5 2
    6 1
    7 1
    8 230080
    9 26
    10 F2
    11 S
    
    ----------------------------
    ['342', '1', '1', '" Miss. Alice Elizabeth Fortune"', 'female', '24', '3', '2', '19950', '263', 'C23 C25 C27', 'S\n']
    0 342
    1 1
    2 1
    3 " Miss. Alice Elizabeth Fortune"
    4 female
    5 24
    6 3
    7 2
    8 19950
    9 263
    10 C23 C25 C27
    11 S
    
    ----------------------------
    ['343', '0', '2', '" Mr. Erik Gustaf Collander"', 'male', '28', '0', '0', '248740', '13', '', 'S\n']
    0 343
    1 0
    2 2
    3 " Mr. Erik Gustaf Collander"
    4 male
    5 28
    6 0
    7 0
    8 248740
    9 13
    10 
    11 S
    
    ----------------------------
    ['344', '0', '2', '" Mr. Charles Frederick Waddington Sedgwick"', 'male', '25', '0', '0', '244361', '13', '', 'S\n']
    0 344
    1 0
    2 2
    3 " Mr. Charles Frederick Waddington Sedgwick"
    4 male
    5 25
    6 0
    7 0
    8 244361
    9 13
    10 
    11 S
    
    ----------------------------
    ['345', '0', '2', '" Mr. Stanley Hubert Fox"', 'male', '36', '0', '0', '229236', '13', '', 'S\n']
    0 345
    1 0
    2 2
    3 " Mr. Stanley Hubert Fox"
    4 male
    5 36
    6 0
    7 0
    8 229236
    9 13
    10 
    11 S
    
    ----------------------------
    ['346', '1', '2', '" Miss. Amelia ""Mildred"" Brown"', 'female', '24', '0', '0', '248733', '13', 'F33', 'S\n']
    0 346
    1 1
    2 2
    3 " Miss. Amelia ""Mildred"" Brown"
    4 female
    5 24
    6 0
    7 0
    8 248733
    9 13
    10 F33
    11 S
    
    ----------------------------
    ['347', '1', '2', '" Miss. Marion Elsie Smith"', 'female', '40', '0', '0', '31418', '13', '', 'S\n']
    0 347
    1 1
    2 2
    3 " Miss. Marion Elsie Smith"
    4 female
    5 40
    6 0
    7 0
    8 31418
    9 13
    10 
    11 S
    
    ----------------------------
    ['348', '1', '3', '" Mrs. Thomas Henry (Mary E Finck) Davison"', 'female', '', '1', '0', '386525', '16.1', '', 'S\n']
    0 348
    1 1
    2 3
    3 " Mrs. Thomas Henry (Mary E Finck) Davison"
    4 female
    5 
    6 1
    7 0
    8 386525
    9 16.1
    10 
    11 S
    
    ----------------------------
    ['349', '1', '3', '" Master. William Loch ""William"" Coutts"', 'male', '3', '1', '1', 'C.A. 37671', '15.9', '', 'S\n']
    0 349
    1 1
    2 3
    3 " Master. William Loch ""William"" Coutts"
    4 male
    5 3
    6 1
    7 1
    8 C.A. 37671
    9 15.9
    10 
    11 S
    
    ----------------------------
    ['350', '0', '3', '" Mr. Jovan Dimic"', 'male', '42', '0', '0', '315088', '8.6625', '', 'S\n']
    0 350
    1 0
    2 3
    3 " Mr. Jovan Dimic"
    4 male
    5 42
    6 0
    7 0
    8 315088
    9 8.6625
    10 
    11 S
    
    ----------------------------
    ['351', '0', '3', '" Mr. Nils Martin Odahl"', 'male', '23', '0', '0', '7267', '9.225', '', 'S\n']
    0 351
    1 0
    2 3
    3 " Mr. Nils Martin Odahl"
    4 male
    5 23
    6 0
    7 0
    8 7267
    9 9.225
    10 
    11 S
    
    ----------------------------
    ['352', '0', '1', '" Mr. Fletcher Fellows Williams-Lambert"', 'male', '', '0', '0', '113510', '35', 'C128', 'S\n']
    0 352
    1 0
    2 1
    3 " Mr. Fletcher Fellows Williams-Lambert"
    4 male
    5 
    6 0
    7 0
    8 113510
    9 35
    10 C128
    11 S
    
    ----------------------------
    ['353', '0', '3', '" Mr. Tannous Elias"', 'male', '15', '1', '1', '2695', '7.2292', '', 'C\n']
    0 353
    1 0
    2 3
    3 " Mr. Tannous Elias"
    4 male
    5 15
    6 1
    7 1
    8 2695
    9 7.2292
    10 
    11 C
    
    ----------------------------
    ['354', '0', '3', '" Mr. Josef Arnold-Franchi"', 'male', '25', '1', '0', '349237', '17.8', '', 'S\n']
    0 354
    1 0
    2 3
    3 " Mr. Josef Arnold-Franchi"
    4 male
    5 25
    6 1
    7 0
    8 349237
    9 17.8
    10 
    11 S
    
    ----------------------------
    ['355', '0', '3', '" Mr. Wazli Yousif"', 'male', '', '0', '0', '2647', '7.225', '', 'C\n']
    0 355
    1 0
    2 3
    3 " Mr. Wazli Yousif"
    4 male
    5 
    6 0
    7 0
    8 2647
    9 7.225
    10 
    11 C
    
    ----------------------------
    ['356', '0', '3', '" Mr. Leo Peter Vanden Steen"', 'male', '28', '0', '0', '345783', '9.5', '', 'S\n']
    0 356
    1 0
    2 3
    3 " Mr. Leo Peter Vanden Steen"
    4 male
    5 28
    6 0
    7 0
    8 345783
    9 9.5
    10 
    11 S
    
    ----------------------------
    ['357', '1', '1', '" Miss. Elsie Edith Bowerman"', 'female', '22', '0', '1', '113505', '55', 'E33', 'S\n']
    0 357
    1 1
    2 1
    3 " Miss. Elsie Edith Bowerman"
    4 female
    5 22
    6 0
    7 1
    8 113505
    9 55
    10 E33
    11 S
    
    ----------------------------
    ['358', '0', '2', '" Miss. Annie Clemmer Funk"', 'female', '38', '0', '0', '237671', '13', '', 'S\n']
    0 358
    1 0
    2 2
    3 " Miss. Annie Clemmer Funk"
    4 female
    5 38
    6 0
    7 0
    8 237671
    9 13
    10 
    11 S
    
    ----------------------------
    ['359', '1', '3', '" Miss. Mary McGovern"', 'female', '', '0', '0', '330931', '7.8792', '', 'Q\n']
    0 359
    1 1
    2 3
    3 " Miss. Mary McGovern"
    4 female
    5 
    6 0
    7 0
    8 330931
    9 7.8792
    10 
    11 Q
    
    ----------------------------
    ['360', '1', '3', '" Miss. Helen Mary ""Ellie"" Mockler"', 'female', '', '0', '0', '330980', '7.8792', '', 'Q\n']
    0 360
    1 1
    2 3
    3 " Miss. Helen Mary ""Ellie"" Mockler"
    4 female
    5 
    6 0
    7 0
    8 330980
    9 7.8792
    10 
    11 Q
    
    ----------------------------
    ['361', '0', '3', '" Mr. Wilhelm Skoog"', 'male', '40', '1', '4', '347088', '27.9', '', 'S\n']
    0 361
    1 0
    2 3
    3 " Mr. Wilhelm Skoog"
    4 male
    5 40
    6 1
    7 4
    8 347088
    9 27.9
    10 
    11 S
    
    ----------------------------
    ['362', '0', '2', '" Mr. Sebastiano del Carlo"', 'male', '29', '1', '0', 'SC/PARIS 2167', '27.7208', '', 'C\n']
    0 362
    1 0
    2 2
    3 " Mr. Sebastiano del Carlo"
    4 male
    5 29
    6 1
    7 0
    8 SC/PARIS 2167
    9 27.7208
    10 
    11 C
    
    ----------------------------
    ['363', '0', '3', '" Mrs. (Catherine David) Barbara"', 'female', '45', '0', '1', '2691', '14.4542', '', 'C\n']
    0 363
    1 0
    2 3
    3 " Mrs. (Catherine David) Barbara"
    4 female
    5 45
    6 0
    7 1
    8 2691
    9 14.4542
    10 
    11 C
    
    ----------------------------
    ['364', '0', '3', '" Mr. Adola Asim"', 'male', '35', '0', '0', 'SOTON/O.Q. 3101310', '7.05', '', 'S\n']
    0 364
    1 0
    2 3
    3 " Mr. Adola Asim"
    4 male
    5 35
    6 0
    7 0
    8 SOTON/O.Q. 3101310
    9 7.05
    10 
    11 S
    
    ----------------------------
    ['365', '0', '3', '" Mr. Thomas O\'Brien"', 'male', '', '1', '0', '370365', '15.5', '', 'Q\n']
    0 365
    1 0
    2 3
    3 " Mr. Thomas O'Brien"
    4 male
    5 
    6 1
    7 0
    8 370365
    9 15.5
    10 
    11 Q
    
    ----------------------------
    ['366', '0', '3', '" Mr. Mauritz Nils Martin Adahl"', 'male', '30', '0', '0', 'C 7076', '7.25', '', 'S\n']
    0 366
    1 0
    2 3
    3 " Mr. Mauritz Nils Martin Adahl"
    4 male
    5 30
    6 0
    7 0
    8 C 7076
    9 7.25
    10 
    11 S
    
    ----------------------------
    ['367', '1', '1', '" Mrs. Frank Manley (Anna Sophia Atkinson) Warren"', 'female', '60', '1', '0', '110813', '75.25', 'D37', 'C\n']
    0 367
    1 1
    2 1
    3 " Mrs. Frank Manley (Anna Sophia Atkinson) Warren"
    4 female
    5 60
    6 1
    7 0
    8 110813
    9 75.25
    10 D37
    11 C
    
    ----------------------------
    ['368', '1', '3', '" Mrs. (Mantoura Boulos) Moussa"', 'female', '', '0', '0', '2626', '7.2292', '', 'C\n']
    0 368
    1 1
    2 3
    3 " Mrs. (Mantoura Boulos) Moussa"
    4 female
    5 
    6 0
    7 0
    8 2626
    9 7.2292
    10 
    11 C
    
    ----------------------------
    ['369', '1', '3', '" Miss. Annie Jermyn"', 'female', '', '0', '0', '14313', '7.75', '', 'Q\n']
    0 369
    1 1
    2 3
    3 " Miss. Annie Jermyn"
    4 female
    5 
    6 0
    7 0
    8 14313
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['370', '1', '1', '" Mme. Leontine Pauline Aubart"', 'female', '24', '0', '0', 'PC 17477', '69.3', 'B35', 'C\n']
    0 370
    1 1
    2 1
    3 " Mme. Leontine Pauline Aubart"
    4 female
    5 24
    6 0
    7 0
    8 PC 17477
    9 69.3
    10 B35
    11 C
    
    ----------------------------
    ['371', '1', '1', '" Mr. George Achilles Harder"', 'male', '25', '1', '0', '11765', '55.4417', 'E50', 'C\n']
    0 371
    1 1
    2 1
    3 " Mr. George Achilles Harder"
    4 male
    5 25
    6 1
    7 0
    8 11765
    9 55.4417
    10 E50
    11 C
    
    ----------------------------
    ['372', '0', '3', '" Mr. Jakob Alfred Wiklund"', 'male', '18', '1', '0', '3101267', '6.4958', '', 'S\n']
    0 372
    1 0
    2 3
    3 " Mr. Jakob Alfred Wiklund"
    4 male
    5 18
    6 1
    7 0
    8 3101267
    9 6.4958
    10 
    11 S
    
    ----------------------------
    ['373', '0', '3', '" Mr. William Thomas Beavan"', 'male', '19', '0', '0', '323951', '8.05', '', 'S\n']
    0 373
    1 0
    2 3
    3 " Mr. William Thomas Beavan"
    4 male
    5 19
    6 0
    7 0
    8 323951
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['374', '0', '1', '" Mr. Sante Ringhini"', 'male', '22', '0', '0', 'PC 17760', '135.6333', '', 'C\n']
    0 374
    1 0
    2 1
    3 " Mr. Sante Ringhini"
    4 male
    5 22
    6 0
    7 0
    8 PC 17760
    9 135.6333
    10 
    11 C
    
    ----------------------------
    ['375', '0', '3', '" Miss. Stina Viola Palsson"', 'female', '3', '3', '1', '349909', '21.075', '', 'S\n']
    0 375
    1 0
    2 3
    3 " Miss. Stina Viola Palsson"
    4 female
    5 3
    6 3
    7 1
    8 349909
    9 21.075
    10 
    11 S
    
    ----------------------------
    ['376', '1', '1', '" Mrs. Edgar Joseph (Leila Saks) Meyer"', 'female', '', '1', '0', 'PC 17604', '82.1708', '', 'C\n']
    0 376
    1 1
    2 1
    3 " Mrs. Edgar Joseph (Leila Saks) Meyer"
    4 female
    5 
    6 1
    7 0
    8 PC 17604
    9 82.1708
    10 
    11 C
    
    ----------------------------
    ['377', '1', '3', '" Miss. Aurora Adelia Landergren"', 'female', '22', '0', '0', 'C 7077', '7.25', '', 'S\n']
    0 377
    1 1
    2 3
    3 " Miss. Aurora Adelia Landergren"
    4 female
    5 22
    6 0
    7 0
    8 C 7077
    9 7.25
    10 
    11 S
    
    ----------------------------
    ['378', '0', '1', '" Mr. Harry Elkins Widener"', 'male', '27', '0', '2', '113503', '211.5', 'C82', 'C\n']
    0 378
    1 0
    2 1
    3 " Mr. Harry Elkins Widener"
    4 male
    5 27
    6 0
    7 2
    8 113503
    9 211.5
    10 C82
    11 C
    
    ----------------------------
    ['379', '0', '3', '" Mr. Tannous Betros"', 'male', '20', '0', '0', '2648', '4.0125', '', 'C\n']
    0 379
    1 0
    2 3
    3 " Mr. Tannous Betros"
    4 male
    5 20
    6 0
    7 0
    8 2648
    9 4.0125
    10 
    11 C
    
    ----------------------------
    ['380', '0', '3', '" Mr. Karl Gideon Gustafsson"', 'male', '19', '0', '0', '347069', '7.775', '', 'S\n']
    0 380
    1 0
    2 3
    3 " Mr. Karl Gideon Gustafsson"
    4 male
    5 19
    6 0
    7 0
    8 347069
    9 7.775
    10 
    11 S
    
    ----------------------------
    ['381', '1', '1', '" Miss. Rosalie Bidois"', 'female', '42', '0', '0', 'PC 17757', '227.525', '', 'C\n']
    0 381
    1 1
    2 1
    3 " Miss. Rosalie Bidois"
    4 female
    5 42
    6 0
    7 0
    8 PC 17757
    9 227.525
    10 
    11 C
    
    ----------------------------
    ['382', '1', '3', '" Miss. Maria (""Mary"") Nakid"', 'female', '1', '0', '2', '2653', '15.7417', '', 'C\n']
    0 382
    1 1
    2 3
    3 " Miss. Maria (""Mary"") Nakid"
    4 female
    5 1
    6 0
    7 2
    8 2653
    9 15.7417
    10 
    11 C
    
    ----------------------------
    ['383', '0', '3', '" Mr. Juho Tikkanen"', 'male', '32', '0', '0', 'STON/O 2. 3101293', '7.925', '', 'S\n']
    0 383
    1 0
    2 3
    3 " Mr. Juho Tikkanen"
    4 male
    5 32
    6 0
    7 0
    8 STON/O 2. 3101293
    9 7.925
    10 
    11 S
    
    ----------------------------
    ['384', '1', '1', '" Mrs. Alexander Oskar (Mary Aline Towner) Holverson"', 'female', '35', '1', '0', '113789', '52', '', 'S\n']
    0 384
    1 1
    2 1
    3 " Mrs. Alexander Oskar (Mary Aline Towner) Holverson"
    4 female
    5 35
    6 1
    7 0
    8 113789
    9 52
    10 
    11 S
    
    ----------------------------
    ['385', '0', '3', '" Mr. Vasil Plotcharsky"', 'male', '', '0', '0', '349227', '7.8958', '', 'S\n']
    0 385
    1 0
    2 3
    3 " Mr. Vasil Plotcharsky"
    4 male
    5 
    6 0
    7 0
    8 349227
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['386', '0', '2', '" Mr. Charles Henry Davies"', 'male', '18', '0', '0', 'S.O.C. 14879', '73.5', '', 'S\n']
    0 386
    1 0
    2 2
    3 " Mr. Charles Henry Davies"
    4 male
    5 18
    6 0
    7 0
    8 S.O.C. 14879
    9 73.5
    10 
    11 S
    
    ----------------------------
    ['387', '0', '3', '" Master. Sidney Leonard Goodwin"', 'male', '1', '5', '2', 'CA 2144', '46.9', '', 'S\n']
    0 387
    1 0
    2 3
    3 " Master. Sidney Leonard Goodwin"
    4 male
    5 1
    6 5
    7 2
    8 CA 2144
    9 46.9
    10 
    11 S
    
    ----------------------------
    ['388', '1', '2', '" Miss. Kate Buss"', 'female', '36', '0', '0', '27849', '13', '', 'S\n']
    0 388
    1 1
    2 2
    3 " Miss. Kate Buss"
    4 female
    5 36
    6 0
    7 0
    8 27849
    9 13
    10 
    11 S
    
    ----------------------------
    ['389', '0', '3', '" Mr. Matthew Sadlier"', 'male', '', '0', '0', '367655', '7.7292', '', 'Q\n']
    0 389
    1 0
    2 3
    3 " Mr. Matthew Sadlier"
    4 male
    5 
    6 0
    7 0
    8 367655
    9 7.7292
    10 
    11 Q
    
    ----------------------------
    ['390', '1', '2', '" Miss. Bertha Lehmann"', 'female', '17', '0', '0', 'SC 1748', '12', '', 'C\n']
    0 390
    1 1
    2 2
    3 " Miss. Bertha Lehmann"
    4 female
    5 17
    6 0
    7 0
    8 SC 1748
    9 12
    10 
    11 C
    
    ----------------------------
    ['391', '1', '1', '" Mr. William Ernest Carter"', 'male', '36', '1', '2', '113760', '120', 'B96 B98', 'S\n']
    0 391
    1 1
    2 1
    3 " Mr. William Ernest Carter"
    4 male
    5 36
    6 1
    7 2
    8 113760
    9 120
    10 B96 B98
    11 S
    
    ----------------------------
    ['392', '1', '3', '" Mr. Carl Olof Jansson"', 'male', '21', '0', '0', '350034', '7.7958', '', 'S\n']
    0 392
    1 1
    2 3
    3 " Mr. Carl Olof Jansson"
    4 male
    5 21
    6 0
    7 0
    8 350034
    9 7.7958
    10 
    11 S
    
    ----------------------------
    ['393', '0', '3', '" Mr. Johan Birger Gustafsson"', 'male', '28', '2', '0', '3101277', '7.925', '', 'S\n']
    0 393
    1 0
    2 3
    3 " Mr. Johan Birger Gustafsson"
    4 male
    5 28
    6 2
    7 0
    8 3101277
    9 7.925
    10 
    11 S
    
    ----------------------------
    ['394', '1', '1', '" Miss. Marjorie Newell"', 'female', '23', '1', '0', '35273', '113.275', 'D36', 'C\n']
    0 394
    1 1
    2 1
    3 " Miss. Marjorie Newell"
    4 female
    5 23
    6 1
    7 0
    8 35273
    9 113.275
    10 D36
    11 C
    
    ----------------------------
    ['395', '1', '3', '" Mrs. Hjalmar (Agnes Charlotta Bengtsson) Sandstrom"', 'female', '24', '0', '2', 'PP 9549', '16.7', 'G6', 'S\n']
    0 395
    1 1
    2 3
    3 " Mrs. Hjalmar (Agnes Charlotta Bengtsson) Sandstrom"
    4 female
    5 24
    6 0
    7 2
    8 PP 9549
    9 16.7
    10 G6
    11 S
    
    ----------------------------
    ['396', '0', '3', '" Mr. Erik Johansson"', 'male', '22', '0', '0', '350052', '7.7958', '', 'S\n']
    0 396
    1 0
    2 3
    3 " Mr. Erik Johansson"
    4 male
    5 22
    6 0
    7 0
    8 350052
    9 7.7958
    10 
    11 S
    
    ----------------------------
    ['397', '0', '3', '" Miss. Elina Olsson"', 'female', '31', '0', '0', '350407', '7.8542', '', 'S\n']
    0 397
    1 0
    2 3
    3 " Miss. Elina Olsson"
    4 female
    5 31
    6 0
    7 0
    8 350407
    9 7.8542
    10 
    11 S
    
    ----------------------------
    ['398', '0', '2', '" Mr. Peter David McKane"', 'male', '46', '0', '0', '28403', '26', '', 'S\n']
    0 398
    1 0
    2 2
    3 " Mr. Peter David McKane"
    4 male
    5 46
    6 0
    7 0
    8 28403
    9 26
    10 
    11 S
    
    ----------------------------
    ['399', '0', '2', '" Dr. Alfred Pain"', 'male', '23', '0', '0', '244278', '10.5', '', 'S\n']
    0 399
    1 0
    2 2
    3 " Dr. Alfred Pain"
    4 male
    5 23
    6 0
    7 0
    8 244278
    9 10.5
    10 
    11 S
    
    ----------------------------
    ['400', '1', '2', '" Mrs. William H (Jessie L) Trout"', 'female', '28', '0', '0', '240929', '12.65', '', 'S\n']
    0 400
    1 1
    2 2
    3 " Mrs. William H (Jessie L) Trout"
    4 female
    5 28
    6 0
    7 0
    8 240929
    9 12.65
    10 
    11 S
    
    ----------------------------
    ['401', '1', '3', '" Mr. Juha Niskanen"', 'male', '39', '0', '0', 'STON/O 2. 3101289', '7.925', '', 'S\n']
    0 401
    1 1
    2 3
    3 " Mr. Juha Niskanen"
    4 male
    5 39
    6 0
    7 0
    8 STON/O 2. 3101289
    9 7.925
    10 
    11 S
    
    ----------------------------
    ['402', '0', '3', '" Mr. John Adams"', 'male', '26', '0', '0', '341826', '8.05', '', 'S\n']
    0 402
    1 0
    2 3
    3 " Mr. John Adams"
    4 male
    5 26
    6 0
    7 0
    8 341826
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['403', '0', '3', '" Miss. Mari Aina Jussila"', 'female', '21', '1', '0', '4137', '9.825', '', 'S\n']
    0 403
    1 0
    2 3
    3 " Miss. Mari Aina Jussila"
    4 female
    5 21
    6 1
    7 0
    8 4137
    9 9.825
    10 
    11 S
    
    ----------------------------
    ['404', '0', '3', '" Mr. Pekka Pietari Hakkarainen"', 'male', '28', '1', '0', 'STON/O2. 3101279', '15.85', '', 'S\n']
    0 404
    1 0
    2 3
    3 " Mr. Pekka Pietari Hakkarainen"
    4 male
    5 28
    6 1
    7 0
    8 STON/O2. 3101279
    9 15.85
    10 
    11 S
    
    ----------------------------
    ['405', '0', '3', '" Miss. Marija Oreskovic"', 'female', '20', '0', '0', '315096', '8.6625', '', 'S\n']
    0 405
    1 0
    2 3
    3 " Miss. Marija Oreskovic"
    4 female
    5 20
    6 0
    7 0
    8 315096
    9 8.6625
    10 
    11 S
    
    ----------------------------
    ['406', '0', '2', '" Mr. Shadrach Gale"', 'male', '34', '1', '0', '28664', '21', '', 'S\n']
    0 406
    1 0
    2 2
    3 " Mr. Shadrach Gale"
    4 male
    5 34
    6 1
    7 0
    8 28664
    9 21
    10 
    11 S
    
    ----------------------------
    ['407', '0', '3', '" Mr. Carl/Charles Peter Widegren"', 'male', '51', '0', '0', '347064', '7.75', '', 'S\n']
    0 407
    1 0
    2 3
    3 " Mr. Carl/Charles Peter Widegren"
    4 male
    5 51
    6 0
    7 0
    8 347064
    9 7.75
    10 
    11 S
    
    ----------------------------
    ['408', '1', '2', '" Master. William Rowe Richards"', 'male', '3', '1', '1', '29106', '18.75', '', 'S\n']
    0 408
    1 1
    2 2
    3 " Master. William Rowe Richards"
    4 male
    5 3
    6 1
    7 1
    8 29106
    9 18.75
    10 
    11 S
    
    ----------------------------
    ['409', '0', '3', '" Mr. Hans Martin Monsen Birkeland"', 'male', '21', '0', '0', '312992', '7.775', '', 'S\n']
    0 409
    1 0
    2 3
    3 " Mr. Hans Martin Monsen Birkeland"
    4 male
    5 21
    6 0
    7 0
    8 312992
    9 7.775
    10 
    11 S
    
    ----------------------------
    ['410', '0', '3', '" Miss. Ida Lefebre"', 'female', '', '3', '1', '4133', '25.4667', '', 'S\n']
    0 410
    1 0
    2 3
    3 " Miss. Ida Lefebre"
    4 female
    5 
    6 3
    7 1
    8 4133
    9 25.4667
    10 
    11 S
    
    ----------------------------
    ['411', '0', '3', '" Mr. Todor Sdycoff"', 'male', '', '0', '0', '349222', '7.8958', '', 'S\n']
    0 411
    1 0
    2 3
    3 " Mr. Todor Sdycoff"
    4 male
    5 
    6 0
    7 0
    8 349222
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['412', '0', '3', '" Mr. Henry Hart"', 'male', '', '0', '0', '394140', '6.8583', '', 'Q\n']
    0 412
    1 0
    2 3
    3 " Mr. Henry Hart"
    4 male
    5 
    6 0
    7 0
    8 394140
    9 6.8583
    10 
    11 Q
    
    ----------------------------
    ['413', '1', '1', '" Miss. Daisy E Minahan"', 'female', '33', '1', '0', '19928', '90', 'C78', 'Q\n']
    0 413
    1 1
    2 1
    3 " Miss. Daisy E Minahan"
    4 female
    5 33
    6 1
    7 0
    8 19928
    9 90
    10 C78
    11 Q
    
    ----------------------------
    ['414', '0', '2', '" Mr. Alfred Fleming Cunningham"', 'male', '', '0', '0', '239853', '0', '', 'S\n']
    0 414
    1 0
    2 2
    3 " Mr. Alfred Fleming Cunningham"
    4 male
    5 
    6 0
    7 0
    8 239853
    9 0
    10 
    11 S
    
    ----------------------------
    ['415', '1', '3', '" Mr. Johan Julian Sundman"', 'male', '44', '0', '0', 'STON/O 2. 3101269', '7.925', '', 'S\n']
    0 415
    1 1
    2 3
    3 " Mr. Johan Julian Sundman"
    4 male
    5 44
    6 0
    7 0
    8 STON/O 2. 3101269
    9 7.925
    10 
    11 S
    
    ----------------------------
    ['416', '0', '3', '" Mrs. Thomas (Annie Louise Rowley) Meek"', 'female', '', '0', '0', '343095', '8.05', '', 'S\n']
    0 416
    1 0
    2 3
    3 " Mrs. Thomas (Annie Louise Rowley) Meek"
    4 female
    5 
    6 0
    7 0
    8 343095
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['417', '1', '2', '" Mrs. James Vivian (Lulu Thorne Christian) Drew"', 'female', '34', '1', '1', '28220', '32.5', '', 'S\n']
    0 417
    1 1
    2 2
    3 " Mrs. James Vivian (Lulu Thorne Christian) Drew"
    4 female
    5 34
    6 1
    7 1
    8 28220
    9 32.5
    10 
    11 S
    
    ----------------------------
    ['418', '1', '2', '" Miss. Lyyli Karoliina Silven"', 'female', '18', '0', '2', '250652', '13', '', 'S\n']
    0 418
    1 1
    2 2
    3 " Miss. Lyyli Karoliina Silven"
    4 female
    5 18
    6 0
    7 2
    8 250652
    9 13
    10 
    11 S
    
    ----------------------------
    ['419', '0', '2', '" Mr. William John Matthews"', 'male', '30', '0', '0', '28228', '13', '', 'S\n']
    0 419
    1 0
    2 2
    3 " Mr. William John Matthews"
    4 male
    5 30
    6 0
    7 0
    8 28228
    9 13
    10 
    11 S
    
    ----------------------------
    ['420', '0', '3', '" Miss. Catharina Van Impe"', 'female', '10', '0', '2', '345773', '24.15', '', 'S\n']
    0 420
    1 0
    2 3
    3 " Miss. Catharina Van Impe"
    4 female
    5 10
    6 0
    7 2
    8 345773
    9 24.15
    10 
    11 S
    
    ----------------------------
    ['421', '0', '3', '" Mr. Stanio Gheorgheff"', 'male', '', '0', '0', '349254', '7.8958', '', 'C\n']
    0 421
    1 0
    2 3
    3 " Mr. Stanio Gheorgheff"
    4 male
    5 
    6 0
    7 0
    8 349254
    9 7.8958
    10 
    11 C
    
    ----------------------------
    ['422', '0', '3', '" Mr. David Charters"', 'male', '21', '0', '0', 'A/5. 13032', '7.7333', '', 'Q\n']
    0 422
    1 0
    2 3
    3 " Mr. David Charters"
    4 male
    5 21
    6 0
    7 0
    8 A/5. 13032
    9 7.7333
    10 
    11 Q
    
    ----------------------------
    ['423', '0', '3', '" Mr. Leo Zimmerman"', 'male', '29', '0', '0', '315082', '7.875', '', 'S\n']
    0 423
    1 0
    2 3
    3 " Mr. Leo Zimmerman"
    4 male
    5 29
    6 0
    7 0
    8 315082
    9 7.875
    10 
    11 S
    
    ----------------------------
    ['424', '0', '3', '" Mrs. Ernst Gilbert (Anna Sigrid Maria Brogren) Danbom"', 'female', '28', '1', '1', '347080', '14.4', '', 'S\n']
    0 424
    1 0
    2 3
    3 " Mrs. Ernst Gilbert (Anna Sigrid Maria Brogren) Danbom"
    4 female
    5 28
    6 1
    7 1
    8 347080
    9 14.4
    10 
    11 S
    
    ----------------------------
    ['425', '0', '3', '" Mr. Viktor Richard Rosblom"', 'male', '18', '1', '1', '370129', '20.2125', '', 'S\n']
    0 425
    1 0
    2 3
    3 " Mr. Viktor Richard Rosblom"
    4 male
    5 18
    6 1
    7 1
    8 370129
    9 20.2125
    10 
    11 S
    
    ----------------------------
    ['426', '0', '3', '" Mr. Phillippe Wiseman"', 'male', '', '0', '0', 'A/4. 34244', '7.25', '', 'S\n']
    0 426
    1 0
    2 3
    3 " Mr. Phillippe Wiseman"
    4 male
    5 
    6 0
    7 0
    8 A/4. 34244
    9 7.25
    10 
    11 S
    
    ----------------------------
    ['427', '1', '2', '" Mrs. Charles V (Ada Maria Winfield) Clarke"', 'female', '28', '1', '0', '2003', '26', '', 'S\n']
    0 427
    1 1
    2 2
    3 " Mrs. Charles V (Ada Maria Winfield) Clarke"
    4 female
    5 28
    6 1
    7 0
    8 2003
    9 26
    10 
    11 S
    
    ----------------------------
    ['428', '1', '2', '" Miss. Kate Florence (""Mrs Kate Louise Phillips Marshall"") Phillips"', 'female', '19', '0', '0', '250655', '26', '', 'S\n']
    0 428
    1 1
    2 2
    3 " Miss. Kate Florence (""Mrs Kate Louise Phillips Marshall"") Phillips"
    4 female
    5 19
    6 0
    7 0
    8 250655
    9 26
    10 
    11 S
    
    ----------------------------
    ['429', '0', '3', '" Mr. James Flynn"', 'male', '', '0', '0', '364851', '7.75', '', 'Q\n']
    0 429
    1 0
    2 3
    3 " Mr. James Flynn"
    4 male
    5 
    6 0
    7 0
    8 364851
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['430', '1', '3', '" Mr. Berk (Berk Trembisky) Pickard"', 'male', '32', '0', '0', 'SOTON/O.Q. 392078', '8.05', 'E10', 'S\n']
    0 430
    1 1
    2 3
    3 " Mr. Berk (Berk Trembisky) Pickard"
    4 male
    5 32
    6 0
    7 0
    8 SOTON/O.Q. 392078
    9 8.05
    10 E10
    11 S
    
    ----------------------------
    ['431', '1', '1', '" Mr. Mauritz Hakan Bjornstrom-Steffansson"', 'male', '28', '0', '0', '110564', '26.55', 'C52', 'S\n']
    0 431
    1 1
    2 1
    3 " Mr. Mauritz Hakan Bjornstrom-Steffansson"
    4 male
    5 28
    6 0
    7 0
    8 110564
    9 26.55
    10 C52
    11 S
    
    ----------------------------
    ['432', '1', '3', '" Mrs. Percival (Florence Kate White) Thorneycroft"', 'female', '', '1', '0', '376564', '16.1', '', 'S\n']
    0 432
    1 1
    2 3
    3 " Mrs. Percival (Florence Kate White) Thorneycroft"
    4 female
    5 
    6 1
    7 0
    8 376564
    9 16.1
    10 
    11 S
    
    ----------------------------
    ['433', '1', '2', '" Mrs. Charles Alexander (Alice Adelaide Slow) Louch"', 'female', '42', '1', '0', 'SC/AH 3085', '26', '', 'S\n']
    0 433
    1 1
    2 2
    3 " Mrs. Charles Alexander (Alice Adelaide Slow) Louch"
    4 female
    5 42
    6 1
    7 0
    8 SC/AH 3085
    9 26
    10 
    11 S
    
    ----------------------------
    ['434', '0', '3', '" Mr. Nikolai Erland Kallio"', 'male', '17', '0', '0', 'STON/O 2. 3101274', '7.125', '', 'S\n']
    0 434
    1 0
    2 3
    3 " Mr. Nikolai Erland Kallio"
    4 male
    5 17
    6 0
    7 0
    8 STON/O 2. 3101274
    9 7.125
    10 
    11 S
    
    ----------------------------
    ['435', '0', '1', '" Mr. William Baird Silvey"', 'male', '50', '1', '0', '13507', '55.9', 'E44', 'S\n']
    0 435
    1 0
    2 1
    3 " Mr. William Baird Silvey"
    4 male
    5 50
    6 1
    7 0
    8 13507
    9 55.9
    10 E44
    11 S
    
    ----------------------------
    ['436', '1', '1', '" Miss. Lucile Polk Carter"', 'female', '14', '1', '2', '113760', '120', 'B96 B98', 'S\n']
    0 436
    1 1
    2 1
    3 " Miss. Lucile Polk Carter"
    4 female
    5 14
    6 1
    7 2
    8 113760
    9 120
    10 B96 B98
    11 S
    
    ----------------------------
    ['437', '0', '3', '" Miss. Doolina Margaret ""Daisy"" Ford"', 'female', '21', '2', '2', 'W./C. 6608', '34.375', '', 'S\n']
    0 437
    1 0
    2 3
    3 " Miss. Doolina Margaret ""Daisy"" Ford"
    4 female
    5 21
    6 2
    7 2
    8 W./C. 6608
    9 34.375
    10 
    11 S
    
    ----------------------------
    ['438', '1', '2', '" Mrs. Sidney (Emily Hocking) Richards"', 'female', '24', '2', '3', '29106', '18.75', '', 'S\n']
    0 438
    1 1
    2 2
    3 " Mrs. Sidney (Emily Hocking) Richards"
    4 female
    5 24
    6 2
    7 3
    8 29106
    9 18.75
    10 
    11 S
    
    ----------------------------
    ['439', '0', '1', '" Mr. Mark Fortune"', 'male', '64', '1', '4', '19950', '263', 'C23 C25 C27', 'S\n']
    0 439
    1 0
    2 1
    3 " Mr. Mark Fortune"
    4 male
    5 64
    6 1
    7 4
    8 19950
    9 263
    10 C23 C25 C27
    11 S
    
    ----------------------------
    ['440', '0', '2', '" Mr. Johan Henrik Johannesson Kvillner"', 'male', '31', '0', '0', 'C.A. 18723', '10.5', '', 'S\n']
    0 440
    1 0
    2 2
    3 " Mr. Johan Henrik Johannesson Kvillner"
    4 male
    5 31
    6 0
    7 0
    8 C.A. 18723
    9 10.5
    10 
    11 S
    
    ----------------------------
    ['441', '1', '2', '" Mrs. Benjamin (Esther Ada Bloomfield) Hart"', 'female', '45', '1', '1', 'F.C.C. 13529', '26.25', '', 'S\n']
    0 441
    1 1
    2 2
    3 " Mrs. Benjamin (Esther Ada Bloomfield) Hart"
    4 female
    5 45
    6 1
    7 1
    8 F.C.C. 13529
    9 26.25
    10 
    11 S
    
    ----------------------------
    ['442', '0', '3', '" Mr. Leon Hampe"', 'male', '20', '0', '0', '345769', '9.5', '', 'S\n']
    0 442
    1 0
    2 3
    3 " Mr. Leon Hampe"
    4 male
    5 20
    6 0
    7 0
    8 345769
    9 9.5
    10 
    11 S
    
    ----------------------------
    ['443', '0', '3', '" Mr. Johan Emil Petterson"', 'male', '25', '1', '0', '347076', '7.775', '', 'S\n']
    0 443
    1 0
    2 3
    3 " Mr. Johan Emil Petterson"
    4 male
    5 25
    6 1
    7 0
    8 347076
    9 7.775
    10 
    11 S
    
    ----------------------------
    ['444', '1', '2', '" Ms. Encarnacion Reynaldo"', 'female', '28', '0', '0', '230434', '13', '', 'S\n']
    0 444
    1 1
    2 2
    3 " Ms. Encarnacion Reynaldo"
    4 female
    5 28
    6 0
    7 0
    8 230434
    9 13
    10 
    11 S
    
    ----------------------------
    ['445', '1', '3', '" Mr. Bernt Johannesen-Bratthammer"', 'male', '', '0', '0', '65306', '8.1125', '', 'S\n']
    0 445
    1 1
    2 3
    3 " Mr. Bernt Johannesen-Bratthammer"
    4 male
    5 
    6 0
    7 0
    8 65306
    9 8.1125
    10 
    11 S
    
    ----------------------------
    ['446', '1', '1', '" Master. Washington Dodge"', 'male', '4', '0', '2', '33638', '81.8583', 'A34', 'S\n']
    0 446
    1 1
    2 1
    3 " Master. Washington Dodge"
    4 male
    5 4
    6 0
    7 2
    8 33638
    9 81.8583
    10 A34
    11 S
    
    ----------------------------
    ['447', '1', '2', '" Miss. Madeleine Violet Mellinger"', 'female', '13', '0', '1', '250644', '19.5', '', 'S\n']
    0 447
    1 1
    2 2
    3 " Miss. Madeleine Violet Mellinger"
    4 female
    5 13
    6 0
    7 1
    8 250644
    9 19.5
    10 
    11 S
    
    ----------------------------
    ['448', '1', '1', '" Mr. Frederic Kimber Seward"', 'male', '34', '0', '0', '113794', '26.55', '', 'S\n']
    0 448
    1 1
    2 1
    3 " Mr. Frederic Kimber Seward"
    4 male
    5 34
    6 0
    7 0
    8 113794
    9 26.55
    10 
    11 S
    
    ----------------------------
    ['449', '1', '3', '" Miss. Marie Catherine Baclini"', 'female', '5', '2', '1', '2666', '19.2583', '', 'C\n']
    0 449
    1 1
    2 3
    3 " Miss. Marie Catherine Baclini"
    4 female
    5 5
    6 2
    7 1
    8 2666
    9 19.2583
    10 
    11 C
    
    ----------------------------
    ['450', '1', '1', '" Major. Arthur Godfrey Peuchen"', 'male', '52', '0', '0', '113786', '30.5', 'C104', 'S\n']
    0 450
    1 1
    2 1
    3 " Major. Arthur Godfrey Peuchen"
    4 male
    5 52
    6 0
    7 0
    8 113786
    9 30.5
    10 C104
    11 S
    
    ----------------------------
    ['451', '0', '2', '" Mr. Edwy Arthur West"', 'male', '36', '1', '2', 'C.A. 34651', '27.75', '', 'S\n']
    0 451
    1 0
    2 2
    3 " Mr. Edwy Arthur West"
    4 male
    5 36
    6 1
    7 2
    8 C.A. 34651
    9 27.75
    10 
    11 S
    
    ----------------------------
    ['452', '0', '3', '" Mr. Ingvald Olai Olsen Hagland"', 'male', '', '1', '0', '65303', '19.9667', '', 'S\n']
    0 452
    1 0
    2 3
    3 " Mr. Ingvald Olai Olsen Hagland"
    4 male
    5 
    6 1
    7 0
    8 65303
    9 19.9667
    10 
    11 S
    
    ----------------------------
    ['453', '0', '1', '" Mr. Benjamin Laventall Foreman"', 'male', '30', '0', '0', '113051', '27.75', 'C111', 'C\n']
    0 453
    1 0
    2 1
    3 " Mr. Benjamin Laventall Foreman"
    4 male
    5 30
    6 0
    7 0
    8 113051
    9 27.75
    10 C111
    11 C
    
    ----------------------------
    ['454', '1', '1', '" Mr. Samuel L Goldenberg"', 'male', '49', '1', '0', '17453', '89.1042', 'C92', 'C\n']
    0 454
    1 1
    2 1
    3 " Mr. Samuel L Goldenberg"
    4 male
    5 49
    6 1
    7 0
    8 17453
    9 89.1042
    10 C92
    11 C
    
    ----------------------------
    ['455', '0', '3', '" Mr. Joseph Peduzzi"', 'male', '', '0', '0', 'A/5 2817', '8.05', '', 'S\n']
    0 455
    1 0
    2 3
    3 " Mr. Joseph Peduzzi"
    4 male
    5 
    6 0
    7 0
    8 A/5 2817
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['456', '1', '3', '" Mr. Ivan Jalsevac"', 'male', '29', '0', '0', '349240', '7.8958', '', 'C\n']
    0 456
    1 1
    2 3
    3 " Mr. Ivan Jalsevac"
    4 male
    5 29
    6 0
    7 0
    8 349240
    9 7.8958
    10 
    11 C
    
    ----------------------------
    ['457', '0', '1', '" Mr. Francis Davis Millet"', 'male', '65', '0', '0', '13509', '26.55', 'E38', 'S\n']
    0 457
    1 0
    2 1
    3 " Mr. Francis Davis Millet"
    4 male
    5 65
    6 0
    7 0
    8 13509
    9 26.55
    10 E38
    11 S
    
    ----------------------------
    ['458', '1', '1', '" Mrs. Frederick R (Marion) Kenyon"', 'female', '', '1', '0', '17464', '51.8625', 'D21', 'S\n']
    0 458
    1 1
    2 1
    3 " Mrs. Frederick R (Marion) Kenyon"
    4 female
    5 
    6 1
    7 0
    8 17464
    9 51.8625
    10 D21
    11 S
    
    ----------------------------
    ['459', '1', '2', '" Miss. Ellen Toomey"', 'female', '50', '0', '0', 'F.C.C. 13531', '10.5', '', 'S\n']
    0 459
    1 1
    2 2
    3 " Miss. Ellen Toomey"
    4 female
    5 50
    6 0
    7 0
    8 F.C.C. 13531
    9 10.5
    10 
    11 S
    
    ----------------------------
    ['460', '0', '3', '" Mr. Maurice O\'Connor"', 'male', '', '0', '0', '371060', '7.75', '', 'Q\n']
    0 460
    1 0
    2 3
    3 " Mr. Maurice O'Connor"
    4 male
    5 
    6 0
    7 0
    8 371060
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['461', '1', '1', '" Mr. Harry Anderson"', 'male', '48', '0', '0', '19952', '26.55', 'E12', 'S\n']
    0 461
    1 1
    2 1
    3 " Mr. Harry Anderson"
    4 male
    5 48
    6 0
    7 0
    8 19952
    9 26.55
    10 E12
    11 S
    
    ----------------------------
    ['462', '0', '3', '" Mr. William Morley"', 'male', '34', '0', '0', '364506', '8.05', '', 'S\n']
    0 462
    1 0
    2 3
    3 " Mr. William Morley"
    4 male
    5 34
    6 0
    7 0
    8 364506
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['463', '0', '1', '" Mr. Arthur H Gee"', 'male', '47', '0', '0', '111320', '38.5', 'E63', 'S\n']
    0 463
    1 0
    2 1
    3 " Mr. Arthur H Gee"
    4 male
    5 47
    6 0
    7 0
    8 111320
    9 38.5
    10 E63
    11 S
    
    ----------------------------
    ['464', '0', '2', '" Mr. Jacob Christian Milling"', 'male', '48', '0', '0', '234360', '13', '', 'S\n']
    0 464
    1 0
    2 2
    3 " Mr. Jacob Christian Milling"
    4 male
    5 48
    6 0
    7 0
    8 234360
    9 13
    10 
    11 S
    
    ----------------------------
    ['465', '0', '3', '" Mr. Simon Maisner"', 'male', '', '0', '0', 'A/S 2816', '8.05', '', 'S\n']
    0 465
    1 0
    2 3
    3 " Mr. Simon Maisner"
    4 male
    5 
    6 0
    7 0
    8 A/S 2816
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['466', '0', '3', '" Mr. Manuel Estanslas Goncalves"', 'male', '38', '0', '0', 'SOTON/O.Q. 3101306', '7.05', '', 'S\n']
    0 466
    1 0
    2 3
    3 " Mr. Manuel Estanslas Goncalves"
    4 male
    5 38
    6 0
    7 0
    8 SOTON/O.Q. 3101306
    9 7.05
    10 
    11 S
    
    ----------------------------
    ['467', '0', '2', '" Mr. William Campbell"', 'male', '', '0', '0', '239853', '0', '', 'S\n']
    0 467
    1 0
    2 2
    3 " Mr. William Campbell"
    4 male
    5 
    6 0
    7 0
    8 239853
    9 0
    10 
    11 S
    
    ----------------------------
    ['468', '0', '1', '" Mr. John Montgomery Smart"', 'male', '56', '0', '0', '113792', '26.55', '', 'S\n']
    0 468
    1 0
    2 1
    3 " Mr. John Montgomery Smart"
    4 male
    5 56
    6 0
    7 0
    8 113792
    9 26.55
    10 
    11 S
    
    ----------------------------
    ['469', '0', '3', '" Mr. James Scanlan"', 'male', '', '0', '0', '36209', '7.725', '', 'Q\n']
    0 469
    1 0
    2 3
    3 " Mr. James Scanlan"
    4 male
    5 
    6 0
    7 0
    8 36209
    9 7.725
    10 
    11 Q
    
    ----------------------------
    ['470', '1', '3', '" Miss. Helene Barbara Baclini"', 'female', '0.75', '2', '1', '2666', '19.2583', '', 'C\n']
    0 470
    1 1
    2 3
    3 " Miss. Helene Barbara Baclini"
    4 female
    5 0.75
    6 2
    7 1
    8 2666
    9 19.2583
    10 
    11 C
    
    ----------------------------
    ['471', '0', '3', '" Mr. Arthur Keefe"', 'male', '', '0', '0', '323592', '7.25', '', 'S\n']
    0 471
    1 0
    2 3
    3 " Mr. Arthur Keefe"
    4 male
    5 
    6 0
    7 0
    8 323592
    9 7.25
    10 
    11 S
    
    ----------------------------
    ['472', '0', '3', '" Mr. Luka Cacic"', 'male', '38', '0', '0', '315089', '8.6625', '', 'S\n']
    0 472
    1 0
    2 3
    3 " Mr. Luka Cacic"
    4 male
    5 38
    6 0
    7 0
    8 315089
    9 8.6625
    10 
    11 S
    
    ----------------------------
    ['473', '1', '2', '" Mrs. Edwy Arthur (Ada Mary Worth) West"', 'female', '33', '1', '2', 'C.A. 34651', '27.75', '', 'S\n']
    0 473
    1 1
    2 2
    3 " Mrs. Edwy Arthur (Ada Mary Worth) West"
    4 female
    5 33
    6 1
    7 2
    8 C.A. 34651
    9 27.75
    10 
    11 S
    
    ----------------------------
    ['474', '1', '2', '" Mrs. Amin S (Marie Marthe Thuillard) Jerwan"', 'female', '23', '0', '0', 'SC/AH Basle 541', '13.7917', 'D', 'C\n']
    0 474
    1 1
    2 2
    3 " Mrs. Amin S (Marie Marthe Thuillard) Jerwan"
    4 female
    5 23
    6 0
    7 0
    8 SC/AH Basle 541
    9 13.7917
    10 D
    11 C
    
    ----------------------------
    ['475', '0', '3', '" Miss. Ida Sofia Strandberg"', 'female', '22', '0', '0', '7553', '9.8375', '', 'S\n']
    0 475
    1 0
    2 3
    3 " Miss. Ida Sofia Strandberg"
    4 female
    5 22
    6 0
    7 0
    8 7553
    9 9.8375
    10 
    11 S
    
    ----------------------------
    ['476', '0', '1', '" Mr. George Quincy Clifford"', 'male', '', '0', '0', '110465', '52', 'A14', 'S\n']
    0 476
    1 0
    2 1
    3 " Mr. George Quincy Clifford"
    4 male
    5 
    6 0
    7 0
    8 110465
    9 52
    10 A14
    11 S
    
    ----------------------------
    ['477', '0', '2', '" Mr. Peter Henry Renouf"', 'male', '34', '1', '0', '31027', '21', '', 'S\n']
    0 477
    1 0
    2 2
    3 " Mr. Peter Henry Renouf"
    4 male
    5 34
    6 1
    7 0
    8 31027
    9 21
    10 
    11 S
    
    ----------------------------
    ['478', '0', '3', '" Mr. Lewis Richard Braund"', 'male', '29', '1', '0', '3460', '7.0458', '', 'S\n']
    0 478
    1 0
    2 3
    3 " Mr. Lewis Richard Braund"
    4 male
    5 29
    6 1
    7 0
    8 3460
    9 7.0458
    10 
    11 S
    
    ----------------------------
    ['479', '0', '3', '" Mr. Nils August Karlsson"', 'male', '22', '0', '0', '350060', '7.5208', '', 'S\n']
    0 479
    1 0
    2 3
    3 " Mr. Nils August Karlsson"
    4 male
    5 22
    6 0
    7 0
    8 350060
    9 7.5208
    10 
    11 S
    
    ----------------------------
    ['480', '1', '3', '" Miss. Hildur E Hirvonen"', 'female', '2', '0', '1', '3101298', '12.2875', '', 'S\n']
    0 480
    1 1
    2 3
    3 " Miss. Hildur E Hirvonen"
    4 female
    5 2
    6 0
    7 1
    8 3101298
    9 12.2875
    10 
    11 S
    
    ----------------------------
    ['481', '0', '3', '" Master. Harold Victor Goodwin"', 'male', '9', '5', '2', 'CA 2144', '46.9', '', 'S\n']
    0 481
    1 0
    2 3
    3 " Master. Harold Victor Goodwin"
    4 male
    5 9
    6 5
    7 2
    8 CA 2144
    9 46.9
    10 
    11 S
    
    ----------------------------
    ['482', '0', '2', '" Mr. Anthony Wood ""Archie"" Frost"', 'male', '', '0', '0', '239854', '0', '', 'S\n']
    0 482
    1 0
    2 2
    3 " Mr. Anthony Wood ""Archie"" Frost"
    4 male
    5 
    6 0
    7 0
    8 239854
    9 0
    10 
    11 S
    
    ----------------------------
    ['483', '0', '3', '" Mr. Richard Henry Rouse"', 'male', '50', '0', '0', 'A/5 3594', '8.05', '', 'S\n']
    0 483
    1 0
    2 3
    3 " Mr. Richard Henry Rouse"
    4 male
    5 50
    6 0
    7 0
    8 A/5 3594
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['484', '1', '3', '" Mrs. (Hedwig) Turkula"', 'female', '63', '0', '0', '4134', '9.5875', '', 'S\n']
    0 484
    1 1
    2 3
    3 " Mrs. (Hedwig) Turkula"
    4 female
    5 63
    6 0
    7 0
    8 4134
    9 9.5875
    10 
    11 S
    
    ----------------------------
    ['485', '1', '1', '" Mr. Dickinson H Bishop"', 'male', '25', '1', '0', '11967', '91.0792', 'B49', 'C\n']
    0 485
    1 1
    2 1
    3 " Mr. Dickinson H Bishop"
    4 male
    5 25
    6 1
    7 0
    8 11967
    9 91.0792
    10 B49
    11 C
    
    ----------------------------
    ['486', '0', '3', '" Miss. Jeannie Lefebre"', 'female', '', '3', '1', '4133', '25.4667', '', 'S\n']
    0 486
    1 0
    2 3
    3 " Miss. Jeannie Lefebre"
    4 female
    5 
    6 3
    7 1
    8 4133
    9 25.4667
    10 
    11 S
    
    ----------------------------
    ['487', '1', '1', '" Mrs. Frederick Maxfield (Jane Anne Forby) Hoyt"', 'female', '35', '1', '0', '19943', '90', 'C93', 'S\n']
    0 487
    1 1
    2 1
    3 " Mrs. Frederick Maxfield (Jane Anne Forby) Hoyt"
    4 female
    5 35
    6 1
    7 0
    8 19943
    9 90
    10 C93
    11 S
    
    ----------------------------
    ['488', '0', '1', '" Mr. Edward Austin Kent"', 'male', '58', '0', '0', '11771', '29.7', 'B37', 'C\n']
    0 488
    1 0
    2 1
    3 " Mr. Edward Austin Kent"
    4 male
    5 58
    6 0
    7 0
    8 11771
    9 29.7
    10 B37
    11 C
    
    ----------------------------
    ['489', '0', '3', '" Mr. Francis William Somerton"', 'male', '30', '0', '0', 'A.5. 18509', '8.05', '', 'S\n']
    0 489
    1 0
    2 3
    3 " Mr. Francis William Somerton"
    4 male
    5 30
    6 0
    7 0
    8 A.5. 18509
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['490', '1', '3', '" Master. Eden Leslie ""Neville"" Coutts"', 'male', '9', '1', '1', 'C.A. 37671', '15.9', '', 'S\n']
    0 490
    1 1
    2 3
    3 " Master. Eden Leslie ""Neville"" Coutts"
    4 male
    5 9
    6 1
    7 1
    8 C.A. 37671
    9 15.9
    10 
    11 S
    
    ----------------------------
    ['491', '0', '3', '" Mr. Konrad Mathias Reiersen Hagland"', 'male', '', '1', '0', '65304', '19.9667', '', 'S\n']
    0 491
    1 0
    2 3
    3 " Mr. Konrad Mathias Reiersen Hagland"
    4 male
    5 
    6 1
    7 0
    8 65304
    9 19.9667
    10 
    11 S
    
    ----------------------------
    ['492', '0', '3', '" Mr. Einar Windelov"', 'male', '21', '0', '0', 'SOTON/OQ 3101317', '7.25', '', 'S\n']
    0 492
    1 0
    2 3
    3 " Mr. Einar Windelov"
    4 male
    5 21
    6 0
    7 0
    8 SOTON/OQ 3101317
    9 7.25
    10 
    11 S
    
    ----------------------------
    ['493', '0', '1', '" Mr. Harry Markland Molson"', 'male', '55', '0', '0', '113787', '30.5', 'C30', 'S\n']
    0 493
    1 0
    2 1
    3 " Mr. Harry Markland Molson"
    4 male
    5 55
    6 0
    7 0
    8 113787
    9 30.5
    10 C30
    11 S
    
    ----------------------------
    ['494', '0', '1', '" Mr. Ramon Artagaveytia"', 'male', '71', '0', '0', 'PC 17609', '49.5042', '', 'C\n']
    0 494
    1 0
    2 1
    3 " Mr. Ramon Artagaveytia"
    4 male
    5 71
    6 0
    7 0
    8 PC 17609
    9 49.5042
    10 
    11 C
    
    ----------------------------
    ['495', '0', '3', '" Mr. Edward Roland Stanley"', 'male', '21', '0', '0', 'A/4 45380', '8.05', '', 'S\n']
    0 495
    1 0
    2 3
    3 " Mr. Edward Roland Stanley"
    4 male
    5 21
    6 0
    7 0
    8 A/4 45380
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['496', '0', '3', '" Mr. Gerious Yousseff"', 'male', '', '0', '0', '2627', '14.4583', '', 'C\n']
    0 496
    1 0
    2 3
    3 " Mr. Gerious Yousseff"
    4 male
    5 
    6 0
    7 0
    8 2627
    9 14.4583
    10 
    11 C
    
    ----------------------------
    ['497', '1', '1', '" Miss. Elizabeth Mussey Eustis"', 'female', '54', '1', '0', '36947', '78.2667', 'D20', 'C\n']
    0 497
    1 1
    2 1
    3 " Miss. Elizabeth Mussey Eustis"
    4 female
    5 54
    6 1
    7 0
    8 36947
    9 78.2667
    10 D20
    11 C
    
    ----------------------------
    ['498', '0', '3', '" Mr. Frederick William Shellard"', 'male', '', '0', '0', 'C.A. 6212', '15.1', '', 'S\n']
    0 498
    1 0
    2 3
    3 " Mr. Frederick William Shellard"
    4 male
    5 
    6 0
    7 0
    8 C.A. 6212
    9 15.1
    10 
    11 S
    
    ----------------------------
    ['499', '0', '1', '" Mrs. Hudson J C (Bessie Waldo Daniels) Allison"', 'female', '25', '1', '2', '113781', '151.55', 'C22 C26', 'S\n']
    0 499
    1 0
    2 1
    3 " Mrs. Hudson J C (Bessie Waldo Daniels) Allison"
    4 female
    5 25
    6 1
    7 2
    8 113781
    9 151.55
    10 C22 C26
    11 S
    
    ----------------------------
    ['500', '0', '3', '" Mr. Olof Svensson"', 'male', '24', '0', '0', '350035', '7.7958', '', 'S\n']
    0 500
    1 0
    2 3
    3 " Mr. Olof Svensson"
    4 male
    5 24
    6 0
    7 0
    8 350035
    9 7.7958
    10 
    11 S
    
    ----------------------------
    ['501', '0', '3', '" Mr. Petar Calic"', 'male', '17', '0', '0', '315086', '8.6625', '', 'S\n']
    0 501
    1 0
    2 3
    3 " Mr. Petar Calic"
    4 male
    5 17
    6 0
    7 0
    8 315086
    9 8.6625
    10 
    11 S
    
    ----------------------------
    ['502', '0', '3', '" Miss. Mary Canavan"', 'female', '21', '0', '0', '364846', '7.75', '', 'Q\n']
    0 502
    1 0
    2 3
    3 " Miss. Mary Canavan"
    4 female
    5 21
    6 0
    7 0
    8 364846
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['503', '0', '3', '" Miss. Bridget Mary O\'Sullivan"', 'female', '', '0', '0', '330909', '7.6292', '', 'Q\n']
    0 503
    1 0
    2 3
    3 " Miss. Bridget Mary O'Sullivan"
    4 female
    5 
    6 0
    7 0
    8 330909
    9 7.6292
    10 
    11 Q
    
    ----------------------------
    ['504', '0', '3', '" Miss. Kristina Sofia Laitinen"', 'female', '37', '0', '0', '4135', '9.5875', '', 'S\n']
    0 504
    1 0
    2 3
    3 " Miss. Kristina Sofia Laitinen"
    4 female
    5 37
    6 0
    7 0
    8 4135
    9 9.5875
    10 
    11 S
    
    ----------------------------
    ['505', '1', '1', '" Miss. Roberta Maioni"', 'female', '16', '0', '0', '110152', '86.5', 'B79', 'S\n']
    0 505
    1 1
    2 1
    3 " Miss. Roberta Maioni"
    4 female
    5 16
    6 0
    7 0
    8 110152
    9 86.5
    10 B79
    11 S
    
    ----------------------------
    ['506', '0', '1', '" Mr. Victor de Satode Penasco y Castellana"', 'male', '18', '1', '0', 'PC 17758', '108.9', 'C65', 'C\n']
    0 506
    1 0
    2 1
    3 " Mr. Victor de Satode Penasco y Castellana"
    4 male
    5 18
    6 1
    7 0
    8 PC 17758
    9 108.9
    10 C65
    11 C
    
    ----------------------------
    ['507', '1', '2', '" Mrs. Frederick Charles (Jane Richards) Quick"', 'female', '33', '0', '2', '26360', '26', '', 'S\n']
    0 507
    1 1
    2 2
    3 " Mrs. Frederick Charles (Jane Richards) Quick"
    4 female
    5 33
    6 0
    7 2
    8 26360
    9 26
    10 
    11 S
    
    ----------------------------
    ['508', '1', '1', '" Mr. George (""George Arthur Brayton"") Bradley"', 'male', '', '0', '0', '111427', '26.55', '', 'S\n']
    0 508
    1 1
    2 1
    3 " Mr. George (""George Arthur Brayton"") Bradley"
    4 male
    5 
    6 0
    7 0
    8 111427
    9 26.55
    10 
    11 S
    
    ----------------------------
    ['509', '0', '3', '" Mr. Henry Margido Olsen"', 'male', '28', '0', '0', 'C 4001', '22.525', '', 'S\n']
    0 509
    1 0
    2 3
    3 " Mr. Henry Margido Olsen"
    4 male
    5 28
    6 0
    7 0
    8 C 4001
    9 22.525
    10 
    11 S
    
    ----------------------------
    ['510', '1', '3', '" Mr. Fang Lang"', 'male', '26', '0', '0', '1601', '56.4958', '', 'S\n']
    0 510
    1 1
    2 3
    3 " Mr. Fang Lang"
    4 male
    5 26
    6 0
    7 0
    8 1601
    9 56.4958
    10 
    11 S
    
    ----------------------------
    ['511', '1', '3', '" Mr. Eugene Patrick Daly"', 'male', '29', '0', '0', '382651', '7.75', '', 'Q\n']
    0 511
    1 1
    2 3
    3 " Mr. Eugene Patrick Daly"
    4 male
    5 29
    6 0
    7 0
    8 382651
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['512', '0', '3', '" Mr. James Webber"', 'male', '', '0', '0', 'SOTON/OQ 3101316', '8.05', '', 'S\n']
    0 512
    1 0
    2 3
    3 " Mr. James Webber"
    4 male
    5 
    6 0
    7 0
    8 SOTON/OQ 3101316
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['513', '1', '1', '" Mr. James Robert McGough"', 'male', '36', '0', '0', 'PC 17473', '26.2875', 'E25', 'S\n']
    0 513
    1 1
    2 1
    3 " Mr. James Robert McGough"
    4 male
    5 36
    6 0
    7 0
    8 PC 17473
    9 26.2875
    10 E25
    11 S
    
    ----------------------------
    ['514', '1', '1', '" Mrs. Martin (Elizabeth L. Barrett) Rothschild"', 'female', '54', '1', '0', 'PC 17603', '59.4', '', 'C\n']
    0 514
    1 1
    2 1
    3 " Mrs. Martin (Elizabeth L. Barrett) Rothschild"
    4 female
    5 54
    6 1
    7 0
    8 PC 17603
    9 59.4
    10 
    11 C
    
    ----------------------------
    ['515', '0', '3', '" Mr. Satio Coleff"', 'male', '24', '0', '0', '349209', '7.4958', '', 'S\n']
    0 515
    1 0
    2 3
    3 " Mr. Satio Coleff"
    4 male
    5 24
    6 0
    7 0
    8 349209
    9 7.4958
    10 
    11 S
    
    ----------------------------
    ['516', '0', '1', '" Mr. William Anderson Walker"', 'male', '47', '0', '0', '36967', '34.0208', 'D46', 'S\n']
    0 516
    1 0
    2 1
    3 " Mr. William Anderson Walker"
    4 male
    5 47
    6 0
    7 0
    8 36967
    9 34.0208
    10 D46
    11 S
    
    ----------------------------
    ['517', '1', '2', '" Mrs. (Amelia Milley) Lemore"', 'female', '34', '0', '0', 'C.A. 34260', '10.5', 'F33', 'S\n']
    0 517
    1 1
    2 2
    3 " Mrs. (Amelia Milley) Lemore"
    4 female
    5 34
    6 0
    7 0
    8 C.A. 34260
    9 10.5
    10 F33
    11 S
    
    ----------------------------
    ['518', '0', '3', '" Mr. Patrick Ryan"', 'male', '', '0', '0', '371110', '24.15', '', 'Q\n']
    0 518
    1 0
    2 3
    3 " Mr. Patrick Ryan"
    4 male
    5 
    6 0
    7 0
    8 371110
    9 24.15
    10 
    11 Q
    
    ----------------------------
    ['519', '1', '2', '" Mrs. William A (Florence ""Mary"" Agnes Hughes) Angle"', 'female', '36', '1', '0', '226875', '26', '', 'S\n']
    0 519
    1 1
    2 2
    3 " Mrs. William A (Florence ""Mary"" Agnes Hughes) Angle"
    4 female
    5 36
    6 1
    7 0
    8 226875
    9 26
    10 
    11 S
    
    ----------------------------
    ['520', '0', '3', '" Mr. Stefo Pavlovic"', 'male', '32', '0', '0', '349242', '7.8958', '', 'S\n']
    0 520
    1 0
    2 3
    3 " Mr. Stefo Pavlovic"
    4 male
    5 32
    6 0
    7 0
    8 349242
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['521', '1', '1', '" Miss. Anne Perreault"', 'female', '30', '0', '0', '12749', '93.5', 'B73', 'S\n']
    0 521
    1 1
    2 1
    3 " Miss. Anne Perreault"
    4 female
    5 30
    6 0
    7 0
    8 12749
    9 93.5
    10 B73
    11 S
    
    ----------------------------
    ['522', '0', '3', '" Mr. Janko Vovk"', 'male', '22', '0', '0', '349252', '7.8958', '', 'S\n']
    0 522
    1 0
    2 3
    3 " Mr. Janko Vovk"
    4 male
    5 22
    6 0
    7 0
    8 349252
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['523', '0', '3', '" Mr. Sarkis Lahoud"', 'male', '', '0', '0', '2624', '7.225', '', 'C\n']
    0 523
    1 0
    2 3
    3 " Mr. Sarkis Lahoud"
    4 male
    5 
    6 0
    7 0
    8 2624
    9 7.225
    10 
    11 C
    
    ----------------------------
    ['524', '1', '1', '" Mrs. Louis Albert (Ida Sophia Fischer) Hippach"', 'female', '44', '0', '1', '111361', '57.9792', 'B18', 'C\n']
    0 524
    1 1
    2 1
    3 " Mrs. Louis Albert (Ida Sophia Fischer) Hippach"
    4 female
    5 44
    6 0
    7 1
    8 111361
    9 57.9792
    10 B18
    11 C
    
    ----------------------------
    ['525', '0', '3', '" Mr. Fared Kassem"', 'male', '', '0', '0', '2700', '7.2292', '', 'C\n']
    0 525
    1 0
    2 3
    3 " Mr. Fared Kassem"
    4 male
    5 
    6 0
    7 0
    8 2700
    9 7.2292
    10 
    11 C
    
    ----------------------------
    ['526', '0', '3', '" Mr. James Farrell"', 'male', '40.5', '0', '0', '367232', '7.75', '', 'Q\n']
    0 526
    1 0
    2 3
    3 " Mr. James Farrell"
    4 male
    5 40.5
    6 0
    7 0
    8 367232
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['527', '1', '2', '" Miss. Lucy Ridsdale"', 'female', '50', '0', '0', 'W./C. 14258', '10.5', '', 'S\n']
    0 527
    1 1
    2 2
    3 " Miss. Lucy Ridsdale"
    4 female
    5 50
    6 0
    7 0
    8 W./C. 14258
    9 10.5
    10 
    11 S
    
    ----------------------------
    ['528', '0', '1', '" Mr. John Farthing"', 'male', '', '0', '0', 'PC 17483', '221.7792', 'C95', 'S\n']
    0 528
    1 0
    2 1
    3 " Mr. John Farthing"
    4 male
    5 
    6 0
    7 0
    8 PC 17483
    9 221.7792
    10 C95
    11 S
    
    ----------------------------
    ['529', '0', '3', '" Mr. Johan Werner Salonen"', 'male', '39', '0', '0', '3101296', '7.925', '', 'S\n']
    0 529
    1 0
    2 3
    3 " Mr. Johan Werner Salonen"
    4 male
    5 39
    6 0
    7 0
    8 3101296
    9 7.925
    10 
    11 S
    
    ----------------------------
    ['530', '0', '2', '" Mr. Richard George Hocking"', 'male', '23', '2', '1', '29104', '11.5', '', 'S\n']
    0 530
    1 0
    2 2
    3 " Mr. Richard George Hocking"
    4 male
    5 23
    6 2
    7 1
    8 29104
    9 11.5
    10 
    11 S
    
    ----------------------------
    ['531', '1', '2', '" Miss. Phyllis May Quick"', 'female', '2', '1', '1', '26360', '26', '', 'S\n']
    0 531
    1 1
    2 2
    3 " Miss. Phyllis May Quick"
    4 female
    5 2
    6 1
    7 1
    8 26360
    9 26
    10 
    11 S
    
    ----------------------------
    ['532', '0', '3', '" Mr. Nakli Toufik"', 'male', '', '0', '0', '2641', '7.2292', '', 'C\n']
    0 532
    1 0
    2 3
    3 " Mr. Nakli Toufik"
    4 male
    5 
    6 0
    7 0
    8 2641
    9 7.2292
    10 
    11 C
    
    ----------------------------
    ['533', '0', '3', '" Mr. Joseph Jr Elias"', 'male', '17', '1', '1', '2690', '7.2292', '', 'C\n']
    0 533
    1 0
    2 3
    3 " Mr. Joseph Jr Elias"
    4 male
    5 17
    6 1
    7 1
    8 2690
    9 7.2292
    10 
    11 C
    
    ----------------------------
    ['534', '1', '3', '" Mrs. Catherine (Catherine Rizk) Peter"', 'female', '', '0', '2', '2668', '22.3583', '', 'C\n']
    0 534
    1 1
    2 3
    3 " Mrs. Catherine (Catherine Rizk) Peter"
    4 female
    5 
    6 0
    7 2
    8 2668
    9 22.3583
    10 
    11 C
    
    ----------------------------
    ['535', '0', '3', '" Miss. Marija Cacic"', 'female', '30', '0', '0', '315084', '8.6625', '', 'S\n']
    0 535
    1 0
    2 3
    3 " Miss. Marija Cacic"
    4 female
    5 30
    6 0
    7 0
    8 315084
    9 8.6625
    10 
    11 S
    
    ----------------------------
    ['536', '1', '2', '" Miss. Eva Miriam Hart"', 'female', '7', '0', '2', 'F.C.C. 13529', '26.25', '', 'S\n']
    0 536
    1 1
    2 2
    3 " Miss. Eva Miriam Hart"
    4 female
    5 7
    6 0
    7 2
    8 F.C.C. 13529
    9 26.25
    10 
    11 S
    
    ----------------------------
    ['537', '0', '1', '" Major. Archibald Willingham Butt"', 'male', '45', '0', '0', '113050', '26.55', 'B38', 'S\n']
    0 537
    1 0
    2 1
    3 " Major. Archibald Willingham Butt"
    4 male
    5 45
    6 0
    7 0
    8 113050
    9 26.55
    10 B38
    11 S
    
    ----------------------------
    ['538', '1', '1', '" Miss. Bertha LeRoy"', 'female', '30', '0', '0', 'PC 17761', '106.425', '', 'C\n']
    0 538
    1 1
    2 1
    3 " Miss. Bertha LeRoy"
    4 female
    5 30
    6 0
    7 0
    8 PC 17761
    9 106.425
    10 
    11 C
    
    ----------------------------
    ['539', '0', '3', '" Mr. Samuel Beard Risien"', 'male', '', '0', '0', '364498', '14.5', '', 'S\n']
    0 539
    1 0
    2 3
    3 " Mr. Samuel Beard Risien"
    4 male
    5 
    6 0
    7 0
    8 364498
    9 14.5
    10 
    11 S
    
    ----------------------------
    ['540', '1', '1', '" Miss. Hedwig Margaritha Frolicher"', 'female', '22', '0', '2', '13568', '49.5', 'B39', 'C\n']
    0 540
    1 1
    2 1
    3 " Miss. Hedwig Margaritha Frolicher"
    4 female
    5 22
    6 0
    7 2
    8 13568
    9 49.5
    10 B39
    11 C
    
    ----------------------------
    ['541', '1', '1', '" Miss. Harriet R Crosby"', 'female', '36', '0', '2', 'WE/P 5735', '71', 'B22', 'S\n']
    0 541
    1 1
    2 1
    3 " Miss. Harriet R Crosby"
    4 female
    5 36
    6 0
    7 2
    8 WE/P 5735
    9 71
    10 B22
    11 S
    
    ----------------------------
    ['542', '0', '3', '" Miss. Ingeborg Constanzia Andersson"', 'female', '9', '4', '2', '347082', '31.275', '', 'S\n']
    0 542
    1 0
    2 3
    3 " Miss. Ingeborg Constanzia Andersson"
    4 female
    5 9
    6 4
    7 2
    8 347082
    9 31.275
    10 
    11 S
    
    ----------------------------
    ['543', '0', '3', '" Miss. Sigrid Elisabeth Andersson"', 'female', '11', '4', '2', '347082', '31.275', '', 'S\n']
    0 543
    1 0
    2 3
    3 " Miss. Sigrid Elisabeth Andersson"
    4 female
    5 11
    6 4
    7 2
    8 347082
    9 31.275
    10 
    11 S
    
    ----------------------------
    ['544', '1', '2', '" Mr. Edward Beane"', 'male', '32', '1', '0', '2908', '26', '', 'S\n']
    0 544
    1 1
    2 2
    3 " Mr. Edward Beane"
    4 male
    5 32
    6 1
    7 0
    8 2908
    9 26
    10 
    11 S
    
    ----------------------------
    ['545', '0', '1', '" Mr. Walter Donald Douglas"', 'male', '50', '1', '0', 'PC 17761', '106.425', 'C86', 'C\n']
    0 545
    1 0
    2 1
    3 " Mr. Walter Donald Douglas"
    4 male
    5 50
    6 1
    7 0
    8 PC 17761
    9 106.425
    10 C86
    11 C
    
    ----------------------------
    ['546', '0', '1', '" Mr. Arthur Ernest Nicholson"', 'male', '64', '0', '0', '693', '26', '', 'S\n']
    0 546
    1 0
    2 1
    3 " Mr. Arthur Ernest Nicholson"
    4 male
    5 64
    6 0
    7 0
    8 693
    9 26
    10 
    11 S
    
    ----------------------------
    ['547', '1', '2', '" Mrs. Edward (Ethel Clarke) Beane"', 'female', '19', '1', '0', '2908', '26', '', 'S\n']
    0 547
    1 1
    2 2
    3 " Mrs. Edward (Ethel Clarke) Beane"
    4 female
    5 19
    6 1
    7 0
    8 2908
    9 26
    10 
    11 S
    
    ----------------------------
    ['548', '1', '2', '" Mr. Julian Padro y Manent"', 'male', '', '0', '0', 'SC/PARIS 2146', '13.8625', '', 'C\n']
    0 548
    1 1
    2 2
    3 " Mr. Julian Padro y Manent"
    4 male
    5 
    6 0
    7 0
    8 SC/PARIS 2146
    9 13.8625
    10 
    11 C
    
    ----------------------------
    ['549', '0', '3', '" Mr. Frank John Goldsmith"', 'male', '33', '1', '1', '363291', '20.525', '', 'S\n']
    0 549
    1 0
    2 3
    3 " Mr. Frank John Goldsmith"
    4 male
    5 33
    6 1
    7 1
    8 363291
    9 20.525
    10 
    11 S
    
    ----------------------------
    ['550', '1', '2', '" Master. John Morgan Jr Davies"', 'male', '8', '1', '1', 'C.A. 33112', '36.75', '', 'S\n']
    0 550
    1 1
    2 2
    3 " Master. John Morgan Jr Davies"
    4 male
    5 8
    6 1
    7 1
    8 C.A. 33112
    9 36.75
    10 
    11 S
    
    ----------------------------
    ['551', '1', '1', '" Mr. John Borland Jr Thayer"', 'male', '17', '0', '2', '17421', '110.8833', 'C70', 'C\n']
    0 551
    1 1
    2 1
    3 " Mr. John Borland Jr Thayer"
    4 male
    5 17
    6 0
    7 2
    8 17421
    9 110.8833
    10 C70
    11 C
    
    ----------------------------
    ['552', '0', '2', '" Mr. Percival James R Sharp"', 'male', '27', '0', '0', '244358', '26', '', 'S\n']
    0 552
    1 0
    2 2
    3 " Mr. Percival James R Sharp"
    4 male
    5 27
    6 0
    7 0
    8 244358
    9 26
    10 
    11 S
    
    ----------------------------
    ['553', '0', '3', '" Mr. Timothy O\'Brien"', 'male', '', '0', '0', '330979', '7.8292', '', 'Q\n']
    0 553
    1 0
    2 3
    3 " Mr. Timothy O'Brien"
    4 male
    5 
    6 0
    7 0
    8 330979
    9 7.8292
    10 
    11 Q
    
    ----------------------------
    ['554', '1', '3', '" Mr. Fahim (""Philip Zenni"") Leeni"', 'male', '22', '0', '0', '2620', '7.225', '', 'C\n']
    0 554
    1 1
    2 3
    3 " Mr. Fahim (""Philip Zenni"") Leeni"
    4 male
    5 22
    6 0
    7 0
    8 2620
    9 7.225
    10 
    11 C
    
    ----------------------------
    ['555', '1', '3', '" Miss. Velin Ohman"', 'female', '22', '0', '0', '347085', '7.775', '', 'S\n']
    0 555
    1 1
    2 3
    3 " Miss. Velin Ohman"
    4 female
    5 22
    6 0
    7 0
    8 347085
    9 7.775
    10 
    11 S
    
    ----------------------------
    ['556', '0', '1', '" Mr. George Wright"', 'male', '62', '0', '0', '113807', '26.55', '', 'S\n']
    0 556
    1 0
    2 1
    3 " Mr. George Wright"
    4 male
    5 62
    6 0
    7 0
    8 113807
    9 26.55
    10 
    11 S
    
    ----------------------------
    ['557', '1', '1', '" Lady. (Lucille Christiana Sutherland) (""Mrs Morgan"") Duff Gordon"', 'female', '48', '1', '0', '11755', '39.6', 'A16', 'C\n']
    0 557
    1 1
    2 1
    3 " Lady. (Lucille Christiana Sutherland) (""Mrs Morgan"") Duff Gordon"
    4 female
    5 48
    6 1
    7 0
    8 11755
    9 39.6
    10 A16
    11 C
    
    ----------------------------
    ['558', '0', '1', '" Mr. Victor Robbins"', 'male', '', '0', '0', 'PC 17757', '227.525', '', 'C\n']
    0 558
    1 0
    2 1
    3 " Mr. Victor Robbins"
    4 male
    5 
    6 0
    7 0
    8 PC 17757
    9 227.525
    10 
    11 C
    
    ----------------------------
    ['559', '1', '1', '" Mrs. Emil (Tillie Mandelbaum) Taussig"', 'female', '39', '1', '1', '110413', '79.65', 'E67', 'S\n']
    0 559
    1 1
    2 1
    3 " Mrs. Emil (Tillie Mandelbaum) Taussig"
    4 female
    5 39
    6 1
    7 1
    8 110413
    9 79.65
    10 E67
    11 S
    
    ----------------------------
    ['560', '1', '3', '" Mrs. Guillaume Joseph (Emma) de Messemaeker"', 'female', '36', '1', '0', '345572', '17.4', '', 'S\n']
    0 560
    1 1
    2 3
    3 " Mrs. Guillaume Joseph (Emma) de Messemaeker"
    4 female
    5 36
    6 1
    7 0
    8 345572
    9 17.4
    10 
    11 S
    
    ----------------------------
    ['561', '0', '3', '" Mr. Thomas Rowan Morrow"', 'male', '', '0', '0', '372622', '7.75', '', 'Q\n']
    0 561
    1 0
    2 3
    3 " Mr. Thomas Rowan Morrow"
    4 male
    5 
    6 0
    7 0
    8 372622
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['562', '0', '3', '" Mr. Husein Sivic"', 'male', '40', '0', '0', '349251', '7.8958', '', 'S\n']
    0 562
    1 0
    2 3
    3 " Mr. Husein Sivic"
    4 male
    5 40
    6 0
    7 0
    8 349251
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['563', '0', '2', '" Mr. Robert Douglas Norman"', 'male', '28', '0', '0', '218629', '13.5', '', 'S\n']
    0 563
    1 0
    2 2
    3 " Mr. Robert Douglas Norman"
    4 male
    5 28
    6 0
    7 0
    8 218629
    9 13.5
    10 
    11 S
    
    ----------------------------
    ['564', '0', '3', '" Mr. John Simmons"', 'male', '', '0', '0', 'SOTON/OQ 392082', '8.05', '', 'S\n']
    0 564
    1 0
    2 3
    3 " Mr. John Simmons"
    4 male
    5 
    6 0
    7 0
    8 SOTON/OQ 392082
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['565', '0', '3', '" Miss. (Marion Ogden) Meanwell"', 'female', '', '0', '0', 'SOTON/O.Q. 392087', '8.05', '', 'S\n']
    0 565
    1 0
    2 3
    3 " Miss. (Marion Ogden) Meanwell"
    4 female
    5 
    6 0
    7 0
    8 SOTON/O.Q. 392087
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['566', '0', '3', '" Mr. Alfred J Davies"', 'male', '24', '2', '0', 'A/4 48871', '24.15', '', 'S\n']
    0 566
    1 0
    2 3
    3 " Mr. Alfred J Davies"
    4 male
    5 24
    6 2
    7 0
    8 A/4 48871
    9 24.15
    10 
    11 S
    
    ----------------------------
    ['567', '0', '3', '" Mr. Ilia Stoytcheff"', 'male', '19', '0', '0', '349205', '7.8958', '', 'S\n']
    0 567
    1 0
    2 3
    3 " Mr. Ilia Stoytcheff"
    4 male
    5 19
    6 0
    7 0
    8 349205
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['568', '0', '3', '" Mrs. Nils (Alma Cornelia Berglund) Palsson"', 'female', '29', '0', '4', '349909', '21.075', '', 'S\n']
    0 568
    1 0
    2 3
    3 " Mrs. Nils (Alma Cornelia Berglund) Palsson"
    4 female
    5 29
    6 0
    7 4
    8 349909
    9 21.075
    10 
    11 S
    
    ----------------------------
    ['569', '0', '3', '" Mr. Tannous Doharr"', 'male', '', '0', '0', '2686', '7.2292', '', 'C\n']
    0 569
    1 0
    2 3
    3 " Mr. Tannous Doharr"
    4 male
    5 
    6 0
    7 0
    8 2686
    9 7.2292
    10 
    11 C
    
    ----------------------------
    ['570', '1', '3', '" Mr. Carl Jonsson"', 'male', '32', '0', '0', '350417', '7.8542', '', 'S\n']
    0 570
    1 1
    2 3
    3 " Mr. Carl Jonsson"
    4 male
    5 32
    6 0
    7 0
    8 350417
    9 7.8542
    10 
    11 S
    
    ----------------------------
    ['571', '1', '2', '" Mr. George Harris"', 'male', '62', '0', '0', 'S.W./PP 752', '10.5', '', 'S\n']
    0 571
    1 1
    2 2
    3 " Mr. George Harris"
    4 male
    5 62
    6 0
    7 0
    8 S.W./PP 752
    9 10.5
    10 
    11 S
    
    ----------------------------
    ['572', '1', '1', '" Mrs. Edward Dale (Charlotte Lamson) Appleton"', 'female', '53', '2', '0', '11769', '51.4792', 'C101', 'S\n']
    0 572
    1 1
    2 1
    3 " Mrs. Edward Dale (Charlotte Lamson) Appleton"
    4 female
    5 53
    6 2
    7 0
    8 11769
    9 51.4792
    10 C101
    11 S
    
    ----------------------------
    ['573', '1', '1', '" Mr. John Irwin (""Irving"") Flynn"', 'male', '36', '0', '0', 'PC 17474', '26.3875', 'E25', 'S\n']
    0 573
    1 1
    2 1
    3 " Mr. John Irwin (""Irving"") Flynn"
    4 male
    5 36
    6 0
    7 0
    8 PC 17474
    9 26.3875
    10 E25
    11 S
    
    ----------------------------
    ['574', '1', '3', '" Miss. Mary Kelly"', 'female', '', '0', '0', '14312', '7.75', '', 'Q\n']
    0 574
    1 1
    2 3
    3 " Miss. Mary Kelly"
    4 female
    5 
    6 0
    7 0
    8 14312
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['575', '0', '3', '" Mr. Alfred George John Rush"', 'male', '16', '0', '0', 'A/4. 20589', '8.05', '', 'S\n']
    0 575
    1 0
    2 3
    3 " Mr. Alfred George John Rush"
    4 male
    5 16
    6 0
    7 0
    8 A/4. 20589
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['576', '0', '3', '" Mr. George Patchett"', 'male', '19', '0', '0', '358585', '14.5', '', 'S\n']
    0 576
    1 0
    2 3
    3 " Mr. George Patchett"
    4 male
    5 19
    6 0
    7 0
    8 358585
    9 14.5
    10 
    11 S
    
    ----------------------------
    ['577', '1', '2', '" Miss. Ethel Garside"', 'female', '34', '0', '0', '243880', '13', '', 'S\n']
    0 577
    1 1
    2 2
    3 " Miss. Ethel Garside"
    4 female
    5 34
    6 0
    7 0
    8 243880
    9 13
    10 
    11 S
    
    ----------------------------
    ['578', '1', '1', '" Mrs. William Baird (Alice Munger) Silvey"', 'female', '39', '1', '0', '13507', '55.9', 'E44', 'S\n']
    0 578
    1 1
    2 1
    3 " Mrs. William Baird (Alice Munger) Silvey"
    4 female
    5 39
    6 1
    7 0
    8 13507
    9 55.9
    10 E44
    11 S
    
    ----------------------------
    ['579', '0', '3', '" Mrs. Joseph (Maria Elias) Caram"', 'female', '', '1', '0', '2689', '14.4583', '', 'C\n']
    0 579
    1 0
    2 3
    3 " Mrs. Joseph (Maria Elias) Caram"
    4 female
    5 
    6 1
    7 0
    8 2689
    9 14.4583
    10 
    11 C
    
    ----------------------------
    ['580', '1', '3', '" Mr. Eiriik Jussila"', 'male', '32', '0', '0', 'STON/O 2. 3101286', '7.925', '', 'S\n']
    0 580
    1 1
    2 3
    3 " Mr. Eiriik Jussila"
    4 male
    5 32
    6 0
    7 0
    8 STON/O 2. 3101286
    9 7.925
    10 
    11 S
    
    ----------------------------
    ['581', '1', '2', '" Miss. Julie Rachel Christy"', 'female', '25', '1', '1', '237789', '30', '', 'S\n']
    0 581
    1 1
    2 2
    3 " Miss. Julie Rachel Christy"
    4 female
    5 25
    6 1
    7 1
    8 237789
    9 30
    10 
    11 S
    
    ----------------------------
    ['582', '1', '1', '" Mrs. John Borland (Marian Longstreth Morris) Thayer"', 'female', '39', '1', '1', '17421', '110.8833', 'C68', 'C\n']
    0 582
    1 1
    2 1
    3 " Mrs. John Borland (Marian Longstreth Morris) Thayer"
    4 female
    5 39
    6 1
    7 1
    8 17421
    9 110.8833
    10 C68
    11 C
    
    ----------------------------
    ['583', '0', '2', '" Mr. William James Downton"', 'male', '54', '0', '0', '28403', '26', '', 'S\n']
    0 583
    1 0
    2 2
    3 " Mr. William James Downton"
    4 male
    5 54
    6 0
    7 0
    8 28403
    9 26
    10 
    11 S
    
    ----------------------------
    ['584', '0', '1', '" Mr. John Hugo Ross"', 'male', '36', '0', '0', '13049', '40.125', 'A10', 'C\n']
    0 584
    1 0
    2 1
    3 " Mr. John Hugo Ross"
    4 male
    5 36
    6 0
    7 0
    8 13049
    9 40.125
    10 A10
    11 C
    
    ----------------------------
    ['585', '0', '3', '" Mr. Uscher Paulner"', 'male', '', '0', '0', '3411', '8.7125', '', 'C\n']
    0 585
    1 0
    2 3
    3 " Mr. Uscher Paulner"
    4 male
    5 
    6 0
    7 0
    8 3411
    9 8.7125
    10 
    11 C
    
    ----------------------------
    ['586', '1', '1', '" Miss. Ruth Taussig"', 'female', '18', '0', '2', '110413', '79.65', 'E68', 'S\n']
    0 586
    1 1
    2 1
    3 " Miss. Ruth Taussig"
    4 female
    5 18
    6 0
    7 2
    8 110413
    9 79.65
    10 E68
    11 S
    
    ----------------------------
    ['587', '0', '2', '" Mr. John Denzil Jarvis"', 'male', '47', '0', '0', '237565', '15', '', 'S\n']
    0 587
    1 0
    2 2
    3 " Mr. John Denzil Jarvis"
    4 male
    5 47
    6 0
    7 0
    8 237565
    9 15
    10 
    11 S
    
    ----------------------------
    ['588', '1', '1', '" Mr. Maxmillian Frolicher-Stehli"', 'male', '60', '1', '1', '13567', '79.2', 'B41', 'C\n']
    0 588
    1 1
    2 1
    3 " Mr. Maxmillian Frolicher-Stehli"
    4 male
    5 60
    6 1
    7 1
    8 13567
    9 79.2
    10 B41
    11 C
    
    ----------------------------
    ['589', '0', '3', '" Mr. Eliezer Gilinski"', 'male', '22', '0', '0', '14973', '8.05', '', 'S\n']
    0 589
    1 0
    2 3
    3 " Mr. Eliezer Gilinski"
    4 male
    5 22
    6 0
    7 0
    8 14973
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['590', '0', '3', '" Mr. Joseph Murdlin"', 'male', '', '0', '0', 'A./5. 3235', '8.05', '', 'S\n']
    0 590
    1 0
    2 3
    3 " Mr. Joseph Murdlin"
    4 male
    5 
    6 0
    7 0
    8 A./5. 3235
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['591', '0', '3', '" Mr. Matti Rintamaki"', 'male', '35', '0', '0', 'STON/O 2. 3101273', '7.125', '', 'S\n']
    0 591
    1 0
    2 3
    3 " Mr. Matti Rintamaki"
    4 male
    5 35
    6 0
    7 0
    8 STON/O 2. 3101273
    9 7.125
    10 
    11 S
    
    ----------------------------
    ['592', '1', '1', '" Mrs. Walter Bertram (Martha Eustis) Stephenson"', 'female', '52', '1', '0', '36947', '78.2667', 'D20', 'C\n']
    0 592
    1 1
    2 1
    3 " Mrs. Walter Bertram (Martha Eustis) Stephenson"
    4 female
    5 52
    6 1
    7 0
    8 36947
    9 78.2667
    10 D20
    11 C
    
    ----------------------------
    ['593', '0', '3', '" Mr. William James Elsbury"', 'male', '47', '0', '0', 'A/5 3902', '7.25', '', 'S\n']
    0 593
    1 0
    2 3
    3 " Mr. William James Elsbury"
    4 male
    5 47
    6 0
    7 0
    8 A/5 3902
    9 7.25
    10 
    11 S
    
    ----------------------------
    ['594', '0', '3', '" Miss. Mary Bourke"', 'female', '', '0', '2', '364848', '7.75', '', 'Q\n']
    0 594
    1 0
    2 3
    3 " Miss. Mary Bourke"
    4 female
    5 
    6 0
    7 2
    8 364848
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['595', '0', '2', '" Mr. John Henry Chapman"', 'male', '37', '1', '0', 'SC/AH 29037', '26', '', 'S\n']
    0 595
    1 0
    2 2
    3 " Mr. John Henry Chapman"
    4 male
    5 37
    6 1
    7 0
    8 SC/AH 29037
    9 26
    10 
    11 S
    
    ----------------------------
    ['596', '0', '3', '" Mr. Jean Baptiste Van Impe"', 'male', '36', '1', '1', '345773', '24.15', '', 'S\n']
    0 596
    1 0
    2 3
    3 " Mr. Jean Baptiste Van Impe"
    4 male
    5 36
    6 1
    7 1
    8 345773
    9 24.15
    10 
    11 S
    
    ----------------------------
    ['597', '1', '2', '" Miss. Jessie Wills Leitch"', 'female', '', '0', '0', '248727', '33', '', 'S\n']
    0 597
    1 1
    2 2
    3 " Miss. Jessie Wills Leitch"
    4 female
    5 
    6 0
    7 0
    8 248727
    9 33
    10 
    11 S
    
    ----------------------------
    ['598', '0', '3', '" Mr. Alfred Johnson"', 'male', '49', '0', '0', 'LINE', '0', '', 'S\n']
    0 598
    1 0
    2 3
    3 " Mr. Alfred Johnson"
    4 male
    5 49
    6 0
    7 0
    8 LINE
    9 0
    10 
    11 S
    
    ----------------------------
    ['599', '0', '3', '" Mr. Hanna Boulos"', 'male', '', '0', '0', '2664', '7.225', '', 'C\n']
    0 599
    1 0
    2 3
    3 " Mr. Hanna Boulos"
    4 male
    5 
    6 0
    7 0
    8 2664
    9 7.225
    10 
    11 C
    
    ----------------------------
    ['600', '1', '1', '" Sir. Cosmo Edmund (""Mr Morgan"") Duff Gordon"', 'male', '49', '1', '0', 'PC 17485', '56.9292', 'A20', 'C\n']
    0 600
    1 1
    2 1
    3 " Sir. Cosmo Edmund (""Mr Morgan"") Duff Gordon"
    4 male
    5 49
    6 1
    7 0
    8 PC 17485
    9 56.9292
    10 A20
    11 C
    
    ----------------------------
    ['601', '1', '2', '" Mrs. Sidney Samuel (Amy Frances Christy) Jacobsohn"', 'female', '24', '2', '1', '243847', '27', '', 'S\n']
    0 601
    1 1
    2 2
    3 " Mrs. Sidney Samuel (Amy Frances Christy) Jacobsohn"
    4 female
    5 24
    6 2
    7 1
    8 243847
    9 27
    10 
    11 S
    
    ----------------------------
    ['602', '0', '3', '" Mr. Petco Slabenoff"', 'male', '', '0', '0', '349214', '7.8958', '', 'S\n']
    0 602
    1 0
    2 3
    3 " Mr. Petco Slabenoff"
    4 male
    5 
    6 0
    7 0
    8 349214
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['603', '0', '1', '" Mr. Charles H Harrington"', 'male', '', '0', '0', '113796', '42.4', '', 'S\n']
    0 603
    1 0
    2 1
    3 " Mr. Charles H Harrington"
    4 male
    5 
    6 0
    7 0
    8 113796
    9 42.4
    10 
    11 S
    
    ----------------------------
    ['604', '0', '3', '" Mr. Ernst William Torber"', 'male', '44', '0', '0', '364511', '8.05', '', 'S\n']
    0 604
    1 0
    2 3
    3 " Mr. Ernst William Torber"
    4 male
    5 44
    6 0
    7 0
    8 364511
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['605', '1', '1', '" Mr. Harry (""Mr E Haven"") Homer"', 'male', '35', '0', '0', '111426', '26.55', '', 'C\n']
    0 605
    1 1
    2 1
    3 " Mr. Harry (""Mr E Haven"") Homer"
    4 male
    5 35
    6 0
    7 0
    8 111426
    9 26.55
    10 
    11 C
    
    ----------------------------
    ['606', '0', '3', '" Mr. Edvard Bengtsson Lindell"', 'male', '36', '1', '0', '349910', '15.55', '', 'S\n']
    0 606
    1 0
    2 3
    3 " Mr. Edvard Bengtsson Lindell"
    4 male
    5 36
    6 1
    7 0
    8 349910
    9 15.55
    10 
    11 S
    
    ----------------------------
    ['607', '0', '3', '" Mr. Milan Karaic"', 'male', '30', '0', '0', '349246', '7.8958', '', 'S\n']
    0 607
    1 0
    2 3
    3 " Mr. Milan Karaic"
    4 male
    5 30
    6 0
    7 0
    8 349246
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['608', '1', '1', '" Mr. Robert Williams Daniel"', 'male', '27', '0', '0', '113804', '30.5', '', 'S\n']
    0 608
    1 1
    2 1
    3 " Mr. Robert Williams Daniel"
    4 male
    5 27
    6 0
    7 0
    8 113804
    9 30.5
    10 
    11 S
    
    ----------------------------
    ['609', '1', '2', '" Mrs. Joseph (Juliette Marie Louise Lafargue) Laroche"', 'female', '22', '1', '2', 'SC/Paris 2123', '41.5792', '', 'C\n']
    0 609
    1 1
    2 2
    3 " Mrs. Joseph (Juliette Marie Louise Lafargue) Laroche"
    4 female
    5 22
    6 1
    7 2
    8 SC/Paris 2123
    9 41.5792
    10 
    11 C
    
    ----------------------------
    ['610', '1', '1', '" Miss. Elizabeth W Shutes"', 'female', '40', '0', '0', 'PC 17582', '153.4625', 'C125', 'S\n']
    0 610
    1 1
    2 1
    3 " Miss. Elizabeth W Shutes"
    4 female
    5 40
    6 0
    7 0
    8 PC 17582
    9 153.4625
    10 C125
    11 S
    
    ----------------------------
    ['611', '0', '3', '" Mrs. Anders Johan (Alfrida Konstantia Brogren) Andersson"', 'female', '39', '1', '5', '347082', '31.275', '', 'S\n']
    0 611
    1 0
    2 3
    3 " Mrs. Anders Johan (Alfrida Konstantia Brogren) Andersson"
    4 female
    5 39
    6 1
    7 5
    8 347082
    9 31.275
    10 
    11 S
    
    ----------------------------
    ['612', '0', '3', '" Mr. Jose Neto Jardin"', 'male', '', '0', '0', 'SOTON/O.Q. 3101305', '7.05', '', 'S\n']
    0 612
    1 0
    2 3
    3 " Mr. Jose Neto Jardin"
    4 male
    5 
    6 0
    7 0
    8 SOTON/O.Q. 3101305
    9 7.05
    10 
    11 S
    
    ----------------------------
    ['613', '1', '3', '" Miss. Margaret Jane Murphy"', 'female', '', '1', '0', '367230', '15.5', '', 'Q\n']
    0 613
    1 1
    2 3
    3 " Miss. Margaret Jane Murphy"
    4 female
    5 
    6 1
    7 0
    8 367230
    9 15.5
    10 
    11 Q
    
    ----------------------------
    ['614', '0', '3', '" Mr. John Horgan"', 'male', '', '0', '0', '370377', '7.75', '', 'Q\n']
    0 614
    1 0
    2 3
    3 " Mr. John Horgan"
    4 male
    5 
    6 0
    7 0
    8 370377
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['615', '0', '3', '" Mr. William Alfred Brocklebank"', 'male', '35', '0', '0', '364512', '8.05', '', 'S\n']
    0 615
    1 0
    2 3
    3 " Mr. William Alfred Brocklebank"
    4 male
    5 35
    6 0
    7 0
    8 364512
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['616', '1', '2', '" Miss. Alice Herman"', 'female', '24', '1', '2', '220845', '65', '', 'S\n']
    0 616
    1 1
    2 2
    3 " Miss. Alice Herman"
    4 female
    5 24
    6 1
    7 2
    8 220845
    9 65
    10 
    11 S
    
    ----------------------------
    ['617', '0', '3', '" Mr. Ernst Gilbert Danbom"', 'male', '34', '1', '1', '347080', '14.4', '', 'S\n']
    0 617
    1 0
    2 3
    3 " Mr. Ernst Gilbert Danbom"
    4 male
    5 34
    6 1
    7 1
    8 347080
    9 14.4
    10 
    11 S
    
    ----------------------------
    ['618', '0', '3', '" Mrs. William Arthur (Cordelia K Stanlick) Lobb"', 'female', '26', '1', '0', 'A/5. 3336', '16.1', '', 'S\n']
    0 618
    1 0
    2 3
    3 " Mrs. William Arthur (Cordelia K Stanlick) Lobb"
    4 female
    5 26
    6 1
    7 0
    8 A/5. 3336
    9 16.1
    10 
    11 S
    
    ----------------------------
    ['619', '1', '2', '" Miss. Marion Louise Becker"', 'female', '4', '2', '1', '230136', '39', 'F4', 'S\n']
    0 619
    1 1
    2 2
    3 " Miss. Marion Louise Becker"
    4 female
    5 4
    6 2
    7 1
    8 230136
    9 39
    10 F4
    11 S
    
    ----------------------------
    ['620', '0', '2', '" Mr. Lawrence Gavey"', 'male', '26', '0', '0', '31028', '10.5', '', 'S\n']
    0 620
    1 0
    2 2
    3 " Mr. Lawrence Gavey"
    4 male
    5 26
    6 0
    7 0
    8 31028
    9 10.5
    10 
    11 S
    
    ----------------------------
    ['621', '0', '3', '" Mr. Antoni Yasbeck"', 'male', '27', '1', '0', '2659', '14.4542', '', 'C\n']
    0 621
    1 0
    2 3
    3 " Mr. Antoni Yasbeck"
    4 male
    5 27
    6 1
    7 0
    8 2659
    9 14.4542
    10 
    11 C
    
    ----------------------------
    ['622', '1', '1', '" Mr. Edwin Nelson Jr Kimball"', 'male', '42', '1', '0', '11753', '52.5542', 'D19', 'S\n']
    0 622
    1 1
    2 1
    3 " Mr. Edwin Nelson Jr Kimball"
    4 male
    5 42
    6 1
    7 0
    8 11753
    9 52.5542
    10 D19
    11 S
    
    ----------------------------
    ['623', '1', '3', '" Mr. Sahid Nakid"', 'male', '20', '1', '1', '2653', '15.7417', '', 'C\n']
    0 623
    1 1
    2 3
    3 " Mr. Sahid Nakid"
    4 male
    5 20
    6 1
    7 1
    8 2653
    9 15.7417
    10 
    11 C
    
    ----------------------------
    ['624', '0', '3', '" Mr. Henry Damsgaard Hansen"', 'male', '21', '0', '0', '350029', '7.8542', '', 'S\n']
    0 624
    1 0
    2 3
    3 " Mr. Henry Damsgaard Hansen"
    4 male
    5 21
    6 0
    7 0
    8 350029
    9 7.8542
    10 
    11 S
    
    ----------------------------
    ['625', '0', '3', '" Mr. David John ""Dai"" Bowen"', 'male', '21', '0', '0', '54636', '16.1', '', 'S\n']
    0 625
    1 0
    2 3
    3 " Mr. David John ""Dai"" Bowen"
    4 male
    5 21
    6 0
    7 0
    8 54636
    9 16.1
    10 
    11 S
    
    ----------------------------
    ['626', '0', '1', '" Mr. Frederick Sutton"', 'male', '61', '0', '0', '36963', '32.3208', 'D50', 'S\n']
    0 626
    1 0
    2 1
    3 " Mr. Frederick Sutton"
    4 male
    5 61
    6 0
    7 0
    8 36963
    9 32.3208
    10 D50
    11 S
    
    ----------------------------
    ['627', '0', '2', '" Rev. Charles Leonard Kirkland"', 'male', '57', '0', '0', '219533', '12.35', '', 'Q\n']
    0 627
    1 0
    2 2
    3 " Rev. Charles Leonard Kirkland"
    4 male
    5 57
    6 0
    7 0
    8 219533
    9 12.35
    10 
    11 Q
    
    ----------------------------
    ['628', '1', '1', '" Miss. Gretchen Fiske Longley"', 'female', '21', '0', '0', '13502', '77.9583', 'D9', 'S\n']
    0 628
    1 1
    2 1
    3 " Miss. Gretchen Fiske Longley"
    4 female
    5 21
    6 0
    7 0
    8 13502
    9 77.9583
    10 D9
    11 S
    
    ----------------------------
    ['629', '0', '3', '" Mr. Guentcho Bostandyeff"', 'male', '26', '0', '0', '349224', '7.8958', '', 'S\n']
    0 629
    1 0
    2 3
    3 " Mr. Guentcho Bostandyeff"
    4 male
    5 26
    6 0
    7 0
    8 349224
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['630', '0', '3', '" Mr. Patrick D O\'Connell"', 'male', '', '0', '0', '334912', '7.7333', '', 'Q\n']
    0 630
    1 0
    2 3
    3 " Mr. Patrick D O'Connell"
    4 male
    5 
    6 0
    7 0
    8 334912
    9 7.7333
    10 
    11 Q
    
    ----------------------------
    ['631', '1', '1', '" Mr. Algernon Henry Wilson Barkworth"', 'male', '80', '0', '0', '27042', '30', 'A23', 'S\n']
    0 631
    1 1
    2 1
    3 " Mr. Algernon Henry Wilson Barkworth"
    4 male
    5 80
    6 0
    7 0
    8 27042
    9 30
    10 A23
    11 S
    
    ----------------------------
    ['632', '0', '3', '" Mr. Johan Svensson Lundahl"', 'male', '51', '0', '0', '347743', '7.0542', '', 'S\n']
    0 632
    1 0
    2 3
    3 " Mr. Johan Svensson Lundahl"
    4 male
    5 51
    6 0
    7 0
    8 347743
    9 7.0542
    10 
    11 S
    
    ----------------------------
    ['633', '1', '1', '" Dr. Max Stahelin-Maeglin"', 'male', '32', '0', '0', '13214', '30.5', 'B50', 'C\n']
    0 633
    1 1
    2 1
    3 " Dr. Max Stahelin-Maeglin"
    4 male
    5 32
    6 0
    7 0
    8 13214
    9 30.5
    10 B50
    11 C
    
    ----------------------------
    ['634', '0', '1', '" Mr. William Henry Marsh Parr"', 'male', '', '0', '0', '112052', '0', '', 'S\n']
    0 634
    1 0
    2 1
    3 " Mr. William Henry Marsh Parr"
    4 male
    5 
    6 0
    7 0
    8 112052
    9 0
    10 
    11 S
    
    ----------------------------
    ['635', '0', '3', '" Miss. Mabel Skoog"', 'female', '9', '3', '2', '347088', '27.9', '', 'S\n']
    0 635
    1 0
    2 3
    3 " Miss. Mabel Skoog"
    4 female
    5 9
    6 3
    7 2
    8 347088
    9 27.9
    10 
    11 S
    
    ----------------------------
    ['636', '1', '2', '" Miss. Mary Davis"', 'female', '28', '0', '0', '237668', '13', '', 'S\n']
    0 636
    1 1
    2 2
    3 " Miss. Mary Davis"
    4 female
    5 28
    6 0
    7 0
    8 237668
    9 13
    10 
    11 S
    
    ----------------------------
    ['637', '0', '3', '" Mr. Antti Gustaf Leinonen"', 'male', '32', '0', '0', 'STON/O 2. 3101292', '7.925', '', 'S\n']
    0 637
    1 0
    2 3
    3 " Mr. Antti Gustaf Leinonen"
    4 male
    5 32
    6 0
    7 0
    8 STON/O 2. 3101292
    9 7.925
    10 
    11 S
    
    ----------------------------
    ['638', '0', '2', '" Mr. Harvey Collyer"', 'male', '31', '1', '1', 'C.A. 31921', '26.25', '', 'S\n']
    0 638
    1 0
    2 2
    3 " Mr. Harvey Collyer"
    4 male
    5 31
    6 1
    7 1
    8 C.A. 31921
    9 26.25
    10 
    11 S
    
    ----------------------------
    ['639', '0', '3', '" Mrs. Juha (Maria Emilia Ojala) Panula"', 'female', '41', '0', '5', '3101295', '39.6875', '', 'S\n']
    0 639
    1 0
    2 3
    3 " Mrs. Juha (Maria Emilia Ojala) Panula"
    4 female
    5 41
    6 0
    7 5
    8 3101295
    9 39.6875
    10 
    11 S
    
    ----------------------------
    ['640', '0', '3', '" Mr. Percival Thorneycroft"', 'male', '', '1', '0', '376564', '16.1', '', 'S\n']
    0 640
    1 0
    2 3
    3 " Mr. Percival Thorneycroft"
    4 male
    5 
    6 1
    7 0
    8 376564
    9 16.1
    10 
    11 S
    
    ----------------------------
    ['641', '0', '3', '" Mr. Hans Peder Jensen"', 'male', '20', '0', '0', '350050', '7.8542', '', 'S\n']
    0 641
    1 0
    2 3
    3 " Mr. Hans Peder Jensen"
    4 male
    5 20
    6 0
    7 0
    8 350050
    9 7.8542
    10 
    11 S
    
    ----------------------------
    ['642', '1', '1', '" Mlle. Emma Sagesser"', 'female', '24', '0', '0', 'PC 17477', '69.3', 'B35', 'C\n']
    0 642
    1 1
    2 1
    3 " Mlle. Emma Sagesser"
    4 female
    5 24
    6 0
    7 0
    8 PC 17477
    9 69.3
    10 B35
    11 C
    
    ----------------------------
    ['643', '0', '3', '" Miss. Margit Elizabeth Skoog"', 'female', '2', '3', '2', '347088', '27.9', '', 'S\n']
    0 643
    1 0
    2 3
    3 " Miss. Margit Elizabeth Skoog"
    4 female
    5 2
    6 3
    7 2
    8 347088
    9 27.9
    10 
    11 S
    
    ----------------------------
    ['644', '1', '3', '" Mr. Choong Foo"', 'male', '', '0', '0', '1601', '56.4958', '', 'S\n']
    0 644
    1 1
    2 3
    3 " Mr. Choong Foo"
    4 male
    5 
    6 0
    7 0
    8 1601
    9 56.4958
    10 
    11 S
    
    ----------------------------
    ['645', '1', '3', '" Miss. Eugenie Baclini"', 'female', '0.75', '2', '1', '2666', '19.2583', '', 'C\n']
    0 645
    1 1
    2 3
    3 " Miss. Eugenie Baclini"
    4 female
    5 0.75
    6 2
    7 1
    8 2666
    9 19.2583
    10 
    11 C
    
    ----------------------------
    ['646', '1', '1', '" Mr. Henry Sleeper Harper"', 'male', '48', '1', '0', 'PC 17572', '76.7292', 'D33', 'C\n']
    0 646
    1 1
    2 1
    3 " Mr. Henry Sleeper Harper"
    4 male
    5 48
    6 1
    7 0
    8 PC 17572
    9 76.7292
    10 D33
    11 C
    
    ----------------------------
    ['647', '0', '3', '" Mr. Liudevit Cor"', 'male', '19', '0', '0', '349231', '7.8958', '', 'S\n']
    0 647
    1 0
    2 3
    3 " Mr. Liudevit Cor"
    4 male
    5 19
    6 0
    7 0
    8 349231
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['648', '1', '1', '" Col. Oberst Alfons Simonius-Blumer"', 'male', '56', '0', '0', '13213', '35.5', 'A26', 'C\n']
    0 648
    1 1
    2 1
    3 " Col. Oberst Alfons Simonius-Blumer"
    4 male
    5 56
    6 0
    7 0
    8 13213
    9 35.5
    10 A26
    11 C
    
    ----------------------------
    ['649', '0', '3', '" Mr. Edward Willey"', 'male', '', '0', '0', 'S.O./P.P. 751', '7.55', '', 'S\n']
    0 649
    1 0
    2 3
    3 " Mr. Edward Willey"
    4 male
    5 
    6 0
    7 0
    8 S.O./P.P. 751
    9 7.55
    10 
    11 S
    
    ----------------------------
    ['650', '1', '3', '" Miss. Amy Zillah Elsie Stanley"', 'female', '23', '0', '0', 'CA. 2314', '7.55', '', 'S\n']
    0 650
    1 1
    2 3
    3 " Miss. Amy Zillah Elsie Stanley"
    4 female
    5 23
    6 0
    7 0
    8 CA. 2314
    9 7.55
    10 
    11 S
    
    ----------------------------
    ['651', '0', '3', '" Mr. Mito Mitkoff"', 'male', '', '0', '0', '349221', '7.8958', '', 'S\n']
    0 651
    1 0
    2 3
    3 " Mr. Mito Mitkoff"
    4 male
    5 
    6 0
    7 0
    8 349221
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['652', '1', '2', '" Miss. Elsie Doling"', 'female', '18', '0', '1', '231919', '23', '', 'S\n']
    0 652
    1 1
    2 2
    3 " Miss. Elsie Doling"
    4 female
    5 18
    6 0
    7 1
    8 231919
    9 23
    10 
    11 S
    
    ----------------------------
    ['653', '0', '3', '" Mr. Johannes Halvorsen Kalvik"', 'male', '21', '0', '0', '8475', '8.4333', '', 'S\n']
    0 653
    1 0
    2 3
    3 " Mr. Johannes Halvorsen Kalvik"
    4 male
    5 21
    6 0
    7 0
    8 8475
    9 8.4333
    10 
    11 S
    
    ----------------------------
    ['654', '1', '3', '" Miss. Hanora ""Norah"" O\'Leary"', 'female', '', '0', '0', '330919', '7.8292', '', 'Q\n']
    0 654
    1 1
    2 3
    3 " Miss. Hanora ""Norah"" O'Leary"
    4 female
    5 
    6 0
    7 0
    8 330919
    9 7.8292
    10 
    11 Q
    
    ----------------------------
    ['655', '0', '3', '" Miss. Hanora ""Nora"" Hegarty"', 'female', '18', '0', '0', '365226', '6.75', '', 'Q\n']
    0 655
    1 0
    2 3
    3 " Miss. Hanora ""Nora"" Hegarty"
    4 female
    5 18
    6 0
    7 0
    8 365226
    9 6.75
    10 
    11 Q
    
    ----------------------------
    ['656', '0', '2', '" Mr. Leonard Mark Hickman"', 'male', '24', '2', '0', 'S.O.C. 14879', '73.5', '', 'S\n']
    0 656
    1 0
    2 2
    3 " Mr. Leonard Mark Hickman"
    4 male
    5 24
    6 2
    7 0
    8 S.O.C. 14879
    9 73.5
    10 
    11 S
    
    ----------------------------
    ['657', '0', '3', '" Mr. Alexander Radeff"', 'male', '', '0', '0', '349223', '7.8958', '', 'S\n']
    0 657
    1 0
    2 3
    3 " Mr. Alexander Radeff"
    4 male
    5 
    6 0
    7 0
    8 349223
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['658', '0', '3', '" Mrs. John (Catherine) Bourke"', 'female', '32', '1', '1', '364849', '15.5', '', 'Q\n']
    0 658
    1 0
    2 3
    3 " Mrs. John (Catherine) Bourke"
    4 female
    5 32
    6 1
    7 1
    8 364849
    9 15.5
    10 
    11 Q
    
    ----------------------------
    ['659', '0', '2', '" Mr. George Floyd Eitemiller"', 'male', '23', '0', '0', '29751', '13', '', 'S\n']
    0 659
    1 0
    2 2
    3 " Mr. George Floyd Eitemiller"
    4 male
    5 23
    6 0
    7 0
    8 29751
    9 13
    10 
    11 S
    
    ----------------------------
    ['660', '0', '1', '" Mr. Arthur Webster Newell"', 'male', '58', '0', '2', '35273', '113.275', 'D48', 'C\n']
    0 660
    1 0
    2 1
    3 " Mr. Arthur Webster Newell"
    4 male
    5 58
    6 0
    7 2
    8 35273
    9 113.275
    10 D48
    11 C
    
    ----------------------------
    ['661', '1', '1', '" Dr. Henry William Frauenthal"', 'male', '50', '2', '0', 'PC 17611', '133.65', '', 'S\n']
    0 661
    1 1
    2 1
    3 " Dr. Henry William Frauenthal"
    4 male
    5 50
    6 2
    7 0
    8 PC 17611
    9 133.65
    10 
    11 S
    
    ----------------------------
    ['662', '0', '3', '" Mr. Mohamed Badt"', 'male', '40', '0', '0', '2623', '7.225', '', 'C\n']
    0 662
    1 0
    2 3
    3 " Mr. Mohamed Badt"
    4 male
    5 40
    6 0
    7 0
    8 2623
    9 7.225
    10 
    11 C
    
    ----------------------------
    ['663', '0', '1', '" Mr. Edward Pomeroy Colley"', 'male', '47', '0', '0', '5727', '25.5875', 'E58', 'S\n']
    0 663
    1 0
    2 1
    3 " Mr. Edward Pomeroy Colley"
    4 male
    5 47
    6 0
    7 0
    8 5727
    9 25.5875
    10 E58
    11 S
    
    ----------------------------
    ['664', '0', '3', '" Mr. Peju Coleff"', 'male', '36', '0', '0', '349210', '7.4958', '', 'S\n']
    0 664
    1 0
    2 3
    3 " Mr. Peju Coleff"
    4 male
    5 36
    6 0
    7 0
    8 349210
    9 7.4958
    10 
    11 S
    
    ----------------------------
    ['665', '1', '3', '" Mr. Eino William Lindqvist"', 'male', '20', '1', '0', 'STON/O 2. 3101285', '7.925', '', 'S\n']
    0 665
    1 1
    2 3
    3 " Mr. Eino William Lindqvist"
    4 male
    5 20
    6 1
    7 0
    8 STON/O 2. 3101285
    9 7.925
    10 
    11 S
    
    ----------------------------
    ['666', '0', '2', '" Mr. Lewis Hickman"', 'male', '32', '2', '0', 'S.O.C. 14879', '73.5', '', 'S\n']
    0 666
    1 0
    2 2
    3 " Mr. Lewis Hickman"
    4 male
    5 32
    6 2
    7 0
    8 S.O.C. 14879
    9 73.5
    10 
    11 S
    
    ----------------------------
    ['667', '0', '2', '" Mr. Reginald Fenton Butler"', 'male', '25', '0', '0', '234686', '13', '', 'S\n']
    0 667
    1 0
    2 2
    3 " Mr. Reginald Fenton Butler"
    4 male
    5 25
    6 0
    7 0
    8 234686
    9 13
    10 
    11 S
    
    ----------------------------
    ['668', '0', '3', '" Mr. Knud Paust Rommetvedt"', 'male', '', '0', '0', '312993', '7.775', '', 'S\n']
    0 668
    1 0
    2 3
    3 " Mr. Knud Paust Rommetvedt"
    4 male
    5 
    6 0
    7 0
    8 312993
    9 7.775
    10 
    11 S
    
    ----------------------------
    ['669', '0', '3', '" Mr. Jacob Cook"', 'male', '43', '0', '0', 'A/5 3536', '8.05', '', 'S\n']
    0 669
    1 0
    2 3
    3 " Mr. Jacob Cook"
    4 male
    5 43
    6 0
    7 0
    8 A/5 3536
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['670', '1', '1', '" Mrs. Elmer Zebley (Juliet Cummins Wright) Taylor"', 'female', '', '1', '0', '19996', '52', 'C126', 'S\n']
    0 670
    1 1
    2 1
    3 " Mrs. Elmer Zebley (Juliet Cummins Wright) Taylor"
    4 female
    5 
    6 1
    7 0
    8 19996
    9 52
    10 C126
    11 S
    
    ----------------------------
    ['671', '1', '2', '" Mrs. Thomas William Solomon (Elizabeth Catherine Ford) Brown"', 'female', '40', '1', '1', '29750', '39', '', 'S\n']
    0 671
    1 1
    2 2
    3 " Mrs. Thomas William Solomon (Elizabeth Catherine Ford) Brown"
    4 female
    5 40
    6 1
    7 1
    8 29750
    9 39
    10 
    11 S
    
    ----------------------------
    ['672', '0', '1', '" Mr. Thornton Davidson"', 'male', '31', '1', '0', 'F.C. 12750', '52', 'B71', 'S\n']
    0 672
    1 0
    2 1
    3 " Mr. Thornton Davidson"
    4 male
    5 31
    6 1
    7 0
    8 F.C. 12750
    9 52
    10 B71
    11 S
    
    ----------------------------
    ['673', '0', '2', '" Mr. Henry Michael Mitchell"', 'male', '70', '0', '0', 'C.A. 24580', '10.5', '', 'S\n']
    0 673
    1 0
    2 2
    3 " Mr. Henry Michael Mitchell"
    4 male
    5 70
    6 0
    7 0
    8 C.A. 24580
    9 10.5
    10 
    11 S
    
    ----------------------------
    ['674', '1', '2', '" Mr. Charles Wilhelms"', 'male', '31', '0', '0', '244270', '13', '', 'S\n']
    0 674
    1 1
    2 2
    3 " Mr. Charles Wilhelms"
    4 male
    5 31
    6 0
    7 0
    8 244270
    9 13
    10 
    11 S
    
    ----------------------------
    ['675', '0', '2', '" Mr. Ennis Hastings Watson"', 'male', '', '0', '0', '239856', '0', '', 'S\n']
    0 675
    1 0
    2 2
    3 " Mr. Ennis Hastings Watson"
    4 male
    5 
    6 0
    7 0
    8 239856
    9 0
    10 
    11 S
    
    ----------------------------
    ['676', '0', '3', '" Mr. Gustaf Hjalmar Edvardsson"', 'male', '18', '0', '0', '349912', '7.775', '', 'S\n']
    0 676
    1 0
    2 3
    3 " Mr. Gustaf Hjalmar Edvardsson"
    4 male
    5 18
    6 0
    7 0
    8 349912
    9 7.775
    10 
    11 S
    
    ----------------------------
    ['677', '0', '3', '" Mr. Frederick Charles Sawyer"', 'male', '24.5', '0', '0', '342826', '8.05', '', 'S\n']
    0 677
    1 0
    2 3
    3 " Mr. Frederick Charles Sawyer"
    4 male
    5 24.5
    6 0
    7 0
    8 342826
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['678', '1', '3', '" Miss. Anna Sofia Turja"', 'female', '18', '0', '0', '4138', '9.8417', '', 'S\n']
    0 678
    1 1
    2 3
    3 " Miss. Anna Sofia Turja"
    4 female
    5 18
    6 0
    7 0
    8 4138
    9 9.8417
    10 
    11 S
    
    ----------------------------
    ['679', '0', '3', '" Mrs. Frederick (Augusta Tyler) Goodwin"', 'female', '43', '1', '6', 'CA 2144', '46.9', '', 'S\n']
    0 679
    1 0
    2 3
    3 " Mrs. Frederick (Augusta Tyler) Goodwin"
    4 female
    5 43
    6 1
    7 6
    8 CA 2144
    9 46.9
    10 
    11 S
    
    ----------------------------
    ['680', '1', '1', '" Mr. Thomas Drake Martinez Cardeza"', 'male', '36', '0', '1', 'PC 17755', '512.3292', 'B51 B53 B55', 'C\n']
    0 680
    1 1
    2 1
    3 " Mr. Thomas Drake Martinez Cardeza"
    4 male
    5 36
    6 0
    7 1
    8 PC 17755
    9 512.3292
    10 B51 B53 B55
    11 C
    
    ----------------------------
    ['681', '0', '3', '" Miss. Katie Peters"', 'female', '', '0', '0', '330935', '8.1375', '', 'Q\n']
    0 681
    1 0
    2 3
    3 " Miss. Katie Peters"
    4 female
    5 
    6 0
    7 0
    8 330935
    9 8.1375
    10 
    11 Q
    
    ----------------------------
    ['682', '1', '1', '" Mr. Hammad Hassab"', 'male', '27', '0', '0', 'PC 17572', '76.7292', 'D49', 'C\n']
    0 682
    1 1
    2 1
    3 " Mr. Hammad Hassab"
    4 male
    5 27
    6 0
    7 0
    8 PC 17572
    9 76.7292
    10 D49
    11 C
    
    ----------------------------
    ['683', '0', '3', '" Mr. Thor Anderson Olsvigen"', 'male', '20', '0', '0', '6563', '9.225', '', 'S\n']
    0 683
    1 0
    2 3
    3 " Mr. Thor Anderson Olsvigen"
    4 male
    5 20
    6 0
    7 0
    8 6563
    9 9.225
    10 
    11 S
    
    ----------------------------
    ['684', '0', '3', '" Mr. Charles Edward Goodwin"', 'male', '14', '5', '2', 'CA 2144', '46.9', '', 'S\n']
    0 684
    1 0
    2 3
    3 " Mr. Charles Edward Goodwin"
    4 male
    5 14
    6 5
    7 2
    8 CA 2144
    9 46.9
    10 
    11 S
    
    ----------------------------
    ['685', '0', '2', '" Mr. Thomas William Solomon Brown"', 'male', '60', '1', '1', '29750', '39', '', 'S\n']
    0 685
    1 0
    2 2
    3 " Mr. Thomas William Solomon Brown"
    4 male
    5 60
    6 1
    7 1
    8 29750
    9 39
    10 
    11 S
    
    ----------------------------
    ['686', '0', '2', '" Mr. Joseph Philippe Lemercier Laroche"', 'male', '25', '1', '2', 'SC/Paris 2123', '41.5792', '', 'C\n']
    0 686
    1 0
    2 2
    3 " Mr. Joseph Philippe Lemercier Laroche"
    4 male
    5 25
    6 1
    7 2
    8 SC/Paris 2123
    9 41.5792
    10 
    11 C
    
    ----------------------------
    ['687', '0', '3', '" Mr. Jaako Arnold Panula"', 'male', '14', '4', '1', '3101295', '39.6875', '', 'S\n']
    0 687
    1 0
    2 3
    3 " Mr. Jaako Arnold Panula"
    4 male
    5 14
    6 4
    7 1
    8 3101295
    9 39.6875
    10 
    11 S
    
    ----------------------------
    ['688', '0', '3', '" Mr. Branko Dakic"', 'male', '19', '0', '0', '349228', '10.1708', '', 'S\n']
    0 688
    1 0
    2 3
    3 " Mr. Branko Dakic"
    4 male
    5 19
    6 0
    7 0
    8 349228
    9 10.1708
    10 
    11 S
    
    ----------------------------
    ['689', '0', '3', '" Mr. Eberhard Thelander Fischer"', 'male', '18', '0', '0', '350036', '7.7958', '', 'S\n']
    0 689
    1 0
    2 3
    3 " Mr. Eberhard Thelander Fischer"
    4 male
    5 18
    6 0
    7 0
    8 350036
    9 7.7958
    10 
    11 S
    
    ----------------------------
    ['690', '1', '1', '" Miss. Georgette Alexandra Madill"', 'female', '15', '0', '1', '24160', '211.3375', 'B5', 'S\n']
    0 690
    1 1
    2 1
    3 " Miss. Georgette Alexandra Madill"
    4 female
    5 15
    6 0
    7 1
    8 24160
    9 211.3375
    10 B5
    11 S
    
    ----------------------------
    ['691', '1', '1', '" Mr. Albert Adrian Dick"', 'male', '31', '1', '0', '17474', '57', 'B20', 'S\n']
    0 691
    1 1
    2 1
    3 " Mr. Albert Adrian Dick"
    4 male
    5 31
    6 1
    7 0
    8 17474
    9 57
    10 B20
    11 S
    
    ----------------------------
    ['692', '1', '3', '" Miss. Manca Karun"', 'female', '4', '0', '1', '349256', '13.4167', '', 'C\n']
    0 692
    1 1
    2 3
    3 " Miss. Manca Karun"
    4 female
    5 4
    6 0
    7 1
    8 349256
    9 13.4167
    10 
    11 C
    
    ----------------------------
    ['693', '1', '3', '" Mr. Ali Lam"', 'male', '', '0', '0', '1601', '56.4958', '', 'S\n']
    0 693
    1 1
    2 3
    3 " Mr. Ali Lam"
    4 male
    5 
    6 0
    7 0
    8 1601
    9 56.4958
    10 
    11 S
    
    ----------------------------
    ['694', '0', '3', '" Mr. Khalil Saad"', 'male', '25', '0', '0', '2672', '7.225', '', 'C\n']
    0 694
    1 0
    2 3
    3 " Mr. Khalil Saad"
    4 male
    5 25
    6 0
    7 0
    8 2672
    9 7.225
    10 
    11 C
    
    ----------------------------
    ['695', '0', '1', '" Col. John Weir"', 'male', '60', '0', '0', '113800', '26.55', '', 'S\n']
    0 695
    1 0
    2 1
    3 " Col. John Weir"
    4 male
    5 60
    6 0
    7 0
    8 113800
    9 26.55
    10 
    11 S
    
    ----------------------------
    ['696', '0', '2', '" Mr. Charles Henry Chapman"', 'male', '52', '0', '0', '248731', '13.5', '', 'S\n']
    0 696
    1 0
    2 2
    3 " Mr. Charles Henry Chapman"
    4 male
    5 52
    6 0
    7 0
    8 248731
    9 13.5
    10 
    11 S
    
    ----------------------------
    ['697', '0', '3', '" Mr. James Kelly"', 'male', '44', '0', '0', '363592', '8.05', '', 'S\n']
    0 697
    1 0
    2 3
    3 " Mr. James Kelly"
    4 male
    5 44
    6 0
    7 0
    8 363592
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['698', '1', '3', '" Miss. Katherine ""Katie"" Mullens"', 'female', '', '0', '0', '35852', '7.7333', '', 'Q\n']
    0 698
    1 1
    2 3
    3 " Miss. Katherine ""Katie"" Mullens"
    4 female
    5 
    6 0
    7 0
    8 35852
    9 7.7333
    10 
    11 Q
    
    ----------------------------
    ['699', '0', '1', '" Mr. John Borland Thayer"', 'male', '49', '1', '1', '17421', '110.8833', 'C68', 'C\n']
    0 699
    1 0
    2 1
    3 " Mr. John Borland Thayer"
    4 male
    5 49
    6 1
    7 1
    8 17421
    9 110.8833
    10 C68
    11 C
    
    ----------------------------
    ['700', '0', '3', '" Mr. Adolf Mathias Nicolai Olsen Humblen"', 'male', '42', '0', '0', '348121', '7.65', 'F G63', 'S\n']
    0 700
    1 0
    2 3
    3 " Mr. Adolf Mathias Nicolai Olsen Humblen"
    4 male
    5 42
    6 0
    7 0
    8 348121
    9 7.65
    10 F G63
    11 S
    
    ----------------------------
    ['701', '1', '1', '" Mrs. John Jacob (Madeleine Talmadge Force) Astor"', 'female', '18', '1', '0', 'PC 17757', '227.525', 'C62 C64', 'C\n']
    0 701
    1 1
    2 1
    3 " Mrs. John Jacob (Madeleine Talmadge Force) Astor"
    4 female
    5 18
    6 1
    7 0
    8 PC 17757
    9 227.525
    10 C62 C64
    11 C
    
    ----------------------------
    ['702', '1', '1', '" Mr. Spencer Victor Silverthorne"', 'male', '35', '0', '0', 'PC 17475', '26.2875', 'E24', 'S\n']
    0 702
    1 1
    2 1
    3 " Mr. Spencer Victor Silverthorne"
    4 male
    5 35
    6 0
    7 0
    8 PC 17475
    9 26.2875
    10 E24
    11 S
    
    ----------------------------
    ['703', '0', '3', '" Miss. Saiide Barbara"', 'female', '18', '0', '1', '2691', '14.4542', '', 'C\n']
    0 703
    1 0
    2 3
    3 " Miss. Saiide Barbara"
    4 female
    5 18
    6 0
    7 1
    8 2691
    9 14.4542
    10 
    11 C
    
    ----------------------------
    ['704', '0', '3', '" Mr. Martin Gallagher"', 'male', '25', '0', '0', '36864', '7.7417', '', 'Q\n']
    0 704
    1 0
    2 3
    3 " Mr. Martin Gallagher"
    4 male
    5 25
    6 0
    7 0
    8 36864
    9 7.7417
    10 
    11 Q
    
    ----------------------------
    ['705', '0', '3', '" Mr. Henrik Juul Hansen"', 'male', '26', '1', '0', '350025', '7.8542', '', 'S\n']
    0 705
    1 0
    2 3
    3 " Mr. Henrik Juul Hansen"
    4 male
    5 26
    6 1
    7 0
    8 350025
    9 7.8542
    10 
    11 S
    
    ----------------------------
    ['706', '0', '2', '" Mr. Henry Samuel (""Mr Henry Marshall"") Morley"', 'male', '39', '0', '0', '250655', '26', '', 'S\n']
    0 706
    1 0
    2 2
    3 " Mr. Henry Samuel (""Mr Henry Marshall"") Morley"
    4 male
    5 39
    6 0
    7 0
    8 250655
    9 26
    10 
    11 S
    
    ----------------------------
    ['707', '1', '2', '" Mrs. Florence ""Fannie"" Kelly"', 'female', '45', '0', '0', '223596', '13.5', '', 'S\n']
    0 707
    1 1
    2 2
    3 " Mrs. Florence ""Fannie"" Kelly"
    4 female
    5 45
    6 0
    7 0
    8 223596
    9 13.5
    10 
    11 S
    
    ----------------------------
    ['708', '1', '1', '" Mr. Edward Pennington Calderhead"', 'male', '42', '0', '0', 'PC 17476', '26.2875', 'E24', 'S\n']
    0 708
    1 1
    2 1
    3 " Mr. Edward Pennington Calderhead"
    4 male
    5 42
    6 0
    7 0
    8 PC 17476
    9 26.2875
    10 E24
    11 S
    
    ----------------------------
    ['709', '1', '1', '" Miss. Alice Cleaver"', 'female', '22', '0', '0', '113781', '151.55', '', 'S\n']
    0 709
    1 1
    2 1
    3 " Miss. Alice Cleaver"
    4 female
    5 22
    6 0
    7 0
    8 113781
    9 151.55
    10 
    11 S
    
    ----------------------------
    ['710', '1', '3', '" Master. Halim Gonios (""William George"") Moubarek"', 'male', '', '1', '1', '2661', '15.2458', '', 'C\n']
    0 710
    1 1
    2 3
    3 " Master. Halim Gonios (""William George"") Moubarek"
    4 male
    5 
    6 1
    7 1
    8 2661
    9 15.2458
    10 
    11 C
    
    ----------------------------
    ['711', '1', '1', '" Mlle. Berthe Antonine (""Mrs de Villiers"") Mayne"', 'female', '24', '0', '0', 'PC 17482', '49.5042', 'C90', 'C\n']
    0 711
    1 1
    2 1
    3 " Mlle. Berthe Antonine (""Mrs de Villiers"") Mayne"
    4 female
    5 24
    6 0
    7 0
    8 PC 17482
    9 49.5042
    10 C90
    11 C
    
    ----------------------------
    ['712', '0', '1', '" Mr. Herman Klaber"', 'male', '', '0', '0', '113028', '26.55', 'C124', 'S\n']
    0 712
    1 0
    2 1
    3 " Mr. Herman Klaber"
    4 male
    5 
    6 0
    7 0
    8 113028
    9 26.55
    10 C124
    11 S
    
    ----------------------------
    ['713', '1', '1', '" Mr. Elmer Zebley Taylor"', 'male', '48', '1', '0', '19996', '52', 'C126', 'S\n']
    0 713
    1 1
    2 1
    3 " Mr. Elmer Zebley Taylor"
    4 male
    5 48
    6 1
    7 0
    8 19996
    9 52
    10 C126
    11 S
    
    ----------------------------
    ['714', '0', '3', '" Mr. August Viktor Larsson"', 'male', '29', '0', '0', '7545', '9.4833', '', 'S\n']
    0 714
    1 0
    2 3
    3 " Mr. August Viktor Larsson"
    4 male
    5 29
    6 0
    7 0
    8 7545
    9 9.4833
    10 
    11 S
    
    ----------------------------
    ['715', '0', '2', '" Mr. Samuel Greenberg"', 'male', '52', '0', '0', '250647', '13', '', 'S\n']
    0 715
    1 0
    2 2
    3 " Mr. Samuel Greenberg"
    4 male
    5 52
    6 0
    7 0
    8 250647
    9 13
    10 
    11 S
    
    ----------------------------
    ['716', '0', '3', '" Mr. Peter Andreas Lauritz Andersen Soholt"', 'male', '19', '0', '0', '348124', '7.65', 'F G73', 'S\n']
    0 716
    1 0
    2 3
    3 " Mr. Peter Andreas Lauritz Andersen Soholt"
    4 male
    5 19
    6 0
    7 0
    8 348124
    9 7.65
    10 F G73
    11 S
    
    ----------------------------
    ['717', '1', '1', '" Miss. Caroline Louise Endres"', 'female', '38', '0', '0', 'PC 17757', '227.525', 'C45', 'C\n']
    0 717
    1 1
    2 1
    3 " Miss. Caroline Louise Endres"
    4 female
    5 38
    6 0
    7 0
    8 PC 17757
    9 227.525
    10 C45
    11 C
    
    ----------------------------
    ['718', '1', '2', '" Miss. Edwina Celia ""Winnie"" Troutt"', 'female', '27', '0', '0', '34218', '10.5', 'E101', 'S\n']
    0 718
    1 1
    2 2
    3 " Miss. Edwina Celia ""Winnie"" Troutt"
    4 female
    5 27
    6 0
    7 0
    8 34218
    9 10.5
    10 E101
    11 S
    
    ----------------------------
    ['719', '0', '3', '" Mr. Michael McEvoy"', 'male', '', '0', '0', '36568', '15.5', '', 'Q\n']
    0 719
    1 0
    2 3
    3 " Mr. Michael McEvoy"
    4 male
    5 
    6 0
    7 0
    8 36568
    9 15.5
    10 
    11 Q
    
    ----------------------------
    ['720', '0', '3', '" Mr. Malkolm Joackim Johnson"', 'male', '33', '0', '0', '347062', '7.775', '', 'S\n']
    0 720
    1 0
    2 3
    3 " Mr. Malkolm Joackim Johnson"
    4 male
    5 33
    6 0
    7 0
    8 347062
    9 7.775
    10 
    11 S
    
    ----------------------------
    ['721', '1', '2', '" Miss. Annie Jessie ""Nina"" Harper"', 'female', '6', '0', '1', '248727', '33', '', 'S\n']
    0 721
    1 1
    2 2
    3 " Miss. Annie Jessie ""Nina"" Harper"
    4 female
    5 6
    6 0
    7 1
    8 248727
    9 33
    10 
    11 S
    
    ----------------------------
    ['722', '0', '3', '" Mr. Svend Lauritz Jensen"', 'male', '17', '1', '0', '350048', '7.0542', '', 'S\n']
    0 722
    1 0
    2 3
    3 " Mr. Svend Lauritz Jensen"
    4 male
    5 17
    6 1
    7 0
    8 350048
    9 7.0542
    10 
    11 S
    
    ----------------------------
    ['723', '0', '2', '" Mr. William Henry Gillespie"', 'male', '34', '0', '0', '12233', '13', '', 'S\n']
    0 723
    1 0
    2 2
    3 " Mr. William Henry Gillespie"
    4 male
    5 34
    6 0
    7 0
    8 12233
    9 13
    10 
    11 S
    
    ----------------------------
    ['724', '0', '2', '" Mr. Henry Price Hodges"', 'male', '50', '0', '0', '250643', '13', '', 'S\n']
    0 724
    1 0
    2 2
    3 " Mr. Henry Price Hodges"
    4 male
    5 50
    6 0
    7 0
    8 250643
    9 13
    10 
    11 S
    
    ----------------------------
    ['725', '1', '1', '" Mr. Norman Campbell Chambers"', 'male', '27', '1', '0', '113806', '53.1', 'E8', 'S\n']
    0 725
    1 1
    2 1
    3 " Mr. Norman Campbell Chambers"
    4 male
    5 27
    6 1
    7 0
    8 113806
    9 53.1
    10 E8
    11 S
    
    ----------------------------
    ['726', '0', '3', '" Mr. Luka Oreskovic"', 'male', '20', '0', '0', '315094', '8.6625', '', 'S\n']
    0 726
    1 0
    2 3
    3 " Mr. Luka Oreskovic"
    4 male
    5 20
    6 0
    7 0
    8 315094
    9 8.6625
    10 
    11 S
    
    ----------------------------
    ['727', '1', '2', '" Mrs. Peter Henry (Lillian Jefferys) Renouf"', 'female', '30', '3', '0', '31027', '21', '', 'S\n']
    0 727
    1 1
    2 2
    3 " Mrs. Peter Henry (Lillian Jefferys) Renouf"
    4 female
    5 30
    6 3
    7 0
    8 31027
    9 21
    10 
    11 S
    
    ----------------------------
    ['728', '1', '3', '" Miss. Margareth Mannion"', 'female', '', '0', '0', '36866', '7.7375', '', 'Q\n']
    0 728
    1 1
    2 3
    3 " Miss. Margareth Mannion"
    4 female
    5 
    6 0
    7 0
    8 36866
    9 7.7375
    10 
    11 Q
    
    ----------------------------
    ['729', '0', '2', '" Mr. Kurt Arnold Gottfrid Bryhl"', 'male', '25', '1', '0', '236853', '26', '', 'S\n']
    0 729
    1 0
    2 2
    3 " Mr. Kurt Arnold Gottfrid Bryhl"
    4 male
    5 25
    6 1
    7 0
    8 236853
    9 26
    10 
    11 S
    
    ----------------------------
    ['730', '0', '3', '" Miss. Pieta Sofia Ilmakangas"', 'female', '25', '1', '0', 'STON/O2. 3101271', '7.925', '', 'S\n']
    0 730
    1 0
    2 3
    3 " Miss. Pieta Sofia Ilmakangas"
    4 female
    5 25
    6 1
    7 0
    8 STON/O2. 3101271
    9 7.925
    10 
    11 S
    
    ----------------------------
    ['731', '1', '1', '" Miss. Elisabeth Walton Allen"', 'female', '29', '0', '0', '24160', '211.3375', 'B5', 'S\n']
    0 731
    1 1
    2 1
    3 " Miss. Elisabeth Walton Allen"
    4 female
    5 29
    6 0
    7 0
    8 24160
    9 211.3375
    10 B5
    11 S
    
    ----------------------------
    ['732', '0', '3', '" Mr. Houssein G N Hassan"', 'male', '11', '0', '0', '2699', '18.7875', '', 'C\n']
    0 732
    1 0
    2 3
    3 " Mr. Houssein G N Hassan"
    4 male
    5 11
    6 0
    7 0
    8 2699
    9 18.7875
    10 
    11 C
    
    ----------------------------
    ['733', '0', '2', '" Mr. Robert J Knight"', 'male', '', '0', '0', '239855', '0', '', 'S\n']
    0 733
    1 0
    2 2
    3 " Mr. Robert J Knight"
    4 male
    5 
    6 0
    7 0
    8 239855
    9 0
    10 
    11 S
    
    ----------------------------
    ['734', '0', '2', '" Mr. William John Berriman"', 'male', '23', '0', '0', '28425', '13', '', 'S\n']
    0 734
    1 0
    2 2
    3 " Mr. William John Berriman"
    4 male
    5 23
    6 0
    7 0
    8 28425
    9 13
    10 
    11 S
    
    ----------------------------
    ['735', '0', '2', '" Mr. Moses Aaron Troupiansky"', 'male', '23', '0', '0', '233639', '13', '', 'S\n']
    0 735
    1 0
    2 2
    3 " Mr. Moses Aaron Troupiansky"
    4 male
    5 23
    6 0
    7 0
    8 233639
    9 13
    10 
    11 S
    
    ----------------------------
    ['736', '0', '3', '" Mr. Leslie Williams"', 'male', '28.5', '0', '0', '54636', '16.1', '', 'S\n']
    0 736
    1 0
    2 3
    3 " Mr. Leslie Williams"
    4 male
    5 28.5
    6 0
    7 0
    8 54636
    9 16.1
    10 
    11 S
    
    ----------------------------
    ['737', '0', '3', '" Mrs. Edward (Margaret Ann Watson) Ford"', 'female', '48', '1', '3', 'W./C. 6608', '34.375', '', 'S\n']
    0 737
    1 0
    2 3
    3 " Mrs. Edward (Margaret Ann Watson) Ford"
    4 female
    5 48
    6 1
    7 3
    8 W./C. 6608
    9 34.375
    10 
    11 S
    
    ----------------------------
    ['738', '1', '1', '" Mr. Gustave J Lesurer"', 'male', '35', '0', '0', 'PC 17755', '512.3292', 'B101', 'C\n']
    0 738
    1 1
    2 1
    3 " Mr. Gustave J Lesurer"
    4 male
    5 35
    6 0
    7 0
    8 PC 17755
    9 512.3292
    10 B101
    11 C
    
    ----------------------------
    ['739', '0', '3', '" Mr. Kanio Ivanoff"', 'male', '', '0', '0', '349201', '7.8958', '', 'S\n']
    0 739
    1 0
    2 3
    3 " Mr. Kanio Ivanoff"
    4 male
    5 
    6 0
    7 0
    8 349201
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['740', '0', '3', '" Mr. Minko Nankoff"', 'male', '', '0', '0', '349218', '7.8958', '', 'S\n']
    0 740
    1 0
    2 3
    3 " Mr. Minko Nankoff"
    4 male
    5 
    6 0
    7 0
    8 349218
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['741', '1', '1', '" Mr. Walter James Hawksford"', 'male', '', '0', '0', '16988', '30', 'D45', 'S\n']
    0 741
    1 1
    2 1
    3 " Mr. Walter James Hawksford"
    4 male
    5 
    6 0
    7 0
    8 16988
    9 30
    10 D45
    11 S
    
    ----------------------------
    ['742', '0', '1', '" Mr. Tyrell William Cavendish"', 'male', '36', '1', '0', '19877', '78.85', 'C46', 'S\n']
    0 742
    1 0
    2 1
    3 " Mr. Tyrell William Cavendish"
    4 male
    5 36
    6 1
    7 0
    8 19877
    9 78.85
    10 C46
    11 S
    
    ----------------------------
    ['743', '1', '1', '" Miss. Susan Parker ""Suzette"" Ryerson"', 'female', '21', '2', '2', 'PC 17608', '262.375', 'B57 B59 B63 B66', 'C\n']
    0 743
    1 1
    2 1
    3 " Miss. Susan Parker ""Suzette"" Ryerson"
    4 female
    5 21
    6 2
    7 2
    8 PC 17608
    9 262.375
    10 B57 B59 B63 B66
    11 C
    
    ----------------------------
    ['744', '0', '3', '" Mr. Neal McNamee"', 'male', '24', '1', '0', '376566', '16.1', '', 'S\n']
    0 744
    1 0
    2 3
    3 " Mr. Neal McNamee"
    4 male
    5 24
    6 1
    7 0
    8 376566
    9 16.1
    10 
    11 S
    
    ----------------------------
    ['745', '1', '3', '" Mr. Juho Stranden"', 'male', '31', '0', '0', 'STON/O 2. 3101288', '7.925', '', 'S\n']
    0 745
    1 1
    2 3
    3 " Mr. Juho Stranden"
    4 male
    5 31
    6 0
    7 0
    8 STON/O 2. 3101288
    9 7.925
    10 
    11 S
    
    ----------------------------
    ['746', '0', '1', '" Capt. Edward Gifford Crosby"', 'male', '70', '1', '1', 'WE/P 5735', '71', 'B22', 'S\n']
    0 746
    1 0
    2 1
    3 " Capt. Edward Gifford Crosby"
    4 male
    5 70
    6 1
    7 1
    8 WE/P 5735
    9 71
    10 B22
    11 S
    
    ----------------------------
    ['747', '0', '3', '" Mr. Rossmore Edward Abbott"', 'male', '16', '1', '1', 'C.A. 2673', '20.25', '', 'S\n']
    0 747
    1 0
    2 3
    3 " Mr. Rossmore Edward Abbott"
    4 male
    5 16
    6 1
    7 1
    8 C.A. 2673
    9 20.25
    10 
    11 S
    
    ----------------------------
    ['748', '1', '2', '" Miss. Anna Sinkkonen"', 'female', '30', '0', '0', '250648', '13', '', 'S\n']
    0 748
    1 1
    2 2
    3 " Miss. Anna Sinkkonen"
    4 female
    5 30
    6 0
    7 0
    8 250648
    9 13
    10 
    11 S
    
    ----------------------------
    ['749', '0', '1', '" Mr. Daniel Warner Marvin"', 'male', '19', '1', '0', '113773', '53.1', 'D30', 'S\n']
    0 749
    1 0
    2 1
    3 " Mr. Daniel Warner Marvin"
    4 male
    5 19
    6 1
    7 0
    8 113773
    9 53.1
    10 D30
    11 S
    
    ----------------------------
    ['750', '0', '3', '" Mr. Michael Connaghton"', 'male', '31', '0', '0', '335097', '7.75', '', 'Q\n']
    0 750
    1 0
    2 3
    3 " Mr. Michael Connaghton"
    4 male
    5 31
    6 0
    7 0
    8 335097
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['751', '1', '2', '" Miss. Joan Wells"', 'female', '4', '1', '1', '29103', '23', '', 'S\n']
    0 751
    1 1
    2 2
    3 " Miss. Joan Wells"
    4 female
    5 4
    6 1
    7 1
    8 29103
    9 23
    10 
    11 S
    
    ----------------------------
    ['752', '1', '3', '" Master. Meier Moor"', 'male', '6', '0', '1', '392096', '12.475', 'E121', 'S\n']
    0 752
    1 1
    2 3
    3 " Master. Meier Moor"
    4 male
    5 6
    6 0
    7 1
    8 392096
    9 12.475
    10 E121
    11 S
    
    ----------------------------
    ['753', '0', '3', '" Mr. Johannes Joseph Vande Velde"', 'male', '33', '0', '0', '345780', '9.5', '', 'S\n']
    0 753
    1 0
    2 3
    3 " Mr. Johannes Joseph Vande Velde"
    4 male
    5 33
    6 0
    7 0
    8 345780
    9 9.5
    10 
    11 S
    
    ----------------------------
    ['754', '0', '3', '" Mr. Lalio Jonkoff"', 'male', '23', '0', '0', '349204', '7.8958', '', 'S\n']
    0 754
    1 0
    2 3
    3 " Mr. Lalio Jonkoff"
    4 male
    5 23
    6 0
    7 0
    8 349204
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['755', '1', '2', '" Mrs. Samuel (Jane Laver) Herman"', 'female', '48', '1', '2', '220845', '65', '', 'S\n']
    0 755
    1 1
    2 2
    3 " Mrs. Samuel (Jane Laver) Herman"
    4 female
    5 48
    6 1
    7 2
    8 220845
    9 65
    10 
    11 S
    
    ----------------------------
    ['756', '1', '2', '" Master. Viljo Hamalainen"', 'male', '0.67', '1', '1', '250649', '14.5', '', 'S\n']
    0 756
    1 1
    2 2
    3 " Master. Viljo Hamalainen"
    4 male
    5 0.67
    6 1
    7 1
    8 250649
    9 14.5
    10 
    11 S
    
    ----------------------------
    ['757', '0', '3', '" Mr. August Sigfrid Carlsson"', 'male', '28', '0', '0', '350042', '7.7958', '', 'S\n']
    0 757
    1 0
    2 3
    3 " Mr. August Sigfrid Carlsson"
    4 male
    5 28
    6 0
    7 0
    8 350042
    9 7.7958
    10 
    11 S
    
    ----------------------------
    ['758', '0', '2', '" Mr. Percy Andrew Bailey"', 'male', '18', '0', '0', '29108', '11.5', '', 'S\n']
    0 758
    1 0
    2 2
    3 " Mr. Percy Andrew Bailey"
    4 male
    5 18
    6 0
    7 0
    8 29108
    9 11.5
    10 
    11 S
    
    ----------------------------
    ['759', '0', '3', '" Mr. Thomas Leonard Theobald"', 'male', '34', '0', '0', '363294', '8.05', '', 'S\n']
    0 759
    1 0
    2 3
    3 " Mr. Thomas Leonard Theobald"
    4 male
    5 34
    6 0
    7 0
    8 363294
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['760', '1', '1', '" the Countess. of (Lucy Noel Martha Dyer-Edwards) Rothes"', 'female', '33', '0', '0', '110152', '86.5', 'B77', 'S\n']
    0 760
    1 1
    2 1
    3 " the Countess. of (Lucy Noel Martha Dyer-Edwards) Rothes"
    4 female
    5 33
    6 0
    7 0
    8 110152
    9 86.5
    10 B77
    11 S
    
    ----------------------------
    ['761', '0', '3', '" Mr. John Garfirth"', 'male', '', '0', '0', '358585', '14.5', '', 'S\n']
    0 761
    1 0
    2 3
    3 " Mr. John Garfirth"
    4 male
    5 
    6 0
    7 0
    8 358585
    9 14.5
    10 
    11 S
    
    ----------------------------
    ['762', '0', '3', '" Mr. Iisakki Antino Aijo Nirva"', 'male', '41', '0', '0', 'SOTON/O2 3101272', '7.125', '', 'S\n']
    0 762
    1 0
    2 3
    3 " Mr. Iisakki Antino Aijo Nirva"
    4 male
    5 41
    6 0
    7 0
    8 SOTON/O2 3101272
    9 7.125
    10 
    11 S
    
    ----------------------------
    ['763', '1', '3', '" Mr. Hanna Assi Barah"', 'male', '20', '0', '0', '2663', '7.2292', '', 'C\n']
    0 763
    1 1
    2 3
    3 " Mr. Hanna Assi Barah"
    4 male
    5 20
    6 0
    7 0
    8 2663
    9 7.2292
    10 
    11 C
    
    ----------------------------
    ['764', '1', '1', '" Mrs. William Ernest (Lucile Polk) Carter"', 'female', '36', '1', '2', '113760', '120', 'B96 B98', 'S\n']
    0 764
    1 1
    2 1
    3 " Mrs. William Ernest (Lucile Polk) Carter"
    4 female
    5 36
    6 1
    7 2
    8 113760
    9 120
    10 B96 B98
    11 S
    
    ----------------------------
    ['765', '0', '3', '" Mr. Hans Linus Eklund"', 'male', '16', '0', '0', '347074', '7.775', '', 'S\n']
    0 765
    1 0
    2 3
    3 " Mr. Hans Linus Eklund"
    4 male
    5 16
    6 0
    7 0
    8 347074
    9 7.775
    10 
    11 S
    
    ----------------------------
    ['766', '1', '1', '" Mrs. John C (Anna Andrews) Hogeboom"', 'female', '51', '1', '0', '13502', '77.9583', 'D11', 'S\n']
    0 766
    1 1
    2 1
    3 " Mrs. John C (Anna Andrews) Hogeboom"
    4 female
    5 51
    6 1
    7 0
    8 13502
    9 77.9583
    10 D11
    11 S
    
    ----------------------------
    ['767', '0', '1', '" Dr. Arthur Jackson Brewe"', 'male', '', '0', '0', '112379', '39.6', '', 'C\n']
    0 767
    1 0
    2 1
    3 " Dr. Arthur Jackson Brewe"
    4 male
    5 
    6 0
    7 0
    8 112379
    9 39.6
    10 
    11 C
    
    ----------------------------
    ['768', '0', '3', '" Miss. Mary Mangan"', 'female', '30.5', '0', '0', '364850', '7.75', '', 'Q\n']
    0 768
    1 0
    2 3
    3 " Miss. Mary Mangan"
    4 female
    5 30.5
    6 0
    7 0
    8 364850
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['769', '0', '3', '" Mr. Daniel J Moran"', 'male', '', '1', '0', '371110', '24.15', '', 'Q\n']
    0 769
    1 0
    2 3
    3 " Mr. Daniel J Moran"
    4 male
    5 
    6 1
    7 0
    8 371110
    9 24.15
    10 
    11 Q
    
    ----------------------------
    ['770', '0', '3', '" Mr. Daniel Danielsen Gronnestad"', 'male', '32', '0', '0', '8471', '8.3625', '', 'S\n']
    0 770
    1 0
    2 3
    3 " Mr. Daniel Danielsen Gronnestad"
    4 male
    5 32
    6 0
    7 0
    8 8471
    9 8.3625
    10 
    11 S
    
    ----------------------------
    ['771', '0', '3', '" Mr. Rene Aime Lievens"', 'male', '24', '0', '0', '345781', '9.5', '', 'S\n']
    0 771
    1 0
    2 3
    3 " Mr. Rene Aime Lievens"
    4 male
    5 24
    6 0
    7 0
    8 345781
    9 9.5
    10 
    11 S
    
    ----------------------------
    ['772', '0', '3', '" Mr. Niels Peder Jensen"', 'male', '48', '0', '0', '350047', '7.8542', '', 'S\n']
    0 772
    1 0
    2 3
    3 " Mr. Niels Peder Jensen"
    4 male
    5 48
    6 0
    7 0
    8 350047
    9 7.8542
    10 
    11 S
    
    ----------------------------
    ['773', '0', '2', '" Mrs. (Mary) Mack"', 'female', '57', '0', '0', 'S.O./P.P. 3', '10.5', 'E77', 'S\n']
    0 773
    1 0
    2 2
    3 " Mrs. (Mary) Mack"
    4 female
    5 57
    6 0
    7 0
    8 S.O./P.P. 3
    9 10.5
    10 E77
    11 S
    
    ----------------------------
    ['774', '0', '3', '" Mr. Dibo Elias"', 'male', '', '0', '0', '2674', '7.225', '', 'C\n']
    0 774
    1 0
    2 3
    3 " Mr. Dibo Elias"
    4 male
    5 
    6 0
    7 0
    8 2674
    9 7.225
    10 
    11 C
    
    ----------------------------
    ['775', '1', '2', '" Mrs. Elizabeth (Eliza Needs) Hocking"', 'female', '54', '1', '3', '29105', '23', '', 'S\n']
    0 775
    1 1
    2 2
    3 " Mrs. Elizabeth (Eliza Needs) Hocking"
    4 female
    5 54
    6 1
    7 3
    8 29105
    9 23
    10 
    11 S
    
    ----------------------------
    ['776', '0', '3', '" Mr. Pehr Fabian Oliver Malkolm Myhrman"', 'male', '18', '0', '0', '347078', '7.75', '', 'S\n']
    0 776
    1 0
    2 3
    3 " Mr. Pehr Fabian Oliver Malkolm Myhrman"
    4 male
    5 18
    6 0
    7 0
    8 347078
    9 7.75
    10 
    11 S
    
    ----------------------------
    ['777', '0', '3', '" Mr. Roger Tobin"', 'male', '', '0', '0', '383121', '7.75', 'F38', 'Q\n']
    0 777
    1 0
    2 3
    3 " Mr. Roger Tobin"
    4 male
    5 
    6 0
    7 0
    8 383121
    9 7.75
    10 F38
    11 Q
    
    ----------------------------
    ['778', '1', '3', '" Miss. Virginia Ethel Emanuel"', 'female', '5', '0', '0', '364516', '12.475', '', 'S\n']
    0 778
    1 1
    2 3
    3 " Miss. Virginia Ethel Emanuel"
    4 female
    5 5
    6 0
    7 0
    8 364516
    9 12.475
    10 
    11 S
    
    ----------------------------
    ['779', '0', '3', '" Mr. Thomas J Kilgannon"', 'male', '', '0', '0', '36865', '7.7375', '', 'Q\n']
    0 779
    1 0
    2 3
    3 " Mr. Thomas J Kilgannon"
    4 male
    5 
    6 0
    7 0
    8 36865
    9 7.7375
    10 
    11 Q
    
    ----------------------------
    ['780', '1', '1', '" Mrs. Edward Scott (Elisabeth Walton McMillan) Robert"', 'female', '43', '0', '1', '24160', '211.3375', 'B3', 'S\n']
    0 780
    1 1
    2 1
    3 " Mrs. Edward Scott (Elisabeth Walton McMillan) Robert"
    4 female
    5 43
    6 0
    7 1
    8 24160
    9 211.3375
    10 B3
    11 S
    
    ----------------------------
    ['781', '1', '3', '" Miss. Banoura Ayoub"', 'female', '13', '0', '0', '2687', '7.2292', '', 'C\n']
    0 781
    1 1
    2 3
    3 " Miss. Banoura Ayoub"
    4 female
    5 13
    6 0
    7 0
    8 2687
    9 7.2292
    10 
    11 C
    
    ----------------------------
    ['782', '1', '1', '" Mrs. Albert Adrian (Vera Gillespie) Dick"', 'female', '17', '1', '0', '17474', '57', 'B20', 'S\n']
    0 782
    1 1
    2 1
    3 " Mrs. Albert Adrian (Vera Gillespie) Dick"
    4 female
    5 17
    6 1
    7 0
    8 17474
    9 57
    10 B20
    11 S
    
    ----------------------------
    ['783', '0', '1', '" Mr. Milton Clyde Long"', 'male', '29', '0', '0', '113501', '30', 'D6', 'S\n']
    0 783
    1 0
    2 1
    3 " Mr. Milton Clyde Long"
    4 male
    5 29
    6 0
    7 0
    8 113501
    9 30
    10 D6
    11 S
    
    ----------------------------
    ['784', '0', '3', '" Mr. Andrew G Johnston"', 'male', '', '1', '2', 'W./C. 6607', '23.45', '', 'S\n']
    0 784
    1 0
    2 3
    3 " Mr. Andrew G Johnston"
    4 male
    5 
    6 1
    7 2
    8 W./C. 6607
    9 23.45
    10 
    11 S
    
    ----------------------------
    ['785', '0', '3', '" Mr. William Ali"', 'male', '25', '0', '0', 'SOTON/O.Q. 3101312', '7.05', '', 'S\n']
    0 785
    1 0
    2 3
    3 " Mr. William Ali"
    4 male
    5 25
    6 0
    7 0
    8 SOTON/O.Q. 3101312
    9 7.05
    10 
    11 S
    
    ----------------------------
    ['786', '0', '3', '" Mr. Abraham (David Lishin) Harmer"', 'male', '25', '0', '0', '374887', '7.25', '', 'S\n']
    0 786
    1 0
    2 3
    3 " Mr. Abraham (David Lishin) Harmer"
    4 male
    5 25
    6 0
    7 0
    8 374887
    9 7.25
    10 
    11 S
    
    ----------------------------
    ['787', '1', '3', '" Miss. Anna Sofia Sjoblom"', 'female', '18', '0', '0', '3101265', '7.4958', '', 'S\n']
    0 787
    1 1
    2 3
    3 " Miss. Anna Sofia Sjoblom"
    4 female
    5 18
    6 0
    7 0
    8 3101265
    9 7.4958
    10 
    11 S
    
    ----------------------------
    ['788', '0', '3', '" Master. George Hugh Rice"', 'male', '8', '4', '1', '382652', '29.125', '', 'Q\n']
    0 788
    1 0
    2 3
    3 " Master. George Hugh Rice"
    4 male
    5 8
    6 4
    7 1
    8 382652
    9 29.125
    10 
    11 Q
    
    ----------------------------
    ['789', '1', '3', '" Master. Bertram Vere Dean"', 'male', '1', '1', '2', 'C.A. 2315', '20.575', '', 'S\n']
    0 789
    1 1
    2 3
    3 " Master. Bertram Vere Dean"
    4 male
    5 1
    6 1
    7 2
    8 C.A. 2315
    9 20.575
    10 
    11 S
    
    ----------------------------
    ['790', '0', '1', '" Mr. Benjamin Guggenheim"', 'male', '46', '0', '0', 'PC 17593', '79.2', 'B82 B84', 'C\n']
    0 790
    1 0
    2 1
    3 " Mr. Benjamin Guggenheim"
    4 male
    5 46
    6 0
    7 0
    8 PC 17593
    9 79.2
    10 B82 B84
    11 C
    
    ----------------------------
    ['791', '0', '3', '" Mr. Andrew ""Andy"" Keane"', 'male', '', '0', '0', '12460', '7.75', '', 'Q\n']
    0 791
    1 0
    2 3
    3 " Mr. Andrew ""Andy"" Keane"
    4 male
    5 
    6 0
    7 0
    8 12460
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['792', '0', '2', '" Mr. Alfred Gaskell"', 'male', '16', '0', '0', '239865', '26', '', 'S\n']
    0 792
    1 0
    2 2
    3 " Mr. Alfred Gaskell"
    4 male
    5 16
    6 0
    7 0
    8 239865
    9 26
    10 
    11 S
    
    ----------------------------
    ['793', '0', '3', '" Miss. Stella Anna Sage"', 'female', '', '8', '2', 'CA. 2343', '69.55', '', 'S\n']
    0 793
    1 0
    2 3
    3 " Miss. Stella Anna Sage"
    4 female
    5 
    6 8
    7 2
    8 CA. 2343
    9 69.55
    10 
    11 S
    
    ----------------------------
    ['794', '0', '1', '" Mr. William Fisher Hoyt"', 'male', '', '0', '0', 'PC 17600', '30.6958', '', 'C\n']
    0 794
    1 0
    2 1
    3 " Mr. William Fisher Hoyt"
    4 male
    5 
    6 0
    7 0
    8 PC 17600
    9 30.6958
    10 
    11 C
    
    ----------------------------
    ['795', '0', '3', '" Mr. Ristiu Dantcheff"', 'male', '25', '0', '0', '349203', '7.8958', '', 'S\n']
    0 795
    1 0
    2 3
    3 " Mr. Ristiu Dantcheff"
    4 male
    5 25
    6 0
    7 0
    8 349203
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['796', '0', '2', '" Mr. Richard Otter"', 'male', '39', '0', '0', '28213', '13', '', 'S\n']
    0 796
    1 0
    2 2
    3 " Mr. Richard Otter"
    4 male
    5 39
    6 0
    7 0
    8 28213
    9 13
    10 
    11 S
    
    ----------------------------
    ['797', '1', '1', '" Dr. Alice (Farnham) Leader"', 'female', '49', '0', '0', '17465', '25.9292', 'D17', 'S\n']
    0 797
    1 1
    2 1
    3 " Dr. Alice (Farnham) Leader"
    4 female
    5 49
    6 0
    7 0
    8 17465
    9 25.9292
    10 D17
    11 S
    
    ----------------------------
    ['798', '1', '3', '" Mrs. Mara Osman"', 'female', '31', '0', '0', '349244', '8.6833', '', 'S\n']
    0 798
    1 1
    2 3
    3 " Mrs. Mara Osman"
    4 female
    5 31
    6 0
    7 0
    8 349244
    9 8.6833
    10 
    11 S
    
    ----------------------------
    ['799', '0', '3', '" Mr. Yousseff Ibrahim Shawah"', 'male', '30', '0', '0', '2685', '7.2292', '', 'C\n']
    0 799
    1 0
    2 3
    3 " Mr. Yousseff Ibrahim Shawah"
    4 male
    5 30
    6 0
    7 0
    8 2685
    9 7.2292
    10 
    11 C
    
    ----------------------------
    ['800', '0', '3', '" Mrs. Jean Baptiste (Rosalie Paula Govaert) Van Impe"', 'female', '30', '1', '1', '345773', '24.15', '', 'S\n']
    0 800
    1 0
    2 3
    3 " Mrs. Jean Baptiste (Rosalie Paula Govaert) Van Impe"
    4 female
    5 30
    6 1
    7 1
    8 345773
    9 24.15
    10 
    11 S
    
    ----------------------------
    ['801', '0', '2', '" Mr. Martin Ponesell"', 'male', '34', '0', '0', '250647', '13', '', 'S\n']
    0 801
    1 0
    2 2
    3 " Mr. Martin Ponesell"
    4 male
    5 34
    6 0
    7 0
    8 250647
    9 13
    10 
    11 S
    
    ----------------------------
    ['802', '1', '2', '" Mrs. Harvey (Charlotte Annie Tate) Collyer"', 'female', '31', '1', '1', 'C.A. 31921', '26.25', '', 'S\n']
    0 802
    1 1
    2 2
    3 " Mrs. Harvey (Charlotte Annie Tate) Collyer"
    4 female
    5 31
    6 1
    7 1
    8 C.A. 31921
    9 26.25
    10 
    11 S
    
    ----------------------------
    ['803', '1', '1', '" Master. William Thornton II Carter"', 'male', '11', '1', '2', '113760', '120', 'B96 B98', 'S\n']
    0 803
    1 1
    2 1
    3 " Master. William Thornton II Carter"
    4 male
    5 11
    6 1
    7 2
    8 113760
    9 120
    10 B96 B98
    11 S
    
    ----------------------------
    ['804', '1', '3', '" Master. Assad Alexander Thomas"', 'male', '0.42', '0', '1', '2625', '8.5167', '', 'C\n']
    0 804
    1 1
    2 3
    3 " Master. Assad Alexander Thomas"
    4 male
    5 0.42
    6 0
    7 1
    8 2625
    9 8.5167
    10 
    11 C
    
    ----------------------------
    ['805', '1', '3', '" Mr. Oskar Arvid Hedman"', 'male', '27', '0', '0', '347089', '6.975', '', 'S\n']
    0 805
    1 1
    2 3
    3 " Mr. Oskar Arvid Hedman"
    4 male
    5 27
    6 0
    7 0
    8 347089
    9 6.975
    10 
    11 S
    
    ----------------------------
    ['806', '0', '3', '" Mr. Karl Johan Johansson"', 'male', '31', '0', '0', '347063', '7.775', '', 'S\n']
    0 806
    1 0
    2 3
    3 " Mr. Karl Johan Johansson"
    4 male
    5 31
    6 0
    7 0
    8 347063
    9 7.775
    10 
    11 S
    
    ----------------------------
    ['807', '0', '1', '" Mr. Thomas Jr Andrews"', 'male', '39', '0', '0', '112050', '0', 'A36', 'S\n']
    0 807
    1 0
    2 1
    3 " Mr. Thomas Jr Andrews"
    4 male
    5 39
    6 0
    7 0
    8 112050
    9 0
    10 A36
    11 S
    
    ----------------------------
    ['808', '0', '3', '" Miss. Ellen Natalia Pettersson"', 'female', '18', '0', '0', '347087', '7.775', '', 'S\n']
    0 808
    1 0
    2 3
    3 " Miss. Ellen Natalia Pettersson"
    4 female
    5 18
    6 0
    7 0
    8 347087
    9 7.775
    10 
    11 S
    
    ----------------------------
    ['809', '0', '2', '" Mr. August Meyer"', 'male', '39', '0', '0', '248723', '13', '', 'S\n']
    0 809
    1 0
    2 2
    3 " Mr. August Meyer"
    4 male
    5 39
    6 0
    7 0
    8 248723
    9 13
    10 
    11 S
    
    ----------------------------
    ['810', '1', '1', '" Mrs. Norman Campbell (Bertha Griggs) Chambers"', 'female', '33', '1', '0', '113806', '53.1', 'E8', 'S\n']
    0 810
    1 1
    2 1
    3 " Mrs. Norman Campbell (Bertha Griggs) Chambers"
    4 female
    5 33
    6 1
    7 0
    8 113806
    9 53.1
    10 E8
    11 S
    
    ----------------------------
    ['811', '0', '3', '" Mr. William Alexander"', 'male', '26', '0', '0', '3474', '7.8875', '', 'S\n']
    0 811
    1 0
    2 3
    3 " Mr. William Alexander"
    4 male
    5 26
    6 0
    7 0
    8 3474
    9 7.8875
    10 
    11 S
    
    ----------------------------
    ['812', '0', '3', '" Mr. James Lester"', 'male', '39', '0', '0', 'A/4 48871', '24.15', '', 'S\n']
    0 812
    1 0
    2 3
    3 " Mr. James Lester"
    4 male
    5 39
    6 0
    7 0
    8 A/4 48871
    9 24.15
    10 
    11 S
    
    ----------------------------
    ['813', '0', '2', '" Mr. Richard James Slemen"', 'male', '35', '0', '0', '28206', '10.5', '', 'S\n']
    0 813
    1 0
    2 2
    3 " Mr. Richard James Slemen"
    4 male
    5 35
    6 0
    7 0
    8 28206
    9 10.5
    10 
    11 S
    
    ----------------------------
    ['814', '0', '3', '" Miss. Ebba Iris Alfrida Andersson"', 'female', '6', '4', '2', '347082', '31.275', '', 'S\n']
    0 814
    1 0
    2 3
    3 " Miss. Ebba Iris Alfrida Andersson"
    4 female
    5 6
    6 4
    7 2
    8 347082
    9 31.275
    10 
    11 S
    
    ----------------------------
    ['815', '0', '3', '" Mr. Ernest Portage Tomlin"', 'male', '30.5', '0', '0', '364499', '8.05', '', 'S\n']
    0 815
    1 0
    2 3
    3 " Mr. Ernest Portage Tomlin"
    4 male
    5 30.5
    6 0
    7 0
    8 364499
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['816', '0', '1', '" Mr. Richard Fry"', 'male', '', '0', '0', '112058', '0', 'B102', 'S\n']
    0 816
    1 0
    2 1
    3 " Mr. Richard Fry"
    4 male
    5 
    6 0
    7 0
    8 112058
    9 0
    10 B102
    11 S
    
    ----------------------------
    ['817', '0', '3', '" Miss. Wendla Maria Heininen"', 'female', '23', '0', '0', 'STON/O2. 3101290', '7.925', '', 'S\n']
    0 817
    1 0
    2 3
    3 " Miss. Wendla Maria Heininen"
    4 female
    5 23
    6 0
    7 0
    8 STON/O2. 3101290
    9 7.925
    10 
    11 S
    
    ----------------------------
    ['818', '0', '2', '" Mr. Albert Mallet"', 'male', '31', '1', '1', 'S.C./PARIS 2079', '37.0042', '', 'C\n']
    0 818
    1 0
    2 2
    3 " Mr. Albert Mallet"
    4 male
    5 31
    6 1
    7 1
    8 S.C./PARIS 2079
    9 37.0042
    10 
    11 C
    
    ----------------------------
    ['819', '0', '3', '" Mr. John Fredrik Alexander Holm"', 'male', '43', '0', '0', 'C 7075', '6.45', '', 'S\n']
    0 819
    1 0
    2 3
    3 " Mr. John Fredrik Alexander Holm"
    4 male
    5 43
    6 0
    7 0
    8 C 7075
    9 6.45
    10 
    11 S
    
    ----------------------------
    ['820', '0', '3', '" Master. Karl Thorsten Skoog"', 'male', '10', '3', '2', '347088', '27.9', '', 'S\n']
    0 820
    1 0
    2 3
    3 " Master. Karl Thorsten Skoog"
    4 male
    5 10
    6 3
    7 2
    8 347088
    9 27.9
    10 
    11 S
    
    ----------------------------
    ['821', '1', '1', '" Mrs. Charles Melville (Clara Jennings Gregg) Hays"', 'female', '52', '1', '1', '12749', '93.5', 'B69', 'S\n']
    0 821
    1 1
    2 1
    3 " Mrs. Charles Melville (Clara Jennings Gregg) Hays"
    4 female
    5 52
    6 1
    7 1
    8 12749
    9 93.5
    10 B69
    11 S
    
    ----------------------------
    ['822', '1', '3', '" Mr. Nikola Lulic"', 'male', '27', '0', '0', '315098', '8.6625', '', 'S\n']
    0 822
    1 1
    2 3
    3 " Mr. Nikola Lulic"
    4 male
    5 27
    6 0
    7 0
    8 315098
    9 8.6625
    10 
    11 S
    
    ----------------------------
    ['823', '0', '1', '" Jonkheer. John George Reuchlin"', 'male', '38', '0', '0', '19972', '0', '', 'S\n']
    0 823
    1 0
    2 1
    3 " Jonkheer. John George Reuchlin"
    4 male
    5 38
    6 0
    7 0
    8 19972
    9 0
    10 
    11 S
    
    ----------------------------
    ['824', '1', '3', '" Mrs. (Beila) Moor"', 'female', '27', '0', '1', '392096', '12.475', 'E121', 'S\n']
    0 824
    1 1
    2 3
    3 " Mrs. (Beila) Moor"
    4 female
    5 27
    6 0
    7 1
    8 392096
    9 12.475
    10 E121
    11 S
    
    ----------------------------
    ['825', '0', '3', '" Master. Urho Abraham Panula"', 'male', '2', '4', '1', '3101295', '39.6875', '', 'S\n']
    0 825
    1 0
    2 3
    3 " Master. Urho Abraham Panula"
    4 male
    5 2
    6 4
    7 1
    8 3101295
    9 39.6875
    10 
    11 S
    
    ----------------------------
    ['826', '0', '3', '" Mr. John Flynn"', 'male', '', '0', '0', '368323', '6.95', '', 'Q\n']
    0 826
    1 0
    2 3
    3 " Mr. John Flynn"
    4 male
    5 
    6 0
    7 0
    8 368323
    9 6.95
    10 
    11 Q
    
    ----------------------------
    ['827', '0', '3', '" Mr. Len Lam"', 'male', '', '0', '0', '1601', '56.4958', '', 'S\n']
    0 827
    1 0
    2 3
    3 " Mr. Len Lam"
    4 male
    5 
    6 0
    7 0
    8 1601
    9 56.4958
    10 
    11 S
    
    ----------------------------
    ['828', '1', '2', '" Master. Andre Mallet"', 'male', '1', '0', '2', 'S.C./PARIS 2079', '37.0042', '', 'C\n']
    0 828
    1 1
    2 2
    3 " Master. Andre Mallet"
    4 male
    5 1
    6 0
    7 2
    8 S.C./PARIS 2079
    9 37.0042
    10 
    11 C
    
    ----------------------------
    ['829', '1', '3', '" Mr. Thomas Joseph McCormack"', 'male', '', '0', '0', '367228', '7.75', '', 'Q\n']
    0 829
    1 1
    2 3
    3 " Mr. Thomas Joseph McCormack"
    4 male
    5 
    6 0
    7 0
    8 367228
    9 7.75
    10 
    11 Q
    
    ----------------------------
    ['830', '1', '1', '" Mrs. George Nelson (Martha Evelyn) Stone"', 'female', '62', '0', '0', '113572', '80', 'B28', '\n']
    0 830
    1 1
    2 1
    3 " Mrs. George Nelson (Martha Evelyn) Stone"
    4 female
    5 62
    6 0
    7 0
    8 113572
    9 80
    10 B28
    11 
    
    ----------------------------
    ['831', '1', '3', '" Mrs. Antoni (Selini Alexander) Yasbeck"', 'female', '15', '1', '0', '2659', '14.4542', '', 'C\n']
    0 831
    1 1
    2 3
    3 " Mrs. Antoni (Selini Alexander) Yasbeck"
    4 female
    5 15
    6 1
    7 0
    8 2659
    9 14.4542
    10 
    11 C
    
    ----------------------------
    ['832', '1', '2', '" Master. George Sibley Richards"', 'male', '0.83', '1', '1', '29106', '18.75', '', 'S\n']
    0 832
    1 1
    2 2
    3 " Master. George Sibley Richards"
    4 male
    5 0.83
    6 1
    7 1
    8 29106
    9 18.75
    10 
    11 S
    
    ----------------------------
    ['833', '0', '3', '" Mr. Amin Saad"', 'male', '', '0', '0', '2671', '7.2292', '', 'C\n']
    0 833
    1 0
    2 3
    3 " Mr. Amin Saad"
    4 male
    5 
    6 0
    7 0
    8 2671
    9 7.2292
    10 
    11 C
    
    ----------------------------
    ['834', '0', '3', '" Mr. Albert Augustsson"', 'male', '23', '0', '0', '347468', '7.8542', '', 'S\n']
    0 834
    1 0
    2 3
    3 " Mr. Albert Augustsson"
    4 male
    5 23
    6 0
    7 0
    8 347468
    9 7.8542
    10 
    11 S
    
    ----------------------------
    ['835', '0', '3', '" Mr. Owen George Allum"', 'male', '18', '0', '0', '2223', '8.3', '', 'S\n']
    0 835
    1 0
    2 3
    3 " Mr. Owen George Allum"
    4 male
    5 18
    6 0
    7 0
    8 2223
    9 8.3
    10 
    11 S
    
    ----------------------------
    ['836', '1', '1', '" Miss. Sara Rebecca Compton"', 'female', '39', '1', '1', 'PC 17756', '83.1583', 'E49', 'C\n']
    0 836
    1 1
    2 1
    3 " Miss. Sara Rebecca Compton"
    4 female
    5 39
    6 1
    7 1
    8 PC 17756
    9 83.1583
    10 E49
    11 C
    
    ----------------------------
    ['837', '0', '3', '" Mr. Jakob Pasic"', 'male', '21', '0', '0', '315097', '8.6625', '', 'S\n']
    0 837
    1 0
    2 3
    3 " Mr. Jakob Pasic"
    4 male
    5 21
    6 0
    7 0
    8 315097
    9 8.6625
    10 
    11 S
    
    ----------------------------
    ['838', '0', '3', '" Mr. Maurice Sirota"', 'male', '', '0', '0', '392092', '8.05', '', 'S\n']
    0 838
    1 0
    2 3
    3 " Mr. Maurice Sirota"
    4 male
    5 
    6 0
    7 0
    8 392092
    9 8.05
    10 
    11 S
    
    ----------------------------
    ['839', '1', '3', '" Mr. Chang Chip"', 'male', '32', '0', '0', '1601', '56.4958', '', 'S\n']
    0 839
    1 1
    2 3
    3 " Mr. Chang Chip"
    4 male
    5 32
    6 0
    7 0
    8 1601
    9 56.4958
    10 
    11 S
    
    ----------------------------
    ['840', '1', '1', '" Mr. Pierre Marechal"', 'male', '', '0', '0', '11774', '29.7', 'C47', 'C\n']
    0 840
    1 1
    2 1
    3 " Mr. Pierre Marechal"
    4 male
    5 
    6 0
    7 0
    8 11774
    9 29.7
    10 C47
    11 C
    
    ----------------------------
    ['841', '0', '3', '" Mr. Ilmari Rudolf Alhomaki"', 'male', '20', '0', '0', 'SOTON/O2 3101287', '7.925', '', 'S\n']
    0 841
    1 0
    2 3
    3 " Mr. Ilmari Rudolf Alhomaki"
    4 male
    5 20
    6 0
    7 0
    8 SOTON/O2 3101287
    9 7.925
    10 
    11 S
    
    ----------------------------
    ['842', '0', '2', '" Mr. Thomas Charles Mudd"', 'male', '16', '0', '0', 'S.O./P.P. 3', '10.5', '', 'S\n']
    0 842
    1 0
    2 2
    3 " Mr. Thomas Charles Mudd"
    4 male
    5 16
    6 0
    7 0
    8 S.O./P.P. 3
    9 10.5
    10 
    11 S
    
    ----------------------------
    ['843', '1', '1', '" Miss. Augusta Serepeca"', 'female', '30', '0', '0', '113798', '31', '', 'C\n']
    0 843
    1 1
    2 1
    3 " Miss. Augusta Serepeca"
    4 female
    5 30
    6 0
    7 0
    8 113798
    9 31
    10 
    11 C
    
    ----------------------------
    ['844', '0', '3', '" Mr. Peter L Lemberopolous"', 'male', '34.5', '0', '0', '2683', '6.4375', '', 'C\n']
    0 844
    1 0
    2 3
    3 " Mr. Peter L Lemberopolous"
    4 male
    5 34.5
    6 0
    7 0
    8 2683
    9 6.4375
    10 
    11 C
    
    ----------------------------
    ['845', '0', '3', '" Mr. Jeso Culumovic"', 'male', '17', '0', '0', '315090', '8.6625', '', 'S\n']
    0 845
    1 0
    2 3
    3 " Mr. Jeso Culumovic"
    4 male
    5 17
    6 0
    7 0
    8 315090
    9 8.6625
    10 
    11 S
    
    ----------------------------
    ['846', '0', '3', '" Mr. Anthony Abbing"', 'male', '42', '0', '0', 'C.A. 5547', '7.55', '', 'S\n']
    0 846
    1 0
    2 3
    3 " Mr. Anthony Abbing"
    4 male
    5 42
    6 0
    7 0
    8 C.A. 5547
    9 7.55
    10 
    11 S
    
    ----------------------------
    ['847', '0', '3', '" Mr. Douglas Bullen Sage"', 'male', '', '8', '2', 'CA. 2343', '69.55', '', 'S\n']
    0 847
    1 0
    2 3
    3 " Mr. Douglas Bullen Sage"
    4 male
    5 
    6 8
    7 2
    8 CA. 2343
    9 69.55
    10 
    11 S
    
    ----------------------------
    ['848', '0', '3', '" Mr. Marin Markoff"', 'male', '35', '0', '0', '349213', '7.8958', '', 'C\n']
    0 848
    1 0
    2 3
    3 " Mr. Marin Markoff"
    4 male
    5 35
    6 0
    7 0
    8 349213
    9 7.8958
    10 
    11 C
    
    ----------------------------
    ['849', '0', '2', '" Rev. John Harper"', 'male', '28', '0', '1', '248727', '33', '', 'S\n']
    0 849
    1 0
    2 2
    3 " Rev. John Harper"
    4 male
    5 28
    6 0
    7 1
    8 248727
    9 33
    10 
    11 S
    
    ----------------------------
    ['850', '1', '1', '" Mrs. Samuel L (Edwiga Grabowska) Goldenberg"', 'female', '', '1', '0', '17453', '89.1042', 'C92', 'C\n']
    0 850
    1 1
    2 1
    3 " Mrs. Samuel L (Edwiga Grabowska) Goldenberg"
    4 female
    5 
    6 1
    7 0
    8 17453
    9 89.1042
    10 C92
    11 C
    
    ----------------------------
    ['851', '0', '3', '" Master. Sigvard Harald Elias Andersson"', 'male', '4', '4', '2', '347082', '31.275', '', 'S\n']
    0 851
    1 0
    2 3
    3 " Master. Sigvard Harald Elias Andersson"
    4 male
    5 4
    6 4
    7 2
    8 347082
    9 31.275
    10 
    11 S
    
    ----------------------------
    ['852', '0', '3', '" Mr. Johan Svensson"', 'male', '74', '0', '0', '347060', '7.775', '', 'S\n']
    0 852
    1 0
    2 3
    3 " Mr. Johan Svensson"
    4 male
    5 74
    6 0
    7 0
    8 347060
    9 7.775
    10 
    11 S
    
    ----------------------------
    ['853', '0', '3', '" Miss. Nourelain Boulos"', 'female', '9', '1', '1', '2678', '15.2458', '', 'C\n']
    0 853
    1 0
    2 3
    3 " Miss. Nourelain Boulos"
    4 female
    5 9
    6 1
    7 1
    8 2678
    9 15.2458
    10 
    11 C
    
    ----------------------------
    ['854', '1', '1', '" Miss. Mary Conover Lines"', 'female', '16', '0', '1', 'PC 17592', '39.4', 'D28', 'S\n']
    0 854
    1 1
    2 1
    3 " Miss. Mary Conover Lines"
    4 female
    5 16
    6 0
    7 1
    8 PC 17592
    9 39.4
    10 D28
    11 S
    
    ----------------------------
    ['855', '0', '2', '" Mrs. Ernest Courtenay (Lilian Hughes) Carter"', 'female', '44', '1', '0', '244252', '26', '', 'S\n']
    0 855
    1 0
    2 2
    3 " Mrs. Ernest Courtenay (Lilian Hughes) Carter"
    4 female
    5 44
    6 1
    7 0
    8 244252
    9 26
    10 
    11 S
    
    ----------------------------
    ['856', '1', '3', '" Mrs. Sam (Leah Rosen) Aks"', 'female', '18', '0', '1', '392091', '9.35', '', 'S\n']
    0 856
    1 1
    2 3
    3 " Mrs. Sam (Leah Rosen) Aks"
    4 female
    5 18
    6 0
    7 1
    8 392091
    9 9.35
    10 
    11 S
    
    ----------------------------
    ['857', '1', '1', '" Mrs. George Dennick (Mary Hitchcock) Wick"', 'female', '45', '1', '1', '36928', '164.8667', '', 'S\n']
    0 857
    1 1
    2 1
    3 " Mrs. George Dennick (Mary Hitchcock) Wick"
    4 female
    5 45
    6 1
    7 1
    8 36928
    9 164.8667
    10 
    11 S
    
    ----------------------------
    ['858', '1', '1', '" Mr. Peter Denis  Daly"', 'male', '51', '0', '0', '113055', '26.55', 'E17', 'S\n']
    0 858
    1 1
    2 1
    3 " Mr. Peter Denis  Daly"
    4 male
    5 51
    6 0
    7 0
    8 113055
    9 26.55
    10 E17
    11 S
    
    ----------------------------
    ['859', '1', '3', '" Mrs. Solomon (Latifa Qurban) Baclini"', 'female', '24', '0', '3', '2666', '19.2583', '', 'C\n']
    0 859
    1 1
    2 3
    3 " Mrs. Solomon (Latifa Qurban) Baclini"
    4 female
    5 24
    6 0
    7 3
    8 2666
    9 19.2583
    10 
    11 C
    
    ----------------------------
    ['860', '0', '3', '" Mr. Raihed Razi"', 'male', '', '0', '0', '2629', '7.2292', '', 'C\n']
    0 860
    1 0
    2 3
    3 " Mr. Raihed Razi"
    4 male
    5 
    6 0
    7 0
    8 2629
    9 7.2292
    10 
    11 C
    
    ----------------------------
    ['861', '0', '3', '" Mr. Claus Peter Hansen"', 'male', '41', '2', '0', '350026', '14.1083', '', 'S\n']
    0 861
    1 0
    2 3
    3 " Mr. Claus Peter Hansen"
    4 male
    5 41
    6 2
    7 0
    8 350026
    9 14.1083
    10 
    11 S
    
    ----------------------------
    ['862', '0', '2', '" Mr. Frederick Edward Giles"', 'male', '21', '1', '0', '28134', '11.5', '', 'S\n']
    0 862
    1 0
    2 2
    3 " Mr. Frederick Edward Giles"
    4 male
    5 21
    6 1
    7 0
    8 28134
    9 11.5
    10 
    11 S
    
    ----------------------------
    ['863', '1', '1', '" Mrs. Frederick Joel (Margaret Welles Barron) Swift"', 'female', '48', '0', '0', '17466', '25.9292', 'D17', 'S\n']
    0 863
    1 1
    2 1
    3 " Mrs. Frederick Joel (Margaret Welles Barron) Swift"
    4 female
    5 48
    6 0
    7 0
    8 17466
    9 25.9292
    10 D17
    11 S
    
    ----------------------------
    ['864', '0', '3', '" Miss. Dorothy Edith ""Dolly"" Sage"', 'female', '', '8', '2', 'CA. 2343', '69.55', '', 'S\n']
    0 864
    1 0
    2 3
    3 " Miss. Dorothy Edith ""Dolly"" Sage"
    4 female
    5 
    6 8
    7 2
    8 CA. 2343
    9 69.55
    10 
    11 S
    
    ----------------------------
    ['865', '0', '2', '" Mr. John William Gill"', 'male', '24', '0', '0', '233866', '13', '', 'S\n']
    0 865
    1 0
    2 2
    3 " Mr. John William Gill"
    4 male
    5 24
    6 0
    7 0
    8 233866
    9 13
    10 
    11 S
    
    ----------------------------
    ['866', '1', '2', '" Mrs. (Karolina) Bystrom"', 'female', '42', '0', '0', '236852', '13', '', 'S\n']
    0 866
    1 1
    2 2
    3 " Mrs. (Karolina) Bystrom"
    4 female
    5 42
    6 0
    7 0
    8 236852
    9 13
    10 
    11 S
    
    ----------------------------
    ['867', '1', '2', '" Miss. Asuncion Duran y More"', 'female', '27', '1', '0', 'SC/PARIS 2149', '13.8583', '', 'C\n']
    0 867
    1 1
    2 2
    3 " Miss. Asuncion Duran y More"
    4 female
    5 27
    6 1
    7 0
    8 SC/PARIS 2149
    9 13.8583
    10 
    11 C
    
    ----------------------------
    ['868', '0', '1', '" Mr. Washington Augustus II Roebling"', 'male', '31', '0', '0', 'PC 17590', '50.4958', 'A24', 'S\n']
    0 868
    1 0
    2 1
    3 " Mr. Washington Augustus II Roebling"
    4 male
    5 31
    6 0
    7 0
    8 PC 17590
    9 50.4958
    10 A24
    11 S
    
    ----------------------------
    ['869', '0', '3', '" Mr. Philemon van Melkebeke"', 'male', '', '0', '0', '345777', '9.5', '', 'S\n']
    0 869
    1 0
    2 3
    3 " Mr. Philemon van Melkebeke"
    4 male
    5 
    6 0
    7 0
    8 345777
    9 9.5
    10 
    11 S
    
    ----------------------------
    ['870', '1', '3', '" Master. Harold Theodor Johnson"', 'male', '4', '1', '1', '347742', '11.1333', '', 'S\n']
    0 870
    1 1
    2 3
    3 " Master. Harold Theodor Johnson"
    4 male
    5 4
    6 1
    7 1
    8 347742
    9 11.1333
    10 
    11 S
    
    ----------------------------
    ['871', '0', '3', '" Mr. Cerin Balkic"', 'male', '26', '0', '0', '349248', '7.8958', '', 'S\n']
    0 871
    1 0
    2 3
    3 " Mr. Cerin Balkic"
    4 male
    5 26
    6 0
    7 0
    8 349248
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['872', '1', '1', '" Mrs. Richard Leonard (Sallie Monypeny) Beckwith"', 'female', '47', '1', '1', '11751', '52.5542', 'D35', 'S\n']
    0 872
    1 1
    2 1
    3 " Mrs. Richard Leonard (Sallie Monypeny) Beckwith"
    4 female
    5 47
    6 1
    7 1
    8 11751
    9 52.5542
    10 D35
    11 S
    
    ----------------------------
    ['873', '0', '1', '" Mr. Frans Olof Carlsson"', 'male', '33', '0', '0', '695', '5', 'B51 B53 B55', 'S\n']
    0 873
    1 0
    2 1
    3 " Mr. Frans Olof Carlsson"
    4 male
    5 33
    6 0
    7 0
    8 695
    9 5
    10 B51 B53 B55
    11 S
    
    ----------------------------
    ['874', '0', '3', '" Mr. Victor Vander Cruyssen"', 'male', '47', '0', '0', '345765', '9', '', 'S\n']
    0 874
    1 0
    2 3
    3 " Mr. Victor Vander Cruyssen"
    4 male
    5 47
    6 0
    7 0
    8 345765
    9 9
    10 
    11 S
    
    ----------------------------
    ['875', '1', '2', '" Mrs. Samuel (Hannah Wizosky) Abelson"', 'female', '28', '1', '0', 'P/PP 3381', '24', '', 'C\n']
    0 875
    1 1
    2 2
    3 " Mrs. Samuel (Hannah Wizosky) Abelson"
    4 female
    5 28
    6 1
    7 0
    8 P/PP 3381
    9 24
    10 
    11 C
    
    ----------------------------
    ['876', '1', '3', '" Miss. Adele Kiamie ""Jane"" Najib"', 'female', '15', '0', '0', '2667', '7.225', '', 'C\n']
    0 876
    1 1
    2 3
    3 " Miss. Adele Kiamie ""Jane"" Najib"
    4 female
    5 15
    6 0
    7 0
    8 2667
    9 7.225
    10 
    11 C
    
    ----------------------------
    ['877', '0', '3', '" Mr. Alfred Ossian Gustafsson"', 'male', '20', '0', '0', '7534', '9.8458', '', 'S\n']
    0 877
    1 0
    2 3
    3 " Mr. Alfred Ossian Gustafsson"
    4 male
    5 20
    6 0
    7 0
    8 7534
    9 9.8458
    10 
    11 S
    
    ----------------------------
    ['878', '0', '3', '" Mr. Nedelio Petroff"', 'male', '19', '0', '0', '349212', '7.8958', '', 'S\n']
    0 878
    1 0
    2 3
    3 " Mr. Nedelio Petroff"
    4 male
    5 19
    6 0
    7 0
    8 349212
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['879', '0', '3', '" Mr. Kristo Laleff"', 'male', '', '0', '0', '349217', '7.8958', '', 'S\n']
    0 879
    1 0
    2 3
    3 " Mr. Kristo Laleff"
    4 male
    5 
    6 0
    7 0
    8 349217
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['880', '1', '1', '" Mrs. Thomas Jr (Lily Alexenia Wilson) Potter"', 'female', '56', '0', '1', '11767', '83.1583', 'C50', 'C\n']
    0 880
    1 1
    2 1
    3 " Mrs. Thomas Jr (Lily Alexenia Wilson) Potter"
    4 female
    5 56
    6 0
    7 1
    8 11767
    9 83.1583
    10 C50
    11 C
    
    ----------------------------
    ['881', '1', '2', '" Mrs. William (Imanita Parrish Hall) Shelley"', 'female', '25', '0', '1', '230433', '26', '', 'S\n']
    0 881
    1 1
    2 2
    3 " Mrs. William (Imanita Parrish Hall) Shelley"
    4 female
    5 25
    6 0
    7 1
    8 230433
    9 26
    10 
    11 S
    
    ----------------------------
    ['882', '0', '3', '" Mr. Johann Markun"', 'male', '33', '0', '0', '349257', '7.8958', '', 'S\n']
    0 882
    1 0
    2 3
    3 " Mr. Johann Markun"
    4 male
    5 33
    6 0
    7 0
    8 349257
    9 7.8958
    10 
    11 S
    
    ----------------------------
    ['883', '0', '3', '" Miss. Gerda Ulrika Dahlberg"', 'female', '22', '0', '0', '7552', '10.5167', '', 'S\n']
    0 883
    1 0
    2 3
    3 " Miss. Gerda Ulrika Dahlberg"
    4 female
    5 22
    6 0
    7 0
    8 7552
    9 10.5167
    10 
    11 S
    
    ----------------------------
    ['884', '0', '2', '" Mr. Frederick James Banfield"', 'male', '28', '0', '0', 'C.A./SOTON 34068', '10.5', '', 'S\n']
    0 884
    1 0
    2 2
    3 " Mr. Frederick James Banfield"
    4 male
    5 28
    6 0
    7 0
    8 C.A./SOTON 34068
    9 10.5
    10 
    11 S
    
    ----------------------------
    ['885', '0', '3', '" Mr. Henry Jr Sutehall"', 'male', '25', '0', '0', 'SOTON/OQ 392076', '7.05', '', 'S\n']
    0 885
    1 0
    2 3
    3 " Mr. Henry Jr Sutehall"
    4 male
    5 25
    6 0
    7 0
    8 SOTON/OQ 392076
    9 7.05
    10 
    11 S
    
    ----------------------------
    ['886', '0', '3', '" Mrs. William (Margaret Norton) Rice"', 'female', '39', '0', '5', '382652', '29.125', '', 'Q\n']
    0 886
    1 0
    2 3
    3 " Mrs. William (Margaret Norton) Rice"
    4 female
    5 39
    6 0
    7 5
    8 382652
    9 29.125
    10 
    11 Q
    
    ----------------------------
    ['887', '0', '2', '" Rev. Juozas Montvila"', 'male', '27', '0', '0', '211536', '13', '', 'S\n']
    0 887
    1 0
    2 2
    3 " Rev. Juozas Montvila"
    4 male
    5 27
    6 0
    7 0
    8 211536
    9 13
    10 
    11 S
    
    ----------------------------
    ['888', '1', '1', '" Miss. Margaret Edith Graham"', 'female', '19', '0', '0', '112053', '30', 'B42', 'S\n']
    0 888
    1 1
    2 1
    3 " Miss. Margaret Edith Graham"
    4 female
    5 19
    6 0
    7 0
    8 112053
    9 30
    10 B42
    11 S
    
    ----------------------------
    ['889', '0', '3', '" Miss. Catherine Helen ""Carrie"" Johnston"', 'female', '', '1', '2', 'W./C. 6607', '23.45', '', 'S\n']
    0 889
    1 0
    2 3
    3 " Miss. Catherine Helen ""Carrie"" Johnston"
    4 female
    5 
    6 1
    7 2
    8 W./C. 6607
    9 23.45
    10 
    11 S
    
    ----------------------------
    ['890', '1', '1', '" Mr. Karl Howell Behr"', 'male', '26', '0', '0', '111369', '30', 'C148', 'C\n']
    0 890
    1 1
    2 1
    3 " Mr. Karl Howell Behr"
    4 male
    5 26
    6 0
    7 0
    8 111369
    9 30
    10 C148
    11 C
    
    ----------------------------
    ['891', '0', '3', '" Mr. Patrick Dooley"', 'male', '32', '0', '0', '370376', '7.75', '', 'Q\n']
    0 891
    1 0
    2 3
    3 " Mr. Patrick Dooley"
    4 male
    5 32
    6 0
    7 0
    8 370376
    9 7.75
    10 
    11 Q
    
    ----------------------------
    

## linhas = Todo o arquivo, sem nenhum tratamento, onde cada indice é linha, por exemplo linha[0]

## colunas = ['PassengerId', 'Survived', 'Pclass', 'Name', 'Sex', 'Age', 'SibSp', 'Parch', 'Ticket', 'Fare', 'Cabin', 'Embarked\n']

## dados =['1', '0', '3', '"Braund', ' Mr. Owen Harris"', 'male', '22', '1', '0', 'A/5 21171', '7.25', '', 'S\n']

## titanic_dados = o dicionario com as chaves (colunas) sem os valores



```python
for passageiro in dados_tratados:
    for indice, dado in enumerate(passageiro):
        coluna = colunas[indice]
        titanic_dados[coluna].append(dado)
```


```python
titanic_dados["Age"][0]
```




    '22'




```python
for dado in titanic_dados["Age"]:
    print(dado)
```

    22
    38
    26
    35
    35
    
    54
    2
    27
    14
    4
    58
    20
    39
    14
    55
    2
    
    31
    
    35
    34
    15
    28
    8
    38
    
    19
    
    
    40
    
    
    66
    28
    42
    
    21
    18
    14
    40
    27
    
    3
    19
    
    
    
    
    18
    7
    21
    49
    29
    65
    
    21
    28.5
    5
    11
    22
    38
    45
    4
    
    
    29
    19
    17
    26
    32
    16
    21
    26
    32
    25
    
    
    0.83
    30
    22
    29
    
    28
    17
    33
    16
    
    23
    24
    29
    20
    46
    26
    59
    
    71
    23
    34
    34
    28
    
    21
    33
    37
    28
    21
    
    38
    
    47
    14.5
    22
    20
    17
    21
    70.5
    29
    24
    2
    21
    
    32.5
    32.5
    54
    12
    
    24
    
    45
    33
    20
    47
    29
    25
    23
    19
    37
    16
    24
    
    22
    24
    19
    18
    19
    27
    9
    36.5
    42
    51
    22
    55.5
    40.5
    
    51
    16
    30
    
    
    44
    40
    26
    17
    1
    9
    
    45
    
    28
    61
    4
    1
    21
    56
    18
    
    50
    30
    36
    
    
    9
    1
    4
    
    
    45
    40
    36
    32
    19
    19
    3
    44
    58
    
    42
    
    24
    28
    
    34
    45.5
    18
    2
    32
    26
    16
    40
    24
    35
    22
    30
    
    31
    27
    42
    32
    30
    16
    27
    51
    
    38
    22
    19
    20.5
    18
    
    35
    29
    59
    5
    24
    
    44
    8
    19
    33
    
    
    29
    22
    30
    44
    25
    24
    37
    54
    
    29
    62
    30
    41
    29
    
    30
    35
    50
    
    3
    52
    40
    
    36
    16
    25
    58
    35
    
    25
    41
    37
    
    63
    45
    
    7
    35
    65
    28
    16
    19
    
    33
    30
    22
    42
    22
    26
    19
    36
    24
    24
    
    23.5
    2
    
    50
    
    
    19
    
    
    0.92
    
    17
    30
    30
    24
    18
    26
    28
    43
    26
    24
    54
    31
    40
    22
    27
    30
    22
    
    36
    61
    36
    31
    16
    
    45.5
    38
    16
    
    
    29
    41
    45
    45
    2
    24
    28
    25
    36
    24
    40
    
    3
    42
    23
    
    15
    25
    
    28
    22
    38
    
    
    40
    29
    45
    35
    
    30
    60
    
    
    24
    25
    18
    19
    22
    3
    
    22
    27
    20
    19
    42
    1
    32
    35
    
    18
    1
    36
    
    17
    36
    21
    28
    23
    24
    22
    31
    46
    23
    28
    39
    26
    21
    28
    20
    34
    51
    3
    21
    
    
    
    33
    
    44
    
    34
    18
    30
    10
    
    21
    29
    28
    18
    
    28
    19
    
    32
    28
    
    42
    17
    50
    14
    21
    24
    64
    31
    45
    20
    25
    28
    
    4
    13
    34
    5
    52
    36
    
    30
    49
    
    29
    65
    
    50
    
    48
    34
    47
    48
    
    38
    
    56
    
    0.75
    
    38
    33
    23
    22
    
    34
    29
    22
    2
    9
    
    50
    63
    25
    
    35
    58
    30
    9
    
    21
    55
    71
    21
    
    54
    
    25
    24
    17
    21
    
    37
    16
    18
    33
    
    28
    26
    29
    
    36
    54
    24
    47
    34
    
    36
    32
    30
    22
    
    44
    
    40.5
    50
    
    39
    23
    2
    
    17
    
    30
    7
    45
    30
    
    22
    36
    9
    11
    32
    50
    64
    19
    
    33
    8
    17
    27
    
    22
    22
    62
    48
    
    39
    36
    
    40
    28
    
    
    24
    19
    29
    
    32
    62
    53
    36
    
    16
    19
    34
    39
    
    32
    25
    39
    54
    36
    
    18
    47
    60
    22
    
    35
    52
    47
    
    37
    36
    
    49
    
    49
    24
    
    
    44
    35
    36
    30
    27
    22
    40
    39
    
    
    
    35
    24
    34
    26
    4
    26
    27
    42
    20
    21
    21
    61
    57
    21
    26
    
    80
    51
    32
    
    9
    28
    32
    31
    41
    
    20
    24
    2
    
    0.75
    48
    19
    56
    
    23
    
    18
    21
    
    18
    24
    
    32
    23
    58
    50
    40
    47
    36
    20
    32
    25
    
    43
    
    40
    31
    70
    31
    
    18
    24.5
    18
    43
    36
    
    27
    20
    14
    60
    25
    14
    19
    18
    15
    31
    4
    
    25
    60
    52
    44
    
    49
    42
    18
    35
    18
    25
    26
    39
    45
    42
    22
    
    24
    
    48
    29
    52
    19
    38
    27
    
    33
    6
    17
    34
    50
    27
    20
    30
    
    25
    25
    29
    11
    
    23
    23
    28.5
    48
    35
    
    
    
    36
    21
    24
    31
    70
    16
    30
    19
    31
    4
    6
    33
    23
    48
    0.67
    28
    18
    34
    33
    
    41
    20
    36
    16
    51
    
    30.5
    
    32
    24
    48
    57
    
    54
    18
    
    5
    
    43
    13
    17
    29
    
    25
    25
    18
    8
    1
    46
    
    16
    
    
    25
    39
    49
    31
    30
    30
    34
    31
    11
    0.42
    27
    31
    39
    18
    39
    33
    26
    39
    35
    6
    30.5
    
    23
    31
    43
    10
    52
    27
    38
    27
    2
    
    
    1
    
    62
    15
    0.83
    
    23
    18
    39
    21
    
    32
    
    20
    16
    30
    34.5
    17
    42
    
    35
    28
    
    4
    74
    9
    16
    44
    18
    45
    51
    24
    
    41
    21
    48
    
    24
    42
    27
    31
    
    4
    26
    47
    33
    47
    28
    15
    20
    19
    
    56
    25
    33
    22
    28
    25
    39
    27
    19
    
    26
    32
    


```python
##converter idade em float e se estiver ausente, será -1
for indice, age in enumerate(titanic_dados["Age"]):
    if titanic_dados['Age'][indice] != '':
        titanic_dados['Age'][indice] = float(age)
    else:
        titanic_dados['Age'][indice] = -1
```


```python
print(max(titanic_dados['Age']))
```

    80.0
    


```python
print(min(titanic_dados['Age']))
```

    -1
    


```python
#Copiar todas as idades, exceto -1
lista_idade = []

for idade in titanic_dados["Age"]:
    if idade != -1:
        lista_idade.append(idade)
    
```


```python
def media(lista):
    soma_total  = sum(lista)
    quantidade = len(lista)
    return soma_total / quantidade

```


```python
print(media(lista_idade))
```

    29.69911764705882
    


```python
for idade in titanic_dados["Age"]:
    if idade == -1:
        titanic_dados.append(media)
```


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    <ipython-input-80-1087d7d0ec40> in <module>()
          1 for idade in titanic_dados["Age"]:
          2     if idade == -1:
    ----> 3         titanic_dados.append(media)
    

    AttributeError: 'dict' object has no attribute 'append'


# Pandas \o/


```python
titanic_dados['Age']
```




    [22.0,
     38.0,
     26.0,
     35.0,
     35.0,
     -1,
     54.0,
     2.0,
     27.0,
     14.0,
     4.0,
     58.0,
     20.0,
     39.0,
     14.0,
     55.0,
     2.0,
     -1,
     31.0,
     -1,
     35.0,
     34.0,
     15.0,
     28.0,
     8.0,
     38.0,
     -1,
     19.0,
     -1,
     -1,
     40.0,
     -1,
     -1,
     66.0,
     28.0,
     42.0,
     -1,
     21.0,
     18.0,
     14.0,
     40.0,
     27.0,
     -1,
     3.0,
     19.0,
     -1,
     -1,
     -1,
     -1,
     18.0,
     7.0,
     21.0,
     49.0,
     29.0,
     65.0,
     -1,
     21.0,
     28.5,
     5.0,
     11.0,
     22.0,
     38.0,
     45.0,
     4.0,
     -1,
     -1,
     29.0,
     19.0,
     17.0,
     26.0,
     32.0,
     16.0,
     21.0,
     26.0,
     32.0,
     25.0,
     -1,
     -1,
     0.83,
     30.0,
     22.0,
     29.0,
     -1,
     28.0,
     17.0,
     33.0,
     16.0,
     -1,
     23.0,
     24.0,
     29.0,
     20.0,
     46.0,
     26.0,
     59.0,
     -1,
     71.0,
     23.0,
     34.0,
     34.0,
     28.0,
     -1,
     21.0,
     33.0,
     37.0,
     28.0,
     21.0,
     -1,
     38.0,
     -1,
     47.0,
     14.5,
     22.0,
     20.0,
     17.0,
     21.0,
     70.5,
     29.0,
     24.0,
     2.0,
     21.0,
     -1,
     32.5,
     32.5,
     54.0,
     12.0,
     -1,
     24.0,
     -1,
     45.0,
     33.0,
     20.0,
     47.0,
     29.0,
     25.0,
     23.0,
     19.0,
     37.0,
     16.0,
     24.0,
     -1,
     22.0,
     24.0,
     19.0,
     18.0,
     19.0,
     27.0,
     9.0,
     36.5,
     42.0,
     51.0,
     22.0,
     55.5,
     40.5,
     -1,
     51.0,
     16.0,
     30.0,
     -1,
     -1,
     44.0,
     40.0,
     26.0,
     17.0,
     1.0,
     9.0,
     -1,
     45.0,
     -1,
     28.0,
     61.0,
     4.0,
     1.0,
     21.0,
     56.0,
     18.0,
     -1,
     50.0,
     30.0,
     36.0,
     -1,
     -1,
     9.0,
     1.0,
     4.0,
     -1,
     -1,
     45.0,
     40.0,
     36.0,
     32.0,
     19.0,
     19.0,
     3.0,
     44.0,
     58.0,
     -1,
     42.0,
     -1,
     24.0,
     28.0,
     -1,
     34.0,
     45.5,
     18.0,
     2.0,
     32.0,
     26.0,
     16.0,
     40.0,
     24.0,
     35.0,
     22.0,
     30.0,
     -1,
     31.0,
     27.0,
     42.0,
     32.0,
     30.0,
     16.0,
     27.0,
     51.0,
     -1,
     38.0,
     22.0,
     19.0,
     20.5,
     18.0,
     -1,
     35.0,
     29.0,
     59.0,
     5.0,
     24.0,
     -1,
     44.0,
     8.0,
     19.0,
     33.0,
     -1,
     -1,
     29.0,
     22.0,
     30.0,
     44.0,
     25.0,
     24.0,
     37.0,
     54.0,
     -1,
     29.0,
     62.0,
     30.0,
     41.0,
     29.0,
     -1,
     30.0,
     35.0,
     50.0,
     -1,
     3.0,
     52.0,
     40.0,
     -1,
     36.0,
     16.0,
     25.0,
     58.0,
     35.0,
     -1,
     25.0,
     41.0,
     37.0,
     -1,
     63.0,
     45.0,
     -1,
     7.0,
     35.0,
     65.0,
     28.0,
     16.0,
     19.0,
     -1,
     33.0,
     30.0,
     22.0,
     42.0,
     22.0,
     26.0,
     19.0,
     36.0,
     24.0,
     24.0,
     -1,
     23.5,
     2.0,
     -1,
     50.0,
     -1,
     -1,
     19.0,
     -1,
     -1,
     0.92,
     -1,
     17.0,
     30.0,
     30.0,
     24.0,
     18.0,
     26.0,
     28.0,
     43.0,
     26.0,
     24.0,
     54.0,
     31.0,
     40.0,
     22.0,
     27.0,
     30.0,
     22.0,
     -1,
     36.0,
     61.0,
     36.0,
     31.0,
     16.0,
     -1,
     45.5,
     38.0,
     16.0,
     -1,
     -1,
     29.0,
     41.0,
     45.0,
     45.0,
     2.0,
     24.0,
     28.0,
     25.0,
     36.0,
     24.0,
     40.0,
     -1,
     3.0,
     42.0,
     23.0,
     -1,
     15.0,
     25.0,
     -1,
     28.0,
     22.0,
     38.0,
     -1,
     -1,
     40.0,
     29.0,
     45.0,
     35.0,
     -1,
     30.0,
     60.0,
     -1,
     -1,
     24.0,
     25.0,
     18.0,
     19.0,
     22.0,
     3.0,
     -1,
     22.0,
     27.0,
     20.0,
     19.0,
     42.0,
     1.0,
     32.0,
     35.0,
     -1,
     18.0,
     1.0,
     36.0,
     -1,
     17.0,
     36.0,
     21.0,
     28.0,
     23.0,
     24.0,
     22.0,
     31.0,
     46.0,
     23.0,
     28.0,
     39.0,
     26.0,
     21.0,
     28.0,
     20.0,
     34.0,
     51.0,
     3.0,
     21.0,
     -1,
     -1,
     -1,
     33.0,
     -1,
     44.0,
     -1,
     34.0,
     18.0,
     30.0,
     10.0,
     -1,
     21.0,
     29.0,
     28.0,
     18.0,
     -1,
     28.0,
     19.0,
     -1,
     32.0,
     28.0,
     -1,
     42.0,
     17.0,
     50.0,
     14.0,
     21.0,
     24.0,
     64.0,
     31.0,
     45.0,
     20.0,
     25.0,
     28.0,
     -1,
     4.0,
     13.0,
     34.0,
     5.0,
     52.0,
     36.0,
     -1,
     30.0,
     49.0,
     -1,
     29.0,
     65.0,
     -1,
     50.0,
     -1,
     48.0,
     34.0,
     47.0,
     48.0,
     -1,
     38.0,
     -1,
     56.0,
     -1,
     0.75,
     -1,
     38.0,
     33.0,
     23.0,
     22.0,
     -1,
     34.0,
     29.0,
     22.0,
     2.0,
     9.0,
     -1,
     50.0,
     63.0,
     25.0,
     -1,
     35.0,
     58.0,
     30.0,
     9.0,
     -1,
     21.0,
     55.0,
     71.0,
     21.0,
     -1,
     54.0,
     -1,
     25.0,
     24.0,
     17.0,
     21.0,
     -1,
     37.0,
     16.0,
     18.0,
     33.0,
     -1,
     28.0,
     26.0,
     29.0,
     -1,
     36.0,
     54.0,
     24.0,
     47.0,
     34.0,
     -1,
     36.0,
     32.0,
     30.0,
     22.0,
     -1,
     44.0,
     -1,
     40.5,
     50.0,
     -1,
     39.0,
     23.0,
     2.0,
     -1,
     17.0,
     -1,
     30.0,
     7.0,
     45.0,
     30.0,
     -1,
     22.0,
     36.0,
     9.0,
     11.0,
     32.0,
     50.0,
     64.0,
     19.0,
     -1,
     33.0,
     8.0,
     17.0,
     27.0,
     -1,
     22.0,
     22.0,
     62.0,
     48.0,
     -1,
     39.0,
     36.0,
     -1,
     40.0,
     28.0,
     -1,
     -1,
     24.0,
     19.0,
     29.0,
     -1,
     32.0,
     62.0,
     53.0,
     36.0,
     -1,
     16.0,
     19.0,
     34.0,
     39.0,
     -1,
     32.0,
     25.0,
     39.0,
     54.0,
     36.0,
     -1,
     18.0,
     47.0,
     60.0,
     22.0,
     -1,
     35.0,
     52.0,
     47.0,
     -1,
     37.0,
     36.0,
     -1,
     49.0,
     -1,
     49.0,
     24.0,
     -1,
     -1,
     44.0,
     35.0,
     36.0,
     30.0,
     27.0,
     22.0,
     40.0,
     39.0,
     -1,
     -1,
     -1,
     35.0,
     24.0,
     34.0,
     26.0,
     4.0,
     26.0,
     27.0,
     42.0,
     20.0,
     21.0,
     21.0,
     61.0,
     57.0,
     21.0,
     26.0,
     -1,
     80.0,
     51.0,
     32.0,
     -1,
     9.0,
     28.0,
     32.0,
     31.0,
     41.0,
     -1,
     20.0,
     24.0,
     2.0,
     -1,
     0.75,
     48.0,
     19.0,
     56.0,
     -1,
     23.0,
     -1,
     18.0,
     21.0,
     -1,
     18.0,
     24.0,
     -1,
     32.0,
     23.0,
     58.0,
     50.0,
     40.0,
     47.0,
     36.0,
     20.0,
     32.0,
     25.0,
     -1,
     43.0,
     -1,
     40.0,
     31.0,
     70.0,
     31.0,
     -1,
     18.0,
     24.5,
     18.0,
     43.0,
     36.0,
     -1,
     27.0,
     20.0,
     14.0,
     60.0,
     25.0,
     14.0,
     19.0,
     18.0,
     15.0,
     31.0,
     4.0,
     -1,
     25.0,
     60.0,
     52.0,
     44.0,
     -1,
     49.0,
     42.0,
     18.0,
     35.0,
     18.0,
     25.0,
     26.0,
     39.0,
     45.0,
     42.0,
     22.0,
     -1,
     24.0,
     -1,
     48.0,
     29.0,
     52.0,
     19.0,
     38.0,
     27.0,
     -1,
     33.0,
     6.0,
     17.0,
     34.0,
     50.0,
     27.0,
     20.0,
     30.0,
     -1,
     25.0,
     25.0,
     29.0,
     11.0,
     -1,
     23.0,
     23.0,
     28.5,
     48.0,
     35.0,
     -1,
     -1,
     -1,
     36.0,
     21.0,
     24.0,
     31.0,
     70.0,
     16.0,
     30.0,
     19.0,
     31.0,
     4.0,
     6.0,
     33.0,
     23.0,
     48.0,
     0.67,
     28.0,
     18.0,
     34.0,
     33.0,
     -1,
     41.0,
     20.0,
     36.0,
     16.0,
     51.0,
     -1,
     30.5,
     -1,
     32.0,
     24.0,
     48.0,
     57.0,
     -1,
     54.0,
     18.0,
     -1,
     5.0,
     -1,
     43.0,
     13.0,
     17.0,
     29.0,
     -1,
     25.0,
     25.0,
     18.0,
     8.0,
     1.0,
     46.0,
     -1,
     16.0,
     -1,
     -1,
     25.0,
     39.0,
     49.0,
     31.0,
     30.0,
     30.0,
     34.0,
     31.0,
     11.0,
     0.42,
     27.0,
     31.0,
     39.0,
     18.0,
     39.0,
     33.0,
     26.0,
     39.0,
     35.0,
     6.0,
     30.5,
     -1,
     23.0,
     31.0,
     43.0,
     10.0,
     52.0,
     27.0,
     38.0,
     27.0,
     2.0,
     -1,
     -1,
     1.0,
     -1,
     62.0,
     15.0,
     0.83,
     -1,
     23.0,
     18.0,
     39.0,
     21.0,
     -1,
     32.0,
     -1,
     20.0,
     16.0,
     30.0,
     34.5,
     17.0,
     42.0,
     -1,
     35.0,
     28.0,
     -1,
     4.0,
     74.0,
     9.0,
     16.0,
     44.0,
     18.0,
     45.0,
     51.0,
     24.0,
     -1,
     41.0,
     21.0,
     48.0,
     -1,
     24.0,
     42.0,
     27.0,
     31.0,
     -1,
     4.0,
     26.0,
     47.0,
     33.0,
     47.0,
     28.0,
     15.0,
     20.0,
     19.0,
     -1,
     56.0,
     25.0,
     33.0,
     22.0,
     28.0,
     25.0,
     39.0,
     27.0,
     19.0,
     -1,
     26.0,
     32.0]




```python

```


```python

```


```python

```
