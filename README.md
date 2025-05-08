# cdk-aws-serverless-otlp-ch-forwarder-cwl

CDK app showcasing a serverless approach to send OpenTelemetry traces to ClickHouse using CloudWatch Logs and Lambda.

### Related Apps

- [cdk-aws-serverless-otlp-ch-forwarder-kinesis](https://github.com/garysassano/cdk-aws-serverless-otlp-ch-forwarder-kinesis) - Uses Kinesis Data Streams as OTLP transport layer instead of CloudWatch Logs.

- [cdk-aws-serverless-otlp-forwarder-cwl](https://github.com/garysassano/cdk-aws-serverless-otlp-forwarder-cwl) - Sends traces to an OTel-compatible vendor instead of ClickHouse.

- [cdk-aws-serverless-otlp-forwarder-kinesis](https://github.com/garysassano/cdk-aws-serverless-otlp-forwarder-kinesis) - Sends traces to an OTel-compatible vendor instead of ClickHouse; uses Kinesis Data Streams as OTLP transport layer instead of CloudWatch Logs.

## Prerequisites

- **_AWS:_**
  - Must have authenticated with [Default Credentials](https://docs.aws.amazon.com/cdk/v2/guide/cli.html#cli_auth) in your local environment.
  - Must have completed the [CDK bootstrapping](https://docs.aws.amazon.com/cdk/v2/guide/bootstrapping.html) for the target AWS environment.
- **_OTel Vendor:_**
  - Must have set the `CLICKHOUSE_ENDPOINT`, `CLICKHOUSE_DATABASE`, `CLICKHOUSE_USERNAME` and `CLICKHOUSE_PASSWORD` variables in your local environment.
- **_Node.js + npm:_**
  - Must be [installed](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) in your system.
- **_Docker:_**
  - Must be [installed](https://docs.docker.com/get-docker/) in your system and running at deployment.

## Installation

```sh
npx projen install
```

## Deployment

```sh
npx projen deploy
```

## Cleanup

```sh
npx projen destroy
```

## Architecture Diagram

![Architecture Diagram](./src/assets/arch-diagram.svg)

## Observability Diagram

![Observability Diagram](./src/assets/o11y-diagram.svg)
