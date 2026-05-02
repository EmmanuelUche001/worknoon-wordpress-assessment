# Section D: SEO Technical Troubleshooting Diagnosis

**Scenario:** A new Worknoon website is not indexing even after sitemap submission.

Here is the step-by-step diagnostic process to identify and resolve the indexing blocker:

**1. Robots.txt & No-Index Audit**
* **Check `robots.txt`:** I would navigate to `worknoon.com/robots.txt` to ensure there isn't a `Disallow: /` directive blocking search engine bots from crawling the site.
* **Check Meta Tags:** I would inspect the page source code (or use a crawler) to ensure the `<meta name="robots" content="noindex">` tag was not accidentally left on from the development/staging phase. In WordPress, I'd check *Settings > Reading* to ensure "Discourage search engines from indexing this site" is unchecked.

**2. Crawlability Tests**
* I would run a site audit using a tool like Screaming Frog to simulate a crawl. This identifies if there are server errors (5xx), broken internal links (4xx), or redirect loops preventing Googlebot from navigating the site structure.

**3. Canonical Checks**
* I would inspect the source code to ensure the `rel="canonical"` tag points to the correct, absolute URL of the page. If the canonical tag points to an old staging URL or a non-existent page, Google will ignore the live page.

**4. Sitemap Structure Issues**
* I would review the submitted XML sitemap to ensure it only contains 200 OK status pages. If the sitemap contains redirects, 404s, or pages tagged with no-index, it sends conflicting signals to Google and wastes crawl budget.

**5. Page Speed & Rendering Blockers**
* If the site relies heavily on client-side JavaScript to render core content, Google might struggle to index it quickly. I would test the site using Google PageSpeed Insights. Massive layout shifts, extremely slow server response times (TTFB), or heavy un-minified scripts can cause Google to abandon the crawl.

**6. Search Console Debugging Steps**
* Go to **Google Search Console > Pages** report to see exactly *why* pages aren't indexed (e.g., "Crawled - currently not indexed" or "Discovered - currently not indexed").
* Use the **URL Inspection Tool** on the homepage and click "Test Live URL" to see exactly how Google renders the page in real-time and check for specific blocking issues.