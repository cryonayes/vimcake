# :cake: vimcake :cake:
A simple vim configuration package for beginners!

**Ideal** for 42 school students, but not only!

## Plugins list:
- vim-plug
- vim-airline
- vim-airline-themes
- vim-monokai
- colorizer
- nerdtree
- ultisnips
- vim-snippets
- vim-42header 

## How to install
Use the following command in a terminal:
```shell
make install
```
It will potentially erase your current vim config (.vim folder and .vimrc file), backup your files first!

If you don't have configured vim, this package is safe to use, in other words you don't have a .vimrc.

The package can be reinstalled with...
```shell
make re
```
Or removed with:
```shell
make clean
```

## File explorer:
Press _**Ctrl**_+_**n**_ inside vim to open/close NERDTree.

NERDTree is shown by default if you start vim with a directory as argument.

## Autocompletion:
Crush your damn _**Tab**_ key! For example, if you type in a C file:
```c
if|
```
And then you press _**Tab**_, it'll load a snippet and move your cursor in the condition field:
```c
if (|)
{
  
}
```
Now you can add a condition:
```c
if (1 && 0|)
{
  
}
```
Press _**Tab**_ again to move your cursor to the next field (inside brackets in this case):
```c
if (1 && 0)
{
  |
}
```
It works with:
- if -> if _**Tab**_
- else -> else _**Tab**
- while -> while _**Tab**_

and especially for C/C++ files:
- include -> inc _**Tab**_
- main -> main _**Tab**_ (with arguments) or mainn _**Tab**_ (without arguments)

... and more!

## Color visualizer
Colorizer allows detection of text that contains a RGB or RGBa color by coloring its background

See the [documentation](https://github.com/lilydjwg/colorizer/blob/master/README.mkd "Colorizer's documentation") for more details.

## Folding

Press _**F3**_ to fold/unfold your code.

Very handy with huge files!

## 42 Header
42 Header can be added to your files by pressing _**F2**_.

Username and mail can be edited in your ~/.vimrc (Section \<Plugins config\>).

Another simple solution is to use arguments with make by using variables during installation:
```shell
make install USER="username" UMAIL="user" DOMAIN="domain"
# Set header username to "username" and email address to "user@domain"
make install USER="username"
# Set header username to "username" and email address to "username@student.42.fr"
make install UMAIL="user"
# Set header username to $USER and email address to "user@student.42.fr"
```
_UMAIL_ variable takes _$USER_ content by default

_DOMAIN_ variable is set to "student.42.fr" by default

## User Interface
monokai, which has been slightly modified, is the current colorscheme used and airline-theme is set to dark.

Some adjustments have been made in the vim configuration file to make vim more pleasant and convenient to use!
