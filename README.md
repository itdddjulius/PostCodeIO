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

## License

MIT
