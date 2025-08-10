# labor-market-proiect

OED Unemployment Rate Liferay Portlet

This project was developed as part of a Java portlet development assessment. It extends a provided basic Liferay portlet to display historical unemployment rate data for Oregon counties using the QualityInfo.org Labor Force API.
Features

    County Selection: Populates a dropdown list of Oregon counties from a web service.

    Dynamic Data Table: Displays seasonally adjusted monthly unemployment rates from January 2018 to the most recent month in 2023, organized by year (rows) and month (columns).

    Server-Side API Calls: Data retrieval handled on the server side due to CORS restrictions.

    Built-in Liferay Support: Uses jQuery 3.3.1 and Bootstrap 4.0 from the Liferay environment.

Tech Stack

    Language: Java (Portlet)

    Frontend: JSP, JavaScript, jQuery, Bootstrap

    Backend: Liferay MVCResourceCommand, Gradle build system

    IDE: Eclipse

    Deployment: Liferay server inside Oracle VirtualBox

API Used

Endpoint Example:

https://www.qualityinfo.org/lmiservice/service/employment/labforce/41/04/{area}/y?periodtype=03&periodyear=2018

Returns labor force statistics for a specified county (area FIPS code) and date range.
How It Works

    User selects a county from the dropdown.

    Portlet sends a request to the backend.

    Backend calls the Labor Force API and returns unemployment data.

    Frontend dynamically updates the table without page reload.

Installation & Demo

    Note: This project was originally developed in a preconfigured VM with Liferay. The steps below assume you have an existing Liferay development environment.

    Clone this repository:

git clone https://github.com/yourusername/oed-unemployment-portlet.git

Open the project in Eclipse.

Ensure your Liferay server is running.

Deploy the project using Gradle:

    gradle deploy

    Navigate to your Liferay site and add the portlet to a page to test.

Disclaimer

This project was created as part of a programming interview exercise and is not an official Oregon Employment Department application. The code here is my original implementation based on a provided technical prompt. No proprietary source code, virtual machines, or internal documentation from OED are included.
