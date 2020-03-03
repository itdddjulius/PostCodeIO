<h1 align="center">Backend Engineer Coding Test</h1>
<p>
Thank you for applying to work with us. We ask all candidates to complete a coding test so we
can fairly evaluate their technical capabilities.
Please treat this test as a real feature request and treat the work as if it were being used by real
users.
We ask you to complete this test within a week. If you need more time, let us know and we can
give you an extension. You will not be penalised for this.
There are no gotchas or trick questions in this test, we just want you to complete it based on the
instructions provided. We don’t expect you to go beyond the instructions provided.
Feel free to get in touch and ask as many questions as you’d like.
</p>


<h1 align="center">Postcode Checker</h1>
<p>
Your customer would like a simple web application to work out if a given postcode is within their
service area.
Create a form where the input is a UK postcode. When submitting the form, the response should
tell the user if the postcode is whitelisted or not. There’s no need to add any styling.
Requirements
We are using the Postcodes.io REST API as our source for data. The service area is described by
the following rules:
<ul>
<li>
1. <p>Postcodes are grouped into larger blocks called LSOAs. This is returned from the API
when we query a postcode. We want to whitelist any postcode in an LSOA starting
"Southwark" or "Lambeth". Example postcodes for these LSOAs are SE1 7QD and SE1
  7QA respectively.
  </p>
</li>
<li>
2. <p>Some postcodes are unknown by the API or may be served despite being outside of the
whitelisted LSOAs. We need to be able to whitelist these anyway, even though the API
does not recognise them. SH24 1AA and SH24 1AB are both examples of unknown
postcodes that we want to serve.
  </p>
</li>
<li>
3. <p>Any postcode not in the LSOA whitelist or the Postcode whitelist is not servable.
Please note that no guarantees about the format of the input can be given, and the whitelists will
need to be changed from time to time.
Documentation for the Postcodes.io API can be found at http://postcodes.io
  </p>
</li>
</p>

<h1 align="center">
  <img src="https://img.ideal-postcodes.co.uk/Postcodes.io%20Logo@3x.png" alt="Postcodes.io">
</h1>

> UK postcode & geolocation API, serving up open data

[![CircleCI](https://circleci.com/gh/ideal-postcodes/postcodes.io/tree/master.svg?style=svg)](https://circleci.com/gh/ideal-postcodes/postcodes.io/tree/master)
[![codecov](https://codecov.io/gh/ideal-postcodes/postcodes.io/branch/master/graph/badge.svg)](https://codecov.io/gh/ideal-postcodes/postcodes.io)
[![Dependency Status](https://david-dm.org/ideal-postcodes/postcodes.io.svg)](https://david-dm.org/ideal-postcodes/postcodes.io)

Query for UK postcodes and geolocations over HTTP.

Postcodes.io regularly ingests and serves the [ONS Postcode Directory](https://geoportal.statistics.gov.uk/datasets?q=ONSPD&sort=name&t=ons%20postcode%20directory) and [Ordnance Survey Open Names](https://www.ordnancesurvey.co.uk/business-and-government/products/os-open-names.html) datasets.

## Features

- Postcode lookup, resolve administrative and location data for postcodes and outward codes
- Postcode search & autocomplete
- Reverse geocode postcodes
- Nearest postcode search
- Terminated postcode search
- Outward code lookup
- Bulk postcode lookup and reverse geocoding

## Usage

- [Public API](https://postcodes.io)
- [API Documentation](https://postcodes.io/docs)
- [3rd Party API Clients](https://postcodes.io/about)
- [Public API Service Status](https://status.ideal-postcodes.co.uk)
- [Self Hosting](https://postcodes.io/docs#Install-notes)
- [Self Hosting: Docker containers](https://postcodes.io/docs#docker-install)
  - [Docker Hub Container Image: Postcodes.io Application](https://hub.docker.com/r/idealpostcodes/postcodes.io)
  - [Docker Hub Container Image: Postcodes.io Database](https://hub.docker.com/r/idealpostcodes/postcodes.io.db)
- [Self Hosting: Node.js and Postgresql](https://postcodes.io/docs#install-requirements)
- [Self Hosting: Database only - Download and import the raw dataset to Postgresql](https://postcodes.io/docs#import-from-pgdump)
- [Explore](https://postcodes.io/explore)
- [Chat](https://chat.ideal-postcodes.co.uk)

## Quick Start

Start querying UK postcode data immediately on your local machine with Docker

```bash
docker-compose up
```

<p align="center">
  <img src="https://img.ideal-postcodes.co.uk/postcodesio-docker-compose-demo.gif" alt="Docker Compose Demo">
</p>

## Testing

```bash
# Run entire test suite
make test

# Launch test application container and services, and run tests from container
make test-up
make test-shell
$api-container> npm test
```

## Author

<a href="www.raiiar.com"><b style="color: GREEN;">Another solution created by - Julius Olatokunbo</b></a>
