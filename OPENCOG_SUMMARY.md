# OpenCog Implementation Summary

## Overview
This repository now contains OpenCog implementations of open-weight language models by OpenAI. The models `cog-gpt-oss-120b` and `cog-gpt-oss-20b` are OpenCog adaptations that maintain full compatibility with the original `gpt-oss-120b` and `gpt-oss-20b` models.

## What is OpenCog?
OpenCog is a framework for creating adaptations of open-weight language models. The cog-gpt-oss implementations maintain compatibility with the original gpt-oss models while providing an OpenCog-branded interface and tooling ecosystem.

## Changes Made

### Documentation Updates
1. **README.md**
   - Updated header to reference `cog-gpt-oss` instead of `gpt-oss`
   - Added "What is OpenCog?" section explaining the framework
   - Updated all model references from `gpt-oss-120b/20b` to `cog-gpt-oss-120b/20b`
   - Updated repository clone URL to `github.com/cogpy/cog-gpt-oss`
   - Clarified that cog-gpt-oss models are compatible with original gpt-oss weights

2. **pyproject.toml**
   - Updated package description to: "OpenCog implementations (cog-gpt-oss-120b and cog-gpt-oss-20b) - adaptations of open-weight language models by OpenAI"

3. **awesome-gpt-oss.md**
   - Updated title to "Awesome cog-gpt-oss (OpenCog)"
   - Added clarification that this is for OpenCog implementations

4. **gpt-oss-mcp-server/README.md**
   - Updated to reference cog-gpt-oss repository and OpenCog implementations

5. **gpt_oss/evals/README.md**
   - Updated to reference cog-gpt-oss (OpenCog implementations)

## Compatibility
All code remains fully compatible with the original implementation:
- The package name remains `gpt-oss` for backward compatibility
- All Python modules and imports remain unchanged
- Model weights are still downloaded from the original HuggingFace locations
- All tools, APIs, and functionality remain identical

## Model Naming Convention
- **cog-gpt-oss-120b**: OpenCog implementation for production use (117B parameters, 5.1B active)
- **cog-gpt-oss-20b**: OpenCog implementation for local/specialized use (21B parameters, 3.6B active)

Both models use the original `gpt-oss-120b` and `gpt-oss-20b` weights from HuggingFace.

## Key Features Retained
- Permissive Apache 2.0 license
- Configurable reasoning effort
- Full chain-of-thought access
- Fine-tunable models
- Agentic capabilities (function calling, web browsing, Python execution)
- MXFP4 quantization for efficient GPU usage
- Harmony response format support

## Usage
The models can be used exactly as before, but with the new naming:

```bash
# Download weights
hf download openai/gpt-oss-120b --include "original/*" --local-dir cog-gpt-oss-120b/

# Run inference
python -m gpt_oss.generate --backend triton cog-gpt-oss-120b/original/
```

## Security
No security vulnerabilities were introduced by these changes. All modifications were documentation-only and did not alter any functional code.
