# Section E: Short Answer Questions

**1. Difference between Google Knowledge Graph and Google Knowledge Panel**

The Knowledge Graph is Google's massive, invisible backend database that understands how entities (people, places, things) connect to each other. The Knowledge Panel is the visual result you see on the right side of the search engine results page (SERP). The Panel is simply the front-end display of the data pulled from the Knowledge Graph.

**2. How Google determines entity identity**

Google determines an entity's identity by cross-referencing information across the web to build confidence. It looks for consistent "mentions" across authoritative sources (like Wikipedia, Crunchbase, or major news outlets), analyzes structured data (Schema markup) provided by the entity's own website, and maps relationships between other known entities to verify who or what the entity is.

**3. When to create Custom Post Types (CPTs) instead of pages**

You should use Custom Post Types when you have a repeating, structured set of data that doesn't fit the standard chronological flow of a blog post or the static nature of a page. For example, if a website has "Testimonials," "Team Members," or "Properties for Sale," these should be CPTs so you can assign custom fields and taxonomies to them, making the database much easier to manage and scale.

**4. Recommended plugins for speed optimization and why**

* **WP Rocket:** It is the most comprehensive, user-friendly premium caching plugin. It handles page caching, GZIP compression, and advanced features like deferring JavaScript and lazy-loading images all in one place.
* **Perfmatters:** Excellent for disabling unnecessary WordPress bloat and script management. It allows you to disable specific plugins from loading on pages where they aren't needed, drastically reducing page weight.
* **ShortPixel (or Imagify):** Essential for automatically compressing images and serving them in next-gen formats like WebP without losing visual quality.
