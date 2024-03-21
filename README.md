# vale-education-poc
Internal repository for testing Vale for use in local development.

Please note that previous versions of this doc and the configuration only worked with Vale 2.x. The latest version (as of 3/21) is now 3.2.2. The configuration and steps to set up Vale now assume you are using Vale 3.2.2 or later (later versions could also introduce breaking changes).

**New in Vale 3.x**

Unlike Vale version 2.x, the Vale configuration file `vale.ini` MUST be named `.vale.ini` - previous versions were flexible.

The `styles` directory now must exist in an OS-specific directory (see steps below).

The `vocab` directory is now `vocabularies` and must exist in `styles/config`. The remaining vocab configuration (accept.txt and reject.txt) remains the same.

## Feedback, ideas, problems, etc

If you have an idea on how to improve the use of, or find issues when using Vale please open a GitHub issue on this repository.

## Required version

The configuration in this repository requires Vale version `3.2.x` (tested specifically on `3.2.2`).

Run `vale --version` to verify the version you have instaled.

## Known issues

- Setup is very manual at this point. Plan to streamline if/when we choose to adopt Vale.
- This setup is intentionally limited to only 10 different style considerations. This was done to not overwhelm us as we test and figure out what rules we as a team want to use/add.
- The version of Vale is critical to ensure the configuration in this repository works. You must be running at least Vale 3.2.2.

## What is Vale

"Vale is a linter for prose" - said another way - its a way super rad grammar checker for the command line or your favorite IDE (assuming your favorite IDE is one of the Vale supported IDEs).

Vale runs locally and does not send data back to any 3rd parties (looking at you Grammarly). It is completely customizable through the use of configuration files. Sample configuration files can be found at https://github.com/errata-ai.

## Installation (manual)

1. Install Vale (https://vale.sh/docs/vale-cli/installation/).

   **OSX**
   
    ```shell
    brew install vale
    ```

    **Windows**
   
    ```shell
    choco install vale
    ```

1. Open a terminal and navigate to your preferred source code directory.

    ```shell
    cd ~/src
    ```

1. Clone this repository.

    ```shell
    git clone git@github.com:hashicorp-education/vale-education-poc.git
    ```

1. Copy the Vale contents of this repo (`.vale.ini` and `styles` directory and subdirectories) to the `$HOME/Library/"Application Support"/vale/` directory. For Windows, copy to `%LOCALAPPDATA%\vale\`.

    ```shell
    cp -r vale-education-poc/ $HOME/Library/"Application Support"/vale/
    ```

1. Confirm installation by syncing styles.

    ```shell
    vale sync
    ```

   The command should return no output. If you encounter an error instead. confirm that the `Application Support` / `%LOCALAPPDATA%` directories contain the `vale/.vale.ini` configuration file and the `vale/styles`    
   directory.

1. Install the Vale VSCode extension.

1. Once you have installed the VSCode extension, relaunch VSCode.

1. Click the gear icon → Extension settings to access the settings.

1. (Optional) Check the **Enable spell checking with with Vale** checkbox.

1. Restart VSCode and edit away. Vale feedback will be available in the **PROBLEMS** tab:

![image](https://user-images.githubusercontent.com/92055993/206570255-602bdd9e-dcab-4d2d-85ee-17f354c2ec9b.png)

## Additional Vale configs
When looking to add new configurations Vale, start with the Google style guide examples https://github.com/errata-ai/Google
