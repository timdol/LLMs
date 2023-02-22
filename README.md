# LLMs

### Lots of experiments using OpenAI's APIs for working with GPT3, embeddings, etc.


Use cases:

Search--
Calculate embeddings per section of corpus; calculate enbedding for query; return links to best matches.

Question answering--
As with search, but use best matches as context to answer questions.

Summarization--
Especially summarizing meeting notes.
Pre-process transcript, summarize recursively.
Other supporting stuff-- managing summaries 


Vector database--
Fast similarity search of embeddings.  Used for both seach and Q&A.



Looking at vector databases for fast embeddings similarity search.
These are all pretty expensive.  ToDo: what would a self-hosted equivalent cost?


Pinecone-- 
Hosted-only. 
Free tier allows 1 "pod" which is the unit of procing for cpu, ram, storage.  Capable of ~5M 768-dim vectors at the lowest performance tier, about 20% of that storage at the highest perf.
Costs beyond free tier start at about $70/mo per pod.
Maximum vector dimensions 20K

Milvus--
Hosted or self-host, which very particular hardware & software requirements.
Intro tier provides $400 credit.
Pricing ~$190/hr compute + $0.025/GB storage
Maximum vector dimensionality 32,768

Weviate--
Somewhat different than the others, weviate combines json document with a vector.  The embedding vector can be auto-generated from the json document.  Weviate also includes support for RDF support, and a GraphQL interface.
Hosted or self-hosted
Pricing is built around vector dimensions.  Using their calculator, 1540 dims * 1M objects with 10K queries would cost ~$80/mo https://weaviate.io/pricing
Pricing looks like it scales linearly.
Unknown vector dimensionality limits.





