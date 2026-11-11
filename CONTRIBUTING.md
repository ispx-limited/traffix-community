# Contributing

## What is wanted

- An upcoming game release, game update, preload or platform update with
  a source: the publisher's page, the store page, SteamDB, platform news.
- A correction to a published event, with a source for the correct value.

## What is not

- Rumours without a publisher or store page behind them. A leak can be
  mentioned in the notes of a proposal that has a real source, not raised
  on its own.
- Events already published. Check the site first; raise a correction
  instead.

## Filling the templates

- **Title** is the game or platform name as the publisher writes it.
- **Kind** is one of Game release, Game update, Preload, Platform update.
- **Name** is the update or patch name when there is one; leave it empty
  for a release.
- **Platforms** use this vocabulary: pc, playstation, xbox, switch,
  windows, macos, ios, android, linux. Generations are not separated: a
  PS4 and PS5 release is `playstation`.
- **Date** is `YYYY-MM-DD` in UTC. If the publisher gives an hour, put it
  in the notes.
- **Size** is gigabytes, as a number. If the size differs per platform,
  give the largest and list the others in the notes.
- **Source URLs**, one per line. The first should be the page that states
  the date; a second that states the size helps.

Issue forms are parsed by the product, so keep the headings as the
template renders them and put free text in Notes.

## Code

There is no code here. The dataset is generated and the templates are the
interface; a change to a template is a pull request like any other.
