Nepal Schools - MapBox and Tilemill
===================================

[Computer Resources](#computer-resources)  
[Evacuation Map Displayed?](#evacuation-map-displayed)  
[Health Services and First-Aid](#health-services-and-first-aid)  
[Infrastructure Issues](#infrastructure-issues)  
[Non-Core Schools in Area](#non-core-schools-in-area)  
[Reported Hazards](#reported-hazards)  
[Students per Teacher](#students-per-teacher)  
[Type](#type)  

Computer Resources
------------------
######updated Sep 19, 2013######
###CSS: Computer Resources###
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
###Legend: Computer Resources###
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
###Teaser: Computer Resources###
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
######updated Sep 25, 2013######
######[Back to List of Maps](#nepal-schools-mapbox-and-tilemill)######
###CSS: Evacuation Map Displayed?###
```
#school {  
  marker-fill:#ff7b00;
  marker-fill-opacity: 0.8;  
  marker-line-color:black;
  marker-width: 15;
  marker-line-width: 1;
  marker-allow-overlap:true;
  [Evacuation_Map_Displayed="Y"]{
    marker-file: url(icons/map-10.svg);
    marker-fill: #005aff;    
    marker-width: 15;   
    [zoom >= 12]{
      marker-width: 40; 
    }
  }   
}
```
###Legend: Evacuation Map Displayed?###
```
<div class="legend-title">
Evacuation Map Displayed in School?
</div>
Blue map marker indicates that the school has an evacuation map displayed.  
<div class="note"><em>(Mouseover for core school name, district, and reported hazards.)</em></div>
</div> 
   
<style type="text/css">
.legend-title{
    text-align:center;
    margin-bottom: 3px;    
    font-weight:bold;
}
.note {
    margin-left: 5px;
    margin-top: 3px;
}
.wax-legend {
  width: 300px !important;
  font-size: larger;
}
</style>
```
###Teaser: Evacuation Map Displayed?###
```
<div class="schoolname">{{{Name_of_Core_School}}} ({{{District}}} District)</div>
Evacuation map displayed? {{{Evacuation_Map_Displayed}}}<br>
<u>Reported Hazards</u>:<br>
{{#Earthquake}}
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/disaster_earthquake_32px_icon_bluebox.png">
Earthquake
</div>
{{/Earthquake}}
{{#Road_Accident}}
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/security_carjacking_32px_icon_bluebox.png">
Road Accident 
</div>
{{/Road_Accident}}
{{#Windstorm}}
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/disaster_violent_wind_32px_icon_bluebox.png">
Windstorm
</div>
{{/Windstorm}}
{{#Fire}}
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/disaster_fire_32px_icon_bluebox.png">
Fire
</div>
{{/Fire}}
{{#Epidemic}}
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/disaster_epidemic_32px_icon_bluebox.png">
Epidemic
</div>
{{/Epidemic}}
{{#LandSlide}}
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/disaster_landslide_32px_icon_bluebox.png">
Landslide
</div>
{{/LandSlide}}
</wrap>
{{#Cold}}
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/disaster_cold_wave_32px_icon_bluebox.png">
Cold
</div>
{{/Cold}}
{{#Sanitation}}
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/disaster_technological_32px_icon_bluebox.png">
Sanitation
</div>
{{/Sanitation}}
{{#Lightning}}
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/disaster_storm_32px_icon_bluebox.png">
Lightning
</div>
{{/Lightning}}
{{#Flood}}
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/disaster_flood_32px_icon_bluebox.png">
Flood
</div>
{{/Flood}}

<style>
.schoolname {
    font-weight: bold;
    text-decoration: underline;
    text-align: center;
    margin-bottom: 8px;
}
.map-tooltip {  
  font-size: larger;  
} 
img {
    float: left;
    margin: 3px 5px;
    height: 25px;
}
.tooltip-item{
    height:31px; 
}
.map-tooltip {
  min-width: 270px !important;
  font-size: larger;
  max-height: none !important;
} 
</style>
```

Health Services and First-Aid?
------------------------------
######updated Sep 23, 2013######
###CSS: Health Services and First-Aid?###
```
#school {  
  marker-file: url(icons/map-marker-6.svg); 
  marker-fill:#00ffa5;
  marker-fill-opacity: 0.6;  
  marker-line-color:black;
  marker-width: 15;
  marker-line-width: 2;
  marker-allow-overlap:true;
  [Health_Services="Y"]{marker-fill:#c51020}  
  [zoom >= 12] {
    marker-width:30;  	  
  }
}
```
###Legend: Health Services and First-Aid?###
```
<div class="legend-title">
Health Services at Schools
</div>
<div class="items">
    <span class='swatch_no'></span>
    <span class="label">No Health Services</span> <br>
    <span class='swatch_yes'></span>
    <span class="label">Health Services</span><br>
<div class="note"><em>(Mouseover for school name and number of basic first-aid trained individuals.)</em></div>
</div>   

<style type="text/css">
.swatch_no, .swatch_yes {
    height: 16px;
    margin-right: 5px;
    margin-left: 5px;
    display: table-cell;
    vertical-align:middle;
    text-align: center;
    width: 16px;
    display: inline-block;
}
.swatch_no {
    background:#00ffa5;
}
.swatch_yes {
    background: rgba(197, 16, 32, 0.7);
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
  width: 400px !important;
  font-size: larger;
}
</style>
```
###Teaser: Health Services and First-Aid?###
```
<div class="schoolname">{{{Name_of_Core_School}}}</div><br>
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/cluster_health_32px_icon_bluebox.png">
Health Services? <strong>{{{Health_Services}}}</strong>
</div>
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/food_NFI_medical_supply_32px_icon_bluebox.png">
Basic First-Aid Trained Individuals:
</div>
<div class="sublist">
<ul>
<li><strong>{{{Basic_FA_Trained_Teacher_Sponsors}}}</strong> teacher sponsors</li>
<li><strong>{{{Basic_FA_Trained_Teachers}}}</strong> teachers</li> 
<li><strong>{{{Basic_FA_Trained_Students}}}</strong> students</li>
</ul>
</div>

<style>
img {
    float: left;
    margin: 3px 5px;
    height: 25px;
}
.wrap {
    font-size: larger;
}
.tooltip-item{
    height:31px; 
}
.sublist{
    text-indent: 50px;
    
}
.schoolname {
    font-weight: bold;
    text-decoration: underline;
    text-align: center;
}
.map-tooltip {
  width: 300px !important;
  font-size: larger;
  max-height: none !important;
  max-width: none !important;
}
</style>
```

Infrastructure Issues
---------------------
######updated Sep 25, 2013######
###CSS: Infrastructure Issues###
```
#school {  
  marker-width: 20;
  marker-allow-overlap:true;
  marker-file: url(icons/damage_destroyed_64px_icon_redbox.png);
  [Infrastructure_Issues="None"]{
      marker-file: url(icons/damage_building_not_affected_64px_icon_bluebox.png);
      marker-fill: #005aff;     
  }
  [zoom >= 12]{
      marker-width: 35; 
  }
  [zoom >= 14]{
      marker-width: 45; 
  }  
}
```
###Legend: Infrastructure Issues###
```
<div class="legend-title">
Infrastructure Issues at Schools
</div>
<div class="legend-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/damage_building_not_affected_32px_icon_bluebox.png">
None
</div>
<div class="legend-item">
<img src="https://raw.github.com/AmericanRedCross/maptemplates/master/nepal/icons/damage_destroyed_64px_icon_redbox.png">
Yes
</div>
<div class="note"><em>(Mouseover for school name and list of infrastructure issues.)</em></div>  

<style type="text/css">
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
  width: 400px !important;
  font-size: larger;
}
img {
    float: left;
    margin: 3px 5px;
    height: 25px;
}
.legend-item {
    height:32px; 
}
</style>
```
###Teaser: Infrastructure Issues###
```
<div class="schoolname">{{{Name_of_Core_School}}}</div>
Infrastructure Issues: <b>{{{Infrastructure_Issues}}}</b><br>
({{{District}}} District)

<style>
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

Non-Core Schools in Area
------------------------
######updated Sep 18, 2013######
###CSS: Non-Core Schools in Area###
```
#school {  
  marker-fill:#ECE7F2;
  marker-fill-opacity: 0.5;  
  marker-line-color:black;
  marker-width: 17;
  marker-line-width: 2;
  marker-allow-overlap:true;
  [Number_of_NonCore_Schools_in_Area>5]{marker-fill:#A6BDDB}
  [Number_of_NonCore_Schools_in_Area>10]{marker-fill:#2B8CBE}  
  ::labels {
  	text-name:"[Number_of_NonCore_Schools_in_Area]";
    text-face-name:"Arial Bold";
    text-allow-overlap:true;
    text-size: 12;
  }
  [zoom >= 11] {
    marker-width:30;
    ::labels {
      text-size: 18;
    }
  }
  [zoom >= 13] {
    marker-width:45;
    ::labels {
      text-size: 26;
    }
  }    
}
```
###Legend: Non-Core Schools in Area###
```
<div class="legend-title">
Number of Non-Core Schools in Area
</div>
<div class="items">
    <span class='swatch_0to5'></span>
    <span class="label">2-5</span> <br>
    <span class='swatch_6to10'></span>
    <span class="label">6-10</span> <br>
    <span class='swatch_11plus'></span>
    <span class="label">11-15</span> <br>
<div class="note"><em>(Mouseover for core school name and district.)</em></div>
</div> 

<style type="text/css">
.swatch_0to5, .swatch_6to10, .swatch_11plus {
    height: 16px;
    margin-right: 5px;
    margin-left: 20px;
    display: table-cell;
    vertical-align:middle;
    text-align: center;
    width: 16px;
    display: inline-block;
}
.swatch_0to5 {
    background:#ECE7F2;
}
.swatch_6to10 {
    background:#A6BDDB;
}
.swatch_11plus {
    background:#2B8CBE;
}
.legend-title{
    text-align:center;
    margin-bottom: 3px;    
    font-weight:bold;
}
.note {
    margin-left: 5px;
    margin-top: 3px;
}
.wax-legend {
  width: 300px !important;
  font-size: larger;
}
</style>
```
###Teaser: Non-Core Schools in Area###
```
<div class="wrap">
<strong>{{{Name_of_Core_School}}}</strong> in <strong>{{{District}}}</strong> district has <strong>{{{Number_of_NonCore_Schools_in_Area}}}</strong> non-core schools in the area. 
</div>

<style>
.wrap{
    font-size: larger;
}
</style>
```

Reported Hazards
----------------
######updated Sep 20, 2013######
###CSS: Reported Hazards###
```
#school {  
  marker-fill:#f45;
  marker-fill-opacity: 0.6;
  marker-line-opacity: 0.6;
  marker-line-color:black;
  marker-allow-overlap:true;
  [Number_Hazards=2]{marker-fill:#ffffb2; marker-width:11;}
  [Number_Hazards=3]{marker-fill:#fecc5c; marker-width:12;}
  [Number_Hazards=4]{marker-fill:#fd8d3c; marker-width:13;}
  [Number_Hazards=5]{marker-fill:#f03b20; marker-width:14;}
  [Number_Hazards=6]{marker-fill:#bd0026; marker-width:15;}
  [zoom >=11] {
    [Number_Hazards=2]{marker-fill:#ffffb2; marker-width:21;}
    [Number_Hazards=3]{marker-fill:#fecc5c; marker-width:22;}
    [Number_Hazards=4]{marker-fill:#fd8d3c; marker-width:23;}
    [Number_Hazards=5]{marker-fill:#f03b20; marker-width:24;}
    [Number_Hazards=6]{marker-fill:#bd0026; marker-width:25;}
  }
}
```
###Legend: Reported Hazards###
```
<div class="legend-title">
Number of Reported Hazards
</div>
<div class="items">
    <span class='swatch_2'></span>
    <span class="label">2</span> <br>
    <span class='swatch_3'></span>
    <span class="label">3</span> <br>
    <span class='swatch_4'></span>
    <span class="label">4</span> <br>
    <span class='swatch_5'></span>
    <span class="label">5</span> <br>
    <span class='swatch_6'></span>
    <span class="label">6</span> <br>
<div class="note"><em>(Mouseover for school name and type of reported hazards.)</em></div>
</div> 

<style type="text/css">
.swatch_2, .swatch_3, .swatch_4, .swatch_5, .swatch_6 {
    height: 16px;
    margin-right: 5px;
    margin-left: 20px;
    display: table-cell;
    vertical-align:middle;
    text-align: center;
    width: 16px;
    display: inline-block;
}
.swatch_2 {
    background:#ffffb2;
}
.swatch_3 {
    background:#fecc5c;
}
.swatch_4 {
    background:#fd8d3c;
}
.swatch_5 {
    background:#f03b20;
}
.swatch_6 {
    background:#bd0026;
}
.legend-title{
    text-align:center;
    margin-bottom: 5px;    
    font-weight:bold;
    font-size:110%
}
.note {
    margin-left: 20px;
    margin-top: 3px;
}
.wax-legends {
  max-width: 300px !important;
  width: 300px !important;  
  font-size: larger;
}
</style>
```
###Teaser: Reported Hazards###
```
<wrap>
<div class="schoolname">{{{Name_of_Core_School}}}</div>
<u>Reported Hazards</u>:<br>
{{#Earthquake}}
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/disaster_earthquake_32px_icon_bluebox.png">
Earthquake
</div>
{{/Earthquake}}
{{#Road_Accident}}
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/security_carjacking_32px_icon_bluebox.png">
Road Accident 
</div>
{{/Road_Accident}}
{{#Windstorm}}
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/disaster_violent_wind_32px_icon_bluebox.png">
Windstorm
</div>
{{/Windstorm}}
{{#Fire}}
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/disaster_fire_32px_icon_bluebox.png">
Fire
</div>
{{/Fire}}
{{#Epidemic}}
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/disaster_epidemic_32px_icon_bluebox.png">
Epidemic
</div>
{{/Epidemic}}
{{#LandSlide}}
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/disaster_landslide_32px_icon_bluebox.png">
Landslide
</div>
{{/LandSlide}}
</wrap>
{{#Cold}}
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/disaster_cold_wave_32px_icon_bluebox.png">
Cold
</div>
{{/Cold}}
{{#Sanitation}}
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/disaster_technological_32px_icon_bluebox.png">
Sanitation
</div>
{{/Sanitation}}
{{#Lightning}}
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/disaster_storm_32px_icon_bluebox.png">
Lightning
</div>
{{/Lightning}}
{{#Flood}}
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/disaster_flood_32px_icon_bluebox.png">
Flood
</div>
{{/Flood}}

<style>
.schoolname {
    font-weight: bold;
    text-decoration: underline;
    text-align: center;
    margin-bottom: 8px;
}
img {
    float: left;
    margin: 3px 5px;
    height: 25px;
}
.wrap {
    font-size: larger;
}
.tooltip-item{
    height:31px; 
}
.map-tooltip {
  min-width: 270px !important;
  font-size: larger;
  max-height: none !important;
} 
</style>
```

Students per Teacher
--------------------
######updated Sep 19, 2013######
###CSS: Students per Teacher###
```
#school {
  [Students_per_Teacher >= 0] {marker-fill: #ffe0a4; marker-width:9;}
  [Students_per_Teacher >= 20] {marker-fill: #ADDD8E; marker-width:12;}
  [Students_per_Teacher >= 30] {marker-fill: #31A354; marker-width:14;}
  [zoom >= 11] {
    [Students_per_Teacher >= 0] {marker-width:15;}
  	[Students_per_Teacher >= 20] {marker-width:25;}
  	[Students_per_Teacher >= 30] {marker-width:35;}   
  }
  [zoom >= 13] {
    [Students_per_Teacher >= 0] {marker-width:25;}
  	[Students_per_Teacher >= 20] {marker-width:35;}
  	[Students_per_Teacher >= 30] {marker-width:45;}   
  }  
  marker-line-color:#fff;
  marker-line-width: 1;
  marker-fill-opacity: 0.6;
  marker-line-opacity: 0.6;
  marker-allow-overlap:true;
}
```
###Legend: Students per Teacher###
```
<div class="legend-title">
Students per Teacher
</div>
<div class="items">
    <span class='swatch_1'></span>
    <span class="label">9.6 - 19.9</span> <br>
    <span class='swatch_2'></span>
    <span class="label">20.0 - 29.9</span> <br>
    <span class='swatch_3'></span>
    <span class="label">30.0 - 55.6</span> <br>
<div class="note"><em>(Mouseover for school name and specific numbers.)</em></div>
</div>

<style type="text/css">
.swatch_1, .swatch_2, .swatch_3 {
    height: 16px;
    margin-right: 5px;
    margin-left: 20px;
    display: table-cell;
    vertical-align:middle;
    text-align: center;
    width: 16px;
    display: inline-block;
}
.swatch_1 {
    background:#FFE0A4;
}
.swatch_2 {
    background:#ADDD8E;
}
.swatch_3 {
    background:#31A354;
}
.legend-title{
    text-align:center;
    margin-bottom: 5px;    
    font-weight:bold;
    font-size:110%
}
.note {
    margin-left: 20px;
    margin-top: 3px;
}
.wax-legend {
  max-width: 300px !important;
  width: 300px !important;  
  font-size: larger;
}
</style>
```
###Teaser: Students per Teacher###
```
<div class="schoolname">{{{Name_of_Core_School}}}</div>
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/activity_training_32px_icon_bluebox.png">
Number of Teachers: <strong>{{{Number_of_Teachers}}}</strong>
</div>
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/people_children_32px_icon_bluebox.png">
Number of Students: <strong>{{{Student_Population}}}</strong>
</div>
<div class="tooltip-item">
<img src="http://mw1.google.com/crisisresponse/icons/un-ocha/activity_staff_management_32px_icon_bluebox.png">
Students per Teacher: <strong>{{{Students_per_Teacher}}}</strong>
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

Type
----
######updated Sep 23, 2013######
###CSS: Type###
```
#school {  
  marker-file: url(icons/map-marker-6.svg); 
  marker-fill-opacity: 0.8;  
  marker-line-color:black;
  marker-width: 18;
  marker-line-width: 2;
  marker-allow-overlap:true;
  [Type="Lower Secondary"]{marker-fill:#edf8b1}
  [Type="Secondary"]{marker-fill:#7fcdbb}
  [Type="Higher Secondary"]{marker-fill:#2c7fb8}
  [zoom >= 12] {
    marker-width:30;  	  
  }
}
```
###Legend: Type###
```
<div class="legend-title">
School Type
</div>
<div class="items">
    <span class='swatch_1'></span>
    <span class="label">Lower Secondary</span> <br>
    <span class='swatch_2'></span>
    <span class="label">Secondary</span><br>
    <span class='swatch_3'></span>
    <span class="label">Higher Secondary</span><br>
<div class="note"><em>(Mouseover for school name and district.)</em></div>
</div> 

<style type="text/css">
.swatch_1, .swatch_2, .swatch_3 {
    height: 16px;
    margin-right: 5px;
    margin-left: 5px;
    display: table-cell;
    vertical-align:middle;
    text-align: center;
    width: 16px;
    display: inline-block;
}
.swatch_1 {
    background: #edf8b1;
}
.swatch_2 {
    background: #7fcdbb;
}
.swatch_3 {
    background: #2c7fb8;
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
  width: 400px !important;
  font-size: larger;
}
</style>
```
###Teaser: Type###
```
<div class="wrap">
<strong>{{{Name_of_Core_School}}}</strong> in <strong>{{{District}}}</strong> district is <strong>{{{Type}}}</strong>. 
</div>

<style>
.wrap{
    font-size: larger;
}
</style>
```