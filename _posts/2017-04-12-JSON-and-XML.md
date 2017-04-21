---
layout: post
title:  "Handling Data: JSON and XML"
categories: jekyll update
---

## **Exercises 1**


**1. Create a well-formed XML document that describes MP3 files. Add a `<files>` root element, containing 3 `<file>` elements. Each `<file>` element should contain child elements for the title, artist, album, and genre, and should have attributes for the track length and a unique id. Once complete, you should validate that the document is well-formed by opening it in a browser.**<br>

<span class="label label-warning">Answer:</span><br>

```xml
<files>
  <file id="1" trklength="2">
    <title></title>
    <artist></artist>
    <album></album>
    <genre></genre>
  </file>
  <file id="2" trklength="5">
    <title></title>
    <artist></artist>
    <album></album>
    <genre></genre>
  </file>
  <file id="3" trklength="3">
    <title></title>
    <artist></artist>
    <album></album>
    <genre></genre>
  </file>

</files>
```

<br>

<br>
**2.** Create an internal DTD that specifies a set of rules the document you just created must adhere to for it to be valid. You should enforce that the `<title>` and `<artist>` elements should appear first, in that order, and are mandatory. The `<album>` and `<genre>` elements should be optional. Once complete, validate that the DTD works using the online XML validator at codebeautify.org. <br> 

<span class="label label-warning">Answer:</span> <br>

```xml
<?xml version="1.0"?>
<!DOCTYPE files [
<!ELEMENT files (file+)>
<!ELEMENT file (title,artist+,album?,genre?)>
<!ELEMENT title (#PCDATA)>
<!ELEMENT artist (#PCDATA)>
<!ELEMENT album (#PCDATA)>
<!ELEMENT genre (#PCDATA)>
<!ATTLIST file id CDATA #REQUIRED>
<!ATTLIST file trklength CDATA #REQUIRED>
]>

<files>
  <file id="1" trklength="2">
    <title></title>
    <artist></artist>
    <album></album>
    <genre></genre>
  </file>
  <file id="2" trklength="5">
    <title></title>
    <artist></artist>
    <album></album>
    <genre></genre>
  </file>
  <file id="3" trklength="3">
    <title></title>
    <artist></artist>
    <album></album>
    <genre></genre>
  </file>

</files>
```



## **Exercises 2**


**1. Store the same data used in the XML document that you created in the exercises for the previous section, but this time using a JavaScript object. This object should contain a property called files, which is an array containing three objects. Each of these objects should have title, album, and genre properties containing strings and a track_length property containing a number, but the artists property should contain an array of one or more strings. You should validate that the JSON is valid using the JSON Lint site. Once you have validated your JSON, convert it to a JSON string.**<br>

<span class="label label-warning">Answer:</span><br>

```json
var mp3 = {
 "files": [

        {
            "title": "Beat It",
            "artist": ["Michael", "Jackson"],
            "album": "Thriller",
            "genre": "Pop",
            "track_length": 1
        }, {
            "title": "Back in Black",
            "artist": ["AC/DC"],
            "album": "Back in Black",
            "genre": "Hard Rock",
            "track_length": 2
        }, {
            "title": "Money",
            "artist": ["Pink", "Floyd"],
            "album": "The Dark Side of the Moon",
            "genre": "Progressive Rock",
            "track_length": 3
        }

    ]
}

var mp3Json = JSON.stringify(mp3);
```

<br>

<br>
**2.** Parse the JSON string that you ended up with after the previous exercise back to its original object form, but use a reviver function to add an auto-incrementing ID to each object within the files array. <br> 

<span class="label label-warning">Answer:</span> <br>

```json
var mp3Parse = JSON.parse(mp3Json, function(key, value){
    if (typeof value === 'object' && key === 'files') {
      value.map(function (key, value) {
        key.id = value + 1; 
      })
     return value;
    } else {
      return value;
    }
});
```





