# ESQP Labs

![example workflow](https://github.com/tsaplyadmitriy/esqplabs/actions/workflows/spellcheck.yaml/badge.svg)

This repo contains implementation of three tasks for ESQP course:

- Configure GitHub Action to send a message to Telegram when the build fails
- Create GitHub Action to spel check README.nd using aspell
- Design a coding style guide (in Markdown) for your favorite language

I've creaed codestyle document for Dart programming language and added spellchecking + telegram notifications into Github Actions

I've added spellchecking github action that checks all .md files in this repository.

I've added telegram notifications when spellchecking fails.

To activate telegram notifications, you should:

- Create your own telegram bot
- Put bot token as ``TELEGRAM_TOKEN`` repository secret
- Add your chat id as ``TELEGRAM_ID`` repository secret. [See how to do it in this guide](https://github.com/marketplace/actions/telegram-notify)
