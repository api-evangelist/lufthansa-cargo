# Lufthansa Cargo (lufthansa-cargo)

Lufthansa Cargo AG is the air freight arm of the Lufthansa Group, headquartered in Frankfurt, Germany. It sells and operates belly capacity across the Lufthansa passenger fleet plus its own Boeing 777F freighters, and runs the Frankfurt Cargo Center hub, so it sits in the chain as the airline carrier between the freight forwarder and the destination handling agent. Its API posture is real but two-speed: a live Apigee developer portal at developer.lufthansa-cargo.com publishes four OpenAPI 3.0 contracts anonymously downloadable without a login (Routing Offer, Shipment Tracking, Shipment Tracking Subscribe, Station Information), while six further API products in the same portfolio - smartBooking, Truck PreAdvice, ULD Status, AirMail, CargoXML and CargoIMP - are published only as info-block stubs carrying the sentence that access is granted upon prior approval and agreement. Registration is reviewed by Lufthansa Cargo API managers before keys are issued and production access requires successful test-environment validation, so this is application-approval, not self-serve. The published REST surface is a proprietary Lufthansa Cargo shape, but it carries open air-cargo vocabulary inside it - IATA AWB prefix 020 plus 8-digit AWB numbers, 3-letter IATA station codes and the IATA cargo status code set (RCS, MAN, DEP, ARR, RCF, NFD, DLV) - while the legacy Cargo-IMP and Cargo-XML EDI message sets remain in the portfolio as gated products and IATA ONE Record went live in July 2026 through the IBS Software ONE Record server rather than as anything Lufthansa Cargo publishes itself.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/lufthansa-cargo/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/lufthansa-cargo/refs/heads/main/apis.yml)

## Tags

- Logistics
- Supply Chain
- Germany
- Air Cargo
- Freight
- Track and Trace
- Standards
- Aviation

## Timestamps

- **Created:** 2026-07-30
- **Modified:** 2026-07-30

## APIs

### Lufthansa Cargo Shipment Tracking API

Retrieves the current status of an air freight shipment by IATA Air Waybill, keyed on a 3-digit AWB prefix (020 = Lufthansa Cargo) plus an 8-digit AWB number. Returns the milestone plan, booking, flight movement details, e-freight details and the shipment status event history. OpenAPI 3.0.0, version "1.0 - 2022.01.03", secured with an apikey header.

