# juno-tools
Default AURIN jupyter tools


## Test of sf R library

```shell script
sf <- library("sf")
demo(nc, ask = FALSE, echo = FALSE)
nc$geom2 = st_centroid(st_geometry(nc))
print(nc, n = 2)
```

