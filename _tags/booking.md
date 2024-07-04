---
name: Booking
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/booking.png
url: https://example.com/apis/booking.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Booking
apis:
  - aid: amadeus:flight-create-orders
    name: Flight Create Orders
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developers.amadeus.com
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developers.amadeus.com
      - type: OpenAPI
        data:
          swagger: '2.0'
          info:
            title: Flight Create Orders
            x-tags:
              - '#travel-booking'
              - '#quick-connect'
              - '#mobile-services'
              - '#ama-for-dev'
            x-status: validated
            x-release-note:
              1.10.0:
                - Add chargeableSeat element
                - Add lastTicketingDateTime
              1.9.0:
                - Add FormIdentification into the flight-order
              1.8.0:
                - Add new source "NDC" - **only available in Enterprise**
              1.7.0:
                - >-
                  Add new PaymentBrand enum "PYTON" - **only available in
                  Enterprise**
                - >-
                  Add new OtherPaymentMethod enum "PYTON" - **only available in
                  Enterprise**
                - Add FM Commission - **only available in Enterprise**
              1.6.0:
                - >-
                  Add Margins and Discounts content from Margin Manager product
                  - **only available in Enterprise**
              1.5.0:
                - Add new General Remark enum "TOUR_CODE"
              1.4.0:
                - Add new Gender enum "UNSPECIFIED" and "UNDISCLOSED"
                - >-
                  Add EasyPay credit card brand - **only available in
                  Enterprise**
              1.3.0:
                - Add new airlineRemark subtype "ADVANCED_TICKET_TIME_LIMIT"
              1.2.0:
                - >-
                  Add new sources "LTC" and "EAC" - **only available in
                  Enterprise**
              1.1.0:
                - Add Co2Emissions information into Create flight-order reply
                - Add language in Contact for the APN feature
              1.0.0:
                - Initial version
          host: test.api.amadeus.com
          basePath: /v1
          schemes:
            - https
          consumes:
            - application/vnd.amadeus+json
          produces:
            - application/vnd.amadeus+json
          paths:
            /booking/flight-orders:
              post:
                tags:
                  - - - - Booking
                summary: Create Order associated to the Flight offers.
                description: ''
          definitions:
            Error_400:
              type: object
              properties:
                errors:
                  type: array
                  items:
                    $ref: '#/definitions/Issue'
              required:
                - errors
              example:
                errors:
                  - status: 400
                    code: 477
                    title: INVALID FORMAT
                    detail: invalid query parameter format
                    source:
                      parameter: airport
                      example: CDG
            Error_500:
              type: object
              properties:
                errors:
                  type: array
                  items:
                    $ref: '#/definitions/Issue'
              required:
                - errors
              example:
                errors:
                  - status: 500
                    code: 141
                    title: SYSTEM ERROR HAS OCCURRED
            Issue:
              type: object
              properties:
                status:
                  description: the HTTP status code applicable to this error
                  type: integer
                code:
                  description: an application-specific error code
                  type: integer
                  format: int64
                title:
                  description: a short summary of the error
                  type: string
                detail:
                  description: explanation of the error
                  type: string
                source:
                  type: object
                  title: Issue_Source
                  description: an object containing references to the source of the error
                  maxProperties: 1
                  properties:
                    pointer:
                      description: >-
                        a JSON Pointer [RFC6901] to the associated entity in the
                        request document
                      type: string
                    parameter:
                      description: >-
                        a string indicating which URI query parameter caused the
                        issue
                      type: string
                    example:
                      description: a string indicating an example of the right value
                      type: string
            Collection_Meta_Link:
              type: object
              title: Collection_Meta
              properties:
                count:
                  type: integer
                  example: 1
                links:
                  type: object
                  title: CollectionLinks
                  properties:
                    self:
                      type: string
                      format: uri
                      example: https://test.api.amadeus.com/v1/area/resources?...
                    next:
                      type: string
                      format: uri
                      example: https://test.api.amadeus.com/v1/area/resources?...
                    previous:
                      type: string
                      format: uri
                      example: https://test.api.amadeus.com/v1/area/resources?...
                    last:
                      type: string
                      format: uri
                      example: https://test.api.amadeus.com/v1/area/resources?...
                    first:
                      type: string
                      format: uri
                      example: https://test.api.amadeus.com/v1/area/resources?...
                    up:
                      type: string
                      format: uri
                      example: https://test.api.amadeus.com/v1/area/resources?...
                  example:
                    self: https://test.api.amadeus.com/v1/area/resources?param=value
            LocationEntry:
              additionalProperties:
                $ref: '#/definitions/LocationValue'
            AircraftEntry:
              additionalProperties:
                description: the manufacturer/model of aircraft
                type: string
            CurrencyEntry:
              additionalProperties:
                type: string
                example: EUR
            CarrierEntry:
              additionalProperties:
                description: the carrier name
                type: string
            FlightSegment:
              type: object
              description: >-
                defining a flight segment; including both operating and
                marketing details when applicable
              properties:
                departure:
                  $ref: '#/definitions/FlightEndPoint'
                arrival:
                  $ref: '#/definitions/FlightEndPoint'
                carrierCode:
                  type: string
                  description: providing the airline / carrier code
                  minLength: 1
                  maxLength: 2
                  example: DL
                number:
                  type: string
                  description: the flight number as assigned by the carrier
                  minLength: 1
                  maxLength: 4
                  example: '212'
                aircraft:
                  $ref: '#/definitions/AircraftEquipment'
                operating:
                  $ref: '#/definitions/OperatingFlight'
                duration:
                  type: string
                  description: >-
                    stop duration in
                    [ISO8601](https://en.wikipedia.org/wiki/ISO_8601)
                    PnYnMnDTnHnMnS format, e.g. PT2H10M
                  example: PT2H10M
                stops:
                  type: array
                  description: >-
                    information regarding the different stops composing the
                    flight segment. E.g. technical stop, change of gauge...
                  items:
                    $ref: '#/definitions/FlightStop'
            OriginalFlightEndPoint:
              type: object
              description: departure or arrival information
              properties:
                iataCode:
                  description: >-
                    [IATA airline
                    codes](http://www.iata.org/publications/Pages/code-search.aspx)
                  type: string
                  example: JFK
                terminal:
                  description: terminal name / number
                  type: string
                  example: T2
            FlightEndPoint:
              title: FlightEndPoint
              description: departure or arrival information
              allOf:
                - $ref: '#/definitions/OriginalFlightEndPoint'
                - type: object
                  properties:
                    at:
                      description: >-
                        local date and time in
                        [ISO8601](https://en.wikipedia.org/wiki/ISO_8601)
                        YYYY-MM-ddThh:mm:ss format, e.g. 2017-02-10T20:40:00
                      type: string
                      format: date-time
                      example: '2017-10-23T20:00:00'
            OriginalFlightStop:
              description: details of stops for direct or change of gauge flights
              type: object
              properties:
                iataCode:
                  description: >-
                    [IATA airline
                    codes](http://www.iata.org/publications/Pages/code-search.aspx)
                  type: string
                  example: JFK
                duration:
                  type: string
                  description: >-
                    stop duration in
                    [ISO8601](https://en.wikipedia.org/wiki/ISO_8601)
                    PnYnMnDTnHnMnS format, e.g. PT2H10M
                  example: PT2H10M
            FlightStop:
              title: FlightStop
              description: details of stops for direct or change of gauge flights
              allOf:
                - $ref: '#/definitions/OriginalFlightStop'
                - type: object
                  properties:
                    arrivalAt:
                      description: >-
                        arrival at the stop in
                        [ISO8601](https://en.wikipedia.org/wiki/ISO_8601)
                        YYYY-MM-ddThh:mm:ss format, e.g. 2017-02-10T20:40:00
                      type: string
                      format: date-time
                      example: '2017-10-23T20:00:00'
                    departureAt:
                      description: >-
                        departure from the stop in
                        [ISO8601](https://en.wikipedia.org/wiki/ISO_8601)
                        YYYY-MM-ddThh:mm:ss format, e.g. 2017-02-10T20:40:00
                      type: string
                      format: date-time
                      example: '2017-10-23T20:00:00'
            AircraftEquipment:
              description: information related to the aircraft
              properties:
                code:
                  type: string
                  description: >
                    IATA aircraft code
                    (http://www.flugzeuginfo.net/table_accodes_iata_en.php)
                  pattern: '[a-zA-Z0-9]{3}'
                  example: '318'
            OperatingFlight:
              type: object
              description: information about the operating flight
              properties:
                carrierCode:
                  type: string
                  description: providing the airline / carrier code
                  minLength: 1
                  maxLength: 2
                  example: DL
            Price:
              properties:
                currency:
                  type: string
                  example: USD
                total:
                  description: Total amount paid by the user
                  type: string
                  example: '932.70'
                base:
                  description: Amount without taxes
                  type: string
                  example: '632.70'
                fees:
                  description: List of applicable fees
                  type: array
                  items:
                    $ref: '#/definitions/Fee'
                taxes:
                  type: array
                  items:
                    $ref: '#/definitions/Tax'
                refundableTaxes:
                  description: The amount of taxes which are refundable
                  type: string
                  example: '200.00'
            Extended_Price:
              type: object
              title: Price
              description: price information
              allOf:
                - type: object
                  properties:
                    margin:
                      description: >-
                        BOOK step ONLY - The price margin percentage (plus or
                        minus) that the booking can tolerate. When set to 0,
                        then no price magin is tolerated.
                      type: string
                      example: '1.00'
                    grandTotal:
                      description: >-
                        Total amount paid by the user (including fees and
                        selected additional services).
                      type: string
                      example: '987.00'
                    billingCurrency:
                      description: >-
                        Currency of the payment. It may be different than the
                        requested currency
                      type: string
                      example: EUR
                    additionalServices:
                      type: array
                      title: AdditionalServices
                      items:
                        title: AdditionalService
                        type: object
                        properties:
                          amount:
                            type: string
                            example: '332.70'
                          type:
                            $ref: '#/definitions/AdditionalServiceType'
                - $ref: '#/definitions/Price'
            Fee:
              description: a fee
              properties:
                amount:
                  type: string
                  example: '332.70'
                type:
                  $ref: '#/definitions/FeeType'
            FeeType:
              type: string
              description: type of fee
              enum:
                - TICKETING
                - FORM_OF_PAYMENT
                - SUPPLIER
              example: TICKETING
            Tax:
              description: a tax
              type: object
              properties:
                amount:
                  type: string
                  example: '332.70'
                code:
                  type: string
                  example: MX
            TravelClass:
              description: >-
                quality of service offered in the cabin where the seat is
                located in this flight. Economy, premium economy, business or
                first class
              type: string
              enum:
                - ECONOMY
                - PREMIUM_ECONOMY
                - BUSINESS
                - FIRST
              example: PREMIUM_ECONOMY
            Co2Emission:
              type: object
              properties:
                weight:
                  description: Weight of Co2 emitted for the concerned segment
                  type: integer
                  example: 90
                weightUnit:
                  description: Code to qualify unit as pounds or kilos
                  type: string
                  example: KG
                cabin:
                  $ref: '#/definitions/TravelClass'
            FlightOffer:
              title: Flight-offer
              type: object
              required:
                - type
                - id
              properties:
                type:
                  type: string
                  description: the resource name
                  example: flight-offer
                id:
                  description: Id of the flight offer
                  type: string
                  example: '1'
                source:
                  $ref: '#/definitions/FlightOfferSource'
                instantTicketingRequired:
                  description: >-
                    If true, inform that a ticketing will be required at booking
                    step.
                  type: boolean
                  example: false
                disablePricing:
                  description: >-
                    BOOK step ONLY - If true, allows to book a PNR without
                    pricing. Only for the source "GDS"
                  type: boolean
                  example: false
                nonHomogeneous:
                  description: >-
                    If true, upon completion of the booking, this pricing
                    solution is expected to yield multiple records (a record
                    contains booking information confirmed and stored, typically
                    a Passenger Name Record (PNR), in the provider GDS or
                    system)
                  type: boolean
                  example: false
                oneWay:
                  description: >-
                    If true, the flight offer can be combined with other oneWays
                    flight-offers to complete the whole journey (one-Way
                    combinable feature).
                  type: boolean
                  example: false
                paymentCardRequired:
                  description: >-
                    If true, a payment card is mandatory to book this flight
                    offer
                  type: boolean
                  example: false
                lastTicketingDate:
                  description: >-
                    If booked on the same day as the search (with respect to
                    timezone), this flight offer is guaranteed to be thereafter
                    valid for ticketing until this date (included). Unspecified
                    when it does not make sense for this flight offer (e.g. no
                    control over ticketing once booked). YYYY-MM-DD format, e.g.
                    2019-06-07
                  type: string
                  example: '2018-06-19'
                lastTicketingDateTime:
                  description: >-
                    If booked on the same day as the search (with respect to
                    timezone), this flight offer is guaranteed to be thereafter
                    valid for ticketing until this date/time (included).
                    Unspecified when it does not make sense for this flight
                    offer (e.g. no control over ticketing once booked).
                    Information only this attribute is not used in input of
                    pricing request. Local date and time in YYYY-MM-ddThh:mm:ss
                    format, e.g. 2017-02-10T20:40:00
                  type: string
                  format: date-time
                  example: '2018-06-19T15:00:00'
                numberOfBookableSeats:
                  description: >-
                    Number of seats bookable in a single request. Can not be
                    higher than 9.
                  type: number
                  example: 9
                  minimum: 1
                  maximum: 9
                itineraries:
                  type: array
                  minItems: 1
                  maxItems: 250
                  items:
                    title: Itineraries
                    type: object
                    properties:
                      duration:
                        description: >-
                          duration in
                          [ISO8601](https://en.wikipedia.org/wiki/ISO_8601)
                          PnYnMnDTnHnMnS format, e.g. PT2H10M for a duration of
                          2h10m
                        type: string
                        example: PT2H10M
                      segments:
                        title: Segments
                        type: array
                        minItems: 1
                        maxItems: 9
                        items:
                          $ref: '#/definitions/Segment'
                    required:
                      - segments
                price:
                  $ref: '#/definitions/Extended_Price'
                pricingOptions:
                  title: PricingOptions
                  type: object
                  properties:
                    fareType:
                      description: type of fare of the flight-offer
                      $ref: '#/definitions/PricingOptionsFareType'
                    includedCheckedBagsOnly:
                      type: boolean
                      description: >-
                        If true, returns the flight-offers with included checked
                        bags only
                      example: true
                    refundableFare:
                      type: boolean
                      description: >-
                        If true, returns the flight-offers with refundable fares
                        only
                      example: true
                    noRestrictionFare:
                      type: boolean
                      description: >-
                        If true, returns the flight-offers with no restriction
                        fares only
                      example: true
                    noPenaltyFare:
                      type: boolean
                      description: >-
                        If true, returns the flight-offers with no penalty fares
                        only
                      example: true
                validatingAirlineCodes:
                  description: >-
                    This option ensures that the system will only consider
                    offers with these airlines as validating carrier.
                  type: array
                  minItems: 1
                  maxItems: 9
                  items:
                    type: string
                  example:
                    - AF
                travelerPricings:
                  title: TravelerPricings
                  description: Fare information for each traveler/segment
                  type: array
                  minItems: 1
                  maxItems: 18
                  items:
                    title: TravelerPricing
                    required:
                      - travelerId
                      - fareOption
                      - travelerType
                      - fareDetailsBySegment
                    properties:
                      travelerId:
                        type: string
                        example: '1'
                        description: Id of the traveler
                      fareOption:
                        $ref: '#/definitions/TravelerPricingFareOption'
                      travelerType:
                        $ref: '#/definitions/TravelerType'
                      associatedAdultId:
                        type: string
                        description: >-
                          if type="HELD_INFANT", corresponds to the adult
                          traveler's id who will share the seat
                      price:
                        description: price detail of the traveler
                        $ref: '#/definitions/Price'
                      fareDetailsBySegment:
                        type: array
                        minItems: 1
                        maxItems: 18
                        items:
                          title: FareDetailsBySegment
                          description: Fare details of the segment
                          required:
                            - segmentId
                          properties:
                            segmentId:
                              type: string
                              example: '1'
                              description: Id of the segment
                            cabin:
                              $ref: '#/definitions/TravelClass'
                            fareBasis:
                              description: >-
                                Fare basis specifying the rules of a fare.
                                Usually, though not always, is composed of the
                                booking class code followed by a set of letters
                                and digits representing other characteristics of
                                the ticket, such as refundability, minimum stay
                                requirements, discounts or special promotional
                                elements.
                              type: string
                              example: ANNNNF4K
                              pattern: '[[A-Z0-9]{1,18}'
                            brandedFare:
                              description: >-
                                The name of the Fare Family corresponding to the
                                fares. Only for the GDS provider and if the
                                airline has fare families filled
                              type: string
                              example: LIGHTONE
                            class:
                              description: >-
                                The code of the booking class, a.k.a. class of
                                service or Reservations/Booking Designator (RBD)
                              type: string
                              example: A
                              pattern: '[A-Z]{1}'
                            isAllotment:
                              description: >-
                                True if the corresponding booking class is in an
                                allotment
                              type: boolean
                              example: true
                            allotmentDetails:
                              $ref: '#/definitions/AllotmentDetails'
                            sliceDiceIndicator:
                              $ref: '#/definitions/SliceDiceIndicator'
                            includedCheckedBags:
                              title: includedCheckedBags
                              $ref: '#/definitions/BaggageAllowance'
                              description: Details of the included checked bags
                            additionalServices:
                              type: object
                              title: AdditionalServicesRequest
                              properties:
                                chargeableCheckedBags:
                                  title: chargeableCheckedBags
                                  description: Details of chargeable checked bags
                                  $ref: '#/definitions/ChargeableCheckdBags'
                                chargeableSeat:
                                  title: chargeableSeat
                                  description: Details of chargeable seat
                                  $ref: '#/definitions/ChargeableSeat'
                                chargeableSeatNumber:
                                  type: string
                                  description: >-
                                    DEPRECATED - use the chargeableSeat
                                    attribute -  seat number
                                  example: 33D
                                  pattern: '[1-9][0-9]{0,2}[A-Z]?'
                                otherServices:
                                  type: array
                                  description: Other services to add
                                  items:
                                    $ref: '#/definitions/ServiceName'
                                  example:
                                    - PRIORITY_BOARDING
            Segment:
              allOf:
                - type: object
                  properties:
                    id:
                      description: Id of the segment
                      type: string
                      example: 1
                    numberOfStops:
                      description: Number of stops
                      type: integer
                      example: 0
                    blacklistedInEU:
                      description: >
                        When the flight has a marketing or/and operating airline
                        that is identified as blacklisted by the European
                        Commission. 


                        To improve travel safety, the European Commission
                        regularly updates the list of the banned carriers from
                        operating in Europe. It allows any Travel Agency located
                        in the European Union to easily identify and hide any
                        travel recommendation based on some unsafe airlines. 

                        The [list of the banned
                        airlines](https://ec.europa.eu/transport/sites/transport/files/air-safety-list_en.pdf)
                        is published in the Official Journal of the European
                        Union, where they are included as annexes A and B to the
                        Commission Regulation. The blacklist of an airline can
                        concern all its flights or some specific aircraft types
                        pertaining to the airline   
                      type: boolean
                      example: false
                    co2Emissions:
                      description: Co2 informations
                      type: array
                      minItems: 1
                      items:
                        title: Co2Emission
                        $ref: '#/definitions/Co2Emission'
                - $ref: '#/definitions/FlightSegment'
            TravelerType:
              type: string
              description: >
                traveler type

                age restrictions : CHILD < 12y, HELD_INFANT < 2y, SEATED_INFANT
                < 2y, SENIOR >=60y
              enum:
                - ADULT
                - CHILD
                - SENIOR
                - YOUNG
                - HELD_INFANT
                - SEATED_INFANT
                - STUDENT
              example: ADULT
            AdditionalServiceType:
              type: string
              description: additional service type
              enum:
                - CHECKED_BAGS
                - MEALS
                - SEATS
                - OTHER_SERVICES
              example: CHECKED_BAGS
            FlightOfferSource:
              description: source of the flight offer
              type: string
              enum:
                - GDS
              example: GDS
            PricingOptionsFareType:
              type: array
              description: type of fare of the flight-offer
              items:
                type: string
                enum:
                  - PUBLISHED
              example:
                - PUBLISHED
            TravelerPricingFareOption:
              description: >
                option specifying a group of fares, which may be valid under
                certain conditons

                Can be used to specify special fare discount for a passenger
              type: string
              enum:
                - STANDARD
                - INCLUSIVE_TOUR
                - SPANISH_MELILLA_RESIDENT
                - SPANISH_CEUTA_RESIDENT
                - SPANISH_CANARY_RESIDENT
                - SPANISH_BALEARIC_RESIDENT
                - AIR_FRANCE_METROPOLITAN_DISCOUNT_PASS
                - AIR_FRANCE_DOM_DISCOUNT_PASS
                - AIR_FRANCE_COMBINED_DISCOUNT_PASS
                - AIR_FRANCE_FAMILY
                - ADULT_WITH_COMPANION
                - COMPANION
              example: STANDARD
            SliceDiceIndicator:
              description: >-
                slice and Dice indicator, such as Local Availability, Sub
                OnD(Origin and Destination) 1 Availability and Sub OnD 2
                Availability
              type: string
              enum:
                - LOCAL_AVAILABILITY
                - SUB_OD_AVAILABILITY_1
                - SUB_OD_AVAILABILITY_2
            AllotmentDetails:
              title: AllotmentDetails
              type: object
              properties:
                tourName:
                  description: The tour name agreed for this specific allotment.
                  type: string
                tourReference:
                  description: The tour reference agreed for this specific allotment.
                  type: string
            ChargeableCheckdBags:
              description: Details of chargeable checked bags
              allOf:
                - $ref: '#/definitions/BaggageAllowance'
                - type: object
                  properties:
                    id:
                      description: Id of the chargeable bag
                      type: string
                      example: '1'
            ChargeableSeat:
              description: Details of chargeable seat
              type: object
              properties:
                id:
                  description: Id of the chargeable seat
                  type: string
                  example: '1'
                number:
                  type: string
                  description: seat number
                  example: 33D
                  pattern: '[1-9][0-9]{0,2}[A-Z]?'
            Dictionaries:
              type: object
              properties:
                locations:
                  $ref: '#/definitions/LocationEntry'
                aircraft:
                  $ref: '#/definitions/AircraftEntry'
                currencies:
                  $ref: '#/definitions/CurrencyEntry'
                carriers:
                  $ref: '#/definitions/CarrierEntry'
            LocationValue:
              properties:
                cityCode:
                  type: string
                  description: City code associated to the airport
                  example: PAR
                countryCode:
                  type: string
                  description: Country code of the airport
                  example: FR
            ElementaryPrice:
              description: elementaryPrice
              type: object
              properties:
                amount:
                  type: string
                  description: >-
                    Amount of the fare. could be alpha numeric. Ex- 500.20 or
                    514.13A, 'A'signifies additional collection.
                currencyCode:
                  type: string
                  description: Currency type of the fare.
            BaggageAllowance:
              description: baggageAllowance
              type: object
              properties:
                quantity:
                  type: integer
                  description: Total number of units
                  example: 1
                weight:
                  type: integer
                  description: Weight of the baggage allowance
                  example: 20
                weightUnit:
                  type: string
                  description: Code to qualify unit as pounds or kilos
                  example: KG
            ServiceName:
              description: type of service
              type: string
              enum:
                - PRIORITY_BOARDING
                - AIRPORT_CHECKIN
              example: PRIORITY_BOARDING
            FlightOrder:
              title: FlightOrderCreateQuery
              type: object
              description: input parameter to create a flight order
              required:
                - type
                - flightOffers
              properties:
                type:
                  description: the resource name
                  type: string
                  example: flight-order
                id:
                  description: unique identifier of the flight order
                  type: string
                  example: MlpZVkFMfFdBVFNPTnwyMDE1LTExLTAy
                  readOnly: true
                queuingOfficeId:
                  description: office Id where to queue the order
                  type: string
                  example: NCE1A0955
                ownerOfficeId:
                  description: >-
                    office Id where will be transfered the ownership of the
                    order
                  type: string
                  example: NCE1A0955
                associatedRecords:
                  description: list of associated record
                  type: array
                  readOnly: true
                  items:
                    $ref: '#/definitions/AssociatedRecord'
                flightOffers:
                  description: list of flight offer
                  type: array
                  minItems: 1
                  maxItems: 6
                  items:
                    $ref: '#/definitions/FlightOffer'
                travelers:
                  description: list of travelers
                  type: array
                  minItems: 1
                  maxItems: 18
                  items:
                    $ref: '#/definitions/Traveler'
                remarks:
                  description: list of global remarks
                  $ref: '#/definitions/Remarks'
                formOfPayments:
                  description: list of form of payments
                  type: array
                  minItems: 1
                  maxItems: 6
                  readOnly: true
                  items:
                    $ref: '#/definitions/FormOfPayment'
                ticketingAgreement:
                  $ref: '#/definitions/TicketingAgreement'
                automatedProcess:
                  description: list of automatic queuing
                  type: array
                  minItems: 0
                  maxItems: 31
                  items:
                    $ref: '#/definitions/AutomatedProcess'
                contacts:
                  description: list of general contact information
                  type: array
                  items:
                    $ref: '#/definitions/Contact'
                tickets:
                  description: list of tickets
                  readOnly: true
                  type: array
                  items:
                    $ref: '#/definitions/AirTravelDocument'
                formOfIdentifications:
                  description: >-
                    list of forms of identifications applicable to travelers by
                    airline
                  type: array
                  items:
                    $ref: '#/definitions/FormOfIdentification'
            Stakeholder:
              type: object
              description: stakeholder definition
              properties:
                id:
                  description: item identifier
                  type: string
                dateOfBirth:
                  type: string
                  format: date
                  description: The date of birth in ISO 8601 format (yyyy-mm-dd)
                gender:
                  $ref: '#/definitions/StakeholderGender'
                name:
                  $ref: '#/definitions/Name'
                documents:
                  type: array
                  description: >-
                    Advanced Passenger Information - regulatory identity
                    documents - SSR DOCS & DOCO elements
                  items:
                    $ref: '#/definitions/IdentityDocument'
            StakeholderGender:
              type: string
              description: Gender for individual
              enum:
                - MALE
                - FEMALE
                - UNSPECIFIED
                - UNDISCLOSED
              title: Gender
              example: FEMALE
            IdentityDocument:
              title: traveler documents
              description: documents of the traveler
              allOf:
                - $ref: '#/definitions/Document'
                - type: object
                  properties:
                    documentType:
                      $ref: '#/definitions/DocumentType'
                    validityCountry:
                      type: string
                      description: >-
                        [ISO 3166-1
                        alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)
                        of the country where the document is valid
                      example: IN
                      pattern: '[a-zA-Z]{2}'
                    birthCountry:
                      type: string
                      description: >-
                        [ISO 3166-1
                        alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)
                        of the country of birth
                      example: FR
                      pattern: '[a-zA-Z]{2}'
                    holder:
                      type: boolean
                      description: >-
                        boolean to specify if the traveler is the holder of the
                        document
                      example: true
            Document:
              type: object
              description: the information that are found on an ID document
              properties:
                number:
                  type: string
                  description: >-
                    The document number (shown on the document) . E.g.
                    QFU514563221J
                issuanceDate:
                  type: string
                  description: Date at which the document has been issued.
                  format: date
                expiryDate:
                  type: string
                  description: Date after which the document is not valid anymore.
                  format: date
                issuanceCountry:
                  type: string
                  description: >-
                    [ISO 3166-1
                    alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)
                    of the country that issued the document
                  pattern: '[a-zA-Z]{2}'
                issuanceLocation:
                  type: string
                  description: >-
                    A more precise information concerning the place where the
                    document has been issued, when available. It may be a
                    country, a state, a city or any other type of location. e.g.
                    New-York
                nationality:
                  type: string
                  description: >-
                    [ISO 3166-1
                    alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)
                    of the nationality appearing on the document
                  pattern: '[a-zA-Z]{2}'
                birthPlace:
                  type: string
                  description: Birth place as indicated on the document
            DocumentType:
              type: string
              description: the nature/type of the document
              enum:
                - VISA
                - PASSPORT
                - IDENTITY_CARD
                - KNOWN_TRAVELER
                - REDRESS
              example: VISA
            EmergencyContact:
              type: object
              description: emergency contact number
              properties:
                addresseeName:
                  type: string
                  description: >-
                    Adressee name (e.g. in case of emergency purpose it
                    corresponds to name of the person to be contacted).
                  pattern: '[a-zA-Z -]'
                countryCode:
                  type: string
                  description: >-
                    Country code of the country (ISO3166-1). E.g. "US" for the
                    United States
                  pattern: '[A-Z]{2}'
                number:
                  type: string
                  description: >-
                    Phone number. Composed of digits only. The number of digits
                    depends on the country.
                  pattern: '[0-9]{1,15}'
                text:
                  type: string
                  description: additional details
            LoyaltyProgram:
              title: LoyaltyProgram
              description: loyalty program information
              type: object
              properties:
                programOwner:
                  type: string
                  description: loyalty program airline code
                  example: AF
                id:
                  type: string
                  description: loyalty program number
                  example: '12357466574'
            FormOfIdentification:
              type: object
              description: alternative means of identifying stakeholders for eTicket.
              properties:
                identificationType:
                  type: string
                  description: Type of identification
                  enum:
                    - DRIVERS_LICENSE
                    - PASSPORT
                    - NATIONAL_IDENTITY_CARD
                    - BOOKING_CONFIRMATION
                    - TICKET
                    - OTHER_ID
                  example: PASSPORT
                carrierCode:
                  type: string
                  description: providing the airline / carrier code
                  minLength: 1
                  maxLength: 2
                  example: DL
                number:
                  type: string
                  description: >-
                    identification number relative to the type of identification
                    either ticket number, booking number, passport number,
                    identity card number, drivers licence number, other ID
                  example: XN0019390
                travelerIds:
                  description: Ids of the concerned travelers
                  type: array
                  items:
                    type: string
                  example: '1'
                flightOfferIds:
                  description: Id of the concerned flightOffers
                  type: array
                  minItems: 1
                  maxItems: 6
                  items:
                    type: string
                  example: '1'
              title: FormOfIdentification
            Discount:
              title: Discount
              description: traveler discount
              type: object
              properties:
                subType:
                  $ref: '#/definitions/DiscountType'
                cityName:
                  type: string
                  description: city of residence
                  example: MADRID
                travelerType:
                  $ref: '#/definitions/DiscountTravelerType'
                cardNumber:
                  type: string
                  description: resident card number
                  example: 12568215Z
                  pattern: '[0-9A-Z][0-9]{0,12}[A-Z]'
                certificateNumber:
                  type: string
                  description: resident certificate number
                  example: 12568215Z
                  pattern: '[0-9A-Z][0-9]{0,12}[A-Z]'
            DiscountType:
              description: type of discount applied
              type: string
              enum:
                - SPANISH_RESIDENT
                - AIR_FRANCE_DOMESTIC
                - AIR_FRANCE_COMBINED
                - AIR_FRANCE_METROPOLITAN
              example: SPANISH_RESIDENT
            DiscountTravelerType:
              description: type of discount applied
              type: string
              enum:
                - SPANISH_CITIZEN
                - EUROPEAN_CITIZEN
                - GOVERNMENT_WORKER
                - MILITARY
                - MINOR_WITHOUT_ID
              example: SPANISH_CITIZEN
            Traveler:
              title: traveler element
              description: the traveler of the trip
              allOf:
                - $ref: '#/definitions/Stakeholder'
                - type: object
                  properties:
                    emergencyContact:
                      description: emergency contact
                      $ref: '#/definitions/EmergencyContact'
                    loyaltyPrograms:
                      description: list of loyalty program followed by the traveler
                      type: array
                      minItems: 0
                      maxItems: 10
                      items:
                        $ref: '#/definitions/LoyaltyProgram'
                    discountEligibility:
                      description: list of element that allow a discount.
                      type: array
                      minItems: 0
                      maxItems: 10
                      items:
                        $ref: '#/definitions/Discount'
                    contact:
                      $ref: '#/definitions/Contact'
            Contact:
              description: contact information
              allOf:
                - $ref: '#/definitions/ContactDictionary'
                - type: object
                  properties:
                    phones:
                      description: Phone numbers
                      type: array
                      maxItems: 3
                      items:
                        $ref: '#/definitions/Phone'
                    companyName:
                      description: Name of the company
                      type: string
                      example: AMADEUS
                    emailAddress:
                      type: string
                      description: Email address (e.g. john@smith.com)
                      example: support@mail.com
            ContactPurpose:
              description: |-
                the purpose for which this contact is to be used.
                 - STANDARD for standard use, comunication, advertissement etc...
                 - INVOICE for your invoice contact, usually its your billing adress. it's mandatory in france when you buy online
                 - STANDARD_WITHOUT_TRANSMISSION is standard contact that are not share with third party outside of Amadeus
              type: string
              enum:
                - STANDARD
                - INVOICE
                - STANDARD_WITHOUT_TRANSMISSION
            ContactDictionary:
              description: represents a contact
              type: object
              properties:
                addresseeName:
                  description: the name of the person addressed by these contact details
                  $ref: '#/definitions/Name'
                address:
                  $ref: '#/definitions/Address'
                language:
                  description: the preferred language of communication with this Contact
                  type: string
                purpose:
                  $ref: '#/definitions/ContactPurpose'
            Name:
              title: name
              description: name
              allOf:
                - $ref: '#/definitions/BaseName'
                - type: object
                  properties:
                    secondLastName:
                      description: second last name
                      type: string
            BaseName:
              type: object
              description: description of the name of a physical person
              properties:
                firstName:
                  description: First name.
                  type: string
                lastName:
                  description: Last name.
                  type: string
                middleName:
                  description: Middle name(s), for example "Lee" in "John Lee Smith".
                  type: string
            Phone:
              type: object
              description: phone information
              properties:
                deviceType:
                  $ref: '#/definitions/PhoneDeviceType'
                countryCallingCode:
                  type: string
                  description: >-
                    Country calling code of the phone number, as defined by the
                    International Communication Union. Examples - "1" for US,
                    "371" for Latvia.
                  pattern: '[0-9+]{2,5}'
                number:
                  type: string
                  description: >-
                    Phone number. Composed of digits only. The number of digits
                    depends on the country.
                  pattern: '[0-9]{1,15}'
            PhoneDeviceType:
              type: string
              description: Type of the device (Landline, Mobile or Fax)
              enum:
                - MOBILE
                - LANDLINE
                - FAX
            Address:
              type: object
              description: address information
              properties:
                lines:
                  type: array
                  description: >-
                    Line 1 = Street address, Line 2 = Apartment, suite, unit,
                    building, floor, etc 

                    Each line is limited to 35 characters
                  items:
                    type: string
                postalCode:
                  type: string
                  description: 'Example: 74130'
                countryCode:
                  type: string
                  description: >-
                    country code [ISO 3166-1 country
                    code](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)
                  pattern: '[a-zA-Z]{2}'
                cityName:
                  type: string
                  description: 'Full city name. Example: Dublin'
                  pattern: '[a-zA-Z -]{1,35}'
                stateName:
                  type: string
                  description: Full state name
                postalBox:
                  type: string
                  description: E.g. BP 220
            TicketingAgreement:
              title: Ticketing Agreement
              description: ticketing agreement
              type: object
              properties:
                option:
                  $ref: '#/definitions/TicketingAgreementOption'
                delay:
                  description: >-
                    Delay before applying automatic process if no issuance in
                    days
                  type: string
                dateTime:
                  description: >-
                    Exact date to apply automatic process if no issuance.
                    YYYY-MM-DD format, e.g. 2019-06-07
                  type: string
                  readOnly: true
                  example: '2017-10-23'
                segmentIds:
                  description: Ids of the impacted segments
                  type: array
                  readOnly: true
                  items:
                    type: string
                  example: '1'
            TicketingAgreementOption:
              description: >
                Ticketing agreement option

                * **CONFIRM**, when the payment is done

                * **DELAY_TO_QUEUE**, queue the reservation at a wished date if
                the payment is not done

                * **DELAY_TO_CANCEL**, cancel the reservation at a wished date
                if the payment is not done


                Queueing and cancellation occurs at local date and time. When no
                time is specified, reservation is queued or cancelled at 00:00.
              type: string
              enum:
                - CONFIRM
                - DELAY_TO_QUEUE
                - DELAY_TO_CANCEL
              example: DELAY_TO_QUEUE
            AutomatedProcessCommon:
              type: object
              description: >-
                Provides information on ticketing arrangements and Amadeus Time
                Limits
              properties:
                code:
                  $ref: '#/definitions/AutomatedProcessCode'
                queue:
                  title: Queue
                  type: object
                  description: >-
                    Identifies the queue onto which PNR must be automatically
                    placed upon process execution.
                  properties:
                    number:
                      type: string
                    category:
                      type: string
                text:
                  type: string
                  description: Free text
            AutomatedProcess:
              title: Automated Process
              description: automatic process applied to the Order
              allOf:
                - $ref: '#/definitions/AutomatedProcessCommon'
                - type: object
                  properties:
                    delay:
                      description: Delay before applying process in days
                      type: string
                    officeId:
                      description: Office into which the process must be triggered.
                      type: string
                      example: NCE1A0955
                    dateTime:
                      type: string
                      format: date-time
                      description: >-
                        Datetime limit at which the process takes action in case
                        issuance is not done.
            AutomatedProcessCode:
              type: string
              description: queuing action to be taken
              enum:
                - IMMEDIATE
                - DELAYED
                - ERROR
              example: IMMEDIATE
            Remarks:
              title: Remarks
              description: remarks
              type: object
              properties:
                general:
                  description: list of general remarks
                  type: array
                  minItems: 0
                  maxItems: 200
                  items:
                    $ref: '#/definitions/GeneralRemark'
                airline:
                  description: list of airline remarks
                  type: array
                  minItems: 0
                  maxItems: 200
                  items:
                    $ref: '#/definitions/AirlineRemark'
            GeneralRemark:
              title: GeneralRemark
              type: object
              required:
                - subType
                - text
              properties:
                subType:
                  $ref: '#/definitions/GeneralRemarkType'
                category:
                  description: remark category
                  type: string
                  example: Z
                  pattern: '[A-Z]{1}'
                text:
                  description: remark free text
                  type: string
                  example: PASSENGER NEED ASSISTANCE
                travelerIds:
                  description: Id of the concerned traveler
                  type: array
                  items:
                    type: string
                  example: '1'
                flightOfferIds:
                  description: Id of the concern flightOffers
                  type: array
                  minItems: 1
                  maxItems: 6
                  items:
                    type: string
                  example: '1'
            GeneralRemarkType:
              description: general remark type
              type: string
              enum:
                - GENERAL_MISCELLANEOUS
                - CONFIDENTIAL
                - INVOICE
                - QUALITY_CONTROL
                - BACKOFFICE
                - FULFILLMENT
                - ITINERARY
                - TICKETING_MISCELLANEOUS
                - TOUR_CODE
              example: GENERAL_MISCELLANEOUS
            AirlineRemark:
              title: AirlineRemark
              type: object
              required:
                - subType
                - airlineCode
                - text
              properties:
                subType:
                  $ref: '#/definitions/AirlineRemarkType'
                keyword:
                  description: keyword code - only applicable for subType Keyword
                  type: string
                  example: PARK
                airlineCode:
                  description: >
                    Code of the airline following IATA standard ([IATA table
                    codes](http://www.iata.org/publications/Pages/code-search.aspx))


                    When it apply to any airline, value is YY.
                  type: string
                  example: AF
                text:
                  description: remark free text
                  type: string
                  example: CAR PARK
                travelerIds:
                  description: Id of the concerned traveler
                  type: array
                  items:
                    type: string
                  example: '1'
                flightOfferIds:
                  description: Id of the concern flightOffers
                  type: array
                  minItems: 1
                  maxItems: 6
                  items:
                    type: string
                  example: '1'
            AirlineRemarkType:
              description: airline remark type
              type: string
              enum:
                - OTHER_SERVICE_INFORMATION
                - KEYWORD
                - OTHER_SERVICE
                - CLIENT_ID
                - ADVANCED_TICKET_TIME_LIMIT
              example: KEYWORD
            FormOfPayment:
              title: Form Of Payment
              description: form of payment used
              type: object
              properties:
                b2bWallet:
                  description: payment with the solution B2B Wallet
                  $ref: '#/definitions/B2bWallet'
                creditCard:
                  description: payment with a credit card
                  $ref: '#/definitions/CreditCard'
                other:
                  description: payment with an other method
                  $ref: '#/definitions/OtherMethod'
            B2bWallet:
              title: B2bWallet
              type: object
              description: b2b wallet
              properties:
                cardId:
                  readOnly: true
                  description: card identifier
                  type: string
                  example: '1245365895336'
                cardUsageName:
                  description: card usage name
                  type: string
                cardFriendlyName:
                  description: card name
                  type: string
                  example: CB1
                  pattern: '[a-zA-Z0-9]{1,35}'
                reportingData:
                  type: array
                  title: reportingData
                  items:
                    title: reportingData
                    type: object
                    properties:
                      name:
                        type: string
                        example: reconcil1
                      value:
                        type: string
                        example: data1
                virtualCreditCardDetails:
                  readOnly: true
                  $ref: '#/definitions/VirtualCreditCardDetails'
                flightOfferIds:
                  description: Id of the concern flightOffers
                  type: array
                  minItems: 1
                  maxItems: 6
                  items:
                    type: string
                  example: '1'
            VirtualCreditCardDetails:
              description: detail information of the virtual card
              allOf:
                - $ref: '#/definitions/CreditCardCommon'
                - $ref: '#/definitions/ElementaryPrice'
            CreditCard:
              title: creditCard
              type: object
              description: credit card
              allOf:
                - $ref: '#/definitions/CreditCardCommon'
                - type: object
                  properties:
                    securityCode:
                      description: card security code
                      type: string
                      example: '123'
                    flightOfferIds:
                      description: Id of the concern flightOffers
                      type: array
                      minItems: 1
                      maxItems: 6
                      items:
                        type: string
                      example: '1'
            CreditCardCommon:
              title: creditCardCommon
              type: object
              description: credit card common attribute
              properties:
                brand:
                  $ref: '#/definitions/CreditCardBrand'
                holder:
                  description: card holder as on the card
                  type: string
                  example: MR DUPON DAMIEN
                number:
                  description: card number
                  type: string
                  example: '4012999999999999'
                  pattern: '[a-zA-Z0-9]{1,35}'
                expiryDate:
                  description: >-
                    credit card expiration date following [ISO
                    8601](https://en.wikipedia.org/wiki/ISO_8601) (YYYY-MM
                    format, e.g. 2012-08)
                  type: string
                  example: 2021-08
            CreditCardBrand:
              description: credit card brand
              type: string
              enum:
                - VISA
                - AMERICAN_EXPRESS
                - MASTERCARD
                - VISA_ELECTRON
                - VISA_DEBIT
                - MASTERCARD_DEBIT
                - MAESTRO
                - DINERS
                - EASYPAY
              example: VISA
            OtherMethod:
              title: creditCard
              type: object
              description: other payment method
              properties:
                method:
                  $ref: '#/definitions/OtherPaymentMethod'
                flightOfferIds:
                  description: Id of the concern flightOffers
                  type: array
                  minItems: 1
                  maxItems: 6
                  items:
                    type: string
                  example: '1'
            OtherPaymentMethod:
              description: other payment method
              type: string
              enum:
                - ACCOUNT
                - CHECK
                - CASH
                - NONREFUNDABLE
              example: CASH
            AssociatedRecordCommon:
              type: object
              description: >-
                describes the relation between the current reservation and
                another one
              properties:
                reference:
                  type: string
                  description: >-
                    Record locator [Amadeus or OA] with which the current
                    reservation is related. In case of a codeshare relation, it
                    enables to identify the operating PNR.
                creationDate:
                  type: string
                  description: >-
                    Creation date of the referenced reservation. Date and time
                    in [ISO8601](https://en.wikipedia.org/wiki/ISO_8601)
                    YYYY-MM-ddThh:mm:ss.sss format, e.g. 2019-07-09T12:30:00.000
                  example: '2019-07-09T12:30:00.000'
                originSystemCode:
                  type: string
                  description: >-
                    Designates the system which has originated the referenced
                    reservation.
                  minLength: 2
                  maxLength: 3
            AssociatedRecord:
              title: associated record
              description: record associated to the order
              allOf:
                - $ref: '#/definitions/AssociatedRecordCommon'
                - type: object
                  properties:
                    flightOfferId:
                      type: string
                      description: id of the impacted flight offer
                      example: '1'
            AirTravelDocument:
              title: AirTravelDocument
              description: ticket information
              allOf:
                - $ref: '#/definitions/AirTravelDocumentCommon'
                - type: object
                  properties:
                    travelerId:
                      type: string
                      description: id of the impacted traveler
                      example: '1'
                    segmentIds:
                      description: Ids of the impacted segments
                      type: array
                      items:
                        type: string
                      example: '1'
            AirTravelDocumentCommon:
              type: object
              properties:
                documentType:
                  type: string
                  description: Type of the travel document
                  enum:
                    - ETICKET
                    - PTICKET
                    - EMD
                    - MCO
                documentNumber:
                  type: string
                  description: >-
                    Identifier of the travel document prefixed by its owner code
                    [NALC - 3 digits]. Can either be a primary or a conjunctive
                    document number. Necessary for TicketingReference
                    definition.
                documentStatus:
                  type: string
                  description: Status of the travel document contained in the fare element
                  enum:
                    - ISSUED
                    - REFUNDED
                    - VOID
                    - ORIGINAL
                    - EXCHANGED
          responses:
            '500':
              description: Unexpected error
              schema:
                $ref: '#/definitions/Error_500'
            returnFlightOrders:
              description: Successful Operation
              schema:
                title: Success_Booking
                type: object
                required:
                  - data
                properties:
                  meta:
                    $ref: '#/definitions/Collection_Meta_Link'
                  warnings:
                    type: array
                    items:
                      $ref: '#/definitions/Issue'
                  data:
                    $ref: '#/definitions/FlightOrder'
                  dictionaries:
                    $ref: '#/definitions/Dictionaries'
                example:
                  data:
                    type: flight-order
                    id: MlpZVkFMfFdBVFNPTnwyMDE1LTExLTAy
                    queuingOfficeId: NCE1A0950
                    associatedRecords:
                      - reference: 2ZYVAL
                        creationDateTime: '2018-07-13T20:17:00'
                        originSystemCode: 1A
                        flightOfferId: '1'
                    travelers:
                      - id: '1'
                        dateOfBirth: '1982-01-16'
                        name:
                          firstName: STEPHANE
                          lastName: MARTIN
                        contact:
                          phones:
                            - countryCallingCode: '33'
                              number: '487692704'
                        documents:
                          - documentType: PASSPORT
                            number: '012345678'
                            expiryDate: '2009-04-14'
                            issuanceCountry: GB
                            nationality: GB
                            holder: true
                      - id: '3'
                        dateOfBirth: '2018-03-24'
                        name:
                          firstName: JULES
                          lastName: MARTIN
                      - id: '2'
                        dateOfBirth: '2007-10-11'
                        name:
                          firstName: EMILIE
                          lastName: MARTIN
                    flightOffers:
                      - id: '1'
                        type: flight-offer
                        source: GDS
                        itineraries:
                          - duration: PT2H
                            segments:
                              - id: '1'
                                duration: PT2H
                                aircraft:
                                  code: '320'
                                numberOfStops: 0
                                blacklistedInEU: false
                                carrierCode: IB
                                operating:
                                  carrierCode: IB
                                number: '3403'
                                departure:
                                  at: '2018-09-22T10:15:00'
                                  terminal: W
                                  iataCode: ORY
                                arrival:
                                  at: '2018-09-22T12:15:00'
                                  terminal: '4'
                                  iataCode: MAD
                                co2Emissions:
                                  - weight: '100'
                                    weightUnit: KG
                                    cabin: ECONOMY
                          - duration: PT1H20M
                            segments:
                              - id: '20'
                                duration: PT1H20M
                                aircraft:
                                  code: '320'
                                numberOfStops: 0
                                blacklistedInEU: false
                                carrierCode: IB
                                operating:
                                  carrierCode: IB
                                number: '3118'
                                departure:
                                  at: '2018-09-26T23:05:00'
                                  terminal: '4'
                                  iataCode: MAD
                                arrival:
                                  at: '2018-09-26T23:25:00'
                                  terminal: '1'
                                  iataCode: LIS
                                co2Emissions:
                                  - weight: '100'
                                    weightUnit: KG
                                    cabin: ECONOMY
                          - duration: PT4H30M
                            segments:
                              - id: '30'
                                duration: PT2H
                                aircraft:
                                  code: '320'
                                numberOfStops: 0
                                blacklistedInEU: false
                                carrierCode: IB
                                operating:
                                  carrierCode: IB
                                number: '3109'
                                departure:
                                  at: '2018-10-04T12:35:00'
                                  terminal: '1'
                                  iataCode: LIS
                                arrival:
                                  at: '2018-10-04T14:55:00'
                                  terminal: '4'
                                  iataCode: MAD
                                co2Emissions:
                                  - weight: '100'
                                    weightUnit: KG
                                    cabin: ECONOMY
                              - id: '31'
                                duration: PT2H30M
                                aircraft:
                                  code: '320'
                                numberOfStops: 0
                                blacklistedInEU: false
                                carrierCode: IB
                                operating:
                                  carrierCode: IB
                                number: '3444'
                                departure:
                                  at: '2018-10-04T16:05:00'
                                  terminal: '4'
                                  iataCode: MAD
                                arrival:
                                  at: '2018-10-04T18:05:00'
                                  terminal: W
                                  iataCode: ORY
                                co2Emissions:
                                  - weight: '100'
                                    weightUnit: KG
                                    cabin: ECONOMY
                        price:
                          grandTotal: '689.21'
                          total: '423.21'
                          base: '242.00'
                          currency: EUR
                          billingCurrency: EUR
                          fees:
                            - type: SUPPLIER
                              amount: '0'
                            - type: FORM_OF_PAYMENT
                              amount: '6'
                            - type: TICKETING
                              amount: '0'
                          additionalServices:
                            - type: CHECKED_BAGS
                              amount: '100'
                            - type: SEATS
                              amount: '166'
                        pricingOptions:
                          fareType:
                            - PUBLISHED
                          includedCheckedBags: false
                        validatingAirlineCodes:
                          - IB
                        travelerPricings:
                          - travelerId: '1'
                            fareOption: STANDARD
                            travelerType: ADULT
                            price:
                              currency: EUR
                              total: '200.94'
                              base: '126'
                              taxes:
                                - code: YQ
                                  amount: '0.94'
                                - code: CJ
                                  amount: '41.67'
                                - code: FR
                                  amount: '31.33'
                            fareDetailsBySegment:
                              - segmentId: '1'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                              - segmentId: '20'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                              - segmentId: '30'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                              - segmentId: '31'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                          - travelerId: '2'
                            fareOption: STANDARD
                            travelerType: CHILD
                            price:
                              currency: EUR
                              total: '180.94'
                              base: '106'
                              taxes:
                                - code: YQ
                                  amount: '0.94'
                                - code: CJ
                                  amount: '41.67'
                                - code: FR
                                  amount: '31.33'
                            fareDetailsBySegment:
                              - segmentId: '1'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                                additionalServices:
                                  chargeableCheckedBags:
                                    quantity: 1
                                    weight: 20
                                  chargeableSeatNumber: 33D
                              - segmentId: '20'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                                additionalServices:
                                  chargeableCheckedBags:
                                    quantity: 1
                                    weight: 20
                                  chargeableSeatNumber: 28A
                              - segmentId: '30'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                                additionalServices:
                                  chargeableCheckedBags:
                                    quantity: 1
                                    weight: 20
                                  chargeableSeatNumber: 12C
                              - segmentId: '31'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                                additionalServices:
                                  chargeableCheckedBags:
                                    quantity: 1
                                    weight: 20
                                  chargeableSeatNumber: 33D
                          - travelerId: '3'
                            fareOption: STANDARD
                            travelerType: HELD_INFANT
                            associatedAdultId: '1'
                            price:
                              currency: EUR
                              total: '41.33'
                              base: '10'
                              taxes:
                                - code: FR
                                  amount: '31.33'
                            fareDetailsBySegment:
                              - segmentId: '1'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                              - segmentId: '20'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                              - segmentId: '30'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                              - segmentId: '31'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                    ticketingAggreement:
                      option: DELAY_TO_CANCEL
                      dateTime: '2018-08-21T10:15:00.000'
                    contacts:
                      - companyName: AMADEUS
                        purpose: STANDARD
                        phones:
                          - deviceType: FAX
                            countryCallingCode: '33'
                            number: '480080070'
                          - deviceType: LANDLINE
                            countryCallingCode: '33'
                            number: '480080070'
                        emailAddress: support@mail.com
                        address:
                          lines:
                            - 485 route du Pin Montard
                          postalCode: '06902'
                          cityName: Sophia Antipolis Cedex
                          countryCode: FR
                  dictionaries:
                    locations:
                      CDG:
                        cityCode: PAR
                        countryCode: FR
                      ORY:
                        cityCode: PAR
                        countryCode: FR
                      MAD:
                        cityCode: MAD
                        countryCode: ES
            400_Book:
              description: |
                code    | title                                 
                - | - 
                477     | INVALID FORMAT
                1304    | CREDIT CARD NOT ACCEPTED
                2781    | INVALID LENGTH
                4926    | INVALID DATA RECEIVED
                9112    | TICKETING - TKT
                2668    | PARAMETER COMBINATION INVALID/RESTRICTED
                32171   | MANDATORY DATA MISSING
                34107   | NOT APPLICABLE FARE
                34651   | SEGMENT SELL FAILURE
                34733   | VIRTUAL CARD CREATION FAILED
                36870   | BOOKING FAILED
                37200   | PRICE DISCREPANCY
                38034   | ONE OR MORE SERVICES ARE NOT AVAILABLE
              schema:
                $ref: '#/definitions/Error_400'
          x-generatedAt: '2023-02-01T12:47:28.953Z'
          tags: []
    overlays:
      - type: APIs.io Search
        url: overlays/flight-create-orders-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/flight-create-orders-openapi-api-evangelist-ratings.yml
  - aid: amadeus:flight-order-management
    name: Flight Order Management
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developers.amadeus.com
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developers.amadeus.com
      - type: OpenAPI
        data:
          swagger: '2.0'
          info:
            title: Flight Order Management
            x-tags:
              - '#online-retail'
              - '#mobile-services'
              - '#ama-for-dev'
            x-status: validated
            x-release-note:
              1.10.0:
                - Add chargeableSeat element
                - Add lastTicketingDateTime
              1.9.0:
                - Add FormIdentification into the flight-order
              1.8.0:
                - Add new source "NDC" - **only available in Enterprise**
              1.7.0:
                - >-
                  Add new PaymentBrand enum "PYTON" - **only available in
                  Enterprise**
                - >-
                  Add new OtherPaymentMethod enum "PYTON" - **only available in
                  Enterprise**
                - Add FM Commission - **only available in Enterprise**
              1.6.0:
                - Add BookingStatus information
                - Add included Meals content
                - >-
                  Add extra bags options on Get Flight Order - **only available
                  in Enterprise**
                - >-
                  Add Margins and Discounts content from Margin Manager product
                  - **only available in Enterprise**
              1.5.0:
                - Add new Gender enum "UNSPECIFIED" and "UNDISCLOSED"
                - >-
                  Add EasyPay credit card brand - **only available in
                  Enterprise**
              1.4.0:
                - Add new airlineRemark subtype "ADVANCED_TICKET_TIME_LIMIT"
              1.3.0:
                - >-
                  Add new sources "LTC" and "EAC" - **only available in
                  Enterprise**
              1.2.0:
                - >-
                  Add PATCH flight Order End point - **only available in
                  Enterprise**
              1.1.0:
                - Add Delete flight Order End point
                - >-
                  Add Patch flight Order End Point - **only available in
                  Enterprise**
              1.0.0:
                - Initial version
          host: test.api.amadeus.com
          basePath: /v1
          schemes:
            - https
          consumes:
            - application/vnd.amadeus+json
          produces:
            - application/vnd.amadeus+json
          paths:
            /booking/flight-orders/{flight-orderId}:
              parameters:
                - null
              get:
                tags:
                  - - - - Booking
                summary: Retrieve a given flight order
                description: ''
              delete:
                tags:
                  - - - - Booking
                summary: Cancel a given flight order
                description: ''
          definitions:
            Error_400:
              type: object
              properties:
                errors:
                  type: array
                  items:
                    $ref: '#/definitions/Issue'
              required:
                - errors
              example:
                errors:
                  - status: 400
                    code: 477
                    title: INVALID FORMAT
                    detail: invalid query parameter format
                    source:
                      parameter: airport
                      example: CDG
            Error_404:
              type: object
              properties:
                errors:
                  type: array
                  items:
                    $ref: '#/definitions/Issue'
              required:
                - errors
              example:
                errors:
                  - status: 404
                    code: 1797
                    title: NOT FOUND
                    detail: no response found for this query parameter
                    source:
                      parameter: airport
            Error_500:
              type: object
              properties:
                errors:
                  type: array
                  items:
                    $ref: '#/definitions/Issue'
              required:
                - errors
              example:
                errors:
                  - status: 500
                    code: 141
                    title: SYSTEM ERROR HAS OCCURRED
            Issue:
              type: object
              properties:
                status:
                  description: the HTTP status code applicable to this error
                  type: integer
                code:
                  description: an application-specific error code
                  type: integer
                  format: int64
                title:
                  description: a short summary of the error
                  type: string
                detail:
                  description: explanation of the error
                  type: string
                source:
                  type: object
                  title: Issue_Source
                  description: an object containing references to the source of the error
                  maxProperties: 1
                  properties:
                    pointer:
                      description: >-
                        a JSON Pointer [RFC6901] to the associated entity in the
                        request document
                      type: string
                    parameter:
                      description: >-
                        a string indicating which URI query parameter caused the
                        issue
                      type: string
                    example:
                      description: a string indicating an example of the right value
                      type: string
            Collection_Meta_Link:
              type: object
              title: Collection_Meta
              properties:
                count:
                  type: integer
                  example: 1
                links:
                  type: object
                  title: CollectionLinks
                  properties:
                    self:
                      type: string
                      format: uri
                      example: https://test.api.amadeus.com/v1/area/resources?...
                    next:
                      type: string
                      format: uri
                      example: https://test.api.amadeus.com/v1/area/resources?...
                    previous:
                      type: string
                      format: uri
                      example: https://test.api.amadeus.com/v1/area/resources?...
                    last:
                      type: string
                      format: uri
                      example: https://test.api.amadeus.com/v1/area/resources?...
                    first:
                      type: string
                      format: uri
                      example: https://test.api.amadeus.com/v1/area/resources?...
                    up:
                      type: string
                      format: uri
                      example: https://test.api.amadeus.com/v1/area/resources?...
                  example:
                    self: https://test.api.amadeus.com/v1/area/resources?param=value
            LocationEntry:
              additionalProperties:
                $ref: '#/definitions/LocationValue'
            AircraftEntry:
              additionalProperties:
                description: the manufacturer/model of aircraft
                type: string
            CurrencyEntry:
              additionalProperties:
                type: string
                example: EUR
            CarrierEntry:
              additionalProperties:
                description: the carrier name
                type: string
            FlightSegment:
              type: object
              description: >-
                defining a flight segment; including both operating and
                marketing details when applicable
              properties:
                departure:
                  $ref: '#/definitions/FlightEndPoint'
                arrival:
                  $ref: '#/definitions/FlightEndPoint'
                carrierCode:
                  type: string
                  description: providing the airline / carrier code
                  minLength: 1
                  maxLength: 2
                  example: DL
                number:
                  type: string
                  description: the flight number as assigned by the carrier
                  minLength: 1
                  maxLength: 4
                  example: '212'
                aircraft:
                  $ref: '#/definitions/AircraftEquipment'
                operating:
                  $ref: '#/definitions/OperatingFlight'
                duration:
                  type: string
                  description: >-
                    stop duration in
                    [ISO8601](https://en.wikipedia.org/wiki/ISO_8601)
                    PnYnMnDTnHnMnS format, e.g. PT2H10M
                  example: PT2H10M
                stops:
                  type: array
                  description: >-
                    information regarding the different stops composing the
                    flight segment. E.g. technical stop, change of gauge...
                  items:
                    $ref: '#/definitions/FlightStop'
                bookingStatus:
                  description: booking status of the segment
                  type: string
                  enum:
                    - CONFIRMED
                    - WAITLISTED
                    - CANCELLED
                    - PENDING
                    - DENIED
                  example: CONFIRMED
                segmentType:
                  description: type of the segment
                  type: string
                  enum:
                    - ACTIVE
                    - PASSIVE
                    - GHOST
                    - STAFF
                  example: GHOST
                isFlown:
                  type: boolean
                  description: indicator set to true if segment is flown
                  example: true
            OriginalFlightEndPoint:
              type: object
              description: departure or arrival information
              properties:
                iataCode:
                  description: >-
                    [IATA airline
                    codes](http://www.iata.org/publications/Pages/code-search.aspx)
                  type: string
                  example: JFK
                terminal:
                  description: terminal name / number
                  type: string
                  example: T2
            FlightEndPoint:
              title: FlightEndPoint
              description: departure or arrival information
              allOf:
                - $ref: '#/definitions/OriginalFlightEndPoint'
                - type: object
                  properties:
                    at:
                      description: >-
                        local date and time in
                        [ISO8601](https://en.wikipedia.org/wiki/ISO_8601)
                        YYYY-MM-ddThh:mm:ss format, e.g. 2017-02-10T20:40:00
                      type: string
                      format: date-time
                      example: '2017-10-23T20:00:00'
            OriginalFlightStop:
              description: details of stops for direct or change of gauge flights
              type: object
              properties:
                iataCode:
                  description: >-
                    [IATA airline
                    codes](http://www.iata.org/publications/Pages/code-search.aspx)
                  type: string
                  example: JFK
                duration:
                  type: string
                  description: >-
                    stop duration in
                    [ISO8601](https://en.wikipedia.org/wiki/ISO_8601)
                    PnYnMnDTnHnMnS format, e.g. PT2H10M
                  example: PT2H10M
            FlightStop:
              title: FlightStop
              description: details of stops for direct or change of gauge flights
              allOf:
                - $ref: '#/definitions/OriginalFlightStop'
                - type: object
                  properties:
                    arrivalAt:
                      description: >-
                        arrival at the stop in
                        [ISO8601](https://en.wikipedia.org/wiki/ISO_8601)
                        YYYY-MM-ddThh:mm:ss format, e.g. 2017-02-10T20:40:00
                      type: string
                      format: date-time
                      example: '2017-10-23T20:00:00'
                    departureAt:
                      description: >-
                        departure from the stop in
                        [ISO8601](https://en.wikipedia.org/wiki/ISO_8601)
                        YYYY-MM-ddThh:mm:ss format, e.g. 2017-02-10T20:40:00
                      type: string
                      format: date-time
                      example: '2017-10-23T20:00:00'
            AircraftEquipment:
              description: information related to the aircraft
              properties:
                code:
                  type: string
                  description: >
                    IATA aircraft code
                    (http://www.flugzeuginfo.net/table_accodes_iata_en.php)
                  pattern: '[a-zA-Z0-9]{3}'
                  example: '318'
            OperatingFlight:
              type: object
              description: information about the operating flight
              properties:
                carrierCode:
                  type: string
                  description: providing the airline / carrier code
                  minLength: 1
                  maxLength: 2
                  example: DL
            Price:
              properties:
                currency:
                  type: string
                  example: USD
                total:
                  description: Total amount paid by the user
                  type: string
                  example: '932.70'
                base:
                  description: Amount without taxes
                  type: string
                  example: '632.70'
                fees:
                  description: List of applicable fees
                  type: array
                  items:
                    $ref: '#/definitions/Fee'
                taxes:
                  type: array
                  items:
                    $ref: '#/definitions/Tax'
                refundableTaxes:
                  description: The amount of taxes which are refundable
                  type: string
                  example: '200.00'
            Extended_Price:
              type: object
              title: Price
              description: price information
              allOf:
                - type: object
                  properties:
                    margin:
                      description: >-
                        BOOK step ONLY - The price margin percentage (plus or
                        minus) that the booking can tolerate. When set to 0,
                        then no price magin is tolerated.
                      type: string
                      example: '1.00'
                    grandTotal:
                      description: >-
                        Total amount paid by the user (including fees and
                        selected additional services).
                      type: string
                      example: '987.00'
                    billingCurrency:
                      description: >-
                        Currency of the payment. It may be different than the
                        requested currency
                      type: string
                      example: EUR
                    additionalServices:
                      type: array
                      title: AdditionalServices
                      items:
                        title: AdditionalService
                        type: object
                        properties:
                          amount:
                            type: string
                            example: '332.70'
                          type:
                            $ref: '#/definitions/AdditionalServiceType'
                - $ref: '#/definitions/Price'
            Fee:
              description: a fee
              properties:
                amount:
                  type: string
                  example: '332.70'
                type:
                  $ref: '#/definitions/FeeType'
            FeeType:
              type: string
              description: type of fee
              enum:
                - TICKETING
                - FORM_OF_PAYMENT
                - SUPPLIER
              example: TICKETING
            Tax:
              description: a tax
              type: object
              properties:
                amount:
                  type: string
                  example: '332.70'
                code:
                  type: string
                  example: MX
            TravelClass:
              description: >-
                quality of service offered in the cabin where the seat is
                located in this flight. Economy, premium economy, business or
                first class
              type: string
              enum:
                - ECONOMY
                - PREMIUM_ECONOMY
                - BUSINESS
                - FIRST
              example: PREMIUM_ECONOMY
            Co2Emission:
              type: object
              properties:
                weight:
                  description: Weight of Co2 emitted for the concerned segment
                  type: integer
                  example: 90
                weightUnit:
                  description: Code to qualify unit as pounds or kilos
                  type: string
                  example: KG
                cabin:
                  $ref: '#/definitions/TravelClass'
            FlightOffer:
              title: Flight-offer
              type: object
              required:
                - type
                - id
              properties:
                type:
                  type: string
                  description: the resource name
                  example: flight-offer
                id:
                  description: Id of the flight offer
                  type: string
                  example: '1'
                source:
                  $ref: '#/definitions/FlightOfferSource'
                instantTicketingRequired:
                  description: >-
                    If true, inform that a ticketing will be required at booking
                    step.
                  type: boolean
                  example: false
                disablePricing:
                  description: >-
                    BOOK step ONLY - If true, allows to book a PNR without
                    pricing. Only for the source "GDS"
                  type: boolean
                  example: false
                nonHomogeneous:
                  description: >-
                    If true, upon completion of the booking, this pricing
                    solution is expected to yield multiple records (a record
                    contains booking information confirmed and stored, typically
                    a Passenger Name Record (PNR), in the provider GDS or
                    system)
                  type: boolean
                  example: false
                oneWay:
                  description: >-
                    If true, the flight offer can be combined with other oneWays
                    flight-offers to complete the whole journey (one-Way
                    combinable feature).
                  type: boolean
                  example: false
                paymentCardRequired:
                  description: >-
                    If true, a payment card is mandatory to book this flight
                    offer
                  type: boolean
                  example: false
                lastTicketingDate:
                  description: >-
                    If booked on the same day as the search (with respect to
                    timezone), this flight offer is guaranteed to be thereafter
                    valid for ticketing until this date (included). Unspecified
                    when it does not make sense for this flight offer (e.g. no
                    control over ticketing once booked). YYYY-MM-DD format, e.g.
                    2019-06-07
                  type: string
                  example: '2018-06-19'
                lastTicketingDateTime:
                  description: >-
                    If booked on the same day as the search (with respect to
                    timezone), this flight offer is guaranteed to be thereafter
                    valid for ticketing until this date/time (included).
                    Unspecified when it does not make sense for this flight
                    offer (e.g. no control over ticketing once booked).
                    Information only this attribute is not used in input of
                    pricing request. Local date and time in YYYY-MM-ddThh:mm:ss
                    format, e.g. 2017-02-10T20:40:00
                  type: string
                  format: date-time
                  example: '2018-06-19T15:00:00'
                numberOfBookableSeats:
                  description: >-
                    Number of seats bookable in a single request. Can not be
                    higher than 9.
                  type: number
                  example: 9
                  minimum: 1
                  maximum: 9
                itineraries:
                  type: array
                  minItems: 1
                  maxItems: 250
                  items:
                    title: Itineraries
                    type: object
                    properties:
                      duration:
                        description: >-
                          duration in
                          [ISO8601](https://en.wikipedia.org/wiki/ISO_8601)
                          PnYnMnDTnHnMnS format, e.g. PT2H10M for a duration of
                          2h10m
                        type: string
                        example: PT2H10M
                      segments:
                        title: Segments
                        type: array
                        minItems: 1
                        maxItems: 9
                        items:
                          $ref: '#/definitions/Segment'
                    required:
                      - segments
                price:
                  $ref: '#/definitions/Extended_Price'
                pricingOptions:
                  title: PricingOptions
                  type: object
                  properties:
                    fareType:
                      description: type of fare of the flight-offer
                      $ref: '#/definitions/PricingOptionsFareType'
                    includedCheckedBagsOnly:
                      type: boolean
                      description: >-
                        If true, returns the flight-offers with included checked
                        bags only
                      example: true
                    refundableFare:
                      type: boolean
                      description: >-
                        If true, returns the flight-offers with refundable fares
                        only
                      example: true
                    noRestrictionFare:
                      type: boolean
                      description: >-
                        If true, returns the flight-offers with no restriction
                        fares only
                      example: true
                    noPenaltyFare:
                      type: boolean
                      description: >-
                        If true, returns the flight-offers with no penalty fares
                        only
                      example: true
                validatingAirlineCodes:
                  description: >-
                    This option ensures that the system will only consider
                    offers with these airlines as validating carrier.
                  type: array
                  minItems: 1
                  maxItems: 9
                  items:
                    type: string
                  example:
                    - AF
                travelerPricings:
                  title: TravelerPricings
                  description: Fare information for each traveler/segment
                  type: array
                  minItems: 1
                  maxItems: 18
                  items:
                    title: TravelerPricing
                    required:
                      - travelerId
                      - fareOption
                      - travelerType
                      - fareDetailsBySegment
                    properties:
                      travelerId:
                        type: string
                        example: '1'
                        description: Id of the traveler
                      fareOption:
                        $ref: '#/definitions/TravelerPricingFareOption'
                      travelerType:
                        $ref: '#/definitions/TravelerType'
                      associatedAdultId:
                        type: string
                        description: >-
                          if type="HELD_INFANT", corresponds to the adult
                          traveler's id who will share the seat
                      price:
                        description: price detail of the traveler
                        $ref: '#/definitions/Price'
                      fareDetailsBySegment:
                        type: array
                        minItems: 1
                        maxItems: 18
                        items:
                          title: FareDetailsBySegment
                          description: Fare details of the segment
                          required:
                            - segmentId
                          properties:
                            segmentId:
                              type: string
                              example: '1'
                              description: Id of the segment
                            cabin:
                              $ref: '#/definitions/TravelClass'
                            fareBasis:
                              description: >-
                                Fare basis specifying the rules of a fare.
                                Usually, though not always, is composed of the
                                booking class code followed by a set of letters
                                and digits representing other characteristics of
                                the ticket, such as refundability, minimum stay
                                requirements, discounts or special promotional
                                elements.
                              type: string
                              example: ANNNNF4K
                              pattern: '[[A-Z0-9]{1,18}'
                            brandedFare:
                              description: >-
                                The name of the Fare Family corresponding to the
                                fares. Only for the GDS provider and if the
                                airline has fare families filled
                              type: string
                              example: LIGHTONE
                            class:
                              description: >-
                                The code of the booking class, a.k.a. class of
                                service or Reservations/Booking Designator (RBD)
                              type: string
                              example: A
                              pattern: '[A-Z]{1}'
                            isAllotment:
                              description: >-
                                True if the corresponding booking class is in an
                                allotment
                              type: boolean
                              example: true
                            allotmentDetails:
                              $ref: '#/definitions/AllotmentDetails'
                            sliceDiceIndicator:
                              $ref: '#/definitions/SliceDiceIndicator'
                            includedCheckedBags:
                              title: includedCheckedBags
                              $ref: '#/definitions/BaggageAllowance'
                              description: Details of the included checked bags
                            additionalServices:
                              type: object
                              title: AdditionalServicesRequest
                              properties:
                                chargeableCheckedBags:
                                  title: chargeableCheckedBags
                                  description: Details of chargeable checked bags
                                  $ref: '#/definitions/ChargeableCheckdBags'
                                chargeableSeat:
                                  title: chargeableSeat
                                  description: Details of chargeable seat
                                  $ref: '#/definitions/ChargeableSeat'
                                chargeableSeatNumber:
                                  type: string
                                  description: >-
                                    DEPRECATED - use the chargeableSeat
                                    attribute -  seat number
                                  example: 33D
                                  pattern: '[1-9][0-9]{0,2}[A-Z]?'
                                otherServices:
                                  type: array
                                  description: Other services to add
                                  items:
                                    $ref: '#/definitions/ServiceName'
                                  example:
                                    - PRIORITY_BOARDING
            Segment:
              allOf:
                - type: object
                  properties:
                    id:
                      description: Id of the segment
                      type: string
                      example: 1
                    numberOfStops:
                      description: Number of stops
                      type: integer
                      example: 0
                    blacklistedInEU:
                      description: >
                        When the flight has a marketing or/and operating airline
                        that is identified as blacklisted by the European
                        Commission. 


                        To improve travel safety, the European Commission
                        regularly updates the list of the banned carriers from
                        operating in Europe. It allows any Travel Agency located
                        in the European Union to easily identify and hide any
                        travel recommendation based on some unsafe airlines. 

                        The [list of the banned
                        airlines](https://ec.europa.eu/transport/sites/transport/files/air-safety-list_en.pdf)
                        is published in the Official Journal of the European
                        Union, where they are included as annexes A and B to the
                        Commission Regulation. The blacklist of an airline can
                        concern all its flights or some specific aircraft types
                        pertaining to the airline   
                      type: boolean
                      example: false
                    co2Emissions:
                      description: Co2 informations
                      type: array
                      minItems: 1
                      items:
                        title: Co2Emission
                        $ref: '#/definitions/Co2Emission'
                - $ref: '#/definitions/FlightSegment'
            TravelerType:
              type: string
              description: >
                traveler type

                age restrictions : CHILD < 12y, HELD_INFANT < 2y, SEATED_INFANT
                < 2y, SENIOR >=60y
              enum:
                - ADULT
                - CHILD
                - SENIOR
                - YOUNG
                - HELD_INFANT
                - SEATED_INFANT
                - STUDENT
              example: ADULT
            AdditionalServiceType:
              type: string
              description: additional service type
              enum:
                - CHECKED_BAGS
                - MEALS
                - SEATS
                - OTHER_SERVICES
              example: CHECKED_BAGS
            FlightOfferSource:
              description: source of the flight offer
              type: string
              enum:
                - GDS
              example: GDS
            PricingOptionsFareType:
              type: array
              description: type of fare of the flight-offer
              items:
                type: string
                enum:
                  - PUBLISHED
              example:
                - PUBLISHED
            TravelerPricingFareOption:
              description: >
                option specifying a group of fares, which may be valid under
                certain conditons

                Can be used to specify special fare discount for a passenger
              type: string
              enum:
                - STANDARD
                - INCLUSIVE_TOUR
                - SPANISH_MELILLA_RESIDENT
                - SPANISH_CEUTA_RESIDENT
                - SPANISH_CANARY_RESIDENT
                - SPANISH_BALEARIC_RESIDENT
                - AIR_FRANCE_METROPOLITAN_DISCOUNT_PASS
                - AIR_FRANCE_DOM_DISCOUNT_PASS
                - AIR_FRANCE_COMBINED_DISCOUNT_PASS
                - AIR_FRANCE_FAMILY
                - ADULT_WITH_COMPANION
                - COMPANION
              example: STANDARD
            SliceDiceIndicator:
              description: >-
                slice and Dice indicator, such as Local Availability, Sub
                OnD(Origin and Destination) 1 Availability and Sub OnD 2
                Availability
              type: string
              enum:
                - LOCAL_AVAILABILITY
                - SUB_OD_AVAILABILITY_1
                - SUB_OD_AVAILABILITY_2
            AllotmentDetails:
              title: AllotmentDetails
              type: object
              properties:
                tourName:
                  description: The tour name agreed for this specific allotment.
                  type: string
                tourReference:
                  description: The tour reference agreed for this specific allotment.
                  type: string
            ChargeableCheckdBags:
              description: Details of chargeable checked bags
              allOf:
                - $ref: '#/definitions/BaggageAllowance'
                - type: object
                  properties:
                    id:
                      description: Id of the chargeable bag
                      type: string
                      example: '1'
            ChargeableSeat:
              description: Details of chargeable seat
              type: object
              properties:
                id:
                  description: Id of the chargeable seat
                  type: string
                  example: '1'
                number:
                  type: string
                  description: seat number
                  example: 33D
                  pattern: '[1-9][0-9]{0,2}[A-Z]?'
            Dictionaries:
              type: object
              properties:
                locations:
                  $ref: '#/definitions/LocationEntry'
                aircraft:
                  $ref: '#/definitions/AircraftEntry'
                currencies:
                  $ref: '#/definitions/CurrencyEntry'
                carriers:
                  $ref: '#/definitions/CarrierEntry'
            LocationValue:
              properties:
                cityCode:
                  type: string
                  description: City code associated to the airport
                  example: PAR
                countryCode:
                  type: string
                  description: Country code of the airport
                  example: FR
            ElementaryPrice:
              description: elementaryPrice
              type: object
              properties:
                amount:
                  type: string
                  description: >-
                    Amount of the fare. could be alpha numeric. Ex- 500.20 or
                    514.13A, 'A'signifies additional collection.
                currencyCode:
                  type: string
                  description: Currency type of the fare.
            BaggageAllowance:
              description: baggageAllowance
              type: object
              properties:
                quantity:
                  type: integer
                  description: Total number of units
                  example: 1
                weight:
                  type: integer
                  description: Weight of the baggage allowance
                  example: 20
                weightUnit:
                  type: string
                  description: Code to qualify unit as pounds or kilos
                  example: KG
            ServiceName:
              description: type of service
              type: string
              enum:
                - PRIORITY_BOARDING
                - AIRPORT_CHECKIN
              example: PRIORITY_BOARDING
            FlightOrder:
              title: FlightOrderCreateQuery
              type: object
              description: input parameter to create a flight order
              required:
                - type
                - flightOffers
              properties:
                type:
                  description: the resource name
                  type: string
                  example: flight-order
                id:
                  description: unique identifier of the flight order
                  type: string
                  example: MlpZVkFMfFdBVFNPTnwyMDE1LTExLTAy
                  readOnly: true
                queuingOfficeId:
                  description: office Id where to queue the order
                  type: string
                  example: NCE1A0955
                ownerOfficeId:
                  description: >-
                    office Id where will be transfered the ownership of the
                    order
                  type: string
                  example: NCE1A0955
                associatedRecords:
                  description: list of associated record
                  type: array
                  readOnly: true
                  items:
                    $ref: '#/definitions/AssociatedRecord'
                flightOffers:
                  description: list of flight offer
                  type: array
                  minItems: 1
                  maxItems: 6
                  items:
                    $ref: '#/definitions/FlightOffer'
                travelers:
                  description: list of travelers
                  type: array
                  minItems: 1
                  maxItems: 18
                  items:
                    $ref: '#/definitions/Traveler'
                remarks:
                  description: list of global remarks
                  $ref: '#/definitions/Remarks'
                formOfPayments:
                  description: list of form of payments
                  type: array
                  minItems: 1
                  maxItems: 6
                  items:
                    $ref: '#/definitions/FormOfPayment'
                ticketingAgreement:
                  $ref: '#/definitions/TicketingAgreement'
                automatedProcess:
                  description: list of automatic queuing
                  type: array
                  minItems: 0
                  maxItems: 31
                  items:
                    $ref: '#/definitions/AutomatedProcess'
                contacts:
                  description: list of general contact information
                  type: array
                  items:
                    $ref: '#/definitions/Contact'
                tickets:
                  description: list of tickets
                  readOnly: true
                  type: array
                  items:
                    $ref: '#/definitions/AirTravelDocument'
                formOfIdentifications:
                  description: >-
                    list of forms of identifications applicable to travelers by
                    airline
                  type: array
                  items:
                    $ref: '#/definitions/FormOfIdentification'
            Stakeholder:
              type: object
              description: stakeholder definition
              properties:
                id:
                  description: item identifier
                  type: string
                dateOfBirth:
                  type: string
                  format: date
                  description: The date of birth in ISO 8601 format (yyyy-mm-dd)
                gender:
                  $ref: '#/definitions/StakeholderGender'
                name:
                  $ref: '#/definitions/Name'
                documents:
                  type: array
                  description: >-
                    Advanced Passenger Information - regulatory identity
                    documents - SSR DOCS & DOCO elements
                  items:
                    $ref: '#/definitions/IdentityDocument'
            StakeholderGender:
              type: string
              description: Gender for individual
              enum:
                - MALE
                - FEMALE
                - UNSPECIFIED
                - UNDISCLOSED
              title: Gender
              example: FEMALE
            IdentityDocument:
              title: traveler documents
              description: documents of the traveler
              allOf:
                - $ref: '#/definitions/Document'
                - type: object
                  properties:
                    documentType:
                      $ref: '#/definitions/DocumentType'
                    validityCountry:
                      type: string
                      description: >-
                        [ISO 3166-1
                        alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)
                        of the country where the document is valid
                      example: IN
                      pattern: '[a-zA-Z]{2}'
                    birthCountry:
                      type: string
                      description: >-
                        [ISO 3166-1
                        alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)
                        of the country of birth
                      example: FR
                      pattern: '[a-zA-Z]{2}'
                    holder:
                      type: boolean
                      description: >-
                        boolean to specify if the traveler is the holder of the
                        document
                      example: true
            Document:
              type: object
              description: the information that are found on an ID document
              properties:
                number:
                  type: string
                  description: >-
                    The document number (shown on the document) . E.g.
                    QFU514563221J
                issuanceDate:
                  type: string
                  description: Date at which the document has been issued.
                  format: date
                expiryDate:
                  type: string
                  description: Date after which the document is not valid anymore.
                  format: date
                issuanceCountry:
                  type: string
                  description: >-
                    [ISO 3166-1
                    alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)
                    of the country that issued the document
                  pattern: '[a-zA-Z]{2}'
                issuanceLocation:
                  type: string
                  description: >-
                    A more precise information concerning the place where the
                    document has been issued, when available. It may be a
                    country, a state, a city or any other type of location. e.g.
                    New-York
                nationality:
                  type: string
                  description: >-
                    [ISO 3166-1
                    alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)
                    of the nationality appearing on the document
                  pattern: '[a-zA-Z]{2}'
                birthPlace:
                  type: string
                  description: Birth place as indicated on the document
            DocumentType:
              type: string
              description: the nature/type of the document
              enum:
                - VISA
                - PASSPORT
                - IDENTITY_CARD
                - KNOWN_TRAVELER
                - REDRESS
              example: VISA
            EmergencyContact:
              type: object
              description: emergency contact number
              properties:
                addresseeName:
                  type: string
                  description: >-
                    Adressee name (e.g. in case of emergency purpose it
                    corresponds to name of the person to be contacted).
                  pattern: '[a-zA-Z -]'
                countryCode:
                  type: string
                  description: >-
                    Country code of the country (ISO3166-1). E.g. "US" for the
                    United States
                  pattern: '[A-Z]{2}'
                number:
                  type: string
                  description: >-
                    Phone number. Composed of digits only. The number of digits
                    depends on the country.
                  pattern: '[0-9]{1,15}'
                text:
                  type: string
                  description: additional details
            LoyaltyProgram:
              title: LoyaltyProgram
              description: loyalty program information
              type: object
              properties:
                programOwner:
                  type: string
                  description: loyalty program airline code
                  example: AF
                id:
                  type: string
                  description: loyalty program number
                  example: '12357466574'
            FormOfIdentification:
              type: object
              description: alternative means of identifying stakeholders for eTicket.
              properties:
                identificationType:
                  type: string
                  description: Type of identification
                  enum:
                    - DRIVERS_LICENSE
                    - PASSPORT
                    - NATIONAL_IDENTITY_CARD
                    - BOOKING_CONFIRMATION
                    - TICKET
                    - OTHER_ID
                  example: PASSPORT
                carrierCode:
                  type: string
                  description: providing the airline / carrier code
                  minLength: 1
                  maxLength: 2
                  example: DL
                number:
                  type: string
                  description: >-
                    identification number relative to the type of identification
                    either ticket number, booking number, passport number,
                    identity card number, drivers licence number, other ID
                  example: XN0019390
                travelerIds:
                  description: Ids of the concerned travelers
                  type: array
                  items:
                    type: string
                  example: '1'
                flightOfferIds:
                  description: Id of the concerned flightOffers
                  type: array
                  minItems: 1
                  maxItems: 6
                  items:
                    type: string
                  example: '1'
              title: FormOfIdentification
            Discount:
              title: Discount
              description: traveler discount
              type: object
              properties:
                subType:
                  $ref: '#/definitions/DiscountType'
                cityName:
                  type: string
                  description: city of residence
                  example: MADRID
                travelerType:
                  $ref: '#/definitions/DiscountTravelerType'
                cardNumber:
                  type: string
                  description: resident card number
                  example: 12568215Z
                  pattern: '[0-9A-Z][0-9]{0,12}[A-Z]'
                certificateNumber:
                  type: string
                  description: resident certificate number
                  example: 12568215Z
                  pattern: '[0-9A-Z][0-9]{0,12}[A-Z]'
            DiscountType:
              description: type of discount applied
              type: string
              enum:
                - SPANISH_RESIDENT
                - AIR_FRANCE_DOMESTIC
                - AIR_FRANCE_COMBINED
                - AIR_FRANCE_METROPOLITAN
              example: SPANISH_RESIDENT
            DiscountTravelerType:
              description: type of discount applied
              type: string
              enum:
                - SPANISH_CITIZEN
                - EUROPEAN_CITIZEN
                - GOVERNMENT_WORKER
                - MILITARY
                - MINOR_WITHOUT_ID
              example: SPANISH_CITIZEN
            Traveler:
              title: traveler element
              description: the traveler of the trip
              allOf:
                - $ref: '#/definitions/Stakeholder'
                - type: object
                  properties:
                    emergencyContact:
                      description: emergency contact
                      $ref: '#/definitions/EmergencyContact'
                    loyaltyPrograms:
                      description: list of loyalty program followed by the traveler
                      type: array
                      minItems: 0
                      maxItems: 10
                      items:
                        $ref: '#/definitions/LoyaltyProgram'
                    discountEligibility:
                      description: list of element that allow a discount.
                      type: array
                      minItems: 0
                      maxItems: 10
                      items:
                        $ref: '#/definitions/Discount'
                    contact:
                      $ref: '#/definitions/Contact'
            Contact:
              description: contact information
              allOf:
                - $ref: '#/definitions/ContactDictionary'
                - type: object
                  properties:
                    phones:
                      description: Phone numbers
                      type: array
                      maxItems: 3
                      items:
                        $ref: '#/definitions/Phone'
                    companyName:
                      description: Name of the company
                      type: string
                      example: AMADEUS
                    emailAddress:
                      type: string
                      description: Email address (e.g. john@smith.com)
                      example: support@mail.com
            ContactPurpose:
              description: the purpose for which this contact is to be used
              type: string
              enum:
                - STANDARD
                - INVOICE
                - STANDARD_WITHOUT_TRANSMISSION
            ContactDictionary:
              description: represents a contact
              type: object
              properties:
                addresseeName:
                  description: the name of the person addressed by these contact details
                  $ref: '#/definitions/Name'
                address:
                  $ref: '#/definitions/Address'
                language:
                  description: the preferred language of communication with this Contact
                  type: string
                purpose:
                  $ref: '#/definitions/ContactPurpose'
            Name:
              title: name
              description: name
              allOf:
                - $ref: '#/definitions/BaseName'
                - type: object
                  properties:
                    secondLastName:
                      description: second last name
                      type: string
            BaseName:
              type: object
              description: description of the name of a physical person
              properties:
                firstName:
                  description: First name.
                  type: string
                lastName:
                  description: Last name.
                  type: string
                middleName:
                  description: Middle name(s), for example "Lee" in "John Lee Smith".
                  type: string
            Phone:
              type: object
              description: phone information
              properties:
                deviceType:
                  $ref: '#/definitions/PhoneDeviceType'
                countryCallingCode:
                  type: string
                  description: >-
                    Country calling code of the phone number, as defined by the
                    International Communication Union. Examples - "1" for US,
                    "371" for Latvia.
                  pattern: '[0-9+]{2,5}'
                number:
                  type: string
                  description: >-
                    Phone number. Composed of digits only. The number of digits
                    depends on the country.
                  pattern: '[0-9]{1,15}'
            PhoneDeviceType:
              type: string
              description: Type of the device (Landline, Mobile or Fax)
              enum:
                - MOBILE
                - LANDLINE
                - FAX
            Address:
              type: object
              description: address information
              properties:
                lines:
                  type: array
                  description: >-
                    Line 1 = Street address, Line 2 = Apartment, suite, unit,
                    building, floor, etc
                  items:
                    type: string
                postalCode:
                  type: string
                  description: 'Example: 74130'
                countryCode:
                  type: string
                  description: >-
                    country code [ISO 3166-1 country
                    code](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)
                  pattern: '[a-zA-Z]{2}'
                cityName:
                  type: string
                  description: 'Full city name. Example: Dublin'
                  pattern: '[a-zA-Z -]{1,35}'
                stateName:
                  type: string
                  description: Full state name
                postalBox:
                  type: string
                  description: E.g. BP 220
            TicketingAgreement:
              title: Ticketing Agreement
              description: ticketing agreement
              type: object
              properties:
                option:
                  $ref: '#/definitions/TicketingAgreementOption'
                delay:
                  description: >-
                    Delay before applying automatic process if no issuance in
                    days
                  type: string
                dateTime:
                  description: >-
                    Exact date to apply automatic process if no issuance.
                    YYYY-MM-DD format, e.g. 2019-06-07
                  type: string
                  readOnly: true
                  example: '2017-10-23'
                segmentIds:
                  description: Ids of the impacted segments
                  type: array
                  readOnly: true
                  items:
                    type: string
                  example: '1'
            TicketingAgreementOption:
              description: >
                Ticketing agreement option

                * **CONFIRM**, when the payment is done

                * **DELAY_TO_QUEUE**, queue the reservation at a wished date if
                the payment is not done

                * **DELAY_TO_CANCEL**, cancel the reservation at a wished date
                if the payment is not done


                Queueing and cancellation occurs at local date and time. When no
                time is specified, reservation is queued or cancelled at 00:00.
              type: string
              enum:
                - CONFIRM
                - DELAY_TO_QUEUE
                - DELAY_TO_CANCEL
              example: DELAY_TO_QUEUE
            AutomatedProcessCommon:
              type: object
              description: >-
                Provides information on ticketing arrangements and Amadeus Time
                Limits
              properties:
                code:
                  $ref: '#/definitions/AutomatedProcessCode'
                queue:
                  title: Queue
                  type: object
                  description: >-
                    Identifies the queue onto which PNR must be automatically
                    placed upon process execution.
                  properties:
                    number:
                      type: string
                    category:
                      type: string
                text:
                  type: string
                  description: Free text
            AutomatedProcess:
              title: Automated Process
              description: automatic process applied to the Order
              allOf:
                - $ref: '#/definitions/AutomatedProcessCommon'
                - type: object
                  properties:
                    delay:
                      description: Delay before applying process in days
                      type: string
                    officeId:
                      description: Office into which the process must be triggered.
                      type: string
                      example: NCE1A0955
                    dateTime:
                      type: string
                      format: date-time
                      description: >-
                        Datetime limit at which the process takes action in case
                        issuance is not done.
            AutomatedProcessCode:
              type: string
              description: queuing action to be taken
              enum:
                - IMMEDIATE
                - DELAYED
                - ERROR
              example: IMMEDIATE
            Remarks:
              title: Remarks
              description: remarks
              type: object
              properties:
                general:
                  description: list of general remarks
                  type: array
                  minItems: 0
                  maxItems: 200
                  items:
                    $ref: '#/definitions/GeneralRemark'
                airline:
                  description: list of airline remarks
                  type: array
                  minItems: 0
                  maxItems: 200
                  items:
                    $ref: '#/definitions/AirlineRemark'
            GeneralRemark:
              title: GeneralRemark
              type: object
              required:
                - subType
                - text
              properties:
                subType:
                  $ref: '#/definitions/GeneralRemarkType'
                category:
                  description: remark category
                  type: string
                  example: Z
                  pattern: '[A-Z]{1}'
                text:
                  description: remark free text
                  type: string
                  example: PASSENGER NEED ASSISTANCE
                travelerIds:
                  description: Id of the concerned traveler
                  type: array
                  items:
                    type: string
                  example: '1'
                flightOfferIds:
                  description: Id of the concern flightOffers
                  type: array
                  minItems: 1
                  maxItems: 6
                  items:
                    type: string
                  example: '1'
            GeneralRemarkType:
              description: general remark type
              type: string
              enum:
                - GENERAL_MISCELLANEOUS
                - CONFIDENTIAL
                - INVOICE
                - QUALITY_CONTROL
                - BACKOFFICE
                - FULFILLMENT
                - ITINERARY
                - TICKETING_MISCELLANEOUS
                - TOUR_CODE
              example: GENERAL_MISCELLANEOUS
            AirlineRemark:
              title: AirlineRemark
              type: object
              required:
                - subType
                - airlineCode
                - text
              properties:
                subType:
                  $ref: '#/definitions/AirlineRemarkType'
                keyword:
                  description: keyword code - only applicable for subType Keyword
                  type: string
                  example: PARK
                airlineCode:
                  description: >
                    Code of the airline following IATA standard ([IATA table
                    codes](http://www.iata.org/publications/Pages/code-search.aspx))


                    When it apply to any airline, value is YY.
                  type: string
                  example: AF
                text:
                  description: remark free text
                  type: string
                  example: CAR PARK
                travelerIds:
                  description: Id of the concerned traveler
                  type: array
                  items:
                    type: string
                  example: '1'
                flightOfferIds:
                  description: Id of the concern flightOffers
                  type: array
                  minItems: 1
                  maxItems: 6
                  items:
                    type: string
                  example: '1'
            AirlineRemarkType:
              description: airline remark type
              type: string
              enum:
                - OTHER_SERVICE_INFORMATION
                - KEYWORD
                - OTHER_SERVICE
                - CLIENT_ID
                - ADVANCED_TICKET_TIME_LIMIT
              example: KEYWORD
            FormOfPayment:
              title: Form Of Payment
              description: form of payment used
              type: object
              properties:
                b2bWallet:
                  description: payment with the solution B2B Wallet
                  $ref: '#/definitions/B2bWallet'
                creditCard:
                  description: payment with a credit card
                  $ref: '#/definitions/CreditCard'
                other:
                  description: payment with an other method
                  $ref: '#/definitions/OtherMethod'
            B2bWallet:
              title: B2bWallet
              type: object
              description: b2b wallet
              properties:
                cardId:
                  readOnly: true
                  description: card identifier
                  type: string
                  example: '1245365895336'
                cardUsageName:
                  description: card usage name
                  type: string
                cardFriendlyName:
                  description: card name
                  type: string
                  example: CB1
                  pattern: '[a-zA-Z0-9]{1,35}'
                reportingData:
                  type: array
                  title: reportingData
                  items:
                    title: reportingData
                    type: object
                    properties:
                      name:
                        type: string
                        example: reconcil1
                      value:
                        type: string
                        example: data1
                virtualCreditCardDetails:
                  readOnly: true
                  $ref: '#/definitions/VirtualCreditCardDetails'
                flightOfferIds:
                  description: Id of the concern flightOffers
                  type: array
                  minItems: 1
                  maxItems: 6
                  items:
                    type: string
                  example: '1'
            VirtualCreditCardDetails:
              description: detail information of the virtual card
              allOf:
                - $ref: '#/definitions/CreditCardCommon'
                - $ref: '#/definitions/ElementaryPrice'
            CreditCard:
              title: creditCard
              type: object
              description: credit card
              allOf:
                - $ref: '#/definitions/CreditCardCommon'
                - type: object
                  properties:
                    securityCode:
                      description: card security code
                      type: string
                      example: '123'
                    flightOfferIds:
                      description: Id of the concern flightOffers
                      type: array
                      minItems: 1
                      maxItems: 6
                      items:
                        type: string
                      example: '1'
            CreditCardCommon:
              title: creditCardCommon
              type: object
              description: credit card common attribute
              properties:
                brand:
                  $ref: '#/definitions/CreditCardBrand'
                holder:
                  description: card holder as on the card
                  type: string
                  example: MR DUPON DAMIEN
                number:
                  description: card number
                  type: string
                  example: '4012999999999999'
                  pattern: '[a-zA-Z0-9]{1,35}'
                expiryDate:
                  description: >-
                    credit card expiration date following [ISO
                    8601](https://en.wikipedia.org/wiki/ISO_8601) (YYYY-MM
                    format, e.g. 2012-08)
                  type: string
                  example: 2021-08
            CreditCardBrand:
              description: credit card brand
              type: string
              enum:
                - VISA
                - AMERICAN_EXPRESS
                - MASTERCARD
                - VISA_ELECTRON
                - VISA_DEBIT
                - MASTERCARD_DEBIT
                - MAESTRO
                - DINERS
                - EASYPAY
              example: VISA
            OtherMethod:
              title: creditCard
              type: object
              description: other payment method
              properties:
                method:
                  $ref: '#/definitions/OtherPaymentMethod'
                flightOfferIds:
                  description: Id of the concern flightOffers
                  type: array
                  minItems: 1
                  maxItems: 6
                  items:
                    type: string
                  example: '1'
            OtherPaymentMethod:
              description: other payment method
              type: string
              enum:
                - ACCOUNT
                - CHECK
                - CASH
                - NONREFUNDABLE
              example: CASH
            AssociatedRecordCommon:
              type: object
              description: >-
                describes the relation between the current reservation and
                another one
              properties:
                reference:
                  type: string
                  description: >-
                    Record locator [Amadeus or OA] with which the current
                    reservation is related. In case of a codeshare relation, it
                    enables to identify the operating PNR.
                creationDate:
                  type: string
                  description: >-
                    Creation date of the referenced reservation. Date and time
                    in [ISO8601](https://en.wikipedia.org/wiki/ISO_8601)
                    YYYY-MM-ddThh:mm:ss.sss format, e.g. 2019-07-09T12:30:00.000
                  example: '2019-07-09T12:30:00.000'
                originSystemCode:
                  type: string
                  description: >-
                    Designates the system which has originated the referenced
                    reservation.
                  minLength: 2
                  maxLength: 3
            AssociatedRecord:
              title: associated record
              description: record associated to the order
              allOf:
                - $ref: '#/definitions/AssociatedRecordCommon'
                - type: object
                  properties:
                    flightOfferId:
                      type: string
                      description: id of the impacted flight offer
                      example: '1'
            AirTravelDocument:
              title: AirTravelDocument
              description: ticket information
              allOf:
                - $ref: '#/definitions/AirTravelDocumentCommon'
                - type: object
                  properties:
                    travelerId:
                      type: string
                      description: id of the impacted traveler
                      example: '1'
                    segmentIds:
                      description: Ids of the impacted segments
                      type: array
                      items:
                        type: string
                      example: '1'
            AirTravelDocumentCommon:
              type: object
              properties:
                documentType:
                  type: string
                  description: Type of the travel document
                  enum:
                    - ETICKET
                    - PTICKET
                    - EMD
                    - MCO
                documentNumber:
                  type: string
                  description: >-
                    Identifier of the travel document prefixed by its owner code
                    [NALC - 3 digits]. Can either be a primary or a conjunctive
                    document number. Necessary for TicketingReference
                    definition.
                documentStatus:
                  type: string
                  description: Status of the travel document contained in the fare element
                  enum:
                    - ISSUED
                    - REFUNDED
                    - VOID
                    - ORIGINAL
                    - EXCHANGED
          responses:
            '204':
              description: Successfully Deleted
            '404':
              description: Not Found
              schema:
                $ref: '#/definitions/Error_404'
            '500':
              description: Unexpected error
              schema:
                $ref: '#/definitions/Error_500'
            returnFlightOrders:
              description: Successful Operation
              schema:
                title: Success_Booking
                type: object
                required:
                  - data
                properties:
                  meta:
                    $ref: '#/definitions/Collection_Meta_Link'
                  warnings:
                    type: array
                    items:
                      $ref: '#/definitions/Issue'
                  data:
                    $ref: '#/definitions/FlightOrder'
                  dictionaries:
                    $ref: '#/definitions/Dictionaries'
                example:
                  data:
                    type: flight-order
                    id: MlpZVkFMfFdBVFNPTnwyMDE1LTExLTAy
                    queuingOfficeId: NCE1A0950
                    associatedRecords:
                      - reference: 2ZYVAL
                        creationDateTime: '2018-07-13T20:17:00'
                        originSystemCode: 1A
                        flightOfferId: '1'
                    travelers:
                      - id: '1'
                        dateOfBirth: '1982-01-16'
                        name:
                          firstName: STEPHANE
                          lastName: MARTIN
                        contact:
                          phones:
                            - countryCallingCode: '33'
                              number: '487692704'
                        documents:
                          - documentType: PASSPORT
                            number: '012345678'
                            expiryDate: '2009-04-14'
                            issuanceCountry: GB
                            nationality: GB
                            holder: true
                      - id: '3'
                        dateOfBirth: '2018-03-24'
                        name:
                          firstName: JULES
                          lastName: MARTIN
                      - id: '2'
                        dateOfBirth: '2007-10-11'
                        name:
                          firstName: EMILIE
                          lastName: MARTIN
                    flightOffers:
                      - id: '1'
                        type: flight-offer
                        source: GDS
                        itineraries:
                          - duration: PT2H
                            segments:
                              - id: '1'
                                duration: PT2H
                                aircraft:
                                  code: '320'
                                numberOfStops: 0
                                blacklistedInEU: false
                                carrierCode: IB
                                operating:
                                  carrierCode: IB
                                number: '3403'
                                departure:
                                  at: '2018-09-22T10:15:00'
                                  terminal: W
                                  iataCode: ORY
                                arrival:
                                  at: '2018-09-22T12:15:00'
                                  terminal: '4'
                                  iataCode: MAD
                                co2Emissions:
                                  - weight: '100'
                                    weightUnit: KG
                                    cabin: ECONOMY
                          - duration: PT1H20M
                            segments:
                              - id: '20'
                                duration: PT1H20M
                                aircraft:
                                  code: '320'
                                numberOfStops: 0
                                blacklistedInEU: false
                                carrierCode: IB
                                operating:
                                  carrierCode: IB
                                number: '3118'
                                departure:
                                  at: '2018-09-26T23:05:00'
                                  terminal: '4'
                                  iataCode: MAD
                                arrival:
                                  at: '2018-09-26T23:25:00'
                                  terminal: '1'
                                  iataCode: LIS
                                co2Emissions:
                                  - weight: '100'
                                    weightUnit: KG
                                    cabin: ECONOMY
                          - duration: PT4H30M
                            segments:
                              - id: '30'
                                duration: PT2H
                                aircraft:
                                  code: '320'
                                numberOfStops: 0
                                blacklistedInEU: false
                                carrierCode: IB
                                operating:
                                  carrierCode: IB
                                number: '3109'
                                departure:
                                  at: '2018-10-04T12:35:00'
                                  terminal: '1'
                                  iataCode: LIS
                                arrival:
                                  at: '2018-10-04T14:55:00'
                                  terminal: '4'
                                  iataCode: MAD
                                co2Emissions:
                                  - weight: '100'
                                    weightUnit: KG
                                    cabin: ECONOMY
                              - id: '31'
                                duration: PT2H30M
                                aircraft:
                                  code: '320'
                                numberOfStops: 0
                                blacklistedInEU: false
                                carrierCode: IB
                                operating:
                                  carrierCode: IB
                                number: '3444'
                                departure:
                                  at: '2018-10-04T16:05:00'
                                  terminal: '4'
                                  iataCode: MAD
                                arrival:
                                  at: '2018-10-04T18:05:00'
                                  terminal: W
                                  iataCode: ORY
                                co2Emissions:
                                  - weight: '100'
                                    weightUnit: KG
                                    cabin: ECONOMY
                        price:
                          grandTotal: '689.21'
                          total: '423.21'
                          base: '242.00'
                          currency: EUR
                          billingCurrency: EUR
                          fees:
                            - type: SUPPLIER
                              amount: '0'
                            - type: FORM_OF_PAYMENT
                              amount: '6'
                            - type: TICKETING
                              amount: '0'
                          additionalServices:
                            - type: CHECKED_BAGS
                              amount: '100'
                            - type: SEATS
                              amount: '166'
                        pricingOptions:
                          fareType:
                            - PUBLISHED
                          includedCheckedBags: false
                        validatingAirlineCodes:
                          - IB
                        travelerPricings:
                          - travelerId: '1'
                            fareOption: STANDARD
                            travelerType: ADULT
                            price:
                              currency: EUR
                              total: '200.94'
                              base: '126'
                              taxes:
                                - code: YQ
                                  amount: '0.94'
                                - code: CJ
                                  amount: '41.67'
                                - code: FR
                                  amount: '31.33'
                            fareDetailsBySegment:
                              - segmentId: '1'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                              - segmentId: '20'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                              - segmentId: '30'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                              - segmentId: '31'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                          - travelerId: '2'
                            fareOption: STANDARD
                            travelerType: CHILD
                            price:
                              currency: EUR
                              total: '180.94'
                              base: '106'
                              taxes:
                                - code: YQ
                                  amount: '0.94'
                                - code: CJ
                                  amount: '41.67'
                                - code: FR
                                  amount: '31.33'
                            fareDetailsBySegment:
                              - segmentId: '1'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                                additionalServices:
                                  chargeableCheckedBags:
                                    quantity: 1
                                    weight: 20
                                  chargeableSeatNumber: 33D
                              - segmentId: '20'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                                additionalServices:
                                  chargeableCheckedBags:
                                    quantity: 1
                                    weight: 20
                                  chargeableSeatNumber: 28A
                              - segmentId: '30'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                                additionalServices:
                                  chargeableCheckedBags:
                                    quantity: 1
                                    weight: 20
                                  chargeableSeatNumber: 12C
                              - segmentId: '31'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                                additionalServices:
                                  chargeableCheckedBags:
                                    quantity: 1
                                    weight: 20
                                  chargeableSeatNumber: 33D
                          - travelerId: '3'
                            fareOption: STANDARD
                            travelerType: HELD_INFANT
                            associatedAdultId: '1'
                            price:
                              currency: EUR
                              total: '41.33'
                              base: '10'
                              taxes:
                                - code: FR
                                  amount: '31.33'
                            fareDetailsBySegment:
                              - segmentId: '1'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                              - segmentId: '20'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                              - segmentId: '30'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                              - segmentId: '31'
                                cabin: ECONOMY
                                fareBasis: ANNNNF4K
                                brandedFare: LIGHTONE
                                class: A
                                isAllotment: true
                                allotmentDetails:
                                  tourName: tour
                                  tourReference: ref
                                sliceDiceIndicator: ABCDEF
                                includedCheckedBags:
                                  quantity: 0
                    ticketingAggreement:
                      option: DELAY_TO_CANCEL
                      dateTime: '2018-08-21T10:15:00.000'
                    contacts:
                      - companyName: AMADEUS
                        purpose: STANDARD
                        phones:
                          - deviceType: FAX
                            countryCallingCode: '33'
                            number: '480080070'
                          - deviceType: LANDLINE
                            countryCallingCode: '33'
                            number: '480080070'
                        emailAddress: support@mail.com
                        address:
                          lines:
                            - 485 route du Pin Montard
                          postalCode: '06902'
                          cityName: Sophia Antipolis Cedex
                          countryCode: FR
                  dictionaries:
                    locations:
                      CDG:
                        cityCode: PAR
                        countryCode: FR
                      ORY:
                        cityCode: PAR
                        countryCode: FR
                      MAD:
                        cityCode: MAD
                        countryCode: ES
            400_GET_Order:
              description: |
                code    | title                                 
                - | - 
                477     | INVALID FORMAT
                4926    | INVALID DATA RECEIVED
                32171   | MANDATORY DATA MISSING
              schema:
                $ref: '#/definitions/Error_400'
            400_DELETE_Order:
              description: |
                code    | title                                 
                - | - 
                4926    | INVALID DATA RECEIVED
                32171   | MANDATORY DATA MISSING
              schema:
                $ref: '#/definitions/Error_400'
          parameters:
            flight-orderId:
              name: flight-orderId
              description: identifier of the flight order
              required: true
              in: path
              type: string
              x-example: eJzTd9f3s4gKC%2FMEAAt8Ans%3D
          x-generatedAt: '2023-02-01T12:57:32.468Z'
          tags: []
    overlays:
      - type: APIs.io Search
        url: overlays/flight-order-management-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/flight-order-management-openapi-api-evangelist-ratings.yml
  - aid: amadeus:hotel-booking
    name: Hotel Booking
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developers.amadeus.com
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developers.amadeus.com
      - type: OpenAPI
        data:
          swagger: '2.0'
          info:
            title: Hotel Booking
            x-tags:
              - '#mobile-services'
            x-status: validated
          host: test.api.amadeus.com
          basePath: /v1
          schemes:
            - https
          consumes:
            - application/vnd.amadeus+json
          produces:
            - application/vnd.amadeus+json
          paths:
            /booking/hotel-bookings:
              parameters:
                - null
                - null
              post:
                tags:
                  - - - - Booking
                description: ''
                summary: Create Orders associated to the Hotel Offers
          tags:
            - name: Booking
          parameters:
            bookingBody:
              name: requestBody
              in: body
              description: >
                `offerId`, `guests`, `payments` and optional `rooms` for the
                repartition (when used the `rooms` array items must match the
                shopping offer `roomQuantity`)
              required: true
              schema:
                type: object
                title: BookingSchema
                required:
                  - data
                properties:
                  data:
                    type: object
                    title: HotelBookingQuery
                    required:
                      - offerId
                      - guests
                    properties:
                      offerId:
                        type: string
                        description: offerId to book
                        pattern: ^[A-Z0-9]*$
                        minLength: 2
                        maxLength: 100
                        example: >-
                          63A93695B58821ABB0EC2B33FE9FAB24D72BF34B1BD7D707293763D8D9378FC3
                      guests:
                        type: array
                        description: minimum one guest is mandatory
                        minItems: 1
                        maxItems: 99
                        uniqueItems: true
                        items:
                          $ref: '#/definitions/Stakeholder'
                      payments:
                        type: array
                        description: payments (often mandatory)
                        minItems: 1
                        maxItems: 9
                        uniqueItems: true
                        items:
                          $ref: '#/definitions/Payment'
                      rooms:
                        type: array
                        description: >-
                          rooms repartition (when used the `rooms` array items
                          must match the shopping offer `roomQuantity`)
                        minItems: 1
                        maxItems: 9
                        items:
                          type: object
                          title: Room
                          description: room
                          properties:
                            guestIds:
                              type: array
                              description: room main guest (and accompagnants) (optional)
                              uniqueItems: true
                              items:
                                type: integer
                                example: 1
                            paymentId:
                              type: integer
                              description: if missing, the first payment is used (optional)
                              example: 1
                            specialRequest:
                              type: string
                              description: >-
                                special request to send to the reception
                                (optional)
                              minLength: 2
                              maxLength: 120
                              example: I will arrive at midnight
                example:
                  data:
                    offerId: NRPQNQBOJM
                    guests:
                      - name:
                          title: MR
                          firstName: BOB
                          lastName: SMITH
                        contact:
                          phone: '+33679278416'
                          email: bob.smith@email.com
                    payments:
                      - method: creditCard
                        card:
                          vendorCode: VI
                          cardNumber: '0000000000000000'
                          expiryDate: 2026-01
            Ama-Client-Ref:
              name: Ama-Client-Ref
              in: header
              required: false
              type: string
              pattern: ^[A-Z0-9_]*$
              description: Client Reference to track Request/Response
            Accept-Encoding:
              name: Accept-Encoding
              in: header
              required: false
              type: string
              enum:
                - gzip
                - identity
              description: Compress the Response
          definitions:
            ErrorResponse:
              title: ErrorResponse
              type: object
              required:
                - errors
              properties:
                errors:
                  type: array
                  items:
                    $ref: '#/definitions/Error'
            Error:
              type: object
              description: Error
              required:
                - code
                - title
                - status
              properties:
                code:
                  type: integer
                  description: >-
                    [Integer] A machine-readable error code from the Amadeus
                    Canned Messages table, that will enable the API Consumers
                    code to handle this type of error
                  example: 1
                title:
                  type: string
                  description: >-
                    [String] An error title from the Canned Messages table with
                    a 1:1 correspondence to the error code. This may be
                    localized
                  example: Resource not found
                detail:
                  type: string
                  description: >-
                    [String] An easy-to-read explanation specific to this
                    occurrence of the problem. It should give the API consumer
                    an idea of what went wrong and how to recover from it. Like
                    the title, this field value can be localized.
                  example: The targeted resource doesn't exist
                status:
                  type: integer
                  description: >-
                    [Integer] The [HTTP status
                    code](https://www.iana.org/assignments/http-status-codes/http-status-codes.xhtml)
                    of this response. This is present only in terminal errors
                    which cause an unsuccessful response. In the case of
                    multiple errors, they must all have the same status.
                  example: 400
            Warning:
              type: object
              description: Warning
              required:
                - code
                - title
              properties:
                code:
                  type: integer
                  description: >-
                    [Integer] A machine-readable warning code from the Amadeus
                    Canned Messages table, that will enable the API Consumers
                    code to handle this type of warning
                  example: 1
                title:
                  type: string
                  description: >-
                    [String] A warning title from the Canned Messages table with
                    a 1:1 correspondence to the warning code. This may be
                    localized
                  example: Resource not found
                detail:
                  type: string
                  description: >-
                    [String] An easy-to-read explanation specific to this
                    occurrence of the problem. It should give the API consumer
                    an idea of what went wrong and how to recover from it. Like
                    the title, this field value can be localized.
                  example: The targeted resource doesn't exist
            HotelBookingLight:
              type: object
              description: Booking Details
              required:
                - type
                - id
                - providerConfirmationId
              properties:
                type:
                  type: string
                  description: Response Type
                  example: hotel-booking
                id:
                  type: string
                  pattern: ^[A-Z0-9_]*$
                  minLength: 5
                  maxLength: 19
                  description: Booking Id
                  example: XD_8138319951754
                providerConfirmationId:
                  type: string
                  pattern: ^[A-Z0-9_]*$
                  minLength: 2
                  maxLength: 16
                  description: >-
                    GDS Confirmation Number. If you call the Provider, this
                    Reference may be asked
                  example: '8138319951754'
                associatedRecords:
                  type: array
                  minItems: 1
                  maxItems: 1
                  items:
                    $ref: '#/definitions/AssociatedRecord'
                self:
                  type: string
                  format: uri
                  description: Retrieve Booking Details
                  example: >-
                    https://test.api.amadeus.com/v1/booking/hotel-bookings/XD_8138319951754
            AssociatedRecord:
              type: object
              description: Associated Record (Flight Booking Record)
              required:
                - reference
                - originSystemCode
              properties:
                reference:
                  type: string
                  pattern: ^[A-Z0-9]{6}$
                  description: Amadeus GDS Record
                  minLength: 6
                  maxLength: 6
                  example: QVH2BX
                originSystemCode:
                  type: string
                  example: GDS
                  enum:
                    - GDS
                  description: '* GDS: Associated Amadeus GDS Flight Booking PNR Record'
            Stakeholder:
              type: object
              description: Guest Details
              required:
                - name
                - contact
              properties:
                id:
                  type: integer
                  description: item identifier
                  example: 1
                name:
                  $ref: '#/definitions/Name'
                contact:
                  $ref: '#/definitions/Contact'
                hotelRewardsMember:
                  type: string
                  pattern: ^[A-Z0-9-]{1,21}$
                  minLength: 1
                  maxLength: 21
                  example: '3081031320523260'
                  description: >
                    Hotel Chain Rewards Member Number. To receive your Rewards
                    Points, access online check in, fast check out. An error is
                    returned by the Chain if the number is invalid.

                    Example Rewards Programs:

                    * Marriott Bonvoy

                    * Hilton Honors

                    * Hyatt Rewards

                    * IHG Rewards

                    * Wyndham Rewards

                    * Accor Live Limitless ALL

                    * Best Western Rewards

                    * Choice Privileges

                    * Radisson Rewards
              example:
                id: 1
                name:
                  title: MR
                  firstName: BOB
                  lastName: SMITH
                contact:
                  phone: '+33679278416'
                  email: bob.smith@email.com
            Name:
              type: object
              description: Guest Name
              required:
                - firstName
                - lastName
              properties:
                title:
                  type: string
                  description: title/gender of room guest
                  pattern: ^[A-Za-z -]*$
                  minLength: 1
                  maxLength: 54
                  enum:
                    - MR
                    - MRS
                    - MS
                  example: MR
                firstName:
                  type: string
                  description: first name (and middle name) of room guest
                  pattern: ^[A-Za-z \p{Han}\p{Katakana}\p{Hiragana}\p{Hangul}-]*$
                  minLength: 1
                  maxLength: 56
                  example: BOB
                lastName:
                  type: string
                  description: last name of room guest
                  pattern: ^[A-Za-z \p{Han}\p{Katakana}\p{Hiragana}\p{Hangul}-]*$
                  minLength: 1
                  maxLength: 57
                  example: SMITH
            Contact:
              type: object
              description: Contact Details
              required:
                - phone
                - email
              properties:
                phone:
                  type: string
                  description: >-
                    Phone Number in standard
                    E.123(https://en.wikipedia.org/wiki/E.123)
                  pattern: ^[+][1-9][0-9]{4,18}$
                  minLength: 6
                  maxLength: 20
                  example: '+33679278416'
                email:
                  type: string
                  format: email
                  description: Email Address
                  pattern: ^[a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+\\.[a-zA-Z0-9-.]+$
                  minLength: 3
                  maxLength: 90
                  example: bob.smith@email.com
            Payment:
              type: object
              title: Payment
              description: >-
                form of payment (mandatory in case of
                `acceptedPayments`/`methods`)
              required:
                - method
              properties:
                id:
                  type: integer
                  example: 1
                method:
                  type: string
                  example: creditCard
                  enum:
                    - creditCard
                  description: |-
                    The Payment Methods:
                     * creditCard (CC) - Payment Cards in `creditCards` are accepted           
                card:
                  type: object
                  title: Card
                  description: >-
                    payment card details (mandatory in case of `method`
                    creditCard)
                  required:
                    - vendorCode
                    - cardNumber
                    - expiryDate
                  properties:
                    vendorCode:
                      type: string
                      pattern: ^[A-Z]{2}$
                      minLength: 2
                      maxLength: 2
                      example: VI
                      description: |
                        card type (CA, VI, AX, DC...)
                        Examples:
                          * CA - MasterCard (warning: use it instead of MC/IK/EC/MD/XS)
                          * VI - Visa
                          * AX - American Express
                          * DC - Diners Club
                          * AU - Carte Aurore
                          * CG - Cofinoga
                          * DS - Discover
                          * GK - Lufthansa GK Card
                          * JC - Japanese Credit Bureau
                          * TC - Torch Club
                          * TP - Universal Air Travel Card
                          * BC - Bank Card
                          * DL - Delta
                          * MA - Maestro
                          * UP - China UnionPay   
                          * VE - Visa Electron
                    cardNumber:
                      type: string
                      description: card number
                      pattern: ^[0-9]*$
                      minLength: 2
                      maxLength: 22
                    expiryDate:
                      type: string
                      description: Expiration Date YYYY-MM
                      pattern: ^[0-9]{4}-[0-9]{2}$
                      minLength: 7
                      maxLength: 7
                      example: 2019-01
          responses:
            BookingSell:
              description: Booked
              schema:
                type: object
                title: HotelBookedResponse
                properties:
                  warnings:
                    type: array
                    description: All Warnings
                    items:
                      $ref: '#/definitions/Warning'
                  data:
                    type: array
                    description: All room bookings data
                    items:
                      $ref: '#/definitions/HotelBookingLight'
                example:
                  data:
                    - type: hotel-booking
                      id: XD_8138319951754
                      providerConfirmationId: '8138319951754'
                      associatedRecords:
                        - reference: QVH2BX
                          originSystemCode: GDS
            Error400ResponseCreateBooking:
              description: >
                Bad Request


                code    |
                title                                                          |
                owner    | pointer

                - | -- | -- | -
                  477   | INVALID FORMAT                                                 | Amadeus  | 
                 4725   | INVALID PASSENGER ASSOCIATION                                  | Amadeus  | data/rooms/guestIds
                33555   | NUMBER OF ROOMS MISMATCH BETWEEN SHOPPING AND
                BOOKING          | Amadeus  | data/rooms

                33554   | PRICE HAS CHANGED. PLEASE GET A NEW OFFERID AND TRY
                AGAIN      | Amadeus  | data/offerId

                36803   | OFFERID HAS EXPIRED. PLEASE GET A NEW OFFERID AND TRY
                AGAIN    | Amadeus  | data/offerId
                 1205   | INVALID CREDIT CARD TYPE                                       | Amadeus  | data/payments/card/vendorCode
                 8517   | INVALID CREDIT CARD NUMBER                                     | Provider | data/payments/card/cardNumber
                 1427   | GUARANTEE REQUIRED                                             | Provider | data/payments/card
                 1146   | DEPOSIT REQUIRED                                               | Provider | data/payments/card
                 3659   | CREDIT CARD DEPOSIT REQUIRED                                   | Provider | data/payments/card
                 3682   | CREDIT CARD NOT ACCEPTED AT HOTEL PROPERTY                     | Provider | data/payments/card/vendorCode
                 3871   | CREDIT CARD EXPIRATION DATE INVALID FOR CHECK IN DATE          | Provider | data/payments/card/expiryDate
                 
              schema:
                $ref: '#/definitions/ErrorResponse'
            Error500ResponseCreateBooking:
              description: >
                Internal Server Error


                code    |
                title                                                          |
                owner                                

                - | -- | -

                00011   | UNABLE TO
                PROCESS                                              | Provider

                04070   | UNABLE TO PROCESS - CONTACT HELP
                DESK                          | Amadeus
              schema:
                $ref: '#/definitions/ErrorResponse'
          x-generatedAt: '2020-02-12T17:01:55.203Z'
    overlays:
      - type: APIs.io Search
        url: overlays/hotel-booking-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/hotel-booking-openapi-api-evangelist-ratings.yml
  - aid: amadeus:transfer-booking
    name: Transfer Booking
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developers.amadeus.com
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developers.amadeus.com
      - type: OpenAPI
        data:
          swagger: '2.0'
          info:
            title: Transfer Booking
          host: test.api.amadeus.com
          basePath: /v1
          schemes:
            - https
          consumes:
            - application/vnd.amadeus+json
            - application/json
          produces:
            - application/vnd.amadeus+json
            - application/json
          paths:
            /ordering/transfer-orders:
              post:
                tags:
                  - - - - Booking
                summary: Performs a transfer reservation.
                description: ''
          definitions:
            Transfer:
              type: object
              required:
                - transferType
                - start
                - serviceProvider
                - vehicle
                - quotation
                - methodsOfPaymentAccepted
              properties:
                transferType:
                  type: string
                  enum:
                    - PRIVATE
                    - SHARED
                    - TAXI
                    - HOURLY
                    - AIRPORT_EXPRESS
                    - HELICOPTER
                    - PRIVATE_JET
                    - AIRPORT_BUS
                  description: >
                    amadeus transfer service type


                    value           |
                    description                                 

                    --  | 

                    PRIVATE         | Private transfer from point to point

                    SHARED          | Shared transfer from point to point

                    TAXI            | Taxi reservation from point to point,
                    price is estimated

                    HOURLY          | Chauffeured driven transfer per hour

                    AIRPORT_EXPRESS | Express Train from/to Airport

                    AIRPORT_BUS     | Express Bus from/to Airport

                    HELICOPTER      | Private helicopter flight from/to airport

                    PRIVATE_JET     | Private flight from airport to airport
                start:
                  $ref: '#/definitions/Location'
                end:
                  $ref: '#/definitions/Location'
                stopOvers:
                  type: array
                  items:
                    $ref: '#/definitions/StopOver'
                passenegerCharacteristics:
                  type: array
                  items:
                    $ref: '#/definitions/PassengerCharacteristics'
                duration:
                  description: >-
                    transfer duration in
                    [ISO8601](https://en.wikipedia.org/wiki/ISO_8601)
                    PnYnMnDTnHnMnS format, e.g. PT2H10M
                  type: string
                  example: PT2H30M
                vehicle:
                  $ref: '#/definitions/Vehicle'
                serviceProvider:
                  $ref: '#/definitions/ServiceProvider'
                partnerInfo:
                  $ref: '#/definitions/PartnerInfo'
                quotation:
                  $ref: '#/definitions/Quotation'
                converted:
                  $ref: '#/definitions/Quotation'
                extraServices:
                  type: array
                  items:
                    $ref: '#/definitions/ExtraService'
                equipment:
                  type: array
                  items:
                    $ref: '#/definitions/Equipment'
                cancellationRules:
                  type: array
                  items:
                    $ref: '#/definitions/CancellationRule'
                methodsOfPaymentAccepted:
                  type: array
                  description: list of payment methods, allowed by provider
                  items:
                    type: string
                    description: >-
                      Method of payment required when PaymentType equal BT
                      (applicable only for reservation action).
                    enum:
                      - CREDIT_CARD
                      - INVOICE
                      - TRAVEL_ACCOUNT
                      - PAYMENT_SERVICE_PROVIDER
                discountCodes:
                  type: array
                  description: list of discount codes
                  items:
                    $ref: '#/definitions/DiscountCode'
                distance:
                  $ref: '#/definitions/Distance'
            TransferReservation:
              description: transfer reservation
              allOf:
                - type: object
                  properties:
                    confirmNbr:
                      type: string
                      description: >-
                        transfer identifier - confirmation number, received from
                        transfer supplier
                    status:
                      type: string
                      description: status of transfer reservation
                      enum:
                        - CONFIRMED
                        - CANCELLED
                    note:
                      type: string
                      description: Note to transfer provider
                    methodOfPayment:
                      type: string
                      description: >-
                        Method of payment required when PaymentType equal BT
                        (applicable only for reservation action).
                      enum:
                        - CREDIT_CARD
                        - INVOICE
                        - TRAVEL_ACCOUNT
                        - PAYMENT_SERVICE_PROVIDER
                    paymentServiceProvider:
                      type: string
                      description: >-
                        payment service provider details will be passed to
                        provider in case "PAYMENT_SERVICE_PROVIDER" method of
                        payment.
                      enum:
                        - STRIPE_CONNECT
                    offerId:
                      type: string
                      description: offer identifier
                - $ref: '#/definitions/Transfer'
            TransferOrder:
              type: object
              required:
                - type
                - id
                - transfers
              properties:
                type:
                  description: the resource name
                  type: string
                id:
                  type: string
                  description: transfer order identifier
                reference:
                  type: string
                  description: reference of the Trip e.g. YNK4JQ
                transfers:
                  type: array
                  description: transfer reservations, included in the order
                  items:
                    $ref: '#/definitions/TransferReservation'
                passengers:
                  type: array
                  description: passengers, related to the Transfer Order
                  items:
                    $ref: '#/definitions/Passenger'
                agency:
                  $ref: '#/definitions/Agency'
            AddressCommon:
              description: address of the departure location
              properties:
                line:
                  description: Address line with street, number, bulding, etc...
                  type: string
                  minLength: 1
                  maxLength: 70
                zip:
                  description: Post office code number
                  type: string
                  minLength: 1
                  maxLength: 120
                countryCode:
                  description: Country code (two character standard IATA country code)
                  type: string
                  pattern: '[a-zA-Z]{2}'
                cityName:
                  description: City, town or postal station
                  type: string
                  minLength: 1
                  maxLength: 35
                stateCode:
                  description: State code (two character standard IATA state code)
                  type: string
                  pattern: '[a-zA-Z0-9]{1-2}'
            Address:
              type: object
              description: address information
              properties:
                line:
                  description: Address line with street, number, bulding, etc...
                  type: string
                  minLength: 1
                  maxLength: 70
                zip:
                  description: Post office code number
                  type: string
                  minLength: 1
                  maxLength: 120
                countryCode:
                  description: Country code (two character standard IATA country code)
                  type: string
                  pattern: '[a-zA-Z]{2}'
                cityName:
                  description: City, town or postal station
                  type: string
                  minLength: 1
                  maxLength: 35
                stateCode:
                  description: State code (two character standard IATA state code)
                  type: string
                  pattern: '[a-zA-Z0-9]{1-2}'
                latitude:
                  description: latitude of the location
                  type: number
                  format: double
                  example: 43.580418
                longitude:
                  description: longitude of the location
                  type: number
                  format: double
                  example: 7.125102
            Agency:
              type: object
              description: Agency email information.
              properties:
                contacts:
                  type: array
                  description: List of contact information
                  items:
                    type: object
                    properties:
                      email:
                        type: object
                        description: Email information.
                        title: Email
                        properties:
                          address:
                            type: string
                            format: email
                            description: Email address (e.g. john@smith.com)
            Baggage:
              type: object
              properties:
                count:
                  type: integer
                  description: baggage capacity
                  example: 3
                size:
                  type: string
                  description: "baggage size\n\ncode   | name                                 \n | - \nS \t   | Small\nM \t   | Medium\nL \t   | Large\n"
                  enum:
                    - S
                    - M
                    - L
            CancellationRule:
              type: object
              description: cancellation rule information
              properties:
                ruleDescription:
                  type: string
                  description: description of cancellation rule
                feeType:
                  type: string
                  enum:
                    - PERCENTAGE
                    - VALUE
                  description: >
                    type of fee - percentage of total amount (PERCENTAGE) or
                    fixed amount (VALUE)
                feeValue:
                  type: string
                  description: value of the fee, e.g. "100" or "12.50"
                currencyCode:
                  type: string
                  pattern: '[A-Z]{3}'
                  description: >-
                    currency code of the fee in [ISO
                    4217](https://en.wikipedia.org/wiki/ISO_4217) format, e.g.
                    USD, EUR
                metricType:
                  type: string
                  description: type of metric
                  enum:
                    - MINUTES
                    - HOURS
                    - DAYS
                    - YEARS
                metricMin:
                  type: string
                  description: metric min value
                metricMax:
                  type: string
                  description: metric max value
            Contact:
              type: object
              properties:
                phoneNumber:
                  type: string
                  pattern: ([+]?)[0-9]{1,20}
                  description: Contact phone number
                email:
                  type: string
                  format: email
                  description: Contact email
            Corporation:
              type: object
              description: information about corporation
              properties:
                address:
                  $ref: '#/definitions/AddressCommon'
                info:
                  type: object
                  description: "corporate information map. Possible keys\n\nkey    | name\n | -\nAU\t   | Accounting Unit\nON\t   | Order Number\nDC\t   | Department Code\nCC\t   | Company Code\nCN\t   | Company Name\nIA\t   | Internal Account\nCE\t   | Cost Centre\nEN\t   | Employee Number\nPN\t   | Project Number\n"
                  additionalProperties:
                    type: string
                  example:
                    AU: Accounting Unit
                    'ON': Order Number
                    DC: Department Code
                    CC: Company Code
                    CN: Company Name
                    IA: Internal Account
                    CE: Cost Centre
                    EN: Employee Number
                    PN: Project Number
            CreditCard:
              type: object
              description: information about payment card
              required:
                - number
                - holderName
                - vendorCode
                - expiryDate
              properties:
                number:
                  type: string
                  pattern: '[0-9]{16}'
                  description: card number
                holderName:
                  type: string
                  description: card holder name
                vendorCode:
                  type: string
                  pattern: '[a-zA-Z]{2}'
                  description: >-
                    card vendor code, e.g VI – VISA, CA – MasterCard, AX –
                    American Express etc
                expiryDate:
                  type: string
                  pattern: ^(0[1-9]|1[0-2])[0-9]{2}$
                  description: card expiry date in format MMYY, e.g. 0237 for February 2037
                cvv:
                  type: string
                  pattern: '[a-zA-Z0-9]{3,4}'
                  description: >-
                    cerification calue number, as indicated on the credit card.
                    Only for query
            DiscountCode:
              type: object
              description: discount object that gives access to negotiated prices
              properties:
                type:
                  type: string
                  description: describes type of discount
                  enum:
                    - CD
                    - PC
                value:
                  type: string
                  description: >-
                    discount code value. 

                    "CD" type stands for corporate discount code - a number
                    generated by provider in case of
                      special agreement with a given subscriber is passed (airlines, TMC,
                      corporation…). It gives to subscriber access to negotiated prices for
                      transfer      
                    "PC" - for promotional/campaign discount code - a voucher
                    code generated by the
                      provider valid for a given period of time or a given number of usage.
                      The code is sent by customer to provider in order to get a discounted
                      price.
            Distance:
              properties:
                value:
                  description: >-
                    great-circle distance between two locations. This distance
                    thus do not take into account traffic conditions;
                    international boundaries; mountains; water; or other
                    elements that might make the a nearby location hard to
                    reach.
                  type: integer
                  example: 152
                unit:
                  description: unit of the distance
                  type: string
                  example: KM
                  enum:
                    - KM
                    - MI
            Equipment:
              type: object
              description: extra equipment information
              required:
                - code
              properties:
                code:
                  type: string
                  description: >
                    extra equipment codes, which can take following values


                    code   | name                                 

                     | -  

                    BBS    | Baby stroller/Push chair

                    BYC    | Bicycle rack

                    CBB    | Cargo barrier rack

                    CBF    | Cargo barrier front

                    CBS    | Booster seat for child under 135cm or up to 12
                    years

                    CSB    | Child seat determined by weight/age of child 1-3
                    years / 9-18 Kg

                    CSI    | Child seat determined by weight/age of child 0-12
                    month/0-13Kg

                    CST    | Child seat determined by weight/age of child 4-7
                    years/15 – 30 Kg

                    SBR    | Snow board racks

                    SKB    | Ski box

                    SKR    | Ski rack

                    TAB    | Travel Tablet 

                    WAR    | Wheelchair access ramp

                    WHC    | Wheelchair

                    WIF    | Wi-Fi access

                    CNT    | Charger cable
                  enum:
                    - BBS
                    - BYC
                    - CBB
                    - CBF
                    - CBS
                    - CSB
                    - CSI
                    - CST
                    - SBR
                    - SKB
                    - SKR
                    - 'TAB '
                    - WAR
                    - WHC
                    - WIF
                    - CNT
                itemId:
                  type: string
                  description: extra equipment identifier
                description:
                  type: string
                  description: extra equipment description
                quotation:
                  $ref: '#/definitions/Quotation'
                converted:
                  $ref: '#/definitions/Quotation'
                isBookable:
                  type: boolean
                  description: true if extra equipment is available for booking
                taxIncluded:
                  type: boolean
                  description: true if tax included in extra equipment price
                includedInTotal:
                  type: boolean
                  description: >-
                    true if extra equipment price is included in total transfer
                    amount
            ExtraService:
              type: object
              required:
                - code
              properties:
                code:
                  type: string
                  description: >
                    extra service code, which can take following values


                    code   | name                                 

                     | - 

                    DSL    | Driver language specified

                    EWT    | Extra waiting time

                    MAG    | Meet & Greet

                    FLM    | Flight monitoring

                    NWS    | Newspaper

                    CAI    | Cancellation insurance

                    WNR    | Wait and Return. Driver waits at destination and
                    brings back the customer to pick-up point
                  enum:
                    - DSL
                    - EWT
                    - MAG
                    - FLM
                    - NWS
                    - CAI
                    - WNR
                itemId:
                  type: string
                  description: extra service identifier
                description:
                  type: string
                  description: extra service description
                metricType:
                  type: string
                  description: extra service time metric type
                  enum:
                    - YEARS
                    - DAYS
                    - HOURS
                    - MINUTES
                metricValue:
                  type: string
                  description: extra service metric value
                quotation:
                  $ref: '#/definitions/Quotation'
                converted:
                  $ref: '#/definitions/Quotation'
                isBookable:
                  type: boolean
                  description: true if extra service is available for booking
                taxIncluded:
                  type: boolean
                  description: true if tax included in extra service price
                includedInTotal:
                  type: boolean
                  description: >-
                    true if extra service price is included in total transfer
                    amount
            Fee:
              description: single fee information
              allOf:
                - $ref: '#/definitions/PointsAndCash'
                - type: object
                  properties:
                    currencyCode:
                      type: string
                      example: USD
                    indicator:
                      type: string
                      description: >-
                        fee category e.g. "AIRPORT", "CREDITCARD"
                        ,"CANCELLATION"
            Location:
              type: object
              description: location information
              properties:
                dateTime:
                  description: >
                    date and time specified in the [ISO
                    8601](https://en.wikipedia.org/wiki/ISO_8601)
                    YYYY-MM-DDThh:mm:ss format e.g. 2017-11-10T10:00:00

                    not supported for stopOvers object
                  type: string
                  example: '2019-11-10T10:30:00'
                locationCode:
                  type: string
                  description: >-
                    airport code from [IATA table
                    codes](http://www.iata.org/publications/Pages/code-search.aspx),
                    e.g. CDG.
                  pattern: '[A-Za-z]{3}'
                  example: CDG
                lfiCode:
                  type: string
                  description: >-
                    internal airport identifier used for private jets and
                    helicopters e.g. IT87100
                  example: IT87100
                address:
                  $ref: '#/definitions/Address'
                name:
                  type: string
                  description: Place name e.g. Airport Name, Hotel Name etc.
                googlePlaceId:
                  description: >-
                    Google place id only for google address e.g.
                    ChIJL-DOWeBv5kcRfTbh97PimNc.
                  type: string
                  example: ChIJrTLr-GyuEmsRBfy61i59si0
                uicCode:
                  type: string
                  description: >-
                    UIC code defined by the worldwide railway organization e.g.
                    8600626
            StopOver:
              description: >-
                Location of the stop over or the several stop over points. It
                can be defined either using IATA code or Address (address line,
                zip, country, city, state, latitude, longitude, lfi). Vehicle
                change via stop overs is not supported.
              properties:
                duration:
                  description: >-
                    transfer stop duration in
                    [ISO8601](https://en.wikipedia.org/wiki/ISO_8601)
                    PnYnMnDTnHnMnS format, e.g. PT2H10M.
                  type: string
                  example: PT2H30M
                sequenceNumber:
                  description: sequence number of the stop e.g. 3
                  type: number
                  example: 1
                location:
                  $ref: '#/definitions/Location'
            PassengerCharacteristics:
              properties:
                passengerTypeCode:
                  description: >-
                    Passenger type codes e.g. CHD , ADT. CHD is for child and
                    ADT for Adult.
                  type: string
                  example: child
                age:
                  type: integer
                  description: Age of the Passenger (Mandatory if typeCode= “CHD”)
                  example: 12
            LoyaltyNumber:
              type: object
              properties:
                program:
                  type: string
                  description: loyalty program name
                value:
                  type: string
                  description: loyalty number value
            Name:
              type: object
              description: description of the name of a physical person
              properties:
                type:
                  description: The type of the Name
                  type: string
                firstName:
                  description: First name.
                  type: string
                lastName:
                  description: Last name.
                  type: string
                title:
                  description: >-
                    Contains all the suffixes and prefixes that can be appended
                    to a name - Mr, Miss, Pr. - E.g. " Mr".
                  type: string
            Passenger:
              description: passenger data
              allOf:
                - $ref: '#/definitions/Name'
                - type: object
                  properties:
                    contacts:
                      $ref: '#/definitions/Contact'
                    billingAddress:
                      $ref: '#/definitions/AddressCommon'
            Payment:
              type: object
              description: >
                defines the payment in transfer reservation. For "CREDIT_CARD" -
                creditCard is mandatory, for "INVOICE" - paymentReference is
                mandatory, for "TRAVEL_ACCOUNT" - paymentReference is optional,
                for "PAYMENT_SERVICE_PROVIDER" - paymentServiceProvider and
                paymentReference are mandatory.
              properties:
                methodOfPayment:
                  type: string
                  description: >-
                    Method of payment required when PaymentType equal BT
                    (applicable only for reservation action).
                  enum:
                    - CREDIT_CARD
                    - INVOICE
                    - TRAVEL_ACCOUNT
                    - PAYMENT_SERVICE_PROVIDER
                paymentReference:
                  type: string
                  description: >-
                    payment refence that will be passed to provider in case
                    "INVOICE" or "TRAVEL_ACCOUNT" method of payment
                paymentServiceProvider:
                  type: string
                  description: >-
                    payment service provider details will be passed to provider
                    in case "PAYMENT_SERVICE_PROVIDER" method of payment.
                  enum:
                    - STRIPE_CONNECT
                creditCard:
                  $ref: '#/definitions/CreditCard'
            PartnerInfo:
              type: object
              description: >-
                Information about partner/subprovider. Below settings
                configuration is not applicable for sub-provider. Fields 'code',
                'name' and 'logoUrl' are not mandatory for sub-provider.
              properties:
                serviceProvider:
                  $ref: '#/definitions/ServiceProvider'
            PointsAndCash:
              type: object
              properties:
                monetaryAmount:
                  type: string
                  example: '10.5'
            Quotation:
              description: >-
                quotation representing a price valuation and its components. The
                monetaryAmount at the root are the sum of base and all the
                taxes/fees/discounts
              allOf:
                - $ref: '#/definitions/PointsAndCash'
                - type: object
                  properties:
                    currencyCode:
                      type: string
                      example: USD
                    isEstimated:
                      type: boolean
                      description: >-
                        indicates if the price is pre-estimated prior to ride.
                        Becomes mandatory for transferType = TAXI
                    base:
                      description: base price
                      allOf:
                        - $ref: '#/definitions/PointsAndCash'
                    discount:
                      description: discount amount of base price
                      allOf:
                        - $ref: '#/definitions/PointsAndCash'
                    taxes:
                      description: Taxes breakdown
                      type: array
                      items:
                        $ref: '#/definitions/Tax'
                    fees:
                      description: Fees breakdown
                      type: array
                      items:
                        $ref: '#/definitions/Fee'
                    totalTaxes:
                      $ref: '#/definitions/PointsAndCash'
                    totalFees:
                      $ref: '#/definitions/PointsAndCash'
            Seat:
              type: object
              properties:
                count:
                  type: integer
                  description: seat capacity
                  example: 3
                row:
                  type: string
                  description: seat row
                  example: front
                size:
                  type: string
                  description: seat size
                  example: XL
            ServiceProvider:
              type: object
              description: information about provider
              required:
                - code
                - name
                - logoUrl
              properties:
                code:
                  type: string
                  pattern: '[a-zA-Z]{3}'
                  description: provider code
                name:
                  type: string
                  pattern: '[a-zA-Z]{30}'
                  description: provider name
                logoUrl:
                  type: string
                  description: URL to provider logo
                termsUrl:
                  type: string
                  description: URL to provider's terms and conditions page
                isPreferred:
                  type: boolean
                  description: indicates if sub-provider is preferred for the travel-seller
                contacts:
                  $ref: '#/definitions/ContactWithAddress'
                settings:
                  type: array
                  description: list of provider settings
                  items:
                    type: string
                    description: provider setting
                    enum:
                      - BILLING_ADDRESS_REQUIRED
                      - FLIGHT_NUMBER_REQUIRED
                      - CVV_NUMBER_REQUIRED
                businessIdentification:
                  description: >-
                    Information about the Customer stakeholder participating to
                    the described sales summary.
                  properties:
                    vatRegistrationNumber:
                      type: string
                      description: >-
                        VAT (Value Added Tax) Registration Number of the
                        customer applicable ot the current sales.
            Tax:
              description: single tax information
              allOf:
                - type: object
                  properties:
                    monetaryAmount:
                      type: string
                      example: '10.5'
                - type: object
                  properties:
                    indicator:
                      type: string
                      description: Tax category
                    natureCode:
                      type: string
                      description: Tax code
                    countryCode:
                      type: string
                      description: Tax iso country code
                    rate:
                      type: string
                      description: Tax rate
            TransportationType:
              type: string
              title: TransportationType
              description: The type of connection "FLIGHT" or "TRAIN"
              enum:
                - FLIGHT
                - TRAIN
            TravelSegment:
              description: >-
                A segment of an itinerary used by a traveler between 2 locations
                at a given date and time using a particular transportation type
                FLIGHT or TRAIN
              type: object
              properties:
                transportationType:
                  $ref: '#/definitions/TransportationType'
                transportationNumber:
                  type: string
                  example: AF380
                  description: The flight number or train number, e.g. AF380
                departure:
                  $ref: '#/definitions/TravelSegmentLocation'
                arrival:
                  $ref: '#/definitions/TravelSegmentLocation'
            TravelSegmentLocation:
              description: >-
                The flight or train departure/arrival date&time, location
                information
              type: object
              properties:
                uicCode:
                  type: string
                  description: >-
                    The railway UIC code defined by the worldwide railway
                    organization, e.g. 7400001
                  example: 7400001
                iataCode:
                  type: string
                  description: The airport code from IATA table codes, e.g. CDG
                  example: CDG
                localDateTime:
                  type: string
                  description: >-
                    The date and time inspired from ISO 8601
                    (YYYY-MM-DDTHH:MM:SS) format
                  format: date-time
                  example: '2021-03-27T20:03:00'
            Vehicle:
              type: object
              required:
                - code
                - category
                - description
                - seats
              properties:
                code:
                  type: string
                  enum:
                    - CAR
                    - SED
                    - WGN
                    - ELC
                    - VAN
                    - SUV
                    - LMS
                    - MBR
                    - TRN
                    - BUS
                    - HLC
                    - JET
                  description: >
                    vehicle type, which can take following values


                    value           | description

                    --  | 

                    CAR             | Car

                    SED             | Sedan

                    WGN             | Wagon

                    ELC             | Electric car

                    VAN             | Van or minivan

                    SUV             | Sport utility vehicle

                    LMS             | Limousine

                    MBR             | Motorbike

                    TRN             | Train

                    BUS             | Bus

                    HLC             | Helicopter (accessible only for private
                    jet transfer)

                    JET             | Jet (accessible only for private jet
                    transfer)
                category:
                  type: string
                  enum:
                    - ST
                    - BU
                    - FC
                  description: |
                    category of the vehicle, which can take following values

                    value           | description
                    --  | 
                    ST              | Standard
                    BU              | Business
                    FC              | First class
                description:
                  type: string
                  description: >-
                    description of the vehicle. Can describe a list of potential
                    vehicles, e.g. VW Polo or similar
                seats:
                  type: array
                  items:
                    $ref: '#/definitions/Seat'
                baggages:
                  type: array
                  items:
                    $ref: '#/definitions/Baggage'
                imageURL:
                  type: string
                  description: URL to vehicle image
            Error_400:
              properties:
                errors:
                  type: array
                  items:
                    $ref: '#/definitions/Issue'
              required:
                - errors
              example:
                errors:
                  - status: 400
                    code: 4926
                    title: INVALID DATA RECEIVED
                    detail: Transfer type is not valid
                    source:
                      parameter: transferType
            Error_401:
              properties:
                errors:
                  type: array
                  items:
                    $ref: '#/definitions/Issue'
              required:
                - errors
              example:
                errors:
                  - status: 401
                    code: 20
                    title: RESTRICTED
                    detail: Query unauthorized
            Error_500:
              properties:
                errors:
                  type: array
                  items:
                    $ref: '#/definitions/Issue'
              required:
                - errors
              example:
                errors:
                  - status: 500
                    code: 141
                    title: SYSTEM ERROR HAS OCCURRED
            Issue:
              properties:
                status:
                  description: the HTTP status code applicable to this error
                  type: integer
                code:
                  description: an application-specific error code
                  type: integer
                  format: int64
                title:
                  description: a short summary of the error
                  type: string
                detail:
                  description: explanation of the error
                  type: string
                source:
                  type: object
                  title: Issue_Source
                  description: an object containing references to the source of the error
                  maxProperties: 1
                  properties:
                    pointer:
                      description: >-
                        a JSON Pointer [RFC6901] to the associated entity in the
                        request document
                      type: string
                    parameter:
                      description: >-
                        a string indicating which URI query parameter caused the
                        issue
                      type: string
                    example:
                      description: a string indicating an example of the right value
                      type: string
            ContactWithAddress:
              allOf:
                - $ref: '#/definitions/Contact'
                - type: object
                  properties:
                    address:
                      $ref: '#/definitions/AddressCommon'
              description: Contact and Adress details
          responses:
            '401':
              description: Unauthorized
              schema:
                $ref: '#/definitions/Error_401'
            '500':
              description: Unexpected Error
              schema:
                $ref: '#/definitions/Error_500'
            transfer_order:
              description: Successful Operation
              schema:
                title: Success_Reservation
                required:
                  - data
                properties:
                  data:
                    $ref: '#/definitions/TransferOrder'
                  warnings:
                    type: array
                    items:
                      $ref: '#/definitions/Issue'
                example:
                  data:
                    type: transfer-order
                    id: UVZTWlJJfERPRQ
                    reference: YNK4JQ
                    agency:
                      contacts:
                        - email:
                            address: abc@test.com
                    transfers:
                      - status: CONFIRMED
                        confirmNbr: '2904892'
                        note: Note to driver
                        methodOfPayment: CREDIT_CARD
                        offerId: 0cb11574-4a02-11e8-842f-0ed5f89f718b
                        transferType: PRIVATE
                        start:
                          dateTime: '2019-11-10T10:30:00'
                          locationCode: CDG
                        end:
                          address:
                            line: Avenue de la Bourdonnais, 19
                            zip: '75007'
                            countryCode: FR
                            cityName: Paris
                            latitude: 48.859466
                            longitude: 2.2976965
                            uicCode: '7400001'
                          googlePlaceId: ChIJL-DOWeBv5kcRfTbh97PimNc
                          name: Souvenirs De La Tour
                        stopOvers:
                          - duration: PT2H30M
                            sequenceNumber: 1
                            location:
                              locationCode: CDG
                              lfiCode: FR01216
                              address:
                                line: Avenue de la Bourdonnais, 19
                                zip: '75007'
                                countryCode: FR
                                cityName: Paris
                                latitude: 48.859477
                                longitude: 2.2976975
                              googlePlaceId: DOWeBv5kcRfTbh97PimN
                              name: De La Tours
                        vehicle:
                          code: VAN
                          category: BU
                          description: >-
                            Mercedes-Benz V-Class, Chevrolet Suburban, Cadillac
                            Escalade or similar
                          seats:
                            - count: 3
                          baggages:
                            - count: 3
                              size: M
                          imageURL: https://provider.com/images/BU_VAN.png
                        serviceProvider:
                          code: ABC
                          name: Provider name
                          logoUrl: https://provider.com/images/logo.png
                          termsUrl: https://provider.com/terms_and_conditions.html
                          contacts:
                            phoneNumber: '+33123456789'
                            email: support@provider.com
                            address:
                              line: Avenue de la Bourdonnais, 19
                              zip: '75007'
                              countryCode: FR
                              cityName: Paris
                              stateCode: CDG
                          settings:
                            - BILLING_ADDRESS_REQUIRED
                            - FLIGHT_NUMBER_REQUIRED
                            - CVV_NUMBER_REQUIRED
                          businessIdentification:
                            vatRegistrationNumber: GB999 9999 22
                        partnerInfo:
                          serviceProvider:
                            code: XYZ
                            name: SubProvider name
                            logoUrl: https://provider.com/images/logo.png
                            termsUrl: https://provider.com/terms_and_conditions.html
                            isPreferred: true
                            contacts:
                              phoneNumber: '+33123456789'
                              email: support@provider.com
                              address:
                                line: Avenue de la Bourdonnais, 19
                                zip: '75007'
                                countryCode: FR
                                cityName: Paris
                                stateCode: CDG
                            businessIdentification:
                              vatRegistrationNumber: GB999 9999 22
                        quotation:
                          monetaryAmount: '63.70'
                          currencyCode: USD
                          isEstimated: false
                          base:
                            monetaryAmount: '103.70'
                          discount:
                            monetaryAmount: '50.00'
                          fees:
                            - indicator: AIRPORT
                              monetaryAmount: '10.00'
                          totalTaxes:
                            monetaryAmount: '12.74'
                          totalFees:
                            monetaryAmount: '10.00'
                        converted:
                          monetaryAmount: '63.70'
                          currencyCode: EUR
                          isEstimated: false
                          base:
                            monetaryAmount: '103.70'
                          discount:
                            monetaryAmount: '50.00'
                          fees:
                            - indicator: AIRPORT
                              monetaryAmount: '10.00'
                          totalTaxes:
                            monetaryAmount: '12.74'
                          totalFees:
                            monetaryAmount: '10.00'
                        extraServices:
                          - code: EWT
                            itemId: EWT0291
                            description: Extra 15 min. wait
                            quotation:
                              monetaryAmount: '39.20'
                              currencyCode: USD
                              base:
                                monetaryAmount: '36.00'
                              totalTaxes:
                                monetaryAmount: '3.20'
                            converted:
                              monetaryAmount: '32.70'
                              currencyCode: EUR
                              base:
                                monetaryAmount: '30.00'
                              totalTaxes:
                                monetaryAmount: '2.7'
                            isBookable: true
                            taxIncluded: true
                            includedInTotal: true
                        cancellationRules:
                          - feeType: PERCENTAGE
                            feeValue: '100'
                            metricType: DAYS
                            metricMin: '0'
                            metricMax: '1'
                          - feeType: PERCENTAGE
                            feeValue: '0'
                            metricType: DAYS
                            metricMin: '1'
                            metricMax: '100'
                        distance:
                          value: 152
                          unit: KM
                    passengerCharacteristics:
                      - passengerTypeCode: ADT
                        age: 20
                    passengers:
                      - firstName: John
                        lastName: Doe
                        title: MR
                        contacts:
                          phoneNumber: '+33123456789'
                          email: user@email.com
                        billingAddress:
                          line: Avenue de la Bourdonnais, 19
                          zip: '75007'
                          countryCode: FR
                          cityName: Paris
            400_createTransferOrder:
              description: |
                code    | title                                 
                - | - 
                11      | UNABLE TO PROCESS
                391     | NEED TELEPHONE NUMBER
                477     | INVALID FORMAT
                693     | INVALID CITY/AIRPORT CODE
                830     | MISSING/INVALID COUNTRY CODE
                1143    | INVALID CREDIT CARD NUMBER
                1149    | CREDIT CARD EXPIRED
                1426    | EXPIRATION DATE MISSING OR INVALID
                1535    | INVALID VENDOR CODE
                4926    | INVALID DATA RECEIVED 
                11041   | NEED PASSENGER NAME
                11257   | NEED CITY NAME
                12237   | ZIP CODE IS MANDATORY IN ADDRESS
                23883   | EMAIL ADDRESS REQUIRED
                25862   | CREDIT CARD HOLDER NAME REQUIRED
                27599   | INVALID PASSENGER NAME
                28926   | MISSING CARD VERIFICATION VALUE CVV
                32171   | MANDATORY DATA MISSING 
                32804   | INVALID PHONE NUMBER
                34120   | INVALID EMAIL ADDRESS
                34497   | THE LINE IS MANDATORY IN ADDRESS
                34502   | PAYMENT METHOD IS REQUIRED
                37576   | INVALID PAYMENT METHOD
                38597   | CREDIT CARD NUMBER IS REQUIRED
                45514   | INVALID BILLING ADDRESS
                34649   | INVALID FLIGHT INFORMATION
                15566   | INVALID RAIL INFORMATION
              schema:
                $ref: '#/definitions/Error_400'
          x-generatedAt: '2021-04-19T12:58:58.637Z'
          tags: []
    overlays:
      - type: APIs.io Search
        url: overlays/transfer-booking-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/transfer-booking-openapi-api-evangelist-ratings.yml
  - aid: amadeus:transfer-management
    name: Transfer Management
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developers.amadeus.com
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developers.amadeus.com
      - type: OpenAPI
        data:
          swagger: '2.0'
          info:
            title: Transfer Management
          host: test.api.amadeus.com
          basePath: /v1
          schemes:
            - https
          consumes:
            - application/vnd.amadeus+json
            - application/json
          produces:
            - application/vnd.amadeus+json
            - application/json
          paths:
            /ordering/transfer-orders/{orderId}/transfers/cancellation:
              post:
                tags:
                  - - - - Booking
                summary: Cancel a transfer in an existing orderId.
                description: ''
          definitions:
            TransferCancellation:
              type: object
              description: information returned in cancelation response
              properties:
                confirmNbr:
                  type: string
                  description: >-
                    transfer identifier - confirmation number from service
                    provider that identifies the ride
                reservationStatus:
                  type: string
                  enum:
                    - CANCELLED
                    - CONFIRMED
                  description: status of reservation
            Error_400:
              properties:
                errors:
                  type: array
                  items:
                    $ref: '#/definitions/Issue'
              required:
                - errors
              example:
                errors:
                  - status: 400
                    code: 4926
                    title: INVALID DATA RECEIVED
                    detail: Transfer type is not valid
                    source:
                      parameter: transferType
            Error_401:
              properties:
                errors:
                  type: array
                  items:
                    $ref: '#/definitions/Issue'
              required:
                - errors
              example:
                errors:
                  - status: 401
                    code: 20
                    title: RESTRICTED
                    detail: Query unauthorized
            Error_404:
              properties:
                errors:
                  type: array
                  items:
                    $ref: '#/definitions/Issue'
              required:
                - errors
              example:
                errors:
                  - status: 404
                    code: 1797
                    title: NOT FOUND
                    detail: no response found for this query parameter
                    source:
                      parameter: orderId
            Error_500:
              properties:
                errors:
                  type: array
                  items:
                    $ref: '#/definitions/Issue'
              required:
                - errors
              example:
                errors:
                  - status: 500
                    code: 141
                    title: SYSTEM ERROR HAS OCCURRED
            Issue:
              properties:
                status:
                  description: the HTTP status code applicable to this error
                  type: integer
                code:
                  description: an application-specific error code
                  type: integer
                  format: int64
                title:
                  description: a short summary of the error
                  type: string
                detail:
                  description: explanation of the error
                  type: string
                source:
                  type: object
                  title: Issue_Source
                  description: an object containing references to the source of the error
                  maxProperties: 1
                  properties:
                    pointer:
                      description: >-
                        a JSON Pointer [RFC6901] to the associated entity in the
                        request document
                      type: string
                    parameter:
                      description: >-
                        a string indicating which URI query parameter caused the
                        issue
                      type: string
                    example:
                      description: a string indicating an example of the right value
                      type: string
          responses:
            '400':
              description: "code    | title                                 \n- | -                 \n32171   | MANDATORY DATA MISSING \t     \n"
              schema:
                $ref: '#/definitions/Error_400'
            '401':
              description: Unauthorized
              schema:
                $ref: '#/definitions/Error_401'
            '404':
              description: Not Found
              schema:
                $ref: '#/definitions/Error_404'
            '500':
              description: Unexpected Error
              schema:
                $ref: '#/definitions/Error_500'
            transfer_cancel:
              description: Successful Operation
              schema:
                title: Success_Cancellation
                required:
                  - data
                properties:
                  data:
                    $ref: '#/definitions/TransferCancellation'
                example:
                  data:
                    confirmNbr: '2904892'
                    reservationStatus: CANCELLED
          x-generatedAt: '2021-04-19T12:58:58.637Z'
          tags: []
    overlays:
      - type: APIs.io Search
        url: overlays/transfer-management-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/transfer-management-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---