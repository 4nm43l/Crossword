# Lexi Grove

Offline Android word-connect crossword game. The app embeds the bundled game in Android WebView. No network permissions, accounts, or external services are required.

## Build
Open this directory in Android Studio. Install Android SDK 35, use JDK 17 and Gradle 8.9, sync, then Build > Build APK(s). Android Studio can configure/download Gradle. A Gradle wrapper and a compiled APK are not included. Minimum Android: 8.0 (API 26). The SDK and Gradle were unavailable in the creation environment, so the Android shell has not been compiled or device-tested.

## Included
- Forty generated, connected crossword levels; swipe, tap, and keyboard letter selection.
- 32,507 bundled lowercase dictionary headwords (not an exhaustive inflected-word dictionary). Some rare or historical entries may occur; further editorial curation is recommended for a commercial release.
- Five tips initially. One letter per tip. New puzzle completions restore one tip, capped at five. No in-app purchases.
- Six persistent achievements, daily puzzles, and local scoreboard.
- Same-device two-player pass-and-play with matching boards and no tips. No online multiplayer or global leaderboard.
- Game progress saved in WebView local storage; clearing app data removes it.

Scoring: target word length × 10, bonus word length × 5, plus 100 for a newly completed level or daily puzzle. Replayed levels do not grant extra completion tips. Scores are local and are not cheat-resistant.

## Verification
JavaScript syntax checked; 40 boards tested for connectivity, dictionary membership, unique targets, and letter availability. Interaction checks cover submission, duplicate rejection, scoring, exhausted tips, saved progress, completion and rewards. Browser touch behavior and Android runtime remain unverified.

## Dictionary license
See app/src/main/assets/DICTIONARY-LICENSE.txt, retained from the installed US English Hunspell dictionary package. Original game source is provided for modification.
