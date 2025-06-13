![Hero image: Tampa Bay Tech, Entrepreneur, and Nerd Events Builder](./_images/tampa_bay_tech_events_list_builder.jpg)

# The _Tampa Bay Tech Events_ list builder for _Global Nerdy_

Every week, I publish a list of “Tampa Bay tech, entrepreneur, and nerd events” on my blog, [_Global Nerdy_](https://www.globalnerdy.com/). I use this Jupyter Notebook to automate as much of the process as possible.


This is one of those utility projects where I’m the only user. The code’s complete, but the documentation is in progress.

## Installation

### 1. Install the prequisites
This application requires:

- [Python](https://www.python.org/), version 3.8 or later.
- [Jupyter Lab/Notebook(https://jupyter.org/)] or [Visual Studio Code](https://code.visualstudio.com/) with the [Jupyter plugin](https://code.visualstudio.com/docs/datascience/jupyter-notebooks) installed.
- _Global Nerdy_, which is a Wordpress blog. This utility uses the [WordPress REST API](https://developer.wordpress.org/rest-api/) to create the blog post for the upcoming week’s list of events. You can repurpose its code to generate event lists on your WordPress blog — just change the URL to the one for your blog and provide the appropriate login credentials (the username for someone with permissions to create posts and an [application password](https://melapress.com/wordpress-application-passwords/) for the blog) in the `.env` file. _Note that an application password is NOT THE SAME THING as a user password!_
- A Meetup.com account and a Facebook account. This app scrapes Meetup.com using my Meetup.com account, and it uses my Facebook account to log into Meetup.com.

### 2. Create an `.env` file
This application expects an `.env` file with four values defined within:

- `FACEBOOK_USERNAME`: Username for Facebook account associated with Meetup account
- `FACEBOOK_PASSWORD`: Password for that Facebook account
- `WORDPRESS_USERNAME`: Username for account on the Wordpress blog with posting permissions
- `WORDPRESS_APP_PASSWORD`: An app password for the Wordpress blog. Once again, an app password is a password specifically for applications that acces sthe blog using the WordPress REST API. [Read here for more details.](https://melapress.com/wordpress-application-passwords/)

### 3. Run the cells in the Jupyter Notebook
The cells are divided into two sections:

1. The first section automates the creation of a blog post that will house the upcoming week’s tech events list.
2. The second section automates much of the process of creating the table containing the list of tech events for a given day.

[ This part of the README is a work in progress. I’ll be updating regularly, so watch this space! ]