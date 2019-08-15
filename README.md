# IDS-BLUProject
 Github repo for the Bike Lane Uprising class project

#Requirements 
(from Sergey's project Readme)
"The final project should represent original work applying data science techniques to an interesting problem. You own your final projects, but you should be talking frequently with your instructor and classmates about them."

"Address a data-related problem in any field you're passionate about. If you care about the subject matter, you'll create a better project and it will be a lot more fun for you!"

"You can either use [publicly available data](public_data.md) or your own data that you can legally share with the rest of the class. Competing in a data science/stats competition (INCLUDING ANY PAST COMPETITIONS) is also a project option."

#Introduction: 
This project will analyze a publically available data set to determine if traffic tickets being issued in Chicago for obstruction of bike lanes are actually correlated with complaints of bike lane obstruction in that city.  I am working with Bike Lane Uprising to assist me in identification of datasets and geoidentification.  https://www.bikelaneuprising.com.  

#Update8-5: 
Given the time constraints, I have only been able to perform an analysis of the first set (ProPublica)

#Update8-12
Today I discovered the dataset I've been using the zipcode for has the zipcode for the where the vehicle is registered, not where the ticket violation occurred.  That changes the analysis.  


For this, I have two publically available datasets.  


#Dataset #1: 
ProPublica's analysis of Chicago traffic ticket issuance.  This data can be downloaded at: https://www.propublica.org/datastore/dataset/chicago-parking-ticket-data.  I have included the data compressed in  my repository, but I believe it will not be posted when I make the repo public as it exceeds the size requirements, so I have used only a sample of the data available (2000 rows) to do a proof of concept.  

#Dataset #2: 
311 Service Requests: https://data.cityofchicago.org/Service-Requests/311-Service-Requests/v6vf-nfxy
I was not able to analyze this data yet.  

#Geographic identification
 (for mapping tickets to their location): City of Chicago's Data Portal for geographic identirication (the City Data Portal a lot of cool public data and Github repositories!): https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Boundaries-ZIP-Codes/gdcf-axmw
    
**write-up** 
    1. What is the question you hope to answer?

Ultimate goal: 
The purpose of this data analysis is to determine whether there is a way to improve public safety by 
identifying areas of bike lane obstruction (as represented by the 311 complaint database) and correlating it with the actual tickets being written (represented by the ProPublica data).  The city also has the opportunity to increase revenue through parking tickets by identifying places where there are bike lane obstructions.  

The ultimate goal of this project is to identify: 
1. Where are tickets being written
2. Where are bike lane obstructions being written (edited) 
new messages
3. Where are 311 reports for bike lane obstructions located
4. Is there a correlation to those zones?

But for the purposes of this course...
Proof of Concept goal: analyze where are the vehicles registered for which there are traffic tickets being written.  See if there are "hotspots" for ownership.  

    2. What data are you planning to use to answer that question?

The parking ticket data being utilized is from the ProPublica data set.  https://www.propublica.org/datastore/dataset/chicago-parking-ticket-data

The bike lane obstruction data is from the 311 data.  https://data.cityofchicago.org/Service-Requests/311-Service-Requests/v6vf-nfxy

The geographic maps of the area are from the City Data Portal.  https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Boundaries-ZIP-Codes/gdcf-axmw

    3. What do you know about the data you're using so far?

The ProPublica data:

The traffic ticket data that ProPublica obtained from the City of Chicago Department of Finance was enriched by interviews with the Finance Department in order to establish the data dictionary.  The license plate numbers are hashed to anonymize the data.  

In terms of the features available for this dataset, the zipcode data is unstructured.  There are some Zip plus 4 data and some 5 digit zipcode data, as well as some empty fields, and some errors ("IL" for zipcode).  Review of the data dictionary reveals that rather than containing the violation_location zipcode, in fact, it contains the zipcode of the vehicle registration.  


    4. Why did you choose this topic?

I had always been an avid cyclist, and upon moving to Chicago from Los Angeles, it became my primary mode of transport.  The density and flatness of the city, as well as the advocacy of the community and lower street speeds, made cycling a logical choice.  However, in 2014, while transporting my daughter to her daycare on my bike, we were forced over to the curb by a motorist who was angered that we were able to pass in the bike lane while they were queued up waiting at a red light.  When the light changed, they sped ahead of us and cut us off by suddenly pulling to the curb.  After verbally chastising me for endangering my child by cycling with her, they then crossed four lanes of traffic to make a left turn in under a block.  However, although we had photos and a full license plate, the Police Department declined to take a report of the incident. 

Since the CPD declined to record this data, a community group, Bike Lane Uprising, was founded to take data on these kinds of reports. BLU also more commonly records bike lane obstructions and needs for maintenance, and helps promote greater safety.  For example, we are working with a local shopping center developer to get their parking circle geofenced so that Uber / Lyft / rideshare vehicles know to pick up at the parking circle rather than loading in the bike lane, which then forces the bike traffic to suddenly merge with faster moving vehicle traffic.  

With this data, we can go to city stakeholders and present our case more concretely: this location is blocked at this time by these delivery vehicles, or this area needs better enforcement with ticket writers, or this bike lane is obstructed due to poor road conditions.  

    5. Lessons Learned:
    
First lesson: always always always, read the data dictionary first.  Just because the column is named doesn't mean what you think -- I discovered this the hard way when I finally got the 7GB set loaded, only to discover that the zipcode meant the vehicle registration zipcode, not where the violation occurred.  

Second, double check the data in the field, because even if the data dictionary 

Third, data cleansing will suck down 90% of the available time.  
