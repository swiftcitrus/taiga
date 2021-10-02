# Taiga

[![](https://img.shields.io/github/license/erengy/taiga)](https://github.com/erengy/taiga/blob/master/LICENSE)
[![](https://img.shields.io/github/v/release/erengy/taiga)](https://taiga.moe/download.php)
[![](https://img.shields.io/github/v/release/erengy/taiga?color=blue&include_prereleases)](https://github.com/erengy/taiga/releases)
[![](https://img.shields.io/discord/423475967051169813?logo=discord)](https://discord.gg/yeGNktZ)

Taiga is an open-source desktop application for Windows. It automatically detects the anime videos you watch on your computer and synchronizes your progress with [AniList](https://anilist.co), [Kitsu](https://kitsu.io) or [MyAnimeList](https://myanimelist.net). It helps you manage your anime library, discover new series, share watched episodes and download new ones.

Visit our [home page](https://taiga.moe) for more information. See the [guidelines](https://github.com/erengy/taiga/wiki/Guidelines) if you'd like to contribute. Here's [how to compile](https://github.com/erengy/taiga/wiki/How-to-Compile).

## Related projects

- [Anime relations](https://github.com/erengy/anime-relations): Episode redirections
- [Anisthesia](https://github.com/erengy/anisthesia): Media detection library
- [Anitomy](https://github.com/erengy/anitomy): Anime video filename parser
- [taiga.moe](https://github.com/erengy/taiga-moe): Home page of Taiga

## License

Taiga is licensed under [GNU General Public License v3](https://www.gnu.org/licenses/gpl-3.0.html).

## Adding new players

From [https://github.com/erengy/anisthesia/issues/6#issuecomment-761685887](https://github.com/erengy/anisthesia/issues/6#issuecomment-761685887)

First, please download [WinSpy++](https://www.catch22.net/software/winspy) and drag its finder over mpc-qt's window to read the class name. It should be something like Qt5QWindowIcon or Qt5151QWindowIcon. In that case, the following should work:

1. Download players.anisthesia and copy it to Taiga\data\players.anisthesia.
2. Open the file with a text editor and find the Media Player Classic Qute Theater section.
3. Replace Qt5QWindowIcon with ^Qt.+QWindowIcon and save the file.
4. Restart Taiga.