Answer the following questions and provide the SQL queries used to find the answer.

    
**Question 1: Which cities and countries have the highest level of transaction revenues on the site?**


SQL Queries:

SELECT DISTINCT city, MAX(city), COUNT(city)
FROM all_sessions
GROUP BY city
ORDER BY COUNT(city) DESC

SELECT DISTINCT country, MAX(country), COUNT(country)
FROM all_sessions
GROUP BY country
ORDER BY COUNT(country) DESC

Answer:
The connection correlation between the transaction revenues column with city and country could not find directly because it is NULL column and it was drop by data cleaning processes.

But we can find the Maximum frequency for the city and country as indicate to the highest level of transaction revenues on the site

The city: I found the highest level of transaction revenues on the site with frequency = 
not available in demo dataset = 8187
The second highest city is Mountain View = 1142

Whereas the highest country is
United States = 8547
The second highest country is 
India = 708

For the country:

country	max	count
United States	United States	8547
India	India	708
United Kingdom	United Kingdom	658
Canada	Canada	634
Germany	Germany	332
Japan	Japan	238
Australia	Australia	221
France	France	214
Taiwan	Taiwan	172
Netherlands	Netherlands	156
Brazil	Brazil	149
Italy	Italy	133
Singapore	Singapore	118
Spain	Spain	116
Mexico	Mexico	102
Russia	Russia	99
Philippines	Philippines	98
Indonesia	Indonesia	88
Ireland	Ireland	87
Poland	Poland	83
Switzerland	Switzerland	82
Czechia	Czechia	81
Sweden	Sweden	76
Hong Kong	Hong Kong	73
Belgium	Belgium	66
Turkey	Turkey	66
Ukraine	Ukraine	63
Denmark	Denmark	63
Israel	Israel	62
Thailand	Thailand	58
Romania	Romania	53
Colombia	Colombia	53
Malaysia	Malaysia	52
New Zealand	New Zealand	51
South Korea	South Korea	50
Greece	Greece	48
Pakistan	Pakistan	46
Argentina	Argentina	43
Slovakia	Slovakia	39
Austria	Austria	39
Vietnam	Vietnam	38
Norway	Norway	34
Hungary	Hungary	32
Venezuela	Venezuela	32
Bangladesh	Bangladesh	32
Peru	Peru	27
Chile	Chile	27
South Africa	South Africa	26
China	China	26
Portugal	Portugal	25
(not set)	(not set)	24
Croatia	Croatia	19
Lithuania	Lithuania	18
Sri Lanka	Sri Lanka	18
United Arab Emirates	United Arab Emirates	18
Finland	Finland	15
Panama	Panama	15
Saudi Arabia	Saudi Arabia	15
Bulgaria	Bulgaria	15
Serbia	Serbia	15
Ecuador	Ecuador	14
Egypt	Egypt	13
Uruguay	Uruguay	13
Estonia	Estonia	11
Dominican Republic	Dominican Republic	11
El Salvador	El Salvador	10
Morocco	Morocco	9
Guatemala	Guatemala	9
Slovenia	Slovenia	9
Puerto Rico	Puerto Rico	9
Latvia	Latvia	8
Nigeria	Nigeria	8
Costa Rica	Costa Rica	6
Belarus	Belarus	6
Cambodia	Cambodia	6
Cyprus	Cyprus	6
Kuwait	Kuwait	6
Georgia	Georgia	5
Tunisia	Tunisia	5
Honduras	Honduras	5
CÃ´te dâ€™Ivoire	CÃ´te dâ€™Ivoire	4
Bolivia	Bolivia	4
Macedonia (FYROM)	Macedonia (FYROM)	4
Algeria	Algeria	4
Bahrain	Bahrain	4
Kenya	Kenya	4
Nepal	Nepal	4
Iraq	Iraq	4
Qatar	Qatar	3
Bosnia & Herzegovina	Bosnia & Herzegovina	3
Iceland	Iceland	3
Ghana	Ghana	3
Macau	Macau	3
Kazakhstan	Kazakhstan	3
Albania	Albania	3
Laos	Laos	3
Jordan	Jordan	3
Myanmar (Burma)	Myanmar (Burma)	3
Brunei	Brunei	2
San Marino	San Marino	2
Papua New Guinea	Papua New Guinea	2
Bahamas	Bahamas	2
RÃ©union	RÃ©union	2
Trinidad & Tobago	Trinidad & Tobago	2
Ethiopia	Ethiopia	2
Barbados	Barbados	2
Oman	Oman	2
Mauritius	Mauritius	2
Sudan	Sudan	2
Moldova	Moldova	2
Nicaragua	Nicaragua	2
Uganda	Uganda	2
Martinique	Martinique	2
Malta	Malta	2
Lebanon	Lebanon	1
Rwanda	Rwanda	1
Zimbabwe	Zimbabwe	1
Paraguay	Paraguay	1
Jersey	Jersey	1
Mali	Mali	1
Armenia	Armenia	1
Luxembourg	Luxembourg	1
Kyrgyzstan	Kyrgyzstan	1
Belize	Belize	1
French Polynesia	French Polynesia	1
Gibraltar	Gibraltar	1
Botswana	Botswana	1
Haiti	Haiti	1
Jamaica	Jamaica	1
Kosovo	Kosovo	1
Tanzania	Tanzania	1
Somalia	Somalia	1
Maldives	Maldives	1
Sint Maarten	Sint Maarten	1
Palestine	Palestine	1
Montenegro	Montenegro	1


For the city:

city	max	count
not available in demo dataset	not available in demo dataset	8187
Mountain View	Mountain View	1142
New York	New York	636
San Francisco	San Francisco	452
Sunnyvale	Sunnyvale	353
(not set)	(not set)	349
San Jose	San Jose	244
Los Angeles	Los Angeles	218
London	London	196
Chicago	Chicago	192
Toronto	Toronto	130
Seattle	Seattle	118
Austin	Austin	106
Palo Alto	Palo Alto	93
Bengaluru	Bengaluru	73
Chennai	Chennai	73
Sydney	Sydney	72
Santa Clara	Santa Clara	72
Atlanta	Atlanta	66
Melbourne	Melbourne	56
Hyderabad	Hyderabad	56
Dublin	Dublin	55
Houston	Houston	53
Hong Kong	Hong Kong	53
Paris	Paris	53
Mumbai	Mumbai	52
Salem	Salem	51
Singapore	Singapore	47
Ann Arbor	Ann Arbor	47
San Bruno	San Bruno	47
Tel Aviv-Yafo	Tel Aviv-Yafo	45
Kirkland	Kirkland	44
Minato	Minato	41
Washington	Washington	41
Montreal	Montreal	39
New Delhi	New Delhi	39
Bangkok	Bangkok	37
Sao Paulo	Sao Paulo	35
Dallas	Dallas	34
Cambridge	Cambridge	33
Mexico City	Mexico City	29
Istanbul	Istanbul	28
Warsaw	Warsaw	28
San Diego	San Diego	27
Pittsburgh	Pittsburgh	26
Kolkata	Kolkata	26
Boston	Boston	26
Jakarta	Jakarta	25
Philadelphia	Philadelphia	24
Zurich	Zurich	24
Seoul	Seoul	24
Pune	Pune	23
Madrid	Madrid	20
Stockholm	Stockholm	20
Kiev	Kiev	20
Moscow	Moscow	19
Bogota	Bogota	19
Fremont	Fremont	18
Charlotte	Charlotte	18
Barcelona	Barcelona	18
Irvine	Irvine	18
Kuala Lumpur	Kuala Lumpur	17
Berlin	Berlin	15
Eau Claire	Eau Claire	15
Munich	Munich	15
Ho Chi Minh City	Ho Chi Minh City	14
Milan	Milan	14
Cupertino	Cupertino	13
Bucharest	Bucharest	13
Brisbane	Brisbane	12
Hamburg	Hamburg	12
Amsterdam	Amsterdam	12
Ahmedabad	Ahmedabad	12
Gurgaon	Gurgaon	10
Dubai	Dubai	9
Milpitas	Milpitas	9
Buenos Aires	Buenos Aires	9
La Victoria	La Victoria	8
Boulder	Boulder	8
Redmond	Redmond	8
Oakland	Oakland	8
Shinjuku	Shinjuku	8
Yokohama	Yokohama	8
Portland	Portland	8
Quebec City	Quebec City	7
Redwood City	Redwood City	7
Santiago	Santiago	7
Vancouver	Vancouver	7
Phoenix	Phoenix	7
San Antonio	San Antonio	7
Colombo	Colombo	6
Quezon City	Quezon City	6
Denver	Denver	6
Osaka	Osaka	6
Taguig	Taguig	6
Orlando	Orlando	6
Budapest	Budapest	6
Perth	Perth	5
Manila	Manila	5
Prague	Prague	5
Mississauga	Mississauga	5
Indore	Indore	5
Calgary	Calgary	5
Jersey City	Jersey City	5
Rio de Janeiro	Rio de Janeiro	5
Lake Oswego	Lake Oswego	5
Kitchener	Kitchener	5
Athens	Athens	5
Rome	Rome	5
Vienna	Vienna	5
South San Francisco	South San Francisco	4
Riyadh	Riyadh	4
Karachi	Karachi	4
Hanoi	Hanoi	4
Zhongli District	Zhongli District	4
Detroit	Detroit	4
Zagreb	Zagreb	4
Saint Petersburg	Saint Petersburg	4
Menlo Park	Menlo Park	4
Norfolk	Norfolk	4
Maracaibo	Maracaibo	4
Rexburg	Rexburg	3
Sherbrooke	Sherbrooke	3
Jaipur	Jaipur	3
Makati	Makati	3
Edmonton	Edmonton	3
Burnaby	Burnaby	3
Pozuelo de Alarcon	Pozuelo de Alarcon	3
Monterrey	Monterrey	3
San Mateo	San Mateo	3
Las Vegas	Las Vegas	3
Thessaloniki	Thessaloniki	3
Oviedo	Oviedo	3
Chico	Chico	3
Culiacan	Culiacan	3
Timisoara	Timisoara	3
Kansas City	Kansas City	3
Santa Fe	Santa Fe	3
Tempe	Tempe	3
Auckland	Auckland	2
Kharagpur	Kharagpur	2
Council Bluffs	Council Bluffs	2
Glasgow	Glasgow	2
Krakow	Krakow	2
Nairobi	Nairobi	2
Brno	Brno	2
Marseille	Marseille	2
Montreuil	Montreuil	2
Bellflower	Bellflower	2
Bilbao	Bilbao	2
Courbevoie	Courbevoie	2
Ottawa	Ottawa	2
Ashburn	Ashburn	2
Minneapolis	Minneapolis	2
Jacksonville	Jacksonville	2
St. Louis	St. Louis	2
Antwerp	Antwerp	2
Kharkiv	Kharkiv	2
Nagoya	Nagoya	2
Manchester	Manchester	2
Shibuya	Shibuya	2
Petaling Jaya	Petaling Jaya	2
Montevideo	Montevideo	2
Medellin	Medellin	2
Columbus	Columbus	2
Copenhagen	Copenhagen	2
Avon	Avon	2
Patna	Patna	2
Poznan	Poznan	2
Izmir	Izmir	2
The Dalles	The Dalles	2
Lucknow	Lucknow	2
Kalamazoo	Kalamazoo	2
Hayward	Hayward	1
Frankfurt	Frankfurt	1
Panama City	Panama City	1
Nanded	Nanded	1
Oslo	Oslo	1
Westlake Village	Westlake Village	1
Oxford	Oxford	1
Appleton	Appleton	1
Bratislava	Bratislava	1
Berkeley	Berkeley	1
Druid Hills	Druid Hills	1
Esbjerg	Esbjerg	1
Gothenburg	Gothenburg	1
Kovrov	Kovrov	1
Skopje	Skopje	1
Asuncion	Asuncion	1
Egham	Egham	1
Stanford	Stanford	1
Cape Town	Cape Town	1
San Salvador	San Salvador	1
Coventry	Coventry	1
Nice	Nice	1
Cluj-Napoca	Cluj-Napoca	1
Richardson	Richardson	1
Tampa	Tampa	1
Wrexham	Wrexham	1
Sacramento	Sacramento	1
Neipu Township	Neipu Township	1
Watford	Watford	1
Villeneuve-d'Ascq	Villeneuve-d'Ascq	1
University Park	University Park	1
Goose Creek	Goose Creek	1
Santa Monica	Santa Monica	1
Bellingham	Bellingham	1
Bandung	Bandung	1
Akron	Akron	1
Beijing	Beijing	1
East Lansing	East Lansing	1
Brussels	Brussels	1
Longtan District	Longtan District	1
Chiyoda	Chiyoda	1
Vladivostok	Vladivostok	1
Quimper	Quimper	1
Wroclaw	Wroclaw	1
Sakai	Sakai	1
Vilnius	Vilnius	1
LaFayette	LaFayette	1
Belgrade	Belgrade	1
Forest Park	Forest Park	1
Stuttgart	Stuttgart	1
Iasi	Iasi	1
Sandton	Sandton	1
Fort Worth	Fort Worth	1
Belo Horizonte	Belo Horizonte	1
Odessa	Odessa	1
Pleasanton	Pleasanton	1
Wellesley	Wellesley	1
Bhubaneswar	Bhubaneswar	1
Chandigarh	Chandigarh	1
Madison	Madison	1
Parsippany-Troy Hills	Parsippany-Troy Hills	1
Antalya	Antalya	1
Rotterdam	Rotterdam	1
Doha	Doha	1
Ghent	Ghent	1
El Paso	El Paso	1
Lisbon	Lisbon	1
Marlboro	Marlboro	1
Ipoh	Ipoh	1
St. John's	St. John's	1
Waterloo	Waterloo	1
Sapporo	Sapporo	1
Indianapolis	Indianapolis	1
Helsinki	Helsinki	1
Rosario	Rosario	1
Westville	Westville	1
Chuo	Chuo	1
South El Monte	South El Monte	1
Piscataway Township	Piscataway Township	1
Greer	Greer	1
Lahore	Lahore	1
Johnson City	Johnson City	1
Columbia	Columbia	1
Bordeaux	Bordeaux	1
AmÃ£	AmÃ£	1
Fortaleza	Fortaleza	1
Cork	Cork	1
Raleigh	Raleigh	1
Alexandria	Alexandria	1
Adelaide	Adelaide	1
Charlottetown	Charlottetown	1





