# ELK(Elasticsearch、logstash、Kibana)

## ELK 介紹

ELK 主要由三個開源軟件所組成，用於收集日誌資料、檢索資料並將資料做視覺化呈現，三個軟件的介紹如下所示：

<ul>
<li>Logstash：提供了各式各樣的日誌收集及輸出的 Plugin，可用於串接資料庫或是日誌檔案，並將資料收集處理後，輸出至 Elasticsearch。</li>
<li>Elasticsearch：分散的索引搜尋系統，可用於全文檢索，並提供 REST API 串接，ES 也是 NoSQL 資料庫的一種，所有的資料都是以 JSON 的方式進行存取。與 MongoDB 一樣都是 Document DB，但最大的不同是所有欄位都可以建立索引進行全文搜尋。</li>
<li>Kibana：可透過網頁介面來呈現資料、製作圖表，或是透過開發工具更簡易的對 elasticsearch 執行資料操作。</li>

## ELK 串接設定

Logstash 接收資料，Elasticsearch 儲存資料，Kibana 呈現資料
![architecture](/images/architecture.png)

## Reference

[https://oranwind.org/dv-elk-an-zhuang-ji-she-ding-jiao-xue/](https://oranwind.org/dv-elk-an-zhuang-ji-she-ding-jiao-xue/)