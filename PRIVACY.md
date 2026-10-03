# Karoo HR beta — privacy information

Updated 3 October 2026.

Karoo HR connects your Apple Watch and Hammerhead Karoo to share live heart rate and import completed cycling rides into Apple Health. It does not require a Karoo HR account.

## Heart rate and ride data

- With your permission, the Watch reads heart rate and sends it directly to your approved Karoo over Bluetooth. Karoo records the ride using its own recording system.
- When you request an import, the Karoo app reads your saved ride file and transfers its route and supported measurements to your approved Watch over encrypted Bluetooth.
- The Watch stores downloaded ride data locally to support importing and interrupted transfers. It also stores identifiers used to recognise previously imported rides. Local data may remain until replaced or the app is removed.
- With your permission, the Watch writes the completed cycling workout, route and recorded measurements to Apple Health. It reads Workouts to help check for duplicates and recover interrupted saves. Newer beta builds may request Resting Energy for calorie calculations; follow the explanation in your installed build.
- Karoo HR's live heart-rate session is discarded when sharing stops. Apple may still record individual heart-rate or Activity samples during the session.

Karoo HR does not upload your heart-rate readings or ride route to a developer-operated server. It does not use Health data for advertising or sell it. Your existing Hammerhead, Strava and Apple Health settings govern their separate syncing and storage.

## Diagnostics and feedback

The Watch keeps a limited local connection/import event log for troubleshooting. It is designed to describe app events rather than record heart-rate values or route coordinates.

Apple's TestFlight service handles beta distribution and may provide the developer with crash reports, usage information and feedback under Apple's terms. If you submit TestFlight feedback or a GitHub issue, we receive the information you choose to send. GitHub issues are public: do not include private routes, Health records, passwords or pairing codes.

## Your choices

You can stop sharing in the app, revoke its Health permissions in Apple's Health settings, or uninstall it. Removing Karoo HR does not automatically delete workouts already saved in Apple Health or the original rides on Karoo. Manage those records in the respective apps.

## Contact

For support, [Report an issue](https://github.com/paddywills/karoo-sync/issues/new?template=report.yml) on GitHub. Reports are public: do not include email addresses, private Health data or routes. For private or privacy-related questions, use **Send Beta Feedback** in TestFlight. TestFlight and email feedback are reviewed manually.
