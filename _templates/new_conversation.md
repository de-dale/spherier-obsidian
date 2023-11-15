---
<%* const people = {  
  "Adeline": {  
    "name": "Adeline AVRIL",  
    "acronym": "AA"  
  },
  "Benoît": {  
    "name": "Benoît GIUSEPPIN",  
    "acronym": "BG"  
  },
  "Franck": {  
    "name": "Franck GUISNE",  
    "acronym": "FG"
  }, 
  "Maxime": {  
    "name": "Maxime CHANTEAU",  
    "acronym": "MxC"  
  },  
  "Michael": {  
    "name": "Michael SABRI",  
    "acronym": "MS"  
  }, 
  "Vartan": {  
    "name": "Vartan KOKOGHLANIAN",  
    "acronym": "VK"  
  }
}; 
const person = await tp.system.suggester(Object.keys(people), Object.values(people));
const today = tp.date.now("YYYY-MM-DD");
const filename = person.acronym + " - " + today; await tp.file.rename(filename);
%>typology: "Conversation"
date : <%today%>
Personne: <%* if (person) {%>"[[<%person.name%>]]"<%* } %>
---
# Contexte

# Déroulé
