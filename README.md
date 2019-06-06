# Health and Glow

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

### Line Awesome
	https://icons8.com/line-awesome
Used for icons

### Bootstrap3:
	https://getbootstrap.com/
Uses its prebuilt components in HTML

### Datepicker:
	https://bootstrap-datepicker.readthedocs.io/en/latest/
Used for flexible datepicker widget.

### Selectpicker:
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

 


  
