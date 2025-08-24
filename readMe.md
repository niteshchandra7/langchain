# 🚀 Learn LangChain  

## 📌 Prompt Templates  

Prompt templates help translate **user input and parameters** into clear instructions for a language model.  
They **guide the model’s response**, providing structure so the output is relevant and coherent.  

- A **Prompt Template** takes a dictionary as input.  
- Each **key** in the dictionary represents a variable in the template.  
- The template outputs a **PromptValue**, which can be:  
  - Passed to an LLM or ChatModel  
  - Cast into a **string** or a **list of messages**  

👉 The reason `PromptValue` exists is to make switching between **strings** and **messages** easy.  

---

## 📝 String Prompt Templates  

```python
from langchain_core.prompts import PromptTemplate

prompt_template = PromptTemplate.from_template(
    "Tell me a joke about {topic}"
)

# Using the template
prompt_template.invoke({"topic": "cats"})
