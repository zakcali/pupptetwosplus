# pupptetwosplus
puppetWOS + wos2quartile-converter

nodejs backed Electron App, uses puppeteer library for automatic "Web of Knowledge" site browsing, and filters Q1-Q2-Q3-Q4-AHCI status, according to quartile dictionaries. Reads (fetches) quartile dictionaries, and advanced search (query) texts from a (instutuion's) target url

Please edit below code to read target files from your server:
```
const baseUrl='http://xxx.yyy.edu.tr/zzz/';
```

Target files are:
```
department-list.csv
author-list.csv
wosq1.txt
wosq2.txt
wosq3.txt
wosq4.txt
eissnq1.txt
eissnq2.txt
eissnq3.txt
eissnq4.txt
eissnahci.txt
issnq1.txt
issnq2.txt
issnq3.txt
issnq4.txt
issnahci.txt
```
If you know a specific article's Quartile, you obtained from InCites, you can add this article's WOS number to wosq1.txt, or wosq2.txt, or, wosq3.txt, or wosq4.txt. I obtained those lists from InCites for my institute. They're similar to "Endgame Nalimov Tablebases" in Chess. They are precise, and there is no need to look at issn/eissn dictionaries for this specific article

# Beware

Clarivate Analytics, the company owns Web of Knowledge, prevents more than 1.000.000 articles per year to be retrieved for an institution by using WokSearchLite Soap Api:
http://help.incites.clarivate.com/wosWebServicesLite/WebServicesLiteOver-viewGroup/Introduction.html

So, do not publish compiled form of puppetwosplus, unless you made a special deal with Clarivate Analytics