**Question 2: What is the average number of products ordered from visitors in each city and country?**


SQL Queries:

SELECT Country, AVG(total_ordered)
FROM all_sessions aa
JOIN sale_report bb
	ON aa.productsku=bb.productsku 
GROUP BY Country
HAVING COUNT(*) > 1
ORDER BY AVG(total_ordered) DESC;


SELECT city, AVG(total_ordered)
FROM all_sessions aa
JOIN sale_report bb
	ON aa.productsku=bb.productsku 
GROUP BY city
HAVING COUNT(*) > 1
ORDER BY AVG(total_ordered) DESC;

Answer:
For the country:

country	avg
Saudi Arabia	96.28571429
Kuwait	85.75
Laos	85
Papua New Guinea	57.5
Honduras	56
United Arab Emirates	52.1
Croatia	51.7
Trinidad & Tobago	47
Greece	37.96
South Korea	36.37837838
Hong Kong	34.71428571
Guatemala	33.125
Czechia	32.16666667
RÃ©union	32
Mauritius	31
Nepal	30.5
Spain	29.88607595
Denmark	28.97727273
Italy	28.60869565
Taiwan	27.9
Japan	27.82119205
Germany	27.63212435
Romania	26.88235294
Ukraine	26.84615385
Brazil	26.06542056
Thailand	25.45714286
San Marino	25
Mexico	24.875
Malaysia	24.66666667
Israel	24.55263158
Ireland	24.20338983
Bulgaria	24.11111111
Pakistan	23.85185185
Myanmar (Burma)	23.66666667
Slovenia	23
Portugal	23
Russia	22.87692308
Georgia	22.75
Singapore	21.94936709
Argentina	20.70833333
United States	20.4687931
United Kingdom	20.26342711
Canada	20.12440191
Venezuela	20.0625
Netherlands	19.46666667
Australia	19.05109489
Colombia	18.6
(not set)	18.15384615
Vietnam	18.13636364
India	17.79818594
Macedonia (FYROM)	17.66666667
Morocco	17.6
Albania	16.66666667
Belgium	16.59459459
Switzerland	16.23333333
Costa Rica	15.8
Indonesia	15.5
CÃ´te dâ€™Ivoire	15.5
Slovakia	15.5
Philippines	15.15625
Panama	15
France	14.92413793
Peru	14.85
Tunisia	14.75
Turkey	13.66666667
Dominican Republic	13.625
Sweden	13.39473684
Poland	12.80769231
Puerto Rico	12.33333333
Finland	12.27272727
New Zealand	11.84375
Hungary	11.66666667
Bahrain	11.5
Lithuania	11.22222222
Nigeria	11.16666667
Chile	10.25
Serbia	9.714285714
South Africa	9.666666667
Egypt	9.1
Uruguay	8.666666667
Norway	7.578947368
Ghana	7.5
El Salvador	6.5
Bangladesh	6.36
Austria	5.722222222
Sri Lanka	5
China	4.388888889
Bolivia	4
Cambodia	3.25
Latvia	3.166666667
Cyprus	2.5
Bahamas	2.5
Estonia	2.285714286
Macau	2
Qatar	2
Belarus	2
Brunei	2
Ecuador	1.666666667
Kenya	0.666666667
Iraq	0.5


For the city:
city	avg
Rexburg	250.5
Saint Petersburg	101.25
Avon	100
Rome	97.75
Sherbrooke	97
Dubai	89.2
Shinjuku	73
Pune	71.08333333
Rio de Janeiro	65.33333333
San Antonio	58.16666667
Seoul	57.64705882
Menlo Park	51.5
Athens	51.25
Pozuelo de Alarcon	50.5
Salem	46.18518519
Zhongli District	46
Palo Alto	45.57142857
Indore	44
Boston	40.46666667
Bangkok	38.36842105
Hanoi	37.66666667
Hong Kong	34.88888889
Santa Clara	34.79166667
Hamburg	34.25
Munich	33.25
Phoenix	32.2
San Bruno	31.75
Dublin	31.33333333
Bellflower	30
Mumbai	28.03125
Tel Aviv-Yafo	27.14285714
Toronto	26.56962025
Milan	26.4
Mississauga	24.66666667
Madrid	24.58333333
Los Angeles	24.53793103
Charlotte	24.18181818
Seattle	23.97619048
(not set)	23.58847737
Pittsburgh	23.52941176
Kitchener	23.5
Montreuil	23
Philadelphia	22.4375
Mountain View	22.29484029
Buenos Aires	22.25
Amsterdam	22.11111111
Austin	22
Melbourne	21.97142857
Vancouver	21
Sydney	20.79545455
Santiago	20.75
San Francisco	20.61129568
not available in demo dataset	20.35169966
Irvine	20.28571429
Ann Arbor	20.27586207
Chicago	20.04201681
Redmond	19.66666667
Calgary	19.5
Sao Paulo	18.88
San Jose	18.82142857
Kolkata	18.6
Oakland	18.5
Berlin	18.42857143
New York	18.36363636
Hyderabad	18.24390244
Cupertino	18
Ahmedabad	18
Ho Chi Minh City	17.88888889
Redwood City	17.83333333
Chennai	17.53658537
Houston	17.46153846
Sunnyvale	17.25409836
Barcelona	17.15384615
London	16.31034483
Warsaw	16
Kuala Lumpur	15.9
Bucharest	15.28571429
Bogota	15.14285714
Prague	15
Singapore	14.3
Montreal	14.22222222
Quebec City	14
Perth	14
Budapest	14
Paris	13.4375
Lake Oswego	13.33333333
La Victoria	13.33333333
Dallas	13.08695652
Detroit	12.33333333
Washington	12.17857143
Gurgaon	11.83333333
New Delhi	11.80769231
Minato	11.61538462
Taguig	11.6
Osaka	11.6
Cambridge	11.41935484
Kiev	11.28571429
Jaipur	11
Zurich	10.94444444
Bengaluru	10.64583333
Istanbul	10.53333333
Manila	10.5
Stockholm	10.25
Jakarta	9.75
San Diego	9.533333333
Burnaby	9.5
Atlanta	9.333333333
South San Francisco	8.666666667
Mexico City	8.157894737
Moscow	7.666666667
Montevideo	7.5
Courbevoie	7.5
Tempe	7.333333333
Yokohama	7.25
Medellin	7
Fremont	6.583333333
Oviedo	6.5
Kirkland	6.206896552
Kharagpur	6
San Mateo	5.5
Boulder	5.333333333
Denver	5.333333333
Timisoara	5.333333333
Quezon City	5.2
Vienna	4.75
Orlando	4.5
Eau Claire	4.125
Ashburn	4
Culiacan	4
Portland	3.8
Colombo	3.5
Izmir	3.5
Zagreb	3
Petaling Jaya	3
Norfolk	3
Jersey City	2.666666667
Milpitas	2.571428571
Brisbane	2.333333333
Las Vegas	2
Antwerp	1.5
Council Bluffs	1.5
Maracaibo	1.5
Edmonton	1
Patna	1
Kansas City	0.666666667
Minneapolis	0.00E+00
Auckland	0.00E+00
Lucknow	0.00E+00
Karachi	0.00E+00
Nairobi	0.00E+00









**Question 3: Is there any pattern in the types (product categories) of products ordered from visitors in each city and country?**


SQL Queries:

SELECT country, v2productcategory, COUNT(*)
FROM all_sessions 
GROUP BY v2productcategory, country
HAVING COUNT(*) > 1
ORDER BY COUNT(*) DESC;



SELECT city, v2productcategory, COUNT(*)
FROM all_sessions 
GROUP BY v2productcategory, city
HAVING COUNT(*) > 1
ORDER BY COUNT(*) DESC;



Answer:
YES
There is a pattern in the types (product categories) of products ordered from visitors in each city and country.

Please look at the part of Data

For the country:

country	v2productcategory	count
United States	Home/Apparel/Men's/Men's-T-Shirts/	900
United States	Home/Shop by Brand/YouTube/	808
United States	Home/Electronics/	547
United States	Home/Apparel/	536
United States	Home/Shop by Brand/Google/	488
United States	(not set)	458
United States	Home/Apparel/Men's/Men's-Outerwear/	400
United States	Home/Office/	399
United States	Home/Nest/Nest-USA/	338
United States	Home/Drinkware/	315
United States	Home/Apparel/Women's/Women's-T-Shirts/	289
United States	Home/Bags/	289
United Kingdom	Home/Shop by Brand/YouTube/	255
United States	Home/Apparel/Men's/	249
India	Home/Shop by Brand/YouTube/	219
United States	Home/Accessories/	191
India	Home/Apparel/Men's/Men's-T-Shirts/	175
United States	Home/Apparel/Headgear/	158
United States	Home/Shop by Brand/Android/	157
United States	Home/Accessories/Fun/	151
United States	Home/Electronics/Audio/	135
United States	Home/Apparel/Women's/	129
Germany	Home/Shop by Brand/YouTube/	128
United States	Home/Lifestyle/	123
Canada	Home/Shop by Brand/YouTube/	118
United States	Home/Apparel/Women's/Women's-Outerwear/	112
United States	Home/Accessories/Stickers/	103
United States	Home/Drinkware/Water Bottles and Tumblers/	96
United States	Home/Electronics/Electronics Accessories/	88
United States	Home/Bags/Backpacks/	86
Canada	Home/Apparel/Men's/Men's-T-Shirts/	75
United States	Home/Shop by Brand/	74
United Kingdom	Home/Apparel/Men's/Men's-T-Shirts/	73
Australia	Home/Shop by Brand/YouTube/	71
United States	Home/Apparel/Men's/Men's-Performance Wear/	69
United States	Home/Accessories/Drinkware/	65
United States	Home/Apparel/Kid's/Kid's-Infant/	65
United States	Home/Office/Notebooks & Journals/	65
United States	Home/Office/Writing Instruments/	64
United States	Home/Apparel/Kid's/	52
Germany	Home/Apparel/Men's/Men's-T-Shirts/	52
Japan	Home/Apparel/Men's/Men's-T-Shirts/	50
United States	Home/Apparel/Kid's/Kids-Youth/	49
United States	Home/Bags/More Bags/	46
Canada	Home/Electronics/	43
France	Home/Shop by Brand/YouTube/	43
United States	Home/Limited Supply/Bags/	39
United States	Home/Apparel/Kid's/Kid's-Toddler/	39
France	Home/Apparel/Men's/Men's-T-Shirts/	37

