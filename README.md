# Bible Format Converter
Convert Unbound, OSIS, and JSON Bibles to HTML

![bible](https://cloud.githubusercontent.com/assets/5648875/6840545/2ae66460-d348-11e4-891f-11b7b2a0a27c.png)

## Rendering Bibles

Navigate to `/content/index.html` in your browser. The following versions ship with ezra.js.

- American Standard Version (ASV)
- Arabic Smith & Van Dyke (SVD)
- French Ostvervald (FO)
- German Schlachter (GS)
- King James Version (KJV)
- New Chinese Version Simplified (NCVS)
- World English Bible (WEB)

### Features

- Responsive Design
- Version and Book Drop-down Menus
- Hash-based Routing
- Infinite Scrolling

## Generating Bibles

### Supported Formats

&#x2713; [Unbound](http://unbound.biola.edu/)<br>
&#x2713; [OSIS](https://github.com/matt-cook/osis-bibles)<br>
&#x2713; [JSON](https://github.com/honza/bibles)

### Setup

1. Install Node.js (http://nodejs.org/download/) for your platform.
2. Navigate to the `/core/tools/scribe` folder.
3. Run `npm install` to install dependencies.
4. For each Bible that you want to convert, create a file named `info.json`. Use this template as a guide.
```
{
  "type": "Bible",
  "file": "asv",
  "name": "American Standard Version",
  "abbreviation": "ASV",
  "language": "English",
  "format": "unbound"
}
```

### Convert Unbound and OSIS Bibles to JSON

1. Add Unbound and OSIS Bibles to the `/core/tools/scribe/literature` folder.
2. Navigate to the `/core/tools/scribe` folder.
3. Run `node translate.js` to convert all Bibles in the `/core/tools/scribe/literature` folder to JSON.

### Convert JSON Bibles to HTML.

**Note: If you converted Unbound or OSIS Bibles, skip to step 2.**

1. Add JSON Bibles to the `/core/api/literature` folder.
2. Navigate to the `/core/tools/scribe` folder.
3. Run `node write.js` to convert all Bibles in the `/core/api/literature` folder to HTML.

## Versioning

Release format: `<major>.<minor>.<patch>`

## Author

| [![BarryMode](https://avatars3.githubusercontent.com/u/5648875?v=2&s=70)](https://twitter.com/barrymode "Follow @BarryMode on Twitter") |
|---|
| [BarryMode](https://barrymode.com) |

