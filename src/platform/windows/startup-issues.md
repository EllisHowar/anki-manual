# Windows startup issues

<!-- toc -->

## Windows updates

When starting Anki, you may receive a message like the following:

- *Error loading Python DLL*
- *The program can't start because api-ms-win.... is missing*
- *Failed to execute script runanki*
- *Failed to execute script pyi_rth_multiprocessing*
- *Failed to execute script pyi_rth_win32comgenpy*

These errors are usually because your computer is missing a Windows update
or Windows library.

Please open Windows update, and ensure your system has all updates installed.
If any needed to be installed, please restart your device after installing.

## Windows 7/8

On Windows 7/8, you may need to manually install extra updates. Please try:

- <https://www.microsoft.com/en-us/download/details.aspx?id=48234>
- <https://aka.ms/vs/15/release/vc_redist.x64.exe>
- <http://www.catalog.update.microsoft.com/Search.aspx?q=kb4474419>
- <http://www.catalog.update.microsoft.com/Search.aspx?q=kb4490628>

## Video driver issues

Please see [display issues](./windows-display-issues.md).

## Antivirus/firewall software

Third-party software on your machine may prevent Anki from loading. You can
try adding an exception to Anki, or temporarily disabling your antivirus/firewall
to see if it helps.

## Admin access

Some users have reported that Anki did not run for them until they right-clicked
on the Anki icon and chose "Run as administrator". Anki stores all of its data in
your user folder, and should not need administrator privileges, but it's something
you can try if you've exhausted other options.

## Debugging

Starting Anki from a terminal may reveal a bit more information about some
errors. After installing the latest Anki version and ensuring all Windows
updates are installed, instead of running Anki directly, use Start>Run
and type cmd.exe. When a console window appears, type

```bat
cd \program files\anki & anki-console
```

Presumably Anki will fail to open like before, but it may reveal something about
what is causing the problem.

## If all else fails

If you are unable to start Anki after trying the above workarounds, you have
two remaining options:

- You can try [running from Python](./running-from-python.md).
- You can try an older Anki version built with an older toolkit, such as
  2.1.35-alternate, and 2.1.15.