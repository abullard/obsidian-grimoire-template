#diataxis/grimoire/tutorial #obsidian/copilot #localhost
### [[MoC - Grimoire|← Parent]]
### API Key LLM
- You can supply the [Obsidian Copilot](https://www.obsidiancopilot.com/en/docs) plugin with an API key, and push RAG on your Grimoire through a Data Center, but I haven't explored that path yet. I wanted to keep it local first for privacy.
### Local LLM
> [!WARNING] Heads Up
>  I experimented with this for a long time, and eventually concluded that I don't have the hardware to run a local model that's up to the task of RAG on this Obsidian vault. Be aware of hardware requirements.

📘 *RAG*: Retrieval Augmented Generation - Retrieval-augmented generation is a technique that enables large language models to retrieve and incorporate new information. With RAG, LLMs do not respond to user queries until they refer to a specified set of documents. These documents supplement information from the LLM's pre-existing training data. This allows LLMs to use domain-specific and/or updated information that is not available in the training data.

## Install Ollama CLI and the LLMs

```bash
$ brew install ollama
$ ollama serve
```

Leave `ollama serve` running & open a new terminal.

```bash
$ ollama pull gpt-oss:20b
$ ollama pull nomic-embed-text
$ ollama run gpt-oss:20b
```

Set context window size and save the model. 10000 tokens means 10000 words available to reference as "chat history".

```bash
$ /set parameter num_ctx 10000
$ /save gpt-oss:20b
$ /bye
```

Stop the original `ollama serve` command. We need to set Obsidian's Origin path for `ollama serve`. Export `.zshrc` path or make an `alias`.

```bash
$ alias copilot="OLLAMA_ORIGINS=app://obsidian.md* ollama serve"
$ copilot
```

> [!important]
> You don't need to specify a model in the `ollama serve` command. Whatever models you `pull` will be exposed with this one command.

## Hook up the model to Obsidian Copilot Plugin

Open Obsidian Copilot Model settings

![[Pasted image 20250809160151.png]]

Click "+ Add Custom Model" button. Mirror these settings if you're using Ollama `gpt-oss:20b`. Click "Confirm"

![[Pasted image 20250809170025.png]]

Scroll down to the Embedding Models section. Click "+ Add Custom Model" button. Mirror these settings if you're using `nomic-embed-text` for vault vectorization.

![[Pasted image 20250809170215.png]]

> [!success]
> This completes the setup. Trouble shoot any errors you encounter.

---

> [!todo] Try it out!
> You should now be able to open the copilot chat and ask it natural language questions about the contents of your vault. Make sure you use "Vault (QA)" mode.

> [!error]
> If it cannot answer questions about the contents of your vault, your model may be too powerful for your machine, or your embed model may vectorize your vault index in a different dimension than your model can handle.
