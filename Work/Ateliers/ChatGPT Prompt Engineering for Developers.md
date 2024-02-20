---
ressource:
  - 🎓 Formation
trello: https://trello.com/c/b3c3Ny8a/1808-chatgpt-prompt-engineering-for-developers-deeplearningai
link:
  - https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/
tags:
  - IA
---
Formation gratuite

# Notes

LLM : Large Language Model
possibiltes what we can do
ho to do

LLM
- Base LLM
- Intruction Turned LLM / Fine tuned

## Guidelines for prompting

### Prompting Principles

- **Principle 1: Write clear and specific instructions**
- **Principle 2: Give the model time to “think”**
### Principle 1: Write clear and specific instructions
=> clear != short
#### Tactic 1: Use delimiters to clearly indicate distinct parts of the input
Exemple : 
> prompt = f"""
> Summarize the text delimited by triple backticks \ 
> into a single sentence.
> ```{text}```
> """

#### Tactic 2: Ask for a structured output

- JSON, HTML

**Exemple :** 
  > prompt = f"""
  > Generate a list of three made-up book titles along \ 
  > with their authors and genres. 
  > Provide them in JSON format with the following keys: 
  > book_id, title, author, genre.
  > """
#### Tactic 3: Ask the model to check whether conditions are satisfied
Faire des hypothèses sur ce que peut faire le modèle avec les instruction qu'on lui donne, et lui demander de vérifier ces hypothèses et de l'indiquer si les conditions ne sont pas vérifiées.

**Exemple :** 
> prompt = f"""
> You will be provided with text delimited by triple quotes. 
> If it contains a sequence of instructions, \ 
> re-write those instructions in the following format:
> 
> Step 1 - ...
> Step 2 - …
> …
> Step N - …
> 
> If the text does not contain a sequence of instructions, \ 
> then simply write \"No steps provided.\"
> 
> \"\"\"{text_2}\"\"\"
> """

#### Tactic 4: "Few-shot" prompting
> Give successful examples of completing tasks then ask model to perfrom the task

Donner au modèles des exemples de résolution de la tache, conformes à l'atendu, puis lui demander d'exécuter la tâche

Exemple :
> prompt = f"""
> Your task is to answer in a consistent style.
> 
> \<child>: Teach me about patience.
> 
> \<grandparent>: The river that carves the deepest \ 
> valley flows from a modest spring; the \ 
> grandest symphony originates from a single note; \ 
> the most intricate tapestry begins with a solitary thread.
> 
> \<child>: Teach me about resilience.
> """

### Principle 2: Give the model time to "think"

##### Tactic 1: Specify the steps required to complete a task

Exemple : 
> prompt_1 = f"""
> Perform the following actions: 
> 1 - Summarize the following text delimited by triple backticks with 1 sentence.
> 2 - Translate the summary into French.
> 3 - List each name in the French summary.
> 4 - Output a json object that contains the following keys: french_summary, num_names.
> 
> Separate your answers with line breaks.
> 
> Text:
> ```{text}```
> """

###### Ask for output in a specified format

> prompt_2 = f"""
> Your task is to perform the following actions: 
> 1 - Summarize the following text delimited by 
>   <> with 1 sentence.
> 2 - Translate the summary into French.
> 3 - List each name in the French summary.
> 4 - Output a json object that contains the 
  > following keys: french_summary, num_names.
> 
> Use the following format:
> Text: \<text to summarize>
> Summary: \<summary>
> Translation: \<summary translation>
> Names: \<list of names in Italian summary>
> Output JSON: \<json with summary and num_names>
> 
> Text: \<{text}>
> """

##### Tactic 2: Instruct the model to work out its own solution before rushing to a conclusion

Exemple d'une tâche proposée "La solution est-elle correcte ?"
=> Le modèle peut se tromper et considérer que oui, alors que non.

Solution: demenader au modèle de cosntuire sa solution et de la comparer 

