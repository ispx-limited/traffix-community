# traffix-community

traffix tells ISPs which large downloads are coming: game releases, game
updates, preload windows and platform updates such as console firmware and
operating system releases, each with its size, date, platforms and an
impact score. The site is https://traffix.ispx.co.

This repository is the public side of it.

## Propose an event or a correction

Open an issue from one of the two templates. Every proposal, whether raised
by a person or by the traffix research worker, becomes an issue here, with
the evidence behind it in the body.

Review works like this:

1. The traffix worker checks the claims against the sources on its next
   nightly run and comments what it found.
2. A proposal whose date comes from the publisher or store, whose size
   has a good source, whose quotes are found on the pages they cite, and
   which passes every check, is published on its evidence.
3. Anything less waits for an owner, who decides with a comment:
   `/approve` publishes the event, `/deny <reason>` closes it, and
   `/edit field=value ...` corrects fields before an `/approve`.
4. The issue is closed with a link to the published event.

Reactions and comments from anyone else are welcome as signals and are read
during review. They do not approve anything.

See [CONTRIBUTING.md](CONTRIBUTING.md) for what makes a good proposal.

## The dataset

`data/events.json` is every published event, exported by traffix after
each decision. It is generated: pull requests against it are closed with a
pointer to the issue templates. The file's shape is described in
[data/README.md](data/README.md).

## The API and the feeds

- JSON API: needs a key. The site's `/api` page says how to ask for one,
  and https://traffix.ispx.co/docs is the reference. The same key also
  works on a sandbox with fictional data, for building an integration.
- Calendar: https://traffix.ispx.co/feeds/events.ics
- RSS: https://traffix.ispx.co/feeds/events.rss

## Limitations

- A proposal that does not meet the evidence bar waits for an owner to
  review it, usually the following evening.
- The worker runs once a night. An event announced in the morning appears
  the next day at the earliest.
- Publishers move dates. Published events are re-checked as their date
  nears, and corrections are raised when they move, but a date is a date
  until the download starts.
- Sizes are what the publisher or store page states before release, which
  is often the installed size rather than the download.
