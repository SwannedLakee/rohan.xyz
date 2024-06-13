# rohan.xyz

![Initial Page Load Size](https://img.shields.io/badge/page_load-59.2kb-blue) ![JS Minified File Size](https://img.shields.io/badge/js_minified_size-8.6kb-success) ![CSS Minified File Size](https://img.shields.io/badge/css_minified_size-6.5kb-success) ![Photos File Size](https://img.shields.io/badge/image_assets-36.2MB-yellow) 

Vanilla javascript and CSS with no 3rd party libraries (except Maps).

The site is designed to be as small as possible so it will load quickly and smoothly on even the shittiest internet connections. You only download **60kb** of data on page load (yes, including fonts).

Using [MapboxGL JS](https://www.mapbox.com/) to display some shmancy vector maps with my Strava data for "fun" visualisations of my one and only hobby.

---

### Build
Server
````
python3 -m http.server
````

Styles  
````
sass --watch scss/main.scss:css/style.min.css --style compressed
````

Scripts
````
terser js/photos.js js/map.js js/bucket.js js/script.js --source-map -m -o js/script.terser.js
````



### Color List
<div align="center">
	<img src="https://raw.githubusercontent.com/rohanb10/rohan.xyz/gh-pages/assets/color-list.png" alt="color list">
</div>

---



### Resources
Things I used during the development process.
 - [svgo-cli](https://github.com/svg/svgo) - svg optimisation
 - [sqip](https://github.com/axe312ger/sqip#CLI) - svg based polygonal placeholders for photos
 - [Clippy](https://bennettfeely.com/clippy/) - CSS `clip-path` playground
 - Rides scraped via the [Strava API](https://developers.strava.com).
 - Encoded polyline [algorithm](https://developers.google.com/maps/documentation/utilities/polylinealgorithm) to reduce size of all coordinates by over 95%.
 - [Sqoosh](https://squoosh.app/) - A better png compressor to strip unused colours out of images
 - [Easings](https://easings.net/en)

SASS source files in the `scss` directory. All JS files in the `js` directory, then combined and minified for production.

Map related functions are in `js/maps.js` but the request to get latest versions of MapboxGL from the CDN is in `js/scriptj.s`.
