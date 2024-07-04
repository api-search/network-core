---
name: Balancer
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/balancer.png
url: https://example.com/apis/balancer.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Balancer
apis:
  - name: elasticloadbalancing
    description: >-
      <fullname>Elastic Load Balancing</fullname> <p>A load balancer can
      distribute incoming traffic across your EC2 instances. This enables you to
      increase the availability of your application. The load balancer also
      monitors the health of its registered instances and ensures that it routes
      traffic only to healthy instances. You configure your load balancer to
      accept incoming traffic by specifying one or more listeners, which are
      configured with a protocol and port number for connections from clients to
      the load balancer and a protocol and port number for connections from the
      load balancer to the instances.</p> <p>Elastic Load Balancing supports
      three types of load balancers: Application Load Balancers, Network Load
      Balancers, and Classic Load Balancers. You can select a load balancer
      based on your application needs. For more information, see the <a
      href="https://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/">Elastic
      Load Balancing User Guide</a>.</p> <p>This reference covers the 2012-06-01
      API, which supports Classic Load Balancers. The 2015-12-01 API supports
      Application Load Balancers and Network Load Balancers.</p> <p>To get
      started, create a load balancer with one or more listeners using
      <a>CreateLoadBalancer</a>. Register your instances with the load balancer
      using <a>RegisterInstancesWithLoadBalancer</a>.</p> <p>All Elastic Load
      Balancing operations are <i>idempotent</i>, which means that they complete
      at most one time. If you repeat an operation, it succeeds with a 200 OK
      response code.</p>
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
            title: elasticloadbalancing
          paths:
            /:
              POST:
                summary: SetLoadBalancerPoliciesOfListener
                description: >-
                  <p>Replaces the current set of policies for the specified load
                  balancer port with the specified set of policies.</p> <p>To
                  enable back-end server authentication, use
                  <a>SetLoadBalancerPoliciesForBackendServer</a>.</p> <p>For
                  more information about setting policies, see <a
                  href="https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/ssl-config-update.html">Update
                  the SSL Negotiation Configuration</a>, <a
                  href="https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-sticky-sessions.html#enable-sticky-sessions-duration">Duration-Based
                  Session Stickiness</a>, and <a
                  href="https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-sticky-sessions.html#enable-sticky-sessions-application">Application-Controlled
                  Session Stickiness</a> in the <i>Classic Load Balancers Guid
                tags:
                  - Sets
                  - Load
                  - Balancer
                  - Policies
                  - Of
                  - Listen
    overlays:
      - type: APIs.io Search
        url: overlays/elasticloadbalancing-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/elasticloadbalancing-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:elasticloadbalancing
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---