# Preprocessing

1.  Scrape data from <http://denkmalverzeichnis.magdeburg.de/KID/DenkmalDetailInfoMitBild.asp?id=1> for all IDs: [scraper.py](scraper.py)
2.  Geocode the addresses with <https://developer.mapquest.com>: [geocode.py](geocode.py)
3.  Split up each location into individual files and one file that only contains the id and GPS location for each location: [splitup.js](splitup.js). I only discoverd afterwards that splitting the data into individual files would be a good way to avoid to use a database.
4.  I discovered only very late that I can't embed their images. They are served only via HTTP and we use HTTPS. That's why I downloaded all the images and serve them from my server.
