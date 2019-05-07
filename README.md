# ![LOGO](logo.png) Adyen MarketPay Notification Configuration Service MSP Connector

## Description

A generated MSP connector for the Adyen MarketPay Notification Configuration Service API (version 1).

Generated from: https://api.apis.guru/v2/specs/adyen.com/NotificationConfigurationService/1/openapi.json<br/>
Generated at: 2019-05-07T11:15:12+03:00

## API Description

The MarketPay Notification Configuration API provides endpoints for configuration a subscription to a marketplace's MarketPay-related notifications. Notifications are sent upon the occurrence of certain events (such as a KYC check completion or a payout completion), and the subscription to these notifications dictates to where they are sent.

For further information on MarketPay notifications, please visit the [MarketPay documentation](https://docs.adyen.com/developers/marketpay/marketpay-overview).
## Authentication
To connect to the MarketPay API, you must use basic authentication credentials of your web service user. If you don't have one, please contact the [Adyen Support Team](https://support.adyen.com/hc/en-us/requests/new). Then use its credentials to authenticate your request, for example:

```
curl
-U "ws@Company.YourCompany":"YourWsPassword" \
-H "Content-Type: application/json" \
...
```
Note that when going live, you need to generate new web service user credentials to access the [live endpoints](https://docs.adyen.com/developers/api-reference/live-endpoints).

## Versioning
MarketPay API supports versioning of its endpoints through a version suffix in the endpoint URL. This suffix has the following format: "vXX", where XX is the version number.

For example:
```
https://cal-test.adyen.com/cal/services/Notification/v1/createNotificationConfiguration
```

## Authorization

This API does not require authorization.

## Actions

### Configure a new subscription to notifications.

> This endpoint is used to create a subscription to MarketPay event notifications. After the subscription is created, the events specified in the configuration will be sent to the URL specified in the configuration. Subscriptions must be configured on a per-event basis (as opposed to, for example, a per-account holder basis), so all event notifications of a marketplace and of a given type will be sent to the same endpoint(s). A marketplace may have multiple endpoints if desired; an event notification may be sent to as many or as few different endpoints as configured.

### Delete an existing notification subscription configuration.

> This endpoint is used to delete an existing notification subscription configuration. After the subscription is deleted, no further event notifications will be sent to the URL that was in the subscription.

### Retrieve an existing notification subscription configuration.

> This endpoint is used to retrieve the details of the configuration of a notification subscription.

### Retrive a list of existing notification subscription configurations.

> This endpoint is used to retrieve the details of the configurations of all of the notification subscriptions in the marketplace of the executing user.

### Test an existing notification configuration.

> This endpoint is used to test an existing notification subscription configuration. For each event type specified, a test notification will be generated and sent to the URL configured in the subscription specified.

### Update an existing notification subscription configuration.

> This endpoint is used to update an existing notification subscription configuration. If updating the event types, all event types desired must be provided, otherwise the previous event type configuration will be overwritten.

## License

flowground :- Telekom iPaaS / adyen-com-notification-configuration-service-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
