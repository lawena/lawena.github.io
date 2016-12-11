---
layout: page
title: Instructions
---

<div class="message">
  This page is present in the <a href="{{ site.github.repo }}/wiki">Wiki</a>. Check it out for more in-depth articles.
</div>


## Installation and use

* Check the **Download** page for a direct link to Java install and Lawena archive.
* Extract the ``.zip`` to a clean folder
* Run ``lawena.exe``, the updater should run and it will automatically launch the tool
* Your TF2 directory should be auto-detected (you can always change it from the "File" menu in the UI)
* Choose your moviefile directory, where the tool will store everything you record
* Configure it as you like, also you can save settings to a file and edit them later
* Start TF2, Lawena will make a backup of your ``cfg`` and ``custom`` folder while TF2 is running
* Load a demo and press P to start recording. Please note that you might hear buggy or repeating sounds. This is expected and it won't be corrupted in the resulting audio file so don't worry.
* When you close TF2, your files should be restored (there should be no ``lwrt`` folders inside your ``tf`` folder)
* To compile your captured frames to a video file, head over to this [Wiki page](https://github.com/quanticc/lawena-recording-tool/wiki/Synchronize-audio-and-video).
* The resulting file can be passed through an encoding tool or a video editing program.

## Adding custom resources

 * This version will detect all VPKs and folders inside your ``tf/custom`` folder, so just by having your files there you'll have the option to load them when Lawena launches TF2s
 * You can also use the ``custom`` folder of Lawena , where some default VPK were included to show you how it works
 * If you select your custom HUD in the custom resources list, you'll have to select "Custom" as your selected HUD option or there could be conflicts
 * If you want to add extra skyboxes, put the ``.vtf`` files (not the ``.vmt``) inside the ``skybox`` folder of Lawena and it will load along the included

## Troubleshooting

* If Lawena is not closed properly, running it once should restore all folders. Your files are inside the ``lwrtcfg`` and ``lwrtcustom`` folders. In general, Lawena tries to restore your files: (a) when it's starting, (b) when it's closing, (c) before it starts TF2 and, (d) when TF2 finishes running.
* If files can't be replaced (you get a failure message) it's in almost every case caused by a process preventing key folders from being moved/deleted, so to avoid deleting or mixing your files, Lawena aborts the operation. Please try the following in order until it's fixed:

1. Close any opened folder in Windows that's related to TF2 folder (``tf/cfg``, ``tf/custom``, and subfolders)
1. Close any program that could be interfering with TF2 folder
1. Log off and re-log to Windows (alternatively: Try killing and restarting ``explorer.exe`` from the Task Manager)
1. Restart your PC
1. Tell me about it in GitHub issues/Steam

* Check the **FAQ** for more info!
* Please report any [issue](https://github.com/quanticc/lawena-recording-tool/issues) you might find. Also you can use that same page to suggest new features.
