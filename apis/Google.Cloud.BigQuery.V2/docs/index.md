{{title}}

{{description}}
It wraps the `Google.Apis.Bigquery.v2` generated library, providing a higher-level API to make it easier to use.

{{version}}

{{installation}}

{{auth}}

# Getting started

Common operations are exposed via the
[BigQueryClient](obj/api/Google.Cloud.BigQuery.V2.BigQueryClient.yml)
class, and additional wrapper classes are present to make operations
with datasets, tables and query results simpler.

# Client life-cycle management

In many cases you don't need to worry about disposing of
`BigQueryClient` objects, and can create them reasonably freely -
but be aware that this *can* causes issues with memory and network
connection usage. We advise you to reuse a single client object if
possible; if your architecture requires you to frequently create new
client objects, please dispose of them to help with timely resource
clean-up. See [the resource clean-up guide](../guides/cleanup.html#rest-based-apis) for more
details.

# Sample code

## Querying

{{sample:BigQueryClient.QueryOverview}}

## Parameterized queries

Queries can be provided with parameters, either using names (the
default):

{{sample:BigQueryClient.ParameterizedQueryNamedParameters}}

Or using positional parameters:

{{sample:BigQueryClient.ParameterizedQueryPositionalParameters}}

## Using legacy SQL

By default, [BigQueryClient](obj/api/Google.Cloud.BigQuery.V2.BigQueryClient.yml)
uses [Standard SQL](https://cloud.google.com/bigquery/sql-reference/). To
use [Legacy SQL](https://cloud.google.com/bigquery/query-reference),
simply set `UseLegacySql` to true in the query options, and make
sure that you use the legacy format for the table name, as shown
below.

{{sample:BigQueryClient.LegacySql}}

## Data insertion

{{sample:BigQueryClient.InsertOverview}}

## Creating a table partitioned by time

{{sample:BigQueryClient.CreatePartitionedTable}}

## Querying an external data source

As [described in the
documentation](https://cloud.google.com/bigquery/external-data-sources),
BigQuery can query some external data sources. The sample code below
demonstrates querying a CSV file stored in Google Cloud Storage.

{{sample:BigQueryClient.ExternalCsv}}
