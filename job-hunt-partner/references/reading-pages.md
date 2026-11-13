# Reading job pages

Use three levels in order. Move down a level only when the one above fails.

**1. Web search and web fetch.** The default. Most job boards and careers pages read fine this way.

**2. A public ATS endpoint.** Some boards render as a listing index instead of the single job. Greenhouse has a public job board API: fetch `https://boards-api.greenhouse.io/v1/boards/{company}/jobs/{job_id}` for the full description. Lever and Ashby boards usually read fine as normal pages.

**3. A browser tool,** if the session has one (for example Claude in Chrome or a built-in browser). Use it for pages the first two cannot read: LinkedIn, anything behind a login, pages that render client-side, and pages that return an error or a wall. LinkedIn only works in a browser where the user is signed in.

Do not work around a page that refuses the fetch tool with shell commands, curl or scripts. The browser is the fallback, and if there is no browser, ask the user to paste the content.

## Finding the right company page

Company names collide. A search by name can land on a dead page, a regional subsidiary or an unrelated company. In order:

1. The company's own website footer, which usually links its official LinkedIn page and careers page. Take the careers and ATS links from there too.
2. The job posting, if it links the company page.
3. A LinkedIn search by name, as a last resort.

Confirm it is the right page: the website on the LinkedIn page should point back to the site you came from, and the employee count should fit the company.

## Finding people to contact

The company's LinkedIn "People" tab needs a browser. Search it with quoted keywords:

- The function: the user's field, plus "head of" or "lead" for that field.
- "recruiter" and "talent", plus "people partner" or "sourcer", since recruiter titles vary.
- The user's school or past employers, for shared background.
- A keyword from the role itself, which often surfaces the hiring manager when generic searches return nothing.

Record name, title, profile link, connection degree and any shared background. Note what you could not find.

## Rules for the browser

- **Read only.** Never click Connect, send a message, apply, withdraw or change anything in the user's accounts. The user does every action that speaks for them.
- Open a new tab instead of taking over one of theirs, and close it when done.
- Avoid buttons that open a confirmation dialog, since a dialog can freeze the browser tool until the user clears it.
- Read one page at a time at a human pace. No bulk crawling.
- If the tool stops responding or the same action fails twice, stop and tell the user what happened instead of retrying in a loop.
- If a site is not allowed in the browser tool, say so and ask the user to allow it or paste the content.

If a page cannot be read at any level, say so and ask the user for the content. Claim to have read only pages you actually loaded.
