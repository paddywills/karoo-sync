# Karoo HR

**Your Apple Watch heart rate, on your Karoo. Your finished ride, in Apple Health — including the map.**

Karoo HR connects your Apple Watch directly to your Hammerhead Karoo. See your pulse alongside your ride data, then send the completed ride back to your Watch to save in Apple Health.

- **Use your Watch as your heart-rate sensor.** Readings appear in Karoo’s normal heart-rate field.
- **Keep Karoo as your ride recorder.** Your usual ride pages and Strava upload continue to work.
- **Export your route, heart rate and calories to Apple Health.** Supported power, cadence and speed measurements are included too. Recorded calories are imported when available; calorie estimates are still being tested in the beta.
- **Sync beside your bike, without internet.** Ride transfer uses Bluetooth; the Watch saves to Health locally.

## Get the beta

Karoo HR is currently a **limited beta**. You need two apps: Karoo HR on your Apple Watch and the Karoo HR extension on your Karoo.

- **Karoo:** [Download Karoo HR 1.4 (20)](https://github.com/paddywills/karoo-sync/releases/download/karoo-1.4-build20/KarooHR-1.4-build20.apk), then follow the installation steps below. This is the same beta installer used in the current device testing.
- **Apple Watch:** [Public TestFlight joining link](https://testflight.apple.com/join/CcbZKYg6) — **awaiting Apple beta review**. Build 1.4 (25) was submitted on 2 October 2026. Installation will become available after approval, with an initial limit of 100 testers. No individual invitation is needed once the beta opens. The Karoo download alone is not enough to use the app.

Existing invited testers can continue using their TestFlight invitation. The physically tested combination is Watch **1.4 (23)** and Karoo **1.4 (20)**. Public beta build **1.4 (25)** repackages the same Watch app code for external testing. Separate changes for resumable saving and calorie estimates remain under development and are not included in build 25. You do not need a computer, Xcode or Developer Mode for installation.

### What you need

| Device | Requirement |
| --- | --- |
| Apple Watch | watchOS 10 or later, paired with your iPhone |
| iPhone | iOS 17 or later, with TestFlight and Hammerhead Companion installed |
| Karoo | The 2024 / third-generation model, with current software |

This beta has been tested on the third-generation Karoo. Karoo 2 compatibility has not been verified. Earlier supported Apple Watch software versions have not all been physically tested.

## Install

### 1. On your Apple Watch

1. Install **TestFlight** on the iPhone paired with your Watch.
2. Once Apple approves the beta, open the [public joining link](https://testflight.apple.com/join/CcbZKYg6) on your iPhone and follow **View in TestFlight → Accept**. Existing testers can also use their invitation.
3. Find **Karoo HR** in TestFlight and tap **Install**.
4. Wait for Karoo HR to appear in your Watch’s app list, then open it.

Karoo HR is a Watch app; there is no separate Karoo HR phone app to open. See [Apple’s TestFlight installation guide](https://testflight.apple.com/) if the Watch installation is not offered.

### 2. On your Karoo

1. Turn on your Karoo and connect it to Wi-Fi. Keep your iPhone online and connected to Karoo through **Hammerhead Companion**.
2. [Download the Karoo HR installation file](https://github.com/paddywills/karoo-sync/releases/download/karoo-1.4-build20/KarooHR-1.4-build20.apk) and save it to **Files** on your iPhone.
3. In Files, press and hold the file, choose **Share**, then **Hammerhead Companion**.
4. Wait for the transfer, then tap **Install** on your Karoo.
5. Open **Karoo HR** from your Karoo’s apps/extensions list.

The `.apk` is simply the Karoo installation file. Hammerhead also supports sharing a direct download link; see its [illustrated installation guide](https://support.hammerhead.io/hc/en-us/articles/31576497036827-Companion-App-Sideloading).

## Set up once

### Connect your Watch

1. On Karoo, open **Karoo HR → Enable reception**. Allow Bluetooth access if asked.
2. On Watch, open **Karoo HR → Start HR**. Allow the requested heart-rate and workout permissions.
3. If the Watch shows a letter, tap the **matching letter** on Karoo. This selects your Watch when other riders are nearby.
4. Wait until both devices show your heart rate.
5. In Karoo’s **Sensors** settings, pair **Karoo HR (Apple Watch)** and add a **Heart Rate** field to your riding profile.

You can also add the dedicated **Karoo HR** data page to your riding profile. Use a full-page layout: it shows connection status and lets you approve a Watch’s letter without leaving your ride pages.

### Enable saving to Apple Health

1. In Karoo HR, open **More → Set up ride sync** and grant access to saved ride files.
2. Turn off Hammerhead Companion’s **Apple Health sync** if you will use Karoo HR to import these rides. Also avoid exporting the same workout to Health through another app. Your Karoo-to-Strava connection can stay enabled; check Strava’s separate Health export setting if you use it.
3. At your first import, allow Karoo HR to **write workouts, workout routes and the requested ride measurements** to Health.
4. Allow **reading Workouts** too. This helps the app recognise an existing ride and recover a save without creating another workout. Live heart-rate sharing separately needs permission to read **Heart Rate**.

Newer beta builds also request **Resting Energy** access for calorie calculations. These permissions have different jobs; enabling only “write” permissions is not sufficient for all features.

## Go for a ride

### Before you set off

1. Wear and unlock your Watch. Keep it close to your Karoo.
2. Check Karoo HR reception is enabled, then tap **Start HR** on your Watch.
3. Confirm a heart-rate reading appears on your Karoo.
4. Start recording your ride on Karoo as usual.

### While riding

You can lower your wrist or return to the Watch face while sharing heart rate. Use Karoo’s normal ride screens; leaving the Karoo HR screen does not turn reception off.

The Watch runs a temporary workout to obtain frequent readings. It discards that workout when sharing stops; your completed Karoo ride is the workout you import later. Apple may still record individual heart-rate or Activity samples during sharing.

### At the finish

**Finish and save the ride on Karoo first.**

1. On Watch, choose **Sync ride** when the ride-ended reminder appears. If you are still sharing heart rate, tap **End HR + sync ride**.
2. Keep both devices nearby and **stay in the Watch app during the Bluetooth transfer**. Approve a matching letter or system Bluetooth pairing request if prompted.
3. Wait for **Saved to Apple Health**. Saving a long ride can take several minutes; the final Health save does not have a reliable countdown.
4. After your Watch and iPhone sync, check the workout in Apple Health/Fitness on your iPhone, including its route map.

**Watch builds 23 and 25:** keep Karoo HR open through the Health-saving step as well. Do not restart or repeatedly retry while it is saving.

When Karoo confirms a ride has ended, the Watch stops heart-rate sharing and offers the reminder. A pause or lost connection does not count as a finished ride. If the reminder is missed, end sharing yourself. Karoo reception stays enabled for next time; **Disable reception** turns it off.

### Save an earlier ride

On Karoo HR, open **More → Earlier rides** and select the ride. On Watch, open **More → Earlier rides** and follow the selection/import instructions. You can page through three rides at a time.

Do not import a ride already saved through HealthFit or another app. Karoo HR checks for duplicates, but those checks depend on Health permissions and the information available from the other app.

## What reaches Apple Health?

Karoo HR saves one cycling workout using the completed Karoo recording.

| Data | What to expect |
| --- | --- |
| Ride time and distance | Recorded start/end, distance and pause information |
| Route map | The GPS points recorded by Karoo; missing GPS sections cannot be recreated |
| Heart rate | Readings recorded in the ride |
| Speed, cadence and power | Included when present in the recording; cadence/power need a suitable sensor or source |
| Calories | Recorded calories when available; missing calories may show as zero in the current beta |

### Coming in the next beta

Resuming an interrupted Health save and estimated **active and total calories** are implemented but still awaiting release/real-device verification. They are not promised features of the currently installed beta.

In that update, once transfer finishes, the ride is stored on the Watch and you can leave the app during Health saving. If interrupted, reopen it and choose **Resume Health save**. Calorie estimates need sufficiently complete power readings and resting-energy information from Health; the app will label estimates rather than present them as measured values.

## Common questions

**Do I need internet at the end of a ride?**

No. Karoo HR transfers the saved ride directly over Bluetooth and writes to Health on your Watch. You do not have to wait for Karoo’s cloud upload. Installation and updates need an internet connection.

**Will this use more battery?**

In my testing, Apple Watch battery use has been similar to recording a normal cycling workout. Plan on around **two hours of riding**, although this will vary with your Watch model, battery health and starting charge. This is a planning estimate from personal testing, not a guaranteed runtime or a limit on every Watch.

**The Watch says “Searching for Karoo”.**

Bring the devices together, check Karoo HR reception is enabled and Bluetooth is on, then approve the Watch’s letter if shown. After restarting Karoo, enable reception again. Confirm heart rate has returned before continuing.

**The sensor name still says “Apple Watch via WatchKaroo…”.**

That is an older name for this extension. Check the installed Karoo HR version; Karoo may have retained the name of a previously paired sensor.

**It is waiting for a ride.**

Check that you finished and saved the ride on Karoo and granted file access. An internet upload is not required. A discarded ride cannot be imported.

**It is still saving.**

Read the smaller progress text. Health may take several minutes, particularly for a long GPS track. While a save is in progress, avoid restarting the app or starting another import. If an error appears, retain its exact wording when reporting it.

**Is my route sent through another service?**

Karoo HR’s transfer uses Bluetooth between your Karoo and Watch. It does not require a route-upload service or a separate cloud account. Your existing Hammerhead, Strava and Apple Health account settings continue to govern their own syncing.

## Updates and feedback

Update the Watch app through **TestFlight**. Download Karoo updates from [GitHub Releases](https://github.com/paddywills/karoo-sync/releases) and install over the existing app. Follow each beta’s notes about which versions belong together.

For help, [report an issue](https://github.com/paddywills/karoo-sync/issues) or send feedback through TestFlight. Include both app versions, the exact message, and whether you were sharing heart rate, transferring a ride or saving to Health. **Help & version** on Watch and the Karoo app’s version display identify the installed builds. Avoid posting private route maps or Health data publicly.

## Beta disclaimer

Karoo HR is independent beta software and is not affiliated with or endorsed by Apple, Hammerhead or SRAM. It is provided “as is”, without warranty. Install and use it at your own risk. To the extent permitted by applicable law, the developer accepts no liability for damage to your Apple Watch, Karoo or other equipment, loss or corruption of ride or Health data, or other loss arising from its use. Nothing in this notice excludes liability that cannot legally be excluded.

Read the [beta privacy information](https://github.com/paddywills/karoo-sync/blob/main/PRIVACY.md) for data handling and contact details.

## About this repository

This repository provides the rider guide and downloadable Karoo beta. Installation does not require programming. Third-party software acknowledgements are included with the [release downloads](https://github.com/paddywills/karoo-sync/releases).
