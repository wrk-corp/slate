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
{
  "items": [
    {
      "city": null,
      "country": "US",
      "created_at": "2021-01-27T21:21:23.662Z",
      "created_at_timestamp": 1611782483,
      "hash_id": "b2umyqbfkoqe",
      "id": 18012,
      "job_category_name": "Sales & Marketing",
      "job_id": 18012,
      "job_post_url": "https://jobs.wrkhq.com/helium/18012",
      "kind_pretty": "Full-time",
      "location_pretty": "US",
      "organization_name": "Helium",
      "published_at": "2021-01-27T21:27:39.709Z",
      "published_at_timestamp": 1611782859,
      "remote_restriction_city": "San Francisco, CA, USA",
      "remote_restriction_city_google_place_id": "ChIJIQBpAG2ahYAR_6128GcTUEo",
      "remote_restriction_country_list": ["US", "CA"],
      "remote_restriction_country_residency_is_required": true,
      "remote_restriction_overlap_hours": 6,
      "remote_restriction_overlap_hours_is_required": true,
      "remote_restriction_timezone_utc_offset_seconds": null,
      "remoteness_pretty": "Remote friendly",
      "state_region": null,
      "title": "Business Development Manager"
    }
  ],
  "meta": {
    "count": 1,
    "is_first": true,
    "is_last": true,
    "organization_name": "Helium",
    "page": 1,
    "total": 1
  }
}
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
  "city": null,
  "closed_at": null,
  "country": "US",
  "created_at": "2021-01-27T21:21:23.662Z",
  "created_at_timestamp": 1611782483,
  "department": null,
  "description": "Business Development Manager (BDM)\n\n**Reports to:**\nHead of Sales\n\nHelium's mission is to leverage the power of wireless technology and blockchain to build The People\u2019s Network\u2014the world\u2019s first peer-to-peer wireless network that empowers anyone to become a network host for a new class of devices and applications that are impossible today.\nThe Helium network is now in over 2000+ cities, with coverage comparable to cellular in 30+ cities in the USA. We are looking for business development representatives (BDRs) to drive network usage with businesses of all sizes. The job requires the ultimate drive. The goal is simple: do everything you can to get meetings with potential users of the network.\n\n**Job Overview:**\nBDMs at Helium are responsible for a hybrid of outbound pipeline generation and supporting the execution of Memorandums of Understanding (MoUs) with prospects. For the outbound pipeline generation component of the role, BDMs utilize software tools such as Salesforce, Linkedin, and Outreach.io to manage inbound and outbound engagement with prospective Helium partners, taking calls and meetings as needed to qualify and source opportunities for themselves. Besides working the opportunities they source, BDMs at Helium can rely on additional pre-qualified appointments sourced by our BDR/SDR team. Are you ready to get your hustle on?\nIf you are the fit for such an effort, we want to hear from you!\nInterested? Email jobs@helium.com\n\n**Responsibilities and Duties:**\n* Prioritize and maintain the deal pipeline while owning the sales cycle from start to finish - from outreach to discovery to demo to negotiation to close.\n* Approach all deals with a customer-focused mentality. Develop relationships and uncover the needs of stakeholders to find value.\n* Manage outbound automation sequences in Outreach.io.\n* Research accounts, identify essential players, produce interest and develop meaningful relationships with potential customers across multiple verticals.\n* Craft and prioritize high-value accounts in the pipeline for strategic follow-up.\n* Give demos, conduct discovery calls and develop relationships.\n* Have immaculate Salesforce hygiene to ensure efficient lead management and record-keeping while maintaining data integrity.\n* Provide feedback to our product team to ensure continuous product innovation.\n* Be a Subject Matter Expert in Helium, LoraWAN, and IoT network connectivity in general.\n\n**We\u2019re looking for someone who has:**\n* Documented success in a team environment working with customers is critical.\n* Excellent verbal, phone and written communication skills are essential.\n* Self-directed, a quick study, and an enthusiastic team player.\n* Strong organizational skills with the ability to manage time and resources effectively are useful.\n* Self-discipline is crucial for success.\n* Listen, digest, translate to value is the key to success.\n* Intellectual curiosity that is unafraid to ask questions or collaborate with cross-functional teams.\n* Passion for professional development (open to being coached/mentored).\n\n**Bonus Points For:**\n* One year of software sales or customer service experience preferred.\n* Experience using Salesforce.\n* Experience using Outreach, Salesloft, RingDNA, or other sequencing automation tools.\n* A college degree.\n\n**Benefits:**\n* Base salary and commission\n* 100% company-paid health insurance premiums (medical, dental, and vision) for you and your dependents\n* Paid vacation and company holidays\n* Vacation stipend\n* Monthly gym stipend\n* Annual hardware stipend\n* Annual bike stipend\n* Pre-tax commuter benefits\n* Health FSA\n* 401K plan\n* You will be hustling with industry legends like Shawn Fanning, Emily Murray, and Frank Mong\n\n**About Helium:**\nHelium was founded in 2013 by Napster Founder Shawn Fanning, Amir Haleem, and Sean Carey, with a mission to make it easier to build connected devices. Helium has raised equity funding from some of the most prominent Venture Capital (VC) firms globally, including USV, Multicoin Capital, GV (formerly Google Ventures), Khosla Ventures, FirstMark Capital, Marc Benioff, MunichRe, and others.\n\n",
  "hash_id": "b2umyqbfkoqe",
  "id": 18012,
  "job_application_description_url": "https://jobs.wrkhq.com/helium/18012",
  "job_category_name": "Sales & Marketing",
  "job_id": 18012,
  "job_post_url": "https://jobs.wrkhq.com/helium/18012",
  "kind": "full_time",
  "kind_pretty": "Full-time",
  "location_pretty": "US",
  "organization_name": "Helium",
  "published_at": "2021-01-27T21:27:39.709Z",
  "published_at_pretty": "Jan 27th, 2021",
  "published_at_timestamp": 1611782859,
  "questions": [],
  "remote_restriction_city": "San Francisco, CA, USA",
  "remote_restriction_city_google_place_id": "ChIJIQBpAG2ahYAR_6128GcTUEo",
  "remote_restriction_country_list": ["US", "CA"],
  "remote_restriction_country_residency_is_required": true,
  "remote_restriction_overlap_hours": 6,
  "remote_restriction_overlap_hours_is_required": true,
  "remote_restriction_timezone_utc_offset_seconds": null,
  "remoteness_pretty": "Remote friendly",
  "settings": {
    "cover_letter": "optional",
    "email": "required",
    "first_name": "required",
    "last_name": "required",
    "linkedin_url": "required",
    "location": "required",
    "phone": "required",
    "resume": "required",
    "social_share_image_type": "default",
    "website_url": "optional"
  },
  "state_region": null,
  "title": "Business Development Manager"
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
