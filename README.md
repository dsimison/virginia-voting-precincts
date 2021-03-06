<meta name="google-site-verification" content="40S93IIlLJok-0QCMvjzt784RiVlVB9q2mJvrDsnfUA" />

![image](https://user-images.githubusercontent.com/20375915/66695942-3aa9ce80-ec95-11e9-945c-38ee19456de0.png)

The purpose of this project is to create a database with shapefiles of Virginia voting precinct boundaries for all primary and general elections from 2009-2020.

Voting district (VTD) shapefiles from the [US Census Bureau](https://www.census.gov/programs-surveys/geography.html) were used as a starting point to create these maps. Data was then collected for all precinct changes between each election to make a shapefile for every year. This information was obtained from county and city GIS data and Codes of Ordinances, precinct and district-level [voter registration statistics](https://www.elections.virginia.gov/resultsreports/registrationturnout-statistics/), and [election results](https://apps.elections.virginia.gov/SBE_CSV/ELECTIONS/ELECTIONRESULTS/) and [turnout data](https://apps.elections.virginia.gov/SBE_CSV/ELECTIONS/ELECTIONTURNOUT/) from the [Virginia Department of Elections](https://www.elections.virginia.gov/resultsreports/).

All maps were created using [QGIS](https://www.qgis.org/en/site/).  
Encoding: EPSG 4326.  

Please see the [Virginia Voting Precincts Wiki](https://github.com/erikalopresti/virginia-voting-precincts/wiki) for more information and a full list of sources.
## Table of Contents

1. [Shapefiles](#shapefiles)

   [File naming convention](#file-naming-convention)  
   [Years and Elections available](#years-and-elections-available)  
   
2. [Attributes](#attributes)  

   [Shapefile attributes](#shapefile-attributes)  
   [Split precinct map attributes](#split-precinct-map-attributes)  
   
3. [Full index of files](#full-index-of-files)  

   [Files by year](#files-by-year)   
   [Files by type](#files-by-type)  
   
4. [Sources](#sources)  

## Shapefiles
### File naming convention
(YYYY = year, mon = month).  
`va_precincts_YYYY_nov_general` - Precinct boundaries for the November General Election.  
`va_precincts_YYYY_jun_primary` - Precinct boundaries for the June Primary Election.  
`va_precincts_YYYY_mon_split_by_CD` - Displays precincts split by Congressional district boundaries as separate features.  
`va_precincts_YYYY_mon__split_by_SD` - Displays precincts split by Senate of Virginia district boundaries as separate features.  
`va_precincts_YYYY_mon__split_by_HD` - Displays precincts split by Virginia House of Delegates district boundaries as separate features.  
### Years and Elections available
[View repository on Github](https://github.com/erikalopresti/virginia-voting-precincts)
- **2019-2020** - November General, clipped shoreline, split by CD, split by SD, split by HD
- **2018** - November General, June Primary, split by CD
- **2017** - November General, split by CD, split by HD
- **2016** - November General, split by CD
- **2015** - November General, split by SD, split by HD
- **2014** - November General, split by CD
- **2013** - November General, split by CD, split by HD
- **2012** - November General, split by CD
- **2011** - November General, split by SD, split by HD
- **2009-2010** - November General, split by CD, split by HD
## Attributes
### Shapefile attributes
`precinctID` - Corresponds to the VTDID for VTDs in US Census Bureau files.  
`precinctCo` - Precinct code. Corresponds to the VTDST in US Census Bureau files.  
`precinct` - Precinct name.  
`localityCo` - Locality code. Corresponds to the COUNTYFP in US Census Bureau files.  
`locality` - Name of the locality (county or independent city).  
`congDist` - Congressional district current for the map year.  
`senateDist` - Senate of Virginia district current for the map year.  
`hodDist` - House of Delegates district current for the map year.  
`actVoters` - Number of active registered voters in the precinct and district.  
`precUid` - PrecinctUid given in the .csv files of Election Results from the VA Dept. of Elections.  
`localUid` - LocalityUid given in the .csv files of Election Results from the VA Dept. of Elections.  
`changeDate` - Date of last known change to the precinct boundaries, name or number.  
`lastChange` - Last known change to the precinct boundaries, name or number.  
### Split precinct map attributes
`distSplits` - District splits within the precinct.  
`cdPrecinct` - PrecinctID prefixed by Congressional district number.  
`sdPrecinct` - PrecinctID prefixed by Senate of Virginia district number.  
`hdPrecinct` - PrecinctID prefixed by House of Delegates district number.  
## Full Index of Files
[View repository on Github](https://github.com/erikalopresti/virginia-voting-precincts)
### Files by Year
#### [Virginia voting precincts: 2019-2020](https://github.com/erikalopresti/virginia-voting-precincts/tree/master/maps/va-precinct-shapefiles-2019-2020)
`va_precincts_2019_2020`  
`va_precincts_2019_clipped_shore`  
`va_precincts_2020_split_by_CD`  
`va_precincts_2019_split_by_SD`  
`va_precincts_2019_split_by_HD`  
#### [Virginia voting precincts: 2018](https://github.com/erikalopresti/virginia-voting-precincts/tree/master/maps/va-precinct-shapefiles-2018)
`va_precincts_2018_nov_general`  
`va_precincts_2018_nov_split_by_CD`  
`va_precincts_2018_jun_primary` (coming soon)  
#### [Virginia voting precincts: 2017](https://github.com/erikalopresti/virginia-voting-precincts/tree/master/maps/va-precinct-shapefiles-2017)
`va_precincts_2017_nov_general`  
`va_precincts_2017_nov_split_by_CD`  
`va_precincts_2017_nov_split_by_HD`  
#### [Virginia voting precincts: 2016](https://github.com/erikalopresti/virginia-voting-precincts/tree/master/maps/va-precinct-shapefiles-2016)
`va_precincts_2016_nov_general`  
`va_precincts_2016_nov_split_by_CD`  
#### [Virginia voting precincts: 2015](https://github.com/erikalopresti/virginia-voting-precincts/tree/master/maps/va-precinct-shapefiles-2015)
`va_precincts_2015_nov_general`  
`va_precincts_2015_nov_split_by_HD`  
`va_precincts_2015_nov_split_by_SD`  
#### [Virginia voting precincts: 2014](https://github.com/erikalopresti/virginia-voting-precincts/tree/master/maps/va-precinct-shapefiles-2014)
`va_precincts_2014_nov_general`  
`va_precincts_2014_nov_split_by_CD`  
#### [Virginia voting precincts: 2013](https://github.com/erikalopresti/virginia-voting-precincts/tree/master/maps/va-precinct-shapefiles-2013)
`va_precincts_2013_nov_general`  
`va_precincts_2013_nov_split_by_CD`  
`va_precincts_2013_nov_split_by_HD`  
#### [Virginia voting precincts: 2012](https://github.com/erikalopresti/virginia-voting-precincts/tree/master/maps/va-precinct-shapefiles-2012)
`va_precincts_2012_nov_general`  
`va_precincts_2012_nov_split_by_CD`  
#### Virginia voting precincts: 2011 (coming soon)
`va_precincts_2011_nov_general`  
`va_precincts_2011_nov_split_by_HD`  
`va_precincts_2011_nov_split_by_SD`  
#### Virginia voting precincts: 2009-2010 (coming soon)
`va_precincts_2009_2010`  
`va_precincts_2009_2010_split_by_CD`  
`va_precincts_2009_2010_split_by_HD`  
#### [Virginia magisterial districts: 2011-2020](https://github.com/erikalopresti/virginia-voting-precincts/tree/master/maps/va-magisterial-district-shapefiles)
`va_magisterial_districts_2011_2020`  
### Files by Type
#### November General Election precincts
`2019-2020`, `2018`, `2017`, `2016`, `2015`, `2014`, `2013`, `2012`, `2011`, `2009-2010`
#### June Primary Election precincts
`2019-2020`, `2018`
#### Precincts split by Congressional District
`2019-2020`, `2018`, `2017`, `2016`, `2014`, `2013`, `2012`, `2009-2010`
#### Precincts split by VA Senate District
`2019-2020`, `2015`, `2011`
#### Precincts split by VA House of Delegates District
`2019-2020`, `2017`, `2015`, `2013`, `2011`, `2009-2010`
## Sources
[Full list of sources](https://github.com/erikalopresti/virginia-voting-precincts/wiki/Sources)
