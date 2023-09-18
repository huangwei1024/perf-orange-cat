# perf-orange-cat
## Client Performance Testing Platform

![微信图片_20230624120931](https://github.com/1033866383/perf-orange-cat/assets/56209295/ce1d47eb-01bb-41d8-88d4-e07828aea825)

**Demo URL:** [http://112.126.75.188/](http://112.126.75.188/)

**Source Code:** [https://github.com/1033866383/perf-orange-cat](https://github.com/1033866383/perf-orange-cat)

**Pre-built Binaries:** [https://github.com/1033866383/perf-orange-cat/releases](https://github.com/1033866383/perf-orange-cat/releases)

**Installation:** `pip install -U performancetest`

**Startup:** `python -m performancetest.web.main`

Once started, access: [http://localhost/](http://localhost/) to begin Android/IOS performance testing.

**API Documentation:** [http://localhost/redoc/](http://localhost/redoc/)

**System Requirements:** Python 3.9+; if you encounter Python version issues, consider using [pyenv](https://github.com/pyenv/pyenv) for environment isolation.

Please note the open-source license for this project.

**Planned Features:**
- Adding support for performance testing on Windows, macOS, Linux, and other PC platforms.
- Adding the ability to compare performance testing tasks.
- Introducing label functionality for selecting performance testing scenarios.
- Development Branch: dev

## Introduction
- A replacement for client performance testing tools like perfdog.
- Supports performance data testing for applications on Android and IOS platforms, including games and video apps.
- Supports various performance metrics, including CPU, memory, FPS, GPU, temperature, battery, and network traffic.
- Provides detailed CPU performance data, including Top version CPU, Procstat version app CPU, and Procstat version system CPU.
- FPS metrics include jank and big jank indicators.
- Provides accurate performance data consistent with perfdog.
- Can record device screens in real-time and supports clicking to navigate to corresponding scenes.
- Supports use on a local network, allowing performance testing across the entire local network.
- Provides executable files for easy deployment and detailed API documentation.

## Directory Overview
- `performancetest/web/test_result/`: Contains frontend pages and test results.
- `log.log`: Project runtime logs.
- `task.sqlite`: SQLite database containing basic details of each task, also the unique DAO object.

## New Features as of August 10, 2023
**New Features for Android Multi-type CPU and Network Traffic:**

![微信图片_20230810000255](https://github.com/1033866383/perf-orange-cat/assets/56209295/da98d4bc-9784-4e75-8a3c-a8b9e94d02bd)
![微信图片_20230810000359](https://github.com/1033866383/perf-orange-cat/assets/56209295/bb88db4f-2013-4937-b1f2-cd1510adc9d1)

## User Guide
We recommend following these steps to install and start Perf-Orange-Cat:

1. Install Perf-Orange-Cat: `pip install -U performancetest`

![image](https://github.com/1033866383/perf-orange-cat/assets/56209295/b0d566fd-cf1e-4fd2-85eb-21f1e3762619)

2. Start Perf-Orange-Cat: `python -m performancetest.web.main`, and the project will start running.

![image](https://github.com/1033866383/perf-orange-cat/assets/56209295/38f32ab0-a967-4cc4-963a-e57320e9da11)

3. Access [http://localhost/](http://localhost/).

Default page:

![image](https://github.com/1033866383/perf-orange-cat/assets/56209295/6b7d1e37-d488-4dda-b8b3-4e89890edf3f)

4. Click the red button at the top to create a new performance testing task. It will automatically detect devices connected to your computer running Android/Ios.
   **Important points to note:**
   - For Android devices, you need to enable developer mode, and some devices may require selecting file transfer mode.
   - For IOS devices with IOS 16 or above, you need to enable developer mode in the privacy and security settings, as shown below. If you don't see this option on your device, you can use iCareFone to enable developer mode. For IOS devices with versions below 16, you need to connect to Xcode to enable developer options. In practice, connecting your device and selecting it should be enough. IOS 16 can also use this operation to display developer options. If you are connecting an IOS device to a Windows computer, remember to install iTunes.

![微信图片_20230625011358](https://github.com/1033866383/perf-orange-cat/assets/56209295/78d05b9e-7370-486c-b8cd-3ad0afaf5744)

Here's an example of Android emulators and my iPhone that were detected after enabling developer options on the devices:

![image](https://github.com/1033866383/perf-orange-cat/assets/56209295/78634fab-7225-4226-bca1-fdd4884abaec)

5. After selecting the device, scroll down to select the app, and it will automatically display the version number. Then click "Create Task."

![image](https://github.com/1033866383/perf-orange-cat/assets/56209295/ffbb3ef7-0623-44fd-97a2-f9e17135173b)

6. After creating the task, the page will refresh automatically and start performance testing. If you enable the real-time screen display button, the images at the top will show the real-time screen of your mobile device. On the left, there's a time button that represents the task's start time and name. For IOS, the FPS is displayed, and jank and big jank are not calculated. For Android, these metrics are calculated, following the same method as perfdog.

![微信图片_20230810000513](https://github.com/1033866383/perf-orange-cat/assets/56209295/6021212f-d68c-431c-b4a0-50ec464f951e)
![微信图片_20230810000547](https://github.com/1033866383/perf-orange-cat/assets/56209295/b7a33e0e-7a9f-42d5-9dd7-571684ba428d)

7. Finally, click "Stop Task" to stop the task. After stopping the task, you can delete it. Be cautious when deleting tasks, as it will physically delete all task data.

![image](https://github.com/1033866383/perf-orange-cat/assets/56209295/a2f65fca-2256-4fac-a1a3-79fb8899ea0f)
