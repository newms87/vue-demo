# Phase 2 Tasks

## 1. Refactor Audience Panel into a common component
 * Currently it appears as the Audience Panel under the Audience Section, but looks like the code is duplicated in the Search results.
   * Need to re-use the AudiencePanel component in the search results (adding whatever styling / prop changes necessary to make them look the way they are now.)

## 2. Fix framework errors
 * AudienceManager component uses data option without a function, not allowed in VueJS for a component. This is throwing a warning in the console and during compilation.
  
## 3. Import the publishers data for use with the table
 * Add a computed method to format the publisher's data in a usable way for the Table component
 * The mediakits array on each record lists out the available mediakits for each school
   * 1 = Print = newspaper icon
   * 2 = Social = comment icon
   * 3 = Digital = desktop icon
   * 4 = Outdoor = tree icon
   
## 4. Make the table rows selectable (ie: real checkboxes)

## 5. Show the Summary data for the selected rows
  * Sum up the total # of schools selected as the Campuses summary
  * Sum up the total_enrollment field for each school as the Students summary
  * Sum up the number of unique states across all campuses as the States summary
