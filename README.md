# intellij-colorblind-settings
Adjusted color settings for colorblind and color-deficient users of IntelliJ

## Why?

IntelliJ 15 includes support for some colorblind and color-deficient users, but doesn't provide the granularity of an earlier beta release. This repository attempts to correct that by providing settings for the most common types of color blindness. It also allows users of earlier versions to easily tweak their color settings for usability.

## Installation

### Import from settings.jar

1. Download the settings.jar file
2. Go to `Configure | Import Settings`
3. Choose the settings.jar file and click OK. This will only overwrite your color settings.
4. Restart IntelliJ when prompted.
5. Go to `Settings | Editor | Color & Fonts` and chose your theme

### Manual import

1. Open your .IntelliJIdea / .IdeaIC settings folder
2. Navigate to `/config/colors/`
3. Add any .icls file you would like to include. To use a dark style, be sure to include the regular style too because the dark styles import from the regular style. For example, include both "Protanopia.icls" and "ProtanopiaDark.icls"

## Details
Complete color blindness is very rare. Most people who cannot see the full color spectrum have either a **dichromacy** (complete blindness of red, blue, or green) or a **trichromacy** (partial blindness of red, blue, or green). The settings used to create these files were targeted for dichromats, and therefore should also work for trichromats.

Type | Description
------------- | -------------
Protanopia/Protanomaly  | Red-deficient. Difficult to distinguish red/green. Colors that contain red may appear more dull.
Deuteranopia/Deuteranomaly  | Green-deficient. Difficult to distinguish red/green. Colors that contain green may appear more dull.
Tritanopia/Tritanomoly | Blue-deficient. Difficult to distinguish blue/green and yellow/red.

If you need help figuring out which you have, I recommend the tests at [Colbindor](http://www.color-blindness.com/color-blindness-tests/). My personal favorite is the Color Arrangement Test.

Of course, I can only see colors in one way (I am protanomalous). If you are having trouble with the settings for your deficiency, please let me know so we can tweak them. Thanks!

## Sources

I used the color schemes in the [DefaultColorSchemesManager](https://github.com/JetBrains/intellij-community/blob/master/platform/platform-resources/src/DefaultColorSchemesManager.xml) included in the intellij-community source code along with their [DaltonizationFilter](https://github.com/JetBrains/intellij-community/blob/master/platform/editor-ui-api/src/com/intellij/ide/ui/DaltonizationFilter.java) as a reference.
