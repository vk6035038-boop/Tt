# My mHealth Monitor V1 📱

An offline-first Android personal health-record and classroom Remote Patient Monitoring (RPM) demonstration app.

> **Educational/personal tracking prototype. Not a medical device.** It does not diagnose conditions, validate device accuracy, generate treatment advice, or replace professional clinical assessment.

## V1 features

- Manual blood pressure entry (systolic/diastolic)
- Pulse / heart-rate entry
- SpO₂ entry
- Temperature entry
- Weight entry and BMI calculation
- Latest-reading dashboard
- Local measurement history
- Basic health trend/history view
- Profile
- Measurement reminder time selection
- RPM teaching/demo workflow
- Offline operation
- No login, cloud backend, advertisements, or external analytics

## Tech stack

- Android application
- Java
- Android SDK 35
- Minimum Android 6.0 / API 23
- Local device storage for prototype data

## Repository structure

```text
My_mHealth_Monitor_V1/
├── app/
├── .github/
│   ├── workflows/android.yml
│   └── ISSUE_TEMPLATE/bug_report.md
├── build.gradle
├── gradle.properties
├── settings.gradle
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```

## Run locally

### Option A — Android Studio

1. Download or clone this repository.
2. Open the repository root in Android Studio.
3. Let Gradle sync.
4. Connect an Android phone with USB debugging enabled, or start an emulator.
5. Select the `app` run configuration and press **Run**.

### Option B — GitHub Actions

Every push to `main`/`master` and every pull request triggers `.github/workflows/android.yml`.

The workflow:

1. Checks out the repository.
2. Installs JDK 17.
3. Sets up Gradle 8.10.
4. Builds `assembleDebug`.
5. Uploads the generated debug APK as a workflow artifact.

To download the APK: open the GitHub repository → **Actions** → select the latest successful **Android Build** run → **Artifacts** → download `my-mhealth-monitor-debug-apk`.

## Upload to GitHub

Create a new empty GitHub repository, for example:

`my-mhealth-monitor`

Then from this project folder:

```bash
git init
git add .
git commit -m "Initial My mHealth Monitor V1"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/my-mhealth-monitor.git
git push -u origin main
```

Do **not** commit `local.properties`, APK/AAB files, passwords, API keys, keystores, or real patient data.

## Suggested repository description

> Offline-first Android mHealth and Remote Patient Monitoring demonstration app for personal health tracking and MLT/digital-health education.

## V2 roadmap

- Bluetooth Low Energy (BLE) BP and pulse-oximeter integration
- Real interactive charts
- Encrypted local database
- PIN / biometric app lock
- PDF and CSV health summary
- Medication reminders
- FHIR/HL7 interoperability demonstration
- Simulated clinician/RPM dashboard
- Role-based access
- Optional secure cloud backend

## License

MIT License. See `LICENSE`.
