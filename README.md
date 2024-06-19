# Context caching 


In a typical AI workflow, you might pass the same input tokens over and over to a model. Using the Gemini API context caching feature, you can pass some content to the model once, cache the input tokens, and then refer to the cached tokens for subsequent requests. At certain volumes, using cached tokens is lower cost (and can be lower latency) than passing in the same corpus of tokens repeatedly.

When you cache a set of tokens, you can choose how long you want the cache to exist before the tokens are automatically deleted. This caching duration is called the time to live (TTL). The cost for caching depends on the input token size and how long you want the tokens to persist.

Context caching supports both Gemini 1.5 Pro and Gemini 1.5 Flash. Context caching is particularly well suited to scenarios where a substantial initial context is referenced repeatedly by shorter requests
