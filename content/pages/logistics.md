---
$title: Travel & Schedule
$order: 2
events:
- day: Schedule for Saturday, 10/19/2013
  place: Paradise Ridge Winery
  place_url: https://www.google.com/maps/preview#!q=Paradise+Ridge+Winery%2C+4545+Thomas+Lake+Harris+Drive%2C+Santa+Rosa%2C+CA&data=!1m4!1m3!1d12345!2d-122.7269103!3d38.4916597!4m22!1m9!4m8!1m3!1d99757!2d-122.4376!3d37.7577!3m2!1i1296!2i759!4f13.1!5m11!1m10!1sParadise+Ridge+Winery%2C+4545+Thomas+Lake+Harris+Drive%2C+Santa+Rosa%2C+CA!4m8!1m3!1d99757!2d-122.4376!3d37.7577!3m2!1i1296!2i759!4f13.1
  times:
  - time: 5:00pm
    content: Family and friends arrive
  - time: 5:30pm
    content: Wedding ceremony
  - time: 6:30pm
    content: Hors d'oeuvres and mingling
  - time: 7:00pm
    content: Dinner
  - time: 9:00pm
    content: Dancing and merriment
---
<h2>Wedding venue</h2>
<p>Our wedding will take place at <b>Paradise Ridge Winery</b> in Santa Rosa, California! Santa Rosa is about a 90 minute drive north of San Francisco. It is located in California's wine country.

<h2>Airports</h2>
<p>There are a few airports that you can use. The most popular airport nearby is the San Francisco International Airport (SFO), but you may also choose to fly into Oakland (OAK) or Sacramento (SMF).
<p>If you are flying from California (or nearby) on Alaska Airlines, you may choose to fly into Sonoma County Airport (STS) directly, which is only 15 minutes away from Santa Rosa.
<p>If you choose to fly in on Saturday morning, there will be enough time for you to rent a car at any of the nearby airports and travel to Santa Rosa in time for the ceremony.

<h2>Hotels</h2>

<h3>Hilton Sonoma Wine Country</h3>
<p>This is the hotel where the wedding party will stay. It is a 5-minute to both the wedding venue and downtown Santa Rosa.
<p><a href="http://www.hiltonsonomahotel.com/">http://www.hiltonsonomahotel.com/</a>
<p>
<p>Other hotels nearby include:

<h3>Hyatt Santa Rosa</h3>
<p>This hotel is located in downtown Santa Rosa, a 10-minute drive to the wedding venue.
<p><a href="http://vineyardcreek.hyatt.com/en/hotel/home.html?icamp=vineyardcreekredirect">http://vineyardcreek.hyatt.com/</a>

<h3>Courtyard Marriott Santa Rosa</h3>
<p>This hotel is located in downtown Santa Rosa (right next to the Hyatt), a 10-minute drive to the wedding venue.
<p><a href="http://www.marriott.com/hotels/travel/stscy-courtyard-santa-rosa/">http://www.marriott.com/hotels/travel/stscy-courtyard-santa-rosa/</a>

{% if doc.events %}
  {% for event in doc.events %}
  <h2>{{event.day}}</h2>
  {% if event.place %}
    <p><a href="{{event.place_url}}">{{event.place}}</a>
  {% endif %}
    <table>
      {% for time in event.times %}
        <tr>
          <td>{{time.time}}
          <td>{{time.doc}}
      {% endfor %}
    </table>
  {% endfor %}
{% endif %}
