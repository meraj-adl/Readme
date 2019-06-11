
## Project setup

    virtualenv hng
    cd hng
    . bin/activate
    pip install django
    django-admin startproject project
Rename project folder to ProjectContainer

    mv project ProjectContainer

Install requests

    pip install requests
For starting new app

    python manage.py startapp app_name
 The above steps will be common in all django project initialization.

### project/settings.py configurations

In `project/settings.py` add/change the following line

    STATIC_URL = '/static/'
    STATIC_ROOT = 'project/static'
    ALLOWED_HOSTS = ['127.0.0.1', 'hng.adl-icm.com'] 
    # 127.0.0.1 for running local development project
    # hng.adl-icm.com for running through url

## Requiremnets
### Django
Django framework

### requests
	

    pip install requests
Used in `views.py` for accessing request object

### unidecode
	pip install unidecode
For handling non-ascii character

###  jquery
	https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js
JavaScript library used for html dom element accessing and manipulation

### Slider
	https://jqueryui.com/slider/
Used in insights for sliding chart that can not fit in one screen

### Line Awesome
	https://icons8.com/line-awesome
Used for icons

### Bootstrap3
	https://getbootstrap.com/
Uses its prebuilt components in HTML

### Datepicker
	https://bootstrap-datepicker.readthedocs.io/en/latest/
Used for flexible datepicker widget.

### Selectpicker
	https://developer.snapappointments.com/bootstrap-select/
Used for single select, multi select selectpicker

### Datatable
	https://datatables.net/
Used for showing tables with pagination, searching, sorting

### CanvasJS
	https://canvasjs.com/
Chart library
Used for drawing chart
Used in insights page

### Alert
	https://sweetalert2.github.io/
Used for customized pop up
Used for success/error message

### BlockUI
	http://malsup.com/jquery/block
Used for blocking UI element and prevent interaction.
It is used in blocking form when no customers/rule sets are selected


### SVG.js
	https://svgjs.com/
Used for drawing svg. 
It is used in heatmap page

### Material Icon css
	https://fonts.googleapis.com/icon?family=Material+Icons
For using material icons

### Google Font
	https://fonts.googleapis.com/css?family=Roboto
For using Roboto font

## Things to learn
- Django
	- Django settings file
	- Django Templates
	- Django Static files 
	- Handling HTTP requests in Django
	- Django url, views
- Python
- JavaScript
	- JSON parsing
	- grep
	- map
	- filter		
	- promise
	- arrow function
- jQuery
	- ajax
	- selectors
	- events
	- append/prepend
	- dom manipulation
	- css
- Bootstrap
- CSS
	- Selectors
	- Display
	- Position
	- Float

 
## How to match data daily
### Insights:
In "Footfalls and dwell time by day of month" chart, data should be present upto yesterday for each store.

### Insights vs Universe:
#### Compare "Customer composition by number of visits" chart and Customer Universe

`Total customers:` Total customers should match for each customer type filter(registered, unregistered, all) for "all store" filter and each store(1st check for "all store" filter)

`Visitwise customer count:` For each visit(1 visit, 2 to 5 visits, 6 to 10 visits, more than 10 visits), customer count should be matched for each store and each customer type(1st check for "all store" filter)

### Insights vs Flow:
#### Compare "Store-wise customer composition: Customer who visited" chart and Customer Flow(Set Interval period filter to "Month")

`Monthwise customer count:` For each 4 months(current month and previous 3 months), total customer count should match for each store and each customer type(1st check for "all store" filter)

### Insights vs Rule sets:
#### Compare "Customer composition by number of visits" chart and Rule sets

Check with "all store" store filter and each customer filter(registered, unregistered, all) in insights "Customer composition by number of visits" chart.

`Total customer count:` Registered customer count, Unegistered customer count and total customer count should match(Don't apply any filter in Rule sets and change customer filter in insights)

`Visitwise customer count:` In rule set, apply "Total number of visits" filter and check for each visits(1,2,3,4,5,6-10,>10), total customer count should match(Apply "Total number of visits" filter in Rule sets and change customer filter in insights) 

`Life cycle stage wise customer count:` In rule set, apply "Life cycle stage" filter and check for each life cycle stage(new, active, passive, lapsed), total customer count should match(Apply "Life cycle stage" filter in Rule sets and change customer filter in insights)

`Visit + Lifecycle stage:` Combine above two. In rule set, apply "Total number of visits" filter and "Life cycle stage" filter, and check for for each visits(1,2,3,4,5,6-10,>10) and each life cycle stage(new, active, passive, lapsed), total customer count should match(Apply "Total number of visits" filter and "Life cycle stage" filter in Rule sets and change customer filter in insights)

### Insights vs Metrics:
#### Compare "Store-wise customer composition: Customer who visited" chart with Metrics
Apply "all" customer filer in insights and change store filter for each store and compare with metrics for that store and month

Change store filter in insights. For each store and each month(current and last 3 months), total customer in insights(above bar in insights) and unique customers in metrics(visible after clicking +) should match


#### Compare "Store-wise customer composition: Customer who didn't visited" chart with Metrics
Apply "all" customer filer in insights and change store filter for each store and compare with metrics for that store and month

Change store filter in insights. For each store and each month(current and last 3 months), total customer in insights(Customer who didn't visited) and sum "Visited earlier to store, repeat to network and not visited to store" + "Visited earlier to store, not visited to store or network" in metrics should match


  
