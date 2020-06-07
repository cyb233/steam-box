# 


<p align="center">
  <img width="400" src="https://user-images.githubusercontent.com/8252317/83969719-1675be80-a904-11ea-8776-92342421e4ee.png">
  <h3 align="center">steam-box</h3>
  <p align="center"><img width="20" height="20" src="https://store.steampowered.com/favicon.ico"></img> Update a pinned gist to contain your Steam playtime leaderboard. </p>
  
   <p align="center">
    <a href="https://github.com/YouEclipse/steam-box/workflows/Update%20gist%20with%20Steam%20Playtime/badge.svg"><img src="https://github.com/YouEclipse/steam-box/workflows/Update%20gist%20with%20Steam%20Playtime/badge.svg" alt="Update gist with Steam Playtime"></a>
  </p>
</p>


---
English | [简体中文](./README_zh.md)



## 💻 Setup

### 🎒 Prep work
1. Create a new public GitHub Gist (https://gist.github.com/)
1. Create a token with the `gist` scope and copy it. (https://github.com/settings/tokens/new)
1. Create a Steam  API key. (https://steamcommunity.com/dev/apikey)
1. Find the steam ID of your account. (https://steamid.io)


### 🚀 Project setup
1. Fork this repo
1. Edit the [environment variable](https://github.com/YouEclipse/steam-box/actions/runs/126970182/workflow#L17-L19) in `.github/workflows/schedule.yml`:

   - **GIST_ID:** The ID portion from your gist url: `https://gist.github.com/YouEclipse/`**`9bc7025496e478f439b9cd43eba989a4`**.

1. Go to the repo **Settings > Secrets**
1. Add the following environment variables:
   - **GH_TOKEN:** The GitHub token generated above.
   - **STEAM_API_KEY:** The steam API key you created above. 
   - **STEAM_ID:** The steam ID of your account. 
1. If you want to show specific games,put the ids in environmet variable **APP_ID**:
   - like `APP_ID=431960,730`
   - you can get the id of a game from the store url:`https://store.steampowered.com/app/`**730**`/CounterStrike_Global_Offensive/`

## 🕵️ How it works
- Get your games playtime from [Steamwork Web API](https://partner.steamgames.com/doc/webapi) 
- Update Gist with Github API 
- Use Github Actions for updating Gist  

## 📄 License
This project is licensed under [Apache-2.0](./LICENSE)