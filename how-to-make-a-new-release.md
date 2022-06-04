1. Fetch fresh translations.

    1. Go to the project's Poeditor page (use https://poeditor.com/join/project?hash=vQy5XjnrGL to join)

    2. Open one of the translated languages pages, **BUT NOT THE ENGLISH ONE**.

    3. Click "Export" at the top bar.

    4. Select the "ARB" format.

    5. Select "Export - Translated".

    6. Select "Order - Terms Alphabetically" (for simpler diffs).

    7. Filename - "app_LANGCODE", where LANGCODE should be the language's ISO 639-1 language code.

    8. Click the "Export" button.

    9. Repeat for each of the languages, **EXCEPT FOR ENGLISH**.

    10. Put all of the downloaded "app_LANGCODE.arb" files to plante/lib/l10n (replace the old ones).

    11. Ensure the git diff looks okay, make a new branch, make a commit, open a Pull Request, merge it.

2. In the local repository, change active branch to master and fetch the latest commits (the last one should be the translations fetch).

3. Change version of the app in pubspec.yaml.
  First part of the version should be current date, second part is a number always increased by 1.
  For example, if you open pubspec.yaml and it has next version: "22.06.040+59", "22" means 2022, "06" is the month, "040" is the day (in this example it's 4th of June). The "040" has a zero at the end so that hotfixes would be possible ("040" would be the first release of the day, "041" would be the first hotfix).
  Let's say it's the 10th of november, then the new version should be "22.11.100+60".
  **Don't make a commit yet**.

4. Build locally a release version for manual testing (Android-instruction below, an iOS-instruction wanted).

    1. Execute "$ flutter build appbundle" from the app's root directory. In the end, an .aab-file should be produced.

    2. Convert the .aab into an .apk:

        1. Download Bundletool: https://github.com/google/bundletool/releases

        2. Get a release keystore to sign the app (in-app sign-in might not work on a not-properly signed app).

        3. Execute: "java -jar /path/to/bundletool.jar build-apks --bundle=build/app/outputs/bundle/release/app-release.aab --output=/tmp/plante.apks --mode=universal --ks-key-alias KEY_ALIAS_OF_KEY --ks /path/to/keystore.jks

        4. Execute: "unzip /tmp/plante.apks -d /tmp/"

        5. The /tmp/ folder now should contain a freshly built and signed .apk-file.

5. Go through the manual testing process: [manual-test-cases-for-new-releases.md](manual-test-cases-for-new-releases.md)

    1. Proceed only if the manual testing found no problems.

6. Push app's version change.

    1. Make a commit with the new app's version which you have set before manually testing the app.

    2. Ensure the git diff looks okay, make a new branch, make a commit, open a Pull Request, merge it.

7. Make a new release on Github.

    1. Open https://github.com/plante-app-team/plante/releases

    2. Press "Draft a new release".

    3. Click "Choose a tag", paste the new app's version string (e.g. "22.11.100"). Click "Create new tag ...".

    5. Click "Auto-generate release notes".

    6. Click "Publish release".

8. Upload the new app version.

    1. Upload the built .aab (not .apk!) to Google Play.

    2. Upload the built iOS-app to App Store.

