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
Click the settings button
 ```
 ![image](https://user-images.githubusercontent.com/61338779/142527026-093b5424-60aa-417d-8c62-775ef4a0dab5.png)
 ```
 Click the first button in the upper right corner`
 
 ```
 ![image](https://user-images.githubusercontent.com/61338779/142530438-f5dd8165-389e-42a8-be80-9a7a78ec42cc.png)
 ```
 
 or you can press F1 in the VSCode interface, then type "setjson", click "Preferences: Open Settings (JSON)"
 
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
```
![image](https://user-images.githubusercontent.com/61338779/142536670-1fdd30c0-26c8-4282-9eaa-f4a90c107cad.png)

```
Click the triangle button in the upper right corner to compile
then click the second button and you can see the PDF

Enjoy the LaTeX and have a nice day!
 
 
 
