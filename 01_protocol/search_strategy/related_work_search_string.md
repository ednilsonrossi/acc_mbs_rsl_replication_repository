# Related Work Search

For this systematic literature review, an initial search was conducted to identify existing secondary studies, including systematic literature reviews, systematic mapping studies, and other related types of studies. To perform this search, the following search string was used.

```
(
  "microservice" OR "microservices" OR "microservice-based"
  OR "service-oriented" OR SOA
  OR "distributed systems" OR "cloud-based"
  OR "event-driven" OR "message-based"
)
AND
(
  "architectural conformance" OR "architecture conformance"
  OR "architectural compliance" OR "architecture compliance"
  OR "architectural consistency" OR "architecture consistency"
  OR "conformance checking" OR "compliance checking"
  OR "design rule checking" OR "architecture rule enforcement"
  OR "architecture validation" OR "architecture verification"
)
AND
(
  "systematic literature review" OR "systematic review"
  OR "systematic mapping study" OR "mapping study"
  OR "secondary study" OR "survey"
)
```

## Short String

```
(microservice OR microservices OR SOA)
AND
("architecture conformance" OR "architectural consistency" OR "conformance checking")
AND
("systematic review" OR "literature review" OR "mapping study" OR survey)
```

## Using wildcards

```
(
  microservice*
  OR "service-oriented" OR SOA
  OR "distributed systems" OR "cloud-based"
  OR "event-driven" OR "message-based"
)
AND
(
  "architectur* conformance" 
  OR "architectur* compliance"
  OR "architectur* consistency" 
  OR "conformance check*" OR "compliance check*"
  OR "design rule check*" OR "architectur* rule enforce*"
  OR "architectur* validation" OR "architectur* verification"
)
AND
(
  "systematic literature review" OR "systematic review"
  OR "systematic mapping study" OR "mapping study"
  OR "secondary study" OR "survey"
)
```