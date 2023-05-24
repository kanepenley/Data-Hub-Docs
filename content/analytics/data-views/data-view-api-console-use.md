---
uid: data-view-api-console-use
---

# Data views and the API Console

While creating or editing a data view, you can launch it within the API Console by choosing the **View in API Console** button. Launching the data view in the API console allows you to refine the data view endpoint query before specifying its URI in your application code or Microsoft Power BI.

## Data view API console parameters

When viewing a data view from the API Console, you can edit the default parameters that you configured during initial creation of the data view. Additionally, you can provide continuation tokens (in support of data pagination), caching data, or choosing different support response formats.

| Field | Description |
|--|--|
| startIndex | The inclusive start boundary of the data view data. |
| endIndex | The inclusive end boundary of the data view data |
| count | The number of data points included in the request. |
| interval | The requested interval between index values. |
| continuationToken | The field for specifying a continuation token when a request returns. For more information on this field and the **Load from Response** button, see [Continuation token](#continuation-token). |
| cache | The field for setting cache behavior. Values include: <ul><li><code>Preserve</code> (default): Uses cached information, if available.</li><li><code>Refresh</code>: Forces the resource to re-resolve.</li></ul> |
| form | The file format that request responses are returned. For information on the response forms available, see [Response forms](#response-forms). |

## Response forms

When requesting data views from the API Console, the REST API is capable of returning requests in a variety of file formats. Select a form from the dropdown. Supported response forms include:

| Form | Description |
|--|--|
| default (JSON) | Object-style JSON. |
| table (Table) | Table-style JSON. |
| tableh (Table with headers) | Table-style JSON with header row. |
| csv (Comma separated values) | Comma-separated values. |
| csvh (Comma separated values with headers) | Comma-separated values with header row. |
| parquet | Parquet format. For more information on the Parquet format, see <xref:data-views-parquet-format>. |

## Copy or download response body

While making requests using the API console, you can copy or download the response body by choosing the appropriate icon.

- Choose **Copy** ![copy](../../_icons/default/content-copy.svg) to copy the response body to your clipboard.
- Choose **Download** ![download](../../_icons/default/download.svg) to download the response body.

When working with Data Views, response bodies are downloaded in the file format specified in the **form** dropdown.