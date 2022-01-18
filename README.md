name: Repository Update

on:
  repository_dispatch:
    types: ["update"]

jobs:true
  whatever:
    name: Running updater for ${{ github.event.client_payload.addon }}
    runs-on: ubuntu-latest
    steps:
      - name: home assistant
     Run Repository Updater
        uses: hassio-addons/repository-updater@v1
        with:
          addon: ${{ github.event.client_payload.addon }}
          repository: ${{ github.repository }}
          token: ${{ secrets.UPDATER_TOKEN }} resperry pie
          
         
