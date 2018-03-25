MapMyEvents_web is a web implemented (in Flask) Python 3 (3.6.4) script that maps events
 along a route (or for a single location).

Authors: Vasily Kerov (Python)/Alina Shybayeva(Flask/JavaScript/web).

The flow of the Python script:
1. Get trip origin and destination, trip dates, and the keyword from the web page.
2. Submit the origin and the destination to Google Map Directions API and get directions.
3. Parse directions to optimize the route for the next API call to Eventbrite for events.
4. Submit locations from the cleaned directions to Eventbrite and get events.
5. Save them to JSON.
6. Map events using Google Maps JavaScript API.
(upon clicking on the markers an info window pops up with the details of the event)

Install steps:

1. $ python3
2. git clone https://github.com/bazilione/MapMyEvents_web.git
3. cd MapMyEvents_web
4. $ python3 -m venv venv
5. $ virtualenv venv
6. $ source venv/bin/activate
7. (venv) $ pip install flask
8. (venv) $ export FLASK_APP=eventbrite-googlemap.py  
9. (venv) $ pip install flask-wtf requests flask_googlemaps flask_cache
10. (venv) $ flask run

MapMyEvents is currently available on mapmyevents.pythonanywhere.com .
