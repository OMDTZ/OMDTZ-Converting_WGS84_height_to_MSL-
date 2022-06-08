# Converting_WGS84_height_to_MSL


# Introduction

# how to convert

- Download the program and unzip Und_min1x1_egm2008_isw=82_WGS84_TideFree_SE, which is the program will be used for convertion.

- From the files, you will find the input and out put text files. In input text file copy your coordinates, only long and lat. Dont include the headers, you can see the sample data in input file

- Run the program, if your using linux, install wine. For Ubuntu 20. For window, not exactly sure but i guess it will be simple

- After the process, the output file will be loaded with coordinates with additionaly geiod differents.  This file contains POINT values of geoid undulations with respect to WGS 84 in meters, on a 1'x1'global grid (equi-angular spacing in terms of WGS 84 geodetic coordinates), computed from EGM2008 to degree 2190 and using the ζ*-to-N conversion expansion to degree 2160. The file is global, and contains valid values for ALL 1'x1' cells, regardless whether they are located over land or over ocean. The geoid undulations refer to the “Tide-Free” system, as far as the Permanent Tide is concerned. This file holds the 1'x1' geoid undulations in sequential, unformatted, binary format, with each geoid undulation stored as a single, REAL*4 value. Each record contains all of the geoid undulations for a single parallel band. Each geoid undulation is situated at the corner of its respective cell, such that the top-left value in the 1'x1' grid has a longitude of 0° East and a latitude of 90° North. The first record in the file contains the northern-most parallel, and the first value in each record is the western-most value for that parallel. Note that each 1'x1' value situated on the zero meridian appears only once, as the first value in its respective record, at
a longitude of 0° East. These values are NOT repeated at the end of their respective records, at longitude of 360° East. As such, this file contains 10801 rows x 21600 columns of geoid undulations.

- The output which is The geoid undulation, a distance between the geoid and ellipsoid. You will need to substract that with the ellipsoidal height and you will have the MSL elevation.


## Important terms

- Ellipsoid height (h) is the difference between the ellipsoid and a point on the Earth’s surface. It is also called the geodetic height (not to be confused with geodetic datums). If you have coordinates that were captured with a GPS receiver, the elevation data reference the ellipsoid, meaning it has to be transformed to match the more accurate geoid instead.

- Geoid height (N) is the offset value between the reference geoid and the ellipsoid models.

- Orthometric height (H)—AKA the one you really care about— is the distance between a point on the Earth’s surface and the geoid. As we already discussed, the geoid represents Mean Sea Level. When you hear elevation data described as “X feet above (or below) sea level,” that’s referring to orthometric height.
To deliver consistent orthometric heights across your site, we use your chosen datums and this simple formula: H = h – N. Simple, right?


 

# Resources

- https://digiterraexplorer.com/downloads/documentation/DigiTerra_Explorer_v7_RefGuide/mobile/the_geoid_undulation.htm

- https://earth-info.nga.mil/GandG/wgs84/gravitymod/egm2008/egm08_wgs84.html

- https://earth-info.nga.mil/GandG/wgs84/gravitymod/egm2008/index.html

- https://www.eye4software.com/download/

- https://earth-info.nga.mil/GandG/wgs84/gravitymod/egm2008/egm08_wgs84.html

- https://earth-info.nga.mil/GandG/wgs84/gravitymod/egm2008/egm08_gis.html

- https://www.eye4software.com/hydromagic/documentation/manual/utilities/egm2008-geoid/

- mhttps://earth-info.nga.mil/GandG///wgs84/gravitymod/egm2008/egm08_wgs84.html

