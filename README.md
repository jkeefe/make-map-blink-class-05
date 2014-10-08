#Tiled Maps: Green Taxis in NYC

###FILES USED: green_taxis.zip (be sure to unzip it!)

- Download Tilemill from http://mapbox.com/tilemill
- Launch Tilemill
- Pick "New Project"
- Give it a name (no spaces) like green_taxis
- Give it a title, like Green Taxi Pickups
- Leave everything else as-is

Now we see a map. Quick tour.

- Get yourself zoomed in to the NYC area
- Note that it's a "rough sketch" of the countries
- Click the stack of papers/layers in the lower left
- Choose "add layer"

We're adding a file

- give it a short ID, like "pickups"
- leave Class blank
- on the Datasource line, click the "Browse" button and go find your green_taxis.shp file from the zipped file
- click done
- leave the other fields as-is
- click "Save & Style" (the middle button)

OK! Now to styling!

Let's make the borders of the markers disappear. We don't need 'em for clairty.

- add `marker-line-width: 0;` to "pickups" and  hit "Save"

We can't see how many dots are stacked up on each other. Let's try making them half-transparent

- add `marker-opacity: 0.5;` to pickups and hit save.

Getting better! But let's try even more transparent:

- add `marker-opacity: 0.08;` to pickups and hit save.

Let's save our "bounding box" (it'll save us hassle later)

- click on the wrench in the upper right
- zoom in to the data (go down to zoom level 10 for now)
- shift-click-drag a box across the data
- click the center of the box to drop a "center" pin (will have a label like Z10)
- change the "zoom" bar on the right to go from 2 to 16 (dragging each end)
- add a name at the top if you wish
- hit save

First, let's get rid of the countries. We could just delete those lines, but in case we need them, let's "comment them out" -- which turns them into notes instead of code.

Do that by putting a /* at the start of the section and a */ to end it. So like this:

	/*
	#countries {
	  ::outline {
	    line-color: #85c5d3;
	    line-width: 2;
	    line-join: round;
	  }
	  polygon-fill: #fff;
	}
	*/

- click save

OK, let's play with the colors!

- change the background color to #666
- change the marker-fill color to #a5f706

Cool!

Finally, let's mek the marker width a little smaller:

- change to marker-width:3;


Now, you can upload this to Mapbox.
You'll need a free Mapbox account
Go to http://mapbox.com

- Back in Tilemill, first we want to comment-out the background (so we upload only the data layer)

	/*
	Map {
	  background-color: #666;
	}
	*/

- click save
- now use the "Export button"
- Choose "upload"
- Sign in
- ignore the early time estimates (like 6 days!)

Back on the mapbox site, click Projects and make a new project

- create project
- zoom into new york
- play with the colors of the land, streets and areas
- add the data layer by using Data -> (stack icon) -> Add Layers
- get embed code by using Project button