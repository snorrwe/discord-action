Port of https://github.com/hreeder/discord-post-updater

# Discord Message Updater

Post or update messages on [Discord](discord.com/). 


## Configuration

| Environment variable | Required | Default value | Effect |
| :-- | :-- | :-- | :-- |
| `DISCORD_TOKEN` | `true`  | `undefined` | The authentication token of your bot. |
| `DISCORD_CHANNEL` | `true` | `undefined` | The channel id this action will post in. |
| `DISCORD_MESSAGE` | `false` | The id of the last message | The id of the message to update. If omitted, or if the value is `new`, then a new message will be posted. If omitted, then the last message in the channel will be edited. |
| `POST_FILE` | `false` | "/etc/discord-post/post" | The contents of this file will be posted as the message |

## Usage

```yaml
      - name: Deploy on Discord
        uses: snorrwe/discord-action@v1.0.4
        with:
          discord_message: new
          discord_token: ${{ secrets.DISCORD_BOT_TOKEN }}
          post_file: CHANGELOG.md
          discord_channel: '1062517242148958228' # N.B. The quote marks here are required
```
