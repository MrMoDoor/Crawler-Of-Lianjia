Crawler Of Lianjia,Python,Scrapy

#items_*.py 

is for independent spider in directory spiders, every time you want to creat a new spider , please add one and edit it

#lianjia_bj_zufang.py 

crawl data of lianjia_zufang data in beijing .Because the next page is generated by javascript that couldn't get it from scrapy response . So you should crawl all the urls first by lianjia_url.

#lianjia_ershou

I thought it's more simple for crawling data from json url , but the trick here is you have to use for loop and change the 'return' to 'yield' the same as above.The mistake occurs too to lianjia_bj_zufang found here finally.So sad.

#nohup

All the spiders could run with nohup.such as 'nohup scrapy crawl lianjia_ershou -o lianjia_ershou.json > nohup_lianjia_ershou.out&' .So you can run the thread in background and continue something else. More else ,you will get all the log in out file, it's so convenient for crawlers.
