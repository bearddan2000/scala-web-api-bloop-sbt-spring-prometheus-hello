# scala-web-api-bloop-sbt-spring-prometheus-hello

## Description
Another way to serve web content.
Uses prometheus to count http calls.

To see a graph of visitors:
- Nav to http://localhost:81
- Classic UI
  - Click Graph tab
    - Search: 'scrape_series_added'
      or 'scrape_duration_second'
      or 'http_request_duration_ms_bucket'
    - Duration 1m

For health check:
- Nav to http://localhost:81
- Targetes

Compiled and ran from build server `bloop`.

# Build note
Dependencies must be compatable with jdk8 or less.

## Tech stack
- bloop
- scala
- bloop-sbt
- prometheus

## Docker stack
- eed3si9n/sbt
- prom/prometheus:latest

## To run
`sudo ./install.sh -u`
- Available http://localhost
- App metrics http://localhost/metrics
- Prometheus console http://localhost:81

## To stop
`sudo ./install.sh -d`

## For help
`sudo ./install.sh -h`

## Credit
- https://github.com/monodot/spring-boot-with-metrics/blob/main/pom.xml
