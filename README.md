# nanobanana-mcp

Gemini-powered image generation MCP server for Claude Code. Generate and edit images using Google's Gemini models directly from your AI coding workflow.

## Features

- **Multi-Model Support** --- Gemini 3.1 Flash Image (default), Gemini 3 Pro Image, and Gemini 2.5 Flash Image
- **Image Generation** --- Text-to-image with intelligent model selection and 4K output
- **Image Editing** --- Modify existing images with natural language instructions
- **Aspect Ratio Control** --- 1:1, 16:9, 9:16, 21:9, and more formats
- **Conversation Context** --- Multi-turn chat with Gemini for iterative refinement
- **Session Management** --- Track image history and manage generation sessions

## Installation

```bash
claude mcp add -s user nanobanana-mcp -- npx -y @ycse/nanobanana-mcp
```

### API Key Setup

You need a Google AI API key. Get one free at [https://aistudio.google.com/apikey](https://aistudio.google.com/apikey).

Set the environment variable:

```bash
export GOOGLE_AI_API_KEY="your-api-key-here"
```

Or configure it in your MCP server settings:

```json
{
  "env": {
    "GEMINI_API_KEY": "your-api-key-here"
  }
}
```

## Available MCP Tools

| Tool | Description |
|------|-------------|
| `set_model` | Switch between Flash, Pro, and NB2 model tiers |
| `gemini_generate_image` | Generate images from text prompts with model selection |
| `gemini_edit_image` | Edit existing images with natural language instructions |
| `gemini_chat` | Multi-turn conversation with Gemini for iterative work |
| `set_aspect_ratio` | Set output aspect ratio (1:1, 16:9, 9:16, 21:9, etc.) |
| `get_image_history` | Retrieve history of generated images in the session |
| `clear_conversation` | Reset conversation context for a fresh session |

## Usage Examples

Generate an image:

```
Generate a product photo of a coffee mug on a wooden table, morning light
```

Edit an existing image:

```
Edit this image: make the background a sunset beach scene
```

Control the model and aspect ratio:

```
Switch to Pro model, set aspect ratio to 16:9, then generate a cinematic landscape at golden hour
```

Iterative refinement with conversation context:

```
Generate a logo for a tech startup called "Nexus"
Now make the colors more vibrant and add a subtle gradient
```

## stitchkit Integration

Part of the [stitchkit](https://github.com/tygwan/stitchkit) ecosystem --- a Claude Code plugin that combines Google Stitch UI design generation with Gemini image generation via nanobanana.

## Acknowledgments

Inspired by the original [nanobanana-mcp-server](https://github.com/zhongweili/nanobanana-mcp-server) by zhongweili.

## Author

[tygwan](https://github.com/tygwan)

## License

[MIT](LICENSE)
