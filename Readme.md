# Mifos Slack Chat Archive

Uses https://github.com/apache/fineract-chat-archive to archive public Slack chat messages to GitHub Pages.

See automations in `.github/workflows/`.

## Local run

### Bash shell on Ubuntu LTS desktop

```bash
sudo apt install openjdk-25-jdk-headless

git clone https://github.com/apache/fineract-chat-archive/
git clone https://github.com/mifos/chat-archive/

export SLACK_TOKEN="redacted"
export SITE_BASE_URL='https://mifos.github.io/chat-archive'
export CHANNELS_ALLOWLIST='#fineract'
export OUTPUT_DIR="$PWD/chat-archive/docs"
export OUTPUT_DIR="$PWD/chat-archive/state"
export LOOKBACK_DAYS=1

cd fineract-chat-archive
./gradlew --quiet updateChatArchive
```

## Copyright and License

This archive is ©2026 Mifos Initiative. Some rights reserved. Released under the [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0) License](https://creativecommons.org/licenses/by-sa/4.0/).

Includes ASF software `scripts/verify-signed-commits.sh` from <https://github.com/apache/fineract/commit/d61b5e65f940f722e5610c36201b42bf0f3d70f1>.
