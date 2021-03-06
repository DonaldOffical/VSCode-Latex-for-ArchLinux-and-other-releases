# VSCode-Latex-for-ArchLinux-and-other-releases
latex installation note

This note is more suitable for linux(base on Arch and the other linux versions)/ macOS(Unix). You need to replace the "pacman" to your own control rules while using this note. 
Compared with Word, writing papers in latex has the advantage that latex has better page rendering and typesetting is more convenient and faster. In addition, more and more academics/conferences have released official latex templates. Learn latex syntax and focus on content rather than format.

![image](https://github.com/DonaldOffical/VSCode-Latex-for-ArchLinux-and-other-releases/blob/main/images/b.png)

If you don't wanna install the latex on your linux/macOS, you can use this online latex tool.
```
https://www.overleaf.com/
```
1/Build LaTeX environment(install Texlive)
```
sudo pacman -S texlive-most
sudo pacman -S texlive-lang
sudo pacman -S texlive-publishers                  #To solve bibtex problems#
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
you can press F1 in the VSCode interface, then type "setjson", click "Preferences: Open Settings (JSON)"
 
 when you open the JSON, you need to input the content
 ```
 {   
    "latex-workshop.latex.tools": [
        {
            "name": "xelatex",
            "command": "xelatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "-pdf",
                "%DOC%"
            ]
        },
        {
            "name": "latexmk",
            "command": "latexmk",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "-pdf",
                "%DOC%"
            ]
        },
        {
            "name": "pdflatex",
            "command": "pdflatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "%DOC%"
            ]
        },
        {
            "name": "bibtex",
            "command": "bibtex",
            "args": [
                "%DOCFILE%"
            ]
        }
    ],
    "latex-workshop.latex.recipes": [
        {
            "name": "xelatex",
            "tools": [
                "xelatex"
            ]
        },
        {
            "name": "pdflatex -> bibtex -> pdflatex*2",
            "tools": [
                "pdflatex",
                "bibtex",
                "pdflatex",
                "pdflatex"
            ]
        }
    ]
}
```
5/Now enjoy it!
you can download some LaTeX templates to test, such as IEEE
```
https://www.ieee.org/content/dam/ieee-org/ieee/web/org/pubs/conference-latex-template_10-17-19.zip
```
you can find a file with ".tex"
use vscode to open it
![image](https://github.com/DonaldOffical/VSCode-Latex-for-ArchLinux-and-other-releases/blob/main/images/a.png)
Click the triangle button in the upper right corner to compile
then click the second button and you can see the PDF
![image](https://github.com/DonaldOffical/VSCode-Latex-for-ArchLinux-and-other-releases/blob/main/images/2021-11-19%2009-56-40%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE.png)
Enjoy the LaTeX and have a nice day!
 
 
 
