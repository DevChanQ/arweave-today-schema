![Arweave Today Banner](./banner.png)

# Arweave Today - Content Schema

This README describes the structure of the `Arweave Today` article JSON, which captures a snapshot of noteworthy updates, community highlights, and developer activities in the Arweave ecosystem. The schema is designed to support structured, media-rich storytelling for both readers and frontend renderers.

[Check out Arweave Today](https://arweavehub.com/today)

---

## Usage

You can access the JSON content for the latest edition of Arweave Today at [https://today_arweave.ar.io](https://today_arweave.ar.io). To view previous editions, use the Arweave transaction ID found in the `previous` field of the current edition’s JSON. For example, you can fetch a previous edition at `https://arweave.net/{previous}`.

## RSS Feed

Arweave Today is also available as an RSS feed at [https://today-rss_arweave.ar.io](https://today-rss_arweave.ar.io).

---

## :package: JSON Schema

### Top-Level Fields

- **`topics`** (`Array<Topic>`)  
  A list of featured stories or posts from the Arweave community.

- **`chitchat`** (`Topic`)  
  A light or informal sidebar section, often including a tip or fun fact related to the permaweb.

- **`suggested`** (`Topic`)  
  A recommended long-form article or reading piece that complements the day's updates.

- **`ts`** (`Number`)  
  Unix timestamp in milliseconds, representing the publication date and time of the digest.

- **`previous`** (`String`)  
  The Arweave transaction ID of the previous issue or article, used for navigation.

---

## :newspaper: Topic Type

Each object in the `topics` array represents a featured post or announcement.

### Topic Fields

- **`url`** (`String`)  
  The X/Twitter link to the original post or thread.

- **`body`** (`String`)  
  A short summary or excerpt of the post content.

- **`headline`** (`String`)  
  The article's display title.

- **`nature`** (`String`)  
  The type or category of the post, used for tagging and filtering.

- **`button`** *(optional)* (`String`)  
  Label for the call-to-action button (e.g., `"Read article"`).

- **`image`** *(optional)* (`String`)  
  URL to an image preview or poster.

- **`video`** *(optional)* (`String`)  
  URL to a video clip related to the post.

- **`audio`** *(optional)* (`String`)  
  URL to an audio clip or podcast episode.

- **`featured`** *(optional)* (`Boolean`)  
  Indicates if this topic should be visually highlighted in the layout (e.g., `true`).

---

## :label: Supported `nature` Values

The `nature` field helps categorize topics for filtering or visual grouping. Supported values include:

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

- Weekly or daily roundups of the Arweave ecosystem
- Community newsletters
- Embeddable digest widgets for web portals
- Indexing and archiving historical community activity
