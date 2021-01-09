# Web Design for a Manufacturing Company
## AIM: 
To design a static website for a chip manufacturing company.

## DESIGN STEPS:
### Step 1: 
Requirement collection.
### Step 2:
Creating the layout using HTML and CSS.
### Step 3:
Updating the sample content.
### Step 4:
Choose the appropriate style and color scheme.
### Step 5:
Validate the layout in various browsers.
### Step 6:
Validate the HTML code.
### Step 6:
Publish the website in the given URL.

## PROGRAM:

### base.html
```
{% load static %}
<!DOCTYPE html>
<html lang="en">

<head>
    <title>Cisco Private Limited</title>
    <link rel="stylesheet" href="{% static 'css/layout.css' %}">
    <link rel = "icon" href ="{% static 'img/titleicon.png' %}" type = "image/x-icon"> 
              
</head>

<body>
    <div class="container">
    <div class="banner">
    Cisco Private Limited.
    </div>
    <div class="menu">
        <div class="menuitem"><a href="/home">Home</a></div> 
        <div class="menuitem"><a href="/products">Products</a></div> 
        <div class="menuitem"><a href="/people">People</a></div>
        <div class="menuitem"><a href="/contactus">Contact us</a></div>
    </div><div class="content">
    {% block content %}    
    {% endblock  %}
    </div>
    <div class="footer">
        Copyright © 2020 Cisco Private Limited, Developed by A.Fawziya.
    </div>
    </div>
</body>

</html>
```

### home.html
```
{% extends "website/base.html" %}

{% block content %}
    <div class="homecontent">    
   <h1><u>About Us</u></h1>
    <img src="/static/img/place.jpg" alt="Building">
    <div class="contenttext">
    Cisco Pvt Ltd, provides a broad range of semiconductor and infrastructure software applications that serve the data center, networking, software, broadband, wireless, and storage and industrial markets. Common applications for its products include: data center networking, home connectivity, broadband access, telecommunications equipment, smartphones, base stations, data center servers and storage, factory automation, power generation and alternative energy systems, displays, and mainframe operations and management, and application software development. Some of Silicon's core technologies and products include:
    <ul>
        <li>Memory Chips</li>
        <li>SATA HDD</li>
        <li>SATA SSD </li>
        <li>Broadband Modems</li>
        <li>Wifi Devices</li>
        <li>Switching Devices</li>
        <li>Optical Sensors</li>
    </ul> 
    </div>
    </div>
{% endblock  %}
```

### products.html
```
{% extends "website/base.html" %}

{% block content %}
    <div class="productcontent">    
    <h1 style="text-align:center;"><u>Our Premium Products</u></h1>
    <div class="productitems">
        <div class="productitem"> 
            <div class="itemimage">
            <img src="/static/img/c1.jpg" alt="product image">
            </div>
           <div class="itemname"><b>4GB DDRA4 laptop memory</b></div>
           <div class="itemprice"><b>Price: Rs.2000.00</b> </div>
        </div>
        <div class="productitem"> 
            <div class="itemimage">
            <img src="/static/img/c2.jpg"  alt="product image">
            </div>
         <div class="itemname"><b>1TB Laptop HDD</b></div>
            <div class="itemprice"><b>Price: Rs.5000.00 </b></div>
        </div>
        <div class="productitem">
            <div class="itemimage">
            <img src="/static/img/levelsensor.png" alt="product image">
            </div>
           <div class="itemname"><b>Optical liquid level sensor</b></div>
           <div class="itemprice"><b>Price: Rs.1299.00</b></div>
        </div>
        <div class="productitem">
            <div class="itemimage">
            <img src="/static/img/memory.jpg" alt="product image">
            </div>
          <div class="itemname"><b>SATA SDD memory chip</b></div>
          <div class="itemprice"><b>Price: Rs.2540.00</b></div>
        </div>
        <div class="productitem">
            <div class="itemimage">
            <img src="/static/img/ramchip.webp" alt="product image">
            </div>
          <div class="itemname"><b>Winbond Electronics - W9464G6KH-5 DRAM Chip</b></div>
         <div class="itemprice"><b>Price: Rs.500.00</b></div>
        </div>
        <div class="productitem">
            <div class="itemimage">
            <img src="/static/img/sensor.png" alt="product image">
            </div>
           <div class="itemname"><b>Proximity sensor</b></div>
          <div class="itemprice"><b>Price: Rs.547</b></div>
        </div>
        <div class="productitem">
            <div class="itemimage">
            <img src="/static/img/switchingdevices.jpg" alt="product image">
            </div>
          <div class="itemname"><b>Switching devices</b></div>
          <div class="itemprice"><b>Price : Rs.899.00</b></div>
        </div>
        <div class="productitem">
            <div class="itemimage">
            <img src="/static/img/sensorgroove.png" alt="product image">
            </div>
          <div class="itemname"><b>Speed Measuring Sensor Groove Coupler Module</b></div>
          <div class="itemprice"><b>Price : Rs.100.00</b></div>
        </div>
        <div class="productitem">
            <div class="itemimage">
            <img src="/static/img/ssd1.png" alt="product image">
            </div>
           <div class="itemname"><b>2913200 Phoenix Contact - Memory - VL 32 GB SSD</b> </div>
           <div class="itemprice"><b>Price : Rs.49000.00</b></div>
        </div>
        <div class="productitem">
            <div class="itemimage">
            <img src="/static/img/wifi2.png" alt="product image">
            </div>
          <div class="itemname"><b>ASUS ZenWiFi</b></div>
          <div class="itemprice"><b>Price : Rs.43990.00</b></div>
        </div>
        <div class="productitem">
            <div class="itemimage">
            <img src="/static/img/broadband.webp" alt="product image">
            </div>
           <div class="itemname"><b>D-link Dir-819 750 Mbps Router</b></div>
          <div class="itemprice"><b>Price : Rs.1,590.00</b></div>
        </div>
        <div class="productitem">
            <div class="itemimage">
            <img src="/static/img/sata1.webp" alt="product image">
            </div>
           <div class="itemname"><b>Wd Green Sata 2.5/7mm Disque 240 Gb Laptop</b></div>
           <div class="itemprice"><b>Price :Rs.3,150.00</b></div>
        </div>
    </div>
    </div>
{% endblock  %}
```

