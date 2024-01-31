import os
import openai

# Set your OpenAI API key as an environment variable
os.environ["OPENAI_API_KEY"] = "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"

def generate_text(prompt):
    # Create an OpenAI client using your API key
    openai.api_key = os.environ['OPENAI_API_KEY']

    # Generate text using the GPT-3 model
    response = openai.Completion.create(
        engine="text-davinci-002",  # Choose the appropriate engine
        prompt=prompt,
        max_tokens=1000,
        temperature=0.7,
    )

    # Extract the generated text from the response
    generated_text = response["choices"][0]["text"]

    return generated_text

prompt = "Write a haiku about a sunset."
generated_text = generate_text(prompt)
print(generated_text)
