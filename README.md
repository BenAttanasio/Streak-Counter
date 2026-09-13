# Streak Counter

Pick a date and this counts up from it, live, down to the second. It shows the
elapsed time broken into years, months, weeks, days, hours, minutes, and seconds,
plus the last milestone you passed and the next one coming.

One HTML file, around 20 KB, no build step and no dependencies. Open it and it
works.

Try it at [benattanasio.com/lab/streak-counter](https://benattanasio.com/lab/streak-counter).

## The date is in the URL

Your date is stored in the URL hash, so `#2026-01-14` is the whole state. Nothing
is written to `localStorage` and nothing is sent anywhere.

That means you can bookmark a counter, keep several open in different tabs, and
send one to somebody by pasting the link. It also means clearing your browser data
doesn't lose anything, since there's nothing stored to lose.

## Milestones

Thirteen of them, from one day to five years:

1 day, 3 days, 1 week, 2 weeks, 3 weeks, 1 month, 2 months, 3 months, 6 months,
1 year, 2 years, 3 years, 5 years.

The card shows the one you last passed and the one you're heading for, with a
progress bar between them. Edit `MILESTONES` near the top of the script to change
the ladder.

## How the units are calculated

The breakdown uses average lengths: 30.44 days to a month and 365.25 days to a
year. So a counter reading "3 months" is 91 days and change, and it won't line up
exactly with the same date three calendar months later.

Calendar-exact months would drift the other way, where February makes a
"one month" bar shorter than a January one, and the bars stop being comparable.
Averages keep the bar widths honest, which is what the display is for.

## Running it locally

Open `index.html`. There's nothing to install.

## License

MIT. See [LICENSE](LICENSE).

More at [benattanasio.com/lab](https://benattanasio.com/lab).
