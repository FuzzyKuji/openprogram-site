<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/models/providers/adapters/*/provider.json. -->


# Provider registry

Wire-level facts for every built-in provider, straight from its `provider.json`. For how to sign in and use each one, see [Providers](../models/providers.md).

## alibaba-token-plan-cn

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/alibaba_token_plan_cn/` |
| **Protocol** | `openai-completions` |
| **Base URL** | `https://token-plan.cn-beijing.maas.aliyuncs.com/compatible-mode/v1` |

## amazon-bedrock

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/amazon_bedrock/` |
| **Protocol** | `bedrock-converse-stream` |
| **Base URL** | `https://bedrock-runtime.us-east-1.amazonaws.com` |
| **Default effort** | `high` |
| **Effort levels** | `minimal`, `low`, `medium`, `high`, `xhigh`, `max` |
| **Cache policy keys** | `breakpoint_format`, `max_breakpoints`, `mode`, `retention_ttl_map` |

## anthropic

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/anthropic/` |
| **Protocol** | `anthropic-messages` |
| **Base URL** | `https://api.anthropic.com` |
| **API-key env** | `ANTHROPIC_OAUTH_TOKEN`, `ANTHROPIC_API_KEY` |
| **Default effort** | `high` |
| **Effort levels** | `minimal`, `low`, `medium`, `high`, `xhigh`, `max` |
| **Cache policy keys** | `breakpoint_format`, `long_ttl_endpoints`, `max_breakpoints`, `mode`, `retention_ttl_map` |

## atlascloud

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/atlascloud/` |
| **Protocol** | `openai-completions` |
| **Base URL** | `https://api.atlascloud.ai/v1` |
| **API-key env** | `ATLASCLOUD_API_KEY` |

## azure-openai-responses

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/azure_openai_responses/` |
| **Protocol** | `azure-openai-responses` |
| **API-key env** | `AZURE_OPENAI_API_KEY` |
| **Default effort** | `xhigh` |
| **Effort levels** | `minimal`, `low`, `medium`, `high`, `xhigh`, `max` |

## cerebras

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/cerebras/` |
| **Protocol** | `openai-completions` |
| **Base URL** | `https://api.cerebras.ai/v1` |
| **API-key env** | `CEREBRAS_API_KEY` |

## deepseek

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/deepseek/` |
| **Protocol** | `openai-completions` |
| **Base URL** | `https://api.deepseek.com/v1` |
| **API-key env** | `DEEPSEEK_API_KEY` |
| **Default effort** | `medium` |
| **Effort levels** | `minimal`, `low`, `medium`, `high`, `max` |

## gemini-subscription

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/gemini_subscription/` |
| **Protocol** | `gemini-subscription` |
| **Base URL** | `https://cloudcode-pa.googleapis.com` |
| **API-key env** | `GEMINI_API_KEY` |

## github-copilot

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/github_copilot/` |
| **Protocol** | `openai-responses` |
| **Base URL** | `https://api.individual.githubcopilot.com` |
| **Protocol (openai-completions)** | `openai-completions` |
| **Base URL (openai-completions)** | `https://api.individual.githubcopilot.com` |
| **Protocol (anthropic-messages)** | `anthropic-messages` |
| **Base URL (anthropic-messages)** | `https://api.individual.githubcopilot.com` |
| **API-key env** | `COPILOT_GITHUB_TOKEN`, `GH_TOKEN`, `GITHUB_TOKEN` |

## google

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/google/` |
| **Protocol** | `google-generative-ai` |
| **Base URL** | `https://generativelanguage.googleapis.com/v1beta` |
| **API-key env** | `GEMINI_API_KEY`, `GOOGLE_API_KEY`, `GOOGLE_GENERATIVE_AI_API_KEY` |
| **Default effort** | `medium` |

## google-gemini-cli

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/google_gemini_cli/` |
| **Default effort** | `medium` |

## groq

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/groq/` |
| **Protocol** | `openai-completions` |
| **Base URL** | `https://api.groq.com/openai/v1` |
| **API-key env** | `GROQ_API_KEY` |

## huggingface

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/huggingface/` |
| **Protocol** | `openai-completions` |
| **Base URL** | `https://router.huggingface.co/v1` |
| **API-key env** | `HF_TOKEN` |

## kimi-coding

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/kimi_coding/` |
| **Protocol** | `anthropic-messages` |
| **Base URL** | `https://api.kimi.com/coding` |
| **API-key env** | `KIMI_API_KEY`, `MOONSHOT_API_KEY` |

## llamacpp

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/llamacpp/` |
| **Protocol** | `openai-completions` |
| **Base URL** | `http://localhost:8080/v1` |

## lmstudio

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/lmstudio/` |
| **Protocol** | `openai-completions` |
| **Base URL** | `http://localhost:1234/v1` |

## local

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/local/` |
| **Protocol** | `openai-completions` |
| **Base URL** | `http://localhost:8000/v1` |

## minimax

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/minimax/` |
| **Protocol** | `anthropic-messages` |
| **Base URL** | `https://api.minimax.io/anthropic` |
| **API-key env** | `MINIMAX_API_KEY` |

## minimax-cn

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/minimax_cn/` |
| **Protocol** | `anthropic-messages` |
| **Base URL** | `https://api.minimaxi.com/anthropic` |
| **API-key env** | `MINIMAX_CN_API_KEY`, `MINIMAX_API_KEY` |

## mistral

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/mistral/` |
| **Protocol** | `openai-completions` |
| **Base URL** | `https://api.mistral.ai/v1` |
| **API-key env** | `MISTRAL_API_KEY` |

## ollama

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/ollama/` |
| **Protocol** | `openai-completions` |
| **Base URL** | `http://localhost:11434/v1` |

## openai

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/openai/` |
| **Protocol** | `openai-responses` |
| **Base URL** | `https://api.openai.com/v1` |
| **API-key env** | `OPENAI_API_KEY` |

## openai-codex

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/openai_codex/` |
| **Protocol** | `openai-codex` |
| **Base URL** | `https://chatgpt.com/backend-api` |
| **Default effort** | `xhigh` |
| **Effort levels** | `low`, `medium`, `high`, `xhigh`, `max` |

## openai-completions

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/openai_completions/` |
| **Default effort** | `xhigh` |
| **Effort levels** | `minimal`, `low`, `medium`, `high`, `xhigh`, `max` |

## openai-responses

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/openai_responses/` |
| **Default effort** | `xhigh` |
| **Effort levels** | `minimal`, `low`, `medium`, `high`, `xhigh`, `max` |
| **Cache policy keys** | `cache_key_param`, `mode` |

## opencode

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/opencode/` |
| **Protocol** | `openai-completions` |
| **Base URL** | `https://opencode.ai/zen/v1` |
| **Protocol (openai-responses)** | `openai-responses` |
| **Base URL (openai-responses)** | `https://opencode.ai/zen/v1` |
| **Protocol (anthropic-messages)** | `anthropic-messages` |
| **Base URL (anthropic-messages)** | `https://opencode.ai/zen` |
| **Protocol (google-generative-ai)** | `google-generative-ai` |
| **Base URL (google-generative-ai)** | `https://opencode.ai/zen/v1` |
| **API-key env** | `OPENCODE_API_KEY` |

## opencode-go

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/opencode_go/` |
| **Protocol** | `openai-completions` |
| **Base URL** | `https://opencode.ai/zen/go/v1` |
| **API-key env** | `OPENCODE_API_KEY` |

## openrouter

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/openrouter/` |
| **Protocol** | `openai-completions` |
| **Base URL** | `https://openrouter.ai/api/v1` |
| **API-key env** | `OPENROUTER_API_KEY` |

## vercel-ai-gateway

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/vercel_ai_gateway/` |
| **Protocol** | `anthropic-messages` |
| **Base URL** | `https://ai-gateway.vercel.sh` |
| **API-key env** | `AI_GATEWAY_API_KEY` |

## vllm

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/vllm/` |
| **Protocol** | `openai-completions` |
| **Base URL** | `http://localhost:8000/v1` |

## xai

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/xai/` |
| **Protocol** | `openai-completions` |
| **Base URL** | `https://api.x.ai/v1` |
| **API-key env** | `XAI_API_KEY` |

## xai-subscription

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/xai_subscription/` |
| **Protocol** | `openai-responses` |
| **Base URL** | `https://cli-chat-proxy.grok.com/v1` |
| **Default effort** | `high` |
| **Effort levels** | `low`, `medium`, `high`, `xhigh` |

## zai

| | |
|---|---|
| **Directory** | `openprogram/models/providers/adapters/zai/` |
| **Protocol** | `openai-completions` |
| **Base URL** | `https://api.z.ai/api/coding/paas/v4` |
| **API-key env** | `ZAI_API_KEY` |
