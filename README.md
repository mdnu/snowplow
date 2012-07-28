# SnowPlow

## Introduction

SnowPlow is the world's most powerful web analytics platform. It does three things:

* Identifies users, and tracks the way they engage with a website or web-app
* Stores the associated data in a scalable “clickstream” data warehouse
* Makes it possible to leverage a big data toolset (e.g. Hadoop, Pig, Hive) to analyse that data

**To find out more, please check out the [SnowPlow Wiki] [wiki].**

## SnowPlow technology 101

The repository structure follows the conceptual architecture of SnowPlow, which consists of five loosely coupled stages:

![architecture] [architecture-image]

To briefly explain these five sub-systems:

* **Trackers** fire SnowPlow events. Currently we have a JavaScript tracker; iOS and Android trackers are on the roadmap
* **Collectors** capture SnowPlow events from trackers. Currently we have a simple CloudFront-based collector
* **ETL (extract, transform and load)** cleans up the raw SnowPlow events, enriches them and puts them into storage. Currently we have a Hive-based ETL process
* **Storage** is where the SnowPlow events live. Currently we store the SnowPlow events in a Hive-format flatfile structure on S3
* **Analytics** are performed on the SnowPlow events. Currently we have a set of ad hoc analyses written in Hive 

**For more information on the current SnowPlow architecture, please see the [Technical architecture] [architecture-doc]**.

## Contributing

We're committed to a loosely-coupled architecture for SnowPlow and are keen to get as many user contributions as possible in each part of the flow. If you'd like to write a new tracker, try a different ETL approach or load SnowPlow events into a different kind of database, **[get in touch] [contact]**!

## Copyright and license

SnowPlow is copyright 2012 SnowPlow Analytics Ltd. Significant portions of `snowplow.js`
are copyright 2010 Anthon Pang.

Licensed under the [Apache License, Version 2.0] [license] (the "License");
you may not use this software except in compliance with the License.

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

[wiki]: https://github.com/snowplow/snowplow/wiki
[architecture-image]: https://github.com/snowplow/snowplow/raw/features/new-structure/architecture.png
[architecture-doc]: https://github.com/snowplow/snowplow/wiki/Technical-architecture
[contact]: contribute@snowplowanalytics.com
[license]: http://www.apache.org/licenses/LICENSE-2.0