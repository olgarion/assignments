# h6 Onion

## Shavers & Bair 2016: Hiding Behind the Keyboard: The Tor Browser €; subchapters: "Introduction", "History and Intended Use of The Onion Router", "How The Onion Router Works", "Tracking Criminals Using TOR". (https://learning.oreilly.com/library/view/hiding-behind-the/9780128033524/XHTML/B9780128033401000021/B9780128033401000021.xhtml#s0010)

TOR (The Onion Router browser) is an Internet Browser built out of Firefox that hides IP address.
Why to use:
- to access web sites restricted or blocked by government in your country (if you can install TOR)
- anonymous contact of officials such as police

TOR was developed by S government originally in 2002 and now they try to find a awy to deanonymize TOR's users

TOR uses several layers of encryption for disguising a user's internet traffic information, it sends it from a relay to a relay randomly (chooses random routes every 10 minutes) and encrypt information until it reaches the exit relay that connects to the final web site. 3 relays are used for the encryption: Entry, Middle and Exit relays, so information re-routed and encrypted 3 times, and last data is sent to the final address unencrypted. It means if a final receiver would try to understand where the message came from it will know the address of Exit router only.
These relays that allow encryption are users' computers, it is a community of volunteers that are part of the TOR's network. Anyone can make a server that will allow to encrypt the IP and send it to the next server until exit.