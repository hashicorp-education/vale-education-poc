# vale-education-poc
Internal repository for testing Vale for use in local development.

## What is Vale

"Vale is a linter for prose" - said another way - its a way super rad grammar checker for the command line or your favorite IDE (assuming your favorite IDE is one of the Vale supported IDEs).

Vale runs locally, and does not send data back to any 3rd parties (looking at you Grammarly). It is completely customizable though the use of configuration files. Sample configurations files can be found at https://github.com/errata-ai.

## Installation (manual)

1 - Install Vale (https://vale.sh/docs/vale-cli/installation/).

`brew install vale`

2 - Open a terminal and navigate to your home directory.

`cd ~`

3 - Create a directory named `.vale`.

`mkdir .vale`

4 - Change into the `.vale` directory and create sub-directory named `sytles`.

`cd .vale && mkdir styles`

5 - Change into the `styles` directory and create sub-directories named `education` and `vocab`.

`cd styles && mkdir education vocab`

6 - Change into the `vocab` directory and create a sub-direcotry named `hashicorp`.

`cd vocab && mkdir hashicorp`

7 - Copy the `accept.txt` file from this repo to `~/.vale/styles/vocab/hashicorp/`.

8 - Copy all the `yml` files from this repo to `~/.vale/styles/education/`.

9 - Copy the `vale.ini` file from this repo to `~/.vale/`.

10 - Verify the directory structure is similar to

```
theapresont@theapreston-C0EXC311ENT .vale % tree
.
├── styles
│   ├── education
│   │   ├── Accessibility.yml
│   │   ├── Avoid.yml
│   │   ├── ComplexWords.yml
│   │   ├── GenderBias.yml
│   │   ├── HeadingCapitalization.yml
│   │   ├── Inclusion.yml
│   │   ├── OxfordComma.yml
│   │   ├── SentenceLength.yml
│   │   ├── We.yml
│   │   └── Wordiness.yml
│   └── vocab
│       └── hashicorp
│           └── accept.txt
└── vale.ini
```

11 - Install the Vale VSCode extension.

12 - Once installed, click the gear icon >> extension settings to access the settings.

13 - In the **Vale > Vale CLI: Config** text box enter the full path to your `.vale` directory.

Example:

/Users/theapreston/.vale
