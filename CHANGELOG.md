## ResStock v2.3.0 (pending)

Features
- Update the multifamily project with a Geometry Wall Type tsv file for sampling between wood stud and masonry walls ([#382](https://github.com/NREL/OpenStudio-BuildStock/pull/382))

Fixes
- Refactor the RECS tsv makers for years 2009 and 2015 ([#382](https://github.com/NREL/OpenStudio-BuildStock/pull/382))

## ResStock v2.2.0
###### January 30, 2020 - [Diff](https://github.com/NREL/OpenStudio-BuildStock/compare/v2.1.0...v2.2.0)

Features
- The results csv now optionally reports annual totals for all end use subcategories, including appliances, plug loads, etc. ([#371](https://github.com/NREL/OpenStudio-BuildStock/pull/371))
- Split out national average options so not all homes have all miscellaneous equipment, and add none options to appliances ([#362](https://github.com/NREL/OpenStudio-BuildStock/pull/362))
- Update the single-family detached project with a Geometry Wall Type tsv file for sampling between wood stud and masonry walls ([#357](https://github.com/NREL/OpenStudio-BuildStock/pull/357))
- Made housing characteristics a consistent format. Added integrity check to ensure housing characteristics follow the guildelines specified in read-the-docs ([#353](https://github.com/NREL/OpenStudio-BuildStock/pull/353))
- Include additional "daylight saving time" and "utc time" columns to timeseries csv file to account for one hour forward and backward time shifts ([#346](https://github.com/NREL/OpenStudio-BuildStock/pull/346))
- Update bedrooms and occupants tsv files with options and probability distributions based on RECS 2015 data ([#340](https://github.com/NREL/OpenStudio-BuildStock/pull/340))
- Add new QOIReport measure for reporting seasonal quantities of interest for uncertainty quantification ([#334](https://github.com/NREL/OpenStudio-BuildStock/pull/334))
- Separate tsv files for bedrooms, cooking range schedule, corridor, holiday lighting, interior/other lighting use, pool schedule, plug loads schedule, and refrigeration schedule ([#338](https://github.com/NREL/OpenStudio-BuildStock/pull/338))

Fixes
- Allow Wood Stove option as an upgrade, and account for wood heating energy in simulation output ([#372](https://github.com/NREL/OpenStudio-BuildStock/pull/372))
- Custom meters for ceiling fan, hot water recirc pump, and vehicle end use subcategories were not properly implemented ([#371](https://github.com/NREL/OpenStudio-BuildStock/pull/371))
- Some re-labeling of tsv files, such as "Geometry Building Type" to "Geometry Building Type RECS" and "Geometry Building Type FPL" to "Geometry Building Type ACS" ([#356](https://github.com/NREL/OpenStudio-BuildStock/pull/356))
- Removes option "Auto" from parameter "Occupants" in the options lookup file ([#360](https://github.com/NREL/OpenStudio-BuildStock/pull/360))
- Update the multifamily project's neighbors and orientation tsv files to have geometry building type dependency; remove the now obsolete "Geometry Is Multifamily Low Rise.tsv" file ([#350](https://github.com/NREL/OpenStudio-BuildStock/pull/350))
- Update each PAT project's AMI selection to "2.9.0" ([#346](https://github.com/NREL/OpenStudio-BuildStock/pull/346))
- Fixes for custom output meters: total site electricity double-counting exterior holiday lighting, and garage lighting all zeroes ([#349](https://github.com/NREL/OpenStudio-BuildStock/pull/349))
- Remove shared facades tsv files from the multifamily_beta and testing projects ([#301](https://github.com/NREL/OpenStudio-BuildStock/pull/301))
- Move redundant output meter code from individual reporting measures out into shared resource file ([#334](https://github.com/NREL/OpenStudio-BuildStock/pull/334))
- Fix for the power outages measure where the last hour of the day was not getting the new schedule applied ([#238](https://github.com/NREL/OpenStudio-BuildStock/pull/238))

## ResStock v2.1.0
###### November 5, 2019 - [Diff](https://github.com/NREL/OpenStudio-BuildStock/compare/v2.0.0...v2.1.0)

Features
- Update to OpenStudio v2.9.0 ([#322](https://github.com/NREL/OpenStudio-BuildStock/pull/322))
- Unit tests and performance improvements for integrity checks ([#228](https://github.com/NREL/OpenStudio-BuildStock/pull/228), [#237](https://github.com/NREL/OpenStudio-BuildStock/pull/237), [#239](https://github.com/NREL/OpenStudio-BuildStock/pull/239))
- Register climate zones (BA and IECC) based on the simulation EPW file ([#245](https://github.com/NREL/OpenStudio-BuildStock/pull/245))
- Split ResidentialLighting into separate ResidentialLightingInterior and ResidentialLightingOther (with optional exterior holiday lighting) measures ([#244](https://github.com/NREL/OpenStudio-BuildStock/pull/244), [#252](https://github.com/NREL/OpenStudio-BuildStock/pull/252))
- Additional example workflow osw files using TMY/AMY2012/AMY2014 weather for use in regression testing ([#259](https://github.com/NREL/OpenStudio-BuildStock/pull/259), [#261](https://github.com/NREL/OpenStudio-BuildStock/pull/261))
- Update all projects with new heating/cooling setpoint, offset, and magnitude distributions ([#272](https://github.com/NREL/OpenStudio-BuildStock/pull/272))
- Add new ResidentialDemandResponse measure that allows for 8760 DR schedules to be applied to heating/cooling schedules ([#276](https://github.com/NREL/OpenStudio-BuildStock/pull/276))
- Additional options for HVAC, dehumidifier, clothes washer, misc loads, infiltration, etc. ([#264](https://github.com/NREL/OpenStudio-BuildStock/pull/264), [#278](https://github.com/NREL/OpenStudio-BuildStock/pull/278), [#292](https://github.com/NREL/OpenStudio-BuildStock/pull/292))
- Add EV options and update ResidentialMiscLargeUncommonLoads measure with new electric vehicle argument ([#282](https://github.com/NREL/OpenStudio-BuildStock/pull/282))
- Update ResidentialSimulation Controls measure to include a calendar year argument for controlling the simulation start day of week ([#287](https://github.com/NREL/OpenStudio-BuildStock/pull/287))
- Increase number of possible upgrade options from 10 to 25 ([#273](https://github.com/NREL/OpenStudio-BuildStock/pull/273), [#293](https://github.com/NREL/OpenStudio-BuildStock/pull/293))
- Additional "max-tech" options for slab, wall, refrigerator, dishwasher, clothes washer, and lighting ([#296](https://github.com/NREL/OpenStudio-BuildStock/pull/296))
- Add references to ResStock trademark in both the license and readme files ([#302](https://github.com/NREL/OpenStudio-BuildStock/pull/302))
- Report all cost multipliers in the SimulationOutputReport measure ([#304](https://github.com/NREL/OpenStudio-BuildStock/pull/304))
- Add options for low flow fixtures ([#305](https://github.com/NREL/OpenStudio-BuildStock/pull/305))
- Add argument to BuildExistingModel measure that allows the user to ignore measures ([#310](https://github.com/NREL/OpenStudio-BuildStock/pull/310))
- Create example project yaml files for use with buildstockbatch ([#291](https://github.com/NREL/OpenStudio-BuildStock/pull/291), [#314](https://github.com/NREL/OpenStudio-BuildStock/pull/314))
- Create a pull request template to facilitate development ([#317](https://github.com/NREL/OpenStudio-BuildStock/pull/317))
- Update documentation to clarify downselect logic parameters ([#321](https://github.com/NREL/OpenStudio-BuildStock/pull/321))
- Additional options for EnergyStar clothes washer, clothes dryer, dishwasher ([#329](https://github.com/NREL/OpenStudio-BuildStock/pull/329), [#333](https://github.com/NREL/OpenStudio-BuildStock/pull/333))

Fixes
- Bugfix for assuming that all simulations are exactly 365 days ([#255](https://github.com/NREL/OpenStudio-BuildStock/pull/255))
- Bugfix for heating coil defrost strategy ([#258](https://github.com/NREL/OpenStudio-BuildStock/pull/258))
- Various HVAC-related fixes for buildings with central systems ([#263](https://github.com/NREL/OpenStudio-BuildStock/pull/263))
- Update testing project to sweep through more options ([#280](https://github.com/NREL/OpenStudio-BuildStock/pull/280))
- Updates, edits, and clarification to the documentation ([#270](https://github.com/NREL/OpenStudio-BuildStock/pull/270), [#274](https://github.com/NREL/OpenStudio-BuildStock/pull/274), [#285](https://github.com/NREL/OpenStudio-BuildStock/pull/285))
- Skip any reporting measure output requests for datapoints that have been registered as invalid ([#286](https://github.com/NREL/OpenStudio-BuildStock/pull/286))
- Bugfix for when bedrooms are specified for each unit but bathrooms are not ([#295](https://github.com/NREL/OpenStudio-BuildStock/pull/295))
- Ensure that autosizing does not draw the whole tank volume in one minute for solar hot water storage tank ([#307](https://github.com/NREL/OpenStudio-BuildStock/pull/307))
- Remove invalid characters from option names for consistency with buildstockbatch ([#308](https://github.com/NREL/OpenStudio-BuildStock/pull/308))
- Bugfix for ducts occasionally getting placed in the garage attic instead of only unfinished attic ([#309](https://github.com/NREL/OpenStudio-BuildStock/pull/309))
- Able to get past runner values of any type, and not just as string ([#312](https://github.com/NREL/OpenStudio-BuildStock/pull/312))
- Log the error message along with the backtrace when an applied measure fails ([#315](https://github.com/NREL/OpenStudio-BuildStock/pull/315))
- Add tests to ensure that the Run Measure argument is correctly defined in all Apply Upgrade measures for all projects ([#320](https://github.com/NREL/OpenStudio-BuildStock/pull/320))
- Bugfix when specifying numbers of bedrooms to building units ([#330](https://github.com/NREL/OpenStudio-BuildStock/pull/330))
- Enforce rubocop as CI test so code with offenses cannot be merged ([#331](https://github.com/NREL/OpenStudio-BuildStock/pull/331))
- Bugfix for some clothes washer, dishwasher options causing increased energy consumption ([#329](https://github.com/NREL/OpenStudio-BuildStock/pull/329), [#333](https://github.com/NREL/OpenStudio-BuildStock/pull/333))


## ResStock v2.0.0
###### April 17, 2019 - [Diff](https://github.com/NREL/OpenStudio-BuildStock/compare/v1.0.0...v2.0.0)

Features
- Update to OpenStudio v2.8.0 ([#151](https://github.com/NREL/OpenStudio-BuildStock/pull/151))
- Add a multifamily project which includes housing characteristic distributions for single-family detached, single-family attached, and multifamily buildings ([#151](https://github.com/NREL/OpenStudio-BuildStock/pull/151))
- Ability to add central systems (boiler with baseboards, fan coil, PTAC) to multifamily buildings using the openstudio-standards gem ([#151](https://github.com/NREL/OpenStudio-BuildStock/pull/151))
- Ability to simulate large multifamily buildings using "collapsed" buildings with multipliers on building units ([#206](https://github.com/NREL/OpenStudio-BuildStock/pull/206))
- Automatically generate dependency graphs and a dependency wheel for each project ([#211](https://github.com/NREL/OpenStudio-BuildStock/pull/211))
- Add measures for calculating construction properties, modeling power outages and calculating resilience metrics, and calculating utility bills ([#151](https://github.com/NREL/OpenStudio-BuildStock/pull/151))
- Add measure for modeling shared multiifamily facades using adiabatic constructions ([#151](https://github.com/NREL/OpenStudio-BuildStock/pull/151))
- Relocate all measure unit tests, test osw files, and test osm files from archived OpenStudio-BEopt and into this repository ([#151](https://github.com/NREL/OpenStudio-BuildStock/pull/151))
- Create example workflow osw files for single-family detached, single-family attached, and multifamily buildings using TMY weather ([#151](https://github.com/NREL/OpenStudio-BuildStock/pull/151))

Fixes
- Reporting measures read from ReportMeterData table to get disaggregated fan and pump energy ([#151](https://github.com/NREL/OpenStudio-BuildStock/pull/151))
- Break out central system heating, cooling, and pump energy in reporting measures ([#151](https://github.com/NREL/OpenStudio-BuildStock/pull/151))
- Use custom unit conversions script instead of that provided by OpenStudio SDK ([#216](https://github.com/NREL/OpenStudio-BuildStock/pull/216))


## ResStock v1.0.0
###### April 17, 2019