For the city:

city	v2productcategory	count
not available in demo dataset	Home/Shop by Brand/YouTube/	1826
not available in demo dataset	Home/Apparel/Men's/Men's-T-Shirts/	1086
not available in demo dataset	Home/Electronics/	441
not available in demo dataset	Home/Apparel/	430
not available in demo dataset	(not set)	401
not available in demo dataset	Home/Shop by Brand/Google/	360
not available in demo dataset	Home/Office/	349
not available in demo dataset	Home/Apparel/Men's/Men's-Outerwear/	327
not available in demo dataset	Home/Bags/	285
not available in demo dataset	Home/Drinkware/	264
not available in demo dataset	Home/Apparel/Men's/	223
not available in demo dataset	Home/Apparel/Women's/Women's-T-Shirts/	197
not available in demo dataset	Home/Accessories/	181
not available in demo dataset	Home/Shop by Brand/Android/	142
not available in demo dataset	Home/Apparel/Headgear/	129
not available in demo dataset	Home/Nest/Nest-USA/	109
not available in demo dataset	Home/Accessories/Stickers/	107
Mountain View	Home/Apparel/Men's/Men's-T-Shirts/	104
not available in demo dataset	Home/Accessories/Fun/	100
Mountain View	Home/Nest/Nest-USA/	92
not available in demo dataset	Home/Shop by Brand/	87
not available in demo dataset	Home/Electronics/Audio/	87
not available in demo dataset	Home/Lifestyle/	82
Mountain View	Home/Shop by Brand/Google/	79
Mountain View	Home/Electronics/	79
New York	Home/Apparel/Men's/Men's-T-Shirts/	74
not available in demo dataset	Home/Office/Notebooks & Journals/	74
Mountain View	Home/Apparel/Men's/Men's-Outerwear/	69
not available in demo dataset	Home/Bags/Backpacks/	68
not available in demo dataset	Home/Electronics/Electronics Accessories/	67
not available in demo dataset	Home/Apparel/Women's/	65
not available in demo dataset	Home/Drinkware/Water Bottles and Tumblers/	64
Mountain View	Home/Office/	64
London	Home/Shop by Brand/YouTube/	62
not available in demo dataset	Home/Office/Writing Instruments/	56
(not set)	Home/Apparel/Men's/Men's-T-Shirts/	54
not available in demo dataset	Home/Apparel/Men's/Men's-Performance Wear/	53







**Question 4: What is the top-selling product from each city/country? Can we find any pattern worthy of noting in the products sold?**


SQL Queries:

SELECT Country, v2productname, COUNT(total_ordered)
FROM all_sessions aa
JOIN sale_report bb
	ON aa.productsku=bb.productsku 
GROUP BY Country, v2productname
HAVING COUNT(*) > 1
ORDER BY country, COUNT(total_ordered) DESC;



Answer:

Can we find any pattern worthy of noting in the products sold?
No any pattern.

