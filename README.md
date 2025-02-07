This is the source code for the website that is displayed at
[rullypratama.com][]. The source is processed using [Jekyll][].

[rullypratama.com]: https://rullypratama.com
[Jekyll]: http://jekyllrb.com

## Installing dependencies

There are Python, Ruby, and Node dependencies. Using [bundler][]'s `bundle
install` should give you everything you need on the Ruby side, whereas `pip
install -r requirements.txt` should give you all of the Python dependencies.
For node, `npm install purgecss`.

[bundler]: http://bundler.io/

## Deployment

Deployment to S3 and CloudFront invalidation can be done by running `rake
deploy`.

## Stripped fonts

I use a small subset of [Font Awesome][] to provide link icons in the header.
These are stripped using [Fontello][] to only the icons used to minimise
transmission and load time.

I also use two other fonts from [Google Fonts][]: [Open Sans][] and [Droid Sans
Mono][]. These are stored locally in WOFF2.

[Font Awesome]: http://fortawesome.github.io/Font-Awesome/
[Fontello]: http://fontello.com
[Google Fonts]: https://www.google.com/fonts
[Open Sans]: http://www.google.com/fonts/specimen/Open+Sans
[Droid Sans Mono]: http://www.google.com/fonts/specimen/Droid+Sans+Mono

## License

Since this repository contains part code and part content, the contents is
split between two licenses, as appropriate for each medium. The code portion is
[ISC licensed][isc], but the content is licensed under a [Creative Commons
Attribution 4.0][cc] license. There are other included files in this project
that are copyrighted by entities other than myself that use other licenses,
too. See the LICENSE file for full details.

[isc]: http://en.wikipedia.org/wiki/ISC_license
[cc]: http://creativecommons.org/licenses/by/4.0/
