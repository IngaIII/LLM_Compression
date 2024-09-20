# LLMCompression

LLMCompression is a Python module that combines OpenAI's language models with LZMA compression to provide innovative text compression techniques meant for Latex documents.

## Features

- Letter compression: Removes the last letter of every word (with exceptions)
- Space compression: Removes spaces between words
- SL (Space-Letter) compression: Combines both letter and space compression
- Decompression: Restores compressed text to its original form
- Uses OpenAI's GPT models for intelligent text manipulation
- LZMA compression for additional data reduction

## Installation

To install LLMCompression, you'll need Python 3.6 or later. Use pip to install the required dependencies:

```
pip install pylzma openai
```

## Usage

First, import the `LLMCompression` class and initialize it with your OpenAI API key:

```python
from llm_compression import LLMCompression

compressor = LLMCompression(api_key="your-openai-api-key")
```

You can also set your API key as an environment variable named `OPENAI_API_KEY`.

### Letter Compression

```python
text = "Hello, this is a sample text for compression."
compressed = compressor.letter_compression(text)
decompressed = compressor.letter_decompression(compressed)
print(decompressed)  # Should match the original text
```

### Space Compression

```python
compressed = compressor.space_compression(text)
decompressed = compressor.space_decompression(compressed)
print(decompressed)  # Should match the original text
```

### SL Compression

```python
compressed = compressor.sl_compression(text)
decompressed = compressor.sl_decompression(compressed)
print(decompressed)  # Should match the original text
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

