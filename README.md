## About:
* Interactive UI in terminal built using [Urwid](http://urwid.org/index.html)
*	Searches all your files and categorises them according to type.
* Files and directories are ordered such that the ones which are closer to your working directory are displayed first.
* Uses Smart Casing for all the queries i.e If all letters in query are lowercase, case is ignored. Else it is case sensitive.
* Search with or without regex syntax.
* Hidden files and system directories(such as ```boot```,```sys```,```usr```,etc have the option to be indexed or hidden.(By default this is disabled as they can slow down search a lot and are usually not required to be searched.)
* Search for your apps and settings menus as well.
* Google right from your terminal.
* Get straight to your required result using command line arguments.

## Help Text (```srch -h```):
	usage: srch [-h] [-q QUERY] [-H] [-r] [-m] [-D | -A | -g | -t | -c | -d | -a | -i | -v]

    A system search tool to search for your files, apps and the web right from the
    terminal.

    optional arguments:
          -h, --help                show this help message and exit
          -q QUERY, --query QUERY   To search directly from command line
          -H, --hidden              To index hidden files and directories (This takes a lot of time to search)
          -r, --regex               Search query will use regex syntax. By default regex special characters do not work
          -m, --monochrome          UI will be in monochrome colour; i.e Black and white
          -D, --directories         Results are initially shown for directories
          -A, --apps                Results are initially shown for desktop apps(terminalapps not shown)
          -g, --google              Results are initially shown for google search
          -t, --text                Results are initially shown for plain text files
          -c, --codes               Results are initially shown for source code/script files
          -d, --documents           Results are initially shown for documents
          -a, --audio               Results are initially shown for audio files
          -i, --images              Results are initially shown for image files
          -v, --videos              Results are initially shown for videos
  
## Usage:
   Clone, cd into the repo and run ```./setup.sh```. This will install pip,which is required for [Urwid](http://urwid.org/index.html), and [Urwid](http://urwid.org/index.html), the third party TUI library for python. Finally it copies the program to the ```/usr/bin``` folder for accessing everywhere.

   Just running ```srch``` will open the interactive UI. Above arguments will open them applying the corresponding option.

   * Press ```Enter``` to search and ```Esc``` to quit.
   * Single click focuses on an item and double click opens the item.
   * ```Arrow Up```,```Arrow Down```,```Pg Up```,```Pg Down``` and ```Mouse Scroll``` can be used to scroll through the list.

## Known Issues:
   * The app is much slower than ```find```, especially when indexing system directories and hidden files.
   * About colours: Colours were made to go with a black terminal background and might look different on different terminals. It can be changed in the code in the palette array. Also there is a monochrome option available (```-m```)

## Screenshots:

![Imgur](https://i.imgur.com/Ex35t1C.png)
![Imgur](https://imgur.com/1utWL0o.png)
![Imgur](https://imgur.com/7lPikrU.png)

