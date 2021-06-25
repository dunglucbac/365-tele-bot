# 365-tele-bot
# 🍼 `office-user-bot`

[![forthebadge](https://forthebadge.com/images/badges/made-with-python.svg)](https://forthebadge.com)

## 🐙 Create an Office account with Telegram bot

![](readme/ea7870bb.png)
![](readme/adeff432.png)

### 🥼 Environment

```
python 3.6+
```

### 💢 Usage

#### 1. Create a new bot in @botfather

#### 2. Download the project

```
git clone https://github.com/zayabighead/office-user-bot.git
cd office-user-bot
pip install -r requirements.txt
```

#### 3. Create a new `config.json` in the same directory and edit as follows

```
{
  "bot": {
    "admin": bot administrator, fill in the user id of tg,
    "notify": true / false whether to accept the push when creating a new account,
    "token": "bot's token, obtained from botfather"
  },
  "aad": {
    "clientId": "client id of aad app",
    "clientSecret": "client secret of aad app",
    "tenantId": "Tenant id of aad app"
  },
  "office": {
    "subscriptions": [
      {
        "name": "Subscription display name",
        "sku": "Subscription id"
      }
    ],
    "domains": [
      {
        "display": "@******.org is for displaying domain names only",
        "value": "@abcde.org actual domain name"
      }
    ]
  },
  "banned": {
    "tgId": [id of the tg user to be blocked],
    "officeUsername": [
      "admin",
      "Username blacklist"
    ]
  }
}
```

#### 4. Run

```
python bot.py
```

Enter any message and the bot will reply

The generated activation code is saved in `codes.json` in the same directory
