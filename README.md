# My TS API Learning Repo
from openai import OpenAI
client = OpenAI()

response = client.chat.completions.create(
    model="gpt-4o-mini",
    messages=[
        {"role": "system", "content": "あなたは優秀な業務アシスタントです。"},
        {"role": "user", "content": "RAGとは何ですか？"}
    ]
)

print(response.choices[0].message.content)