Exemple : 
> prompt = f"""  
> Your task is to determine if the student's solution \  
> is correct or not.  
> To solve the problem do the following:  
> - First, work out your own solution to the problem.   
> - Then compare your solution to the student's solution \   
> and evaluate if the student's solution is correct or not.   
> Don't decide if the student's solution is correct until   
> you have done the problem yourself.  
>   
> Use the following format:  
> Question:  
> ```  
> question here  
> ```  
> Student's solution:  
> ```  
> student's solution here  
> ```  
> Actual solution:  
> ```  
> steps to work out the solution and your solution here  
> ```  
> Is the student's solution the same as actual solution \  
> just calculated:  
> ```  
> yes or no  
> ```  
> Student grade:  
> ```  
> correct or incorrect  
> ```  
>   
> Question:  
> ```  
> I'm building a solar power installation and I need help \  
> working out the financials.   
> - Land costs $100 / square foot  
> - I can buy solar panels for $250 / square foot  
> - I negotiated a contract for maintenance that will cost \  
> me a flat $100k per year, and an additional $10 / square \  
> foot  
> What is the total cost for the first year of operations \  
> as a function of the number of square feet.  
> ```   
> Student's solution:  
> ```  
> Let x be the size of the installation in square feet.  
> Costs:  
> 1. Land cost: 100x  
> 2. Solar panel cost: 250x  
> 3. Maintenance cost: 100,000 + 100x  
> Total cost: 100x + 250x + 100,000 + 100x = 450x + 100,000  
> ```  
> Actual solution:  
> """



## Iterative Prompt Develelopment

Bien penser que, entraîner un modèle, ne fonctionne presque jamais du premier coup !
Ce qui est important, c'est d'avoir en tête le process permettant de faire fonctionner les prompts qui fonctionnent pour notre cas, plutôt que d'avoir un prompt qui fonctionne du premier coup.

**Prompt guidelines**
- Be clear and specific
- Analyze why result does not give desired output
- Refine the idea and the prompt
- Repeat

**Iterative prompt**
- try something
- Analyse where the result case does not give what you want
- Clarify instructions, give more time to think
- Refine prompts with patch of examples

> good prompt **<** have a process for developping a good prompt

**Quand le prompt ne convient pas : il faut clarifier ce qu'on attend !**

Exemple du prompt qui ne convient pas :
> prompt = f"""  
> Your task is to help a marketing team create a   
> description for a retail website of a product based   
> on a technical fact sheet.  
>   
> Write a product description based on the information   
> provided in the technical specifications delimited by   
> triple backticks.  
>   
> Technical specifications: ```{fact_sheet_chair}```  
> """
#### Issue 1: The text is too long
- Limit the number of words/sentences/characters.

Exemple : 
> prompt = f"""  
> Your task is to help a marketing team create a   
> description for a retail website of a product based   
> on a technical fact sheet.  
>   
> Write a product description based on the information   
> provided in the technical specifications delimited by   
> triple backticks.  
> 
> **Use at most 50 words.** (ou : "*Use 2 sentences*", ou "*Use at most 280 characters*")
>   
> Technical specifications: ```{fact_sheet_chair}```  
> """

#### Issue 2. Text focuses on the wrong details
- Ask it to focus on the aspects that are relevant to the intended audience.

Exemple : 
> prompt = f"""  
> Your task is to help a marketing team create a   
> description for a retail website of a product based   
> on a technical fact sheet.  
>   
> Write a product description based on the information   
> provided in the technical specifications delimited by   
> triple backticks.  
>   
> **The description is intended for furniture retailers,   
> so should be technical in nature and focus on the   
> materials the product is constructed from.  
>**   
> Use at most 50 words.  
>   
> Technical specifications: ```{fact_sheet_chair}```  
> """

#### Issue 3. Description needs a table of dimensions
- Ask it to extract information and organize it in a table.

> prompt = f"""  
> Your task is to help a marketing team create a   
> description for a retail website of a product based   
> on a technical fact sheet.  
>   
> Write a product description based on the information   
> provided in the technical specifications delimited by   
> triple backticks.  
>   
> The description is intended for furniture retailers,   
> so should be technical in nature and focus on the   
> materials the product is constructed from.  
>   
> At the end of the description, include every 7-character   
> Product ID in the technical specification.  
>   
> After the description, include a table that gives the   
> product's dimensions. The table should have two columns.  
> In the first column include the name of the dimension.   
> In the second column include the measurements in inches only.  
>   
> Give the table the title 'Product Dimensions'.  
>   
> Format everything as HTML that can be used in a website.   
> Place the description in a \<div> element.  
>   
> Technical specifications: ```{fact_sheet_chair}```  
> """


## Use Cases

### Summarizing

Résumer

- avec une taille de tecte prédéfinie.

### Inferring

Déduire
### Transforming

Transformer

### Expanding

