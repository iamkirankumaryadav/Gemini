# Gemini
Google Gemini

### Text Generation
```python
# Import genai library:
import google.generativeai as genai

# Configure the api key:
genai.configure(api_key)

# Set the model:
model = genai.GenerativeModel('gemini-pro')

# Generate the response:
def get_response(prompt):
    response = model.generate_content(prompt)
    return response.text

# Response from the model:
result = get_response(prompt = 'What is the capital of the India?')
print(result)
```

### Message and Chat History
```python
# Import genai library:
import google.generativeai as genai

# Configure the api key:
genai.configure(api_key)

# Set the model:
model = genai.GenerativeModel('gemini-pro')

# Start Chat:
chat = model.start_chat()

# Response from the chat:
response = chat.send_message('Help me plan the roadmap for Data Science and AI')
print(response.text)

# Check history:
chat.history

# Count tokens:
model.count_tokens('Help me plan the roadmap for Data Science and AI')
```
