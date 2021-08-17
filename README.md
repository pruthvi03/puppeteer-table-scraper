# puppeteer-table-scraper

```
const {scrapTable} = require('puppeteer-table-scraper');

scrapTable(url, tableSelector, headless?, resultType?)
    .then(data => { console.log(data.resultData, data.headerKeys) } )
    .catch(err => { console.log(err) } );

```
Where,<br>
    url: string = Url of website from which you want to scrap table<br>
    tableSelector: string = table selector<br>
    headless: Boolean = true or false, default true<br>
    resultType: string = 'json', 'csv', default JavaScript array of objects<br>

Result:
```
[
    {
        column1: data1,
        column2: data2,
        .
        .
        .columnN: dataN
    },
    .
    .
    .
]
```
You can scrap *simple table* as well as *table in which header contains colspan*.<br>
Result contains jsonData of table and column headers of table.<br><br>

You can get data in three various format: Java Script Array, 'json', 'csv'. By default it will give you Java Script Array of Objects.
