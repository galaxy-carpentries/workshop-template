---
layout: page
title: FIXME                             # (e.g. RNA-Seq Workshop)
topics:
  - FIXME                                # Some topics like "Galaxy Intro", "QC & Mapping"
  - FIXME                                # Don't forget to edit the schedule below!
contact: fixme@example.com               # Your contact email

collaborative_doc: "https://example.org" # Document where collaboration happens for students (e.g. google docs or etherpad.) We've linked to an example document
galaxy_url: https://usegalaxy.eu         # Which Galaxy server you will use
galaxy_name: European Galaxy Server      # The name of the server

organisers:
 - FIXME                                 # The names of your organisers

sponsors:
 - FIXME                                 # The names of your sponsors

site_size: 15                            # How many people you can accomodate at each location
locations:
-
    name: FIXME                                # A name like "Rotterdam", generally just the city name unless something makes more sense
    street: Wytemaweg 80                       # Street (Freeform)
    postal: 3015 CN                            # Post Code (Freeform)
    city: Rotterdam                            # City name (Freeform)
    country: The Netherlands                   # Country (Freeform)
    registration: https://example.org/register # Replace this with your registration form
    # Any more instructions on how to reach the location
    instructions: |
        The workhop will be held in room 1528 on the 15th floor of the Ee
        building. Computers are provided in this room. To enter the building you will
        need to pick up a visitors pass that will be waiting for you at the reception
        of the Ee building (3rd floor).
    geo:
        lat: 51.9108731 # Latitude in decimal degrees, used in displaying a map
        lon: 4.4690001  # Longitude in decimal degrees, used in displaying a map
---

From FIXME to FIXME

## About

This workshop will cover:

<ul>
{% for topic in page.topics %}
<li>{{ topic }}</li>
{% endfor %}
</ul>

**Code of Conduct**: Everyone who participates in Carpentries activities is required to conform to the Code of Conduct. This document also outlines how to report an incident if needed.

**Accessibility**: We are committed to making this workshop accessible to everybody. Please email [{{ page.contact }}](mailto:{{ page.contact }}) for more information.

# Registration

Each location offers {{ page.site_size }} places, and registration is done on a first come, first served basis.

<table class="table">
  <thead>
    <tr>
      <th>City</th>
      <th>Links</th>
    </tr>
  </thead>
  <tbody>
    {% for location in page.locations %}
    <tr>
      <td>{{ location.city }}, {{ location.country }}</td>
      <td><a href="{{ location.registration }}">Register</a>, <a href="#{{ location.name | slugify }}">Location Information</a></td>
    </tr>
    {% endfor %}
  </tbody>
</table>

Registration closes at FIXME. Selected participants will be notified by FIXME.

# Program

Every day the workshop will run from **9:30 (CEST) / 10:30 (EEST)** to **16:30 (CEST) / 17:30 (EEST)** (give or take, depending on questions at the end). If the times will change, it will be announced during the workshop.


**Monday FIXME**

Time (CEST)   | Time (EEST)   | Topic            | Material | Speaker
 ---          | ---           | ---              | ---      | ---
09:30 - 10:00 | 10:30 - 11:00 | Introduction     |          | Individual Sites
10:00 - 12:00 | 11:00 - 13:00 | Session 1        |          |
12:00 - 13:00 | 13:00 - 14:00 | Lunch            |          |
13:00 - 14:30 | 14:00 - 15:30 | Session 2        |          |
14:30 - 16:00 | 15:30 - 17:00 | Session 3        |          |
16:00 - 16:30 | 17:00 - 17:30 | Recap of the day |          | Individual Sites
{:.table.table-striped}


# Important notes

The workshop is free of charge and covers:

- 3 days of training
- Coffee and tea over the days
- Lunch

No stipends for travel or accommodation are available.

Desktop computers will be available. You can also bring your *own notebook* if you prefer . Eduroam is available, ask your institute how to connect.

A **social dinner** will be organised at each site on Tuesday October 8th. This dinner will be at your own cost, but we would love to have a chat with you after the workshop!

# Workshop Format

This will be a **hybrid training**. This means the instructors will teach in front of a camera, and this video feed is live-streamed to multiple locations around the world. Each location will have several other instructors and helpers on site to answer questions and who can take over teaching in case this is needed.

We will use [a collaborative document]({{ page.collaborative_doc }}) for asking and answering questions during the workshop. This document also contains links to all other materials you will need during the course.

# Preparation

The workshop will use the [{{ page.galaxy_name }}]({{ page.galaxy_url }}) to perform all data analysis. Please register there ahead of time to streamline the training.

You must go through two Galaxy interactive tours before beginning the training.
These interactive tours guide you stepwise through the Galaxy user interface
and the history. They will help you to follow the Galaxy introduction, and
ensure everyone has a basic understanding of how Galaxy works.

- [Galaxy UI](https://usegalaxy.eu/tours/core.galaxy_ui)
- [History Introduction](https://usegalaxy.eu/tours/core.history)

# Venues

This workshop will be offered in parallel in these locations:

{% for location in page.locations %}

## {{ location.name }}

{% include map.html location=location showmap=true zoomlevel=15 hidepopup=true %}

{{ location.instructions }}

{% endfor %}

# Organizers, instructors and helpers

{% for organiser in page.organisers %}
- {{ organiser }}
{% endfor %}

The team will be also instructors and helpers there, in addition to local helpers.

# Sponsors

This event is made possible thanks to our supporting partners:

{% for sponsor in page.sponsors %}
- {{ sponsor }}
{% endfor %}
