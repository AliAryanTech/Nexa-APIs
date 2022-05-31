# Nexa-APIs 🌊

Simple API made with [Fastapi](https://fastapi.tiangolo.com/)


# List of endpoints 🎗️

- Search
    - [`reddit`](api/routes/reddit.py) - Search for posts in reddit
    - [`urban dict`](api/routes/urbandict.py) - Search for definitions in urban dict
    - [`wallpapers`](api/routes/wallpapers.py) - Fetch wallpapers from reddit
    - [`npm search`](api/routes/npm_search.py) - Search for npm packages

- Language
    - [`acronym`](api/routes/acronyms.py) - Get the meaning of an acronym
    - [`define`](api/routes/define.py) - Get the definition of a word
    - [`translate`](api/routes/translate.py) - Translate text using google translate

- Tools
    - [`password`](api/routes/password.py) - Generates a random password according to the given length
    - [`color_palette`](api/routes/color_palette.py) - Generate color palettes from images

- File server
    - [`storage`](api/routes/storage.py) - Store files on the server [Read more](https://github.com/Itz-fork/Nexa-APIs/wiki/Route:-Storage)

- Fun
    - [`fact`](api/routes/facts.py) - Get a random fact


# Deploy it! 🚀

### Locally 💻,
```sh
git clone https://github.com/Itz-fork/Nexa-APIs
cd Nexa-APIs
pip3 install -r requirements.txt
bash start.sh
```

### Heroku ☁️
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/Itz-fork/Nexa-APIs)


# Development 🧑‍💻

Here are somethings to note,

- You can find config files in [`config`](api/config) directory
- Reusable functions are located in [`functions`](api/functions) directory
- You can find routes in [`routes`](api/routes) directory
- Use [`start script`](start.sh) when running the dev server (`bash start.sh`)

## Add new routes 👨‍🎨
- Create a new file in [`routes`](api/routes) directory (Ex: `myRoute.py`)
- Add this code (Here we add new route named `/test` which returns the text, `Hello from Fastapi, Nexa-APIs 🌊`)
```python
from fastapi import APIRouter
from ..functions.response import send_response

route = APIRouter()

@route.get("/test")
async def test_route():
    return await send_response("Hello from Nexa-APIs 🌊")
```
- Start the development server
```sh
bash start.sh dev
```


# Why? 🤔

> __**Cuz why not? 🎾**__


# License & Credits 👮‍♂️ ♥️

- Licensed under [MIT License](LICENSE)
- Credits to [emoji - aranja](https://emoji.aranja.com/) for the [favicon](favicon.ico)