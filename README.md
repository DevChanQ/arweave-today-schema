# Arweave Today - Content Schema

This README describes the structure of the `Arweave Today` article JSON, which captures a snapshot of noteworthy updates, community highlights, and developer activities in the Arweave ecosystem. This schema supports structured, media-rich storytelling for readers and frontend renderers.

---

## :package: JSON Structure

### Top-Level Fields

- **`topics`** (`Array<Object>`)
  A list of featured stories or posts from the Arweave community.

- **`chitchat`** (`Object`)
  A light or informal sidebar section with a tip or fun fact related to the permaweb.

- **`suggested`** (`Object`)
  A recommended long-form article or reading piece that complements the day's updates.

- **`ts`** (`Number`)
  Unix timestamp in milliseconds, representing the publication date/time of the digest.

- **`previous`** (`String`)
  ID or reference to the previous issue/article (used for navigation or versioning).

---

## :newspaper: Topics

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

- **`image`** *(optional)* (`String`)
  URL to an image preview or poster.

- **`video`** *(optional)* (`String`)
  URL to a video clip related to the post.

- **`featured`** *(optional)* (`String` or `Boolean`)
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

## :speech_balloon: Chitchat

An engaging sidebar snippet.

### Fields:

- **`headline`** (`String`)
  Title of the tip or blurb.

- **`body`** (`String`)
  Description or teaser text.

- **`image`** (`String`)
  A visual (often playful) GIF or static image.

- **`nature`** (`String`)
  Type of snippet (e.g., `"Did you know?"`).

---

## :books: Suggested Read

A featured long-form external article or blog post.

### Fields:

- **`url`** (`String`)
  Link to the external article.

- **`headline`** (`String`)
  Title of the article.

- **`body`** (`String`)
  Description or excerpt from the article.

- **`image`** (`String`)
  Banner or thumbnail image.

- **`button`** (`String`)
  Label for the call-to-action button (e.g., `"Read article"`).

- **`nature`** (`String`)
  Label describing the article category (e.g., `"today's read"`).

---

## :compass: Example Use Cases

- Weekly or daily Arweave ecosystem roundups
- Community newsletters
- Embeddable digest widgets on web portals
- Indexing for historical community activity
