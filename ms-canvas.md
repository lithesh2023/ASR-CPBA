
| Name | Payment Service |  |
|--|--|--|
| **Description** |Used for payment services for parking slot booking.|
| **Capabilities** |  |
| | Payment Services | 
| **Service API** |  | 
| **Commands** |**Queries**| **Events Published** |
|Synchronous: |||
| getPayment()|||
|postPayment() |||
 |Asynchronous|||
 |NA|||
 |**Non Functional Requirements**|||
 ||- 99.95% Availability||
 ||- 100 Payments/second||
 |**Observability**|||
 |Key Metrics|||
 ||NA||
 |Health check endpoint|||
 ||/health||
 |**Implementation**|||
 |Domain Model|||
 ||NA||
  |**Dependencies**|||
  |Invokes|Subscribes to||
  |Booking Service|NA||
  |- payment()|||

