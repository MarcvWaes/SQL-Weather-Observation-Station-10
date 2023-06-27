# SQL-Weather-Observation-Station-10

# Challenge:
- Query the list of CITY names from STATION that do not end with vowels. Your result cannot contain duplicates.

- The STATION table is described as follows:

![n1e5uock jot](https://github.com/MarcvWaes/SQL-Weather-Observation-Station-3/assets/120553175/93033af8-77bd-460d-bf7b-fce39386b9e6)

- Where LAT_N is the northern latitude and LONG_W is the western longitude.

# Solution:
- SELECT DISTINCT CITY
- FROM STATION
- WHERE LOWER(SUBSTRING(CITY, -1)) NOT IN ('a', 'e', 'i', 'o', 'u');

- By utilizing LOWER(SUBSTRING(CITY, -1)), we extract the last character of the CITY name using the SUBSTRING function and convert it to lowercase using the LOWER function. Then we check if this lowercase last character is not present in the set of vowels. This approach allows us to exclude CITY names that end with both uppercase and lowercase vowels.
 
# Output:
- Kissee Mills
- Loma Mar
- Sandy Hook
- Tipton
- Arlington
- Turner
- Slidell
- Negreet
- Chignik Lagoon
- Hanna City
- .....
