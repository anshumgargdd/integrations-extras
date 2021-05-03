# Sqreen Integration

## Overview

The Sqreen integration enables you and your team to monitor your service security activity right from Datadog.

It provides you with dashboards, security rules, log facets, and saved views.

This integration is only available to Datadog and Sqreen design partners. 

It requires the Sqreen microagent to be deployed in the web services to secure. 

![Sqreen Insights in Datadog][1]

### Security Rules

This integration contains 2 security rules: 
* Security Incident detected by Sqreen
* A user logged in from a new country

Once set up, you'll be able to review their full definition from the [Security Rules list](https://app.datadoghq.com/security/configuration/rules?sort=rule&query=source%3Asqreen).

## Setup

### Configure the Sqreen -> Datadog data pipeline

Sqreen streams your services security activity to Datadog as logs.

Here's the steps to follow to set it up:

1. Go to the [Sqreen Dashboard > Organization settings > Integrations](https://my.sqreen.com/profile/organization/integrations).
2. Add a new "Push API" integration and select `datadog` as the destination.
3. Choose the corresponding intake server URL. For Datadog US: `http-intake.logs.datadoghq.com`. For Datadog EU: `http-intake.logs.datadoghq.eu`.
4. In the `dd_api_key` field, provide a [Datadog API key][2] used to stream the Sqreen data as logs.

After a few seconds, the first logs with `source:sqreen` should be flowing in. 

The assets bundled in this integration will be deployed into your Datadog account.

### Troubleshooting

For support, reach out to [support@sqreen.com](mailto:support@sqreen.com).

## Payload Reference Documentation

The log format is fully documented on the [Sqreen documentation](https://docs.sqreen.com/integrations/datadog-integration/).

[1]: https://raw.githubusercontent.com/DataDog/integrations-extras/master/sqreen/images/sqreen_dashboard.png
[2]: https://app.datadoghq.com/account/settings#api 
[3]: https://docs.sqreen.com/integrations/datadog-integration/

## Data Collected

### Logs

This integration collects Sqreen events as logs.

### Metrics

No metrics is collected for this integrations

### Service Checks

No service checks are included in this integrations

### Events

No events are collected in this integration