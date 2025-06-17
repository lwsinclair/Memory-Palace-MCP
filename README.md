[![MseeP.ai Security Assessment Badge](https://mseep.net/pr/zeyynepkaraduman-memory-palace-mcp-badge.png)](https://mseep.ai/app/zeyynepkaraduman-memory-palace-mcp)

# Memory Palace MCP 🏰

A Model Context Protocol (MCP) server that implements the ancient "Method of Loci" (Memory Palace) technique for enhanced learning and memory retention. This MCP helps users create virtual memory palaces, organize information spatially, and build memory journeys for effective recall.

## Features ✨

- **🏰 Create Memory Palaces**: Build themed virtual spaces (ancient, modern, nature, space, underwater, library)
- **🏠 Room Management**: Create and organize rooms within palaces with 3D positioning
- **📝 Memory Items**: Store information with visual cues (images, icons, colors, shapes)
- **🗺️ Memory Journeys**: Create guided paths through your palace for structured review
- **🔍 Smart Search**: Find memory items by content, title, or tags
- **📊 Analytics**: Track review counts and get statistics about your memory palaces

## Installation

### From Smithery

```bash
npx @smithery/cli install memory-palace-mcp
```

### Manual Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd memory-palace-mcp
```

2. Install dependencies:
```bash
npm install
```

3. Build the project:
```bash
npm run build
```

4. Start the server:
```bash
npm start
```

## Configuration

Add to your MCP client configuration:

```json
{
  "mcpServers": {
    "memory-palace": {
      "command": "npx",
      "args": ["memory-palace-mcp"]
    }
  }
}
```

For Claude Desktop, add to `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "memory-palace": {
      "command": "node",
      "args": ["/path/to/memory-palace-mcp/dist/index.js"]
    }
  }
}
```

## Usage Guide 📚

### 1. Create Your First Memory Palace

```
Use the create_palace tool:
- name: "Ancient Library"
- description: "A grand library with marble columns"
- theme: "ancient"
```

### 2. Add Rooms to Your Palace

```
Use the create_room tool:
- name: "Main Hall"
- palaceId: [your-palace-id]
- position: { x: 0, y: 0, z: 0 }
- size: "large"
- color: "#FFD700"
```

### 3. Place Memory Items

```
Use the add_memory_item tool:
- title: "Python Syntax"
- content: "for item in list: print(item)"
- roomId: [your-room-id]
- position: { x: 1, y: 1, z: 0 }
- visualCue: { 
    type: "icon", 
    value: "🐍", 
    description: "Snake for Python" 
  }
- tags: ["programming", "python"]
- importance: "high"
```

### 4. Create Memory Journeys

```
Use the create_journey tool:
- name: "Python Basics Tour"
- palaceId: [your-palace-id]
- roomIds: [array-of-room-ids]
- difficulty: "beginner"
```

### 5. Take Your Journey

```
Use the take_journey tool:
- journeyId: [your-journey-id]
```

## Available Tools 🛠️

| Tool | Description |
|------|-------------|
| `create_palace` | Create a new memory palace with themes |
| `list_palaces` | List all your memory palaces |
| `create_room` | Add rooms to your palaces |
| `add_memory_item` | Store information with visual cues |
| `create_journey` | Plan memory tours through rooms |
| `take_journey` | Review memories in sequence |
| `search_memories` | Find items by content or tags |
| `get_palace_layout` | View detailed palace structure |
| `get_statistics` | Get usage analytics |

## Memory Palace Themes 🎨

- **🏛️ Ancient**: Classical Greek/Roman architecture
- **🏢 Modern**: Contemporary office/home spaces
- **🌳 Nature**: Forests, gardens, natural landscapes
- **🚀 Space**: Spaceships, space stations, alien worlds
- **🌊 Underwater**: Ocean depths, coral reefs, submarines
- **📚 Library**: Grand libraries, study halls, archives

## Visual Cue Types 👁️

- **🖼️ Image**: URLs to pictures or illustrations
- **🎯 Icon**: Emoji or icon names (🐍, 📊, 💡)
- **🎨 Color**: Hex color codes (#FF0000, #00FF00)
- **🔺 Shape**: Geometric shapes (circle, square, triangle)

## Example Use Cases 💡

### Learning a Programming Language
- Palace: "Code Academy"
- Rooms: "Syntax Hall", "Function Library", "Debug Dungeon"
- Items: Code snippets with visual metaphors

### Medical Studies
- Palace: "Human Body Hospital"
- Rooms: "Heart Chamber", "Brain Center", "Bone Gallery"
- Items: Anatomical facts with visual diagrams

### Language Learning
- Palace: "French Château"
- Rooms: "Vocabulary Vault", "Grammar Garden", "Phrase Parlor"
- Items: Words and phrases with visual associations

### Historical Events
- Palace: "Timeline Tower"
- Rooms: Floors for different time periods
- Items: Events with memorable visual cues

## Advanced Features 🔬

### Spaced Repetition
The system tracks review counts and last review dates, helping you identify items that need more attention.

### Spatial Intelligence
3D positioning helps leverage spatial memory for better recall. Items placed in memorable locations are easier to remember.

### Multi-sensory Encoding
Visual cues engage multiple memory pathways, making information more memorable and easier to retrieve.

## Development 👩‍💻

### Project Structure
```
src/
├── index.ts        # Main MCP server
├── types.ts        # Type definitions and schemas
└── storage.ts      # In-memory data storage
```

### Building
```bash
npm run build    # Compile TypeScript
npm run dev      # Development with auto-rebuild
npm test         # Run tests
```

### Contributing
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## Memory Science 🧠

This MCP is based on the **Method of Loci**, a mnemonic technique dating back to ancient Greece. Research shows that spatial memory is one of our strongest memory systems, making this technique highly effective for:

- **Enhanced Recall**: Spatial context improves memory retrieval
- **Long-term Retention**: Visual-spatial encoding creates lasting memories
- **Complex Information**: Breaking down information into manageable, memorable chunks
- **Active Learning**: Creating palaces engages multiple cognitive processes

## License

MIT License - see LICENSE file for details.

## Support

- 📧 Issues: [GitHub Issues](link-to-issues)
- 💬 Discussions: [GitHub Discussions](link-to-discussions)
- 📖 Documentation: [Wiki](link-to-wiki)

---

*"The art of memory is the art of attention."* - Ancient proverb

Made with ❤️ for better learning and memory retention. 