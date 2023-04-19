# ChatGPT Telegram Bot: **GPT-4. Fast. No daily limits. Special chat modes**

## Features

- Low latency replies (it usually takes about 3-5 seconds)
- No request limits
- Message streaming (watch demo)
- GPT-4 support
- Voice message recognition
- Code highlighting
- Special chat modes: 👩🏼‍🎓 Assistant, 👩🏼‍💻 Code Assistant, 📝 Text Improver and 🎬 Movie Expert. You can easily create your own chat modes by editing `config/chat_modes.yml`
- Support of [ChatGPT API](https://platform.openai.com/docs/guides/chat/introduction)
- List of allowed Telegram users
- Track $ balance spent on OpenAI API

---

## News

- _24 Mar 2023_: GPT-4 support. Run `/settings` command to choose model
- _15 Mar 2023_: Added message streaming. Now you don't have to wait until the whole message is ready, it's streamed to Telegram part-by-part (watch demo)
- _9 Mar 2023_: Now you can easily create your own Chat Modes by editing `config/chat_modes.yml`
- _8 Mar 2023_: Added voice message recognition with [OpenAI Whisper API](https://openai.com/blog/introducing-chatgpt-and-whisper-apis). Record a voice message and ChatGPT will answer you!
- _2 Mar 2023_: Added support of [ChatGPT API](https://platform.openai.com/docs/guides/chat/introduction). It's enabled by default and can be disabled with `use_chatgpt_api` option in config. Don't forget to **rebuild** you docker image (`--build`).

## Bot commands

- `/retry` – Regenerate last bot answer
- `/new` – Start new dialog
- `/mode` – Select chat mode
- `/balance` – Show balance
- `/settings` – Show settings
- `/help` – Show help

## Setup

1. Get your [OpenAI API](https://openai.com/api/) key

2. Get your Telegram bot token from [@BotFather](https://t.me/BotFather)

3. Edit `config/config.example.yml` to set your tokens and run 2 commands below (_if you're advanced user, you can also edit_ `config/config.example.env`):

   ```bash
   mv config/config.example.yml config/config.yml
   mv config/config.example.env config/config.env
   ```

4. 🔥 And now **run**:
   ```bash
   docker-compose --env-file config/config.env up --build
   ```

## References

1. [_Build ChatGPT from GPT-3_](https://learnprompting.org/docs/applied_prompting/build_chatgpt)
