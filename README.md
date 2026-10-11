# Salvo Brawl

A live 2–4 player tank brawler. The computer (or a TV plugged into it) shows the battle, and each player uses their phone as a controller by scanning a QR code. Keyboards and game controllers work too.

## What's in this folder

| File | What it is |
|---|---|
| `index.html` | The game. Open this on the big screen. |
| `controller.html` | The phone controller. Phones open it by scanning the QR code. |
| `README.md` | This guide. |

## Put it online with GitHub Pages (about 5 minutes)

Phones can only connect when the game runs from a real website, so it needs to be published once.

1. Sign in at [github.com](https://github.com) and click **New** (the green button) to make a new repository.
2. Name it `salvo-brawl`, set it to **Public**, and click **Create repository**.
3. On the new repository page, click **uploading an existing file**. Drag in `index.html`, `controller.html` and `README.md`, then click **Commit changes**.
4. Open the repository's **Settings** tab, then **Pages** in the left sidebar.
5. Under **Build and deployment**, set **Source** to **Deploy from a branch**. Pick the **main** branch and the **/ (root)** folder, then click **Save**.
6. Wait a minute or two, then refresh the Pages settings screen. It shows your site's address, which looks like `https://YOUR-USERNAME.github.io/salvo-brawl/`.

To update the game later, upload the new files to the same repository. The site refreshes on its own within a couple of minutes.

## Playing

1. Open your site address on the computer and click **Fullscreen**.
2. Each player scans the QR code with their phone camera. If scanning doesn't work, open the link shown under the code and type the four-letter room code.
3. On the phone, pick a tank and tap **READY UP**. When everyone is ready, the brawl starts on its own. The computer can also start it with **START BRAWL** or the Enter key.
4. Turn phones sideways for the controller.

Up to 4 players, in any mix of phones, keyboard players and game controllers. You need at least 2 to start.

### Phone controls

- **Left half:** put your thumb down anywhere and slide. Left and right drive. **Push up to fire the jetpack.** Pull down to drop through a floating ledge.
- **Right half:** drag in the direction you want to shoot. The farther you drag, the more power. **Let go to fire.** A quick tap fires your last shot again.

### Keyboard controls

| | Keys 1 | Keys 2 |
|---|---|---|
| Join in the lobby / ready up | G | K |
| Change tank in the lobby | F / H | J / L |
| Drive | A / D | ← / → |
| Jetpack (hold) | W | ↑ |
| Drop through ledge | S | ↓ |
| Aim barrel | F / H | J / L |
| Fire | Hold G to charge, release | Hold K to charge, release |

Esc pauses, M mutes. Game controllers join with A, use the left stick to drive (A or LB for jetpack), the right stick to aim and set power, and RT or RB to fire.

### Rules

- Everyone has **3 lives**.
- Hits drain health. A **direct hit** does the most damage; near misses do less the farther away they land.
- Every hit **knocks you back**, and the more damage you've taken, the farther you fly.
- Use the jetpack to fly back onto the map after a knockback. Fuel refills while you're on the ground.
- Falling off the map is **instant death**: you lose a life no matter how much health you had.
- Running out of health also costs a life. You respawn at the top after a couple of seconds, briefly invincible.
- The last tank with lives left wins.

### Tanks

| Tank | Role | Advantage | Trade-off |
|---|---|---|---|
| Vanguard | All-rounder | Balanced in every stat | None |
| Striker | Scout | 25% faster, 30% more jet fuel | 15% less health |
| Bulwark | Heavy | 35% more health, hard to knock back | 20% slower |
| Ravager | Demolition | 15% bigger blast radius, 15% more knockback | Slower reload |
| Viper | Rapid fire | Reloads 40% faster, quicker missiles | 15% less damage |

## If something goes wrong

- **The QR box says "NO ROOM":** the computer couldn't reach the room server. Check the internet connection and click **TRY AGAIN**.
- **A phone says "ROOM NOT FOUND":** check the code on the big screen. If you reloaded the game page, it makes a new code, so scan again.
- **Phones connect at home but not on another network:** some school, work or public Wi-Fi networks block device-to-device connections. Try a phone hotspot.
- **A phone drops out mid-match:** it reconnects by itself, and its tank keeps its spot. You can also scan the code again.

## How it works

The phones and the computer find each other through PeerJS's free public server. Once connected, controls go straight from each phone to the computer. Nothing is stored online and no accounts are needed.
