# PPrepair

## What is PPRepair?

## How to run as a docker command?

To see the PPrepair help:

	docker run -rm niene/pprepair

	docker run -rm -v `pwd`/repair_files:/repair_files niene/pprepair -i repair_files/input_shapefile.shp -o repair_files/output_shapefile.shp -fix -rp -rtlb -rrlb

The `-rm` flag removes the docker container after it is finished executing. 