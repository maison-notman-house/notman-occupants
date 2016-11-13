# notman-occupants

Metadata for Notman occupants, both people and organizations.  Browse the directory at [maison-notman-house.github.io/notman-occupants/](https://maison-notman-house.github.io/notman-occupants/).

![screenshot](https://maison-notman-house.github.io/notman-occupants/images/screenshot.jpg)

This project was initiated as part of [HackTheHouse 3](http://maison-notman-house.github.io/) and inspiration for this directory comes from [Sniffypedia](https://sniffypedia.org/).


## Structured, Linked Data

Each occupant is represented as structured, linked data in the form of JSON-LD and Schema.org.  This is the format championed by the major search engines.  For example, the OSMO Foundation is represented at [Organizations/OSMO_Foundation](https://maison-notman-house.github.io/notman-occupants/Organization/OSMO_Foundation/), which has the JSON-LD and Schema.org embedded in the human-readable webpage.  The machine-readable JSON-LD and Schema.org can be extracted via a program such as [cormorant](http://reelyactive.github.io/cormorant/?url=https://maison-notman-house.github.io/notman-occupants/Organization/OSMO_Foundation/) ([repository](https://github.com/reelyactive/cormorant)).

    {
      "@context": {
        "schema": "http://schema.org/"
      },
      "@graph": [
        {
          "@id": "organization",
          "@type": "schema:Organization",
          "schema:name": "OSMO Foundation",
          "schema:url": "https://maison-notman-house.github.io/notman-occupants/Organization/OSMO_Foundation/",
          "schema:logo": "https://maison-notman-house.github.io/notman-occupants/Organization/OSMO_Foundation/768x768.jpg",
          "schema:sameAs": []
        }
      ]
    }

In the example of the OSMO Foundation, the above enables computers to understand:
- the organization's name
- the organization's logo
- the organization's social media links (which would be in the "sameAs" array)


## Using the occupants directory in your web application

You can get the latest directory for your web application by importing the index.js file in the <head> of your HTML file:

    <script src="https://maison-notman-house.github.io/notman-occupants/js/index.js"></script>

Then in your Javascript, you'll have access to the following two arrays:
- notman_organizations
- notman_people

See [the index](https://maison-notman-house.github.io/notman-occupants/js/index.js) for the latest values of the above.


## Adding occupants

You can add an occupant in the Organization or Person folder of this repository.  Simply copy an existing organization or person and update the relevant fields in the index.html file (title and JSON-LD).  You can also add a square image.


## License

MIT License

Copyright (c) 2016 HackTheHouse

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR 
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, 
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE 
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER 
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, 
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN 
THE SOFTWARE.

