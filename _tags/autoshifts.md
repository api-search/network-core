---
name: Autoshifts
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/autoshifts.png
url: https://example.com/apis/autoshifts.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Autoshifts
apis:
  - name: arc-zonal-shift
    description: >-
      <p>Welcome to the Zonal Shift API Reference Guide for Amazon Route 53
      Application Recovery Controller (Route 53 ARC).</p> <p>You can start a
      zonal shift to move traffic for a load balancer resource away from an
      Availability Zone to help your application recover quickly from an
      impairment in an Availability Zone. For example, you can recover your
      application from a developer's bad code deployment or from an Amazon Web
      Services infrastructure failure in a single Availability Zone.</p> <p>You
      can also configure zonal autoshift for a load balancer resource. Zonal
      autoshift is a capability in Route 53 ARC where Amazon Web Services shifts
      away application resource traffic from an Availability Zone, on your
      behalf, to help reduce your time to recovery during events. Amazon Web
      Services shifts away traffic for resources that are enabled for zonal
      autoshift whenever Amazon Web Services determines that there's an issue in
      the Availability Zone that could potentially affect customers.</p> <p>To
      ensure that zonal autoshift is safe for your application, you must also
      configure practice runs when you enable zonal autoshift for a resource.
      Practice runs start weekly zonal shifts for a resource, to shift traffic
      for the resource out of an Availability Zone. Practice runs make sure, on
      a regular basis, that you have enough capacity in all the Availability
      Zones in an Amazon Web Services Region for your application to continue to
      operate normally when traffic for a resource is shifted away from one
      Availability Zone.</p> <important> <p>You must prescale resource capacity
      in all Availability Zones in the Region where your application is
      deployed, before you configure practice runs or enable zonal autoshift for
      a resource. You should not rely on scaling on demand when an autoshift or
      practice run starts. </p> </important> <p>For more information about using
      zonal shift and zonal autoshift, see the <a
      href="https://docs.aws.amazon.com/r53recovery/latest/dg/what-is-route53-recovery.html">Amazon
      Route 53 Application Recovery Controller Developer Guide</a>.</p>
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
            title: arc-zonal-shift
          paths:
            /zonalshifts/{zonalShiftId}:
              PATCH:
                summary: UpdateZonalShift
                description: >-
                  <p>Update an active zonal shift in Amazon Route 53 Application
                  Recovery Controller in your Amazon Web Services account. You
                  can update a zonal shift to set a new expiration, or edit or
                  replace the comment for the zonal shift. </p>
                tags:
                  - Update
                  - Zonal
                  - Shift
                  - Shift
                  - Identifiers
            /configuration:
              POST:
                summary: CreatePracticeRunConfiguration
                description: >-
                  <p>A practice run configuration for zonal autoshift is
                  required when you enable zonal autoshift. A practice run
                  configuration includes specifications for blocked dates and
                  blocked time windows, and for Amazon CloudWatch alarms that
                  you create to use with practice runs. The alarms that you
                  specify are an <i>outcome alarm</i>, to monitor application
                  health during practice runs and, optionally, a <i>blocking
                  alarm</i>, to block practice runs from starting.</p> <p>For
                  more information, see <a
                  href="https://docs.aws.amazon.com/r53recovery/latest/dg/arc-zonal-autoshift.considerations.html">
                  Considerations when you configure zonal autoshift</a> in the
                  Amazon Route 53 Application Recovery Controller Developer
                  Guide.</p>
                tags:
                  - Create
                  - Practice
                  - Runs
                  - Configurations
                  - Shift
                  - Identifiers
                  - Configurations
            /configuration/{resourceIdentifier}:
              PATCH:
                summary: UpdatePracticeRunConfiguration
                description: >-
                  <p>Update a practice run configuration to change one or more
                  of the following: add, change, or remove the blocking alarm;
                  change the outcome alarm; or add, change, or remove blocking
                  dates or time windows.</p>
                tags:
                  - Update
                  - Practice
                  - Runs
                  - Configurations
                  - Shift
                  - Identifiers
                  - Configurations
                  - Identifiers
            /managedresources/{resourceIdentifier}:
              PUT:
                summary: UpdateZonalAutoshiftConfiguration
                description: >-
                  <p>You can update the zonal autoshift status for a resource,
                  to enable or disable zonal autoshift. When zonal autoshift is
                  <code>ENABLED</code>, Amazon Web Services shifts away resource
                  traffic from an Availability Zone, on your behalf, when Amazon
                  Web Services determines that there's an issue in the
                  Availability Zone that could potentially affect customers.</p>
                tags:
                  - Update
                  - Zonal
                  - Autoshifts
                  - Configurations
                  - Shift
                  - Identifiers
                  - Configurations
                  - Identifiers
            /autoshifts:
              GET:
                summary: ListAutoshifts
                description: <p>Returns the active autoshifts for a specified resource.</p>
                tags:
                  - Lists
                  - Autoshifts
                  - Shift
                  - Identifiers
                  - Configurations
                  - Identifiers
                  - Autoshifts
            /managedresources:
              GET:
                summary: ListManagedResources
                description: >-
                  <p>Lists all the resources in your Amazon Web Services account
                  in this Amazon Web Services Region that are managed for zonal
                  shifts in Amazon Route 53 Application Recovery Controller, and
                  information about them. The information includes the zonal
                  autoshift status for the resource, as well as the Amazon
                  Resource Name (ARN), the Availability Zones that each resource
                  is deployed in, and the resource name.</p>
                tags:
                  - Lists
                  - Managed
                  - Resources
                  - Shift
                  - Identifiers
                  - Configurations
                  - Identifiers
                  - Autoshifts
                  - Managed Resources
            /zonalshifts:
              POST:
                summary: StartZonalShift
                description: >-
                  <p>You start a zonal shift to temporarily move load balancer
                  traffic away from an Availability Zone in an Amazon Web
                  Services Region, to help your application recover immediately,
                  for example, from a developer's bad code deployment or from an
                  Amazon Web Services infrastructure failure in a single
                  Availability Zone. You can start a zonal shift in Route 53 ARC
                  only for managed resources in your Amazon Web Services account
                  in an Amazon Web Services Region. Resources are automatically
                  registered with Route 53 ARC by Amazon Web Services
                  services.</p> <p>At this time, you can only start a zonal
                  shift for Network Load Balancers and Application Load
                  Balancers with cross-zone load balancing turned off.</p>
                  <p>When you start a zonal shift, traffic for the resource is
                  no longer routed to the Availability Zone. The zonal shift is
                  created immediately in Route 53 ARC. However, it can take a
                  short time, typically up to a few minutes, for existing,
                  in-progress connections in the Availability Zone to
                  complete.</p> <p>For more information, see <a
                  href="https://docs.aws.amazon.com/r53recovery/latest/dg/arc-zonal-shift.html">Zonal
                  shift</a> in the Amazon Route 53 Application Recovery
                  Controller Developer 
                tags:
                  - Start
                  - Zonal
                  - Shift
                  - Shift
                  - Identifiers
                  - Configurations
                  - Identifiers
                  - Autoshifts
                  - Managed Resources
                  - Zonalshif
    overlays:
      - type: APIs.io Search
        url: overlays/arc-zonal-shift-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/arc-zonal-shift-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:arc-zonal-shift
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---