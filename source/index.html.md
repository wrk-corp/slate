---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  # - ruby
  # - javascript

# toc_footers:
#   - <a href='#'>Sign Up for a Developer Key</a>
#   - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

# includes:
#   - errors

search: true

code_clipboard: true
---

# Introduction

Welcome to the Wrk API. You can use our API to access a list of Jobs for an Organization and to view the details of a specific Job. These API endpoints are currently not authenticated but are rate limited.

# Jobs

## Get All Jobs

```shell
curl -H "Content-Type: application/json" \
  https://hire.wrkhq.com/api/v1/public/organizations/aperturelabs/jobs
```

> The above command returns JSON structured like this:

```json
{
  "items": [
    {
      "city": "Charlotte",
      "country": "US",
      "created_at": "2020-09-13T14:31:31.364Z",
      "created_at_timestamp": 1600007491,
      "hash_id": "wUShs3ITY0br",
      "id": 15394,
      "job_category_name": "Design & User Experience",
      "job_id": 15394,
      "job_post_url": "https://jobs.wrkhq.com/aperturelabs/15394",
      "kind_pretty": "Full-time",
      "location_pretty": "Charlotte, NC",
      "organization_name": "Aperture Labs",
      "published_at": "2020-09-13T14:33:11.225Z",
      "published_at_timestamp": 1600007591,
      "remote_restriction_city": null,
      "remote_restriction_city_google_place_id": null,
      "remote_restriction_country_list": ["CA", "US"],
      "remote_restriction_country_residency_is_required": false,
      "remote_restriction_overlap_hours": 4,
      "remote_restriction_overlap_hours_is_required": false,
      "remote_restriction_timezone_utc_offset_seconds": null,
      "remoteness_pretty": "Remote",
      "state_region": "NC",
      "title": "Senior Web Designer"
    }
  ],
  "meta": {
    "count": 3,
    "is_first": true,
    "is_last": true,
    "organization_name": "Aperture Labs",
    "page": 1,
    "total": 1
  }
}
```

This endpoint retrieves all Jobs for an Organization.

### HTTP Request

`GET https://hire.wrkhq.com/api/v1/public/organizations/<organization_slug>/jobs`

### URL Parameters

| Parameter                | Description                                                                    |
| ------------------------ | ------------------------------------------------------------------------------ |
| <b>organization_slug</b> | The url name of the Organization, example Aperture Labs is <b>aperturelabs</b> |

<!-- <aside class="success">
Jobs are awesome and super useful
</aside> -->

## Get a Specific Job

```shell
curl -H "Content-Type: application/json" https://hire.wrkhq.com/api/v1/public/organizations/aperturelabs/jobs/15397
```

> The above command returns JSON structured like this:

```json
{
  "city": "Charlotte",
  "closed_at": null,
  "country": "US",
  "created_at": "2020-09-13T14:32:01.757Z",
  "created_at_timestamp": 1600007521,
  "department": "Design",
  "description": "Exposing new ways to evolve our design language they have downloaded gmail and seems to be working for now not a hill to die on yet usabiltiy. Great plan!\n\nWhen does this sunset? Re-inventing the wheel closer to the metal, game plan nail it down, so c-suite. We need to future-proof this we need to start advertising on social media all hands on deck but baseline the procedure and samepage your department, or bells and whistles, for strategic staircase, gain alignment. Usabiltiy obviously back of the net, yet anti-pattern so we need distributors to evangelize the new line to local markets, so circle back around for time to open the kimono. \n\nTo be inspired is to become creative, innovative and energized we want this philosophy to trickle down to all our stakeholders.",
  "hash_id": "FOHTgVyktkFK",
  "id": 15397,
  "job_application_description_url": "https://jobs.wrkhq.com/aperturelabs/15397",
  "job_category_name": "Design & User Experience",
  "job_id": 15397,
  "job_post_url": "https://jobs.wrkhq.com/aperturelabs/15397",
  "kind": "full_time",
  "kind_pretty": "Full-time",
  "location_pretty": "Charlotte, NC",
  "organization_name": "Aperture Labs",
  "published_at": "2020-09-13T14:32:54.747Z",
  "published_at_pretty": "Sep 13th, 2020",
  "published_at_timestamp": 1600007574,
  "questions": [],
  "remote_restriction_city": null,
  "remote_restriction_city_google_place_id": null,
  "remote_restriction_country_list": [],
  "remote_restriction_country_residency_is_required": false,
  "remote_restriction_overlap_hours": null,
  "remote_restriction_overlap_hours_is_required": false,
  "remote_restriction_timezone_utc_offset_seconds": null,
  "remoteness_pretty": "No remote",
  "settings": {
    "cover_letter": "required",
    "email": "required",
    "first_name": "required",
    "last_name": "required",
    "linkedin_url": "optional",
    "location": "optional",
    "phone": "optional",
    "resume": "optional",
    "social_share_image_type": "default",
    "website_url": "optional"
  },
  "state_region": "NC",
  "title": "Senior Product Designer"
}
```

This endpoint retrieves a specific Job.

<!-- <aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside> -->

### HTTP Request

`GET https://hire.wrkhq.com/api/v1/public/organizations/<organization_slug>/jobs/<job_id>`

### URL Parameters

| Parameter                | Description                                                                                                |
| ------------------------ | ---------------------------------------------------------------------------------------------------------- |
| <b>organization_slug</b> | The name of the Organization formatted for the job board URL, example Aperture Labs is <b>aperturelabs</b> |
| <b>job_id</b>            | The numeric ID of the Job to retrieve                                                                      |
