# evilfactorylabs.org

This website is built with Sapper, a framework for building web applications of all sizes,
with a beautiful development experience and flexible filesystem-based routing.

Unlike single-page apps, Sapper doesn't compromise on SEO, progressive enhancement or the
initial load experience — but unlike traditional server-rendered apps, navigation
is instantaneous for that app-like feel.

Basically I don't care with any SEO-related things, I use Sapper over Svelte was for flexibility
sake on filesystem-based routing.

## Getting started

Ah, here we go again.

1. Clone this repo
2. Run `yarn`
3. Take S2 program
4. Does yarn install still running? If yes, take PhD program
5. If not, run `yarn dev`

Anyone here still using `npm` over `yarn`?

## Directory Structures

All routes are lives in `src/routes` directory. I use common (read: boring) naming conventions
in naming directory and file. So you should be familiar.

## Development Environment

Currently Sapper doesn't support Hot Reload, poor you. Also, `serviceWorker` is used even in Development
Environment and I don't know why, in case your changes doesn't affect to what you see on your screen, make
sure to refresh your browser twice.

Or three times. Or four.

## Production Environment

This site is should be _statically generated_ so you need to run `yarn export` than `yarn build`. Also, this site
probably will be deployed to Netflify. Or Zeit Now? Or Docker? Or to my kubernetes clusters? Who knows?

## License

MIT. Why not.
