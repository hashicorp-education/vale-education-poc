# vale-education-poc
Internal repository for testing Vale for use in local development.

## Feedback, ideas, problems, etc

If you have an idea on how to improve the use of, or find issues when using Vale please open a Github issue on this repository.

## Required version

The configuration in this repository requires Vale version `2.21.x` (tested specifically on `2.21.3`).

Run `vale --version` to verify the version you have instaled.

## Known issues

- Setup is very manual at this point. Plan to streamline if/when we choose to adopt Vale.
- This setup is intentinally limited to only 10 different style considerations. This was done intentially to not overwhelm us as we test and figure out what rules we as a team want to use/add.
- The version of Vale is critical to ensure it works. For example, during testing, the path to styles in `vale.ini` works with version `2.15` using just `styles` but will not work with 2.21. Ensure you are on version `2.21.x`

## What is Vale

"Vale is a linter for prose" - said another way - its a way super rad grammar checker for the command line or your favorite IDE (assuming your favorite IDE is one of the Vale supported IDEs).

Vale runs locally, and does not send data back to any 3rd parties (looking at you Grammarly). It is completely customizable though the use of configuration files. Sample configurations files can be found at https://github.com/errata-ai.

## Installation (manual)

1. Install Vale (https://vale.sh/docs/vale-cli/installation/).

    ```shell
    brew install vale
    ```

1. Open a terminal and navigate to your preferred source code directory.

    ```shell
    cd ~/src
    ```

1. Clone this repository.

    ```shell
    git clone git@github.com:hashicorp-education/vale-education-poc.git
    ```

1. Copy the Vale styles directory from the repository directory to your home directory.

    ```shell
    cp -r vale-education-poc/.vale $HOME/
    ```

1. Move the Vale configuration file from the styles directory to your home directory.

    ```shell
    mv $HOME/.vale/vale.ini $HOME/.vale.ini
    ```

1. Confirm installation by syncing styles.

    ```shell
    vale sync
    ```

    The command should return no output. If you encounter an error instead. confirm that your `$HOME` directory contains both the `.vale.ini` configuration file and the the `.vale` styles directory.

1. Install the Vale VSCode extension.

1. Once you hve installed the VSCode extension, open the VSCode application.

1. Click the gear icon → Extension settings to access the settings.

1. In the **Vale > Vale CLI: Config** text box enter the full path to your `.vale` directory, for example `/Users/username/.vale`

1. Restart VSCode and edit away. Vale feedback will be available in the **PROBLEMS** tab:

![image](https://user-images.githubusercontent.com/92055993/206570255-602bdd9e-dcab-4d2d-85ee-17f354c2ec9b.png)

## Additional Vale configs
When looking to add new configurations Vale, start with the Google style guide examples https://github.com/errata-ai/Google
