# Home-Assistant-Mail-And-Packages-Custom-Card
A Custom Lovelace card to pull together the mail and packages sensors.

<img src="https://github.com/moralmunky/Home-Assistant-Mail-And-Packages-Custom-Card/blob/master/img/card-image.png?raw=true" alt="Preview of card" />

## Lovelace GUI Setup

##Manual Install
Bothh JS files need to be stored inside the path/to/config/www/ folder. In the Lovelace reource URL path, local is the same as the www folder. Construct your path to the JS inside the www folder for the resurce URL. For the example below:
```
path/to/config/www/Home-Assistant-Mail-And-Packages-Custom-Card/Home-Assistant-Mail-And-Packages-Custom-Card.js

path/to/config/www/Home-Assistant-Mail-And-Packages-Custom-Card/Home-Assistant-Mail-And-Packages-Custom-Card-editor.js
```
Configuration > Lovelace Dashboards > Resources

```
url: /local/Home-Assistant-Mail-And-Packages-Custom-Card/Home-Assistant-Mail-And-Packages-Custom-Card.js
type: Javascript Module
```

## HACS Install

HACS will install the files and add an entry in the Lovelace resource

HACS install path
```
/path/to/config/www/community/Home-Assistant-Mail-And-Packages-Custom-Card/
```
Path HACS adds to Lovelace resources
```
/hacsfiles/Home-Assistant-Mail-And-Packages-Custom-Card/Home-Assistant-Mail-And-Packages-Custom-Card.js
```

*You may need to empty your browser cache for the front end to pull the new ha files.

## Card Configuration
Add the card configuration to the cards: section of the view you want the card to be in.

Visual Editor Minimal Setup:
Add a manual card then input the yaml below. The remaining sensors can be added in the visual editor.
```
type: 'custom:mail-and-packages-card'
name: Mail Summary
updated: sensor.mail_updated
details: true
image: false
```
Switch to the visual editor and complete the setup by assigning the sensors you have enabled in the [Mail and Packages integration](https://github.com/moralmunky/Home-Assistant-Mail-And-Packages).
<img src="https://github.com/moralmunky/Home-Assistant-Mail-And-Packages-Custom-Card/blob/master/img/visual-editor.png?raw=true" alt="Preview of visual-editor" />
