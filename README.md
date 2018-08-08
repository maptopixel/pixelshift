# pixelshift

## Overview
Automatically align polygons with gridded (raster) data such as images and surface models.

## Detail
pixelshift is a command-line interface (CLI) tool for automatic conflation of a polygon Shapefile with grid data such as images and surface models. The conflation aligns a 2D geometry using Stochastic Gradient Descent (SGD) optimisation.

    pixelshift inputGrid polygonsShapefile maxIterations displacementMagnitude numCores

The parameters are (order matters):

    inputGrid = a geotiff.
    polygonsShapeFile = Shapefile of polygons in partial alignment with the inputGrid.  
    maxIterations = number of iterations for SGD.
    displacementMagnitude = bound for random distribution used in SGD.
    numCores = number of cores used for the parallelisation of the optimisation.
	outputFilePath = path and name of output file (.shp) of adjusted features.

## Example usage
pixelshift dsmSlopeFile.tif buildingPolygons.shp 100 2 4

