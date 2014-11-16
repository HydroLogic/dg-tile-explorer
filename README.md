# dg-tile-explorer

## Get a geoTif from digital Globe, convert it to tiles and upload it.

## Requirements
  
  - **Python version:** > 2.4
  - GDAL
  - s4cmd (or s3cmd)

## SETUP (Mac OS X)
  
### Python (Mac OS X)
      
      Installing Python on Mac OS X. Follow the instructions [here](http://docs.python-guide.org/en/latest/starting/install/osx).

### GDAL (Mac OS X)
    
      Installing GDAL on Mac OS X. Follow the instructions [here](https://github.com/bloomreach/s4cmd).

### s4cmd

      Install s4cmd: pip install s4cmd - Follow the instructions [here](https://github.com/bloomreach/s4cmd).

      Do not forget to set the S3_ACCESS_KEY and S3_SECRET_KEY environment variables to contain your S3 credentials.

## Process

### Get a geoTif from digital Globe

      Download Images from [https://services.digitalglobe.com](https://services.digitalglobe.com).

### Convert images to tiles

      gdal2tiles.py -z 1-18 image_file_name.tif [folder]

### Upload tiles to Amazon s3
      
      s4cmd.py sync /path_to/dirA s3://bucket/path_to/dirB/


