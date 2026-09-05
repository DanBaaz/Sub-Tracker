# Change Log

All notable changes to Sub Tracker, newest first. This mirrors the
in-app Change Log (Help → Change Log).

## v1.10
- Added Late player marking (mid-game): players who arrive after the game starts can be marked "Late" instead of Present — fully playable right away, with a red segment on their bar recording the time they missed. Toggle it on/off in App Settings
- Added a Missed sub warning (App Settings): flashes the screen and plays a sound if the court has fewer than 5 players for too long, with a configurable delay — skips triggering when the squad has 4 or fewer players available to play
- Added a Flash toggle to Sub reminder cues, alongside Sound and Vibration
- Fixed confirmation dialogs (e.g. Clear All Data) sometimes appearing hidden behind other open pages
- Sub time to cue seconds field now steps in 5-second increments

## v1.09
- "PLAYER LIST" label in team options now shows a live player count, e.g. "PLAYER LIST (19)"
- Added configurable Sub In and Sub Out colours per team
- Fixed the Sub Out highlight sometimes being covered by a player's time-played bar
- All colour settings (background, player bar, on-court, off-court, sub in/out) moved into a dedicated "Colour Schemes" page, with a Reset to Default Theme button

## v1.08
- Added sub reminder cues (per team): sound and/or vibration alerts once "time since last sub" passes a set length, repeating until the next sub — with independent on/off toggles for cues, sound, and vibration, min:sec cue timing, and an iOS vibration note
- Sound/Vibration toggles and cue timing fields laid out on one line each; timing fields grey out automatically if both Sound and Vibration are off
- Added a configurable off-court highlight colour per team, next to the on-court highlight colour — bench players now get their own coloured outline instead of none

## v1.07a
- Number of sub suggestions can now be set up to 5 regardless of current roster size — it still auto-scales down live during a game to match actual bench capacity
- Default number of sub suggestions for new teams is now 3
- "(max #)" hint next to sub suggestions is now a fixed "(max 5)"

## v1.07
- Added a Change Log page (accessible from Help) with full version history
- Absent players now automatically move to the bottom of the list on the setup screen and Edit Team page, with reorder arrows constrained within the present/absent groups

## v1.06
- Added a "time since last sub" timer that resets when the court returns to a full 5 players
- Repositioned the period label, period timer, and sub timer for clarity

## v1.05
- Added a Help page and an App Settings page (export, import, and clear all data)
- Added a default basketball logo shown until a team uploads its own
- Reorganized the Edit Team page: player list moved up, New Game moved to the bottom, Help/Settings added to the header

## v1.04a
- Screen now stays awake automatically during a game on mobile

## v1.04
- Widened the Select button on the Your Teams page
- Sub Out suggestions now freeze and reset the same way Sub In suggestions do
- Number of sub suggestions now auto-scales to match the active squad's real bench capacity

## v1.03
- Fixed Court Time sort order (on-court: most time at top; bench: least time at top)
- Sub Out and Sub In suggestion counts are now capped independently
- Sub In suggestions now freeze instead of changing names until the court is back to a full 5

## v1.02
- Added present/total player count to the setup screen (e.g. 8/12)
- Enforced a 12-player game-day limit, with a clear warning if exceeded
- Added reorder arrows and a starting-5 highlight to the setup screen
- Removed the 12-player cap on the full team roster — only game-day presence is capped

## v1.01
- Delete Team is now hidden while a game is in progress

## v1.0
- Added foul tracking: "Player Foul Limit Reached" button — fouled-out players move to the bottom of the list and are excluded from subs and suggestions
- Added a configurable number of sub suggestions per team, auto-scaling to bench size
- Fixed mid-game player list edits not syncing to the live game roster

## v0.9
- Replaced native browser confirm dialogs with a custom in-app confirmation popup, fixing New Game / Next Period not responding in some environments
- New Game button moved into team options, with confirmation before starting a new game
- Next Period now confirms before resetting the clock if time remains, and resets the countdown
- Added reorder arrows to the team list on the Select Team page

## v0.7
- "Select Team" button replaces the gear icon on the setup screen only
- On-court players now shown at the top of the roster list during a game
- Thicker on-court outline
- Background colour choice now automatically adjusts text and panel contrast

## v0.6
- Added a present/absent toggle directly on the setup screen
- Gear button jumps straight to the current team's settings once a game is in progress

## v0.4
- Player roster management moved into team options (add, rename, remove, reorder) and made persistent across sessions
- Added a present/absent toggle per player in team options
- Added a toggle for sub suggestions based on Court Time vs Next On List

## v0.2
- Earliest saved version: team creation and management (name, format, timer duration, logo, colours), basic roster entry, tap-to-sub tracking with on-court highlighting, and automatic sub suggestions
