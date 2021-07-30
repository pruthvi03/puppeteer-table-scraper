# puppeteer-table-scraper

```
const {scrapTable} = require('puppeteer-table-scraper');

scrapTable(url, tableSelector, headless?, resultType?)
    .then(data => { console.log(data.resultData, data.headerKeys) } )
    .catch(err => { console.log(err) } );

```
Where,
    url: string = Url of website from which you want to scrap table
    tableSelector: string = table selector
    headless: Boolean = true or false, default true
    resultType: string = 'json', 'csv', default JavaScript array of objects

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
You can scrap *simple table* as well as *table in which header contains colspan*.
Result contains jsonData of table and column headers of table.

You can get data in three various format: Java Script Array, 'json', 'csv'. By default it will give you Java Script Array of Objects.
