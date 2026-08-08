## FindSight web app

[Download the complete self-contained project](sandbox:/mnt/data/findsight-web-app.zip)

The package includes the complete application, documentation, test suite, panoramic SVG scene, and reference screenshots. No external libraries, frameworks, CDNs, packages, fonts, or build tools are used.

### Source files

* [index.html](sandbox:/mnt/data/findsight-app/index.html)
* [styles.css](sandbox:/mnt/data/findsight-app/styles.css)
* [app.js](sandbox:/mnt/data/findsight-app/app.js)
* [data.js](sandbox:/mnt/data/findsight-app/data.js)
* [vision-engine.js](sandbox:/mnt/data/findsight-app/vision-engine.js)
* [demo-room.svg](sandbox:/mnt/data/findsight-app/assets/demo-room.svg)

### Documentation and tests

* [README.md](sandbox:/mnt/data/findsight-app/README.md)
* [ARCHITECTURE.md](sandbox:/mnt/data/findsight-app/ARCHITECTURE.md)
* [Test results](sandbox:/mnt/data/findsight-app/tests/TEST-RESULTS.md)
* [Dependency-free logic tests](sandbox:/mnt/data/findsight-app/tests/run-tests.js)
* [Desktop reference screenshot](sandbox:/mnt/data/findsight-app/tests/screenshots/desktop.png)
* [Mobile reference screenshot](sandbox:/mnt/data/findsight-app/tests/screenshots/mobile.png)

### Implemented functionality

The app includes a searchable 12-item panoramic room, animated room-wide rescanning, name and alias matching, color/shape/category/confidence filters, direct bounding-box highlights, optional labels and percentages, matched-only display, automatic panning, live camera support, local video scanning, and multi-frame camera panorama assembly.

Camera and video frames are processed locally. The dependency-free live detector performs HSV color segmentation, connected-region detection, approximate shape classification, and confidence filtering. The documented architecture provides a clean replacement point for adding a bundled on-device object-recognition model later.

### Verification

* 10 of 10 automated matching and vision-engine tests passed.
* The recorded browser smoke suite passed 31 of 31 checks.
* Follow-up regression checks passed after the final detector and media-lifecycle changes.
* Desktop and mobile responsive layouts were rendered at 1440 × 1200 and 390 × 844.
* No JavaScript runtime exceptions or browser error-log entries were detected.
* The ZIP archive passed an integrity check.
* A physical camera was not available in the headless test environment, so final live-camera hardware verification should be performed on the target phone or laptop.
