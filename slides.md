---
# You can also start simply with 'default'
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: src/pexels-spacex-586019.jpg
# some information about your slides (markdown enabled)
title: "Introduction to Data Engineering: History, Lifecycle, and Practice"
info: "Intro to data engineering: history, lifecycle, and practice"
# apply unocss classes to the current slide
class: text-left
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: fade-out
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
---

# Introduction to Data Engineering: History, Lifecycle, and Practice

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: fade-out
---

# Data Engineering Defined

<div class="absolute top-1/2 transform -translate-y-1/2">

- Data engineering is the development, implementation, and maintenance of systems and processes that <text-h>take in raw data and produce high-quality, consistent information</text-h> that supports downstream use cases, such as analysis and machine learning. 
- Data engineering is the <text-h>intersection of security, data management, DataOps, data architecture, orchestration, and software engineering</text-h>. 
- A data engineer manages the data engineering lifecycle, beginning with getting data from source systems and ending with serving data for use cases, such as analysis or machine learning.

</div>

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/features/slide-scope-style
-->

<style>
h1 {
  background-color: #2B90B6;
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
text-h {
  background-color: #2B90B6;
  background-size: 100%;
  font-weight: bold;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
Here is another comment.
-->

---
transition: fade-out
---

# Evolution of the Data Engineer
## 1980 to 2000: from data warehousing to the web

- Bill Inmon coined the term data warehouse in 1989
- IBM developed SQL
- Ralph Kimball and Bill Inmon developed their data modeling techniques and approaches
- Around the mid-1990s, AOL, Yahoo, and Amazon started emerging with the dot-com bubble

<style>
h2 {
  background-color: #2B90B6;
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
text-h {
  background-color: #2B90B6;
  background-size: 100%;
  font-weight: bold;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
layout: two-cols-header
---

# Evolution of the Data Engineer
## Early 2000s: start of big data era

::left::

- Bill Inmon published his book: Building the Data Warehouse
- Ralph Kimball published his book: The Data Warehouse Toolkit: The Complete Guide to Dimensional Modeling
- Hardware prices became cheap and gets faster
- Google published a paper on Google File System in 2003
- In 2004, Google published a paper about MapReduce
- Yahoo developed Apache Hadoop in 2006
- Amazon created EC2, S3, DynamoDB, etc. 

::right::

<img src="../src/historical-cost-of-computer-memory-and-storage.png"/>

<style>
h2 {
  background-color: #2B90B6;
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
text-h {
  background-color: #2B90B6;
  background-size: 100%;
  font-weight: bold;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
layout: quote
---

<!-- <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 "> -->
<img src="../src/de-lifecycle.png" class="h-lg" />
<!-- </div> -->

---
transition: fade-out
layout: two-cols-header
---

# Data Engineering Lifecycle: <h1-bold>Generation</h1-bold>


::left::

<div class="scale-1/1">
Things to consider from the data source:

1. Data generation rate (How many events per second? How many gigabytes per hour?)
2. Data persistence (Is it stored permanently or temporarily?)
3. Data consistency
4. Data errors
5. Data duplication/deduplication
6. Data schema
7. Schema update frequency
8. Data timeliness
9. Data upstream
10. Data quality checking
11. Personal Identifiable Information
</div>

::right::

<div class="absolute inset-y-0 right-0 scale-2/3">
<img src="../src/application-database.png"/>
Application database
<img src="../src/message-queue.png"/>
Message queue
</div>


<style>
h1-bold {
  background-color: #2B90B6;
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
layout: two-cols-header
---

# Data Engineering Lifecycle: <h1-bold>Storage</h1-bold>

::left::

<div class="absolute inset-y-0 -left-120 -top-30 scale-1/4">
<img src="../src/byte-byte-go-cloud-database-cheat-sheet.jpg"/>
Cloud database cheatsheet
</div>

::right::

<div class="absolute top-1/2 transform -translate-y-1/2">
Things to consider for data storage:

1. Write & read speed
2. Storage strength & weaknesses
3. Scalability
4. Metadata generation & management
5. Data retrievability (how to query the data)
6. Data security
7. Regulatory compliance
</div>


<style>
h1-bold {
  background-color: #2B90B6;
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>


---
transition: fade-out
---

# Data Engineering Lifecycle: <h1-bold>Storage (Blob)</h1-bold>

<div class="absolute -top-35 -left-100 scale-7/20">
<img src="../src/gcs-storage-class.jpg"/>
Google Cloud Storage Classes
</div>

<div class="absolute -bottom-35 -right-85 scale-7/20">
<img src="../src/aws-s3-storage-class.jpeg"/>
Amazon Web Services  S3 Storage Class
</div>

<style>
h1-bold {
  background-color: #2B90B6;
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
layout: two-cols-header
---

# Data Engineering Lifecycle: <h1-bold>Ingestion</h1-bold>

---
transition: fade-out
layout: two-cols-header
---

# Data Engineering Lifecycle: <h1-bold>Transformation</h1-bold>