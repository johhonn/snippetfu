Snippet-Fu
==========
Snippet-Fu lets you store and copy frequently used snippets
of text quickly by copying to clipboard with just one click.
All data is stored offline in your own computer and absolutely
nothing is tracked or communicated over the network. 

In analytics, development or even business, we often have to
repeatedly re-use long or complicated text like command lines, 
database connection strings etc. Using ad-hoc solutions like
text editors or note-taking apps to store these is fidgety
due to having to select the text to copy to clipboard and
error-prone due to risk of accidental overtyping.

Snippet-Fu prioritizes simple finding and re-use of text
by simply clicking on the stored text and has a search
function to quickly find what you are looking for. Unlike
clipboard managers, it will only keep what you explicitly
put into it and won't monitor your clipboard.

The snippets are stored as a plain JSON file in your local
data folder. Click the information icon to see the location
where the file is stored. Do not save passwords in Snippet-Fu.

History
-------
Snippet-Fu was originally released as a [Chrome app](https://chrome.google.com/webstore/detail/snippet-fu/goekbdcfildilcmmlodpfemnjlkjajco?hl=en)
but with [sun-setting](https://blog.chromium.org/2016/08/from-chrome-apps-to-web.html)
of the Chrome Apps platform for Windows and Linux, it is released
as a stand-alone app based on [Electron](http://electron.atom.io/).

Screenshots
-----------
![Snippet-Fu screenshot](screenshot.png)


Building
--------
This project is based on [Electron](http://electron.atom.io/) with 
[Electron Builder](https://www.electron.build/), [React](https://facebook.github.io/react/)
and [Material Components for Web](https://github.com/material-components/material-components-web-react/). It uses [Create React App](https://github.com/facebookincubator/create-react-app)
to bootstrap the react components and a modified version of the workflow
explained in [Kitze's blog]((https://medium.com/@kitze/%EF%B8%8F-from-react-to-an-electron-app-ready-for-production-a0468ecb1da3)
to integrate CRA with Electron.

- Clone the repository into a suitable location on the drive
  ```
  git clone https://github.com/srinathh/snippetfu.git
  ```
- Install all the development components and libraries through
  ```
  cd snippetfu
  
  yarn 
  ```
  
- To devlop locally, run the following yarn script
  ```
  yarn electron-dev
  ```

- To build the packed application, use the following script which calls `electron-builder`
  and packs executables for Linux, Mac & Windows. The Linux build is well tested, 
  Windows builds lightly tested & Mac un-tested. Testers & contributors welcome!
  ```
  yarn electron-pack -mwl
  ```

Changes from Version 1
------------------
- Integrated workflow between Electron & React
- New UI library - official React adapters of Material Components for Web
- Simpler architecture & fewer dependencies - specifically no more use of Redux

License
-------
Snippet-Fu, Copyright (C) 2017, Hariharan Srinath

This program is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License
as published by the Free Software Foundation; either version 2
of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software
Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA  02110-1301, USA.
