# juno-tools

Default AURIN jupyter tools


## Test of sf R library

```shell script
sf <- library("sf")
demo(nc, ask = FALSE, echo = FALSE)
nc$geom2 = st_centroid(st_geometry(nc))
print(nc, n = 2)
```


## Shopping user interface

The first step is to create a `secrets.py` file with the usernid and the AURIN API key:
```shell script
userid='<user id>'
apiKey='<api key>'

```

After this prelimanary operation the `shopping/shopping.ipynb` notebook has to be opened and the cells inside it run.
A form with a map should appear. 

Let's go through a shopping scenario:
* Zoom on an area around Perth
* In the WFS drop down choose `WA Landgate - Public Infrastructure - Water_Dam (WCORP-075)`
* Click on the 'Shop' button
* The text box below the `Shop` should show that the request has been accepted
* After a while, three files are created under `../aurin/data`
  - `status-<dataset id from the form>.json`
  - `metadata-<dataset id from the form>.json`
  - `data-<dataset id from the form>.geojson` 
  
