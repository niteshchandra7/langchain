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

### uv add langchain langchain-openai langchain-tavily python-dotenv isort black
```python
from langchain_core.prompts import PromptTemplate

prompt_template = PromptTemplate.from_template(
    "Tell me a joke about {topic}"
)

# Using the template
prompt_template.invoke({"topic": "cats"})
```

## 🔗 LangChain Chain Workflow  

The step-by-step process of how LangChain handles a query:  

1. **📝 User Query** → Raw question or request from the user  
2. **📌 Prompt Template** → Formats the query into a structured prompt  
3. **🤖 Language Model** → Generates a response  
4. **🧩 Output Parser** → Parses LLM output into structured data  
5. **🌐 External API / Tool Call** → Calls external services if needed  
6. **🔁 Final LLM Call** → Processes API responses  

## 📌 AI Agents - ReAct Architecture

1. ** LangChain ReAct Agent** → ReAct Prompt
2. ** Tool Calling Agent** → Function Calling
3. ** LangGraph ReAct Agent** → Function Calling


