## Scope

Service should support redirects to a given URL with given text expanded (to Claude/ChatGPT, for example, think about other useful scenarios).

- Another `?redirect` parameter for the URL
- Parameter supports expansion of `{text}`
- Service loads, decompresses the text, if redirect is present - sends there with expanded URL

## Claude AI

Claude supports the `?q=` URL parameter to pre-fill the prompt field[^1]. The format is:

```
https://claude.ai/new?q=your_prompt_here
```

**Example:**
```
https://claude.ai/new?q=Write%20a%20summary%20of%20machine%20learning
```

This feature was recently added and can be discovered through trial and error[^4]. It's particularly useful for automation tools like Keyboard Maestro or Alfred on Mac, allowing you to quickly send queries without the delay of manually opening Claude and typing[^2].

## ChatGPT

ChatGPT offers more extensive URL parameter support[^1][^3]:

| Parameter | Purpose | Example |
|-----------|---------|---------|
| `?q=` | Pre-fills the prompt field | `https://chatgpt.com/?q=explain%20quantum%20computing` |
| `&hints=search` | Opens with SearchGPT mode (Plus users) | `https://chatgpt.com/?q=latest%20AI%20news&hints=search` |
| `&hints=canvas` | Opens with Canvas mode enabled | `https://chatgpt.com/?q=write%20a%20blog%20post&hints=canvas` |
| `&temporary-chat=true` | Creates temporary chat (doesn't save to history) | `https://chatgpt.com/?q=test%20query&temporary-chat=true` |

**Basic format:**
```
https://chatgpt.com/?q={your_query_here}
```

**With SearchGPT (for Plus users):**
```
https://chatgpt.com/?q={your_query_here}&hints=search
```
