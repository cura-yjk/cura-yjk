# Hi, I'm Yusuke Kamihanawa (上花輪雄介) 👋

Full-stack developer who just wrapped up an intensive AI Software Development bootcamp at Le Wagon: 9 weeks of Ruby on Rails, JavaScript, SQL, and AI integration, capped off with a team-built, deployed app from scratch.

Currently **job hunting** for **AI Software Developer** or **DevOps** roles. Open to opportunities. Let's connect!

---

### 🛠️ Tech Stack

![Ruby](https://img.shields.io/badge/Ruby-CC342D?style=for-the-badge&logo=ruby&logoColor=white)
![Rails](https://img.shields.io/badge/Rails-CC0000?style=for-the-badge&logo=rubyonrails&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![PostGIS](https://img.shields.io/badge/PostGIS-008000?style=for-the-badge&logo=postgresql&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

---

### 🚀 Featured Projects

#### [Moodwalk](https://github.com/cura-yjk/moodwalk)
A Rails 8 app that generates short walking-loop routes ("journeys") near the user's location. Users start a walk along a suggested route and log their mood and a reflection once it's complete.

**Highlights:**
- **Multi-stage route-generation pipeline**: A five-stage service pipeline (`RouteBuilder → PoiFinder → PoiSelector → RouteDescriber → JourneyGenerator`) that pulls real-world waypoints from Google Places and algorithmically decides loop-vs-one-way routing, scoring candidates on distance fit, compass-bearing spread, and category diversity, then checking angular spread to reject loops that just retrace the same street.
- **Resilient retry logic across two APIs**: Self-correcting retry strategy for Mapbox Directions and Google Places that rescales search radius based on distance-tolerance error, while tracking the best result across attempts so a later retry can't discard an earlier working one.
- **Structured LLM integration with safety-conscious prompts**: Three schema-constrained LLM services (via `ruby_llm-schema`) with system prompts tuned for a mental-health-adjacent context, explicitly avoiding achievement/pressure framing and fabricated details. Used to generate route descriptions, preview highlights, and shareable quotes from walk data.

#### [ペラflash](https://github.com/cura-yjk/pera-flash)
An AI-powered Japanese tutor app. Users submit sentences and an LLM (persona: "Pera") returns structured corrections: original text, corrected version, a vocab breakdown table, and grammar notes — with prompt-injection safeguards built into the system prompt. A separate lightweight LLM call auto-generates a short conversation title from the user's first message.

**Highlights:**
- **Adaptive, language-aware tutoring prompt**: Detects the user's interface language from their message and instructs the LLM to translate its own output structure accordingly (including table headers), while enforcing a consistent, scannable feedback format across every response.
- **Schema-constrained flashcard generation with deduplication**: An AI-to-flashcard pipeline (`ruby_llm-schema`) that flattens a chat transcript, constrains output to a strict JSON schema, and deduplicates against the user's existing flashcards, returning fewer (or zero) cards rather than inventing filler.
- **Rich Markdown + syntax-highlighted response rendering**: Server-side Markdown rendering (GFM, Rouge syntax highlighting) wired into the chat pipeline so tutor feedback renders as fully-formatted HTML rather than raw text.

---

### 📫 Connect with me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/cura-yjk/)
