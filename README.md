<!-- Generated from the SocQ API catalog and docs. Do not edit by hand. -->
# X (Twitter) API

[![SocQ X (Twitter) API](https://img.shields.io/badge/API-SocQ%20X%20%28Twitter%29%20API-F64C31)](https://socq.ai/apis/x?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)
[![API documentation](https://img.shields.io/badge/Docs-docs.socq.ai-111827)](https://docs.socq.ai/api-manual/x/overview)
[![License: MIT](https://img.shields.io/badge/License-MIT-2563EB)](LICENSE)
[![Check examples](https://github.com/SocQAPI/x-api/actions/workflows/check.yml/badge.svg)](https://github.com/SocQAPI/x-api/actions/workflows/check.yml)

29 endpoints for public X (Twitter) data through one SocQ API key, with runnable cURL, Node.js and Python examples and a valid request body for every endpoint.

[Browse X (Twitter) APIs](https://socq.ai/apis/x?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api) · [Get an API key](https://socq.ai/dashboard/api-key?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api) · [Documentation](https://docs.socq.ai/api-manual/x/overview) · [All SocQ examples](https://github.com/SocQAPI/socq-examples)

> **Need a ready-made app?** [Open Social Listening](https://github.com/SocQAPI/open-social-listening) is a free, open-source social listening tool you host yourself, built on SocQ search endpoints. It tracks brand, competitor and topic mentions on Reddit, X, YouTube, TikTok, news and the web.

## Endpoints

Prices are in SocQ credits; 1 credit = $0.005.

| Endpoint | publicId | What it returns | Price | Launched |
| --- | --- | --- | --- | --- |
| [Twitter Tweet Scraper API](#twitter-tweet-scraper-api) | `x/posts` | Enrich known public X post URLs with normalized text, author identity, engagement, media, entities, and conversation context. | 0.5 credits ($0.0025) per result | 2026-07-17 |
| [Twitter Profile Scraper API](#twitter-profile-scraper-api) | `x/profiles` | Turn public X usernames into normalized identity, profile, audience, and account-status records for enrichment and research workflows. | 0.6 credits ($0.003) per result | 2026-07-17 |
| [Twitter User Tweets Scraper API](#twitter-user-tweets-scraper-api) | `x/user-posts` | Collect recent public posts with replies excluded from selected X accounts for monitoring, publishing analysis, and recurring datasets. | 0.5 credits ($0.0025) per result | 2026-07-17 |
| [Twitter Search API](#twitter-search-api) | `x/search` | Build structured public X post datasets from a focused query with Latest or Top ordering for discovery, monitoring, and research. | 0.7 credits ($0.0035) per result | 2026-07-17 |
| [X Followers List API](#x-followers-list-api) | `x/followers-list` | Collect public follower accounts for one or more X usernames, with normalized identities, visible profile metrics, asynchronous tasks, and cursor-based retrieval. | 0.5 credits ($0.0025) per result | 2026-07-26 |
| [X Following List API](#x-following-list-api) | `x/following-list` | Collect public profiles followed by one or more X usernames, returning normalized identity, profile context, account signals, visible counters, and source username. | 0.5 credits ($0.0025) per result | 2026-07-26 |
| [X Post Quotes API](#x-post-quotes-api) | `x/post-quotes` | Collect public quote posts that reference known X status URLs, preserving commentary, author context, visible engagement, media, and source-post traceability. | 0.5 credits ($0.0025) per result | 2026-07-26 |
| [X Post Replies API](#x-post-replies-api) | `x/post-replies` | Collect public replies from one or more X post URLs, returning reply text, authors, visible engagement, media, and parent context with per-post limits and sorting. | 0.5 credits ($0.0025) per result | 2026-07-26 |
| [X Post Retweeters API](#x-post-retweeters-api) | `x/post-retweeters` | Resolve public X and Twitter status URLs into a task-level unique set of normalized public profiles for accounts that reposted those posts. | 0.5 credits ($0.0025) per result | 2026-07-25 |
| [X Trends API](#x-trends-api) | `x/trends` | Collect current public X trends for known numeric location identifiers, preserving source rank, query, description, location context, and collection time. | 0.5 credits ($0.0025) per result | 2026-07-26 |
| [Twitter Mentions API](#twitter-mentions-api) | `x/mentions` | Collect public tweets that mention a target user handle, with support for date range filtering and engagement metrics. | 0.7 credits ($0.0035) per result | 2026-09-11 |
| [Twitter User Search API](#twitter-user-search-api) | `x/search-users` | Search public X user accounts by keyword, returning normalized identity, bio, verified status, and audience metrics. | 0.6 credits ($0.003) per result | 2026-09-11 |
| [X Community API](#x-community-api) | `x/community` | Read public X community details from community links, including descriptions, member counts and rules, with support for looking up several communities at once. | 0.5 credits ($0.0025) per result | 2026-10-16 |
| [X Community Posts API](#x-community-posts-api) | `x/community-posts` | Get public posts from X community links, with post text, authors and engagement counts returned together and a separate result limit for each community. | 0.7 credits ($0.0035) per result | 2026-10-16 |
| [X Thread Context API](#x-thread-context-api) | `x/thread-context` | Read the context around an X post from its link, with the target post, earlier posts it replies to and public replies returned together with relationship IDs. | 0.5 credits ($0.0025) per result | 2026-10-16 |
| [X Account Location API](#x-account-location-api) | `x/user-about` | Look up where an X account is based from its username, with the country X lists, how the account connects to X, its join date and how often it changed its username. | 0.7 credits ($0.0035) per result | 2026-11-17 |
| [X Verified Followers API](#x-verified-followers-api) | `x/verified-followers` | Collect the verified accounts that follow any public X profile, with each follower's ID, username, display name, avatar, profile link and join date. | 0.7 credits ($0.0035) per result | 2026-11-17 |
| [X List Tweets API](#x-list-tweets-api) | `x/list-posts` | Read the timeline of a public X list from its URL, newest first, with each post's text, author, media and engagement and reposts flagged with their original author. | 0.7 credits ($0.0035) per result | 2026-11-17 |
| [Twitter List Members API](#twitter-list-members-api) | `x/list-members` | Export the accounts on a public X list from its URL, each with bio, location, website, verification status and follower, following and post counts. | 0.7 credits ($0.0035) per result | 2026-11-17 |
| [Twitter List Followers API](#twitter-list-followers-api) | `x/list-followers` | Collect the accounts that follow a public X list from its URL, each as a full profile with bio, location and follower, following and post counts. | 0.7 credits ($0.0035) per result | 2026-11-17 |
| [X Community Members API](#x-community-members-api) | `x/community-members` | Export the members of a public X community from its URL, each with bio, location, website, verification status and follower, following and post counts. | 0.7 credits ($0.0035) per result | 2026-11-17 |
| [X Community Moderators API](#x-community-moderators-api) | `x/community-moderators` | Get the admins and moderators who run a public X community from its URL, returned in one task as full profiles with bios and audience counts. | 0.7 credits ($0.0035) per result | 2026-11-17 |
| [X Communities Search API](#x-communities-search-api) | `x/search-communities` | Find X communities by keyword, with each community's name, member count, banner and link ready for the member, moderator and post endpoints. | 0.7 credits ($0.0035) per result | 2026-11-17 |
| [X Articles API](#x-articles-api) | `x/article` | Turn X Articles into clean text from the post URL, with the title, preview line, full body, cover image, author and likes, replies, quotes and views. | 0.7 credits ($0.0035) per result | 2026-11-17 |
| [X Spaces API](#x-spaces-api) | `x/space` | Look up X Spaces from their links, with the title, status, scheduled start, hosts, speakers, live listener count, replay count and replay availability. | 0.7 credits ($0.0035) per result | 2026-11-17 |
| [Twitter Media Scraper API](#twitter-media-scraper-api) | `x/user-media` | Collect the photos, videos and GIFs an X account has posted from its username, newest first, with the full-quality media files, captions and engagement counts. | 0.7 credits ($0.0035) per result | 2026-11-17 |
| [X User Replies API](#x-user-replies-api) | `x/user-replies` | Collect the replies an X account has written from its username, newest first, each paired with the post it answers and its author. | 0.7 credits ($0.0035) per result | 2026-11-17 |
| [Twitter Follow Checker API](#twitter-follow-checker-api) | `x/check-follow` | Check whether one X account follows up to 100 others and whether each follows it back, with a mutual-follow flag for every pair. | 0.7 credits ($0.0035) per result | 2026-11-17 |
| [Twitter Video Transcript API](#twitter-video-transcript-api) | `x/post-transcript` | Turn the speech in X videos into plain text from the post URL, with the video length returned alongside each transcript. | 0.7 credits ($0.0035) per result | 2026-11-17 |

## Quick start

1. Create an API key at [socq.ai/dashboard/api-key](https://socq.ai/dashboard/api-key?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api).
2. Export it. The examples read only `SOCQ_API_KEY`.

```bash
git clone https://github.com/SocQAPI/x-api.git
cd x-api
export SOCQ_API_KEY="your-api-key"
```

3. Run any endpoint by its publicId. Without a second argument the script sends `payloads/<slug>.json`; pass a JSON file or an inline JSON object to change the input.

```bash
# Node.js 20+
node examples/node/socq.mjs x/posts

# Python 3.8+ (standard library only)
python3 examples/python/socq.py x/posts payloads/posts.json

# cURL + jq
bash examples/curl/socq.sh x/posts '{"urls":["https://x.com/X/status/2073395918011789670"]}'
```

Each script submits the task, polls it until it succeeds or fails, follows every result page, and writes the records to `output/<slug>-<task_id>.json`. Run `npm run check` to validate the payloads and scripts offline.

Never expose `SOCQ_API_KEY` in browser code, mobile apps, public repositories, screenshots, fixtures or logs.

## How the API works

Base URL `https://api.socq.ai`. Every request sends the API key as a bearer token:

```http
Authorization: Bearer <SOCQ_API_KEY>
Content-Type: application/json
```

All endpoints are asynchronous:

```text
POST /v1/<publicId>  ->  data.task_id  ->  GET /v1/tasks/{task_id}  ->  queued | running | succeeded | failed
```

1. **Submit** the JSON body to `POST https://api.socq.ai/v1/<publicId>`. The response returns `data.task_id` immediately; it means the task was created, not that data is ready.
2. **Poll** `GET https://api.socq.ai/v1/tasks/{task_id}` until `data.status` is `succeeded` or `failed` (a failed task carries `data.error_message`).
3. **Read results.** A succeeded task returns normalized records in `data.results.items`. Use `limit` (default 50, max 500) and pass `data.results.next_cursor` as `cursor` while `data.results.has_more` is true. `fields` selects up to 50 comma-separated fields or dot paths.
4. **Raw files (optional).** `GET https://api.socq.ai/v1/tasks/{task_id}/files` lists raw JSONL exports.

```bash
curl "https://api.socq.ai/v1/tasks/$TASK_ID?limit=100" \
  -H "Authorization: Bearer $SOCQ_API_KEY"

curl "https://api.socq.ai/v1/tasks/$TASK_ID?limit=100&cursor=$NEXT_CURSOR" \
  -H "Authorization: Bearer $SOCQ_API_KEY"
```

`callback_url` (where an endpoint accepts it) makes SocQ POST to your URL when the task reaches a terminal state; keep polling as a fallback.

**Billing.** A submit may reserve credits from `results_limit` or the number of submitted inputs; when the task finishes SocQ settles the charge from the actual result count and returns unused reserved credits. `402` means insufficient credits.

**Errors.** `400` invalid body or unsupported field, `401` missing or invalid key, `402` insufficient credits, `403` IP allowlist or task owned by another account, `404` endpoint or task not found, `422` input validation failed, `429` rate or credit-window limit (respect `Retry-After`), `500` submission failed. A client-side timeout does not cancel a task: resume polling the same `task_id` instead of submitting again.

Reference: [Authentication](https://docs.socq.ai/api-manual/agent-api/authentication) · [Task status and results](https://docs.socq.ai/api-manual/agent-api/status) · [Task files](https://docs.socq.ai/api-manual/agent-api/files) · [Callbacks](https://docs.socq.ai/api-manual/agent-api/callbacks) · [Errors](https://docs.socq.ai/api-manual/agent-api/errors)

## Endpoint reference

### Twitter Tweet Scraper API

Enrich known public X post URLs with normalized text, author identity, engagement, media, entities, and conversation context.

- **Request:** `POST https://api.socq.ai/v1/x/posts`
- **publicId:** `x/posts`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-07-17
- **Example body:** [`payloads/posts.json`](payloads/posts.json)

Collect one normalized post record for each public post URL. Both `x.com` and `twitter.com` post URLs are accepted.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `urls` | array of string | Yes | Public profile or content URLs. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/posts" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "urls": [
    "https://x.com/X/status/2073395918011789670"
  ]
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/posts](https://docs.socq.ai/api-manual/x/posts) · Landing page: [socq.ai/apis/x/posts](https://socq.ai/apis/x/posts?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### Twitter Profile Scraper API

Turn public X usernames into normalized identity, profile, audience, and account-status records for enrichment and research workflows.

- **Request:** `POST https://api.socq.ai/v1/x/profiles`
- **publicId:** `x/profiles`
- **Price:** 0.6 credits ($0.003) per result
- **Launched:** 2026-07-17
- **Example body:** [`payloads/profiles.json`](payloads/profiles.json)

Collect one normalized profile record for each public username. A leading `@` is optional.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `usernames` | array of string | Yes | Public account usernames. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/profiles" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "usernames": [
    "openai",
    "@github"
  ]
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/profiles](https://docs.socq.ai/api-manual/x/profiles) · Landing page: [socq.ai/apis/x/profiles](https://socq.ai/apis/x/profiles?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### Twitter User Tweets Scraper API

Collect recent public posts with replies excluded from selected X accounts for monitoring, publishing analysis, and recurring datasets.

- **Request:** `POST https://api.socq.ai/v1/x/user-posts`
- **publicId:** `x/user-posts`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-07-17
- **Example body:** [`payloads/user-posts.json`](payloads/user-posts.json)

Collect recent public posts for one or more usernames. Replies are excluded.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `results_limit` | integer | No | (value 1 to 2000) |
| `usernames` | array of string | Yes | Public account usernames. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/user-posts" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "usernames": [
    "openai",
    "github"
  ],
  "results_limit": 40
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/user-posts](https://docs.socq.ai/api-manual/x/user-posts) · Landing page: [socq.ai/apis/x/user-posts](https://socq.ai/apis/x/user-posts?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### Twitter Search API

Build structured public X post datasets from a focused query with Latest or Top ordering for discovery, monitoring, and research.

- **Request:** `POST https://api.socq.ai/v1/x/search`
- **publicId:** `x/search`
- **Price:** 0.7 credits ($0.0035) per result
- **Launched:** 2026-07-17
- **Example body:** [`payloads/search.json`](payloads/search.json)

Search public posts using a keyword or search expression.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | Yes | Search query. |
| `results_limit` | integer | No | (value 1 to 2000) |
| `sort_by` | string | No | - |

```bash
curl -X POST "https://api.socq.ai/v1/x/search" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "query": "AI lang:en",
  "results_limit": 100,
  "sort_by": "latest"
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/search](https://docs.socq.ai/api-manual/x/search) · Landing page: [socq.ai/apis/x/search](https://socq.ai/apis/x/search?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### X Followers List API

Collect public follower accounts for one or more X usernames, with normalized identities, visible profile metrics, asynchronous tasks, and cursor-based retrieval.

- **Request:** `POST https://api.socq.ai/v1/x/followers-list`
- **publicId:** `x/followers-list`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-07-26
- **Example body:** [`payloads/followers-list.json`](payloads/followers-list.json)

Collect public X follower profiles. Results are normalized and billed by the actual saved record count.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `results_limit` | integer | No | (value 200 to 2000; default `200`) |
| `usernames` | array of string | Yes | Public account usernames. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/followers-list" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "usernames": [
    "@X"
  ],
  "results_limit": 200
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/followers-list](https://docs.socq.ai/api-manual/x/followers-list) · Landing page: [socq.ai/apis/x/followers-list](https://socq.ai/apis/x/followers-list?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### X Following List API

Collect public profiles followed by one or more X usernames, returning normalized identity, profile context, account signals, visible counters, and source username.

- **Request:** `POST https://api.socq.ai/v1/x/following-list`
- **publicId:** `x/following-list`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-07-26
- **Example body:** [`payloads/following-list.json`](payloads/following-list.json)

Collect public X following profiles. Results are normalized and billed by the actual saved record count.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `results_limit` | integer | No | (value 200 to 2000; default `200`) |
| `usernames` | array of string | Yes | Public account usernames. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/following-list" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "usernames": [
    "@X"
  ],
  "results_limit": 200
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/following-list](https://docs.socq.ai/api-manual/x/following-list) · Landing page: [socq.ai/apis/x/following-list](https://socq.ai/apis/x/following-list?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### X Post Quotes API

Collect public quote posts that reference known X status URLs, preserving commentary, author context, visible engagement, media, and source-post traceability.

- **Request:** `POST https://api.socq.ai/v1/x/post-quotes`
- **publicId:** `x/post-quotes`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-07-26
- **Example body:** [`payloads/post-quotes.json`](payloads/post-quotes.json)

Collect public quote posts for X posts. Results are normalized and billed by the actual saved record count.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `results_limit` | integer | No | (value 20 to 2000; default `100`) |
| `urls` | array of string | Yes | Public profile or content URLs. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/post-quotes" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "urls": [
    "https://x.com/X/status/2073395918011789670"
  ],
  "results_limit": 20
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/post-quotes](https://docs.socq.ai/api-manual/x/post-quotes) · Landing page: [socq.ai/apis/x/post-quotes](https://socq.ai/apis/x/post-quotes?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### X Post Replies API

Collect public replies from one or more X post URLs, returning reply text, authors, visible engagement, media, and parent context with per-post limits and sorting.

- **Request:** `POST https://api.socq.ai/v1/x/post-replies`
- **publicId:** `x/post-replies`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-07-26
- **Example body:** [`payloads/post-replies.json`](payloads/post-replies.json)

Collect public replies to X posts. Results are normalized and billed by the actual saved record count.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `results_limit` | integer | No | (value 20 to 2000; default `100`) |
| `sort_by` | string | No | - |
| `urls` | array of string | Yes | Public profile or content URLs. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/post-replies" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "urls": [
    "https://x.com/X/status/2073395918011789670"
  ],
  "results_limit": 20
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/post-replies](https://docs.socq.ai/api-manual/x/post-replies) · Landing page: [socq.ai/apis/x/post-replies](https://socq.ai/apis/x/post-replies?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### X Post Retweeters API

Resolve public X and Twitter status URLs into a task-level unique set of normalized public profiles for accounts that reposted those posts.

- **Request:** `POST https://api.socq.ai/v1/x/post-retweeters`
- **publicId:** `x/post-retweeters`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-07-25
- **Example body:** [`payloads/post-retweeters.json`](payloads/post-retweeters.json)

Collect public profiles that reposted X posts. Results are normalized and billed by the actual saved record count.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `results_limit` | integer | No | (value 100 to 2000; default `100`) |
| `urls` | array of string | Yes | Public profile or content URLs. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/post-retweeters" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "urls": [
    "https://x.com/X/status/2073395918011789670"
  ],
  "results_limit": 100
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/post-retweeters](https://docs.socq.ai/api-manual/x/post-retweeters) · Landing page: [socq.ai/apis/x/post-retweeters](https://socq.ai/apis/x/post-retweeters?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### X Trends API

Collect current public X trends for known numeric location identifiers, preserving source rank, query, description, location context, and collection time.

- **Request:** `POST https://api.socq.ai/v1/x/trends`
- **publicId:** `x/trends`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-07-26
- **Example body:** [`payloads/trends.json`](payloads/trends.json)

Collect public X trends by WOEID. Results are normalized and billed by the actual saved record count.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `results_limit` | integer | No | (value 20 to 2000; default `100`) |
| `woeids` | array of string | Yes | Numeric X location identifiers represented as strings. (items at least 1; pattern `^[0-9]+$`) |

```bash
curl -X POST "https://api.socq.ai/v1/x/trends" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "woeids": [
    "1"
  ],
  "results_limit": 100
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/trends](https://docs.socq.ai/api-manual/x/trends) · Landing page: [socq.ai/apis/x/trends](https://socq.ai/apis/x/trends?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### Twitter Mentions API

Collect public tweets that mention a target user handle, with support for date range filtering and engagement metrics.

- **Request:** `POST https://api.socq.ai/v1/x/mentions`
- **publicId:** `x/mentions`
- **Price:** 0.7 credits ($0.0035) per result
- **Launched:** 2026-09-11
- **Example body:** [`payloads/mentions.json`](payloads/mentions.json)

Collect public tweets that mention a target user handle, with support for date range filtering and engagement metrics.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `end_date` | string | No | - |
| `results_limit` | integer | No | (value 20 to 2000; default `20`) |
| `start_date` | string | No | - |
| `usernames` | array of string | Yes | Public account usernames. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/mentions" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "usernames": [
    "@OpenAI"
  ],
  "results_limit": 20
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/mentions](https://docs.socq.ai/api-manual/x/mentions) · Landing page: [socq.ai/apis/x/mentions](https://socq.ai/apis/x/mentions?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### Twitter User Search API

Search public X user accounts by keyword, returning normalized identity, bio, verified status, and audience metrics.

- **Request:** `POST https://api.socq.ai/v1/x/search-users`
- **publicId:** `x/search-users`
- **Price:** 0.6 credits ($0.003) per result
- **Launched:** 2026-09-11
- **Example body:** [`payloads/search-users.json`](payloads/search-users.json)

Search public X user accounts by keyword, returning normalized identity, bio, verified status, and audience metrics.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `query` | string | Yes | Search query. |
| `results_limit` | integer | No | (value 20 to 2000; default `20`) |

```bash
curl -X POST "https://api.socq.ai/v1/x/search-users" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "query": "OpenAI",
  "results_limit": 20
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/search-users](https://docs.socq.ai/api-manual/x/search-users) · Landing page: [socq.ai/apis/x/search-users](https://socq.ai/apis/x/search-users?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### X Community API

Read public X community details from community links, including descriptions, member counts and rules, with support for looking up several communities at once.

- **Request:** `POST https://api.socq.ai/v1/x/community`
- **publicId:** `x/community`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-10-16
- **Example body:** [`payloads/community.json`](payloads/community.json)

Submit an asynchronous task, then read its standard results.

Provide public X community URLs in urls, using /i/communities/{numeric_id}.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `urls` | array of string | Yes | Public profile or content URLs. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/community" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "urls": [
    "https://x.com/i/communities/1493446837214187523"
  ]
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/community](https://docs.socq.ai/api-manual/x/community) · Landing page: [socq.ai/apis/x/community](https://socq.ai/apis/x/community?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### X Community Posts API

Get public posts from X community links, with post text, authors and engagement counts returned together and a separate result limit for each community.

- **Request:** `POST https://api.socq.ai/v1/x/community-posts`
- **publicId:** `x/community-posts`
- **Price:** 0.7 credits ($0.0035) per result
- **Launched:** 2026-10-16
- **Example body:** [`payloads/community-posts.json`](payloads/community-posts.json)

Submit an asynchronous task, then read its standard results.

Provide public X community URLs in urls. results_limit applies to each URL, defaults to 100, and must be a multiple of 20 between 20 and 2000.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `results_limit` | integer | No | (value 20 to 2000; default `100`) |
| `urls` | array of string | Yes | Public profile or content URLs. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/community-posts" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "urls": [
    "https://x.com/i/communities/1493446837214187523"
  ],
  "results_limit": 20
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/community-posts](https://docs.socq.ai/api-manual/x/community-posts) · Landing page: [socq.ai/apis/x/community-posts](https://socq.ai/apis/x/community-posts?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### X Thread Context API

Read the context around an X post from its link, with the target post, earlier posts it replies to and public replies returned together with relationship IDs.

- **Request:** `POST https://api.socq.ai/v1/x/thread-context`
- **publicId:** `x/thread-context`
- **Price:** 0.5 credits ($0.0025) per result
- **Launched:** 2026-10-16
- **Example body:** [`payloads/thread-context.json`](payloads/thread-context.json)

Submit an asynchronous task, then read its standard results.

Provide X post URLs in urls. results_limit applies to each URL, defaults to 100, and accepts integers from 1 to 2000. Results retain the target post and its thread relationships.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `results_limit` | integer | No | (value 1 to 2000; default `100`) |
| `urls` | array of string | Yes | Public profile or content URLs. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/thread-context" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "urls": [
    "https://x.com/OpenAI/status/1890818505164038356"
  ],
  "results_limit": 20
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/thread-context](https://docs.socq.ai/api-manual/x/thread-context) · Landing page: [socq.ai/apis/x/thread-context](https://socq.ai/apis/x/thread-context?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### X Account Location API

Look up where an X account is based from its username, with the country X lists, how the account connects to X, its join date and how often it changed its username.

- **Request:** `POST https://api.socq.ai/v1/x/user-about`
- **publicId:** `x/user-about`
- **Price:** 0.7 credits ($0.0035) per result
- **Launched:** 2026-11-17
- **Example body:** [`payloads/user-about.json`](payloads/user-about.json)

Read the "About this account" panel X shows on profiles. For each username you get the country or region X lists as where the account is based, how the account connects to X (for example `United States App Store` or `Web`), the date it joined, how many times it has changed its username and the organization it is affiliated with. These details come from X's own account records, which makes them useful for vetting influencers, spotting coordinated accounts and checking where an audience really comes from.

Provide X usernames in usernames, with or without @. Each account returns one row with the country it is based in, how it connects to X, its join date and username change count. Some accounts, such as many government and public-interest accounts, have no country on X; they still return a row with `country` set to `null`.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `usernames` | array of string | Yes | Public account usernames. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/user-about" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "usernames": [
    "elonmusk",
    "BBCWorld"
  ]
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/user-about](https://docs.socq.ai/api-manual/x/user-about) · Landing page: [socq.ai/apis/x/user-about](https://socq.ai/apis/x/user-about?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### X Verified Followers API

Collect the verified accounts that follow any public X profile, with each follower's ID, username, display name, avatar, profile link and join date.

- **Request:** `POST https://api.socq.ai/v1/x/verified-followers`
- **publicId:** `x/verified-followers`
- **Price:** 0.7 credits ($0.0035) per result
- **Launched:** 2026-11-17
- **Example body:** [`payloads/verified-followers.json`](payloads/verified-followers.json)

Collect the followers of an X account that carry a verified checkmark, the same list X shows under the Verified Followers tab. Every row is a verified account with its ID, username, display name, profile link, avatar and join date, linked back to the account you asked about. Use it to see which creators, brands and paying users already follow a profile, to size the influential part of an audience, or to build an outreach list from the people who pay attention to a competitor.

Provide X usernames in usernames. results_limit applies to each account, defaults to 100, and must be a multiple of 20 between 20 and 2000.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `results_limit` | integer | No | (value 20 to 2000; default `100`) |
| `usernames` | array of string | Yes | Public account usernames. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/verified-followers" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "usernames": [
    "NASA"
  ],
  "results_limit": 20
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/verified-followers](https://docs.socq.ai/api-manual/x/verified-followers) · Landing page: [socq.ai/apis/x/verified-followers](https://socq.ai/apis/x/verified-followers?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### X List Tweets API

Read the timeline of a public X list from its URL, newest first, with each post's text, author, media and engagement and reposts flagged with their original author.

- **Request:** `POST https://api.socq.ai/v1/x/list-posts`
- **publicId:** `x/list-posts`
- **Price:** 0.7 credits ($0.0035) per result
- **Launched:** 2026-11-17
- **Example body:** [`payloads/list-posts.json`](payloads/list-posts.json)

Collect the timeline of a public X list: the posts and reposts its members have shared recently, newest first. A well-curated list is a ready-made feed of journalists, analysts, founders or competitors, so reading it as structured data lets you monitor a whole niche in one request instead of following each account. Reposts are kept and marked with `is_repost`, together with the ID and author of the original post, so you can filter them out or count how often members amplify each other.

Provide public X list URLs in urls, using /i/lists/{numeric_id}. results_limit applies to each list, defaults to 100, and must be a multiple of 20 between 20 and 2000. Reposts shared by list members are included and marked.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `results_limit` | integer | No | (value 20 to 2000; default `100`) |
| `urls` | array of string | Yes | Public profile or content URLs. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/list-posts" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "urls": [
    "https://x.com/i/lists/1940592907737845989"
  ],
  "results_limit": 20
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/list-posts](https://docs.socq.ai/api-manual/x/list-posts) · Landing page: [socq.ai/apis/x/list-posts](https://socq.ai/apis/x/list-posts?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### Twitter List Members API

Export the accounts on a public X list from its URL, each with bio, location, website, verification status and follower, following and post counts.

- **Request:** `POST https://api.socq.ai/v1/x/list-members`
- **publicId:** `x/list-members`
- **Price:** 0.7 credits ($0.0035) per result
- **Launched:** 2026-11-17
- **Example body:** [`payloads/list-members.json`](payloads/list-members.json)

Export the accounts someone has added to a public X list. Each member comes back as a full profile with bio, location, website, verification status and follower, following and post counts. Lists are hand-picked, so their members are often a strong seed for prospecting: a "fintech founders" or "AI researchers" list curated by someone in the field is a shortlist you can enrich, score and reach out to without searching from scratch.

Provide public X list URLs in urls, using /i/lists/{numeric_id}. results_limit applies to each list, defaults to 100, and must be a multiple of 20 between 20 and 2000.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `results_limit` | integer | No | (value 20 to 2000; default `100`) |
| `urls` | array of string | Yes | Public profile or content URLs. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/list-members" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "urls": [
    "https://x.com/i/lists/1940592907737845989"
  ],
  "results_limit": 20
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/list-members](https://docs.socq.ai/api-manual/x/list-members) · Landing page: [socq.ai/apis/x/list-members](https://socq.ai/apis/x/list-members?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### Twitter List Followers API

Collect the accounts that follow a public X list from its URL, each as a full profile with bio, location and follower, following and post counts.

- **Request:** `POST https://api.socq.ai/v1/x/list-followers`
- **publicId:** `x/list-followers`
- **Price:** 0.7 credits ($0.0035) per result
- **Launched:** 2026-11-17
- **Example body:** [`payloads/list-followers.json`](payloads/list-followers.json)

Collect the accounts that subscribe to a public X list. Following a list is a deliberate choice to read a topic, so its followers are people with a stated interest: the audience of a curated "SaaS founders" or "climate tech" list is a precise segment for research, lookalike targeting or community building. Each follower comes back as a full profile with bio, location and follower, following and post counts.

Provide public X list URLs in urls, using /i/lists/{numeric_id}. results_limit applies to each list, defaults to 100, and must be a multiple of 20 between 20 and 2000.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `results_limit` | integer | No | (value 20 to 2000; default `100`) |
| `urls` | array of string | Yes | Public profile or content URLs. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/list-followers" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "urls": [
    "https://x.com/i/lists/1940592907737845989"
  ],
  "results_limit": 20
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/list-followers](https://docs.socq.ai/api-manual/x/list-followers) · Landing page: [socq.ai/apis/x/list-followers](https://socq.ai/apis/x/list-followers?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### X Community Members API

Export the members of a public X community from its URL, each with bio, location, website, verification status and follower, following and post counts.

- **Request:** `POST https://api.socq.ai/v1/x/community-members`
- **publicId:** `x/community-members`
- **Price:** 0.7 credits ($0.0035) per result
- **Launched:** 2026-11-17
- **Example body:** [`payloads/community-members.json`](payloads/community-members.json)

Export the people who have joined a public X community. Joining a community is an opt-in signal around a single topic, whether that is building in public, a programming language or a crypto project, so the member list is a well-defined audience. Each member comes back as a full profile with bio, location, website, verification status and follower, following and post counts, ready for audience research, partner discovery or comparing two communities side by side. Pair it with [X Community](https://docs.socq.ai/api-manual/x/community) for the community's description and rules.

Provide public X community URLs in urls, using /i/communities/{numeric_id}. results_limit applies to each community, defaults to 100, and must be a multiple of 20 between 20 and 2000.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `results_limit` | integer | No | (value 20 to 2000; default `100`) |
| `urls` | array of string | Yes | Public profile or content URLs. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/community-members" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "urls": [
    "https://x.com/i/communities/1493446837214187523"
  ],
  "results_limit": 20
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/community-members](https://docs.socq.ai/api-manual/x/community-members) · Landing page: [socq.ai/apis/x/community-members](https://socq.ai/apis/x/community-members?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### X Community Moderators API

Get the admins and moderators who run a public X community from its URL, returned in one task as full profiles with bios and audience counts.

- **Request:** `POST https://api.socq.ai/v1/x/community-moderators`
- **publicId:** `x/community-moderators`
- **Price:** 0.7 credits ($0.0035) per result
- **Launched:** 2026-11-17
- **Example body:** [`payloads/community-moderators.json`](payloads/community-moderators.json)

Get the team that runs a public X community: its admins and moderators, returned in one request as full profiles. These are the people who set the rules and decide what stays in the feed, which makes them the right contacts for a sponsorship, an AMA or a partnership, and a quick way to judge who is really behind a community before you invest time in it.

Provide public X community URLs in urls, using /i/communities/{numeric_id}. Each community returns its full moderator team, including admins.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `urls` | array of string | Yes | Public profile or content URLs. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/community-moderators" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "urls": [
    "https://x.com/i/communities/1493446837214187523"
  ]
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/community-moderators](https://docs.socq.ai/api-manual/x/community-moderators) · Landing page: [socq.ai/apis/x/community-moderators](https://socq.ai/apis/x/community-moderators?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### X Communities Search API

Find X communities by keyword, with each community's name, member count, banner and link ready for the member, moderator and post endpoints.

- **Request:** `POST https://api.socq.ai/v1/x/search-communities`
- **publicId:** `x/search-communities`
- **Price:** 0.7 credits ($0.0035) per result
- **Launched:** 2026-11-17
- **Example body:** [`payloads/search-communities.json`](payloads/search-communities.json)

Find X communities by keyword. Each result is a community with its name, member count, banner image and whether it is marked as sensitive, along with the community URL you can pass straight to [X Community Members](https://docs.socq.ai/api-manual/x/community-members), [X Community Moderators](https://docs.socq.ai/api-manual/x/community-moderators) or [X Community Posts](https://docs.socq.ai/api-manual/x/community-posts). It is the starting point for mapping where a topic is discussed on X and which groups are big enough to matter.

Provide a keyword in query. results_limit defaults to 20 and must be a multiple of 10 between 10 and 500. A keyword with no matching communities returns an empty result. Search results carry each community's name, member count, banner and sensitive-content flag; the description, rules and join policies come from [X Community](https://docs.socq.ai/api-manual/x/community).

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `query` | string | Yes | Search query. |
| `results_limit` | integer | No | (value 10 to 500; default `20`) |

```bash
curl -X POST "https://api.socq.ai/v1/x/search-communities" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "query": "bitcoin",
  "results_limit": 20
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/search-communities](https://docs.socq.ai/api-manual/x/search-communities) · Landing page: [socq.ai/apis/x/search-communities](https://socq.ai/apis/x/search-communities?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### X Articles API

Turn X Articles into clean text from the post URL, with the title, preview line, full body, cover image, author and likes, replies, quotes and views.

- **Request:** `POST https://api.socq.ai/v1/x/article`
- **publicId:** `x/article`
- **Price:** 0.7 credits ($0.0035) per result
- **Launched:** 2026-11-17
- **Example body:** [`payloads/article.json`](payloads/article.json)

Read X Articles, the long-form posts with a title, cover image and formatted body, as clean text. Pass the URL of the post that publishes the Article and get back its title, the preview line shown in timelines, the full body with paragraphs separated by blank lines, the cover image, the author and its likes, replies, quotes and views. Use it to archive long-form writing, feed it to a summarizer or language model, or track how Articles perform compared with regular posts.

Provide the X post URLs that publish each Article in urls, using /{username}/status/{post_id}. Each Article returns one row. A post that is not an Article returns no row; when none of the URLs is an Article, the task fails and is not charged.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `urls` | array of string | Yes | Public profile or content URLs. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/article" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "urls": [
    "https://x.com/USDOL/status/2119796255089947070"
  ]
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/article](https://docs.socq.ai/api-manual/x/article) · Landing page: [socq.ai/apis/x/article](https://socq.ai/apis/x/article?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### X Spaces API

Look up X Spaces from their links, with the title, status, scheduled start, hosts, speakers, live listener count, replay count and replay availability.

- **Request:** `POST https://api.socq.ai/v1/x/space`
- **publicId:** `x/space`
- **Price:** 0.7 credits ($0.0035) per result
- **Launched:** 2026-11-17
- **Example body:** [`payloads/space.json`](payloads/space.json)

Look up an X Space, the live audio rooms hosted on X, from its link. Each Space returns its title, whether it is scheduled, live or ended, the scheduled start time, the hosts and co-hosts, the speakers who took the stage, how many people listened live, how many times the recording was replayed and whether a replay is available. Use it to report on Spaces you hosted or sponsored, track a competitor's live audio program or build a list of the speakers active in your niche.

Provide X Space URLs in urls, using /i/spaces/{space_id}. Scheduled, live and ended Spaces are supported. Each Space returns one row.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `urls` | array of string | Yes | Public profile or content URLs. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/space" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "urls": [
    "https://x.com/i/spaces/1OdWgBerXWvaQz"
  ]
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/space](https://docs.socq.ai/api-manual/x/space) · Landing page: [socq.ai/apis/x/space](https://socq.ai/apis/x/space?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### Twitter Media Scraper API

Collect the photos, videos and GIFs an X account has posted from its username, newest first, with the full-quality media files, captions and engagement counts.

- **Request:** `POST https://api.socq.ai/v1/x/user-media`
- **publicId:** `x/user-media`
- **Price:** 0.7 credits ($0.0035) per result
- **Launched:** 2026-11-17
- **Example body:** [`payloads/user-media.json`](payloads/user-media.json)

Collect the posts from an account's Media tab on X: every post that carries a photo, video or GIF, newest first. Each post includes its text, engagement counts, views and the media files themselves, with videos pointing to the highest-quality MP4 available and a preview image. Use it to audit a brand's visual content, gather a creator's best-performing clips, or build a media archive of an account without scrolling through its timeline.

Provide one X username in username. results_limit defaults to 20 and accepts integers from 1 to 1000. Results are the account's posts that carry photos, videos or GIFs, newest first.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `results_limit` | integer | No | (value 1 to 1000; default `20`) |
| `username` | string | Yes | A public account username. |

```bash
curl -X POST "https://api.socq.ai/v1/x/user-media" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "username": "NASA",
  "results_limit": 20
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/user-media](https://docs.socq.ai/api-manual/x/user-media) · Landing page: [socq.ai/apis/x/user-media](https://socq.ai/apis/x/user-media?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### X User Replies API

Collect the replies an X account has written from its username, newest first, each paired with the post it answers and its author.

- **Request:** `POST https://api.socq.ai/v1/x/user-replies`
- **publicId:** `x/user-replies`
- **Price:** 0.7 credits ($0.0035) per result
- **Launched:** 2026-11-17
- **Example body:** [`payloads/user-replies.json`](payloads/user-replies.json)

Collect the replies an X account has written, the content of its Replies tab, newest first. Each reply comes with the post it answers: that post's text, author, link and publish time sit in `in_reply_to`, so every row reads as a complete exchange. Replies show who an account talks to and what it says off its main timeline, which is useful for brand-reputation monitoring, customer-service audits, and understanding how executives and creators engage with their audience.

Provide one X username in username. results_limit defaults to 20 and accepts integers from 1 to 1000. Each reply comes with the post it answers.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `results_limit` | integer | No | (value 1 to 1000; default `20`) |
| `username` | string | Yes | A public account username. |

```bash
curl -X POST "https://api.socq.ai/v1/x/user-replies" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "username": "elonmusk",
  "results_limit": 20
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/user-replies](https://docs.socq.ai/api-manual/x/user-replies) · Landing page: [socq.ai/apis/x/user-replies](https://socq.ai/apis/x/user-replies?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### Twitter Follow Checker API

Check whether one X account follows up to 100 others and whether each follows it back, with a mutual-follow flag for every pair.

- **Request:** `POST https://api.socq.ai/v1/x/check-follow`
- **publicId:** `x/check-follow`
- **Price:** 0.7 credits ($0.0035) per result
- **Launched:** 2026-11-17
- **Example body:** [`payloads/check-follow.json`](payloads/check-follow.json)

Check the follow relationship between one X account and a set of others. For every pair you get both directions at once: whether `username` follows the other account, whether that account follows back, and whether the follow is mutual. Use it to verify that campaign participants follow your brand, confirm that a partner account actually follows you back, or map the connections between a group of creators.

Provide the account to check in username and up to 100 accounts to compare it with in usernames. Each pair returns whether username follows the other account and whether it is followed back.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `username` | string | Yes | The X account to check, with or without @. |
| `usernames` | array of string | Yes | X accounts to compare it with, with or without @. (items 1 to 100) |

```bash
curl -X POST "https://api.socq.ai/v1/x/check-follow" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "username": "elonmusk",
  "usernames": [
    "SpaceX",
    "NASA"
  ]
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/check-follow](https://docs.socq.ai/api-manual/x/check-follow) · Landing page: [socq.ai/apis/x/check-follow](https://socq.ai/apis/x/check-follow?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

### Twitter Video Transcript API

Turn the speech in X videos into plain text from the post URL, with the video length returned alongside each transcript.

- **Request:** `POST https://api.socq.ai/v1/x/post-transcript`
- **publicId:** `x/post-transcript`
- **Price:** 0.7 credits ($0.0035) per result
- **Launched:** 2026-11-17
- **Example body:** [`payloads/post-transcript.json`](payloads/post-transcript.json)

Turn the speech in an X video into text. Pass the link of a post that contains a video and get back the transcript as plain text together with the video's length in seconds. Transcripts make video content searchable and quotable: pull the exact wording of an interview clip, summarize a product demo, translate a speech, or feed spoken content into the same analysis you already run on written posts.

Provide X post URLs that contain a video in urls, using /{username}/status/{post_id}. Each video returns its spoken text and duration. A video up to 2 minutes costs 0.7 credits; a longer video costs 4 credits for every started minute of its full length, so a 3-minute video costs 12 credits. Posts without a video return no row and are not charged.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string (uri) | No | - |
| `urls` | array of string | Yes | Public profile or content URLs. (items at least 1) |

```bash
curl -X POST "https://api.socq.ai/v1/x/post-transcript" \
  -H "Authorization: Bearer $SOCQ_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "urls": [
    "https://x.com/NASA/status/2119833829389041896"
  ]
}'
```

Full docs: [https://docs.socq.ai/api-manual/x/post-transcript](https://docs.socq.ai/api-manual/x/post-transcript) · Landing page: [socq.ai/apis/x/post-transcript](https://socq.ai/apis/x/post-transcript?utm_source=github&utm_medium=readme&utm_campaign=socq-x-api)

## Repository contents

| Path | Purpose |
| --- | --- |
| [`examples/curl/socq.sh`](examples/curl/socq.sh) | Submit, poll and paginate with cURL and jq |
| [`examples/node/socq.mjs`](examples/node/socq.mjs) | Same workflow in Node.js 20+ (no dependencies) |
| [`examples/python/socq.py`](examples/python/socq.py) | Same workflow in Python 3.8+ (standard library) |
| [`payloads/`](payloads) | One documented request body per endpoint |
| [`endpoints.json`](endpoints.json) | Endpoint list, prices and request schemas used by the scripts and checks |
| [`fixtures/`](fixtures) | Synthetic submit and task response shapes |
| [`docs/production-notes.md`](docs/production-notes.md) | Retries, timeouts, pagination and data handling |
| [`scripts/check.mjs`](scripts/check.mjs) | Offline check: payloads, syntax and secrets |

## Responsible use and platform scope

- Use only publicly accessible X (Twitter) data and the fields supported by each endpoint.
- Do not use the examples to access restricted content, login-only surfaces, authentication controls or non-public personal information.
- SocQ is not an official API of the represented platform and is not affiliated with or endorsed by it. Platform names and trademarks belong to their respective owners.
- Before production use, assess the laws, platform terms, privacy obligations and retention requirements that apply to your organization and use case.
- Collect only the fields needed for a defined purpose, restrict access, set retention periods, and support correction or deletion workflows where required.

This section describes the public-data boundary; it is not legal advice.

## License

[MIT](LICENSE)
