Nepal Schools MapBox and Tilemill
=================================

[Computer Resources](#computer-resources)
[Evacuation Map Displayed?](#evacuation-map-displayed)


Computer Resources
------------------
###CSS###
```
#school {  
  marker-fill:#e6e6e6;
  marker-fill-opacity: 0.5;  
  marker-line-color:black;
  marker-width: 15;
  marker-line-width: 2;
  marker-allow-overlap:true;
  [Working_Computer_Lab="Y"]{marker-fill:#C994C7}
  [Student_Internet_Access="Y"]{marker-fill:#DD1C77}  
  [zoom >= 11] {
    marker-width:30;  	  
  }
}
```
###Legend###
```
<div class="legend-title">
Computer Resources
</div>
<div class="items">
    <span class='swatch_none'></span>
    <span class="label">No computers or not working</span> <br>
    <span class='swatch_lab'></span>
    <span class="label">Working computer lab</span> <br>
    <span class='swatch_internet'></span>
    <span class="label">Working lab and student internet access</span> <br>
<div class="note"><em>(Mouseover for school name and number of computers.)</em></div>
</div>  

<style type="text/css">
.swatch_none, .swatch_lab, .swatch_internet {
    height: 16px;
    margin-right: 5px;
    margin-left: 5px;
    display: table-cell;
    vertical-align:middle;
    text-align: center;
    width: 16px;
    display: inline-block;
}
.swatch_none {
    background:#e6e6e6;
}
.swatch_lab {
    background:#C994C7;
}
.swatch_internet {
    background:#DD1C77;
}
.legend-title{
    text-align:center;
    margin-bottom: 5px;    
    font-weight:bold;
    font-size:110%
}
.note {
    margin-left: 5px;
    margin-top: 3px;
}
.wax-legend {
  max-width: 400px !important;
  width: 400px !important;  
  font-size: larger;
}
</style>
```
###Teaser###
```
<div class="schoolname">{{{Name_of_Core_School}}}</div>
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/infrastructure_school_32px_icon_bluebox.png">
Working Computer Lab: <strong>{{{Working_Computer_Lab}}}</strong>
</div>
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/activity_information_technology_32px_icon_bluebox.png">
Number of Computers: <strong>{{{Number_of_Computers}}}</strong>
</div>
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/telecommunications_internet_32px_icon_bluebox.png">
Student Internet Access: <strong>{{{Student_Internet_Access}}}</strong>
</div>

<style>
img {
    float: left;
    margin: 3px 5px;
    height: 25px;
}
.tooltip-item{
    height:31px; 
}
.schoolname {
    font-weight: bold;
    text-decoration: underline;
    text-align: center;
    margin-bottom: 8px;
}
.map-tooltip {
  width: 270px !important;
  font-size: larger;
  max-height: none !important;
} 
</style>
```

Evacuation Map Displayed?
-------------------------
###CSS###

