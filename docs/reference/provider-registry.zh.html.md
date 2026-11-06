<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/models/providers/adapters/*/provider.json. -->


# 模型服务清单

各内置模型服务的协议配置直接来自 `provider.json`。登录和使用方法见[模型服务](../models/providers.zh.md)。

## alibaba-token-plan-cn

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/alibaba_token_plan_cn/` |
| **协议** | `openai-completions` |
| **基础 URL** | `https://token-plan.cn-beijing.maas.aliyuncs.com/compatible-mode/v1` |

## amazon-bedrock

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/amazon_bedrock/` |
| **协议** | `bedrock-converse-stream` |
| **基础 URL** | `https://bedrock-runtime.us-east-1.amazonaws.com` |
| **默认推理强度** | `high` |
| **推理等级** | `minimal`, `low`, `medium`, `high`, `xhigh`, `max` |
| **缓存策略键** | `breakpoint_format`, `max_breakpoints`, `mode`, `retention_ttl_map` |

## anthropic

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/anthropic/` |
| **协议** | `anthropic-messages` |
| **基础 URL** | `https://api.anthropic.com` |
| **密钥环境变量** | `ANTHROPIC_OAUTH_TOKEN`, `ANTHROPIC_API_KEY` |
| **默认推理强度** | `high` |
| **推理等级** | `minimal`, `low`, `medium`, `high`, `xhigh`, `max` |
| **缓存策略键** | `breakpoint_format`, `long_ttl_endpoints`, `max_breakpoints`, `mode`, `retention_ttl_map` |

## atlascloud

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/atlascloud/` |
| **协议** | `openai-completions` |
| **基础 URL** | `https://api.atlascloud.ai/v1` |
| **密钥环境变量** | `ATLASCLOUD_API_KEY` |

## azure-openai-responses

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/azure_openai_responses/` |
| **协议** | `azure-openai-responses` |
| **密钥环境变量** | `AZURE_OPENAI_API_KEY` |
| **默认推理强度** | `xhigh` |
| **推理等级** | `minimal`, `low`, `medium`, `high`, `xhigh`, `max` |

## cerebras

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/cerebras/` |
| **协议** | `openai-completions` |
| **基础 URL** | `https://api.cerebras.ai/v1` |
| **密钥环境变量** | `CEREBRAS_API_KEY` |

## deepseek

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/deepseek/` |
| **协议** | `openai-completions` |
| **基础 URL** | `https://api.deepseek.com/v1` |
| **密钥环境变量** | `DEEPSEEK_API_KEY` |
| **默认推理强度** | `medium` |
| **推理等级** | `minimal`, `low`, `medium`, `high`, `max` |

## gemini-subscription

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/gemini_subscription/` |
| **协议** | `gemini-subscription` |
| **基础 URL** | `https://cloudcode-pa.googleapis.com` |
| **密钥环境变量** | `GEMINI_API_KEY` |

## github-copilot

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/github_copilot/` |
| **协议** | `openai-responses` |
| **基础 URL** | `https://api.individual.githubcopilot.com` |
| **协议 (openai-completions)** | `openai-completions` |
| **基础 URL (openai-completions)** | `https://api.individual.githubcopilot.com` |
| **协议 (anthropic-messages)** | `anthropic-messages` |
| **基础 URL (anthropic-messages)** | `https://api.individual.githubcopilot.com` |
| **密钥环境变量** | `COPILOT_GITHUB_TOKEN`, `GH_TOKEN`, `GITHUB_TOKEN` |

## google

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/google/` |
| **协议** | `google-generative-ai` |
| **基础 URL** | `https://generativelanguage.googleapis.com/v1beta` |
| **密钥环境变量** | `GEMINI_API_KEY`, `GOOGLE_API_KEY`, `GOOGLE_GENERATIVE_AI_API_KEY` |
| **默认推理强度** | `medium` |

## google-gemini-cli

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/google_gemini_cli/` |
| **默认推理强度** | `medium` |

## groq

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/groq/` |
| **协议** | `openai-completions` |
| **基础 URL** | `https://api.groq.com/openai/v1` |
| **密钥环境变量** | `GROQ_API_KEY` |

## huggingface

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/huggingface/` |
| **协议** | `openai-completions` |
| **基础 URL** | `https://router.huggingface.co/v1` |
| **密钥环境变量** | `HF_TOKEN` |

## kimi-coding

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/kimi_coding/` |
| **协议** | `anthropic-messages` |
| **基础 URL** | `https://api.kimi.com/coding` |
| **密钥环境变量** | `KIMI_API_KEY`, `MOONSHOT_API_KEY` |

## llamacpp

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/llamacpp/` |
| **协议** | `openai-completions` |
| **基础 URL** | `http://localhost:8080/v1` |

## lmstudio

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/lmstudio/` |
| **协议** | `openai-completions` |
| **基础 URL** | `http://localhost:1234/v1` |

## local

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/local/` |
| **协议** | `openai-completions` |
| **基础 URL** | `http://localhost:8000/v1` |

## minimax

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/minimax/` |
| **协议** | `anthropic-messages` |
| **基础 URL** | `https://api.minimax.io/anthropic` |
| **密钥环境变量** | `MINIMAX_API_KEY` |

## minimax-cn

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/minimax_cn/` |
| **协议** | `anthropic-messages` |
| **基础 URL** | `https://api.minimaxi.com/anthropic` |
| **密钥环境变量** | `MINIMAX_CN_API_KEY`, `MINIMAX_API_KEY` |

## mistral

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/mistral/` |
| **协议** | `openai-completions` |
| **基础 URL** | `https://api.mistral.ai/v1` |
| **密钥环境变量** | `MISTRAL_API_KEY` |

## ollama

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/ollama/` |
| **协议** | `openai-completions` |
| **基础 URL** | `http://localhost:11434/v1` |

## openai

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/openai/` |
| **协议** | `openai-responses` |
| **基础 URL** | `https://api.openai.com/v1` |
| **密钥环境变量** | `OPENAI_API_KEY` |

## openai-codex

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/openai_codex/` |
| **协议** | `openai-codex` |
| **基础 URL** | `https://chatgpt.com/backend-api` |
| **默认推理强度** | `xhigh` |
| **推理等级** | `low`, `medium`, `high`, `xhigh`, `max` |

## openai-completions

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/openai_completions/` |
| **默认推理强度** | `xhigh` |
| **推理等级** | `minimal`, `low`, `medium`, `high`, `xhigh`, `max` |

## openai-responses

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/openai_responses/` |
| **默认推理强度** | `xhigh` |
| **推理等级** | `minimal`, `low`, `medium`, `high`, `xhigh`, `max` |
| **缓存策略键** | `cache_key_param`, `mode` |

## opencode

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/opencode/` |
| **协议** | `openai-completions` |
| **基础 URL** | `https://opencode.ai/zen/v1` |
| **协议 (openai-responses)** | `openai-responses` |
| **基础 URL (openai-responses)** | `https://opencode.ai/zen/v1` |
| **协议 (anthropic-messages)** | `anthropic-messages` |
| **基础 URL (anthropic-messages)** | `https://opencode.ai/zen` |
| **协议 (google-generative-ai)** | `google-generative-ai` |
| **基础 URL (google-generative-ai)** | `https://opencode.ai/zen/v1` |
| **密钥环境变量** | `OPENCODE_API_KEY` |

## opencode-go

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/opencode_go/` |
| **协议** | `openai-completions` |
| **基础 URL** | `https://opencode.ai/zen/go/v1` |
| **密钥环境变量** | `OPENCODE_API_KEY` |

## openrouter

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/openrouter/` |
| **协议** | `openai-completions` |
| **基础 URL** | `https://openrouter.ai/api/v1` |
| **密钥环境变量** | `OPENROUTER_API_KEY` |

## vercel-ai-gateway

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/vercel_ai_gateway/` |
| **协议** | `anthropic-messages` |
| **基础 URL** | `https://ai-gateway.vercel.sh` |
| **密钥环境变量** | `AI_GATEWAY_API_KEY` |

## vllm

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/vllm/` |
| **协议** | `openai-completions` |
| **基础 URL** | `http://localhost:8000/v1` |

## xai

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/xai/` |
| **协议** | `openai-completions` |
| **基础 URL** | `https://api.x.ai/v1` |
| **密钥环境变量** | `XAI_API_KEY` |

## xai-subscription

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/xai_subscription/` |
| **协议** | `openai-responses` |
| **基础 URL** | `https://cli-chat-proxy.grok.com/v1` |
| **默认推理强度** | `high` |
| **推理等级** | `low`, `medium`, `high`, `xhigh` |

## zai

| | |
|---|---|
| **目录** | `openprogram/models/providers/adapters/zai/` |
| **协议** | `openai-completions` |
| **基础 URL** | `https://api.z.ai/api/coding/paas/v4` |
| **密钥环境变量** | `ZAI_API_KEY` |
