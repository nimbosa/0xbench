# Table of Contents #


# Introduction #

Beside saving or benchmarking results to the SD Card (either plain text or XML), 0xbench can also upload your results to a web service that provide visual representation of your results.This article explains in detail the steps needed to upload and how to interpret the results.

# Upload #
After finish running all selected benchmark cases, you can upload your run results to the 0xBench Web service for visual representation and statistically analysis.
Each page in the 0xBench Web can display multiple runs of benchmark results from the same phone or multiple phones.

## To Default Benchmark Page ##
  1. Complete running selected benchmarking cases
  1. Return to main view and click "Upload"
  1. Uncheck "Login", and click the "Send" button
  1. Point your browser to the URL reported on your phone

## Create Your Own Page ##
> New method: Login to Google directly on your phone, no need to type API keys anymore.

> ![http://farm5.static.flickr.com/4144/4970650742_8c9b551af6_m.jpg](http://farm5.static.flickr.com/4144/4970650742_8c9b551af6_m.jpg)
  1. On your phone, check the "Login" checkbox and press the "Login for API-key" button.
  1. Enter your Google account and password to login.
  1. Press "Confirm" to auto-fill Email and API key in the form.
  1. Choose a desire benchmark page name to create or enter an existing page name to upload to.
  1. Click send to upload results to specified page.
> ![http://farm5.static.flickr.com/4090/4970650784_2faa63054a_m.jpg](http://farm5.static.flickr.com/4090/4970650784_2faa63054a_m.jpg)

> Old method: If you are having trouble logging in to Google on your phone.

> ![http://farm5.static.flickr.com/4077/4861799761_08a5839b28_m_d.jpg](http://farm5.static.flickr.com/4077/4861799761_08a5839b28_m_d.jpg)
  1. Use any browser to point to http://0xbenchmark.appspot.com/ .
  1. Login with your google account to acquire an API key.
  1. On your phone, check the "Login" checkbox and enter your email address, API key.
  1. Choose a desire benchmark page name to create or enter an existing page name to upload to.
  1. Click send to upload results to specified page.
> ![http://farm5.static.flickr.com/4080/4862419094_290c97347c_d.jpg](http://farm5.static.flickr.com/4080/4862419094_290c97347c_d.jpg)

# Web Interface #
![http://farm5.static.flickr.com/4143/4858834355_ee039998e2_d.jpg](http://farm5.static.flickr.com/4143/4858834355_ee039998e2_d.jpg)

There are five regions in the Web Interface. The Tabbar at the top selects different benchmark categories to display.

The Option Section controls how the Main Table (third section) will be displayed. Detail of the option section will be explained in latter sections of this article.

The Main Table display results of multiple runs (uploads). Each benchmarking case is presented with a average performance number, and different types of graph representation. All the cases are also assigned with tags so that it's visibility can be controlled via the Option Section.

The Runs Section display details of different runs, including benchmark execution date/time, phone model, kernel version, etc. You can also name/rename or delete a run, if you are the page owner.

At the bottom the Tag Section lists all benchmarking cases with corresponding tags assigned to it.

## Options ##
![http://farm5.static.flickr.com/4080/4858978287_b54c7ec75b_o_d.png](http://farm5.static.flickr.com/4080/4858978287_b54c7ec75b_o_d.png)

The Options Section controls how the Main Table is displayed. These controls include:
  * The visibility of runs and benchmarking cases can be control directly or via tags.
  * Tagging mode (union or filtering)
  * Type of graph to display (bar graph, distribution, distribution (accumulated), or statistics)
  * Bar graphs should be comparing locally (cases within same run) or globally (all cases in all runs)
  * Page permission control
The Permission Field in the Options Section controls who have access to this page. The page owner can enter a semicolon separated list of gmail accounts to grant access. Including a "public" string in the list of account names will open the benchmark page to the public, regardless of whether the user is in the list or not.

## Visualization ##
### Bar Graph ###
![http://farm5.static.flickr.com/4074/4858980485_ab56b63f50_o_d.png](http://farm5.static.flickr.com/4074/4858980485_ab56b63f50_o_d.png)

If a benchmarking case if consists of multiple result values, the bar graph can display five different values, using different colors and T indicators:
  1. The left-side T indicates the minimum measured value.
  1. The left-hand edge of the lighter-colored sections is the first quartile. 25% of the measurements are below this value; 75% are above it.
  1. The middle edge that divides the two lighter-colored sections is the median. 50% of the measurements are below this value; 50% are above it.
  1. The right-hand edge of the lighter-colored sections is the third quartile. 75% of the measurements are below this value; 25% are above it.
  1. The right-side T indicates the maximum measured value.
Many bars will not have all of these features. In that case, the omitted feature is not interesting: it is equal to the adjacent value. If all measurements are exactly equal, then the minimum, first-quartile, median, third-quartile and maximum will all be together at the bar's end.

(some part of the text in this section is adapted from caliper project wiki, more information of bar graph can be found [here](http://mathworld.wolfram.com/Box-and-WhiskerPlot.html))
### Distribution Graph ###
![http://farm5.static.flickr.com/4136/4858980301_526bd061b7_o_d.png](http://farm5.static.flickr.com/4136/4858980301_526bd061b7_o_d.png)


### Distribution Graph (accumulated) ###
![http://farm5.static.flickr.com/4096/4859601266_c125d8b864_o_d.png](http://farm5.static.flickr.com/4096/4859601266_c125d8b864_o_d.png)

### Statistic ###
![http://farm5.static.flickr.com/4114/4859192513_4d8b6a796f_d.jpg](http://farm5.static.flickr.com/4114/4859192513_4d8b6a796f_d.jpg)