# DeepSeek Opens Full App Feature Suite Through Its API, Including Search, File Reading, and Voice

![AI circuit brain illustration](https://cdn.pixabay.com/photo/2018/05/08/08/44/artificial-intelligence-3382507_1280.jpg)
*Image from Pixabay under free Content License. Source: [Pixabay](https://pixabay.com/illustrations/artificial-intelligence-brain-think-3382507/)*

On November 13, 2026, DeepSeek made the core capabilities of its consumer application available through its public API. Developers can now enable web search with citations, file and link reading, content safety checks, and voice interaction (ASR and TTS) directly inside conversations powered by the deepseek-flash model, or call the underlying tools as standalone endpoints.

Previously, building a ChatGPT-style assistant that could search the web, parse documents, and speak required stitching together multiple third-party services. DeepSeek’s update consolidates these functions under a single API key, with the service handling tool calling and context assembly.

## Available Capabilities

In the Messages, Responses, and Chat Completions APIs, developers can activate:

- **Web search**: The model performs text or image searches and returns answers with citations. When thinking mode is enabled, it can interleave search and page reading across multiple reasoning steps.
- **URL reading**: Links in user messages are automatically fetched and incorporated into context.
- **File input**: PDFs, Word documents, PowerPoint files, and images are parsed (plain text or rich layout) and added to the conversation.
- **Safety checks**: Inputs and outputs are reviewed for risk, with refusals when necessary.
- **Automatic titles and user context**: Conversation titles are generated; date, location, and language can be passed to the model.

Standalone endpoints are also available for Search/Fetch, OCR, ASR, and TTS. OCR, ASR, and TTS can be called independently when only one capability is required.

## Pricing (as of November 14, 2026)

| Tool | Unit | Price |
|------|------|-------|
| Search (text/image) | 1,000 successful requests | $0.75 |
| Web fetch | 1,000 successful requests | $0.75 |
| File parsing / OCR | 1,000 pages (successful) | $0.225 |
| TTS | 10,000 billing characters | $0.45 (half-price limited-time $0.225) |
| ASR | 1 hour of audio | $0.116 (half-price limited-time $0.058) |

Token pricing for deepseek-flash itself starts from $0.15 per million input tokens (cache miss, off-peak) and $0.60 per million output tokens. Tool fees are charged in addition to token usage.

## Technical Notes and Limitations

ASR accepts complete audio files (16-bit PCM WAV or Ogg Opus, max 120 seconds / 8 MiB) and returns full transcripts; streaming is not supported. TTS supports voices “stella” (female, default) and “tide” (male), with a maximum of roughly 10,000 billing characters per request. Failed or timed-out OCR pages are not charged.

## Developer Impact

The release lowers the barrier to creating capable agents. Startups and enterprises can now add grounded search, document understanding, and voice interfaces without managing separate vendor relationships or building custom orchestration. Combined with competitive token pricing, it strengthens DeepSeek’s position among developers seeking high-capability, cost-effective alternatives to Western frontier APIs.

## Outlook

By productizing the same tool stack used in its consumer app, DeepSeek is converting application features into developer infrastructure. Early adoption will depend on reliability of the search and parsing pipelines, citation quality, and how the safety layer interacts with agentic workflows. The move continues the trend of frontier-adjacent labs exposing more of their internal agent capabilities through APIs.

## Sources and References

1. DeepSeek API documentation and changelog: Releasing the full suite of application APIs (November 13, 2026). https://api-docs.deepseek.com/updates.md
2. Coverage of pricing and feature set (November 14, 2026). https://intheworldofai.com/p/deepseek-app-api
3. Chinese-language developer guides detailing endpoints and billing (November 2026).
4. Contemporary reporting on DeepSeek App feature availability through the API.

*Article compiled from official documentation and contemporaneous reporting. Images sourced from Pixabay under free license.*