country	v2productname	count
(not set)	Google Men's Long Sleeve Raglan Ocean Blue	2
Argentina	Google Alpine Style Backpack	3
Argentina	YouTube Hard Cover Journal	2
Australia	YouTube Twill Cap	8
Australia	22 oz YouTube Bottle Infuser	8
Australia	YouTube Hard Cover Journal	6
Australia	YouTube Custom Decals	5
Australia	Google Men's Vintage Badge Tee Black	4
Australia	YouTube Men's Vintage Henley	4
Australia	Google Laptop and Cell Phone Stickers	4
Australia	22 oz Android Bottle	3
Australia	Google Men's Watershed Full Zip Hoodie Grey	3
Australia	Basecamp Explorer Powerbank Flashlight	3
Australia	Android Sticker Sheet Ultra Removable	3
Australia	Google High Capacity 10,400mAh Charger	3
Australia	Google Twill Cap	3
Australia	25L Classic Rucksack	2
Australia	Google Men's 100% Cotton Short Sleeve Hero Tee Navy	2
Australia	Electronics Accessory Pouch	2
Australia	Google Device Holder Sticky Pad	2
Australia	You Tube Toddler Short Sleeve Tee Red	2
Australia	Google Men's 100% Cotton Short Sleeve Hero Tee White	2
Australia	Galaxy Screen Cleaning Cloth	2
Australia	Google Women's Short Sleeve Hero Tee Red Heather	2
Australia	Waze Mood Original Window Decal	2
Australia	Waterproof Backpack	2
Australia	YouTube Men's Vintage Tank	2
Australia	Google Women's Hero V-Neck Tee White	2
Australia	Recycled Mouse Pad	2
Australia	Collapsible Shopping Bag	2
Bangladesh	Google Men's Vintage Badge Tee White	2
Bangladesh	YouTube Men's Vintage Henley	2
Bangladesh	Electronics Accessory Pouch	2
Belgium	Google Men's 100% Cotton Short Sleeve Hero Tee White	3
Belgium	Seat Pack Organizer	2
Belgium	Google Men's 100% Cotton Short Sleeve Hero Tee Black	2
Belgium	Google Vintage Henley Grey/Black	2
Belgium	YouTube Men's Short Sleeve Hero Tee Black	2
Belgium	Google Men's 100% Cotton Short Sleeve Hero Tee Navy	2
Belgium	YouTube Men's Short Sleeve Hero Tee Charcoal	2
Brazil	Google Men's Vintage Badge Tee Black	6
Brazil	YouTube Custom Decals	4
Brazil	YouTube Hard Cover Journal	4
Brazil	Google Men's 100% Cotton Short Sleeve Hero Tee White	4
Brazil	Waterproof Backpack	3
Brazil	YouTube Twill Cap	3
Brazil	Collapsible Shopping Bag	3
Brazil	Google Men's 100% Cotton Short Sleeve Hero Tee Red	3
Brazil	22 oz YouTube Bottle Infuser	3
Brazil	Suitcase Organizer Cubes	2
Brazil	Google Slim Utility Travel Bag	2
Brazil	YouTube Men's Vintage Henley	2
Brazil	Google Laptop and Cell Phone Stickers	2
Brazil	Android 17oz Stainless Steel Sport Bottle	2
Brazil	Rocket Flashlight	2
Brazil	Google Snapback Hat Black	2
Brazil	Foam Can and Bottle Cooler	2
Brazil	Google Blackout Cap	2
Brazil	Android Men's Engineer Short Sleeve Tee Charcoal	2
Brazil	Google Men's 100% Cotton Short Sleeve Hero Tee Black	2
Brazil	Google Men's  Zip Hoodie	2
Brazil	1 oz Hand Sanitizer	2
Canada	YouTube Twill Cap	13
Canada	22 oz YouTube Bottle Infuser	13
Canada	YouTube Men's Short Sleeve Hero Tee Black	12
Canada	Google Men's 100% Cotton Short Sleeve Hero Tee White	10
Canada	YouTube Men's Vintage Tank	9
Canada	Google Men's 100% Cotton Short Sleeve Hero Tee Black	9
Canada	Google Men's Vintage Badge Tee Black	9
Canada	YouTube Custom Decals	8
Canada	YouTube Men's Short Sleeve Hero Tee Charcoal	7
Canada	Electronics Accessory Pouch	7
Canada	Recycled Mouse Pad	7
Canada	Rocket Flashlight	7
Canada	Google Men's 100% Cotton Short Sleeve Hero Tee Navy	7
Canada	Google Men's Watershed Full Zip Hoodie Grey	6
Canada	Android Sticker Sheet Ultra Removable	6
Canada	Keyboard DOT Sticker	6
Canada	Google Alpine Style Backpack	6
Canada	YouTube Hard Cover Journal	6
Canada	Android Wool Heather Cap Heather/Black	6
Canada	YouTube Men's Vintage Henley	6
Canada	Bottle Opener Clip	5
Canada	Google Device Holder Sticky Pad	5
Canada	Google Flashlight	5
Canada	Google Metallic Notebook Set	5
Canada	Collapsible Shopping Bag	5
Canada	Android Rise 14 oz Mug	5
Canada	Google Men's Long Sleeve Raglan Ocean Blue	4
Canada	Android Men's Long Sleeve Badge Crew Tee Heather	4
Canada	Google Tube Power Bank	4
Canada	Sport Bag	4
Canada	Google Men's Performance Full Zip Jacket Black	4
Canada	Android Twill Cap	4
Canada	Google 17oz Stainless Steel Sport Bottle	4
Canada	Google Power Bank	4
Canada	22 oz Android Bottle	4
Canada	Android Men's Vintage Henley	4
Canada	Waze Mood Ninja Window Decal	3
Canada	Google Men's  Zip Hoodie	3
Canada	YouTube Women's Short Sleeve Tri-blend Badge Tee Grey	3
Canada	Google Stylus Pen w/ LED Light	3
Canada	Windup Android	3
Canada	Rubber Grip Ballpoint Pen 4 Pack	3
Canada	Android Men's Engineer Short Sleeve Tee Charcoal	3
Canada	Google Men's Vintage Badge Tee Green	3
Canada	SPF-15 Slim & Slender Lip Balm	3
Canada	Google Laptop Backpack	3
Canada	Suitcase Organizer Cubes	3
Canada	Clip-on Compact Charger	3
Canada	Google 2200mAh Micro Charger	3
Canada	Google Lunch Bag	3
Canada	Google Sunglasses	3
Canada	Pen Pencil & Highlighter Set	3
Canada	Google Doodle Decal	3
Canada	Google Insulated Stainless Steel Bottle	3
Canada	Android Men's Short Sleeve Tri-blend Hero Tee Grey	2
Canada	Google High Capacity 10,400mAh Charger	2
Canada	You Tube Toddler Short Sleeve Tee Red	2
Canada	Android Men's Short Sleeve Hero Tee White	2
Canada	Google Twill Cap	2
Canada	Google Rucksack	2
Canada	YouTube Youth Short Sleeve Tee Red	2
Canada	Waze Mobile Phone Vent Mount	2
Canada	Foam Can and Bottle Cooler	2
Canada	Google Women's Short Sleeve Hero Tee White	2
Canada	Google Women's Vintage Hero Tee Black	2
Canada	Spiral Notebook and Pen Set	2
Canada	Waze Pack of 9 Decal Set	2
Canada	Google 4400mAh Power Bank	2
Canada	Galaxy Screen Cleaning Cloth	2
Canada	Google 22 oz Water Bottle	2
Canada	Google Men's 100% Cotton Short Sleeve Hero Tee Red	2
Canada	Google Women's Short Sleeve Hero Tee Heather	2
Canada	Google Device Stand	2
Canada	Android Stretch Fit Hat Black	2
Canada	Google Long Sleeve Raglan Badge Henley Ocean Blue	2
Canada	Four Color Retractable Pen	2
Canada	Badge Holder	2
Canada	Google Women's Lightweight Microfleece Jacket	2
Canada	Android BTTF Moonshot Shirt	2
Canada	Waterproof Backpack	2
Canada	Google Women's Vintage T-Shirt Black	2
Canada	NestÂ® Cam Indoor Security Camera - USA	2
Canada	Ballpoint Stylus Pen	2
Canada	Google Snapback Hat Black	2
Canada	Waze Baby on Board Window Decal	2
Canada	1 oz Hand Sanitizer	2
Canada	Android BTTF Cosmos Shirt	2
Canada	Google Men's Microfiber 1/4 Zip Pullover Blue/Indigo	2
Canada	Google Women's Performance Full Zip Jacket Black	2
Canada	Google Tri-blend Hoodie Grey	2
Canada	Google Men's Bayside Graphic Tee	2
Canada	26 oz Double Wall Insulated Bottle	2
Canada	Google Blackout Cap	2
Canada	Google Vintage Henley Grey/Black	2
Canada	Google Women's Scoop Neck Tee White	2
China	Google Men's Vintage Badge Tee White	2
Colombia	22 oz YouTube Bottle Infuser	4
Colombia	YouTube Hard Cover Journal	3
Colombia	YouTube Men's Short Sleeve Hero Tee Black	2
Colombia	Android Men's Short Sleeve Tri-blend Hero Tee Grey	2
CÃ´te dâ€™Ivoire	YouTube Custom Decals	2
Croatia	Google Men's Watershed Full Zip Hoodie Grey	2
Croatia	YouTube Men's Vintage Henley	2
Czechia	YouTube Hard Cover Journal	6
Czechia	Google Men's 100% Cotton Short Sleeve Hero Tee White	5
Czechia	You Tube Toddler Short Sleeve Tee Red	3
Czechia	Electronics Accessory Pouch	2
Czechia	22 oz YouTube Bottle Infuser	2
Czechia	Google High Capacity 10,400mAh Charger	2
Czechia	Google Snapback Hat Black	2
Czechia	YouTube Men's Vintage Tank	2
Czechia	YouTube Custom Decals	2
Denmark	YouTube Hard Cover Journal	5
Denmark	YouTube Men's Vintage Tank	4
Denmark	Google Men's 100% Cotton Short Sleeve Hero Tee Navy	4
Denmark	YouTube Twill Cap	2
Denmark	You Tube Toddler Short Sleeve Tee Red	2
Denmark	22 oz YouTube Bottle Infuser	2
France	Google Men's 100% Cotton Short Sleeve Hero Tee White	8
France	YouTube Men's Short Sleeve Hero Tee Charcoal	6
France	YouTube Custom Decals	5
France	YouTube Men's Short Sleeve Hero Tee Black	5
France	Google Men's 100% Cotton Short Sleeve Hero Tee Black	5
France	YouTube Men's Vintage Henley	4
France	Google Women's Short Sleeve Hero Tee Black	3
France	Android Wool Heather Cap Heather/Black	3
France	Android Rise 14 oz Mug	3
France	Android Men's Engineer Short Sleeve Tee Charcoal	3
France	Google Men's 100% Cotton Short Sleeve Hero Tee Navy	3
France	YouTube Men's Vintage Tank	3
France	YouTube Hard Cover Journal	3
France	Suitcase Organizer Cubes	3
France	Google G Noise-reducing Bluetooth Headphones	2
France	YouTube Youth Short Sleeve Tee Red	2
France	Google Men's Vintage Badge Tee Black	2
France	Waze Pack of 9 Decal Set	2
France	Sport Bag	2
France	Google Bib Red	2
France	Google Men's Watershed Full Zip Hoodie Grey	2
France	Google Men's Microfiber 1/4 Zip Pullover Blue/Indigo	2
France	Google Laptop and Cell Phone Stickers	2
France	Google Men's 100% Cotton Short Sleeve Hero Tee Red	2
France	Android 17oz Stainless Steel Sport Bottle	2
France	Android Men's Vintage Tank	2
France	22 oz YouTube Bottle Infuser	2
France	Google Men's Vintage Badge Tee White	2
France	YouTube Twill Cap	2
France	Electronics Accessory Pouch	2
Georgia	YouTube Custom Decals	3
Germany	YouTube Twill Cap	13
Germany	YouTube Men's Short Sleeve Hero Tee Black	10
Germany	YouTube Custom Decals	9
Germany	YouTube Hard Cover Journal	9
Germany	YouTube Men's Short Sleeve Hero Tee Charcoal	6
Germany	22 oz YouTube Bottle Infuser	6
Germany	You Tube Toddler Short Sleeve Tee Red	6
Germany	Google Men's Vintage Badge Tee Black	5
Germany	Google Men's 100% Cotton Short Sleeve Hero Tee Navy	5
Germany	YouTube Men's Vintage Henley	4
Germany	YouTube Men's Skater Tee Charcoal	4
Germany	Google Doodle Decal	3
Germany	Electronics Accessory Pouch	3
Germany	Android Wool Heather Cap Heather/Black	3
Germany	Ballpoint LED Light Pen	3
Germany	Google Vintage Henley Grey/Black	3
Germany	Android Men's Engineer Short Sleeve Tee Charcoal	2
Germany	Android Rise 14 oz Mug	2
Germany	Android Men's Long Sleeve Badge Crew Tee Heather	2
Germany	Suitcase Organizer Cubes	2
Germany	Google Laptop Backpack	2
Germany	Google Canvas Tote Natural/Navy	2
Germany	Android Men's Short Sleeve Hero Tee White	2
Germany	Google Men's 100% Cotton Short Sleeve Hero Tee Red	2
Germany	Compact Selfie Stick	2
Germany	Google Men's Skater Tee Charcoal	2
Germany	Google Men's  Zip Hoodie	2
Germany	Google Men's 100% Cotton Short Sleeve Hero Tee Black	2
Germany	Waterpoof Gear Bag	2
Germany	Basecamp Explorer Powerbank Flashlight	2
Germany	Android Luggage Tag	2
Germany	SPF-15 Slim & Slender Lip Balm	2
Germany	Google Men's Watershed Full Zip Hoodie Grey	2
Germany	YouTube Men's Vintage Tank	2
Germany	Seat Pack Organizer	2
Germany	Google Men's Vintage Badge Tee White	2
Germany	Android Men's Short Sleeve Tri-blend Hero Tee Grey	2
Germany	Foam Can and Bottle Cooler	2
Germany	Google Bib White	2
Greece	YouTube Men's Vintage Tank	3
Greece	22 oz YouTube Bottle Infuser	3
Greece	Waterproof Backpack	3
Hong Kong	Recycled Mouse Pad	2
Hong Kong	Galaxy Screen Cleaning Cloth	2
Hong Kong	Sport Bag	2
Hong Kong	Leatherette Journal	2
Hong Kong	YouTube Men's Short Sleeve Hero Tee Charcoal	2
Hong Kong	YouTube Men's Short Sleeve Hero Tee Black	2
Hungary	YouTube Men's Short Sleeve Hero Tee Charcoal	2
Hungary	YouTube Men's Short Sleeve Hero Tee Black	2
India	YouTube Custom Decals	22
India	Google Men's 100% Cotton Short Sleeve Hero Tee White	20
India	YouTube Men's Short Sleeve Hero Tee Black	15
India	YouTube Men's Short Sleeve Hero Tee Charcoal	15
India	22 oz YouTube Bottle Infuser	15
India	Google Men's Vintage Badge Tee Black	14
India	YouTube Twill Cap	13
India	YouTube Men's Vintage Tank	13
India	YouTube Men's Vintage Henley	13
India	Google Men's 100% Cotton Short Sleeve Hero Tee Black	12
India	Google Men's 100% Cotton Short Sleeve Hero Tee Red	12
India	Google Men's 100% Cotton Short Sleeve Hero Tee Navy	12
India	YouTube Hard Cover Journal	11
India	Google Vintage Henley Grey/Black	7
India	Android Men's Vintage Tank	6
India	Google Snapback Hat Black	6
India	You Tube Toddler Short Sleeve Tee Red	5
India	Google Canvas Tote Natural/Navy	5
India	Google Laptop and Cell Phone Stickers	5
India	Google Men's Skater Tee Charcoal	5
India	Google Men's  Zip Hoodie	5
India	Google Men's Convertible Vest-Jacket Pewter	5
India	Google Long Sleeve Raglan Badge Henley Ocean Blue	4
India	Android Luggage Tag	4
India	Android Men's Engineer Short Sleeve Tee Charcoal	4
India	Android Men's Long Sleeve Badge Crew Tee Heather	4
India	Android Men's Short Sleeve Tri-blend Hero Tee Grey	4
India	Google Tri-blend Hoodie Grey	4
India	Android Lunch Kit	4
India	Google Men's Short Sleeve Badge Tee Charcoal	4
India	Sport Bag	3
India	Google Stylus Pen w/ LED Light	3
India	Google Men's Long Sleeve Raglan Ocean Blue	3
India	Google Device Stand	3
India	Red Shine 15 oz Mug	3
India	Android Twill Cap	3
India	Galaxy Screen Cleaning Cloth	3
India	22 oz Android Bottle	3
India	YouTube Youth Short Sleeve Tee Red	3
India	Google Men's Microfiber 1/4 Zip Pullover Blue/Indigo	3
India	Google 17oz Stainless Steel Sport Bottle	3
India	Collapsible Shopping Bag	3
India	Android Sticker Sheet Ultra Removable	3
India	Google Women's 3/4 Sleeve Baseball Raglan Heather/Black	3
India	Google Men's Vintage Badge Tee White	3
India	Suitcase Organizer Cubes	3
India	Basecamp Explorer Powerbank Flashlight	3
India	Google Slim Utility Travel Bag	3
India	Waterproof Backpack	3
India	Keyboard DOT Sticker	3
India	Google Men's Watershed Full Zip Hoodie Grey	2
India	Android RFID Journal	2
India	Google Device Holder Sticky Pad	2
India	Plastic Sliding Flashlight	2
India	Spiral Notebook and Pen Set	2
India	Android Stretch Fit Hat Black	2
India	Colored Pencil Set	2
India	Waze Mood Happy Window Decal	2
India	Windup Android	2
India	Android 17oz Stainless Steel Sport Bottle	2
India	Google Women's Short Sleeve Hero Tee Black	2
India	Google Women's Convertible Vest-Jacket Sea Foam Green	2
India	23 oz Wide Mouth Sport Bottle	2
India	Android Men's Short Sleeve Hero Tee White	2
India	YouTube Men's Skater Tee Charcoal	2
India	Google Rucksack	2
India	Electronics Accessory Pouch	2
India	Bottle Opener Clip	2
India	Google Tote Bag	2
India	Google Men's Short Sleeve Hero Tee Charcoal	2
India	Google Men's Vintage Badge Tee Green	2
India	Switch Tone Color Crayon Pen	2
India	8 pc Android Sticker Sheet	2
India	Google Men's Airflow 1/4 Zip Pullover Lapis	2
India	Maze Pen	2
India	Google Women's Scoop Neck Tee Black	2
India	Android BTTF Cosmos Graphic Tee	2
India	NestÂ® Cam Indoor Security Camera - USA	2
Indonesia	22 oz YouTube Bottle Infuser	6
Indonesia	YouTube Men's Short Sleeve Hero Tee Charcoal	3
Indonesia	Google Men's Vintage Badge Tee White	2
Indonesia	Google Men's 100% Cotton Short Sleeve Hero Tee White	2
Indonesia	Google Men's 100% Cotton Short Sleeve Hero Tee Black	2
Indonesia	Google Slim Utility Travel Bag	2
Indonesia	Google Women's 1/4 Zip Jacket Charcoal	2
Indonesia	YouTube Custom Decals	2
Indonesia	YouTube Men's Vintage Tank	2
Indonesia	Google Metallic Notebook Set	2
Indonesia	YouTube Twill Cap	2
Indonesia	Waze Mood Ninja Window Decal	2
Ireland	You Tube Toddler Short Sleeve Tee Red	3
Ireland	YouTube Men's Vintage Henley	2
Ireland	Recycled Mouse Pad	2
Ireland	YouTube Custom Decals	2
Ireland	Google Men's Watershed Full Zip Hoodie Grey	2
Ireland	Google Snapback Hat Black	2
Ireland	Android 17oz Stainless Steel Sport Bottle	2
Israel	22 oz YouTube Bottle Infuser	3
Israel	YouTube Hard Cover Journal	2
Israel	Android 17oz Stainless Steel Sport Bottle	2
Israel	Google Canvas Tote Natural/Navy	2
Italy	Google Men's 100% Cotton Short Sleeve Hero Tee White	5
Italy	YouTube Men's Vintage Tank	4
Italy	22 oz YouTube Bottle Infuser	4
Italy	Android Sticker Sheet Ultra Removable	4
Italy	YouTube Custom Decals	4
Italy	Leatherette Journal	3
Italy	Google Men's Long Sleeve Raglan Ocean Blue	3
Italy	Google Men's 100% Cotton Short Sleeve Hero Tee Black	3
Italy	YouTube Men's Vintage Henley	3
Italy	YouTube Hard Cover Journal	3
Italy	YouTube Men's Short Sleeve Hero Tee Black	2
Italy	SPF-15 Slim & Slender Lip Balm	2
Italy	Google Men's Vintage Badge Tee White	2
Italy	Google Men's 100% Cotton Short Sleeve Hero Tee Red	2
Italy	YouTube Men's Short Sleeve Hero Tee Charcoal	2
Italy	Google Women's 3/4 Sleeve Baseball Raglan Heather/Black	2
Italy	Google Men's Watershed Full Zip Hoodie Grey	2
Italy	Windup Android	2
Japan	Google Men's 100% Cotton Short Sleeve Hero Tee White	7
Japan	YouTube Men's Vintage Tank	4
Japan	YouTube Custom Decals	4
Japan	YouTube Men's Short Sleeve Hero Tee Black	4
Japan	Android Men's Vintage Tank	3
Japan	Google Sunglasses	3
Japan	Sport Bag	3
Japan	YouTube Hard Cover Journal	3
Japan	Google Snapback Hat Black	3
Japan	Google Women's Short Sleeve Hero Tee Black	3
Japan	Android Men's Short Sleeve Tri-blend Hero Tee Grey	3
Japan	Android Men's Engineer Short Sleeve Tee Charcoal	3
Japan	Windup Android	3
Japan	Google Vintage Henley Grey/Black	2
Japan	YouTube Men's Short Sleeve Hero Tee Charcoal	2
Japan	Android Rise 14 oz Mug	2
Japan	Google 17oz Stainless Steel Sport Bottle	2
Japan	Ballpoint LED Light Pen	2
Japan	Google Alpine Style Backpack	2
Japan	Suitcase Organizer Cubes	2
Japan	Google Laptop and Cell Phone Stickers	2
Japan	Google Slim Utility Travel Bag	2
Japan	Google Men's 100% Cotton Short Sleeve Hero Tee Red	2
Japan	Google Lunch Bag	2
Japan	Android Sticker Sheet Ultra Removable	2
Japan	Google Women's Scoop Neck Tee Black	2
Japan	Google Stylus Pen w/ LED Light	2
Japan	Google Women's Short Sleeve Hero Tee White	2
Japan	Google 5-Panel Snapback Cap	2
Japan	Google Rucksack	2
Japan	Google Men's Vintage Badge Tee Sage	2
Laos	YouTube Hard Cover Journal	2
Malaysia	Google Alpine Style Backpack	2
Malaysia	You Tube Toddler Short Sleeve Tee Red	2
Malaysia	Google Women's Short Sleeve Hero Tee Black	2
Malaysia	Four Color Retractable Pen	2
Malaysia	Google Men's 100% Cotton Short Sleeve Hero Tee White	2
Mexico	YouTube Men's Short Sleeve Hero Tee Black	5
Mexico	YouTube Men's Short Sleeve Hero Tee Charcoal	4
Mexico	YouTube Men's Vintage Tank	3
Mexico	Google Men's 100% Cotton Short Sleeve Hero Tee Navy	3
Mexico	YouTube Twill Cap	3
Mexico	YouTube Hard Cover Journal	2
Mexico	YouTube Men's Vintage Henley	2
Mexico	Google Men's 100% Cotton Short Sleeve Hero Tee White	2
Mexico	Ballpoint Stylus Pen	2
Mexico	Google Rucksack	2
Mexico	Google Alpine Style Backpack	2
Netherlands	22 oz YouTube Bottle Infuser	5
Netherlands	YouTube Men's Vintage Henley	5
Netherlands	YouTube Twill Cap	5
Netherlands	YouTube Men's Short Sleeve Hero Tee Charcoal	5
Netherlands	Google G Noise-reducing Bluetooth Headphones	4
Netherlands	YouTube Men's Vintage Tank	4
Netherlands	Google Men's 100% Cotton Short Sleeve Hero Tee White	3
Netherlands	YouTube Hard Cover Journal	3
Netherlands	Galaxy Screen Cleaning Cloth	3
Netherlands	YouTube Men's Short Sleeve Hero Tee Black	3
Netherlands	Android Women's Fleece Hoodie	2
Netherlands	Google Men's Vintage Badge Tee Black	2
Netherlands	Google Alpine Style Backpack	2
Netherlands	Sport Bag	2
Netherlands	Google Men's 100% Cotton Short Sleeve Hero Tee Navy	2
Netherlands	Google Canvas Tote Natural/Navy	2
Netherlands	Google Men's 100% Cotton Short Sleeve Hero Tee Red	2
Netherlands	YouTube Custom Decals	2
Netherlands	Google Doodle Decal	2
Netherlands	Bottle Opener Clip	2
Netherlands	Google Tube Power Bank	2
Netherlands	Clip-on Compact Charger	2
Netherlands	Google Twill Cap	2
Netherlands	Micro Wireless Earbud	2
Netherlands	Google Men's Airflow 1/4 Zip Pullover Black	2
New Zealand	22 oz YouTube Bottle Infuser	3
New Zealand	YouTube Men's Vintage Tank	2
New Zealand	YouTube Men's Long & Lean Tee Charcoal	2
New Zealand	Google Women's Lightweight Microfleece Jacket	2
New Zealand	Google Men's  Zip Hoodie	2
New Zealand	YouTube Custom Decals	2
Norway	Google Laptop and Cell Phone Stickers	2
Norway	YouTube Men's Short Sleeve Hero Tee Charcoal	2
Pakistan	22 oz YouTube Bottle Infuser	4
Pakistan	YouTube Men's Short Sleeve Hero Tee Black	3
Pakistan	YouTube Men's Short Sleeve Hero Tee Charcoal	3
Peru	22 oz YouTube Bottle Infuser	2
Peru	Compact Selfie Stick	2
Philippines	YouTube Men's Short Sleeve Hero Tee Charcoal	3
Philippines	Google Men's 100% Cotton Short Sleeve Hero Tee Black	3
Philippines	YouTube Twill Cap	3
Philippines	Google Men's Convertible Vest-Jacket Pewter	3
Philippines	22 oz YouTube Bottle Infuser	2
Philippines	Android Twill Cap	2
Philippines	Google Tri-blend Hoodie Grey	2
Philippines	Google Men's Vintage Badge Tee Black	2
Philippines	Google Men's 100% Cotton Short Sleeve Hero Tee Navy	2
Philippines	Spiral Notebook and Pen Set	2
Poland	YouTube Men's Vintage Tank	3
Poland	YouTube Custom Decals	2
Poland	Android BTTF Moonshot Graphic Tee	2
Poland	Android Twill Cap	2
Poland	Google Women's Short Sleeve Hero Dark Grey	2
Poland	Android Men's Engineer Short Sleeve Tee Charcoal	2
Poland	Google Laptop and Cell Phone Stickers	2
Poland	Keyboard DOT Sticker	2
Poland	7&quot; Dog Frisbee	2
Poland	YouTube Twill Cap	2
Portugal	Google Men's 100% Cotton Short Sleeve Hero Tee Black	2
Romania	YouTube Custom Decals	5
Romania	Google Men's 100% Cotton Short Sleeve Hero Tee Navy	2
Romania	YouTube Men's Short Sleeve Hero Tee Black	2
Romania	Google Men's 100% Cotton Short Sleeve Hero Tee Black	2
Romania	Google Men's 100% Cotton Short Sleeve Hero Tee Red	2
Russia	YouTube Twill Cap	4
Russia	YouTube Men's Vintage Henley	3
Russia	Google Alpine Style Backpack	3
Russia	Google Women's 1/4 Zip Jacket Charcoal	2
Russia	Google Canvas Tote Natural/Navy	2
Russia	SPF-15 Slim & Slender Lip Balm	2
Russia	Switch Tone Color Crayon Pen	2
Russia	YouTube Men's Short Sleeve Hero Tee Charcoal	2
Russia	YouTube Hard Cover Journal	2
Russia	Windup Android	2
Russia	Google Men's 100% Cotton Short Sleeve Hero Tee Navy	2
Serbia	YouTube Twill Cap	2
Singapore	Google Men's 100% Cotton Short Sleeve Hero Tee Black	5
Singapore	Google Men's 100% Cotton Short Sleeve Hero Tee White	4
Singapore	Google Men's Vintage Badge Tee Black	3
Singapore	UpCycled Handlebar Bag	2
Singapore	Sport Bag	2
Singapore	Google Alpine Style Backpack	2
Singapore	Google Men's Watershed Full Zip Hoodie Grey	2
Singapore	Android Men's Vintage Tank	2
Singapore	Google Men's 100% Cotton Short Sleeve Hero Tee Red	2
Singapore	SPF-15 Slim & Slender Lip Balm	2
Singapore	Google Toddler Short Sleeve Tee White	2
Singapore	Android Men's Engineer Short Sleeve Tee Charcoal	2
Singapore	Google RFID Journal	2
Singapore	Google Men's 100% Cotton Short Sleeve Hero Tee Navy	2
Singapore	You Tube Toddler Short Sleeve Tee Red	2
Slovakia	YouTube Twill Cap	2
Slovakia	YouTube Custom Decals	2
Slovakia	YouTube Hard Cover Journal	2
South Africa	YouTube Men's Vintage Henley	2
South Africa	Google Men's 100% Cotton Short Sleeve Hero Tee Black	2
South Korea	YouTube Custom Decals	2
South Korea	Ballpoint Stylus Pen	2
South Korea	22 oz YouTube Bottle Infuser	2
Spain	22 oz YouTube Bottle Infuser	4
Spain	Android Rise 14 oz Mug	3
Spain	Google Men's 100% Cotton Short Sleeve Hero Tee Navy	3
Spain	YouTube Men's Short Sleeve Hero Tee Black	3
Spain	Google Rucksack	2
Spain	SPF-15 Slim & Slender Lip Balm	2
Spain	YouTube Hard Cover Journal	2
Spain	Android Twill Cap	2
Spain	Waze Dress Socks	2
Spain	Google Lunch Bag	2
Spain	Android Men's Engineer Short Sleeve Tee Charcoal	2
Sri Lanka	Android Men's Vintage Henley	2
Sri Lanka	Google Men's 100% Cotton Short Sleeve Hero Tee White	2
Sweden	YouTube Men's Vintage Henley	3
Sweden	Google Men's 100% Cotton Short Sleeve Hero Tee Black	2
Sweden	Waterproof Backpack	2
Sweden	Metal Texture Roller Pen	2
Sweden	Android Rise 14 oz Mug	2
Sweden	Google Men's 100% Cotton Short Sleeve Hero Tee Navy	2
Sweden	YouTube Twill Cap	2
Switzerland	Google G Noise-reducing Bluetooth Headphones	3
Switzerland	YouTube Twill Cap	3
Switzerland	Sport Bag	3
Switzerland	Google Men's Watershed Full Zip Hoodie Grey	2
Switzerland	Compact Selfie Stick	2
Switzerland	Google Laptop and Cell Phone Stickers	2
Switzerland	Google Men's Vintage Badge Tee Black	2
Switzerland	Google Rucksack	2
Switzerland	Suitcase Organizer Cubes	2
Switzerland	YouTube Men's Short Sleeve Hero Tee Charcoal	2
Taiwan	Google Men's 100% Cotton Short Sleeve Hero Tee White	6
Taiwan	Sport Bag	5
Taiwan	YouTube Men's Vintage Tank	3
Taiwan	26 oz Double Wall Insulated Bottle	3
Taiwan	Google Laptop and Cell Phone Stickers	3
Taiwan	Waterproof Backpack	3
Taiwan	Basecamp Explorer Powerbank Flashlight	3
Taiwan	Galaxy Screen Cleaning Cloth	3
Taiwan	YouTube Hard Cover Journal	3
Taiwan	Google Men's 100% Cotton Short Sleeve Hero Tee Black	3
Taiwan	Collapsible Shopping Bag	2
Taiwan	Google G Noise-reducing Bluetooth Headphones	2
Taiwan	Google Men's Vintage Badge Tee Green	2
Taiwan	Google Women's Short Sleeve Hero Tee Grey	2
Taiwan	Google Men's Long Sleeve Raglan Ocean Blue	2
Taiwan	Keyboard DOT Sticker	2
Taiwan	Google Tote Bag	2
Taiwan	Google Women's Performance Full Zip Jacket Black	2
Taiwan	Electronics Accessory Pouch	2
Taiwan	Windup Android	2
Taiwan	Google Laptop Backpack	2
Taiwan	YouTube Custom Decals	2
Taiwan	Spiral Notebook and Pen Set	2
Taiwan	Suitcase Organizer Cubes	2
Taiwan	Google Women's 1/4 Zip Performance Pullover Black	2
Taiwan	Pen Pencil & Highlighter Set	2
Taiwan	Google Alpine Style Backpack	2
Taiwan	Google Lunch Bag	2
Taiwan	YouTube Men's Short Sleeve Hero Tee Black	2
Taiwan	Rubber Grip Ballpoint Pen 4 Pack	2
Thailand	YouTube Men's Vintage Henley	3
Thailand	Google Men's Vintage Badge Tee Black	3
Thailand	22 oz YouTube Bottle Infuser	3
Thailand	Keyboard DOT Sticker	2
Thailand	YouTube Twill Cap	2
Tunisia	Google Device Holder Sticky Pad	2
Turkey	YouTube Hard Cover Journal	4
Turkey	YouTube Men's Vintage Henley	2
Turkey	Google G Noise-reducing Bluetooth Headphones	2
Ukraine	YouTube Hard Cover Journal	3
Ukraine	Google Men's 100% Cotton Short Sleeve Hero Tee White	3
Ukraine	Micro Wireless Earbud	2
Ukraine	YouTube Custom Decals	2
Ukraine	Android Rise 14 oz Mug	2
Ukraine	Google Men's 100% Cotton Short Sleeve Hero Tee Black	2
United Kingdom	22 oz YouTube Bottle Infuser	22
United Kingdom	YouTube Hard Cover Journal	21
United Kingdom	YouTube Twill Cap	20
United Kingdom	YouTube Men's Short Sleeve Hero Tee Black	15
United Kingdom	YouTube Custom Decals	13
United Kingdom	YouTube Men's Vintage Henley	12
United Kingdom	Google Men's 100% Cotton Short Sleeve Hero Tee White	11
United Kingdom	You Tube Toddler Short Sleeve Tee Red	9
United Kingdom	Google Men's 100% Cotton Short Sleeve Hero Tee Red	9
United Kingdom	Electronics Accessory Pouch	7
United Kingdom	YouTube Youth Short Sleeve Tee Red	7
United Kingdom	Google Men's 100% Cotton Short Sleeve Hero Tee Navy	6
United Kingdom	Google Men's Vintage Badge Tee Black	6
United Kingdom	YouTube Men's Short Sleeve Hero Tee Charcoal	6
United Kingdom	Google Snapback Hat Black	5
United Kingdom	Android Men's Engineer Short Sleeve Tee Charcoal	5
United Kingdom	Google Men's Watershed Full Zip Hoodie Grey	5
United Kingdom	Google Alpine Style Backpack	5
United Kingdom	Google Canvas Tote Natural/Navy	5
United Kingdom	Google Men's 100% Cotton Short Sleeve Hero Tee Black	4
United Kingdom	Google Device Holder Sticky Pad	4
United Kingdom	Google Insulated Stainless Steel Bottle	4
United Kingdom	Android Wool Heather Cap Heather/Black	4
United Kingdom	Google Stylus Pen w/ LED Light	4
United Kingdom	Google Laptop and Cell Phone Stickers	4
United Kingdom	YouTube Men's Skater Tee Charcoal	4
United Kingdom	Google Men's Vintage Badge Tee White	4
United Kingdom	Android Sticker Sheet Ultra Removable	4
United Kingdom	SPF-15 Slim & Slender Lip Balm	3
United Kingdom	Android Twill Cap	3
United Kingdom	Google Slim Utility Travel Bag	3
United Kingdom	Google Women's Convertible Vest-Jacket Sea Foam Green	3
United Kingdom	Android Men's Short Sleeve Hero Tee White	3
United Kingdom	Android Hard Cover Journal	3
United Kingdom	Google Men's  Zip Hoodie	3
United Kingdom	Red Shine 15 oz Mug	3
United Kingdom	Metal Texture Roller Pen	3
United Kingdom	Google Twill Cap	3
United Kingdom	Google Tote Bag	3
United Kingdom	Basecamp Explorer Powerbank Flashlight	3
United Kingdom	Google Rucksack	3
United Kingdom	Android Lunch Kit	3
United Kingdom	Google Men's Quilted Insulated Vest Black	2
United Kingdom	Sport Bag	2
United Kingdom	Google Men's Short Sleeve Hero Tee Charcoal	2
United Kingdom	Google Women's Lightweight Microfleece Jacket	2
United Kingdom	Google Flashlight	2
United Kingdom	Google Sunglasses	2
United Kingdom	Bottle Opener Clip	2
United Kingdom	8 pc Android Sticker Sheet	2
United Kingdom	Google Men's Airflow 1/4 Zip Pullover Lapis	2
United Kingdom	Google Men's Performance Full Zip Jacket Black	2
United Kingdom	Android 17oz Stainless Steel Sport Bottle	2
United Kingdom	Google Tri-blend Hoodie Grey	2
United Kingdom	1 oz Hand Sanitizer	2
United Kingdom	Google Women's V-Neck Tee Charcoal	2
United Kingdom	Android Men's Vintage Tank	2
United Kingdom	Google Laptop Backpack	2
United Kingdom	Suitcase Organizer Cubes	2
United Kingdom	Google Men's Convertible Vest-Jacket Pewter	2
United Kingdom	Google Men's Long Sleeve Raglan Ocean Blue	2
United Kingdom	Google 17oz Stainless Steel Sport Bottle	2
United Kingdom	Android Rise 14 oz Mug	2
United Kingdom	Google Women's Short Sleeve Hero Tee White	2
United Kingdom	NestÂ® Cam Outdoor Security Camera - USA	2
United Kingdom	23 oz Wide Mouth Sport Bottle	2
United Kingdom	Google Men's Vintage Badge Tee Green	2
United Kingdom	Android Stretch Fit Hat	2
United Kingdom	YouTube Men's Vintage Tank	2
United Kingdom	Keyboard DOT Sticker	2
United Kingdom	Colored Pencil Set	2
United Kingdom	Windup Android	2
United Kingdom	Google Lunch Bag	2
United Kingdom	Spiral Notebook and Pen Set	2
United Kingdom	Google 22 oz Water Bottle	2
United Kingdom	YouTube Women's Short Sleeve Hero Tee Charcoal	2
United States	Google Men's 100% Cotton Short Sleeve Hero Tee White	169
United States	Google Men's 100% Cotton Short Sleeve Hero Tee Navy	100
United States	22 oz YouTube Bottle Infuser	99
United States	YouTube Twill Cap	90
United States	Google Men's 100% Cotton Short Sleeve Hero Tee Black	90
United States	YouTube Men's Short Sleeve Hero Tee Black	85
United States	YouTube Men's Short Sleeve Hero Tee Charcoal	85
United States	Galaxy Screen Cleaning Cloth	81
United States	YouTube Custom Decals	77
United States	Google Snapback Hat Black	77
United States	Google Men's Watershed Full Zip Hoodie Grey	75
United States	NestÂ® Cam Indoor Security Camera - USA	73
United States	Electronics Accessory Pouch	71
United States	Google Men's Vintage Badge Tee Black	70
United States	Google Men's  Zip Hoodie	70
United States	Google Laptop and Cell Phone Stickers	67
United States	NestÂ® Cam Outdoor Security Camera - USA	66
United States	Google Women's Short Sleeve Hero Tee Black	65
United States	Google G Noise-reducing Bluetooth Headphones	64
United States	Google Twill Cap	64
United States	Recycled Mouse Pad	63
United States	Google Men's 100% Cotton Short Sleeve Hero Tee Red	62
United States	NestÂ® Protect Smoke + CO White Battery Alarm-USA	59
United States	Google Women's Short Sleeve Hero Tee White	57
United States	NestÂ® Protect Smoke + CO White Wired Alarm-USA	57
United States	YouTube Men's Vintage Henley	56
United States	Android Sticker Sheet Ultra Removable	56
United States	YouTube Men's Vintage Tank	56
United States	Windup Android	50
United States	Waterproof Backpack	49
United States	Android Wool Heather Cap Heather/Black	49
United States	Google Lunch Bag	47
United States	Google Men's Microfiber 1/4 Zip Pullover Blue/Indigo	46
United States	Google Men's Long Sleeve Raglan Ocean Blue	45
United States	YouTube Hard Cover Journal	45
United States	Google Alpine Style Backpack	45
United States	Google Men's Quilted Insulated Vest Black	43
United States	Google 17oz Stainless Steel Sport Bottle	43
United States	Google High Capacity 10,400mAh Charger	43
United States	Bottle Opener Clip	43
United States	Google Laptop Backpack	43
United States	Suitcase Organizer Cubes	42
United States	Keyboard DOT Sticker	41
United States	Google Rucksack	41
United States	Basecamp Explorer Powerbank Flashlight	41
United States	Google Insulated Stainless Steel Bottle	41
United States	Compact Selfie Stick	41
United States	Google Men's Vintage Badge Tee White	40
United States	Android Rise 14 oz Mug	40
United States	Google Men's Convertible Vest-Jacket Pewter	39
United States	Google Tote Bag	39
United States	Seat Pack Organizer	38
United States	Android 17oz Stainless Steel Sport Bottle	38
United States	Google Men's Performance Full Zip Jacket Black	38
United States	Google Stylus Pen w/ LED Light	37
United States	1 oz Hand Sanitizer	37
United States	Android Twill Cap	36
United States	Google Tri-blend Hoodie Grey	35
United States	Google Device Holder Sticky Pad	35
United States	Google Women's Convertible Vest-Jacket Sea Foam Green	35
United States	Google Women's Lightweight Microfleece Jacket	34
United States	Android Men's Vintage Tank	33
United States	Google Flashlight	33
United States	Collapsible Shopping Bag	33
United States	Switch Tone Color Crayon Pen	32
United States	Sport Bag	32
United States	Android Men's Vintage Henley	31
United States	Google Slim Utility Travel Bag	31
United States	8 pc Android Sticker Sheet	30
United States	22 oz Android Bottle	30
United States	Rocket Flashlight	30
United States	Google Power Bank	29
United States	Google Men's Vintage Badge Tee Sage	28
United States	Red Shine 15 oz Mug	28
United States	Google Canvas Tote Natural/Navy	28
United States	26 oz Double Wall Insulated Bottle	28
United States	Android Men's Short Sleeve Tri-blend Hero Tee Grey	28
United States	Colored Pencil Set	27
United States	YouTube Youth Short Sleeve Tee Red	26
United States	Micro Wireless Earbud	26
United States	Pen Pencil & Highlighter Set	25
United States	Google Tube Power Bank	25
United States	Plastic Sliding Flashlight	25
United States	You Tube Toddler Short Sleeve Tee Red	25
United States	Google Vintage Henley Grey/Black	25
United States	Rubber Grip Ballpoint Pen 4 Pack	25
United States	Google Women's 1/4 Zip Jacket Charcoal	25
United States	Four Color Retractable Pen	24
United States	Metal Texture Roller Pen	24
United States	Google Kick Ball	24
United States	Android Lunch Kit	23
United States	Google Bib White	23
United States	Ballpoint LED Light Pen	23
United States	Clip-on Compact Charger	23
United States	Foam Can and Bottle Cooler	22
United States	SPF-15 Slim & Slender Lip Balm	22
United States	Yoga Block	21
United States	Google Doodle Decal	21
United States	Google Men's Skater Tee Charcoal	21
United States	Google Women's Short Sleeve Hero Dark Grey	21
United States	Google Women's Short Sleeve Hero Tee Red Heather	21
United States	YouTube Women's Short Sleeve Tri-blend Badge Tee Grey	20
United States	Google Device Stand	20
United States	Google Women's Short Sleeve Hero Tee Grey	20
United States	Google Men's Airflow 1/4 Zip Pullover Lapis	20
United States	Leatherette Journal	19
United States	Android Men's Long Sleeve Badge Crew Tee Heather	19
United States	Google 4400mAh Power Bank	19
United States	Google Women's 3/4 Sleeve Baseball Raglan Heather/Black	19
United States	Ballpoint Stylus Pen	19
United States	Maze Pen	18
United States	Google 5-Panel Snapback Cap	18
United States	Google Men's Bayside Graphic Tee	18
United States	Google Sunglasses	18
United States	Google Bib Red	18
United States	Google Men's Airflow 1/4 Zip Pullover Black	17
United States	23 oz Wide Mouth Sport Bottle	17
United States	Google Luggage Tag	17
United States	Google Men's Vintage Badge Tee Green	17
United States	Google Long Sleeve Raglan Badge Henley Ocean Blue	16
United States	Android Men's Engineer Short Sleeve Tee Charcoal	16
United States	Android Luggage Tag	16
United States	NestÂ® Learning Thermostat 3rd Gen-USA - White	16
United States	Google Metallic Notebook Set	15
United States	Android Men's Short Sleeve Hero Tee White	15
United States	Crunch Noise Dog Toy	15
United States	Google Women's Short Sleeve Badge Tee Grey	15
United States	Android Women's Short Sleeve Badge Tee Dark Heather	15
United States	Google 22 oz Water Bottle	15
United States	25L Classic Rucksack	15
United States	Android Women's Long Sleeve Blended Cardigan Grey	15
United States	Waze Mobile Phone Vent Mount	14
United States	Google Men's Short Sleeve Performance Badge Tee Charcoal	14
United States	Android Women's Fleece Hoodie	14
United States	Google Women's Vintage Hero Tee White	14
United States	Google Women's Vintage T-Shirt Black	14
United States	NestÂ® Learning Thermostat 3rd Gen-USA - Copper	14
United States	Google Women's Performance Full Zip Jacket Black	13
United States	Google Women's Scoop Neck Tee White	13
United States	Android Stretch Fit Hat	13
United States	Google Blackout Cap	12
United States	Google Women's 1/4 Zip Performance Pullover Black	12
United States	Google Men's Short Sleeve Performance Badge Tee Navy	12
United States	Android Hard Cover Journal	12
United States	Google Women's Hero V-Neck Tee White	12
United States	Waze Dress Socks	12
United States	Google Women's 1/4 Zip Performance Pullover Two-Tone Blue	12
United States	Spiral Notebook and Pen Set	12
United States	Waze Baby on Board Window Decal	12
United States	Google Pet Feeding Mat	11
United States	Google Women's Quilted Insulated Vest Black	11
United States	Waze Mood Ninja Window Decal	11
United States	Android RFID Journal	11
United States	Google Men's Short Sleeve Hero Tee Charcoal	10
United States	Google 2200mAh Micro Charger	10
United States	YouTube Men's Fleece Hoodie Black	10
United States	Google 25 oz Red Stainless Steel Bottle	10
United States	Waze Mood Original Window Decal	10
United States	Google Collapsible Pet Bowl	9
United States	Google Men's Skater Tee Grey	9
United States	Badge Holder	9
United States	Android Women's Short Sleeve Hero Tee Black	9
United States	Waterproof Gear Bag	9
United States	Google Men's Short Sleeve Badge Tee Charcoal	9
United States	Google Women's Scoop Neck Tee Black	9
United States	Google Infant Short Sleeve Tee White	9
United States	Google Women's Quilted Insulated Vest White	9
United States	7&quot; Dog Frisbee	9
United States	YouTube Men's Skater Tee Charcoal	8
United States	Google Onesie Red/Graphite	8
United States	Set of 3 Packing Cubes	8
United States	Micro Wireless Earbuds	8
United States	Google Women's Short Sleeve Shirt Dark Grey	8
United States	Android Infant Short Sleeve Tee Pewter	8
United States	Google Women's Convertible Vest-Jacket Black	8
United States	Google Men's Short Sleeve Performance Badge Tee Pewter	8
United States	Android BTTF Moonshot Graphic Tee	7
United States	UpCycled Handlebar Bag	7
United States	Android BTTF Cosmos Graphic Tee	6
United States	Android Men's Skater Badge Tee Charcoal	6
United States	Waze Mood Happy Window Decal	6
United States	YouTube Women's Short Sleeve Crew Tee	6
United States	Google Men's Softshell Jacket Black/Grey	6
United States	Google Women's Tee Grey	6
United States	Speed Zone Air Mesh Tote	6
United States	UpCycled Bike Saddle Bag	5
United States	Google Women's Shell Jacket Blue/Black	5
United States	Gift Card - $250.00	5
United States	Google Women's V-Neck Tee Charcoal	5
United States	Google Toddler Short Sleeve Tee Red	5
United States	Crunch-It Dog Toy	5
United States	Google Youth Short Sleeve Tee Red	5
United States	Google Women's Recycled Fabric Tee	5
United States	Google Hard Cover Journal	5
United States	Deluge Waterproof Backpack	5
United States	YouTube Women's Short Sleeve Hero Tee Charcoal	5
United States	Waze Pack of 9 Decal Set	5
United States	Google Executive Umbrella	5
United States	Satin Black Ballpoint Pen	5
United States	YouTube Men's Long & Lean Tee Charcoal	5
United States	Android Onesie Gold	5
United States	Google Women's Vintage Hero Tee Black	5
United States	Waterpoof Gear Bag	5
United States	Android 5-Panel Low Cap	5
United States	Google Women's Quilted Insulated Vest Pewter	4
United States	Koozie Can Kooler	4
United States	Mistral Rucksack	4
United States	ATOM Wireless Earbud Headset	4
United States	Google Women's Short Sleeve Hero Tee Heather	4
United States	Android BTTF Moonshot Shirt	4
United States	YouTube Sticker Sheet	4
United States	Parker Gunmetal CT Ball Pen	4
United States	Android Stretch Fit Hat Black	4
United States	YouTube Men's Eco-Jersey Henley	4
United States	Google Youth Short Sleeve T-shirt Royal Blue	4
United States	Google Youth Short Sleeve Tee White	4
United States	NestÂ® Learning Thermostat 3rd Gen-USA - Stainless Steel	4
United States	Google RFID Journal	3
United States	Android Men's Long & Lean Badge Tee Charcoal	3
United States	Kick Ball	3
United States	Oasis Backpack	3
United States	Google Toddler Short Sleeve T-shirt Grey	3
United States	Android Infant Short Sleeve Tee Pink	3
United States	Pop-a-Point Crayon	3
United States	Google Leather Journal	3
United States	Google Women's Weatherblock Shell Jacket Black	3
United States	Google Infant Short Sleeve Tee Red	3
United States	Google Youth Baseball Raglan Heather/Black	3
United States	Google Spiral Leather Journal	3
United States	Latitudes Foldaway Shopper	3
United States	Google Men's Zip Hoodie	3
United States	Gunmetal Roller Ball Pen	2
United States	Google Toddler Short Sleeve Tee White	2
United States	Blue Metallic Textured Spiral Notebook Set	2
United States	YouTube Women's Fleece Hoodie Black	2
United States	Google Women's Short Sleeve Hero Tee Sky Blue	2
United States	Google Women's Short Sleeve Performance Tee Charcoal	2
United States	22 oz Mini Mountain Bottle	2
United States	Solo Pro Backpack	2
United States	Google Women's Short Sleeve Badge Tee Navy	2
United States	Android BTTF Cosmos Shirt	2
United States	Google Infant Short Sleeve Tee Green	2
United States	Google Leather Perforated Journal	2
United States	Gift Card - $50.00	2
United States	Gift Card - $25.00	2
Uruguay	YouTube Men's Vintage Tank	2
Venezuela	YouTube Twill Cap	2
Venezuela	YouTube Hard Cover Journal	2
Vietnam	Android Men's Vintage Tank	2






