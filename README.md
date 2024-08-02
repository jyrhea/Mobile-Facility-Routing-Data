# Mobile-Facility-Routing-Data
Data for the manuscript "Mobile Facility Routing for Equitable Service of Covered Stochastic Demand"

There are three main data sources for this work: the capacitated team orienteering problem (CTOP) / capacitated profitable tour problem (CPTP) instances from Archetti et al. (2009), urban pickup-and-delivery instances from Ulmer et al. (2021), and close enough vehicle routing problem (CEVRP) instances from Mennell et al. (2009).

CTOP/CPTP: Each .cri file holds the location of the depot and each customer. Within this file, the first column is latitude, the second column is longitude. 
Each p*datafilename*.cri file houses the corresponding list of parking locations called parkingLocs-*datafilename*.txt. 
The demand for each customer in each period across 1000 realizations is located in file distribList-*datafilename*-p*numPeriods*.csv, where the number of periods (numPeriods) is 3 or 5. Within the file, the first column corresponds to the customer, the second column is the period, and the third column is the realized demand. 

Urban: The UrbanLocs.csv file contains customer locations. The coordinates for the CID airport are used to represent the location of the depot. The number of customers (numCust) considered in our experiments are 50, 100, 150, 200, 250, 300, 400, and 500. These numbers are used to identify the parking list and 1000 demand realizations for each collection of customers (parkingLocs-IC*numCust*.txt and distribList-IC*numCust*-p*numPeriods*.csv, respectively). 

CEVRP: Each *datafilename*.txt file (that does not include "distribList" or "parkingLocs") holds the customer and depot location for the given instance. Each "distribList" and "parkingLocs" file holds the customer demand over 1000 realizations and the parking locations, respectively, for each set of customers.
