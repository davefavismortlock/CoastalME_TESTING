# TO DO LIST
## Table of contents
- [User input](#user-input)
- [Error handling](#error-handling)
- [Theory/Efficiency](#theory-efficiency)
- [Output](#output)

## User input
   TODO should user input be split in two main files: one for frequently-changed things, one for rarely-changed things? If so, what should go into each file ('testing only' OK, but what else?

   TODO 003 Make coastline curvature moving window size a user input *** FIXED in 1.1.22
   TODO 011 Should this constant be a user input?
   TODO 036 Read in changed deep water wave values
   TODO 030 Do we also need to be able to input landform sub-categories?
   TODO 027 Sort out GDAL problem with raster reference units
   TODO 022 Get intervention update working
   TODO 041 Read in SWL per-timestep
   TODO 042 Should we have a smallest valid input for KLS in the CERC equation?
   TODO 045 Method of getting depth of closure value needs to be a user input
   TODO 047 Where is the GDAL description for the deep water wave stations vector file?
   TODO 048 Where is the GDAL description for the flood input locations point or vector file?
   TODO 049 Handle other command line parameters e.g. path to .ini file, path to datafile
   TODO 035 Also handle other EPSG for vector spatial reference systems
   TODO 054 Choose more files to omit from "usual" raster output

##   Error handling
   TODO 004 Improve error handling of situation where we have a valid shadow zone but cannot find a neighbouring cell which is 'under' the coastline
   TODO 006 Check GDALGridCreate() with only start-of-coast or an end-of-coast profiles
   TODO 009 Decide what to do when we have eroded down to basement
   TODO 015 Improve situation where profile hits another profile which belongs to a different coast object (will certainly need this for estuaries)
   TODO 017 Extra safety check needed, make sure that each point is within valid grid
   TODO 018 Improve situation where new landwards point on parallel profile is not within the raster grid
   TODO 019 Improve situation where Dean profile has a near-zero elevation difference
   TODO 020 Check calculation of elevation of coast point of Dean parallel profile
   TODO 021 Improve situation where all layers have zero thickness
   TODO 025 Improve situation where this point has only zero thickness layers
   TODO 026 Check situation where cell in parallel profile is not in a polygon
   TODO 028 Give a warning if raster input layer has several bands
   TODO 038 Do better error handling if insufficient memory
   TODO 053 Improve handling of situation where landward elevation of profile is -ve
   TODO 055 Maybe add a safety check?

##   Theory/Efficiency
   TODO 002 Do we really need D50 for drift landform class? What do we need for drift?
   TODO 005 Maybe give every coast point a value for end-of-profile wave height and direction instead of for deep water wave height and direction
   TODO 010 Do we also need to update the active zone cells?
   TODO 012 Change finding of adjacent polygons, and calculation of the length of shared normals, when we make polygon seaward length determined by depth of closure
   TODO 013 Change calculation (need user input?) of coastline smoothing convexity threshold
   TODO 014 Profile spacing, vould try gradually increasing the profile spacing with increasing concavity, and decreasing the profile spacing with increasing convexity
   TODO 016 Check mass balance for recirculating unconsolidated sediment option
   TODO 023 Only calculate shore platform erosion if cell is in a polygon
   TODO 024 Should we calculate platform erosion on a profile that has hit dry land?
   TODO 037 Need more info on nFindIndex()
   TODO 039 Rewrite reading of multiple random number seeds
   TODO 044 Estuaries :-)
   TODO 046 Why is cliff collapse eroded during deposition (three size classes) no longer calculated?
   TODO 050 Update for recent versions of Windows
   TODO 051 Implement other ways of calculating depth of closure, see TODO 045
   TODO 056 Check this please Andres
   TODO 057 Check this please Manuel
   TODO 058 Dave to check this
   TODO 059 Implement dune landform class
   TODO 060 Remove 'magic numbers' from code here
   TODO 061 Is this safety check to depth of breaking a reasonable thing to do?
   TODO 066 Should this be for all layers? Check
   TODO 067 Is this ever non-zero? Check

##  Output
   TODO 065 Get GPKG output working: currently get floating point exception on pDriver->Create(). Also seems not to support raster overwrite. Will need to convert float to byte RGBA, see e.g. https://www.gamedev.net/forums/topic/486847-encoding-16-and-32-bit-floating-point-value-into-rgba-byte-texture/ And what about gpkg input?
   TODO 063 Add NetCDF support, see https://trac.osgeo.org/gdal/wiki/NetCDF
   TODO 064 Add support for grids that are not oriented N-S and W-E, but are still rectangular (will need to add a transformation in the reading and writing process, the first to bring it to the local base and the second to save it in global coordinates)
   TODO 031 Get raster slice output working with multiple slices
   TODO 032 Improve output scaling for DBL_NODATA situation
   TODO 033 Also test and configure (e.g. by passing open() options) other vector output file formats
   TODO 034 Also test and configure (e.g. by passing open() options) other raster output file formats
   TODO 043 When outputting profiles, how do we deal with randomness of profile spacing (since profile location is determined by curvature)?
   TODO 052 Improve saving of profiles and parallel profiles
   TODO 062 Show end-of-iteration number of cells with sediment somewhere
   TODO 068 Only show output in log file that is relevant to processes being simulated

   068 is max