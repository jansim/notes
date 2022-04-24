- Easy to use internet radio powered by raspberry Pi
- Single knob => corresponds to locations across the world

## Steps
1. Set up basic linux image on rpi (debian?)
	- incl sftp, ssh
	- remote development via vscode
2. Upgrade / update requirements
3. Install Python3
4. Install VLC
5. Install Python requirements

## ToDo
- [ ] Setup Basic Rpi Image
- [ ] Test audio playback via vlc
- [ ] Test basic GPIO (need hardware for this)
- [ ] Develop more complex interactions

## Info
- User: `pi`; password: `raspberry`
- 

## Hardware
- Jumper wires to connect stuff
	- definitely try female-to-female, maybe also try female-to-male
- Maybe other type of rotatry encoder
- https://www.tinytronics.nl/shop/en/cables-and-connectors/cables-and-adapters/prototyping-wires/dupont-compatible-and-jumper/dupont-jumper-wire-female-female-10cm-10-wires

## Resources
- Setup
	- https://desertbot.io/blog/headless-raspberry-pi-4-ssh-wifi-setup
- Complete
	- http://bobrathbone.com/raspberrypi/pi_internet_radio.html
		- Pi v1 not supported anymore!
- GPIO Interface
	- https://gpiozero.readthedocs.io/en/stable/installing.html
- Internetradio
	- Stations: https://www.radio-browser.info/
	- https://stackoverflow.com/questions/46758360/how-to-play-streaming-audio-from-internet-radio-on-python-3-5-3
- Airplay
	- https://github.com/openairplay/airplay2-receiver
	- https://github.com/mikebrady/shairport-sync
- Faster Boot
	- https://github.com/IronOxidizer/instant-pi

## Design
Angled big wooden plate (50 x 30cm or 40 x 25cm) with world map on it and one knob at the front. Slightly biger chuck at bottom to hold electronics; aux port at the end to connect to external speakers.
- evtl nutzbar: [Schon geschnittene Platte](https://www.amazon.de/Rayher-62810000-Holz-Weltkarte-100-gelasert/dp/B079CCF9BN/ref=sr_1_1?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=36EY0HORVH0FR&keywords=RAYHER+HOBBY+Holz-Weltkarte%2C+2+Platten%2C+FSC+100%25+Wooden+World+Map%2C+30+x+21+x+1+cm%2C+Brown&qid=1643464419&sprefix=rayher+hobby+holz-weltkarte+2+platten+fsc+100%25+wooden+world+map+30+x+21+x+1+cm+brown+%2Caps%2C47&sr=8-1)

![[World Radio Concept.excalidraw]]

![Wooden World Map &amp; Display Stand – Gladfolk](https://cdn.shopify.com/s/files/1/2198/6617/products/WorldMapBoardListing4_1024x1024@2x.jpg?v=1598383846)