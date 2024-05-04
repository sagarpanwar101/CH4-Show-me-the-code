Recap of chapter3 
creating food ordering app 
UI/UX planning -- roughly design the layout and make components
header > body > search >scrollbar > footer  

Will divide the components but they are in same page. First will be header component 
HeaderComponnent -> Logo > title > Navitems etc
Body-> body parts like cards,caraousel,search bar etc
footer-> footer cols logo descp etc

but if you want to give attributes style we can use 
style={color:red};

Props is like argument to func and attributes to html

Config Driven UI - basically means to design the layout of in which data comes according
to the area,city or country. 

api = https://www.swiggy.com/dapi/restaurants/list/v5?lat=12.9351929&lng=77.624480699999&page_type=DESKTOP_WEB_LISTING

New api =https://www.swiggy.com/dapi/menu/pl?page-type=REGULAR_MENU&complete-menu=true&lat=28.6738274&lng=77.1642584&restaurantId=57484

optional chaining 
map filter  reduce imp

Virtual DOM -> copy of DOM is used for React reconcilation - react use diff algorithm to diff tree
another for which needs to determines what need to be updated 

re-render everytime if key is not mention

react fiber?

construct deconstruct rest operator 