# The Incident Log (unlisted)

A daily two-host conversation built from the rogue agent brief, narrated by
the `daily-incident-log` scheduled task. The repo is public only because free
GitHub Pages needs that; the name is random and the page carries noindex.
Treat the feed URL as a secret.

This repo holds data only: `show.json`, `episodes.json`, `feed.xml`, covers
and audio. The task publishes with the shared kit (`podcast-kit`). The one
workflow, `pages-retry`, re-runs a failed or timed-out Pages deploy up to
twice (3 attempts in all) unless a newer push has superseded it. If the
deploy still does not go out, it opens an issue titled "Pages deploy failed
after retries" with the episode/commit, the run link and each attempt's
result, or comments on that issue if one is already open. If the retry job
is killed or cancelled before it can post that (for example at its time
limit), a second job posts a shorter alert to the same issue. Close the issue
once the episode is live.
