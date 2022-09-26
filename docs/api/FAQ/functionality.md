---
title: Dune API Functionality
description: Answers to questions about how the Dune API works.
---
# FAQ: Functionality

## General

### How many Requests Per Second can I make?

The API is temporarily rate-limited to ~12 requests per minute for overload protection. Please reach out if you require higher throughput!

### Are there specified SLAs?

SLAs will be available in the future on Enterprise pricing plans.

## Executing Queries

### How do I find a query id?

When navigating to a query, it’s the first number after “/queries/” in the URL.

![query-id-example](../images/query-id-example.jpg)

### Does the API support Query Parameters?

The API does support Query Parameters!

For Dune Queries that include Parameters, you can pass parameter data as part of the [Execute Query ID endpoint](../../api/api-reference/execute-query-id.md)!

Learn more about [building Dune Queries with Parameters here](../../features/parameters.md).

And learn how to pass parameter data using [cURL here](../../api/api-reference/execute-query-id.md#curl-with-parameters) and with [Python here](../../api/quick-start/api-py.md).

### What are the performance and overall differences between the Dune API and the Dune web app? What are the differences in what I can query?

There are no major performance differences or differences in what can be accessed between the two.

The Dune API simply gives you programmatic access to the capabilities and data sets that can already be accessed from the Dune web app.

### What is the execution timeout limit and can I request a longer limit?

Initially, the query execution timeout limit will match the Dune web app - 30 minutes.

Later, we plan to allow overrides of this, but we’d need to adjust our query execution billing to reflect this as well.

### When do you plan on supporting the use of sending raw SQL directly from the server?

We don’t have a committed timeline yet, but this is tentatively planned to be a feature only available on Enterprise plans.

### Can I query using both Dune v2 Engine and the original v1 databases?

Currently yes, but we’re slowly deprecating usage and support of the old engine, so we recommend using the new Dune v2 Engine as much as possible.