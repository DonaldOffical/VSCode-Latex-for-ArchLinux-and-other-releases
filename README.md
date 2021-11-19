# VSCode-Latex-for-ArchLinux-and-other-releases
latex installation note

This note is more suitable for linux(base on Arch and the other linux versions)/ macOS(Unix). You need to replace the "pacman" to your own control rules while using this note. 
Compared with Word, writing papers in latex has the advantage that latex has better page rendering and typesetting is more convenient and faster. In addition, more and more academics/conferences have released official latex templates. Learn latex syntax and focus on content rather than format.

If you don't wanna install the latex on your linux/macOS, you can use this online latex tool.
```
https://www.overleaf.com/
```
1/Build LaTeX environment(install Texlive)
```
sudo pacman -S texlive-most
sudo pacman -S texlive-lang
texlive-publishers                  #To solve bibtex problems#
```
2/Install VSCode (for mac you can download from appstore)
Offical site of VSCode
```
https://code.visualstudio.com/
```
you can use this command to install if you use linux
```
yay -S visual-studio-code-bin
```
if you don't install yay before, you can use this command
```
 sudo pacman -S yay base-devel 
 ```
 3/add these two extensions on your vscode
 ```
 LaTeX Workshop
 LaTeX language support
 ```
 4/modify the setJSON
 
