# ![LOGO](logo.png) G Suite Alert Center **flow**ground Connector

## Description

A generated **flow**ground connector for the G Suite Alert Center API (version v1beta1).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/alertcenter/v1beta1/swagger.json<br/>
Generated at: 2019-05-07T17:41:08+03:00

## API Description

Manages alerts on issues affecting your domain.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Lists the alerts.

*Tags:* `alerts`

#### Input Parameters
* `customerId` - _optional_ - Optional. The unique identifier of the G Suite organization account of the
customer the alerts are associated with.
Inferred from the caller identity if not provided.
* `filter` - _optional_ - Optional. A query string for filtering alert results.
For more details, see [Query
filters](/admin-sdk/alertcenter/guides/query-filters) and [Supported
query filter
fields](/admin-sdk/alertcenter/reference/filter-fields#alerts.list).
* `orderBy` - _optional_ - Optional. The sort order of the list results.
If not specified results may be returned in arbitrary order.
You can sort the results in descending order based on the creation
timestamp using `order_by="create_time desc"`.
Currently, only sorting by `create_time desc` is supported.
* `pageSize` - _optional_ - Optional. The requested page size. Server may return fewer items than
requested. If unspecified, server picks an appropriate default.
* `pageToken` - _optional_ - Optional. A token identifying a page of results the server should return.
If empty, a new iteration is started. To continue an iteration, pass in
the value from the previous ListAlertsResponse's
next_page_token field.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Marks the specified alert for deletion. An alert that has been marked for<br/>
> deletion is removed from Alert Center after 30 days.<br/>
> Marking an alert for deletion has no effect on an alert which has<br/>
> already been marked for deletion. Attempting to mark a nonexistent alert<br/>
> for deletion results in a `NOT_FOUND` error.

*Tags:* `alerts`

#### Input Parameters
* `alertId` - _required_ - Required. The identifier of the alert to delete.
* `customerId` - _optional_ - Optional. The unique identifier of the G Suite organization account of the
customer the alert is associated with.
Inferred from the caller identity if not provided.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets the specified alert. Attempting to get a nonexistent alert returns<br/>
> `NOT_FOUND` error.

*Tags:* `alerts`

#### Input Parameters
* `alertId` - _required_ - Required. The identifier of the alert to retrieve.
* `customerId` - _optional_ - Optional. The unique identifier of the G Suite organization account of the
customer the alert is associated with.
Inferred from the caller identity if not provided.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists all the feedback for an alert. Attempting to list feedbacks for<br/>
> a non-existent alert returns `NOT_FOUND` error.

*Tags:* `alerts`

#### Input Parameters
* `alertId` - _required_ - Required. The alert identifier.
The "-" wildcard could be used to represent all alerts.
* `customerId` - _optional_ - Optional. The unique identifier of the G Suite organization account of the
customer the alert feedback are associated with.
Inferred from the caller identity if not provided.
* `filter` - _optional_ - Optional. A query string for filtering alert feedback results.
For more details, see [Query
filters](/admin-sdk/alertcenter/guides/query-filters) and [Supported
query filter
fields](/admin-sdk/alertcenter/reference/filter-fields#alerts.feedback.list).
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates new feedback for an alert. Attempting to create a feedback for<br/>
> a non-existent alert returns `NOT_FOUND` error.

*Tags:* `alerts`

#### Input Parameters
* `alertId` - _required_ - Required. The identifier of the alert this feedback belongs to.
* `customerId` - _optional_ - Optional. The unique identifier of the G Suite organization account of the
customer the alert is associated with.
Inferred from the caller identity if not provided.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Restores, or "undeletes", an alert that was marked for deletion within the<br/>
> past 30 days. Attempting to undelete an alert which was marked for deletion<br/>
> over 30 days ago (which has been removed from the Alert Center database) or<br/>
> a nonexistent alert returns a `NOT_FOUND` error. Attempting to<br/>
> undelete an alert which has not been marked for deletion has no effect.

*Tags:* `alerts`

#### Input Parameters
* `alertId` - _required_ - Required. The identifier of the alert to undelete.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns customer-level settings.

*Tags:* `v1beta1`

#### Input Parameters
* `customerId` - _optional_ - Optional. The unique identifier of the G Suite organization account of the
customer the alert settings are associated with.
Inferred from the caller identity if not provided.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Updates the customer-level settings.

*Tags:* `v1beta1`

#### Input Parameters
* `customerId` - _optional_ - Optional. The unique identifier of the G Suite organization account of the
customer the alert settings are associated with.
Inferred from the caller identity if not provided.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-alertcenter-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
