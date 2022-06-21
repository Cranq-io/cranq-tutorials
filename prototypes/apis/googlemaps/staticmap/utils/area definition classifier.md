# Area definition classifier

[apis/googlemaps/staticmap/utils]

### Input ports:

* __area__: _({optional "type" :"center", "center" :[number,number], "zoom" :number} or {"type" :"path", "points" :[number,number][], "style" :{optional "weight" :number, optional "color" :string, optional "fillColor" :string, optional "geodesic" :boolean}} or {"type" :"markers", "points" :[number,number][], "style" :{optional "size" :("tiny" or "mid" or "small"), optional "color" :string, optional "label" :string}})_



### Output ports:

* __center area__: _{"center" :[number,number], "zoom" :number}_



* __unknown__: _any_



