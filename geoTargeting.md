# Geo Targeting #

We are using a free ip-to-country datatabase available at <a href='http://ip-to-country.webhosting.info/node/view/6'><a href='http://ip-to-country.webhosting.info/node/view/6'>http://ip-to-country.webhosting.info/node/view/6</a></a>.

Determining whether to serve the banner is implemented in db/procs/is\_valid\_country.sql


## NOTE ##
We are refactoring geo targeting by country to use MaxMind's GeoLite Country (http://www.maxmind.com/app/geolitecountry) and adding GeoLite City (http://www.maxmind.com/app/geolitecity) .