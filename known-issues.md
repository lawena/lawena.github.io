---
layout: page
title: Known Issues
---

<div class="message">
  This page is present in the <a href="{{ site.github.repo }}/wiki">Wiki</a>. Check it out for more in-depth articles.
</div>

## About this page

This is a list of **known limitations and problems** while using Lawena Recording Tool. All of them come with a workaround of varying complexity. It is divided in the following categories:

* _Avoidable_: As long as you're aware of this you should not have any problems.
* _Uncertain solution_: Depends on your particular setup. Sometimes it's a threading issue, or the demo is just too taxing for the engine and/or your system.
* _Manual fix required_: Unfortunately the tool cannot fix these for you, should they occur.
* _Mostly fixed_: Issues almost leaving this page! They could still be triggered in certain situations though.

### Avoidable

* Selecting your own files ending in ``*.cfg`` to load into TF2 can cause loss of recording quality and lawena's keybindings due to setting conflicts. See [#10](https://github.com/iabarca/lawena-recording-tool/issues/10)
* Choosing a movie/recording folder with special characters like brackets, exclamation points or accents might confuse Source Recorder and Lawena itself and not save any frames. Use simpler path names. See [#63](https://github.com/iabarca/lawena-recording-tool/issues/63)
* Demos don't work if they have spaces in their names and you load them with demoui. This is also true for folder names. Load them via console using ``playdemo`` instead. See [#58](https://github.com/iabarca/lawena-recording-tool/issues/58)
* Lawena always saves your settings, however if you make a change to an editable input box and close the program immediately, it might not get saved due to the control never losing cursor focus (and therefore saving changes).
* Classic Windows 7 interface (not Aero) does not work well with Lawena's current GUI. Use Aero instead. Sorry for the inconvenience. See [#34](https://github.com/iabarca/lawena-recording-tool/issues/34)

### Uncertain solution

* The maxquality graphics config used might cause more crashes than normal when playing demos. Try ``mat_queue_mode 1`` first and then try to workaround it using another graphics config for the game. See [#52](https://github.com/iabarca/lawena-recording-tool/issues/52)

### Manual fix required

* If you have your own class configs with ``bind`` command in them, you can lose some of the lawena's own keybindings, because class configs get recorded into the ``.dem`` files. Just check out ``recbindings.cfg`` and execute the equivalent console command.
* Some keybindings might be missing, for instance the original "P" bind might be lost. Rebind using ``bind P startrecording`` or just type ``startrecording`` into the console. Make sure you're not playing a demo that rebinds some keys used by Lawena and if they do, edit ``recbindings.cfg`` inside lawena ``cfg`` folder accordingly to solve it.

### Mostly fixed

* Custom HUDs can trigger a "Failed to restore files" due to Windows locking a custom font file. In case your custom files somehow get misplaced and disappear upon restoring, there are backup archives of your custom files in your ``tf`` folder named lawena-user._timestamp_.bak.zip. **Update:** Recent Lawena versions fix this by installing custom fonts found on your chosen HUD before launching the game. If this causes visual glitches, uninstall the fonts and disable the option from the Advanced menu.
* Even though on latest versions this problem seems fixed, avoid extracting Lawena to the game folder (like TF2's "tf" directory). See [#25](https://github.com/iabarca/lawena-recording-tool/issues/25)
