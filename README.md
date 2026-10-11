[Download Etch 0.1.407 for macOS](https://github.com/fabric-8/etch-releases/releases/download/build-407/Etch-0.1.407-build-407.dmg)

# Install and update Etch

Etch supports Apple Silicon and Intel Macs running macOS 26 or newer.

## Install

1. Open https://github.com/fabric-8/etch-releases and use its current Etch DMG download link.
2. Open the DMG and drag Etch into Applications. Replace the existing Etch if asked.
3. Open Etch from Applications, then eject the disk image.

The app includes its themes, the Etch MCP helper, and its agent skills. You do not
need the Etch repository, Xcode, GitHub access, or a developer certificate. On a
managed work Mac, your organization may need to allow installation or app updates.

## Set up this Mac

Start planning immediately. Grant calendar, microphone, speech, screen recording,
or accessibility permission when you use the corresponding feature. You can change
those grants later in System Settings → Privacy & Security.

For sync, sign into your Apple Account in System Settings and enable iCloud Drive.
Settings → Sync reports Etch's connection. Use the same Apple Account on both Macs
to share Etch data and the Etch project folder in iCloud Drive. Etch also works
locally when iCloud is unavailable.

On a Mac that is new to Etch, let the initial iCloud download restore your existing
workspace. A new, empty account gets starter life areas after that check completes.
While offline, you can plan in Inbox and create your own life areas immediately.
If the initial download is interrupted, use Settings → Sync → Retry Sync.

For agents and synthesis, install Claude Code using its setup guide at
https://code.claude.com/docs/en/setup and sign into your own account. In Etch,
Settings → AI Agent lists the accounts, lets you assign one to each life area,
and offers to install the included skills. Repeat this setup on each Mac.

Work and personal Claude accounts can both be configured on one Mac, each with its
own login folder. Give them clear names and check the selected account before
starting work. These Claude accounts are separate from your Mac's Apple Account.
Different Apple Accounts have separate iCloud data; switching the Mac's Apple
Account does not create an isolated Etch workspace. Use separate macOS users when
you need independent local workspaces.

Some optional agent skills and session-capture hooks use Python 3. Install Python 3
if your Mac does not have it before enabling those integrations. Native planning,
the MCP helper, and application updates do not require Python.

## Update

Open Etch → Check for Updates, or Settings → General → Updates. Etch normally
checks automatically; General has the preference to turn those checks on or off.

When an update is available, review the changes since your installed version and
choose Install Update. Etch downloads and verifies it, replaces the app, and
relaunches. Finish active work first; Etch's normal quit handling still applies to
running agents. Your calendar data, account logins, preferences, and project files
live outside the app and remain in place.

The updated app includes fresh agent skills. In Settings → AI Agent, use each
agent's Install/Update action, or enable its automatic skill updates after its
first installation. An app update does not sign into accounts on your behalf.

If the update check fails while offline, try again when connected. If an update
cannot be installed, quit Etch and install the latest DMG into Applications.
Do not delete your Application Support folder to fix an update.

On the Mac where you develop Etch, use the updater for the app you use day to day.
`scripts/run.sh` builds the repository's development version and replaces the same
Applications copy; that version connects to CloudKit Development. Use the script
when you deliberately want to run a development build. To return to the distributed
app and CloudKit Production, install the current DMG again.
