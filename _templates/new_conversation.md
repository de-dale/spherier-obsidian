---
<%* const people = {
  "Christelle": {  
    "name": "Christelle BARADÉ",  
    "acronym": "CB"  
  },
  "Benoît": {  
    "name": "Benoît GIUSEPPIN",  
    "acronym": "BG"  
  },
  "Florian": {  
    "name": "Florian LEFEUVRE",  
    "acronym": "FL"  
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
