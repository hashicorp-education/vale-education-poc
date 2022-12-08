# vale-education-poc
Internal repository for testing Vale for use in local development.

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
