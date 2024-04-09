# NoPixel-4.0-bug

BUG: No Clothing (+ No Voice Chat?): 2 logs + UI png


Note: I'm a pretty new gta player so there could be some simple things I am doing wrong on the client side that cause or compound the issues I'm having.

## Behavior:
1. While at clothing store, cannot view or buy any clothing articles.
2. Unable to hear any player voice chat, though all other game sounds appear work (Did hear one player in voice-chat in the stairwell of the apartments on load).

## Expected behavior:
1. Be able to view and purchase clothes.
2. Be able to hear player voice chat.

## Detailed Player-actions:
- On very first time joining NoPixel Blue server, at character creation screen, only 1 or 2 clothing item available per character.
- On load -> Adjusted key-binds in apartment.
- Walked down apartment stairs, crossed paths with 2 people, 1 said hi. This is the only voice-chat I heard during 2 session over ~2 hours on server. 
- Went to clothing store by apartments -> no clothing available to view or purchase (other than change color of current clothes).
- Went to second clothing store, same behavior -> then to barber shop where I could change my ped model  (and get the new default clothes with the ped).
- Went to second clothing store again (iirc), no change in behavior.
- Tried to work a job (Gruppe 6), sign-in -> purchase smallest truck -> create group -> ready-up from jobs all successfully. 
- A couple of  other players present, tried communicating with voice chat, no response from anyone, to ask questions / or join job
- No jobs offers, after ~20 minutes leave Gruppe 6.
- Got run over by NPC, limped to hospital.
- One doctor on duty, told him my injuries and that warned him that my "ears" might not be working.
- Doctor seems to respond but I cant hear anything, only see his mouth moving.
- Doctor heals my injuries, thank him and leave, second player there but didn't hear him either.
- Walked back to apartment.
- Quit client and rejoined server.
- Went back to clothing store, same behavior.
- Ultimately went back to apartments and quit client.

## Extenuating Circumstances
- This was my first successfully server-join on NoPixel 4.0 Public Blue.
- Client running on remote desktop (Windows 10 rented server by ShadowPc -> OVH Datacenter).
- My peripherals (mouse, keyboard, headset, mic, PlayStation controller) were all working on the remote machine on discord/GTA V base/ self-hosted FiveM base server.
- Upon connecting to NoPixel Blue, my FiveM client must restart to be compatible with server FiveM version (2802 ?).

## Possible relevant lines in logs (Start of error):
Just anything I could find related to general errors/clothing/audio. I used log 02 since it it shorter and the session had the same bugs. 

### log 02
- [    122984] [b2802_GTAProce]             MainThrd/ can't register compcache:/np_4.0_f2_clothing_encrypted/pedalternatevariations.meta: no streaming module (does this file even belong in stream?)

- [    238109] [b2802_GTAProce] ResourcePlacementThr/ Physics validation failed for asset char_sel_shell_col.ybn.
- [    238109] [b2802_GTAProce] ResourcePlacementThr/ This asset is **INVALID**, but we've fixed it for this load. Please fix the exporter used to export it.

- [    315250] [b2802_GTAProce]             MainThrd/ Returning device Speakers (Virtual Audio Device (WDM) - ShadowVirtualSpeaker) for GUID {4AA7DB14-79E4-4744-BE39-93A5726B6812}
- [    315266] [b2802_GTAProce] [Mumble] Audio Input/ Returning device Microphone (Steam Streaming Microphone) for GUID {0C0B938C-32F3-4AD4-A010-0EBB526B458E}
- [    315297] [b2802_GTAProce] [Mumble] Audio Input/ MumbleAudioInput::InitializeAudioDevice: Initialized audio capture device.

- [    343188] [b2802_GTAProce] ResourcePlacementThr/ Mumble: ConnectedPhysics validation failed for asset kt1_12_0.ybn.

- [    343203] [b2802_GTAProce]      UV loop: mumble/ ^3Warning: UDP packets can *not* be received. Switching to TCP tunnel mode.^7
- [    343703] [b2802_GTAProce]      UV loop: mumble/ UDP packets can be received. Switching to UDP mode.

- [    697500] [b2802_GTAProce]        CrBrowserMain/ ResizeObserver loop limit exceeded (@clothing/nui/dist/index.html:0)
