# Coordinates to words

[apis/what3words]

### Input ports:

* __coordinates__: _[number,number]_

    Receives the coordinates to be converted to what3words.
    
    Format: [latitude, longitude]



* __params__: _{"apiKey" :string, optional "language" :string, optional "format" :("json" or "geojson")}_

    Receives what3words API parameters.



### Output ports:

* __data__: _({"country" :string, "square" :{"southwest" :{"lng" :number, "lat" :number}, "northeast" :{"lng" :number, "lat" :number}}, "nearestPlace" :string, "coordinates" :{"lng" :string, "lat" :string}, "words" :string, "language" :string, "map" :string} or {"features" :[{"bbox" :[number,number,number,number], "geometry" :{"coordinates" :[number,number], "type" :"Point"}, "type" :"Feature", "properties" :{"country" :string, "nearestPlace" :string, "words" :string, "language" :string, "map" :string}}], "type" :"FeatureCollection"})_

    Sends data structure describing the geographical area identified by the 3-word address.



* __response__: _{"status" :number, "headers" :{string: any}, "body" :string}_



* __error__: _{"error" :string, optional "details" :any}_



