# Quick Hacks

We have various repos full of code to extract complex datasets... but sometimes all you need is a couple of lines of code to grab something important. When someone does something clever and (hopefully) repeatable, we put it here. So, here you go, have fun!

### Harvest videos from a youtube account

Install [youtube-dl](https://github.com/rg3/youtube-dl) (instructions in link, or in Arch Linux `yaourt -S youtube-dl`, doubtless similar in other Linuxes).

Then, in shell:

```sh
youtube-dl -o '%(uploader)s/%(playlist)s/%(playlist_index)s - %(title)s.%(ext)s' -f 'bestvideo[height<=480]+bestaudio/best[height<=480]' --yes-playlist https://www.youtube.com/user/USEPAgov/playlists
```

### Browsing via Selenium

See this gist [gist](https://gist.github.com/grosscol/6f0cef8236e2099166bd343a414fcdd0)

## Resources

- [jq](https://stedolan.github.io/jq/) for parsing JSON
- Inspecting Ajax requests with [Chrome Developer tools](https://coderwall.com/p/-fdgoq/chrome-developer-tools-adds-copy-as-curl):
  - Use inspect, network, and under Headers "copy as curl" (sessionID etc..) (useful for ajax, js)
- Ruby gem [watir](https://watir.com) headless browsing
