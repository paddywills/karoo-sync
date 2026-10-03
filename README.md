# Karoo HR

**Apple Watch heart rate on your Karoo. Your finished ride in Apple Health, including the route.**

- See live heart rate in Karoo’s normal ride fields and record it with your ride.
- Save completed rides to Apple Health with GPS routes, heart rate, distance, and recorded calories, speed, cadence and power where available.
- Transfer directly over Bluetooth, without internet or waiting for Karoo’s cloud upload. Your usual Strava sync can stay enabled.

## What’s new — Watch 1.4 (28)

- **Clearer finish:** a successful import no longer leaves “Import paused” on the home screen.
- **Consistent navigation:** use the top-left arrow to go back. During Health saving, return home and use **View progress**.
- **Updates and feedback:** release notes appear once after an update and remain under **More → What’s new**. **More → Report an issue** gives feedback options.
- **Name corrected:** app metadata now uses **Karoo HR**. Apple Health may retain the old **WatchKarooBLE** source name on existing records.

Since the first public build (25): Health saves can resume on Watch, missing calories can be estimated from recorded power, and resting energy is read without adding duplicate resting calories. See the saving and calorie notes below.

## Get the beta

You need both apps. No computer, Xcode or Developer Mode is required.

| Device | Install |
| --- | --- |
| Apple Watch — watchOS 10+, paired with an iPhone on iOS 17+ | [Join through TestFlight](https://testflight.apple.com/join/CcbZKYg6) |
| Karoo — 2024 / third-generation model | [Download Karoo HR 1.4 (20)](https://github.com/paddywills/karoo-sync/releases/download/karoo-1.4-build20/KarooHR-1.4-build20.apk) |

**Available now (3 October):** Watch 1.4 (28) is approved and available through the public TestFlight link and existing invitations. Check your build under **More → Help & version**. The public link initially allows 100 testers.

These update notes describe Watch 28 with Karoo 20. Karoo 2 and every supported Watch/OS combination have not been verified.

### Install

1. **Watch:** install TestFlight on your iPhone, open the joining link, accept the beta and install Karoo HR on your Watch. There is no separate Karoo HR phone app.
2. **Karoo:** download the APK above to **Files** on your iPhone. Press and hold it → **Share → Hammerhead Companion**, then tap **Install** on Karoo. Keep both devices online and connected through Companion. [Illustrated installation guide](https://support.hammerhead.io/hc/en-us/articles/31576497036827-Companion-App-Sideloading).

## Set up once

1. On Karoo, open **Karoo HR → Enable reception** and allow Bluetooth access.
2. On Watch, tap **Start HR** and grant the requested heart-rate and workout permissions. If a letter appears, approve the **matching letter** on Karoo.
3. When heart rate appears, pair **Karoo HR (Apple Watch)** in Karoo’s **Sensors** settings and add a Heart Rate field to your riding profile.
4. Optionally add the full-page **Karoo HR** data field to your ride profile for connection status and letter approval while riding.
5. In the Karoo app, open **More → Set up ride sync** and allow access to saved rides.
6. Turn off Hammerhead’s Apple Health export and any other app’s export of the same rides to avoid duplicates. Strava ride uploads can stay on; check its separate Health export setting.

At your first import, allow Health **write access** for workouts, routes and ride measurements, plus **read access to Workouts** for duplicate detection and save recovery, and **Resting Energy** for the calorie split. Live sharing also needs **Heart Rate read access**.

## Ride and save

**Before riding:** enable Karoo reception, tap **Start HR** on Watch, confirm heart rate on Karoo, then start recording your ride normally.

**During riding:** lower your wrist or return to the Watch face normally. You can leave the Karoo HR screen too. The Watch uses a temporary workout for frequent readings and discards it when sharing ends; Apple may still retain individual heart-rate or Activity samples.

**At the finish:**

1. **Finish and save the ride on Karoo first.**
2. On Watch, choose **Sync ride** from the reminder, or **End HR + sync ride** if still sharing.
3. Keep both devices nearby and **stay in the Watch app during Bluetooth transfer**. Approve pairing if asked.
4. **Build 28:** once **Saving to Apple Health** starts, you can return to the Watch face. If interrupted, reopen Karoo HR → **Resume Health save**. The ride is stored on Watch; Karoo and internet are no longer needed. **Build 25: keep the app open until saved.** Saving can take several minutes; do not restart or retry while Health is still working.
5. When **Saved to Health** appears, use the **top-left arrow** to return home. After Watch/iPhone syncing, check the workout and route in Apple Health/Fitness.

The reminder stops HR sharing when Karoo confirms the ride has ended. A pause or disconnection does not mean the ride has finished. If you miss the reminder, end sharing yourself. Karoo reception stays enabled for next time.

## If something goes wrong

- **Watch disconnects or runs out of battery:** Karoo continues recording. Watch heart-rate readings are missing until reconnection, but a ride saved on Karoo can still be imported into Health later.
- **Karoo needs restarting:** use Karoo’s **Resume Ride** feature if offered, then reopen Karoo HR, enable reception and re-pair the Watch. This recovery worked during a real ride after a Karoo GPS problem; missing readings or GPS points cannot be recreated.
- **Import later:** choose **More → Earlier rides** on Karoo to select a saved ride, then on Watch to import it. Historical imports are not limited to the latest ride. Avoid importing rides already saved through HealthFit or another app.
- **Searching or waiting:** bring the devices together, check reception and Bluetooth, approve the matching letter, and confirm the ride is saved with file access granted. Internet is not required.

## Battery and current limits

In my testing, Watch battery use is similar to recording a normal cycling workout. **Plan on around two hours**, depending on Watch model, battery health and starting charge; this is not a guaranteed runtime.

**Calories:** recorded active calories are used when available. Otherwise, sufficiently complete recorded power can provide an estimate. Karoo HR shows active calories and a total estimate including resting energy during active riding. It saves active calories to Health and keeps the total estimate in workout metadata. **Fitness may display the same figure for active and total calories.** Karoo HR never adds derived resting-energy entries.

Older build 25 requires the Watch app open throughout transfer and Health saving and can show zero calories when the ride has none recorded. Update to 28 for resumable saving and estimates.

## Updates and help

Update Watch through TestFlight and Karoo through [GitHub Releases](https://github.com/paddywills/karoo-sync/releases), following the version-pairing notes. Install Karoo updates over the existing app.

[Report an issue](https://github.com/paddywills/karoo-sync/issues/new?template=report.yml) for problems or support questions. Sign in to GitHub to use the short form. Include both app versions if known; your Watch version is under **More → Help & version**. Reports are public: do not include email addresses, private routes or Health data. TestFlight and email feedback are reviewed manually.

## Beta disclaimer

Karoo HR is independent beta software and is not affiliated with or endorsed by Apple, Hammerhead or SRAM. It is provided “as is”, without warranty. Install and use it at your own risk. To the extent permitted by applicable law, the developer accepts no liability for damage to your Apple Watch, Karoo or other equipment, loss or corruption of ride or Health data, or other loss arising from its use. Nothing in this notice excludes liability that cannot legally be excluded.

[Privacy and contact details](https://github.com/paddywills/karoo-sync/blob/main/PRIVACY.md) · [Third-party acknowledgements](https://github.com/paddywills/karoo-sync/releases)
