
# Ailif

A **Rust-based AI agent** leveraging [rig](https://github.com/0xPlaygrounds/rig) for AI functionality to autonomously manage a social media presence on **X (formerly Twitter)**.

**Follow the AI agent here**: [@AilifAgent](https://x.com/AilifAgent)

---

## 📖 Overview

Ailif is an AI-powered autonomous social media agent designed to engage naturally and consistently with users. Built with **Rust** for exceptional performance and reliability, it uses the `rig` framework for advanced AI capabilities.

---

## ✨ Key Features

### 🎭 Character-Based Design
- Structured personality system ensuring consistent behavior and traits  
- Configurable writing styles, topics, and tone preferences  
- Dynamic and context-aware response generation  

### 🤖 Autonomous Interaction
- Generates original, contextually relevant posts  
- Responds intelligently to mentions and interactions  
- Smart engagement filtering for prioritizing meaningful interactions  
- Maintains a natural and fluid conversation flow  

### 🧠 Advanced Memory System
- Persistent storage of interaction history  
- Context-aware memory for generating relevant responses  
- Tracks relationships and recurring interactions with users  

### 📡 Platform Integration
- Integrated with **Twitter API v2** for seamless posting and engagement  
- Built-in rate limiting and scheduling to mimic natural activity  
- Randomized delays for realistic posting patterns  

### 🛠️ Modular and Extensible
- Clear separation of core logic, character traits, and integrations  
- Extensible character system for easy customization  
- Pluggable architecture for future AI or service expansions  
- Optimized memory and performance management  

---

## ⚙️ Prerequisites

To run Ailif, you will need:

- **Rust** (latest stable version)  
- **API Keys**:
  - Anthropic Claude API access  
  - Twitter API v2 credentials (OAuth 1.0a)  

---

## 🛠️ Installation

Follow these steps to set up and run Ailif:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/markspole/Ailif
   cd Ailif
   ```

2. **Create a `.env` file** with your credentials:
   ```env
   ANTHROPIC_API_KEY=your_api_key
   TWITTER_CONSUMER_KEY=your_key
   TWITTER_CONSUMER_SECRET=your_secret
   TWITTER_ACCESS_TOKEN=your_token
   TWITTER_ACCESS_TOKEN_SECRET=your_token_secret
   CHARACTER_NAME=your_character_name
   ```

3. **Configure your character**:
   - Create a new directory: `characters/{CHARACTER_NAME}/`
   - Define your character in `character.json`:

   ```json
   {
     "instructions": {
       "base": "Base character instructions",
       "suffix": "Additional instructions"
     },
     "adjectives": ["trait1", "trait2"],
     "bio": {
       "headline": "Character headline",
       "key_traits": ["trait1", "trait2"]
     },
     "lore": ["background1", "background2"],
     "styles": ["style1", "style2"],
     "topics": ["topic1", "topic2"],
     "post_style_examples": ["example1", "example2"]
   }
   ```

4. **Run the AI agent**:
   ```bash
   cargo run
   ```

---

## 📁 Project Structure

```
Ailif/
├── src/
│   ├── core/            # Core AI agent functionality
│   ├── characteristics/ # Character trait implementations
│   ├── providers/       # External API and service integrations
│   └── memory/          # Persistent memory and history management
├── characters/          # Character JSON definitions
└── tests/               # Test suite
```

---

## 🔗 Dependencies

- [rig](https://github.com/0xPlaygrounds/rig) - AI agent framework  
- `twitter-v2` - Twitter API client  
- `tokio` - Asynchronous runtime  
- `serde` - Serialization/deserialization  
- `anyhow` - Simplified error handling  

---

## 💬 Support

For questions, suggestions, or support, please open an **issue** in the [GitHub repository](https://github.com/markspole/Ailif/issues).  

---

## 🙌 Acknowledgments

Special thanks to:  
- The [rig](https://github.com/0xPlaygrounds/rig) team for their powerful AI agent framework.  
- All contributors and maintainers who help make Ailif better!  
