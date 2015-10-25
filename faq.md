---
layout: page
title: FAQ
---

<div class="message">
  This page is present in the <a href="{{ site.github.repo }}/wiki">Wiki</a>. Check it out for more in-depth articles.
</div>

### The P key to record does not work anymore! How can I fix this?

It is possible that the P bind is lost due to own scripts or demos (since they record all commands you use). So please rebind the key using the console by typing ``bind p startrecording`` and it should work fine.

### TF2 is crashing when it's run from the tool! What can I do?

Try the following until it's fixed:

* Go to your Steam library and Validate your game cache (you might have a default file missing)
* Watch your demo using ``mat_queue_mode 1`` in your console (fixes multithreading issues)
* Temporarily rename or remove the ``recording.cfg`` file inside Lawena folder before running the game. Crashes might be related to graphic configuration set by that cfg file.
* Come to our [chat](https://gitter.im/iabarca/lawena-recording-tool) and let me know about it, or report an [issue](https://github.com/iabarca/lawena-recording-tool/issues) with the ``lawena.log`` file that the tool created and we'll figure it out together.

### Lawena is not replacing my cfg and/or HUD files correctly, and I'm getting an ``AccessDeniedException`` in the log! What's wrong?

When replacing files, sometimes the tool encounters a process that is blocking a folder (like ``tf/cfg`` or ``tf/custom``) from being moved, failing to put lawena's files into TF2. Most of the time it's explorer.exe, in which case you could try killing/relaunching it from the Task Manager. If that does not help, try relogging or restarting. Sorry for this inconvenience while I work on a definitive fix.

### I ran TF2 through the tool, and when I tried to run it normally afterwards, my whole config was gone! What can I do to recover it?

Just open the tool once again and then close it. That should restore your cfg, hud and sounds to normal. If it doesn't check the Troubleshooting section under **Instructions** and follow those steps.

**Don't ever delete folders named 'lwrtcfg' or 'lwrtcustom'. They contain YOUR files!**

### The tool is asking me for permission to edit my registry! Is this normal?

Yes, it's the only way to ensure that you recover your previous DirectX level on TF2. Otherwise, you'll be stuck at dxlevel 98. (the key is ``HKEY_CURRENT_USER\Software\Valve\Source\tf\Settings\DXLevel_V1``)

### The tool is running lots of vbscripts! Is this normal?

Yes, it's the same script running over and over to check if your TF2 is still running, don't worry.
