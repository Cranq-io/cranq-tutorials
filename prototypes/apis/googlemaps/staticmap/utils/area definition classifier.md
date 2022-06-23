# Area definition classifier

[apis/googlemaps/staticmap/utils]

### Input ports:

* __area__: 
    ```
    ({optional "type" :"center", "center" :[number,number], "zoom" :number} or {"type" :"path", "points" :[number,number][], "style" :{optional "weight" :number, optional "color" :string, optional "fillColor" :string, optional "geodesic" :boolean}} or {"type" :"markers", "points" :[number,number][], "style" :{optional "size" :("tiny" or "mid" or "small"), optional "color" :string, optional "label" :string}})
    ```

### Output ports:

* __center area__: `{"center" :[number,number], "zoom" :number}`


* __unknown__: `any`