- **Human URL:** [https://developer.lufthansa-cargo.com/apis/shipmenttrackingpublic](https://developer.lufthansa-cargo.com/apis/shipmenttrackingpublic)
- **Base URL:** `https://api.lufthansa-cargo.com`

#### Tags

- Track and Trace
- Air Cargo
- Shipment Status
- Air Waybill

#### Properties

- [Open A P I](openapi/lufthansa-cargo-shipment-tracking-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Documentation](https://developer.lufthansa-cargo.com/apis/shipmenttrackingpublic)
- [Authentication](https://developer.lufthansa-cargo.com/how-to-connect)

### Lufthansa Cargo Shipment Tracking Subscribe API

Subscription API that pushes shipment milestone updates to a caller-supplied HTTPS callback URL. Create, read, update, delete and list subscriptions for a given Air Waybill and status filter; the OpenAPI declares a shipmentStatusUpdate callback against the request-body callback field, with 401 for a disabled callback host and 403 for a callback host not allowed. Status filter values are the IATA cargo status codes RCS, MAN, DEP, ARR, RCF, NFD, DLV, DDL, RCT, TFD, DIS, TOA and PRE. OpenAPI 3.0.0, version "1.0 - 2022.01.03".

- **Human URL:** [https://developer.lufthansa-cargo.com/apis/shipmenttrackingsubscribepublic](https://developer.lufthansa-cargo.com/apis/shipmenttrackingsubscribepublic)
- **Base URL:** `https://api.lufthansa-cargo.com`

#### Tags

- Webhooks
- Track and Trace
- Air Cargo
- Events
- Air Waybill

#### Properties

- [Open A P I](openapi/lufthansa-cargo-shipment-tracking-subscribe-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Documentation](https://developer.lufthansa-cargo.com/apis/shipmenttrackingsubscribepublic)
- [Authentication](https://developer.lufthansa-cargo.com/how-to-connect)

### Lufthansa Cargo Routing Offer API

Returns possible direct and connecting route offers between an origin and a destination 3-letter IATA airport code for a given departure date and Lufthansa Cargo product code, based on Latest Acceptance Time. Product codes are the carrier's own enumeration (FAN, FCO, FCP, FDG, FTF, FUN, FWN, YCO, YCP, YDG, YNB, YNZ, YTF, YUN, ZXB, ZXF, ZXO), with a filter for freighter and truck connections only. OpenAPI 3.0.0, version "1.1 - 2022.04.27".

- **Human URL:** [https://developer.lufthansa-cargo.com/apis/routingpublic](https://developer.lufthansa-cargo.com/apis/routingpublic)
- **Base URL:** `https://api.lufthansa-cargo.com`

#### Tags

- Routing
- Schedules
- Air Cargo
- Capacity

#### Properties

- [Open A P I](openapi/lufthansa-cargo-routing-offer-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Documentation](https://developer.lufthansa-cargo.com/apis/routingpublic)
- [Authentication](https://developer.lufthansa-cargo.com/how-to-connect)

### Lufthansa Cargo Station Information API

Reference data for Lufthansa Cargo stations worldwide, keyed on 3-letter IATA station codes. Lists all station codes, returns detail for a single station, and accepts a POST batch of codes. Detail covers addresses, contacts, ground handling agents, daily opening hours, and export and import operational capability including dangerous-goods classes, temperature-controlled and frozen storage ranges, dry ice, tarmac protection and container types. OpenAPI 3.0.0, version 2.0.

- **Human URL:** [https://developer.lufthansa-cargo.com/apis/stationinformationpublic](https://developer.lufthansa-cargo.com/apis/stationinformationpublic)
- **Base URL:** `https://api.lufthansa-cargo.com`

#### Tags

- Reference Data
- Stations
- Air Cargo
- Handling

#### Properties

- [Open A P I](openapi/lufthansa-cargo-station-information-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Documentation](https://developer.lufthansa-cargo.com/apis/stationinformationpublic)
- [Authentication](https://developer.lufthansa-cargo.com/how-to-connect)

### Lufthansa Cargo smartBooking API

Prior-agreement API. Lufthansa Cargo's digital booking connect for forwarders wiring an in-house system to the carrier and for ePlatforms integrating LH Cargo offers and bookings. Documented services are Product Offer Request, Booking, Update Booking, Get Booking, Delete Booking, and proactive status updates on existing bookings via Booking Push. The portal publishes only an OpenAPI info block for this product carrying the sentence that access is granted upon prior approval and agreement; no paths, servers or schemas are published, so no machine-readable contract was harvested.

- **Human URL:** [https://developer.lufthansa-cargo.com/prior-agreement-apis](https://developer.lufthansa-cargo.com/prior-agreement-apis)

#### Tags

- Booking
- Rates
- Air Cargo
- Prior Agreement

#### Properties

- [Documentation](https://developer.lufthansa-cargo.com/prior-agreement-apis)
- [Onboarding](https://developer.lufthansa-cargo.com/partneronboardingprocess)

### Lufthansa Cargo TruckPreAdvice API

Prior-agreement API. Manages advance notification of truck deliveries as an alternative to the Quick Drop-Off/Pick-Up page in the Lufthansa ePortal. Documented functions are Save (create Visit Declarations used for check-in at LH Cargo onsite terminals), Get and Update. The portal publishes only an OpenAPI info block; no paths or schemas were published to harvest.

- **Human URL:** [https://developer.lufthansa-cargo.com/prior-agreement-apis](https://developer.lufthansa-cargo.com/prior-agreement-apis)

#### Tags

- Trucking
- Terminals
- Air Cargo
- Prior Agreement

#### Properties

- [Documentation](https://developer.lufthansa-cargo.com/prior-agreement-apis)
- [Onboarding](https://developer.lufthansa-cargo.com/partneronboardingprocess)

### Lufthansa Cargo ULDStatus API

Prior-agreement API behind the smartULD add-on service. Exposes sensory data from smart Unit Load Devices - ambient temperature, battery level, geodata - plus container check status from handling for both smart and regular ULDs, aimed at Active Temp Control shipments. Documented services are get container data, create container subscriptions, list subscriptions, get a single subscription and delete a subscription. The portal publishes only an OpenAPI info block; no paths or schemas were published to harvest.

- **Human URL:** [https://developer.lufthansa-cargo.com/prior-agreement-apis](https://developer.lufthansa-cargo.com/prior-agreement-apis)

#### Tags

- ULD
- Telematics
- Cold Chain
- Air Cargo
- Prior Agreement

#### Properties

- [Documentation](https://developer.lufthansa-cargo.com/prior-agreement-apis)
- [Onboarding](https://developer.lufthansa-cargo.com/partneronboardingprocess)

### Lufthansa Cargo CargoXML API

Prior-agreement API product named CargoXML in the Lufthansa Cargo portfolio, referencing the IATA Cargo-XML message standard. The portal publishes an OpenAPI 3.0.3 info block titled "CargoXML APIs" whose entire description is the notice that Lufthansa Cargo will only give access upon prior approval and agreement. No version of the Cargo-XML standard, no message set, no endpoint and no schema is published, so nothing machine-readable was harvestable.

- **Human URL:** [https://developer.lufthansa-cargo.com/apis/cargoxml](https://developer.lufthansa-cargo.com/apis/cargoxml)

#### Tags

- EDI
- Cargo-XML
- IATA
- Messaging
- Prior Agreement

#### Properties

- [Documentation](https://developer.lufthansa-cargo.com/apis/cargoxml)
- [Onboarding](https://developer.lufthansa-cargo.com/partneronboardingprocess)

### Lufthansa Cargo CargoIMP API

Prior-agreement API product listed as CargoIMP in the portfolio, referencing the legacy IATA Cargo Interchange Message Procedures EDI message set. The portal publishes an OpenAPI 3.0.1 info block titled "CargoMessaging APIs" whose entire description is the prior-approval notice. No message set, edition, endpoint or schema is published.

- **Human URL:** [https://developer.lufthansa-cargo.com/apis/cargoimp](https://developer.lufthansa-cargo.com/apis/cargoimp)

#### Tags

- EDI
- Cargo-IMP
- IATA
- Messaging
- Prior Agreement

#### Properties

- [Documentation](https://developer.lufthansa-cargo.com/apis/cargoimp)
- [Onboarding](https://developer.lufthansa-cargo.com/partneronboardingprocess)

### Lufthansa Cargo AirMail API

Prior-agreement API product covering airmail carriage for postal operators. The portal publishes an OpenAPI 3.0.3 info block titled "AirMail APIs" whose entire description is the prior-approval notice. No operations, endpoints or schemas are published, and no postal standard (UPU, CARDIT/RESDIT) is referenced anywhere on the portal.

- **Human URL:** [https://developer.lufthansa-cargo.com/apis/airmail](https://developer.lufthansa-cargo.com/apis/airmail)

#### Tags

- Airmail
- Postal
- Air Cargo
- Prior Agreement

#### Properties

- [Documentation](https://developer.lufthansa-cargo.com/apis/airmail)
- [Onboarding](https://developer.lufthansa-cargo.com/partneronboardingprocess)

## Common Properties

- [Website](https://www.lufthansa-cargo.com/)
- [Developer Portal](https://developer.lufthansa-cargo.com/)
- [Documentation](https://developer.lufthansa-cargo.com/how-to-connect)
- [Onboarding](https://developer.lufthansa-cargo.com/partneronboardingprocess)
- [Terms Of Service](https://developer.lufthansa-cargo.com/terms)
- [Support](https://developer.lufthansa-cargo.com/contact)
- [Email](mailto:apisupport.lcag@dlh.de)
- [Change Log](https://developer.lufthansa-cargo.com/news)
- [Sign Up](https://developer.lufthansa-cargo.com/login)
- [Sandbox](https://developer-test.lufthansa-cargo.com)
- [GitHub Organization](https://github.com/LufthansaCargo)
- [LinkedIn](https://www.linkedin.com/company/lufthansa-cargo)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
