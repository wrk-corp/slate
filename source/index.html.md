---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - ruby
  - javascript

# toc_footers:
#   - <a href='#'>Sign Up for a Developer Key</a>
#   - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true

code_clipboard: true
---

# Introduction

Welcome to the Wrk API. You can use our API to access a list of Jobs for an Organization and to view the details of a specific Job. These API endpoints are currently not authenticated but are rate limited.

# Jobs

## Get All Jobs

```shell
curl -H "Content-Type: application/json" \
  https://hire.wrkhq.com/api/v1/public/organizations/helium/jobs
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all Jobs for an Organization.

### HTTP Request

`GET https://wrkhq.com/api/v1/public/jobs/`

<aside class="success">
Jobs are awesome and super useful
</aside>

## Get a Specific Job

```shell
curl -H "Content-Type: application/json" https://hire.wrkhq.com/api/v1/public/organizations/helium/jobs/18012
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific Job.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/Jobs/<ID>`

### URL Parameters

| Parameter | Description                   |
| --------- | ----------------------------- |
| ID        | The ID of the Job to retrieve |

### URL Parameters

| Parameter | Description                 |
| --------- | --------------------------- |
| ID        | The ID of the Job to delete |
