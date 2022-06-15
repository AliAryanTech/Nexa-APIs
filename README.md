# Nexa-API 🌊
Simple, Free and easy to use Public api built with [Fastapi](https://fastapi.tiangolo.com/)


# List of endpoints 🎗️
- Search
    - [`reddit`](api/routes/reddit.py) - Search for posts in reddit
    - [`urban dict`](api/routes/urbandict.py) - Search for definitions in urban dict
    - [`wallpapers`](api/routes/wallpapers.py) - Fetch wallpapers from reddit
    - [`npm search`](api/routes/npm_search.py) - Search for npm packages
    - [`1337x search`](api/routes/1337x_search.py) - Search for torrents in 1337x

- Language
    - [`acronym`](api/routes/acronyms.py) - Get the meaning of an acronym
    - [`define`](api/routes/define.py) - Get the definition of a word
    - [`translate`](api/routes/translate.py) - Translate text using google translate

- Tools
    - [`password`](api/routes/password.py) - Generates a random password according to the given length
    - [`color_palette`](api/routes/color_palette.py) - Generate color palettes from images
    - [`currency`](api/routes/currency_cov.py) - Exchange rate from 'x' to 'y'. Data is **scraped** from [x-rates](https://www.x-rates.com/)

- File server
    - [`storage`](api/routes/storage.py) - Store files on the server [Read more](https://github.com/Itz-fork/Nexa-API/wiki/Route:-Storage)

- Fun
    - [`fact`](api/routes/facts.py) - Get a random fact
    - [`insult`](api/routes/insult.py) - Insult somebody ( ✧≖ ͜ʖ≖)


# Deploy it! 🚀
This api is open source, you can deploy your own version easily 🤗

### Locally 💻,
```sh
git clone https://github.com/Itz-fork/Nexa-API
cd Nexa-API
pip3 install -r requirements.txt
bash start.sh
```

### Heroku ☁️
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/Itz-fork/Nexa-API)


# Development 🧑‍💻
Here are somethings to note,

- You can find config files in [`config`](api/config) directory
- Reusable functions are located in [`functions`](api/functions) directory
- You can find routes in [`routes`](api/routes) directory
- Use [`start script`](start.sh) when running the dev server (`bash start.sh dev`)

## Add new routes 👨‍🎨
- Create a new file in [`routes`](api/routes) directory (Ex: `myRoute.py`)
- Add this code (Here we add new route named `/test` which returns the text, `Hello from Fastapi, Nexa-API 🌊`)
```python
from fastapi import APIRouter
from ..functions.response import send_response

route = APIRouter()

@route.get("/test")
async def test_route():
    return await send_response("Hello from Nexa-API 🌊")
```
- Start the development server
```sh
bash start.sh dev
```


# License & Credits 👮‍♂️ ♥️
- Licensed under [MIT License](LICENSE)
- Credits to [emoji - aranja](https://emoji.aranja.com/) for the [favicon](favicon.ico)