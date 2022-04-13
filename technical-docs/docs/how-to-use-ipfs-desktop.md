# How to use IPFS Desktop

## How to use IPFS Desktop

## Hiya!

Uploading gigantic folders and files to IPFS sometimes could be tricky! But we are going to make it. I tried to write complete instructions on how to do this. But feel free to ask if something isn't going according to plan. 😉

### IPFS Desktop

1. First thing we need to do is to install [IPFS Desktop client](https://docs.ipfs.io/install/ipfs-desktop/#install-instructions). Follow the link and choose your option.
2. Open your IPFS Desktop and wait a bit until it loads.

### Configurations

1. By default IPFS protects you from memory clogging. But it also prevents us from uploading large files! On sidebar on the left go to `SETTINGS` tab.

![https://user-images.githubusercontent.com/33105890/154506592-19594304-3c34-4e41-949d-2859a6d4cac0.png](https://user-images.githubusercontent.com/33105890/154506592-19594304-3c34-4e41-949d-2859a6d4cac0.png)

1. Scroll down to `IPFS CONFIG` section

![https://user-images.githubusercontent.com/33105890/154507662-afc0c937-3230-473d-b467-eb991ee67030.png](https://user-images.githubusercontent.com/33105890/154507662-afc0c937-3230-473d-b467-eb991ee67030.png)

1. Set `"GCPeriod"` to `"10h"` (it should be `"1h"` by default)

![https://user-images.githubusercontent.com/33105890/154508482-c9c268e0-0b08-4cf8-aebc-8bc6d1249bcf.png](https://user-images.githubusercontent.com/33105890/154508482-c9c268e0-0b08-4cf8-aebc-8bc6d1249bcf.png)

1. Set `"StorageGCWatermark"` to 99. And set `"StorageMax"` to your content size + 15GB (e.g. if your folder size is 50GB set `"StorageMax"` to `"65GB"`)

![https://user-images.githubusercontent.com/33105890/154508801-0df387b1-169d-4b29-ab75-6408ad1141cb.png](https://user-images.githubusercontent.com/33105890/154508801-0df387b1-169d-4b29-ab75-6408ad1141cb.png)

1. Go up to `IPFS CONFIG` section and hit `Save`

![https://user-images.githubusercontent.com/33105890/154509205-e5ccb3e6-2345-4708-8885-fc937ec8128c.png](https://user-images.githubusercontent.com/33105890/154509205-e5ccb3e6-2345-4708-8885-fc937ec8128c.png)

1. Yep! Restart your IPFS app. Just close and open it again 😄

That was the hardest part! Let's start uploading 😜

### Uploading

1. Go to `FILES` tab on your sidebar.

![https://user-images.githubusercontent.com/33105890/154509872-e8ad006f-a21a-4e64-b796-3d45052f57ee.png](https://user-images.githubusercontent.com/33105890/154509872-e8ad006f-a21a-4e64-b796-3d45052f57ee.png)

1. Click `+Import` button and select your folder.

![https://user-images.githubusercontent.com/33105890/154510047-bac65fe0-8b7d-426c-bf22-b3f34b33d097.png](https://user-images.githubusercontent.com/33105890/154510047-bac65fe0-8b7d-426c-bf22-b3f34b33d097.png)

1. Wait a bit and you should see folder on your screen. Click on three dots on the right and select `Set pinning`.

![https://user-images.githubusercontent.com/33105890/154511227-3df170c5-11eb-456a-b59a-2e6665d87ee2.png](https://user-images.githubusercontent.com/33105890/154511227-3df170c5-11eb-456a-b59a-2e6665d87ee2.png)

1. Select `Local node` and `Apply`

![https://user-images.githubusercontent.com/33105890/154511608-166c33cb-37dc-43a0-bd2a-15da80aa6d06.png](https://user-images.githubusercontent.com/33105890/154511608-166c33cb-37dc-43a0-bd2a-15da80aa6d06.png)

1. Click on three dots again and copy your CID.

![https://user-images.githubusercontent.com/33105890/154512085-00a0f739-c6fa-4d23-8b20-b17f0cd10aed.png](https://user-images.githubusercontent.com/33105890/154512085-00a0f739-c6fa-4d23-8b20-b17f0cd10aed.png)

1. Send your CID to us!

This is it! Now it's time for us to retrieve your content from your node! It's like a torrenting. So please don't close your IPFS Desktop app until we upload all your files (we'll pin it to the IPFS network - so when you disconnect, the files will still be available). We'll let you know when it's over. 😊
