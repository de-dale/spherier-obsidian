<%* const people = {  
  "Adeline": {  
    "name": "Adeline AVRIL",  
    "acronym": "AA"  
  },  
  "Baptiste": {  
    "name": "Baptiste FOUCHER",  
    "acronym": "BF"  
  },  
  "Maxime": {  
    "name": "Maxime CHANTEAU",  
    "acronym": "MxC"  
  },  
  "Michael": {  
    "name": "Michael SABRI",  
    "acronym": "MS"  
  },  
  "Romain": {  
    "name": "Romain COCHENNEC",  
    "acronym": "RC"  
  }  
}; 
const person = await tp.system.suggester(Object.keys(people), Object.values(people));
const today = tp.date.now("YYYY-MM-DD");
const filename = person.acronym + " - " + today; await tp.file.rename(filename);%>Date : [[<%today%>]]
Personne:  <%* if (person) {%>[[<%person.name%>]]<%* } %>

# Contexte

# Déroulé
