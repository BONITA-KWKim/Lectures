# Android reference pages
android.com  
developer.android.com(d.android.com)  
source.android.com  
androidxref.com  

<hr/>

cf) IPC, ITC architecture
-> binder and service

<hr/>

# Android Studio
- android studio
  * JDK
  * IDE
  
- SDK
  * Tools(performance monitoring tool, ADB, emulator tool, etc.)
  * Android API set(need to check API level for android version)
  
- setting files(copy and paste -> if you don't want it, setting at configure>project default>project structure)
  * .android
  * .AndroidStudio3.0
  * .gradle

<hr/>

cf) why using JNI + NDK: 1) performance, 2) reusing c++ code
  --> if you used JNI+NDK, security should be implemented.
  
cf) you need to understand linux kernel

<hr/>

# Android porting example
girhub repo: https://github.com/edu-cafe/and-porting

# Android menifest
- Android application statement.
- Android platform creates objects by menifest. user is not permitted to create objects in android.
- If you want to add activity or service etc., you will add statement in menifest. (request create my application to android platform)

cf) IOC: inversion of control --> You can find in d.android.com

# Android activity life cycle (important)

# Service
- Parallel task
- android manages to our tasks. So, our thread is barely create threads. Custom threads do not be managed.
- When starting service, service process would be created and that information is written in menifest file.
- startService(): batch task. Activity calling service do not or can not call function in service.
- bindService(): Activity calling service do or can call function in service. Therefore, activity can control service.
- You can call system services by using manager(e.g. AlarmManager am = (AlarmManager) getSystemService(ALARM_SERVICE);)
- 
<hr/>

- IPC: Kernel level(binder).
- AIDL: Custom binder. Implemented functions are accessed by external environment, that is process, activity and so on.
- Messenger: If you need simple communication, you will implement messenger alternative to AIDL.
- Data object for communicating between processes have to serialize. Parse class will give you that functions.

cf) intent class: it created based on binder.

# Content provider

# Broadcast Receiver
- Event receiver.
- Kernel emits some event and application receives that with BR.
- BR can use IPC alternative to binder. Application emits BR signal and other application receive that BR signal.


# Context
- very important......


# Source Tree
- VM: art/, dalvic/
- HAL: Hardware/, device/
- HW: bionic/, bootable/, cts/ 
- External library(open source): external/
- Android Framework: frameworks
- Compiler tools: prebuildts/
- basic application: packages/
- booting: /system/core/init/init.cpp


