# World Universities Database

Global universities and higher education institutions database. 10,200+ universities across 200+ countries with domains and websites.

## What is this?

This repository provides a **ready-to-use database** of world universities database with **10,239 records**. Available as SQLite database and SQL dumps — ideal for developers, data analysts, and fintech applications.

## Downloads

| Format | Description | Link |
|---|---|---|
| **SQLite** | Single database file, ready to query | [Releases](../../releases) |
| **SQL** | SQL dump, import into MySQL/PostgreSQL/etc. | [Releases](../../releases) |
| **Excel / CSV / PDF** | Formatted spreadsheets | [listbase.org](https://listbase.org/en/education/) |

## Database Schema

```sql
CREATE TABLE universities (
  name TEXT NOT NULL,
  country TEXT NOT NULL,
  alpha_two_code TEXT,
  state_province TEXT,
  domains TEXT,
  web_pages TEXT
);
CREATE INDEX idx_universities_alpha_two_code ON universities (alpha_two_code);
CREATE INDEX idx_universities_country ON universities (country);
CREATE INDEX idx_universities_name ON universities (name);
```

## Stats

- **10,239** records
- **1** datasets
- Updated: **2026-07-30**

## Preview

| name | country | alpha_two_code | state_province | domains | web_pages |
| --- | --- | --- | --- | --- | --- |
| Hellenic College of Noah | Greece | GR | Macedonia | noah.edu.gr | https://noah.edu.gr |
| Engineering Institute of Technology | Australia | AU |  | student.eit.edu.au | https://www.eit.edu.au/ |
| Universitas Nusa Putra | Indonesia | ID |  | nusaputra.ac.id | https://nusaputra.ac.id |
| Regent University College of Science and | Ghana | GH |  | regent.edu.gh | https://regent.edu.gh |
| Wroclaw Akademia Biznesu | Poland | PL |  | student.wab.edu.pl, wab.edu.pl | https://wab.edu.pl |
| Atharva College of Engineering | India | IN | Mumbai | atharvacoe.ac.in | https://atharvacoe.ac.in |
| Toronto Baptist Seminary and Bible Colle | Canada | CA | Ontario | tbs.edu | https://tbs.edu |
| Universidade Comunitária da Região de Ch | Brazil | BR |  | unochapeco.edu.br | https://unochapeco.edu.br |
| West Herts College | United Kingdom | GB |  | student.westherts.ac.uk, westherts.ac.uk | https://westherts.ac.uk |
| Bhagwan Parshuram Institute of Technolog | India | IN | Delhi | bpitindia.edu.in, bpitindia.in | http://bpitindia.ac.in |
| National Institute of Applied Sciences o | France | FR |  | insa-toulouse.fr | https://insa-toulouse.fr |
| Bugema University | Uganda | UG | Luweero | bugemauniv.ac.ug | https://bugemauniv.ac.ug/ |
| Mohamed bin Zayed University of Artifici | United Arab Emirates | AE | Abu Dhabi | mbzuai.ac.ae | https://mbzuai.ac.ae/ |
| Centro Universitário de Brasília, UNICEU | Brazil | BR |  | sempreceub.com, uniceub.br | https://www.uniceub.br |
| Kharkiv National University | Ukraine | UA |  | student.karazin.ua, karazin.ua, univer.k | https://karazin.ua, http://www.univer.kh |
| ... | ... | ... | ... | ... | ... |

*Showing 15 of 10,239 records*

## Release Files

| File | Records | Description |
|---|---|---|
| `world-universities.db` | 10,239 | SQLite database (all data) |
| `world-universities.sql` | 1-10,239 | SQL dump |


## Usage

### SQLite
```bash
sqlite3 world-universities.db "SELECT name, country, domains FROM universities WHERE country = 'Thailand' ORDER BY name;"
```

### Import SQL (MySQL)
```bash
mysql -u root -p your_database < world-universities.sql
```

### Import SQL (PostgreSQL)
```bash
psql -U postgres -d your_database -f world-universities.sql
```

## Use Cases

- **University search** — Find universities by country, state, or name
- **Email validation** — Verify academic email domains (e.g., .edu, .ac.uk)
- **Student applications** — Build university selectors for application forms
- **Research** — Analyze higher education landscape across countries
- **Data enrichment** — Enrich student/alumni data with university details

## FAQ

### How many universities are in this database?
The database contains 10,200+ universities and higher education institutions across 200+ countries worldwide.

### Does this include university websites and domains?
Yes. Each entry includes the university's web domain(s) and website URL(s), useful for email validation and academic verification.

### How often is this data updated?
The database is updated monthly. Check the [Releases](../../releases) page for the latest version.

### Can I use this data commercially?
Yes. This data is released under the [MIT License](LICENSE) — free to use for any purpose, including commercial applications.

### How do I find all universities in a country?
```sql
SELECT name, domains FROM universities WHERE country = 'Japan' ORDER BY name;
```

### How do I search by domain?
```sql
SELECT name, country FROM universities WHERE domains LIKE '%stanford.edu%';
```


## Countries (1)

| Country | Code | Records | Details |
|---|---|---|---|
| United States | United States | 2,349 | [View](countries/United States/) |
| Japan | Japan | 572 | [View](countries/Japan/) |
| India | India | 474 | [View](countries/India/) |
| China | China | 398 | [View](countries/China/) |
| Germany | Germany | 319 | [View](countries/Germany/) |
| Russian Federation | Russian Federation | 309 | [View](countries/Russian Federation/) |
| France | France | 297 | [View](countries/France/) |
| Korea, Republic of | Korea, Republic of | 244 | [View](countries/Korea, Republic of/) |
| United Kingdom | United Kingdom | 195 | [View](countries/United Kingdom/) |
| Iran | Iran | 193 | [View](countries/Iran/) |
| Indonesia | Indonesia | 192 | [View](countries/Indonesia/) |
| Turkiye | Turkiye | 192 | [View](countries/Turkiye/) |
| Brazil | Brazil | 190 | [View](countries/Brazil/) |
| Mexico | Mexico | 166 | [View](countries/Mexico/) |
| Canada | Canada | 157 | [View](countries/Canada/) |
| Malaysia | Malaysia | 145 | [View](countries/Malaysia/) |
| Poland | Poland | 137 | [View](countries/Poland/) |
| Pakistan | Pakistan | 136 | [View](countries/Pakistan/) |
| Argentina | Argentina | 121 | [View](countries/Argentina/) |
| Philippines | Philippines | 118 | [View](countries/Philippines/) |
| Nigeria | Nigeria | 115 | [View](countries/Nigeria/) |
| Colombia | Colombia | 103 | [View](countries/Colombia/) |
| Spain | Spain | 97 | [View](countries/Spain/) |
| Italy | Italy | 93 | [View](countries/Italy/) |
| Taiwan, Province of China | Taiwan, Province of China | 86 | [View](countries/Taiwan, Province of China/) |
| Switzerland | Switzerland | 76 | [View](countries/Switzerland/) |
| Ukraine | Ukraine | 75 | [View](countries/Ukraine/) |
| Bangladesh | Bangladesh | 75 | [View](countries/Bangladesh/) |
| Peru | Peru | 67 | [View](countries/Peru/) |
| Thailand | Thailand | 67 | [View](countries/Thailand/) |
| Portugal | Portugal | 66 | [View](countries/Portugal/) |
| Chile | Chile | 65 | [View](countries/Chile/) |
| Saudi Arabia | Saudi Arabia | 63 | [View](countries/Saudi Arabia/) |
| Romania | Romania | 62 | [View](countries/Romania/) |
| Australia | Australia | 58 | [View](countries/Australia/) |
| Belgium | Belgium | 51 | [View](countries/Belgium/) |
| Kenya | Kenya | 49 | [View](countries/Kenya/) |
| Viet Nam | Viet Nam | 49 | [View](countries/Viet Nam/) |
| Netherlands | Netherlands | 48 | [View](countries/Netherlands/) |
| Iraq | Iraq | 47 | [View](countries/Iraq/) |
| Austria | Austria | 46 | [View](countries/Austria/) |
| Egypt | Egypt | 44 | [View](countries/Egypt/) |
| Ecuador | Ecuador | 43 | [View](countries/Ecuador/) |
| Hungary | Hungary | 42 | [View](countries/Hungary/) |
| Afghanistan | Afghanistan | 40 | [View](countries/Afghanistan/) |
| United Arab Emirates | United Arab Emirates | 37 | [View](countries/United Arab Emirates/) |
| Bulgaria | Bulgaria | 37 | [View](countries/Bulgaria/) |
| Venezuela, Bolivarian Republic of | Venezuela, Bolivarian Republic of | 37 | [View](countries/Venezuela, Bolivarian Republic of/) |
| Sweden | Sweden | 36 | [View](countries/Sweden/) |
| Finland | Finland | 35 | [View](countries/Finland/) |
| Sudan | Sudan | 35 | [View](countries/Sudan/) |
| Belarus | Belarus | 34 | [View](countries/Belarus/) |
| Denmark | Denmark | 34 | [View](countries/Denmark/) |
| Greece | Greece | 33 | [View](countries/Greece/) |
| Morocco | Morocco | 33 | [View](countries/Morocco/) |
| Azerbaijan | Azerbaijan | 32 | [View](countries/Azerbaijan/) |
| Costa Rica | Costa Rica | 32 | [View](countries/Costa Rica/) |
| Ghana | Ghana | 31 | [View](countries/Ghana/) |
| Bolivia, Plurinational State of | Bolivia, Plurinational State of | 31 | [View](countries/Bolivia, Plurinational State of/) |
| Slovakia | Slovakia | 31 | [View](countries/Slovakia/) |
| Czech Republic | Czech Republic | 30 | [View](countries/Czech Republic/) |
| Ethiopia | Ethiopia | 30 | [View](countries/Ethiopia/) |
| Algeria | Algeria | 29 | [View](countries/Algeria/) |
| Jordan | Jordan | 29 | [View](countries/Jordan/) |
| Kazakhstan | Kazakhstan | 29 | [View](countries/Kazakhstan/) |
| South Africa | South Africa | 29 | [View](countries/South Africa/) |
| Ireland | Ireland | 27 | [View](countries/Ireland/) |
| Sri Lanka | Sri Lanka | 27 | [View](countries/Sri Lanka/) |
| Dominican Republic | Dominican Republic | 26 | [View](countries/Dominican Republic/) |
| El Salvador | El Salvador | 25 | [View](countries/El Salvador/) |
| Puerto Rico | Puerto Rico | 25 | [View](countries/Puerto Rico/) |
| Israel | Israel | 24 | [View](countries/Israel/) |
| Latvia | Latvia | 24 | [View](countries/Latvia/) |
| Lebanon | Lebanon | 24 | [View](countries/Lebanon/) |
| Norway | Norway | 24 | [View](countries/Norway/) |
| Uzbekistan | Uzbekistan | 23 | [View](countries/Uzbekistan/) |
| Cambodia | Cambodia | 21 | [View](countries/Cambodia/) |
| Tanzania, United Republic of | Tanzania, United Republic of | 20 | [View](countries/Tanzania, United Republic of/) |
| Tunisia | Tunisia | 19 | [View](countries/Tunisia/) |
| Uganda | Uganda | 18 | [View](countries/Uganda/) |
| Singapore | Singapore | 18 | [View](countries/Singapore/) |
| Cyprus | Cyprus | 17 | [View](countries/Cyprus/) |
| Lithuania | Lithuania | 17 | [View](countries/Lithuania/) |
| Nicaragua | Nicaragua | 17 | [View](countries/Nicaragua/) |
| Panama | Panama | 17 | [View](countries/Panama/) |
| Somalia | Somalia | 17 | [View](countries/Somalia/) |
| Albania | Albania | 16 | [View](countries/Albania/) |
| Bosnia and Herzegovina | Bosnia and Herzegovina | 16 | [View](countries/Bosnia and Herzegovina/) |
| Palestine, State of | Palestine, State of | 16 | [View](countries/Palestine, State of/) |
| Georgia | Georgia | 15 | [View](countries/Georgia/) |
| Hong Kong | Hong Kong | 15 | [View](countries/Hong Kong/) |
| Syrian Arab Republic | Syrian Arab Republic | 15 | [View](countries/Syrian Arab Republic/) |
| Zimbabwe | Zimbabwe | 15 | [View](countries/Zimbabwe/) |
| Paraguay | Paraguay | 14 | [View](countries/Paraguay/) |
| Cuba | Cuba | 13 | [View](countries/Cuba/) |
| Kyrgyzstan | Kyrgyzstan | 13 | [View](countries/Kyrgyzstan/) |
| Serbia | Serbia | 13 | [View](countries/Serbia/) |
| Yemen | Yemen | 13 | [View](countries/Yemen/) |
| Armenia | Armenia | 12 | [View](countries/Armenia/) |
| Bahrain | Bahrain | 12 | [View](countries/Bahrain/) |
| Croatia | Croatia | 12 | [View](countries/Croatia/) |
| Moldova, Republic of | Moldova, Republic of | 12 | [View](countries/Moldova, Republic of/) |
| Nepal | Nepal | 12 | [View](countries/Nepal/) |
| New Zealand | New Zealand | 12 | [View](countries/New Zealand/) |
| Guatemala | Guatemala | 11 | [View](countries/Guatemala/) |
| Libya | Libya | 11 | [View](countries/Libya/) |
| Mongolia | Mongolia | 11 | [View](countries/Mongolia/) |
| Oman | Oman | 11 | [View](countries/Oman/) |
| Rwanda | Rwanda | 11 | [View](countries/Rwanda/) |
| Cameroon | Cameroon | 10 | [View](countries/Cameroon/) |
| Congo, the Democratic Republic of the | Congo, the Democratic Republic of the | 10 | [View](countries/Congo, the Democratic Republic of the/) |
| Estonia | Estonia | 10 | [View](countries/Estonia/) |
| Iceland | Iceland | 10 | [View](countries/Iceland/) |
| Senegal | Senegal | 10 | [View](countries/Senegal/) |
| Botswana | Botswana | 9 | [View](countries/Botswana/) |
| Honduras | Honduras | 9 | [View](countries/Honduras/) |
| North Macedonia | North Macedonia | 9 | [View](countries/North Macedonia/) |
| Angola | Angola | 8 | [View](countries/Angola/) |
| Kuwait | Kuwait | 8 | [View](countries/Kuwait/) |
| Malawi | Malawi | 8 | [View](countries/Malawi/) |
| Mozambique | Mozambique | 8 | [View](countries/Mozambique/) |
| Zambia | Zambia | 7 | [View](countries/Zambia/) |
| Haiti | Haiti | 6 | [View](countries/Haiti/) |
| Madagascar | Madagascar | 6 | [View](countries/Madagascar/) |
| Uruguay | Uruguay | 6 | [View](countries/Uruguay/) |
| Belize | Belize | 5 | [View](countries/Belize/) |
| Myanmar | Myanmar | 5 | [View](countries/Myanmar/) |
| Holy See (Vatican City State) | Holy See (Vatican City State) | 5 | [View](countries/Holy See (Vatican City State)/) |
| Kosovo | Kosovo | 5 | [View](countries/Kosovo/) |
| Namibia | Namibia | 5 | [View](countries/Namibia/) |
| Papua New Guinea | Papua New Guinea | 5 | [View](countries/Papua New Guinea/) |
| Qatar | Qatar | 5 | [View](countries/Qatar/) |
| Côte d&#39;Ivoire | Côte d&#39;Ivoire | 4 | [View](countries/Côte d&#39;Ivoire/) |
| Fiji | Fiji | 4 | [View](countries/Fiji/) |
| Guinea | Guinea | 4 | [View](countries/Guinea/) |
| Guyana | Guyana | 4 | [View](countries/Guyana/) |
| Macao | Macao | 4 | [View](countries/Macao/) |
| Malta | Malta | 4 | [View](countries/Malta/) |
| Saint Kitts and Nevis | Saint Kitts and Nevis | 4 | [View](countries/Saint Kitts and Nevis/) |
| Sierra Leone | Sierra Leone | 4 | [View](countries/Sierra Leone/) |
| Slovenia | Slovenia | 4 | [View](countries/Slovenia/) |
| Benin | Benin | 3 | [View](countries/Benin/) |
| Brunei Darussalam | Brunei Darussalam | 3 | [View](countries/Brunei Darussalam/) |
| Burundi | Burundi | 3 | [View](countries/Burundi/) |
| Dominica | Dominica | 3 | [View](countries/Dominica/) |
| Gambia | Gambia | 3 | [View](countries/Gambia/) |
| Jamaica | Jamaica | 3 | [View](countries/Jamaica/) |
| Maldives | Maldives | 3 | [View](countries/Maldives/) |
| Tajikistan | Tajikistan | 3 | [View](countries/Tajikistan/) |
| Trinidad and Tobago | Trinidad and Tobago | 3 | [View](countries/Trinidad and Tobago/) |
| Antigua and Barbuda | Antigua and Barbuda | 2 | [View](countries/Antigua and Barbuda/) |
| Cayman Islands | Cayman Islands | 2 | [View](countries/Cayman Islands/) |
| Lao People&#39;s Democratic Republic | Lao People&#39;s Democratic Republic | 2 | [View](countries/Lao People&#39;s Democratic Republic/) |
| Liechtenstein | Liechtenstein | 2 | [View](countries/Liechtenstein/) |
| Luxembourg | Luxembourg | 2 | [View](countries/Luxembourg/) |
| Mauritius | Mauritius | 2 | [View](countries/Mauritius/) |
| Seychelles | Seychelles | 2 | [View](countries/Seychelles/) |
| South Sudan | South Sudan | 2 | [View](countries/South Sudan/) |
| Vietnam | Vietnam | 2 | [View](countries/Vietnam/) |
| Andorra | Andorra | 1 | [View](countries/Andorra/) |
| Bahamas | Bahamas | 1 | [View](countries/Bahamas/) |
| Barbados | Barbados | 1 | [View](countries/Barbados/) |
| Bermuda | Bermuda | 1 | [View](countries/Bermuda/) |
| Bhutan | Bhutan | 1 | [View](countries/Bhutan/) |
| Burkina Faso | Burkina Faso | 1 | [View](countries/Burkina Faso/) |
| Cape Verde | Cape Verde | 1 | [View](countries/Cape Verde/) |
| Central African Republic | Central African Republic | 1 | [View](countries/Central African Republic/) |
| Chad | Chad | 1 | [View](countries/Chad/) |
| Congo | Congo | 1 | [View](countries/Congo/) |
| Djibouti | Djibouti | 1 | [View](countries/Djibouti/) |
| Equatorial Guinea | Equatorial Guinea | 1 | [View](countries/Equatorial Guinea/) |
| Eritrea | Eritrea | 1 | [View](countries/Eritrea/) |
| Faroe Islands | Faroe Islands | 1 | [View](countries/Faroe Islands/) |
| French Guiana | French Guiana | 1 | [View](countries/French Guiana/) |
| French Polynesia | French Polynesia | 1 | [View](countries/French Polynesia/) |
| Gabon | Gabon | 1 | [View](countries/Gabon/) |
| Greenland | Greenland | 1 | [View](countries/Greenland/) |
| Grenada | Grenada | 1 | [View](countries/Grenada/) |
| Guadeloupe | Guadeloupe | 1 | [View](countries/Guadeloupe/) |
| Guam | Guam | 1 | [View](countries/Guam/) |
| Korea, Democratic People&#39;s Republic of | Korea, Democratic People&#39;s Republic of | 1 | [View](countries/Korea, Democratic People&#39;s Republic of/) |
| Lesotho | Lesotho | 1 | [View](countries/Lesotho/) |
| Liberia | Liberia | 1 | [View](countries/Liberia/) |
| Mali | Mali | 1 | [View](countries/Mali/) |
| Mauritania | Mauritania | 1 | [View](countries/Mauritania/) |
| Monaco | Monaco | 1 | [View](countries/Monaco/) |
| Montenegro | Montenegro | 1 | [View](countries/Montenegro/) |
| Montserrat | Montserrat | 1 | [View](countries/Montserrat/) |
| New Caledonia | New Caledonia | 1 | [View](countries/New Caledonia/) |
| Niger | Niger | 1 | [View](countries/Niger/) |
| Niue | Niue | 1 | [View](countries/Niue/) |
| Réunion | Réunion | 1 | [View](countries/Réunion/) |
| Saint Lucia | Saint Lucia | 1 | [View](countries/Saint Lucia/) |
| Saint Vincent and the Grenadines | Saint Vincent and the Grenadines | 1 | [View](countries/Saint Vincent and the Grenadines/) |
| Samoa | Samoa | 1 | [View](countries/Samoa/) |
| San Marino | San Marino | 1 | [View](countries/San Marino/) |
| Suriname | Suriname | 1 | [View](countries/Suriname/) |
| Swaziland | Swaziland | 1 | [View](countries/Swaziland/) |
| Togo | Togo | 1 | [View](countries/Togo/) |
| Turkmenistan | Turkmenistan | 1 | [View](countries/Turkmenistan/) |
| Turks and Caicos Islands | Turks and Caicos Islands | 1 | [View](countries/Turks and Caicos Islands/) |
| Virgin Islands, British | Virgin Islands, British | 1 | [View](countries/Virgin Islands, British/) |


## Browse Online

Explore and download individual datasets at **[listbase.org](https://listbase.org/en/education/)**.

## License

[MIT](LICENSE) — Free to use for any purpose.

## Source

Hipo/university-domains-list (GitHub)

---

Made with data from [ListBase.org](https://listbase.org/en/education/) — Free Reference Tables & Lists