**Question 5: Can we summarize the impact of revenue generated from each city/country?**

SQL Queries:
SELECT aa.country, aa.city, SUM(ck.total_ordered * aa.productprice) as total
	, ROW_NUMBER() OVER (PARTITION BY aa.country ORDER BY SUM(ck.total_ordered * aa.productprice)) as seqnum
      FROM all_sessions aa
	  INNER JOIN sales_by_sku ck
           ON aa.productsku = ck.productsku
      GROUP BY country, city



Answer:
country	city	total	seqnum
(not set)	(not set)	3730640000	1
Albania	not available in demo dataset	249500000	1
Algeria	not available in demo dataset	98910000	1
Argentina	Rosario	18990000	1
Argentina	Santa Fe	150000000	2
Argentina	Buenos Aires	729110000	3
Argentina	not available in demo dataset	4579580000	4
Armenia	not available in demo dataset	63840000	1
Australia	Los Angeles	32970000	1
Australia	Mountain View	119990000	2
Australia	Brisbane	295860000	3
Australia	Adelaide	329970000	4
Australia	Perth	848580000	5
Australia	not available in demo dataset	13270000000	6
Australia	Melbourne	14352530000	7
Australia	Sydney	24436870000	8
Austria	Vienna	439810000	1
Austria	not available in demo dataset	1600160000	2
Bahamas	(not set)	32970000	1
Bahamas	not available in demo dataset	59980000	2
Bahrain	not available in demo dataset	390770000	1
Bangladesh	(not set)	498880000	1
Bangladesh	not available in demo dataset	1583560000	2
Belarus	not available in demo dataset	250980000	1
Belgium	Antwerp	8970000	1
Belgium	Ghent	63840000	2
Belgium	Brussels	67960000	3
Belgium	not available in demo dataset	10722090000	4
Bolivia	not available in demo dataset	135920000	1
Bosnia & Herzegovina	not available in demo dataset	33980000	1
Botswana	not available in demo dataset	499950000	1
Brazil	Fortaleza	0	1
Brazil	(not set)	18990000	2
Brazil	Belo Horizonte	214570000	3
Brazil	Sao Paulo	3477320000	4
Brazil	Rio de Janeiro	3825040000	5
Brazil	not available in demo dataset	26715840000	6
Brunei	not available in demo dataset	93960000	1
Bulgaria	not available in demo dataset	1335830000	1
Cambodia	not available in demo dataset	258870000	1
Canada	St. John's	0	1
Canada	Waterloo	0	2
Canada	Edmonton	11000000	3
Canada	Calgary	58500000	4
Canada	New York	167970000	5
Canada	Kitchener	207980000	6
Canada	Quebec City	263580000	7
Canada	Mississauga	291260000	8
Canada	Burnaby	322810000	9
Canada	Vancouver	1894950000	10
Canada	Montreal	5585800000	11
Canada	Sherbrooke	23887110000	12
Canada	Toronto	29054110000	13
Canada	not available in demo dataset	1.10043E+11	14
Chile	Santiago	527170000	1
Chile	not available in demo dataset	1930190000	2
China	Beijing	0	1
China	not available in demo dataset	1593810000	2
Colombia	Medellin	368470000	1
Colombia	Bogota	2459480000	2
Colombia	not available in demo dataset	3894640000	3
Costa Rica	not available in demo dataset	3459210000	1
CÃ´te dâ€™Ivoire	(not set)	59700000	1
CÃ´te dâ€™Ivoire	not available in demo dataset	119680000	2
Croatia	Zagreb	659940000	1
Croatia	not available in demo dataset	1680450000	2
Cyprus	not available in demo dataset	109950000	1
Czechia	Prague	569400000	1
Czechia	Brno	3505810000	2
Czechia	not available in demo dataset	16167020000	3
Denmark	Copenhagen	79840000	1
Denmark	not available in demo dataset	16570300000	2
Dominican Republic	(not set)	0	1
Dominican Republic	not available in demo dataset	601520000	2
Ecuador	not available in demo dataset	603900000	1
Egypt	not available in demo dataset	1040090000	1
El Salvador	San Salvador	0	1
El Salvador	not available in demo dataset	220870000	2
Estonia	not available in demo dataset	226840000	1
Ethiopia	not available in demo dataset	1274150000	1
Finland	Helsinki	143940000	1
Finland	not available in demo dataset	361630000	2
France	Singapore	18990000	1
France	Villeneuve-d'Ascq	22990000	2
France	Marseille	67960000	3
France	Montreuil	223540000	4
France	Courbevoie	254850000	5
France	Paris	6925900000	6
France	not available in demo dataset	20569960000	7
Georgia	not available in demo dataset	254090000	1
Germany	Frankfurt	83930000	1
Germany	Berlin	617710000	2
Germany	Munich	2240010000	3
Germany	Hamburg	4488260000	4
Germany	not available in demo dataset	40013270000	5
Ghana	not available in demo dataset	254850000	1
Gibraltar	not available in demo dataset	59980000	1
Greece	Thessaloniki	83930000	1
Greece	(not set)	617930000	2
Greece	Athens	1872950000	3
Greece	not available in demo dataset	6380700000	4
Guatemala	not available in demo dataset	4345690000	1
Honduras	not available in demo dataset	22288000000	1
Hong Kong	(not set)	2757700000	1
Hong Kong	not available in demo dataset	3505810000	2
Hong Kong	Hong Kong	12299330000	3
Hungary	Istanbul	32890000	1
Hungary	Budapest	124470000	2
Hungary	not available in demo dataset	1509430000	3
Iceland	(not set)	0	1
India	Lucknow	0	1
India	Patna	5980000	2
India	Nanded	113940000	3
India	Chandigarh	220870000	4
India	Jaipur	387780000	5
India	Kharagpur	559880000	6
India	Gurgaon	678290000	7
India	Indore	1307120000	8
India	Ahmedabad	1543100000	9
India	(not set)	2134180000	10
India	New Delhi	3249930000	11
India	Kolkata	3948140000	12
India	Bengaluru	4600490000	13
India	Chennai	8146810000	14
India	Pune	8463030000	15
India	Hyderabad	12029390000	16
India	Mumbai	31488070000	17
India	not available in demo dataset	46058010000	18
Indonesia	(not set)	11980000	1
Indonesia	Bandung	113940000	2
Indonesia	Jakarta	1191440000	3
Indonesia	not available in demo dataset	7161960000	4
Iraq	not available in demo dataset	18990000	1
Ireland	Cork	59700000	1
Ireland	not available in demo dataset	4067090000	2
Ireland	Dublin	37740350000	3
Israel	not available in demo dataset	1867270000	1
Israel	Tel Aviv-Yafo	11742400000	2
Italy	Milan	1382980000	1
Italy	Rome	3965120000	2
Italy	not available in demo dataset	44347410000	3
Jamaica	not available in demo dataset	167970000	1
Japan	Shibuya	0	1
Japan	Chuo	0	2
Japan	San Francisco	0	3
Japan	Nagoya	0	4
Japan	(not set)	84950000	5
Japan	Mountain View	132930000	6
Japan	Yokohama	1064710000	7
Japan	Minato	2190240000	8
Japan	Osaka	5821860000	9
Japan	Shinjuku	6585350000	10
Japan	not available in demo dataset	35009480000	11
Jersey	not available in demo dataset	439890000	1
Jordan	not available in demo dataset	109950000	1
Kazakhstan	not available in demo dataset	214570000	1
Kenya	Nairobi	0	1
Kenya	not available in demo dataset	33980000	2
Kosovo	(not set)	16990000	1
Kuwait	not available in demo dataset	6910570000	1
Kyrgyzstan	not available in demo dataset	79840000	1
Laos	not available in demo dataset	2548300000	1
Latvia	not available in demo dataset	280810000	1
Lithuania	Vilnius	16990000	1
Lithuania	not available in demo dataset	423000000	2
Macau	not available in demo dataset	49960000	1
Macedonia (FYROM)	not available in demo dataset	506470000	1
Malaysia	Ipoh	38500000	1
Malaysia	Petaling Jaya	245940000	2
Malaysia	Kuala Lumpur	3404410000	3
Malaysia	not available in demo dataset	3746440000	4
Maldives	not available in demo dataset	119990000	1
Mali	not available in demo dataset	59700000	1
Malta	not available in demo dataset	0	1
Martinique	not available in demo dataset	111980000	1
Mauritius	not available in demo dataset	3249380000	1
Mexico	Culiacan	135920000	1
Mexico	Mexico City	1686340000	2
Mexico	not available in demo dataset	24797290000	3
Moldova	not available in demo dataset	59700000	1
Montenegro	not available in demo dataset	59700000	1
Morocco	not available in demo dataset	401140000	1
Myanmar (Burma)	not available in demo dataset	606290000	1
Nepal	not available in demo dataset	249500000	1
Nepal	(not set)	769890000	2
Netherlands	Dublin	19080000	1
Netherlands	Amsterdam	2691010000	2
Netherlands	not available in demo dataset	19960480000	3
New Zealand	Auckland	0	1
New Zealand	not available in demo dataset	4018210000	2
Nicaragua	not available in demo dataset	44950000	1
Nigeria	not available in demo dataset	548360000	1
Norway	Oslo	16990000	1
Norway	not available in demo dataset	1576570000	2
Oman	not available in demo dataset	1274150000	1
Pakistan	Karachi	0	1
Pakistan	Lahore	16990000	2
Pakistan	not available in demo dataset	8365570000	3
Palestine	(not set)	299970000	1
Panama	not available in demo dataset	1293110000	1
Papua New Guinea	not available in demo dataset	1333850000	1
Paraguay	Asuncion	220870000	1
Peru	La Victoria	717200000	1
Peru	(not set)	1064340000	2
Peru	not available in demo dataset	1930490000	3
Philippines	Makati	0	1
Philippines	(not set)	63840000	2
Philippines	Manila	97790000	3
Philippines	Quezon City	396740000	4
Philippines	Taguig	1794420000	5
Philippines	not available in demo dataset	10484110000	6
Poland	Poznan	67960000	1
Poland	Warsaw	1547900000	2
Poland	not available in demo dataset	1921510000	3
Portugal	not available in demo dataset	1843670000	1
Portugal	Lisbon	3589110000	2
Puerto Rico	(not set)	0	1
Puerto Rico	not available in demo dataset	914260000	2
Qatar	not available in demo dataset	0	1
Qatar	Doha	67960000	2
RÃ©union	(not set)	161360000	1
Romania	Iasi	59980000	1
Romania	Cluj-Napoca	67960000	2
Romania	Timisoara	183840000	3
Romania	Bucharest	1492930000	4
Romania	not available in demo dataset	6559150000	5
Russia	Moscow	660680000	1
Russia	Vladivostok	991380000	2
Russia	Saint Petersburg	4854950000	3
Russia	not available in demo dataset	12934210000	4
San Marino	(not set)	249500000	1
Saudi Arabia	Riyadh	3505810000	1
Saudi Arabia	not available in demo dataset	7228450000	2
Serbia	(not set)	38500000	1
Serbia	not available in demo dataset	328430000	2
Singapore	not available in demo dataset	637290000	1
Singapore	Singapore	6485320000	2
Singapore	(not set)	17123490000	3
Sint Maarten	(not set)	11000000	1
Slovakia	Bratislava	0	1
Slovakia	not available in demo dataset	5415330000	2
Slovenia	not available in demo dataset	1576620000	1
South Africa	Westville	349300000	1
South Africa	not available in demo dataset	5492380000	2
South Korea	not available in demo dataset	4417390000	1
South Korea	Seoul	8537760000	2
Spain	Pozuelo de Alarcon	1353990000	1
Spain	Barcelona	4766770000	2
Spain	Madrid	5836560000	3
Spain	not available in demo dataset	34947770000	4
Sri Lanka	(not set)	0	1
Sri Lanka	not available in demo dataset	394510000	2
Sri Lanka	Colombo	414790000	3
Sweden	Stockholm	2110180000	1
Sweden	not available in demo dataset	27435850000	2
Switzerland	(not set)	11000000	1
Switzerland	Zurich	1978030000	2
Switzerland	not available in demo dataset	4708840000	3
Taiwan	Zhongli District	2197160000	1
Taiwan	Longtan District	2424030000	2
Taiwan	not available in demo dataset	7689160000	3
Taiwan	(not set)	31014600000	4
Tanzania	not available in demo dataset	98910000	1
Thailand	(not set)	39980000	1
Thailand	not available in demo dataset	1087400000	2
Thailand	Bangkok	7642770000	3
Trinidad & Tobago	(not set)	1373060000	1
Tunisia	not available in demo dataset	348410000	1
Turkey	Izmir	118930000	1
Turkey	Istanbul	2243530000	2
Turkey	not available in demo dataset	7247310000	3
Uganda	not available in demo dataset	38870000	1
Ukraine	Kharkiv	75960000	1
Ukraine	Kiev	2535060000	2
Ukraine	not available in demo dataset	10327150000	3
United Arab Emirates	not available in demo dataset	687250000	1
United Arab Emirates	Dubai	4904430000	2
United Kingdom	Coventry	0	1
United Kingdom	Manchester	0	2
United Kingdom	Wrexham	38870000	3
United Kingdom	(not set)	652690000	4
United Kingdom	London	69965120000	5
United Kingdom	not available in demo dataset	92694980000	6
United States	Paris	0	1
United States	Marlboro	0	2
United States	Minneapolis	0	3
United States	Hayward	0	4
United States	Goose Creek	0	5
United States	Mexico City	0	6
United States	Tampa	0	7
United States	Indianapolis	0	8
United States	Amsterdam	0	9
United States	London	0	10
United States	Pleasanton	0	11
United States	Panama City	0	12
United States	Forest Park	0	13
United States	Toronto	0	14
United States	Bangkok	0	15
United States	South El Monte	0	16
United States	Westlake Village	0	17
United States	Council Bluffs	4770000	18
United States	Druid Hills	8970000	19
United States	Wellesley	8970000	20
United States	Piscataway Township	16990000	21
United States	Jacksonville	24950000	22
United States	Columbia	24950000	23
United States	The Dalles	25870000	24
United States	Madison	29970000	25
United States	Hong Kong	32890000	26
United States	Kansas City	37980000	27
United States	Bellingham	59700000	28
United States	Las Vegas	67960000	29
United States	Chico	69980000	30
United States	Greer	74990000	31
United States	Lake Oswego	75490000	32
United States	St. Louis	83930000	33
United States	Ashburn	98920000	34
United States	Bellflower	119400000	35
United States	Norfolk	128940000	36
United States	Jersey City	151920000	37
United States	Richardson	159960000	38
United States	Stanford	167970000	39
United States	Tempe	186780000	40
United States	Oviedo	186870000	41
United States	Santa Monica	194870000	42
United States	Detroit	210630000	43
United States	LaFayette	220870000	44
United States	Akron	220870000	45
United States	Milpitas	256820000	46
United States	Portland	334810000	47
United States	Redmond	348410000	48
United States	Boulder	404290000	49
United States	San Mateo	439890000	50
United States	University Park	499950000	51
United States	Eau Claire	539670000	52
United States	Orlando	635820000	53
United States	East Lansing	699930000	54
United States	Denver	724680000	55
United States	South San Francisco	870740000	56
United States	Oakland	976920000	57
United States	Charlotte	1313420000	58
United States	Kirkland	3051120000	59
United States	Boston	3337490000	60
United States	Sacramento	3589110000	61
United States	Avon	3627610000	62
United States	Irvine	3860850000	63
United States	Fremont	4023470000	64
United States	Dallas	4137450000	65
United States	Kalamazoo	4198950000	66
United States	Philadelphia	4393410000	67
United States	San Diego	5011070000	68
United States	Ann Arbor	6492780000	69
United States	San Antonio	6515510000	70
United States	Washington	8407050000	71
United States	Rexburg	9513990000	72
United States	Houston	10206260000	73
United States	(not set)	13387770000	74
United States	San Bruno	18289170000	75
United States	Atlanta	20134320000	76
United States	Menlo Park	20320990000	77
United States	Redwood City	20464950000	78
United States	Phoenix	20610410000	79
United States	Salem	20928160000	80
United States	Cupertino	24387820000	81
United States	Cambridge	26572220000	82
United States	Pittsburgh	29551730000	83
United States	Chicago	44880820000	84
United States	Seattle	66175160000	85
United States	Austin	68327140000	86
United States	Los Angeles	81034870000	87
United States	Santa Clara	87837450000	88
United States	San Jose	1.32302E+11	89
United States	Palo Alto	2.51565E+11	90
United States	San Francisco	2.57191E+11	91
United States	New York	2.63442E+11	92
United States	Sunnyvale	2.67192E+11	93
United States	Mountain View	9.84621E+11	94
United States	not available in demo dataset	1.39606E+12	95
Uruguay	Montevideo	254850000	1
Uruguay	not available in demo dataset	416370000	2
Venezuela	Maracaibo	76970000	1
Venezuela	not available in demo dataset	5752820000	2
Vietnam	Ho Chi Minh City	1063310000	1
Vietnam	not available in demo dataset	1885750000	2
Vietnam	Hanoi	2687870000	3
Zimbabwe	not available in demo dataset	23880000	1









