---
name: Comma
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/comma.png
url: https://example.com/apis/comma.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Comma
apis:
  - name: qldb-session
    description: >-
      <p>The transactional data APIs for Amazon QLDB</p> <note> <p>Instead of
      interacting directly with this API, we recommend using the QLDB driver or
      the QLDB shell to execute data transactions on a ledger.</p> <ul> <li>
      <p>If you are working with an AWS SDK, use the QLDB driver. The driver
      provides a high-level abstraction layer above this <i>QLDB Session</i>
      data plane and manages <code>SendCommand</code> API calls for you. For
      information and a list of supported programming languages, see <a
      href="https://docs.aws.amazon.com/qldb/latest/developerguide/getting-started-driver.html">Getting
      started with the driver</a> in the <i>Amazon QLDB Developer Guide</i>.</p>
      </li> <li> <p>If you are working with the AWS Command Line Interface (AWS
      CLI), use the QLDB shell. The shell is a command line interface that uses
      the QLDB driver to interact with a ledger. For information, see <a
      href="https://docs.aws.amazon.com/qldb/latest/developerguide/data-shell.html">Accessing
      Amazon QLDB using the QLDB shell</a>.</p> </li> </ul> </note>
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://example.com
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://example.com
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            title: qldb-session
          paths:
            /:
              POST:
                summary: SendCommand
                description: >-
                  <p>Sends a command to an Amazon QLDB ledger.</p> <note>
                  <p>Instead of interacting directly with this API, we recommend
                  using the QLDB driver or the QLDB shell to execute data
                  transactions on a ledger.</p> <ul> <li> <p>If you are working
                  with an AWS SDK, use the QLDB driver. The driver provides a
                  high-level abstraction layer above this <i>QLDB Session</i>
                  data plane and manages <code>SendCommand</code> API calls for
                  you. For information and a list of supported programming
                  languages, see <a
                  href="https://docs.aws.amazon.com/qldb/latest/developerguide/getting-started-driver.html">Getting
                  started with the driver</a> in the <i>Amazon QLDB Developer
                  Guide</i>.</p> </li> <li> <p>If you are working with the AWS
                  Command Line Interface (AWS CLI), use the QLDB shell. The
                  shell is a command line interface that uses the QLDB driver to
                  interact with a ledger. For information, see <a
                  href="https://docs.aws.amazon.com/qldb/latest/developerguide/data-shell.html">Accessing
                  Amazon QLDB using the QLDB shell</a>.</p> </li> </u
                tags:
                  - Send
                  - Comma
    overlays:
      - type: APIs.io Search
        url: overlays/qldb-session-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/qldb-session-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:qldb-session
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---