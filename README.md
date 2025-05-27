# sp9820e

## APK Editing

After some investigation, I found that the error could be caused by other
factor; so in order to move on, I have to diagnose the reason by applying these
patches from your side:

* Patch 1: in-place modification

  - Download [Settings.apk](./inplace/Settings.apk?raw=true) and place it at `/priv-app`;
  - Keep original stock `Settings.odex`.

  This patch modifies the ARSC file in place as the resources file in APK isn't
  compressed by specification. The string "About phone" has been changed to
  "About PATCH" to validate the effect.

  If it does not crash the system, it could be a potential solution since you
  just want to add translations to the resources file, and I can make a tool for
  you to automate on that.
