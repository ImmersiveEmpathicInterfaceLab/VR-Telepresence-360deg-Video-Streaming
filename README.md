# VR-Telepresence-360deg-Video-Streaming
VR Telepresence system with Unity integrating Ricoh Theta spherical camera for 360 degree video streaming.

## Updates:
Old C# codebase with deprecated API calls to XR Interaction Toolkit. The following example doesn't compile.
```c#
using UnityEngine.XR.Interaction.Toolkit;
...
UnityEngine.XR.Interaction.Toolkit.Interactors.XRBaseController m_BaseController;
```
New C# code.
```c#
using UnityEngine.XR.Interaction.Toolkit;
...
XRBaseController m_BaseController;
```
The project originally compiled and ran with the old code. However, after an attempted port from Windows to Android, then back to Windows, the project no longer compiled.
* Initial Problem: Compiler errors due to missing namespace "Interactors" in XR Interaction Toolkit.
* Context: Old project with outdated XRI version, complicated by an attempted port from Windows to Android.
* Attempted Solutions: Uninstalling and reinstalling XRI and its dependencies, which didn't resolve the issue.
* Root Cause: The reinstallation of XRI resulted in a newer version incompatible with the existing codebase.
* Solution: Inspected current XRI version and documentation. Updated the C# scripts to adhere to modern XRI conventions. Removed unnecessary and incorrect namespace scope resolution statements. Specifically, removed the "Interactor" namespace which was no longer part of the current XRI structure.
* Outcome: Successfully compiled and ran the project after these changes.

## Contributors
* Nicholas Wile
* Umme Afifa Jinan
