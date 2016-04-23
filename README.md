# HNClient – A desktop client for Hacker News

## Features
- You can easily choose articles to view and switch to the comments, no more
  endless new tabs for HN
- Optional split screen: View articles and their comments next to each other
- Easily navigate the App with Vim like keyboard shortcuts
- Comments are foldable
- Things that are overlooked by most HN apps weren't forgotten, stuff like
  displaying HN polls, rendering PDFs or not showing a website for Ask HN posts
- Automatically loads new articles if you scrolled down far enough
- It's Open Source, you can change it however you like! :)

![](https://i.imgur.com/L3eyTqZ.png)
![](https://i.imgur.com/4e36YVo.png)

## Keyboard shortcuts

| action | shortcut |
|:--|:--|
| next story |  <kbd>j</kbd> |
| previous story |  <kbd>l</kbd> |
| cycle between display modes (links, comments, both) |  <kbd>l</kbd> |
| next comment |  <kbd>n</kbd> |
| previous comment |  <kbd>m</kbd> |
| fold / expand the current comment |  <kbd>enter</kbd> |
| reload stories list |  <kbd>r</kbd> |
| display a list of all shortcuts |  <kbd>h</kbd> |


## Tech overview
- Electron
- ES6, React and Redux
- Stylus and [css-modules](https://github.com/css-modules/css-modules)
- Webpack
- JavaScript [standard](https://github.com/feross/standard) style
- Mostly follows the conventions of the [electron-react-boilerplate](https://github.com/chentsulin/electron-react-boilerplate)
- Uses the nice [node-hnapi](https://github.com/cheeaun/node-hnapi) which wraps HN's official API. HN's API itself is sadly not very usable so far, e.g. to fetch all 200 comments of a thread we'd need to do 200 requests, which would greatly degrade user experience. Thanks to node-hnapi this app does not need to do that.
