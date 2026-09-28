# Week 4 prompts — polish + launch

The point of this week is not a finished website. It's a live website plus the
loop you'll run forever: critique, fix, ship. Feedback doesn't stop when the
week does.

## In session — critique, experiment, polish

The site is functionally complete now, so a scored critique can find systemic
problems instead of judging a fragment.

1. **Baseline first** — know where you stand before changing anything:
   > /impeccable critique the complete portfolio at [local URL]. Use the homepage as the primary artifact, and also inspect every route in my site map. Save one prioritized report before changing code.

2. **Fix the priorities** — before any detail polish:
   > Use the saved critique report. Show me its priority issues in impact order, separate systemic problems from cosmetic ones, fix the highest-impact issue across every affected page, verify at desktop, tablet, and mobile widths, then stop for review.

3. **The experiment loop** — repeat with `layout` and `colorize`:
   > Commit what we have so we can revert. Then run /impeccable typeset on my homepage and show me what changed and why. I'll keep it or ask you to revert.

   The ritual matters more than any single result: commit, experiment, judge,
   keep or revert. Git makes taste experiments free.

## The launch checklist

Six things to check, and the tool that checks each one. These are pass or fail,
not opinions — that's what makes it a checklist instead of a mood.

| Check | Tool | Passes when |
|---|---|---|
| Performance | Lighthouse locally, PageSpeed Insights on the live URL | The deployed site scores well on mobile, not just your laptop on your wifi |
| Accessibility | `rams`, plus Lighthouse's accessibility score | Contrast passes AA, every control works by keyboard, images have alt text |
| Mobile | `/impeccable adapt`, then your actual phone | Nothing overflows, tap targets fit a thumb, text is readable without zoom |
| Code and design system | `/impeccable audit`, `/impeccable polish`, then `polish` | Every page uses the tokens and components in DESIGN.md, with no one-off values |
| Favicon | `favicon` skill | Your mark shows in the tab, in a bookmark, and on a phone home screen |
| SEO | The prompts below, then Google Search Console | Unique titles, one canonical host, sitemap submitted, no stray noindex |

### 1 · Performance

4. **Score it yourself.** In Chrome: open your local site, press `Cmd + Option + I`,
   choose the Lighthouse tab, select Mobile, click Analyze page load. Then bring
   the numbers back:
   > My Lighthouse scores for [page] are Performance [x], Accessibility [x], Best Practices [x], SEO [x]. Group the failing audits into what matters for a portfolio and what is noise. Start with images and fonts — they're usually most of the gap. Fix one issue, explain it in a sentence, then stop so I can re-run Lighthouse and watch the score move.

### 2 · Accessibility

5. **Contrast, keyboard, alt text** — the findings your eyes miss:
   > Run the rams skill on my components. Fix the contrast and accessibility findings — explain each fix in one line.

### 3 · Mobile

6. **Run the pass, then open the site on your real phone.** The simulator lies
   about thumbs:
   > /impeccable adapt my site for mobile

### 4 · Code and design system

7. **Audit first, and fix nothing yet** — you want causes, not symptoms:
   > /impeccable audit the complete portfolio at [local URL]. Inspect every route in my site map, turn the findings into a fix list ordered by impact, and show me the list without fixing anything.

8. **Then pull every page back onto the system:**
   > /impeccable polish my site. Align every page with DESIGN.md and the shared tokens and components. Fix inconsistent spacing, alignment, typography, color, interaction states, imagery, and copy. Fix systemic causes instead of patching one page at a time. Preserve the approved direction and my written content, then stop for review.

### 5 · Favicon

9. **Your mark in the browser tab, from one image:**
   > Run the favicon skill on [your image]. Show me the generated files and verify the favicon appears in the browser tab.

### 6 · SEO

10. **What people see when you send the link:**
    > Give every page an accurate title and description. Add social-preview tags and one preview image. Show me how the homepage and one case study will look when shared.

11. **What people see when you don't send the link:**
    > Make my site findable in search, not only by link. 1) Confirm every page has a unique title and description that reads like a sentence, not a keyword list. 2) Check heading structure: one h1 per page, in order, and real text instead of text baked into images. 3) Add descriptive alt text to every meaningful image. 4) Pick one host, apex or www, redirect the other to it, and give each page a self-referencing canonical tag on that host. 5) Generate sitemap.xml and robots.txt, and confirm no page still carries a noindex tag from the starter. 6) Add Person structured data with my name, role, and links. Show me each change and the file it lives in.

12. **Then tell Google you exist.** Add your site at
    [Google Search Console](https://search.google.com/search-console), verify
    ownership, and submit your sitemap. Indexing can take days or weeks and is
    never guaranteed, so do it the day you launch.

    Optional, if you want to go deeper than a portfolio needs:
    [claude-seo](https://github.com/AgriciDaniel/claude-seo) is a plugin with a
    specialist skill per SEO concern. Install it with `/plugin marketplace add
    AgriciDaniel/claude-seo`, then `/plugin install
    claude-seo@agricidaniel-claude-seo`, then `/seo setup` — the last step builds
    its own Python environment, so give it a minute. Worth your time:
    `/seo-technical` (crawlability, indexability, Core Web Vitals, structured
    data), `/seo-schema` (generates and validates your JSON-LD), and `/seo-geo`
    (whether ChatGPT, Perplexity, and AI Overviews can find and cite you). If a
    skill fails to run, `/seo doctor` tells you what's missing.

## Launch — the last mile

13. **What breaks in public is rarely the design.** Walk the list before you
    announce it:
    > Walk my pre-launch checklist and report pass or fail on each item: 1) Every internal and external link resolves — no 404s, no placeholder hrefs. 2) A real 404 page exists and matches the design. 3) The site loads over https on my custom domain, and one address redirects to the other. 4) Analytics is installed and recording a visit. 5) Resume and contact links open correctly, including on mobile. 6) No API keys, .env files, or private client work are committed. Fix what fails, then re-check. If a key was ever committed, treat it as public: revoke and reissue it first, then clean it out of the repository.

14. **Ship it**
    > Run the polish skill on my changes, commit, push, and deploy. Then give me the final URL and a one-paragraph summary of what shipped in four weeks.

15. **Now score the deployed site.** Run your live URL through
    [PageSpeed Insights](https://pagespeed.web.dev) — the same Lighthouse audits,
    but run on Google's machines with mobile throttling, so it usually scores
    lower than your laptop did:
    > My site is live at [URL]. PageSpeed Insights gives it [x] mobile and [x] desktop, and flags: [paste the top issues]. Tell me which flags actually matter for a portfolio and which to ignore, fix the top two largest first, redeploy, then stop so I can re-run PageSpeed and confirm the score moved.

By Friday: a portfolio that passes all six checks, refined by experiments you
chose to keep, findable when shared and when searched — live at a URL you're
proud to text someone.

Launch is a checkpoint, not a finish line. Stretch goal continues: keep growing
your interactivity samples. And keep the loop running: critique, fix, ship.
