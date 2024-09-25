---
layout: post
title: 'Profiling InfluxDB Cloud Time Series API'
image: https://kinlane-productions2.s3.amazonaws.com/apis-io/influx-time-series.png
tags:
    - Time Series
    - Databases
---
[I profiled the InfluxDB time series API](https://github.com/api-search/influxdb/blob/main/apis.yml). Their cloud API is the one I profiled, and there may be other opportunity to profile their other API offerings. I was able to find the documentation and an OpenAPI, as well as a number of other common properties.

InfluxDB has all the basic resources including getting started, white papers, videos, case studies, and webinars. They also have pricing, authentication, headers, and pagination. Making for a nice mix of the business and technology of their API operations.

They have the usual support mechanisms for an API, but they also have an interesting usage of GitHub issues and templates to gather API errors, experience problems, feedback, but also security. I will write another post about this approach on API Evangelist.

You can [view the APIs.json for the InfluxDB time series API on GitHub](https://github.com/api-search/influxdb/blob/main/apis.yml). Next we'll index the OpenAPI, and see which search node we should publish the API to, making it easier to search and discover, as well as maintain in it's central repository. If this is your API, we are happy to hand over control over the repository to you to make more authoritative. 