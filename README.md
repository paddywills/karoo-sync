# Karoo HR

**Use your Apple Watch as a heart-rate sensor for Karoo, and import saved Karoo rides into Apple Health. Use either function independently.**

Karoo records the ride. Your Watch sends live heart rate directly over Bluetooth, without a chest strap or bridge device. Afterwards, it can import a saved ride into Health with its **route, heart rate, distance, calories and available speed, cadence and power**. Older rides and rides recorded with another sensor can be imported too.

Ride transfer and Health saving need **no internet or Karoo cloud upload**. Your usual Karoo-to-Strava sync can stay enabled.

## What’s new — Watch 1.4 (29) / Karoo 1.4 (21)

**Recovery update — in internal testing, 4 October 2026.** Both builds are installed on the test devices, with Watch 29 distributed through internal TestFlight. Automatic recovery requires both updates. Reboot and out-of-range testing is still pending.

**Joining the public beta?** The downloads below still provide Watch **1.4 (28)** and Karoo **1.4 (20)**. They do not yet include automatic recovery.

- After a lost HR connection, Watch keeps measuring and tries to reconnect to the same Karoo for **up to five minutes**.
- After restarting Karoo, **resume the ride**. Reception restarts if it was previously enabled, and the remembered Watch can reconnect without selecting its letter again.
- If recovery times out, Watch alerts you, stops and discards its temporary session, and shows **Reconnect**.
- **Disable reception** is an intentional stop, not a reason to reconnect. If Watch is already out of range, stop HR on Watch yourself or let its recovery window expire.

The public Watch **1.4 (28)** improves save completion, top-left back navigation and app naming. Since the first public build, Health saves can resume on Watch and missing calories can be estimated without adding duplicate resting energy.

## Install the public beta

You need both apps for either function. No computer, Xcode or Developer Mode is required.

