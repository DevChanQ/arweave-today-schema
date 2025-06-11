![Arweave Today Banner](./banner.png)

# Arweave Today - Content Schema

This README describes the structure of the `Arweave Today` article JSON, which captures a snapshot of noteworthy updates, community highlights, and developer activities in the Arweave ecosystem. This schema supports structured, media-rich storytelling for readers and frontend renderers.

[Check out Arweave Today](https://arweavehub.com/today)

---

## Usage

You can get the JSON content of the latest edition of Arweave Today at https://today_arweave.ar.io. You can also get previous editions of Arweave Today by fetching the content of the Arweave transaction id stored in the `previous` field of the Arweave Today JSON, e.g. `https://arweave.net/{previous}`

## RSS feed

Arweave Today is also available as a RSS feed at https://today-rss_arweave.ar.io

## :package: JSON Schema

### Top-Level Fields

- **`topics`** (`Array<Topic>`)
  A list of featured stories or posts from the Arweave community.

- **`chitchat`** (`Topic`)
  A light or informal sidebar section with a tip or fun fact related to the permaweb.

- **`suggested`** (`Topic`)
  A recommended long-form article or reading piece that complements the day's updates.

- **`ts`** (`Number`)
  Unix timestamp in milliseconds, representing the publication date/time of the digest.

- **`previous`** (`String`)
  Arweave transaction id of the previous issue/article (used for navigation).

---

## :newspaper: Topic type

Each object in the `topics` array represents a featured post or announcement.

### Topic Fields

- **`url`** (`String`)
  The X/Twitter link to the original post or thread.

- **`body`** (`String`)
  A short summary or excerpt of the post content.

- **`headline`** (`String`)
  The article's display title.

- **`nature`** (`String`)
  The type/category of the post. Used for tagging and filtering.

- **`button`** *(optional)* (`String`)
  Label for the call-to-action button (e.g., `"Read article"`).

- **`image`** *(optional)* (`String`)
  URL to an image preview or poster.

- **`video`** *(optional)* (`String`)
  URL to a video clip related to the post.

- **`featured`** *(optional)* (`Boolean`)
  Indicates if this topic is visually highlighted in the layout (e.g., `"true"`).

---

## :label: Supported `nature` Values

The `nature` field helps categorize topics for filtering or visual grouping. Valid values include:

- `event`
- `community`
- `stats`
- `nfts`
- `media`
- `developer`
- `ao-computer`
- `token`
- `giveaway`
- `tutorial`
- `games`
- `ai`
- `update`
- `security`
- `newsletter`
- `defi`
- `privacy`
- `storage`
- `funding`

---

## :compass: Example Use Cases

- Weekly or daily Arweave ecosystem roundups
- Community newsletters
- Embeddable digest widgets on web portals
- Indexing for historical community activity
