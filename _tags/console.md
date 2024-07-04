---
name: Console
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/console.png
url: https://example.com/apis/console.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Console
apis:
  - name: ec2-instance-connect
    description: >-
      <p>Amazon EC2 Instance Connect enables system administrators to publish
      one-time use SSH public keys to EC2, providing users a simple and secure
      way to connect to their instances.</p>
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
            title: ec2-instance-connect
          paths:
            /:
              POST:
                summary: SendSerialConsoleSSHPublicKey
                description: >-
                  <p>Pushes an SSH public key to the specified EC2 instance. The
                  key remains for 60 seconds, which gives you 60 seconds to
                  establish a serial console connection to the instance using
                  SSH. For more information, see <a
                  href="https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-serial-console.html">EC2
                  Serial Console</a> in the <i>Amazon EC2 User Guid
                tags:
                  - Send
                  - Serial
                  - Console
                  - Public
                  - null
    overlays:
      - type: APIs.io Search
        url: overlays/ec2-instance-connect-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/ec2-instance-connect-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:ec2-instance-connect
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---