# ELK (Elasticsearch、logstash、Kibana)

## ELK 介紹

ELK 主要由三個開源軟件所組成，用於收集日誌資料、檢索資料並將資料做視覺化呈現。ELK Stack 已經成為目前最流行的集中式日誌解决方案，三個軟件的介紹如下所示：

<ul>
<li>Logstash：提供了各式各樣的日誌收集及輸出的 Plugin，可用於串接資料庫或是日誌檔案，並將資料收集處理後，輸出至 Elasticsearch。</li>
<li>Elasticsearch：分散的索引搜尋系統，可用於全文檢索，並提供 REST API 串接，ES 也是 NoSQL 資料庫的一種，所有的資料都是以 JSON 的方式進行存取。與 MongoDB 一樣都是 Document DB，但最大的不同是所有欄位都可以建立索引進行全文搜尋。</li>
<li>Kibana：可透過網頁介面來呈現資料、製作圖表、建立即時監控儀表板，或是透過開發工具更簡易的對 elasticsearch 執行資料操作。</li>
</ul>

## ELK 串接設定

Logstash 接收資料，Elasticsearch 儲存資料，Kibana 呈現資料
![architecture](/images/architecture.png)

## Logstash 和 Elasticsearch 串聯
![pipeline](/images/pipeline.png)

## Kibana View
![kibana](/images/kibana.png)

## Filebeat
ELK Stack 的新成員，一個輕量級開源日誌文件數據蒐集器，基於 Logstash-Forwarder 源代碼開發，是對它的替代。在需要採集日誌數據的 server 上安裝 Filebeat，並指定日誌目錄或日誌文件後，Filebeat 就能讀取數據，迅速發送到 Logstash 進行解析，亦或直接發送到 Elasticsearch 進行集中式存儲和分析。
![filebeat](/images/filebeat.png)

## Logstash with Message Queues (e.g. Kafka, Redis, RabbitMQ)
![message_queue](/images/message_queue.png)


## Reference

[https://oranwind.org/dv-elk-an-zhuang-ji-she-ding-jiao-xue/](https://oranwind.org/dv-elk-an-zhuang-ji-she-ding-jiao-xue/)

[https://blog.csdn.net/xlgen157387/article/details/56831017](https://blog.csdn.net/xlgen157387/article/details/56831017)

[https://www.ibm.com/developerworks/cn/opensource/os-cn-elk-filebeat/index.html](https://www.ibm.com/developerworks/cn/opensource/os-cn-elk-filebeat/index.html)

[https://blog.johnwu.cc/article/how-to-install-elasticsearch-logstash-and-kibana-elk-stack-on-centos-red-hat.html](https://blog.johnwu.cc/article/how-to-install-elasticsearch-logstash-and-kibana-elk-stack-on-centos-red-hat.html)

[http://puremonkey2010.blogspot.com/2017/06/elk-elasticsearch.html](http://puremonkey2010.blogspot.com/2017/06/elk-elasticsearch.html)

[https://atceiling.blogspot.com/2018/05/elk.html](https://atceiling.blogspot.com/2018/05/elk.html)