### people.html
```
{% extends "website/base.html" %}

{% block content %}
    <div class="peoplecontent">
        <h1>OUR EXECUTIVES</h1>
    </div>
    <div class="peoplelists">
        <div class="peoplelist">
            <div class="peopleimage">
                <img src="/static/img/michaelgambon.jpg" alt="founder image" width="200" height="300">
            </div>
            <div class="peoplename"><h2>Michael Gambon</h2></div>
            <div class="peoplepost"><h3>(Founder)</h3></div>
        </div>
    
        
    </div>
    <div class="peoplelists">
        <div class="peoplelist">
            <div class="peopleimage">
                <img src="/static/img/alanrick.jpg" alt="CEO image" width="200" height="300">
            </div>
            <div class="peoplename"><h2>Alan Rickman</h2></div>
            <div class="peoplepost"><h3>(Chief Executive Officer)</h3></div>
        </div>
    
       
    </div>
    <div class="peoplelists">
        <div class="peoplelist">
            <div class="peopleimage">
                <img src="/static/img/dan.jpg" alt="COO image" width="200" height="300">
            </div>
            <div class="peoplename"><h2>Daniel Radcliffe</h2></div>
            <div class="peoplepost"><h3>(Chief Operating Officer)</h3></div>
        </div>
    </div>
    
    <div class="peoplelists">
        <div class="peoplelist">
            <div class="peopleimage">
                <img src="/static/img/davidthewlis.jpg" alt="CFO image" width="200" height="310">
            </div>
            <div class="peoplename"><h2>David Thewlis</h2></div>
            <div class="peoplepost"><h3>(Chief Financial Officer)</h3></div>
        </div>
    </div>
    
    <div class="peoplelists">
        <div class="peoplelist">
            <div class="peopleimage">
                <img src="/static/img/tom.jpg" alt="CLO image" width="200" height="310">
            </div>
            <div class="peoplename"><h2>Tom Felton</h2></div>
            <div class="peoplepost"><h3>(Chief Legal Officer)</h3></div>
        </div>
    </div>
    
    <div class="peoplelists">
        <div class="peoplelist">
            <div class="peopleimage">
                <img src="/static/img/oldman.jpg" alt="CMO image" width="230" height="300">
            </div>
            <div class="peoplename"><h2>Gary Oldman</h2></div>
            <div class="peoplepost"><h3>(Chief Marketing Officer)</h3></div>
        </div>
    </div>
{% endblock  %}
```

### contactus.html
```
{% extends "website/base.html" %}

{% block content %}
<div id="img">
<img src="/static/img/cu.jpg" alt="contactus">
</div>
    <h1 class="contactcenter">
        CONTACT
    </h1>
    <h2 class="contactcenter">
    CONTACT ADDRESS: 85 Cowcross St, Farringdon, London EC1M 6PF, United Kingdom<br>
      
    EMAIL ID:ciscocorp@gmail.com<br>
            
       CONTACT NO:9865477236
    </h2>


{% endblock  %}
```

## OUTPUT:
![output](./static/img/Home.png)
![output](./static/img/people.png)
![output](./static/img/p1.png)
![output](./static/img/peop.png)
![output](./static/img/Product.png)
![output](./static/img/contact.png)

## CODE VALIDATION REPORT:
![output](./static/img/reporthome.png)

![output](./static/img/reportpeople.png)

![output](./static/img/reportproduct.png )

![output](./static/img/reportcontact.png)
## RESULT:
Thus a website is designed for the chip manufacturing company and is hosted in the URL http://fawziya.student.saveetha.in:8000/. HTML code is validated.