# PPrepair

## What is PPRepair?

PPrepair is developed by  Ken Arroyo Ohori at TU Delft. See https://github.com/tudelft3d/pprepair

pprepair (planar partition repair) takes a set of polygons and ensures that they form a valid planar partition, made of valid polygons and having no gaps or overlaps. It can be used as a validator, telling of problems in individual polygons or in the planar partition, and also as an automatic repair tool, outputting a set of polygons that do form a valid planar partition. If you are only interested in repairing individual polygons, have a look at prepair.

This docker installs pprepair in a docker container so you can use docker to run the pprepair commands. 

## How to run as a docker command?

To see the PPrepair help:

	docker run --rm niene/pprepair

To run the docker pprepair command put your shapefiles in a seperate folder, called `repair_files`. Then run: 

	docker run --rm -v `pwd`/repair_files:/repair_files niene/pprepair -i repair_files/input_shapefile.shp -o repair_files/output_shapefile.shp -fix -rp -rtlb -rrlb


The `--rm` flag removes the docker container and its volume after it is finished executing. 