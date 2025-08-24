# Learn LangChain

## Prompt Templates

### Prompt templates help to translate user input and parameters into instructions for a language model.
### This can be used to guilde a model's response, helping it understand the context and generate relevant and coherent language-based output.

### Prompt Template takes dictionary as a input, where each key represents a variable in the prompt template to fill in.

### Prompt Template outputs a PromptValue. This PromptValue can be passed to an LLM or a chatModel, and can also be cast to a string or a list of messages.

### The reason this PromptValue exists to make it easy to switch between strings and messages

## String Prompt Templates
`
    from langchain_coreprompts import PromptTemplate
    prompt_template = PromptTemplate.from_template("Tell me a joke about {topic}")
    prompt_template.invoke({"topic":"cats"})
`

## LangChain Chain Workflow

### UserQuery                     
### Prompt Template               -> Format query into structured prompt
### Language Model                -> Generate
### Output Parser                 -> Parse LLM output into structred data
### External API Tool Call        -> Call external service
### Final LLM Call                -> Process API response
### Final Output