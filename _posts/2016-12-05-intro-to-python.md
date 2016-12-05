---
layout: post
title: "Intro to Python Tutorial"
date: 2016-10-24
---
<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />
<title>Intro_to_Python</title>

<script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>

<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.6 (http://getbootstrap.com)
 * Copyright 2011-2015 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    color: #000 !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: thin dotted;
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: thin dotted;
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: thin dotted;
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.2.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.2.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.2.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.2.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.2.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.2.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=1);
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2);
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=3);
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1);
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1);
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
@media (max-width: 991px) {
  #ipython_notebook {
    margin-left: 10px;
  }
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#login_widget {
  float: right;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  text-align: center;
  vertical-align: middle;
  display: inline;
  opacity: 0;
  z-index: 2;
  width: 12ex;
  margin-right: -12ex;
}
.alternate_upload .btn-upload {
  height: 22px;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
ul#tabs {
  margin-bottom: 4px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: baseline;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
#tree-selector {
  padding-right: 0px;
}
#button-select-all {
  min-width: 50px;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI colors. */
.ansibold {
  font-weight: bold;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  border-left-width: 1px;
  padding-left: 5px;
  background: linear-gradient(to right, transparent -40px, transparent 1px, transparent 1px, transparent 100%);
}
div.cell.jupyter-soft-selected {
  border-left-color: #90CAF9;
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected {
  border-color: #ababab;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 5px, transparent 5px, transparent 100%);
}
@media print {
  div.cell.selected {
    border-color: transparent;
  }
}
div.cell.selected.jupyter-soft-selected {
  border-left-width: 0;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 7px, #E3F2FD 7px, #E3F2FD 100%);
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #66BB6A -40px, #66BB6A 5px, transparent 5px, transparent 100%);
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
@-moz-document url-prefix() {
  div.inner_cell {
    overflow-x: hidden;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  padding: 0.4em;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. We need the 0 value because of how we size */
  /* .CodeMirror-lines */
  padding: 0;
  border: 0;
  border-radius: 0;
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul {
  list-style: disc;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ul ul {
  list-style: square;
  margin: 0em 2em;
}
.rendered_html ul ul ul {
  list-style: circle;
  margin: 0em 2em;
}
.rendered_html ol {
  list-style: decimal;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
  margin: 0em 2em;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  background-color: #fff;
  color: #000;
  font-size: 100%;
  padding: 0px;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: 1px solid black;
  border-collapse: collapse;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  border: 1px solid black;
  border-collapse: collapse;
  margin: 1em 2em;
}
.rendered_html td,
.rendered_html th {
  text-align: left;
  vertical-align: middle;
  padding: 4px;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget {
  float: right !important;
  float: right;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 20ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  margin-top: 6px;
}
span.save_widget span.filename {
  height: 1em;
  line-height: 1em;
  padding: 3px;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  display: none;
}
.command-shortcut:before {
  content: "(command)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>
<style type="text/css">
    
/* Temporary definitions which will become obsolete with Notebook release 5.0 */
.ansi-black-fg { color: #3E424D; }
.ansi-black-bg { background-color: #3E424D; }
.ansi-black-intense-fg { color: #282C36; }
.ansi-black-intense-bg { background-color: #282C36; }
.ansi-red-fg { color: #E75C58; }
.ansi-red-bg { background-color: #E75C58; }
.ansi-red-intense-fg { color: #B22B31; }
.ansi-red-intense-bg { background-color: #B22B31; }
.ansi-green-fg { color: #00A250; }
.ansi-green-bg { background-color: #00A250; }
.ansi-green-intense-fg { color: #007427; }
.ansi-green-intense-bg { background-color: #007427; }
.ansi-yellow-fg { color: #DDB62B; }
.ansi-yellow-bg { background-color: #DDB62B; }
.ansi-yellow-intense-fg { color: #B27D12; }
.ansi-yellow-intense-bg { background-color: #B27D12; }
.ansi-blue-fg { color: #208FFB; }
.ansi-blue-bg { background-color: #208FFB; }
.ansi-blue-intense-fg { color: #0065CA; }
.ansi-blue-intense-bg { background-color: #0065CA; }
.ansi-magenta-fg { color: #D160C4; }
.ansi-magenta-bg { background-color: #D160C4; }
.ansi-magenta-intense-fg { color: #A03196; }
.ansi-magenta-intense-bg { background-color: #A03196; }
.ansi-cyan-fg { color: #60C6C8; }
.ansi-cyan-bg { background-color: #60C6C8; }
.ansi-cyan-intense-fg { color: #258F8F; }
.ansi-cyan-intense-bg { background-color: #258F8F; }
.ansi-white-fg { color: #C5C1B4; }
.ansi-white-bg { background-color: #C5C1B4; }
.ansi-white-intense-fg { color: #A1A6B2; }
.ansi-white-intense-bg { background-color: #A1A6B2; }

.ansi-bold { font-weight: bold; }

    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}

@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Intro-to-Python-Programming">Intro to Python Programming<a class="anchor-link" href="#Intro-to-Python-Programming">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Why-Python?">Why Python?<a class="anchor-link" href="#Why-Python?">&#182;</a></h1><ul>
<li>It's a full and general purpose programming language.</li>
<li>Clean and elegant, easy to learn and be productive.</li>
<li>It's free and open source (you can always know exactly what your code is doing)!</li>
<li>Huge community.</li>
<li>Very popular for scientific programming and data science.</li>
</ul>
<p>Projects using Python:</p>
<ul>
<li>YouTube</li>
<li>Google</li>
<li>NASA</li>
<li>Dropbox</li>
<li>Many more.</li>
</ul>
<h1 id="Workshop-Objectives">Workshop Objectives<a class="anchor-link" href="#Workshop-Objectives">&#182;</a></h1><ul>
<li>To give you the essential Python tools so that you can start to apply it to help you in your own work or research!</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Programming-Basics">Programming Basics<a class="anchor-link" href="#Programming-Basics">&#182;</a></h1><p>We can boil down programming into two main 'entities': Data and Operations. In a program, we have some information, or data, and we perform some operations on it to produce the desired output. So let's see how these two are represented in Python.</p>
<h2 id="Data">Data<a class="anchor-link" href="#Data">&#182;</a></h2><p>As you can imagine, data can come in several forms and be packaged in many ways. The fundamental Python data types that we will cover here are the following: integers, floats, booleans, and strings. We can store the values of these different types in what we call 'variables'. You can just think of them as containers with a name (no spaces or special characters!) that have a piece of data. Below are some examples of how we can work with these data types.</p>
<h3 id="Primitives">Primitives<a class="anchor-link" href="#Primitives">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[49]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># this is a comment. anything that follows a &#39;#&#39; symbol in Python is ignored by the interpeter</span>

<span class="c1"># here are two ways we can represent numbers</span>

<span class="c1">#integers a.k.a int</span>
<span class="n">x</span> <span class="o">=</span> <span class="mi">4</span>  <span class="c1">#here we store the integer value of 4 in the variable x</span>
<span class="n">y</span> <span class="o">=</span> <span class="mi">2</span>

<span class="c1">#floating point numbers </span>
<span class="n">a</span> <span class="o">=</span> <span class="mf">0.5</span>
<span class="n">b</span> <span class="o">=</span> <span class="mf">0.1</span>

<span class="c1"># strings are sequences of characters. they are always contained in single or double quotes</span>
<span class="n">s</span> <span class="o">=</span> <span class="s2">&quot;Hello, world.&quot;</span>

<span class="c1">#booleans are data types that can take on only the values &#39;True&#39; or &#39;False&#39;:</span>

<span class="n">n</span> <span class="o">=</span> <span class="kc">False</span>
<span class="n">m</span>  <span class="o">=</span> <span class="kc">True</span>

<span class="c1">#finally, we have the &#39;None&#39; type which is basically nothing, it&#39;s like an empty variable</span>

<span class="n">t</span> <span class="o">=</span> <span class="kc">None</span>

<span class="c1">## so now what we&#39;ve done is store some values in some variables. how can we see what those values are? print!</span>

<span class="nb">print</span><span class="p">(</span><span class="n">x</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">y</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">a</span><span class="p">,</span> <span class="n">b</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">s</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">n</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">m</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">t</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>4
2
0.5 0.1
Hello, world.
False
True
None
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[14]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#another useful thing is type-casting where we can convert some types into other types.</span>

<span class="n">x</span> <span class="o">=</span> <span class="mf">5.0</span>
<span class="n">y</span> <span class="o">=</span> <span class="s2">&quot;5.0&quot;</span>

<span class="c1">#converts a floating point number to an integer</span>
<span class="nb">print</span><span class="p">(</span><span class="nb">int</span><span class="p">(</span><span class="n">x</span><span class="p">))</span>

<span class="c1">#converts the string &quot;5.0&quot; into a numeric value</span>
<span class="nb">print</span><span class="p">(</span><span class="nb">float</span><span class="p">(</span><span class="n">x</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>5
5.0
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[38]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># we can do some basic operations on these data types</span>

<span class="nb">print</span><span class="p">(</span><span class="mi">4</span> <span class="o">+</span> <span class="mi">4</span><span class="p">)</span>  <span class="c1">#add or subtract two integers</span>
<span class="nb">print</span><span class="p">(</span><span class="mi">4</span><span class="o">/</span><span class="mi">5</span><span class="p">)</span>    <span class="c1"># divide</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>8
0.8
5
Hello, world. How are you?
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[39]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># we can assign the value of a variable back to itself.</span>

<span class="n">x</span> <span class="o">=</span> <span class="n">x</span> <span class="o">+</span> <span class="mi">1</span>
<span class="nb">print</span><span class="p">(</span><span class="n">x</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>6
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[40]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#we can &#39;concatenate&#39; two strings</span>

<span class="nb">print</span><span class="p">(</span><span class="n">s</span> <span class="o">+</span> <span class="s2">&quot; How are you?&quot;</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>Hello, world. How are you?
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Data-structures">Data structures<a class="anchor-link" href="#Data-structures">&#182;</a></h3><p>Now that we have a better idea of the types of information Python handles. We would like to scale things up and be able to store the data in a way as to be able to easily handle many values at once.</p>
<h4 id="Lists">Lists<a class="anchor-link" href="#Lists">&#182;</a></h4><p>A list is simply an ordered collection of values.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[16]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># This is a list:</span>
<span class="n">l</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>
<span class="c1"># we can access each element in a list with its index (starting from 0)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">l</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">l</span><span class="p">[</span><span class="mi">0</span><span class="p">])</span> <span class="c1">#prints the first element in the list</span>
<span class="nb">print</span><span class="p">(</span><span class="n">l</span><span class="p">[</span><span class="mi">1</span><span class="p">])</span> <span class="c1">#prints the second element in the list</span>
<span class="nb">print</span><span class="p">(</span><span class="n">l</span><span class="p">[</span><span class="o">-</span><span class="mi">1</span><span class="p">])</span> <span class="c1">#what does this print?</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>[1, 2, 3, 4]
1
2
4
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[20]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#list slicing. very useful way in python to access sub-lists in python</span>

<span class="c1">#say we want to make a list that only has the elements between positions 2 and 4 in list l</span>

<span class="n">sliced</span> <span class="o">=</span> <span class="n">l</span><span class="p">[</span><span class="mi">2</span><span class="p">:</span><span class="mi">4</span><span class="p">]</span>

<span class="nb">print</span><span class="p">(</span><span class="n">sliced</span><span class="p">)</span>

<span class="c1">#now say we want a list that contains everything but the first number in l</span>

<span class="n">everything_but_first</span> <span class="o">=</span> <span class="n">l</span><span class="p">[</span><span class="mi">1</span><span class="p">:]</span>

<span class="nb">print</span><span class="p">(</span><span class="n">everything_but_first</span><span class="p">)</span>

<span class="c1">#now make a list that has everything except the last element in the list (remember the -1 index)</span>

<span class="n">everything_but_last</span> <span class="o">=</span> <span class="n">l</span><span class="p">[:</span><span class="o">-</span><span class="mi">1</span><span class="p">]</span>
<span class="nb">print</span><span class="p">(</span><span class="n">everything_but_last</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>[3, 4]
[2, 3, 4]
[1, 2, 3]
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[11]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#we can modify the values in the list</span>
<span class="n">l</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">=</span> <span class="mi">3000</span>
<span class="nb">print</span><span class="p">(</span><span class="n">l</span><span class="p">[</span><span class="mi">1</span><span class="p">])</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>3000
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[12]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#we can add values to the end of the list with the append() function</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;adding a value&quot;</span><span class="p">)</span>
<span class="n">l</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="s2">&quot;hi!&quot;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">l</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>adding a value
[1, 3000, 3, 4, &#39;hi!&#39;]
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Tuples">Tuples<a class="anchor-link" href="#Tuples">&#182;</a></h4><p>Tuples are like lists, but they are less flexible. Unlike lists, they have a fixed size, and you can't reassign elements to them once they're assigned. The advantage is that they are more memory efficient than lists. So it's good to use them when you know that you will not be changing your data around much.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[18]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#declare a tuple. use round brackets instead of square brackets</span>
<span class="n">person</span> <span class="o">=</span> <span class="p">(</span><span class="s1">&#39;Martin&#39;</span><span class="p">,</span> <span class="mi">50</span><span class="p">,</span> <span class="mf">1.65</span><span class="p">)</span> 
<span class="nb">print</span><span class="p">(</span><span class="n">person</span><span class="p">)</span>

<span class="c1">#you can still access its elements just like in a list</span>
<span class="nb">print</span><span class="p">(</span><span class="n">person</span><span class="p">[</span><span class="mi">1</span><span class="p">])</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>(&#39;Martin&#39;, 50, 1.65)
50
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Dictionaries">Dictionaries<a class="anchor-link" href="#Dictionaries">&#182;</a></h4><p>Dictionaries are one of the most useful data structures in Python and because they are very powerful for organizing data. A dictionary is like a list, except every element is indexed by a 'key instead of a number like we saw with lists and tuples.</p>
<p><code>d[key] = value</code></p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[76]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># dictionaries are initialized with curly braces</span>
<span class="n">d</span> <span class="o">=</span> <span class="p">{}</span> <span class="c1"># is an empty dictionary</span>

<span class="c1">#let&#39;s add some keys to the dictionary and give it a value.</span>
<span class="n">d</span><span class="p">[</span><span class="s1">&#39;heights&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="p">[]</span>
<span class="n">d</span><span class="p">[</span><span class="s1">&#39;weights&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="p">[]</span>

<span class="nb">print</span><span class="p">(</span><span class="n">d</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>{&#39;heights&#39;: [], &#39;weights&#39;: []}
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[77]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#now we can add &#39;heights&#39; to the list </span>
<span class="n">d</span><span class="p">[</span><span class="s1">&#39;heights&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="mf">165.4</span><span class="p">)</span>
<span class="n">d</span><span class="p">[</span><span class="s1">&#39;weights&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="mf">221.2</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="n">d</span><span class="p">)</span>

<span class="c1">#if we want to get the &#39;keys&#39; of the dictionary we use the keys() function</span>

<span class="nb">print</span><span class="p">(</span><span class="n">d</span><span class="o">.</span><span class="n">keys</span><span class="p">())</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>{&#39;heights&#39;: [165.4], &#39;weights&#39;: [221.2]}
dict_keys([&#39;heights&#39;, &#39;weights&#39;])
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Python-is-very-flexible-with-data">Python is very flexible with data<a class="anchor-link" href="#Python-is-very-flexible-with-data">&#182;</a></h3><p>As you may have started to notice, it is possible to store any kind of mixture of data into lists, tuples, and dictionaries. Here are some examples:</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[35]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">mix</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;hi&#39;</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="p">(</span><span class="s1">&#39;a&#39;</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="s1">&#39;e&#39;</span><span class="p">)]</span>
<span class="nb">print</span><span class="p">(</span><span class="n">mix</span><span class="p">)</span>

<span class="n">d2</span> <span class="o">=</span> <span class="p">{</span><span class="mi">1</span><span class="p">:</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">],</span> <span class="s1">&#39;bob&#39;</span><span class="p">:</span> <span class="mi">4</span><span class="p">}</span>
<span class="nb">print</span><span class="p">(</span><span class="n">d2</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>[&#39;hi&#39;, 1, 2, (&#39;a&#39;, 2, &#39;e&#39;)]
{1: [1, 2, 3], &#39;bob&#39;: 4}
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Operations">Operations<a class="anchor-link" href="#Operations">&#182;</a></h2><p>Now that we have an idea of how Python stores data, we would like to be able to do something interesting with is. That is, peform operations on the data in an efficient manner.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="for-loops"><code>for</code> loops<a class="anchor-link" href="#for-loops">&#182;</a></h3><p>Loops make python repeat a set of commands a given number of times. They are by far the most widely used loop.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[36]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># for loops store the each item in the list in the variable following the &#39;for&#39; one at a time.</span>

<span class="c1">#let&#39;s iterate through that &#39;mix&#39; list that we made in the previous cell and print each item in the list</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">mix</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">i</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>hi
1
2
(&#39;a&#39;, 2, &#39;e&#39;)
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[37]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># we can also iterate through a range of numbers by using the range(n) command which returns a list containing the</span>
<span class="c1"># integers within the specified range</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">):</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">i</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>0
1
2
3
4
5
6
7
8
9
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[47]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#write a for loop that adds the numbers from 1 to n. declare any variables you may need</span>

<span class="n">n</span> <span class="o">=</span> <span class="mi">4</span>
<span class="n">total</span> <span class="o">=</span> <span class="mi">0</span>

<span class="c1">#the loop will repeat whatever is under it and indented to the right</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="n">n</span><span class="p">):</span>
    <span class="n">total</span> <span class="o">=</span> <span class="n">total</span> <span class="o">+</span> <span class="n">i</span>
    
<span class="nb">print</span><span class="p">(</span><span class="n">total</span><span class="p">)</span>   
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>6
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="if-statements"><code>if</code> statements<a class="anchor-link" href="#if-statements">&#182;</a></h3><p><code>if</code> statements allow us to control which parts of code are executed depending on a condition. This condition is expressed as a boolean that can be <code>True</code> or <code>False</code>. If the statement is <code>True</code> then the code contained in the <code>if</code> statement will execute. Otherwise, it gets skipped.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[48]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#first, a bit more about booleans. we can compare two booleans using the &#39;==&#39; operator to obtain a &#39;True&#39; if they are</span>
<span class="c1"># equal and &#39;False&#39; if they are not equal.</span>

<span class="nb">print</span><span class="p">(</span><span class="kc">True</span> <span class="o">==</span> <span class="kc">True</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="kc">True</span> <span class="o">==</span> <span class="kc">False</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>True
False
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[53]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># We can perform some operations on boolean variables to better express conditions</span>

<span class="c1">#the &#39;and&#39; operation gives a True boolean if both elements are true</span>
<span class="n">a</span><span class="p">,</span><span class="n">b</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span> <span class="kc">True</span>
<span class="nb">print</span><span class="p">(</span><span class="n">a</span> <span class="ow">and</span> <span class="n">b</span><span class="p">)</span>

<span class="n">a</span><span class="p">,</span><span class="n">b</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span> <span class="kc">False</span>
<span class="nb">print</span><span class="p">(</span><span class="n">a</span> <span class="ow">and</span> <span class="n">b</span><span class="p">)</span>


<span class="c1"># the &#39;or&#39; operator gives True if either one (or both) of the elements is true</span>
<span class="nb">print</span><span class="p">(</span><span class="n">a</span> <span class="ow">or</span> <span class="n">b</span><span class="p">)</span>

<span class="c1"># the &#39;not&#39; operator simply gives you the opposite of the given element</span>
<span class="nb">print</span><span class="p">(</span><span class="ow">not</span> <span class="n">a</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>True
False
True
False
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[55]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">feel_like_it</span> <span class="o">=</span> <span class="kc">True</span>
<span class="n">raining</span> <span class="o">=</span> <span class="kc">False</span>
<span class="n">date_tonight</span> <span class="o">=</span> <span class="kc">True</span>


<span class="c1">#write a boolean to decide if you should go to the gym based on the three booleans above.</span>
<span class="n">go_to_gym</span> <span class="o">=</span> <span class="p">(</span><span class="n">feel_like_it</span> <span class="ow">and</span> <span class="ow">not</span> <span class="n">raining</span><span class="p">)</span> <span class="ow">or</span> <span class="n">date_tonight</span>

<span class="nb">print</span><span class="p">(</span><span class="n">go_to_gym</span><span class="p">)</span>

<span class="c1">#play around with different values of the variables!</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>True
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>We can use <code>if</code> statements to make our loops more powerful</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#write a for loop that prints every even number up until n. (hint. use the modulo operator which returns the </span>
<span class="c1"># remainder of dividing two numbers. e.g. 5 % 2 = 3, 10%2 = 0)</span>

<span class="n">n</span> <span class="o">=</span> <span class="mi">25</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="n">n</span><span class="p">):</span>
    <span class="k">if</span> <span class="n">i</span> <span class="o">%</span> <span class="mi">2</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="n">i</span><span class="p">)</span>
    <span class="k">else</span><span class="p">:</span>
        <span class="k">continue</span> <span class="c1">#the &#39;continue&#39; statement lets you skip to the next iteration in the loop</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Now we can use these booleans to control how our code gets executed. Here's an example:</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[61]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">if</span> <span class="n">feel_like_it</span> <span class="ow">and</span> <span class="n">raining</span><span class="p">:</span> <span class="c1">#whatever follows the if has to be a boolean statement</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;i feel like it, but it&#39;s raining&quot;</span><span class="p">)</span>
<span class="c1">#if the previous clause is not met, the &#39;elif&#39; or &#39;else if&#39; block is checked</span>
<span class="k">elif</span> <span class="n">date_tonight</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;i have a date tonight&quot;</span>
<span class="c1">#if neither the if or the elif match then we go into the &#39;else&#39;</span>
<span class="k">else</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;i should just stay home&quot;</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>i have a date tonight
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Try an example for yourself. This is a famous programming challenge to test <code>if</code> statements, known as the 'fizzbuzz' test. You have to print the numbers from 0 to 50 following three rules:</p>
<ul>
<li>If the number is divisible by 3, print 'fizz'</li>
<li>If the number is divisible by 5, print 'buzz'</li>
<li>If the number is divisible by both 3 and 5, pring 'fizzbuzz'</li>
<li>Otherwise, print the number.</li>
</ul>
<p>There are many different ways to do this, so take a couple of minutes to come up with yours. (hint. use the <code>%</code> operator).</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">100</span><span class="p">):</span>
    <span class="k">if</span> <span class="n">i</span> <span class="o">%</span> <span class="mi">15</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;fizzbuzz&quot;</span><span class="p">)</span>
    <span class="k">elif</span> <span class="n">i</span> <span class="o">%</span> <span class="mi">3</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;fizz&quot;</span><span class="p">)</span>
    <span class="k">elif</span> <span class="n">i</span> <span class="o">%</span> <span class="mi">5</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;buzz&quot;</span><span class="p">)</span>
    <span class="k">else</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="n">i</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>fizzbuzz
1
2
fizz
4
buzz
fizz
7
8
fizz
buzz
11
fizz
13
14
fizzbuzz
16
17
fizz
19
buzz
fizz
22
23
fizz
buzz
26
fizz
28
29
fizzbuzz
31
32
fizz
34
buzz
fizz
37
38
fizz
buzz
41
fizz
43
44
fizzbuzz
46
47
fizz
49
buzz
fizz
52
53
fizz
buzz
56
fizz
58
59
fizzbuzz
61
62
fizz
64
buzz
fizz
67
68
fizz
buzz
71
fizz
73
74
fizzbuzz
76
77
fizz
79
buzz
fizz
82
83
fizz
buzz
86
fizz
88
89
fizzbuzz
91
92
fizz
94
buzz
fizz
97
98
fizz
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="List-comprehensions">List comprehensions<a class="anchor-link" href="#List-comprehensions">&#182;</a></h3><p>List comprehensions are a very nice Python feature that allow you to make lists in a single line. Let's see how they work.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># this will grow a list where each element in the list is whatever the statement preceding the &#39;for&#39; evaluates to</span>
<span class="n">numbers_times_two</span> <span class="o">=</span> <span class="p">[</span><span class="n">n</span><span class="o">*</span><span class="mi">2</span> <span class="k">for</span> <span class="n">n</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">)]</span> 
<span class="nb">print</span><span class="p">(</span><span class="n">numbers_time_two</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># we can also add if statements in the list comprehension</span>
<span class="n">odd_numbers</span> <span class="o">=</span> <span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">)</span> <span class="k">if</span> <span class="n">i</span> <span class="o">%</span> <span class="mi">2</span> <span class="o">!=</span> <span class="mi">0</span><span class="p">]</span>
<span class="nb">print</span><span class="p">(</span><span class="n">odd_numbers</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#now try one yourself. make a list comprehension where each item is a tuple (number, number*number) </span>
<span class="n">square_tuples</span> <span class="o">=</span> <span class="p">[(</span><span class="n">i</span><span class="p">,</span> <span class="n">i</span><span class="o">*</span><span class="n">i</span><span class="p">)</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">)]</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Functions">Functions<a class="anchor-link" href="#Functions">&#182;</a></h2><p>That day of the week function was super useful! Let's say we want to use that code again many times, but sometimes we want it to find a different day of the week. We would have to change our if statement each time and re-run the code. This seems like a bit of a pain. Thankfully there is a better way.. functions! Think of a function as a little machine that takes in some input and does something to it and returns some output. So let's turn the days of the week finder into a function.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[69]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#the first line of every function is a header. headers have 3 parts. the &#39;def&#39; keyword which tells python you are</span>
<span class="c1">#about to declare a function, then the name of the function, and finally the inputs to the function</span>

<span class="k">def</span> <span class="nf">day_finder</span><span class="p">(</span><span class="n">day_to_find</span><span class="p">):</span>
    <span class="n">days_of_week</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;Monday&#39;</span><span class="p">,</span> <span class="s1">&#39;Tuesday&#39;</span><span class="p">,</span> <span class="s1">&#39;Wednesday&#39;</span><span class="p">,</span> <span class="s1">&#39;Thursday&#39;</span><span class="p">,</span> <span class="s1">&#39;Friday&#39;</span><span class="p">,</span> <span class="s1">&#39;Satuday&#39;</span><span class="p">,</span> <span class="s1">&#39;Sunday&#39;</span><span class="p">]</span>
    <span class="k">for</span> <span class="n">day</span> <span class="ow">in</span> <span class="n">days_of_week</span><span class="p">:</span>
        <span class="k">if</span> <span class="n">day</span> <span class="o">==</span> <span class="n">day_to_find</span><span class="p">:</span>
            <span class="c1">#the return statement ends every function and it &#39;sends&#39; the output of your function to whoever called it</span>
            <span class="k">return</span> <span class="s2">&quot;Thank God it&#39;s </span><span class="si">%s</span><span class="s2">.&quot;</span> <span class="o">%</span> <span class="p">(</span><span class="n">day</span><span class="p">)</span> <span class="c1"># the %s in the string is like a placeholder that gets filled with</span>
                                                <span class="c1"># the value of the string variable &#39;day&#39;</span>
        <span class="k">else</span><span class="p">:</span>
            <span class="k">continue</span>
    
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[70]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#you can call any function just by typing its name and the arguments you want it to work on in braces ()</span>
<span class="nb">print</span><span class="p">(</span><span class="n">day_finder</span><span class="p">(</span><span class="s1">&#39;Tuesday&#39;</span><span class="p">))</span> <span class="c1">#&quot;thank god it&#39;s tuesday&quot; is the return value of the function day_finder()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>Thank God it&#39;s Tuesday
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="A-word-on-'variable-scope'">A word on 'variable scope'<a class="anchor-link" href="#A-word-on-'variable-scope'">&#182;</a></h3><p>As you may have noticed, it would be a mess if variables were accessible from everywhere in the code. In fact, in Python, anything that is defined within an 'indentation block' is shared but not otherwise.</p>
<p>Example:</p>

<pre><code>a = 3

def fun():
    b  = 3
    for i in range(10):
        i = i + 1</code></pre>
<p>In this example <code>a</code> can be accessed from anywhere in the code. <code>b</code> can only be seen inside the indentation block started by <code>fun()</code> and <code>i</code> can only be seen within the indentation block defined by the <code>for</code> loop.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Object-Oriented-Programming">Object Oriented Programming<a class="anchor-link" href="#Object-Oriented-Programming">&#182;</a></h2><p>Just how we generalized a piece of code that runs on similar kinds of input and gave it a name with the functions example, we can do the same thing with just about any piece of Python. Objects let us easily work with instances of some kind of <em>thing</em> where each instance might be a little different from the other but still behave according to its type of <em>thing</em>.</p>
<p>Let's illustrate this with our <em>thing</em> being a Recipe. We can have many different types of recipes but we would like to be able to deal with each one in a uniform manner. We therefore define a Recipe as an object that is defined by some 'attributes'</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[78]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># every object is defined in a &#39;class&#39; and classes are declared with the &#39;class&#39; keyword</span>
<span class="k">class</span> <span class="nc">Recipe</span><span class="p">:</span>
    <span class="k">def</span> <span class="nf">__init__</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">n</span><span class="p">,</span> <span class="n">ig</span><span class="p">,</span> <span class="n">ml</span><span class="p">,</span> <span class="n">pt</span><span class="p">):</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">name</span> <span class="o">=</span> <span class="n">n</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">ingredients</span> <span class="o">=</span> <span class="n">ig</span> <span class="c1">#set the ingredients attribute of the object to the value of ig</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">meal</span> <span class="o">=</span> <span class="n">ml</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">prep_time</span> <span class="o">=</span> <span class="n">pt</span>
    
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[79]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#now that we&#39;ve defined what a Recipe should look like, we can nicely store some new recipes. </span>

<span class="c1">#let&#39;s make some recipes</span>

<span class="n">sandwich</span> <span class="o">=</span> <span class="n">Recipe</span><span class="p">(</span><span class="s1">&#39;sandwich&#39;</span><span class="p">,</span> <span class="p">[</span><span class="s1">&#39;ham&#39;</span><span class="p">,</span> <span class="s1">&#39;bread&#39;</span><span class="p">,</span> <span class="s1">&#39;cheese&#39;</span><span class="p">],</span> <span class="s1">&#39;lunch&#39;</span><span class="p">,</span> <span class="mi">10</span><span class="p">)</span>
<span class="n">cake</span> <span class="o">=</span> <span class="n">Recipe</span><span class="p">(</span><span class="s1">&#39;cake&#39;</span><span class="p">,</span> <span class="p">[</span><span class="s1">&#39;flour&#39;</span><span class="p">,</span> <span class="s1">&#39;sugar&#39;</span><span class="p">,</span> <span class="s1">&#39;eggs&#39;</span><span class="p">],</span> <span class="s1">&#39;dessert&#39;</span><span class="p">,</span> <span class="mi">90</span><span class="p">)</span>

<span class="c1">#add two more recipes of your own!</span>


<span class="c1"># now we can very conveniently access some information about our recipes by name. This can be done with the &#39;.&#39; </span>
<span class="c1"># operator that we saw above</span>

<span class="c1">#print the ingredients in the sandwich, and the preparation time of the cake</span>

<span class="nb">print</span><span class="p">(</span><span class="n">sandwich</span><span class="o">.</span><span class="n">ingredients</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="n">cake</span><span class="o">.</span><span class="n">prep_time</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>[&#39;ham&#39;, &#39;bread&#39;, &#39;cheese&#39;]
90
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Let's go even further and make a new object to contain our Recipe objects. Let's call this class <em>Cookbook</em> and it will simply contain a list of Recipe objects. However, it will not only have some data variables, but it will also be able to perform functions.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[102]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">class</span> <span class="nc">Cookbook</span><span class="p">:</span>
    <span class="k">def</span> <span class="nf">__init__</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">r</span><span class="p">):</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">recipes</span> <span class="o">=</span> <span class="n">r</span>
        
    <span class="c1">#functions declared inside a class are called &#39;Class functions&#39; and they act on an object</span>
    <span class="k">def</span> <span class="nf">get_vegetarian</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
        <span class="sd">&quot;&quot;&quot;This function is going to return recipes in the cookbook that do not contain meat.&quot;&quot;&quot;</span>
        <span class="n">meats</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;ham&#39;</span><span class="p">,</span> <span class="s1">&#39;beef&#39;</span><span class="p">,</span> <span class="s1">&#39;chicken&#39;</span><span class="p">,</span> <span class="s1">&#39;fish&#39;</span><span class="p">]</span>
        <span class="n">veg_dishes</span> <span class="o">=</span> <span class="p">[]</span>
        <span class="k">for</span> <span class="n">recipe</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">recipes</span><span class="p">:</span> <span class="c1">#the &#39;self&#39; keyword is used to access the object the function is being called on</span>
            <span class="k">if</span> <span class="n">meats</span> <span class="ow">not</span> <span class="ow">in</span> <span class="n">recipe</span><span class="o">.</span><span class="n">ingredients</span><span class="p">:</span> <span class="c1">#hint: use the &#39;in&#39; operator which returns true if a value is in the </span>
                                                <span class="c1">#given list. e.g.: 5 in [1, 3, 5] returns True.</span>
                <span class="n">veg_dishes</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">recipe</span><span class="p">)</span>
        <span class="k">return</span> <span class="n">veg_dishes</span>
    
    <span class="c1">#write a class function that returns a list of recipes that take under &#39;n&#39; minutes to prepare</span>
    <span class="k">def</span> <span class="nf">preptime</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">n</span><span class="p">):</span>
        <span class="n">recipes</span> <span class="o">=</span> <span class="p">[]</span>
        <span class="k">for</span> <span class="n">recipe</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">recipes</span><span class="p">:</span>
            <span class="k">if</span> <span class="n">recipe</span><span class="o">.</span><span class="n">prep_time</span> <span class="o">&lt;</span> <span class="n">n</span><span class="p">:</span>
                <span class="n">recipes</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">recipe</span><span class="p">)</span>
        <span class="k">return</span> <span class="n">recipes</span>
                
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[94]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># let&#39;s make a cookbook</span>

<span class="c1">#gather some recipes</span>
<span class="n">recipes</span> <span class="o">=</span> <span class="p">[]</span>

<span class="n">recipes</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">Recipe</span><span class="p">(</span><span class="s1">&#39;steak&#39;</span><span class="p">,</span> <span class="p">[</span><span class="s1">&#39;beef&#39;</span><span class="p">,</span> <span class="s1">&#39;butter&#39;</span><span class="p">,</span> <span class="s1">&#39;mashed potatoes&#39;</span><span class="p">],</span> <span class="s1">&#39;main&#39;</span><span class="p">,</span> <span class="mi">120</span><span class="p">))</span>
<span class="n">recipes</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">Recipe</span><span class="p">(</span><span class="s1">&#39;toast&#39;</span><span class="p">,</span> <span class="p">[</span><span class="s1">&#39;nutella&#39;</span><span class="p">,</span> <span class="s1">&#39;bread&#39;</span><span class="p">],</span> <span class="s1">&#39;snack&#39;</span><span class="p">,</span> <span class="mi">5</span><span class="p">))</span>
<span class="n">recipes</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">Recipe</span><span class="p">(</span><span class="s1">&#39;salad&#39;</span><span class="p">,</span> <span class="p">[</span><span class="s1">&#39;lettuce&#39;</span><span class="p">,</span> <span class="s1">&#39;kale&#39;</span><span class="p">,</span> <span class="s1">&#39;tomatoes&#39;</span><span class="p">],</span> <span class="s1">&#39;main&#39;</span><span class="p">,</span> <span class="mi">15</span><span class="p">))</span>
<span class="n">recipes</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">Recipe</span><span class="p">(</span><span class="s1">&#39;chicken parm&#39;</span><span class="p">,</span> <span class="p">[</span><span class="s1">&#39;chicken&#39;</span><span class="p">,</span> <span class="s1">&#39;sauce&#39;</span><span class="p">,</span> <span class="s1">&#39;cheese&#39;</span><span class="p">],</span> <span class="s1">&#39;main&#39;</span><span class="p">,</span> <span class="mi">90</span><span class="p">))</span>
<span class="n">recipes</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">Recipe</span><span class="p">(</span><span class="s1">&#39;brownie&#39;</span><span class="p">,</span> <span class="p">[</span><span class="s1">&#39;chocolate&#39;</span><span class="p">,</span> <span class="s1">&#39;flour&#39;</span><span class="p">,</span> <span class="s1">&#39;eggs&#39;</span><span class="p">],</span> <span class="s1">&#39;dessert&#39;</span><span class="p">,</span> <span class="mi">15</span><span class="p">))</span>

<span class="c1">#put them in a cookbook</span>

<span class="n">cookbook</span> <span class="o">=</span> <span class="n">Cookbook</span><span class="p">(</span><span class="n">recipes</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[100]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#get vegetarian recipes</span>

<span class="nb">print</span><span class="p">(</span><span class="n">cookbook</span><span class="o">.</span><span class="n">get_vegetarian</span><span class="p">())</span>

<span class="c1">#get recipes that take less than 20 minutes to prepare</span>

<span class="nb">print</span><span class="p">(</span><span class="n">cookbook</span><span class="o">.</span><span class="n">preptime</span><span class="p">(</span><span class="mi">20</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>[&lt;__main__.Recipe object at 0x1048ac208&gt;, &lt;__main__.Recipe object at 0x1048ac748&gt;, &lt;__main__.Recipe object at 0x1048ac278&gt;, &lt;__main__.Recipe object at 0x1048ac780&gt;, &lt;__main__.Recipe object at 0x1048ac7b8&gt;]
[&lt;__main__.Recipe object at 0x1048ac748&gt;, &lt;__main__.Recipe object at 0x1048ac278&gt;, &lt;__main__.Recipe object at 0x1048ac7b8&gt;]
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[101]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#oops what is that? because our functions are returning lists of objects we are seeing how the objects are represented</span>
<span class="c1"># when we print them. What you see are addresses in memory where the objects are stored. Let&#39;s print it in a way</span>
<span class="c1"># we can understand</span>


<span class="c1">#print the name and ingredients of recipes that take under 20 minutes to prepare</span>
<span class="n">short_recipes</span> <span class="o">=</span> <span class="n">cookbook</span><span class="o">.</span><span class="n">preptime</span><span class="p">(</span><span class="mi">20</span><span class="p">)</span>

<span class="k">for</span> <span class="n">s</span> <span class="ow">in</span> <span class="n">short_recipes</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">s</span><span class="o">.</span><span class="n">name</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>toast
salad
brownie
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Libraries">Libraries<a class="anchor-link" href="#Libraries">&#182;</a></h1><p>We've now covered most of the basics you need to get up and running. However, one of the nicest things about Python is that it has a fairly extensive 'standard library'. The standard library is a set of functions that come with Python that do a variety of useful things so that you don't have to reinvent the wheel each time you write a program. We've already seen an example with the <code>range()</code> function. I'm going to give some examples of some of the most useful functions in the standard library, but you should always check if what you are trying to do has already been implemented to save you time.</p>
<p>Some functions are directly built-in and some you have to <code>import</code> from a <em>module</em> which is just the name of a Python program whose functions you can use in your code.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Help">Help<a class="anchor-link" href="#Help">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[12]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#help prints what the given function does</span>
<span class="n">help</span><span class="p">(</span><span class="nb">abs</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>Help on built-in function abs in module builtins:

abs(x, /)
    Return the absolute value of the argument.

</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Sets-and-Lists">Sets and Lists<a class="anchor-link" href="#Sets-and-Lists">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#a set is a group of unique items from a list</span>
<span class="n">pop_stars</span> <span class="o">=</span> <span class="p">[</span><span class="s2">&quot;beyonce&quot;</span><span class="p">,</span> <span class="s2">&quot;rihanna&quot;</span><span class="p">,</span> <span class="s2">&quot;lady gaga&quot;</span><span class="p">,</span> <span class="s2">&quot;lady gaga&quot;</span><span class="p">]</span>

<span class="n">hip_hop_stars</span> <span class="o">=</span> <span class="p">[</span><span class="s2">&quot;rihanna&quot;</span><span class="p">,</span> <span class="s2">&quot;nicki minaj&quot;</span><span class="p">,</span> <span class="s2">&quot;lil kim&quot;</span><span class="p">]</span>

<span class="n">pop</span> <span class="o">=</span> <span class="nb">set</span><span class="p">(</span><span class="n">pop_stars</span><span class="p">)</span>

<span class="n">hip_hop</span> <span class="o">=</span> <span class="nb">set</span><span class="p">(</span><span class="n">hip_hop_stars</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="n">pop</span><span class="p">,</span> <span class="n">hip_hop</span><span class="p">)</span>

<span class="c1">#you can perform some set operations. look up the Python set documentation an print the intersection between both sets.</span>

<span class="n">overlap</span> <span class="o">=</span> <span class="n">pop</span><span class="o">.</span><span class="n">intersection</span><span class="p">(</span><span class="n">hip_hop</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="n">overlap</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>{&#39;beyonce&#39;, &#39;lady gaga&#39;, &#39;rihanna&#39;} {&#39;lil kim&#39;, &#39;nicki minaj&#39;, &#39;rihanna&#39;}
{&#39;rihanna&#39;}
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#sort a list</span>

<span class="n">s</span> <span class="o">=</span> <span class="nb">sorted</span><span class="p">([</span><span class="mi">1</span><span class="p">,</span> <span class="mi">5</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">2</span><span class="p">])</span>
<span class="nb">print</span><span class="p">(</span><span class="n">s</span><span class="p">)</span>

<span class="c1">#max and min of a list</span>
<span class="nb">print</span><span class="p">(</span><span class="nb">max</span><span class="p">(</span><span class="n">s</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="nb">min</span><span class="p">(</span><span class="n">s</span><span class="p">))</span>

<span class="c1">#print the sum of a list&#39;s elements</span>

<span class="nb">print</span><span class="p">(</span><span class="nb">sum</span><span class="p">(</span><span class="n">s</span><span class="p">))</span>

<span class="c1">#get length of list</span>

<span class="nb">print</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">s</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>[1, 2, 3, 5]
5
1
11
4
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#write a for loop that iterates through each *index* in s and prints the index</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">s</span><span class="p">)):</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">i</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[27]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#the enumerate() function gives you the item and the index of a list at the same time</span>

<span class="k">for</span> <span class="n">i</span><span class="p">,</span> <span class="n">number</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">hip_hop_stars</span><span class="p">):</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">i</span><span class="p">,</span> <span class="n">number</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>0 rihanna
1 nicki minaj
2 lil kim
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Some-math">Some math<a class="anchor-link" href="#Some-math">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#let&#39;s import some libraries so we can use their functions</span>
<span class="kn">import</span> <span class="nn">math</span> 
<span class="kn">import</span> <span class="nn">random</span>
<span class="c1">#python numerical tools</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[9]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#generate a random floating point number between 0 and 1</span>
<span class="n">ran</span> <span class="o">=</span> <span class="n">random</span><span class="o">.</span><span class="n">random</span><span class="p">()</span>
<span class="nb">print</span><span class="p">(</span><span class="n">ran</span><span class="p">)</span>

<span class="c1">#print a random integer in the given range</span>
<span class="n">random_integer</span> <span class="o">=</span> <span class="n">random</span><span class="o">.</span><span class="n">randint</span><span class="p">(</span><span class="mi">2</span><span class="p">,</span> <span class="mi">100</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">random_integer</span><span class="p">)</span>

<span class="c1">#sample randomly from a list</span>
<span class="nb">print</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">choice</span><span class="p">([</span><span class="s2">&quot;watermelon&quot;</span><span class="p">,</span> <span class="s2">&quot;mango&quot;</span><span class="p">,</span> <span class="s2">&quot;pineapple&quot;</span><span class="p">]))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>0.30930068420811463
6
pineapple
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[40]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#compute e^(n)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">math</span><span class="o">.</span><span class="n">exp</span><span class="p">(</span><span class="mi">10</span><span class="p">))</span>

<span class="c1">#compute x^n</span>
<span class="nb">print</span><span class="p">(</span><span class="n">math</span><span class="o">.</span><span class="n">pow</span><span class="p">(</span><span class="mi">2</span><span class="p">,</span><span class="mi">3</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>22026.465794806718
8.0
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="String-functions">String functions<a class="anchor-link" href="#String-functions">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[11]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># you can remove characters from the end of a string with the strip() function</span>

<span class="n">disney</span> <span class="o">=</span> <span class="s2">&quot;I&#39;m Walt Disney.&quot;</span>

<span class="nb">print</span><span class="p">(</span><span class="n">disney</span><span class="o">.</span><span class="n">strip</span><span class="p">(</span><span class="s2">&quot;.&quot;</span><span class="p">))</span> <span class="c1">#removes the character from the given string</span>

<span class="c1">#the join function inserts characters between elements in a list and joins them into a string</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;-&quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">disney</span><span class="p">))</span>

<span class="c1">#the opposite of join is the split() function which breaks a string up into a list of sub-strings</span>

<span class="nb">print</span><span class="p">(</span><span class="n">disney</span><span class="o">.</span><span class="n">split</span><span class="p">())</span> <span class="c1">#you can also tell split() which characters to break on</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>I&#39;m Walt Disney
I-&#39;-m- -W-a-l-t- -D-i-s-n-e-y-.
[&#34;I&#39;m&#34;, &#39;Walt&#39;, &#39;Disney.&#39;]
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="File-handling">File handling<a class="anchor-link" href="#File-handling">&#182;</a></h3><p>A very important part of dealing with scientific data is handling files containing your data and loading them into your Python scripts. Thankfully Python also makes this very easy.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[63]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#to open a file you just use the open() function along with the &#39;with&#39; context manager (more on this below)</span>

<span class="c1">#the &#39;with&#39; block takes care of opening and closing the file, and giving us the lines of the file to iterate over</span>
<span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="s2">&quot;food.csv&quot;</span><span class="p">,</span> <span class="s2">&quot;r&quot;</span><span class="p">)</span> <span class="k">as</span> <span class="n">food</span><span class="p">:</span> <span class="c1"># the &quot;r&quot; argument tells open() that we want to read the file</span>
    <span class="k">for</span> <span class="n">item</span> <span class="ow">in</span> <span class="n">food</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="n">item</span><span class="o">.</span><span class="n">strip</span><span class="p">(</span><span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">))</span> <span class="c1">#let&#39;s get rid of the linebreak character</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>food_item, price, quantity
bananas, 1.5, 10
cupcakes, 3, 4
skittles, 2, 200
tacos, 2, 100
chips, 1, 2.5
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[64]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#we can also write to a file</span>
<span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="s2">&quot;helloworld.txt&quot;</span><span class="p">,</span> <span class="s2">&quot;w+&quot;</span><span class="p">)</span> <span class="k">as</span> <span class="n">hello</span><span class="p">:</span>
    <span class="n">hello</span><span class="o">.</span><span class="n">write</span><span class="p">(</span><span class="s2">&quot;Hello, world!&quot;</span><span class="p">)</span>
    
<span class="c1">#check to see if the file was created</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Multiprocessing">Multiprocessing<a class="anchor-link" href="#Multiprocessing">&#182;</a></h3><p>Most computers today have multiple processors, meaning you can use these processors simulaneously to make your computations go a lot faster. Default python code is run as a single process. So if you have some work to do that can be split up into independent parts, you can easily implement this with the <code>multiprocessing</code> module in Python.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[84]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">multiprocessing</span>
<span class="kn">import</span> <span class="nn">time</span> <span class="c1">#this module allows us to do some operations involving time.</span>

<span class="n">MAX_PROC</span> <span class="o">=</span> <span class="mi">4</span>

<span class="k">def</span> <span class="nf">square</span><span class="p">(</span><span class="n">x</span><span class="p">):</span>
    <span class="n">time</span><span class="o">.</span><span class="n">sleep</span><span class="p">(</span><span class="mi">3</span><span class="p">)</span> <span class="c1">#let&#39;s make it a bit slower by making python sleep for 10 seconds before returning the output</span>
    <span class="k">return</span> <span class="n">x</span><span class="o">*</span><span class="n">x</span>

<span class="n">to_do</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">5</span><span class="p">,</span> <span class="mi">6</span><span class="p">,</span> <span class="mi">7</span><span class="p">,</span> <span class="mi">8</span><span class="p">]</span>

<span class="c1">#let&#39;s write a loop that squares each element in that list in series</span>

<span class="c1">#record the time at which we start the computation</span>
<span class="n">t_start_serial</span> <span class="o">=</span> <span class="n">time</span><span class="o">.</span><span class="n">time</span><span class="p">()</span> 

<span class="n">squared_serial</span> <span class="o">=</span> <span class="p">[]</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">to_do</span><span class="p">:</span>
    <span class="n">squared</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">square</span><span class="p">(</span><span class="n">i</span><span class="p">))</span>

<span class="c1">#get the difference in time between now and the start time to get total time.</span>
<span class="n">t_end_serial</span> <span class="o">=</span> <span class="n">time</span><span class="o">.</span><span class="n">time</span><span class="p">()</span> <span class="o">-</span> <span class="n">t_start_serial</span> 

<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Serial job took </span><span class="si">%s</span><span class="s2"> seconds.&quot;</span> <span class="o">%</span> <span class="p">(</span><span class="n">t_end_serial</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="n">squared_serial</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>Serial job took 24.022435903549194 seconds.
[]
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[83]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#that was slow! now let&#39;s do this in parallel</span>

<span class="n">pool</span> <span class="o">=</span> <span class="n">multiprocessing</span><span class="o">.</span><span class="n">Pool</span><span class="p">(</span><span class="n">MAX_PROC</span><span class="p">)</span> <span class="c1">#we start a &#39;pool&#39; of workers that we can send processing jobs to</span>

<span class="n">t_start_para</span> <span class="o">=</span> <span class="n">time</span><span class="o">.</span><span class="n">time</span><span class="p">()</span>

<span class="n">squared_para</span> <span class="o">=</span> <span class="p">[]</span>
<span class="k">for</span> <span class="n">squared_number</span> <span class="ow">in</span> <span class="n">pool</span><span class="o">.</span><span class="n">map</span><span class="p">(</span><span class="n">square</span><span class="p">,</span> <span class="n">to_do</span><span class="p">):</span>
    <span class="n">squared_para</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">squared_number</span><span class="p">)</span> 

<span class="n">t_end_para</span> <span class="o">=</span> <span class="n">time</span><span class="o">.</span><span class="n">time</span><span class="p">()</span> <span class="o">-</span> <span class="n">t_start_para</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Parallel job took </span><span class="si">%s</span><span class="s2"> seconds!&quot;</span> <span class="o">%</span> <span class="p">(</span><span class="n">t_end_para</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="n">squared_para</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>Parallel job took 6.006745100021362 seconds!
[1, 4, 9, 16, 25, 36, 49, 64]
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Mini-project">Mini-project<a class="anchor-link" href="#Mini-project">&#182;</a></h2><p>At this point you should have a pretty good idea of the Python basics and some of the extras. Yet, we are still only scratching the surface of the surface of the iceberg. Python has appliations in pretty much every field of programming and software development. But since we are mainly interested in using it as a tool for data handling let's do a mini data-science project to get an idea of some more data-specific Python capabilities. Here the goal is to be able to load a data-set efficiently and do some nice visualizations.</p>
<p>The mini project is to take baby name data from the US social security database and try to identify "Hipster" names. This example inspired by a Kaggle post (<a href="https://www.kaggle.com/ryanburge/d/kaggle/us-baby-names/hipster-names">https://www.kaggle.com/ryanburge/d/kaggle/us-baby-names/hipster-names</a>). You can load the original dataset <a href="https://www.kaggle.com/kaggle/us-baby-names">here</a>.</p>
<p>I filtered and re-arranged the original data to make it easier for us to handle (but trust, me I used Python for that and it was very easy). So you can find the dataset we will use in this exercise in the workshop downloads under the name <code>BabyNames.csv</code></p>
<p>Here's what the data looks like:</p>

<pre><code>name, 1880, 1881, 1882, .... , 2014
Aaron, 3, 4, 6, 22, 0, ...., 199
Aaliyah, 0, 0, 0, 0, 1, ...., 100</code></pre>
<p>As you can see, each row in the file is a baby name, and each column contains the number of babies with that name for each year this dataset was collected.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[22]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">os</span>
<span class="c1">#this is python&#39;s main plotting library</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>

<span class="c1">#tell the notebook to make plots appear inline</span>
<span class="o">%</span><span class="k">matplotlib</span> inline

<span class="c1">#set the size of figures</span>
<span class="n">plt</span><span class="o">.</span><span class="n">rcParams</span><span class="p">[</span><span class="s1">&#39;figure.figsize&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="mi">12</span><span class="p">,</span> <span class="mi">10</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stderr output_text">
<pre>/Users/carlosgonzalezoliver/anaconda/envs/py35/lib/python3.5/site-packages/PIL/Image.py:85: RuntimeWarning: The _imaging extension was built for another  version of Pillow or PIL
  warnings.warn(str(v), RuntimeWarning)
/Users/carlosgonzalezoliver/anaconda/envs/py35/lib/python3.5/site-packages/PIL/Image.py:85: RuntimeWarning: The _imaging extension was built for another  version of Pillow or PIL
  warnings.warn(str(v), RuntimeWarning)
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[111]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#the os module lets us take care of operating system operations. let&#39;s use it to specify the path to a  file for opening</span>

<span class="c1">#let&#39;s load the name dataset</span>
<span class="n">babypath</span> <span class="o">=</span> <span class="n">os</span><span class="o">.</span><span class="n">path</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="s2">&quot;/&quot;</span><span class="p">,</span> <span class="s2">&quot;Users&quot;</span><span class="p">,</span> <span class="s2">&quot;carlosgonzalezoliver&quot;</span><span class="p">,</span> <span class="s2">&quot;Projects&quot;</span><span class="p">,</span> <span class="s2">&quot;Notebooks&quot;</span><span class="p">,</span> \
                       <span class="s2">&quot;BabyNames.csv&quot;</span><span class="p">)</span>

<span class="k">def</span> <span class="nf">read_names</span><span class="p">(</span><span class="n">file_path</span><span class="p">):</span>
    <span class="n">names_dict</span> <span class="o">=</span> <span class="p">{}</span>
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">file_path</span><span class="p">)</span> <span class="k">as</span> <span class="n">f</span><span class="p">:</span>
        <span class="k">for</span> <span class="n">row_number</span><span class="p">,</span> <span class="n">row_string</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">f</span><span class="p">):</span>
            <span class="c1">#first we need to check if we&#39;re at a header row</span>
            <span class="k">if</span> <span class="n">row_number</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
                <span class="c1">#let&#39;s store the years so we can use them as labels later             </span>
                <span class="c1">#we split the row_string by the comma since this is a csv file</span>
                <span class="n">years</span> <span class="o">=</span> <span class="n">row_string</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s2">&quot;,&quot;</span><span class="p">)[</span><span class="mi">1</span><span class="p">:]</span>
                
                <span class="c1">#convert each year to an integer</span>
                <span class="n">int_years</span> <span class="o">=</span> <span class="p">[</span><span class="nb">int</span><span class="p">(</span><span class="n">y</span><span class="o">.</span><span class="n">strip</span><span class="p">())</span> <span class="k">for</span> <span class="n">y</span> <span class="ow">in</span> <span class="n">years</span><span class="p">]</span>
                
            <span class="k">else</span><span class="p">:</span>
                <span class="n">row_info</span> <span class="o">=</span> <span class="n">row_string</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s2">&quot;,&quot;</span><span class="p">)</span>
                <span class="n">name</span> <span class="o">=</span> <span class="n">row_info</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
                <span class="n">counts</span> <span class="o">=</span> <span class="p">[</span><span class="nb">float</span><span class="p">(</span><span class="n">c</span><span class="o">.</span><span class="n">strip</span><span class="p">())</span> <span class="k">for</span> <span class="n">c</span> <span class="ow">in</span> <span class="n">row_info</span><span class="p">[</span><span class="mi">1</span><span class="p">:]]</span>
                
                <span class="n">names_dict</span><span class="p">[</span><span class="n">name</span><span class="p">]</span> <span class="o">=</span> <span class="n">counts</span>
    <span class="c1">#return a dictionary with all the names and their data, and a list with the years </span>
    <span class="k">return</span> <span class="n">names_dict</span><span class="p">,</span> <span class="n">int_years</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[112]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">baby_dict</span><span class="p">,</span> <span class="n">year_list</span> <span class="o">=</span> <span class="n">read_names</span><span class="p">(</span><span class="n">babypath</span><span class="p">)</span>

<span class="c1">#look up your name in the dictionary!</span>
<span class="nb">print</span><span class="p">(</span><span class="n">baby_dict</span><span class="p">[</span><span class="s1">&#39;Carlos&#39;</span><span class="p">])</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>[17.0, 19.0, 20.0, 22.0, 13.0, 28.0, 16.0, 20.0, 29.0, 25.0, 17.0, 16.0, 24.0, 26.0, 25.0, 20.0, 30.0, 28.0, 30.0, 36.0, 37.0, 38.0, 37.0, 41.0, 38.0, 58.0, 50.0, 74.0, 56.0, 60.0, 82.0, 69.0, 124.0, 165.0, 210.0, 273.0, 234.0, 298.0, 347.0, 313.0, 431.0, 399.0, 447.0, 434.0, 453.0, 477.0, 506.0, 551.0, 584.0, 570.0, 587.0, 553.0, 534.0, 573.0, 568.0, 565.0, 541.0, 544.0, 598.0, 589.0, 668.0, 621.0, 659.0, 709.0, 699.0, 736.0, 878.0, 1037.0, 1043.0, 1149.0, 1207.0, 1252.0, 1271.0, 1408.0, 1628.0, 1719.0, 1816.0, 1810.0, 1923.0, 1954.0, 2027.0, 2029.0, 2144.0, 2132.0, 2208.0, 2159.0, 2187.0, 2317.0, 2532.0, 2925.0, 3415.0, 3469.0, 3473.0, 3613.0, 3914.0, 3839.0, 3827.0, 3842.0, 3772.0, 4209.0, 4127.0, 4215.0, 4316.0, 3952.0, 3998.0, 4113.0, 4142.0, 4189.0, 4174.0, 4682.0, 5251.0, 5369.0, 5365.0, 5381.0, 5349.0, 5565.0, 5490.0, 5481.0, 5491.0, 6679.0, 6332.0, 6861.0, 6606.0, 6231.0, 6269.0, 6571.0, 6551.0, 6414.0, 6048.0, 5371.0, 4592.0, 4179.0, 4008.0, 3668.0, 3402.0]
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[99]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#first let&#39;s look for an individual name and plot its popularity trend in time.</span>

<span class="c1">#this function takes as input a name to search for, and the dataframe. it will return a list of years that name</span>
<span class="c1"># appears in, and a list of the counts for each of those years</span>

<span class="c1">#one obstacle for this task is that some names have multiple counts for the same year. so we will have to deal with</span>
<span class="c1"># this. we&#39;ll take the average of the years and use that as our count.</span>


<span class="c1">#notice the &#39;title=&#39; argument. this is known as keyword argument. it is useful for giving a default value to a function</span>
<span class="c1">#so in this case the user can decide whether or not he gives the title of the plot. If he/she doesn&#39;t then the title</span>
<span class="c1">#defaults to &quot;Plot Title&quot;</span>

<span class="k">def</span> <span class="nf">name_plot</span><span class="p">(</span><span class="n">name</span><span class="p">,</span> <span class="n">names_dict</span><span class="p">,</span> <span class="n">year_list</span><span class="p">,</span> <span class="n">title</span><span class="o">=</span><span class="s2">&quot;Plot Title&quot;</span><span class="p">):</span>
    <span class="c1">#we give the matplotlib function plot() the x and y lists that we would like to plot</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">year_list</span><span class="p">,</span> <span class="n">baby_dict</span><span class="p">[</span><span class="n">name</span><span class="p">],</span> <span class="n">label</span><span class="o">=</span><span class="n">name</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="n">title</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s2">&quot;Year&quot;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s2">&quot;Count&quot;</span><span class="p">)</span>
    
    <span class="k">pass</span>
   
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[89]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#let&#39;s try out the function. give it a name and the names_df</span>
<span class="n">name_plot</span><span class="p">(</span><span class="s2">&quot;Carlos&quot;</span><span class="p">,</span> <span class="n">baby_dict</span><span class="p">,</span> <span class="n">year_list</span><span class="p">,</span> <span class="n">title</span><span class="o">=</span><span class="s2">&quot;Carlos Popularity&quot;</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>


<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
ZP8f7qzqegj4bO8AAAAASUVORK5CYII=
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[106]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># we define a hipster name with the three following criteria. let&#39;s say a name is popular if it reaches 1000 babies in </span>
<span class="c1"># a given year.</span>
<span class="c1"># Criteria:</span>
<span class="c1"># * was very popular a long time ago (at least 1000 count between 1915-1930)</span>
<span class="c1"># * very unpopular 30 years ago (under 1000 between 1980-2000)</span>
<span class="c1"># * popular in recent years (more than 1000 after 2010)</span>


<span class="k">def</span> <span class="nf">hipster_names</span><span class="p">(</span><span class="n">baby_dict</span><span class="p">,</span> <span class="n">year_list</span><span class="p">):</span>
    
    <span class="c1">#let&#39;s start an emty list to contain all the matching &#39;hip&#39; names</span>
    <span class="n">hip_names</span> <span class="o">=</span> <span class="p">[]</span>
    
    <span class="c1">#let&#39;s establish the ranges of time to look at</span>
    <span class="n">popular_range</span> <span class="o">=</span> <span class="nb">range</span><span class="p">(</span><span class="mi">1915</span><span class="p">,</span> <span class="mi">1930</span><span class="p">)</span>
    <span class="n">unpopular_range</span> <span class="o">=</span> <span class="nb">range</span><span class="p">(</span><span class="mi">1960</span><span class="p">,</span> <span class="mi">2000</span><span class="p">)</span>
    <span class="n">recent</span> <span class="o">=</span> <span class="mi">2010</span>
    
    <span class="n">names</span> <span class="o">=</span> <span class="n">baby_dict</span><span class="o">.</span><span class="n">keys</span><span class="p">()</span>

    <span class="c1">#we go through each row in the name group</span>
    <span class="k">for</span> <span class="n">name</span> <span class="ow">in</span> <span class="n">names</span><span class="p">:</span>
        <span class="c1">#set some booleans with some initial values that will tell us together if the name is hip</span>
        <span class="n">was_popular</span> <span class="o">=</span> <span class="kc">False</span>
        <span class="n">was_unpopular</span> <span class="o">=</span> <span class="kc">True</span>
        <span class="n">becoming_popular</span> <span class="o">=</span> <span class="kc">False</span>
        
        <span class="c1">#we go through each year in the name</span>
        <span class="k">for</span> <span class="n">index</span><span class="p">,</span> <span class="n">count</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">baby_dict</span><span class="p">[</span><span class="n">name</span><span class="p">]):</span>
            <span class="n">current_year</span> <span class="o">=</span> <span class="n">year_list</span><span class="p">[</span><span class="n">index</span><span class="p">]</span>
            <span class="c1">#check if the name was popular a long time ago</span>
            <span class="k">if</span> <span class="n">current_year</span> <span class="ow">in</span> <span class="n">popular_range</span> <span class="ow">and</span> <span class="n">count</span> <span class="o">&gt;=</span> <span class="mi">1000</span><span class="p">:</span>
                <span class="n">was_popular</span> <span class="o">=</span> <span class="kc">True</span>
                <span class="k">continue</span>
            <span class="c1">#check if the year was unpopular recently</span>
            <span class="k">if</span> <span class="n">current_year</span> <span class="ow">in</span> <span class="n">unpopular_range</span> <span class="ow">and</span> <span class="n">count</span> <span class="o">&gt;=</span> <span class="mi">1000</span><span class="p">:</span>
                <span class="n">was_unpopular</span> <span class="o">=</span> <span class="kc">False</span>
                <span class="k">continue</span>
            <span class="c1">#check if the name is growing in popularity</span>
            <span class="k">if</span> <span class="n">current_year</span> <span class="o">&gt;=</span> <span class="n">recent</span> <span class="ow">and</span> <span class="n">count</span> <span class="o">&gt;=</span> <span class="mi">1000</span><span class="p">:</span>
                <span class="n">becoming_popular</span> <span class="o">=</span> <span class="kc">True</span>
                <span class="k">continue</span>

        <span class="c1">#combine all the booleans to tell us if the name matches all our criteria. if it does, add it to the list</span>
        <span class="k">if</span> <span class="n">was_popular</span> <span class="ow">and</span> <span class="n">was_unpopular</span> <span class="ow">and</span> <span class="n">becoming_popular</span><span class="p">:</span>
            <span class="nb">print</span><span class="p">(</span><span class="n">name</span><span class="p">)</span>
            <span class="n">hip_names</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">name</span><span class="p">)</span>

    <span class="c1">#return the list.</span>
    <span class="k">return</span> <span class="n">hip_names</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[107]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#now we just have to call the function hipster_names. give this a couple of minutes as it&#39;s a lot of data!</span>
<span class="n">hip_names</span> <span class="o">=</span> <span class="n">hipster_names</span><span class="p">(</span><span class="n">baby_dict</span><span class="p">,</span> <span class="n">year_list</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">hip_names</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>Violet
Eleanor
Oliver
Genevieve
Rosalie
Hazel
Lena
Ella
Stella
Clara
[&#39;Violet&#39;, &#39;Eleanor&#39;, &#39;Oliver&#39;, &#39;Genevieve&#39;, &#39;Rosalie&#39;, &#39;Hazel&#39;, &#39;Lena&#39;, &#39;Ella&#39;, &#39;Stella&#39;, &#39;Clara&#39;]
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[108]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#let&#39;s plot the trendlines of each hip name</span>
<span class="k">for</span> <span class="n">n</span> <span class="ow">in</span> <span class="n">hip_names</span><span class="p">:</span>
    <span class="n">name_plot</span><span class="p">(</span><span class="n">n</span><span class="p">,</span> <span class="n">baby_dict</span><span class="p">,</span> <span class="n">year_list</span><span class="p">,</span> <span class="n">title</span><span class="o">=</span><span class="s2">&quot;Hipster Names&quot;</span><span class="p">)</span>

<span class="c1">#we set the legend, x-axis label, y-axis label, and title of the plot</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">(</span><span class="n">loc</span><span class="o">=</span><span class="s2">&quot;upper left&quot;</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt output_prompt">Out[108]:</div>


<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.legend.Legend at 0x10d93a748&gt;</pre>
</div>

</div>

<div class="output_area"><div class="prompt"></div>


<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
IiIiIm3Jpcm6ZVn1n1xX45xGjv8z8OcGtq8HTm5gexnVyb6IiIiISHvjCRNMpQMYPXq0u0PosPS9
dy99/91L33/30ffevfT9bz9c+gRTT2KMsTrKvYqIiIh4q/Jy8PMD48Vr/BljsLxogqlH69atG8YY
vbzg1a1bN3f/5yIiIiIudtFFsHixu6PwHB2+sl79yccNEUlz6WclIiLSvqWlQffujoT97bfdHU3L
qbIuIiIiIu3O4sXwf/8Hn38Odru7o/EMStZFRERExO2qquCll+DOO6FnT1izxt0ReQYl6yIiIiLi
dl9+CcHBMGQInHcefPSRuyPyDErWvdiNN97Iww8/3KRjfXx82LVrl4sjEhEREWmZl16Cq692rAKj
ZP03StY92HnnnccDDzxwxPZly5aRkJDA/Pnzuffee5t0LdPE9Y9WrVpFUlJSc8IUEREROS5FRfDO
O3DllY73p50GmZmwd6974/IEStY92PTp03nllVeO2P7KK68wderUJifgQJNXUbEsq1nXFRERETle
b74Jo0ZBfLzjva8vjB0L//ufe+PyBErWPVhqairZ2dmsXr3auS0vL4/333+fqVOncvXVV3P//fc7
9y1cuJCTTjqJ2NhYUlNTyczMbPC6drudO+64g5SUFBISErjxxhspKyujpKSE888/n4yMDMLCwggP
D2f//v0uv08RERHp2GpaYGpTK4yDknUPFhQUxKWXXsriWk8GeP311+nTpw8nn3xynWNXrFjBn/70
J/7zn/+QmZlJcnIyl19+eYPXveuuu9ixYwebN29mx44dZGRk8OCDD2Kz2fjoo49ITEyksLCQgoIC
Onfu7NJ7FBERkY5t5074+We44IK628eOhc8+czzRtCNTsn4MxrTOq6WmT5/Om2++ib16sdGXX36Z
q6666ojjlixZwrXXXsuAAQPw9/fnz3/+M19//TV79uw54tiFCxfyzDPPEBERQUhICHfffTdLly5t
eZAiIiIiLbRoEVxxBQQE1N0eHw89esBXX7knLk/h5+4APJ27H5h5xhln0KlTJ9555x2GDBnCt99+
yzvvvHPEcRkZGQwePNj5PiQkhJiYGNLT00lOTnZuP3ToECUlJXWOraqq0pNBRUREpM1VVTmS9Xff
bXh/TSvM737XtnF5ElXWvcDUqVNZtGgRr7zyCuPGjSM2NvaIYxITE0lLS3O+Ly4uJjs7m65du9Y5
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
ERGRjqy8HJYtg3POabsxlayLiIiIiDTB3/8O3brBiBFtN+awYfD11004sB20wWiCqSYteg39rERE
RDxLerpjbfWvvoKePdtu3KIi6NTJUTg/6iTToCDHE5SCgtosNtAEUxERERHxAH/8I9xwQ9sm6uCY
YBoUBNnZRzmostLRoxMY2GZxuYKfuwMQEREREe/z2WeOvvEXXnDP+ElJsG8fxMY2ckBNv7qXP21d
lXURERERaRa7HW6+Gf76V/fN3+zaFfbuPcoB7WByKShZ93pz585l6tSpAOzdu5fw8HD1dYuIiIhL
PfMMnHgiTJjgvhhqKuuNageTS0HJuld46aWXOOWUUwgJCSExMZGZM2eSn5/v3G+q/7yTlJREQUGB
872IiIhIa9uzB554wlFVd2fKkZSkyrp4gKeeeop77rmHp556ioKCAtauXUtaWhpjx46loqKiTWKo
rKxsk3FERETE8/31r3DddY7KujupDUbcrrCwkAceeIB//OMfnHvuufj6+pKcnMwbb7zB7t27eeWV
V+ocn5aWho+PD1VVVbzxxhucdtppdfY/88wzpKamAmC327njjjtISUkhISGBmTNnUlZWBsCqVatI
Skri8ccfJyEhgWuuuaZtblhEREQ83q5dMGSIu6NQG4x4gK+++oqysjImTpxYZ3tISAjnnXcen3zy
yRHn1LTAjB8/nm3btrFz507nvqVLlzJlyhQA7rrrLnbs2MHmzZvZsWMH6enpPPjgg85j9+/fT15e
Hnv27OG5555zxe2JiIiIF0pPd1S13U1tMOJgTOu8WiArK4vY2Fh8fI78MSUkJJCVldXoucHBwVx0
0UUsXboUgO3bt7N161YmVM8EWbhwIc888wwRERGEhIRw9913O48F8PX1Ze7cufj7+xPo5euTioiI
SOtJT4cuXdwdheMDQ3o6NLquhpL1DsKyWufVArGxsWRlZVFVVXXEvszMTGIbXVjUYfLkyc4EfMmS
JaSmphIYGMihQ4coKSlh8ODBREdHEx0dzXnnnUd2rScLdOrUCX9//xbFLSIiIu1TRQUcOgSdO7s7
EkcebrNBo7VLtcGIqw0fPpzAwEDeeuutOtuLior46KOPGDNmzFHPP/fcczl06BCbNm3itdde44or
rgAcHwJsNhtbtmwhJyeHnJwc8vLyGlxhRkRERKTGgQMQEwOeUs876iRTVdbF1cLDw7n//vu55ZZb
+N///kdFRQW7d+9m0qRJJCcnO9dXr632Gut+fn5ceuml3HnnneTm5nLuuecCjkT8+uuvZ9asWRw6
dAiA9PR0li9f3jY3JiIiIl5p3z7PaIGpcdRJpkrWpS3ceeedPPLII9xxxx1EREQwfPhwUlJS+PTT
TxtsU6lfEZ88eTKfffYZl112WZ3e98cee4wePXowbNgwIiMjGTt2LNu2bXP5/YiIiIj38pR+9RpH
nWTaTtpgTEd52qUxxmroXo0xeuKnl9DPSkRExL3+/nf4+WeYP9/dkTg8/DAUFcGf/9zAzrvuguho
x79trDpnaZWeYlXWRURERKRJVFlve0rWRURERKRJPC1Z1wRTEREREZFqnpasa4KpiIiIiEg1T0vW
ax6M1MAjadQGIyIiIiIdh2V5XrIeHAyhoY08GEmVdRERERHpKAoKHP+Gh7s3jvoanWSqZF1ERERE
OoqaqrqnPeS80WRdbTAiIiIi0lF4WgtMja5dG5lkqsq6dFR79+4lPDxcDygSERHpQDw1WT9qZV3J
urSF1157jWHDhhEaGkrnzp0ZPnw4zz77rNviSUpKoqCgAONpfwcTERERl/HUZP2olXW1wYirPfXU
U9x2223cddddHDhwgP3797NgwQK++uorysvL3R2eiIiIdBCemqxrgqm4TUFBAXPmzOHZZ59l4sSJ
hFR/OhwwYAAvv/wy/v7+2O127rjjDlJSUkhISGDmzJmUlZUBsGrVKpKSknj66aeJj4+nS5cuvPTS
S87r1z/3xhtvdJ7bt29fPvzwQ+exlZWVxMXFsXHjRtLS0vDx8aGqelHTgoICrrvuOhITE0lKSmL2
7NlYloXdbicqKoqffvrJeZ2srCxsNhtZ1Wssvf/++wwcOJCoqChGjhzJDz/84NLvqYiIiLRMerqj
iu1pGkzW7XbHTFh/f7fE1JqUrHuwr7/+GrvdzoQJExo95q677mLHjh1s3ryZHTt2kJ6ezoMPPujc
v3//fgoLC8nIyOD555/npptuIj8/v8FzMzIynOdOnjyZJUuWOK/z8ccf06lTJ0499VSAOi0w06dP
JyAggF27drFhwwY++eQTnn/+eQICArjkkktYunSp89g33niD0aNHExsby4YNG7j22mtZuHAhOTk5
zJgxgwkTJugvBiIiIh7IUyvrXbpARka9ByO1k6o6gOkokwSNMVZD92qMOepESbNyZauMb40e3exz
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
RvZVCHcmAAAAAElFTkSuQmCC
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Things-we-didn't-cover">Things we didn't cover<a class="anchor-link" href="#Things-we-didn't-cover">&#182;</a></h2><p>There are many, many, many more useful libraries that I didn't have time to cover. I'm going to list a few of the ones that you might want to check out.</p>
<ul>
<li><a href="http://www.numpy.org/">numpy</a> very powerful numerical and matrix operations </li>
<li><a href="http://pandas.pydata.org/">pandas</a> game changer for data handling</li>
<li><a href="http://seaborn.pydata.org/index.html">seaborn</a> scientific plotting </li>
<li><a href="http://scikit-learn.org/stable/">scikit-learn</a> very complete Machine Learning algorithms and tools</li>
<li><a href="http://biopython.org/wiki/Biopython">BioPython</a> biological sequence data and analysis. (alignments, trees, etc.)</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

</div>
</div>
</div>

</div>
    </div>
  </div>
</body>
</html>