| Device | Download |
| --- | --- |
| Apple Watch — watchOS 10+, paired with an iPhone on iOS 17+ | [Join through TestFlight](https://testflight.apple.com/join/CcbZKYg6) — public Watch 1.4 (28) |
| Karoo — 2024 / third-generation model | [Download Karoo HR 1.4 (20)](https://github.com/paddywills/karoo-sync/releases/download/karoo-1.4-build20/KarooHR-1.4-build20.apk) |

1. **Watch:** install TestFlight on your iPhone, open the joining link, accept the beta and install Karoo HR on Watch. There is no separate Karoo HR phone app.
2. **Karoo:** download the APK to **Files** on your iPhone. Press and hold it → **Share → Hammerhead Companion**, then tap **Install** on Karoo. Installation needs both devices online and connected through Companion. [Illustrated installation guide](https://support.hammerhead.io/hc/en-us/articles/31576497036827-Companion-App-Sideloading).

Install updates over the existing apps. Watch updates come through TestFlight; Karoo updates are on [GitHub Releases](https://github.com/paddywills/karoo-sync/releases). Check Watch under **More → Help & version** and Karoo under **More**. Karoo 2 and every Watch/OS combination have not been verified.

## Set up the functions you want

First open **Karoo HR → Enable reception** on Karoo and allow Bluetooth access.

### Live heart rate

1. Tap **Start HR** on Watch and grant Heart Rate read access and the requested workout permission.
2. Approve the **matching letter** on Karoo. With Watch 29 / Karoo 21, also complete Bluetooth pairing if asked: keep Karoo HR open on Karoo to enter the code shown on Watch. This remembers the approved Watch for later reconnections.
3. Once heart rate appears, pair **Karoo HR (Apple Watch)** in Karoo’s **Sensors** settings and add a Heart Rate field to your riding profile.
4. Optionally add the full-page **Karoo HR** data field to your ride profile for status and letter approval while riding. This is a profile data page, not a Karoo system tab.

Only the approved Watch supplies heart rate. Another nearby Watch still needs your letter approval. In Watch 29 / Karoo 21, automatic recovery uses the stored Bluetooth bond, not the displayed name or letter. If you replace your Karoo, Watch 29 offers **More → Help & version → Pair another Karoo** while HR is stopped.

### Apple Health ride import

1. On Karoo, open **More → Set up ride sync** and allow access to saved rides.
2. Disable Hammerhead’s Apple Health export and any other app’s Health export of the same rides to avoid duplicates. Strava uploads can stay enabled; check Strava’s separate Health export setting.
3. At the first import, allow Health **write access** for workouts, routes and ride measurements. Allow **read access to Workouts** for duplicate detection and save recovery, and **Resting Energy** for the calorie split. Approve the matching letter and Bluetooth pairing if asked.

You do not need to start HR or configure Karoo’s heart-rate sensor to import saved rides. Likewise, you can use live HR without setting up ride imports.

## During a ride

**Start:** enable reception on Karoo, tap **Start HR** on Watch, confirm heart rate on Karoo, then record your ride normally.

**Ride:** lower your wrist or return to the Watch face normally. You can leave the Karoo HR screen too. Watch uses a temporary workout for frequent readings and discards it when sharing ends. Apple may still retain individual heart-rate or Activity samples.

**Finish:** finish and save the ride on Karoo first. When Karoo confirms it has ended, Watch stops HR and offers **Sync ride** or **Later**. If the reminder does not arrive, choose **End HR + sync ride** yourself. A pause or lost connection never counts as a finished ride. Reception remains enabled for next time unless you disable it.

### Recovering a lost HR connection

**Watch 29 / Karoo 21 (internal testing):** leave Watch running while it shows **Reconnecting…**. It keeps measuring for up to five minutes; you can lower your wrist normally. Bring the devices together or, after a Karoo reboot, use **Resume Ride** if offered. Reception and the remembered Watch should reconnect automatically. Check that fresh HR returns on Karoo.

If it takes longer, Watch stops HR, alerts you and offers **Reconnect** on its home screen. Resume the ride on Karoo first, then tap it. If reception did not restart, open Karoo HR and **Enable reception**. To import instead, choose **More → Sync ride** on Watch.

**Watch 28 / Karoo 20 (public beta):** after a restart, reopen Karoo HR, enable reception, and use **More → Start HR** on Watch. Approve the matching letter again if asked.

Karoo continues recording if Watch disconnects or its battery runs out. Missing HR readings are not backfilled, but any ride saved on Karoo can still be imported into Health later. Recovery cannot recreate missing measurements or recover an unsaved ride. If you disable reception while Watch is out of range, it cannot receive that stop immediately; use **Stop HR** on the reconnecting Watch to end it straight away.

## Import a saved ride into Apple Health

1. **Finish and save the ride on Karoo first.** No cloud upload is needed.
2. **After Watch HR sharing:** choose **Sync ride** from the reminder, or **End HR + sync ride** if still sharing.
3. **For any other saved ride:** choose **More → Earlier rides** on Karoo and select it, then **More → Earlier rides** on Watch. This also works for your most recent ride, with or without recorded heart rate.
4. Keep the devices nearby and **stay in the Watch app during Bluetooth transfer**. Approve pairing if asked.
5. Once **Saving to Apple Health** starts, you can return to the Watch face. Karoo and internet are no longer needed. If interrupted, reopen the app → **Resume Health save**. Saving can take several minutes; do not restart or retry while Health is working.
6. Wait for **Saved to Health**, then use the top-left arrow to return home. After Watch/iPhone syncing, check the workout and route in Apple Health/Fitness.

Avoid importing a ride already saved by HealthFit or another app. Available measurements depend on what Karoo recorded.

### From riding to saved in Health

These Watch screenshots show both functions used together for one ride: sharing heart rate, transferring the saved ride and finishing the Health save. If you only use ride transfer, start with **More → Earlier rides** and follow the transfer and saving stages shown in screenshots 3–6. Read left to right, then continue on the next row. The readings, calories and elapsed times are examples from this ride.

| 1. Live heart rate | 2. Ready to sync | 3. Bluetooth transfer |
| :---: | :---: | :---: |
| <img src="docs/screenshots/01-live-heart-rate.jpg" alt="Karoo HR showing 103 bpm and End HR + sync ride" width="200"> | <img src="docs/screenshots/02-heart-rate-stopped.jpg" alt="Heart rate stopped, with Sync ride and Later buttons" width="200"> | <img src="docs/screenshots/03-transferring-ride.jpg" alt="Syncing ride: receiving ride at 12 percent, with instructions to stay here and keep Karoo nearby" width="200"> |
| Finish and save on Karoo first, then tap **End HR + sync ride**. | When sharing has stopped, tap **Sync ride** to import the saved ride. | **Stay in the Watch app** and keep Karoo nearby until transfer finishes. |

| 4. Saving measurements | 5. Final Health save | 6. Saved to Health |
| :---: | :---: | :---: |
| <img src="docs/screenshots/04-saving-measurements.jpg" alt="Saving measurements: 3250 of 4233 records, with Resume Health save instructions" width="200"> | <img src="docs/screenshots/05-final-health-save.jpg" alt="Final Health save waiting for confirmation, with no time estimate available" width="200"> | <img src="docs/screenshots/06-saved-to-health.jpg" alt="Saved to Health: 346 active kcal, 477 total kcal estimated from power, route included" width="200"> |
| You can leave the app during Health saving. If interrupted, reopen it and choose **Resume Health save**. | Wait for Health confirmation; this stage has no time estimate. | The Watch confirms the save and shows the calorie summary and whether the route is included. Check Health/Fitness after Watch and iPhone syncing. |

### Recorded on Karoo, saved to Apple Health

These screenshots illustrate the two functions: the Karoo ride data shows the recorded heart-rate trace alongside the ride measurements. That recording remains useful even if you do not use Apple Health. After importing, Apple Fitness displays the workout saved to Apple Health, including its route, distance, workout and elapsed times, calories, average power, cadence and speed.

| Heart rate recorded with the ride | Imported workout in Apple Fitness |
| :---: | :---: |
| <img src="docs/screenshots/07-karoo-recorded-heart-rate.jpg" alt="Karoo ride data showing a heart-rate graph and lap statistics for distance, time, elevation, speed, heart rate and cadence" width="281"> | <img src="docs/screenshots/08-apple-fitness-workout.jpg" alt="Apple Fitness showing an imported 22.20 km outdoor cycle with route map, times, calories, average power, cadence and speed" width="281"> |
| The heart-rate graph confirms that readings were recorded in the Karoo ride. The selected lap also shows average, maximum and minimum heart rate. | The route and ride measurements appear in Fitness after Health syncing. Available measurements depend on what Karoo recorded. |

The Fitness summary does not show every stored measurement; check Apple Health for the imported heart-rate data. In this example, Fitness displays the same active and total calories, as described below. Apple Health may retain the older **WatchKarooBLE** source name on existing records.

## Battery and calories

In my testing, Watch battery use is similar to recording a normal cycling workout. **Plan on around two hours**, depending on model, battery health and starting charge; this is not a guaranteed runtime. With Watch 29 / Karoo 21, the recovery window continues HR measurement for at most five minutes after a lost connection, then stops it if reconnection fails.

Recorded active calories are used when available. Otherwise, sufficiently complete recorded power can provide an estimate. Karoo HR shows active calories and a total estimate including resting energy during active riding. It saves active calories to Health and keeps the total estimate in workout metadata. **Fitness may display the same figure for active and total calories.** Karoo HR never adds derived resting-energy entries.

## Help and feedback

For connection trouble, bring the devices together, check Karoo reception and approve pairing if asked. For an import, also check that the ride is saved and file access is granted. Internet is not required. Release notes are available on Watch under **More → What’s new** and appear once after an update.

[Report an issue](https://github.com/paddywills/karoo-sync/issues/new?template=report.yml) using the short GitHub form; GitHub sign-in is required. Include both app versions and what happened. Watch also offers **More → Report an issue**. Reports are public: leave out email addresses, private routes and Health data. TestFlight and email feedback are reviewed manually.

## Beta disclaimer

Karoo HR is independent beta software and is not affiliated with or endorsed by Apple, Hammerhead or SRAM. It is provided “as is”, without warranty. Install and use it at your own risk. To the extent permitted by applicable law, the developer accepts no liability for damage to your Apple Watch, Karoo or other equipment, loss or corruption of ride or Health data, or other loss arising from its use. Nothing in this notice excludes liability that cannot legally be excluded.

[Privacy and contact details](https://github.com/paddywills/karoo-sync/blob/main/PRIVACY.md) · [Third-party acknowledgements](https://github.com/paddywills/karoo-sync/releases)
