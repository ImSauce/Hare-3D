# 🏕️ Hare's Campsite

View **Omagari Hare** from *Blue Archive* in augmented reality, in both her **Camping** and **Default** outfits. Place her in your own room with just your phone's camera. No app to install. This is just a personal project so i can have Hare in my room using AR camera.

**▶ Open the site:** https://imsauce.github.io/Hare-3D/

## What it does

- Switch between **two outfits**: Camping (33 animations) and Default (6 animations)
- Preview every animation in 3D right in your browser
- Tap **View in my room** to place her on your floor in AR
- Every animation has its own link, so you can share a specific one (for example `#Camping/Exs` for her EX skill, or `#Default/Cutin`)

### Camping outfit (33)

| Group | Animations |
|---|---|
| Victory | Victory, Victory finish |
| EX skill | EX skill, EX cut-in |
| Café | Relaxing, Walking, Reaction |
| Standing combat | Ready, Aim, Firing loop, Lower weapon, Hold aim, Reload, Reload (alt), Callsign |
| Kneeling combat | Ready, Aim, Firing loop, Lower weapon, Hold aim, Reload, Reload (alt) |
| Moving | Running loop, Jump, Stop (standing), Stop (kneeling) |
| Formation | Idle, Picked |
| Taking hits | Panic, Retreat, Down loop, Knocked out |
| Other | Lobby pose |

### Default outfit (6)

| Group | Animations |
|---|---|
| Café | Relaxing, Walking, Reaction |
| Formation | Idle |
| Special | Tactical start, Cut-in |

## Requirements

AR works on **Android phones that support [Google Play Services for AR](https://play.google.com/store/apps/details?id=com.google.ar.core)** (ARCore). You can check whether your phone is supported on Google's [ARCore devices list](https://developers.google.com/ar/devices).

On other devices you can still use the 3D preview, but the AR button won't work.

## How to use

1. Open the site in **Chrome** on your Android phone.
2. Pick an outfit at the top (**Camping** or **Default**), then tap an animation to preview it.
3. Tap **View in my room** and allow camera access.
4. Point your camera at the floor and move the phone slowly until she appears.
5. Drag to move her, pinch to resize, and twist with two fingers to rotate.

Tip: animations loop in AR, so the "loop" ones (firing, running, down) look the smoothest.

## How it works

The original model contains every animation in one file, but Google Scene Viewer (Android's built-in AR viewer) only plays the first one. So the model was split into **one file per animation**, each keeping only its own animation data. This also made the files much smaller (Camping: about 7.7 MB → 2 MB each; Default: about 1.3 MB → 0.9 MB each), so they load faster.

```
index.html                     the website (both outfits)
Hare_Camping_<Animation>.glb   Camping outfit, one file per animation (33 files)
Hare_Default_<Animation>.glb   Default outfit, one file per animation (6 files)
```

## Credits

- 3D models from the [Blue Archive Wiki](https://bluearchive.wiki/wiki/Models), via [lihaohong6/BlueArchiveModels](https://github.com/lihaohong6/BlueArchiveModels)
- Idea inspired by [@KotoriSenseiBA](https://x.com/KotoriSenseiBA)'s AR experiment

## Disclaimer

This is a non-commercial fan project. *Blue Archive* and all of its characters and assets belong to **NEXON Games** and **Yostar**. This project is not affiliated with or endorsed by them. If you're a rights holder and want something removed, please open an issue.
