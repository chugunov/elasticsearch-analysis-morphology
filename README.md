h1. Morphological Analysis Plugin for ElasticSearch

The Morphological Analysis plugin integrates <a href="https://github.com/AKuznetsov/russianmorphology">Russian and English morphology for java and lucene framework</a> into elasticsearch. This plugin adds two new analyzers: "russian_morphology" and "english_morphology" and two token filters with the same names.

The <a href="https://github.com/imotov/elasticsearch-analysis-morphology/blob/master/demo.sh">demo.sh</a> file shows a few examples of the analyzers behavior.

h2. Switching to Hunspell

For Elasticsearch version 6.0 and above there is an officially supported <a href="https://www.elastic.co/guide/en/elasticsearch/reference/current/analysis-hunspell-tokenfilter.html">hunspell</a> token filter with russian dictionaries. But in my opinion it behaves much poorer than this plugin because of limited dictionary and no predefined behavior on unknown words.


h2. Building

For building use gradle 6.7 (https://gradle.org/install/#manually) and run

<pre>
gradle build
</pre>
Java SDK 13+ required.

h2. Compatibility

Plugin is avaliable only for Elasticsearch 7.9.1.

|_. Morphological Analysis Plugin |_.  Elasticsearch   |_. URL  |
| 7.9.1                           | 7.9.1   | build yourself: gradlew build |


h2. Installation

In order to install the plugin, simply run the following command in the elasticsearch home directory:
<pre>
bin/elasticsearch-plugin install https://github.com/chugunov/elasticsearch-analysis-morphology/releases/download/v7.9.1/analysis-morphology-7.9.1.zip
</pre>
