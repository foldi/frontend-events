# Looking for a conference?

This is the code for [a website](http://foldi.github.io/frontend-events/) that lists front-end and general web conferences and meetups. You can also [add an event](https://docs.google.com/spreadsheet/ccc?key=0AsxZWWM7rVLodGt1REhjeGhYMDk2SG9nc0JsNGFxb1E)!

### Fork -n- Go!

This repo only has a **gh-pages** branch, which means as soon as you **fork** it, you have a hosted and live version of it yourself!

Next, create a spreadsheet with the same column headers as [the original](https://docs.google.com/spreadsheet/ccc?key=0AsxZWWM7rVLodGt1REhjeGhYMDk2SG9nc0JsNGFxb1E).

Click on the `index.html` file, click edit and change **line 118** (or thereabouts) it looks like:

```javascript
    document.addEventListener('DOMContentLoaded', function() {
      var gData
      var URL = '0AsxZWWM7rVLodGt1REhjeGhYMDk2SG9nc0JsNGFxb1E'
      Tabletop.init( { key: URL, callback: myData, simpleSheet: true } )
    });
```

Replace the existing spreadsheet URL key with your spreadsheet's key. You'll find that by clicking (in Google Spreadsheets) File > Publish to the Web > Start Publishing, it will then display the key in a window. ![get key](https://raw.github.com/jllord/sheetsee-cache/master/img/key.png)

Commit those changes and **LIKE WOAH** you now have a version of this website hooked to a spreadsheet that you can distrubute however you'd like.

You can find your version at **yourGitHubName.github.io/theReposName** (in this case /frontend-evnets).

## But How?

A Google Spreadsheet holds all the data and it is connected to this website using the goodies in [sheetsee.js](http://www.github.com/jlord/sheetsee.js). Everytime you visit the website, you'll have the most up to date data that has been entered into the spreadsheet.
