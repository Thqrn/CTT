---
icon: material/folder-zip
---

# Programs

this section contains my curated list of software I use and love,

if you'd like to see more, I can't recommend enough to dive in FMHY's various [tools lists](https://fmhy.net/system-tools), 


## Honorable mentions:

I've used these in the past, or have been recommended by others

* [DeepL](https://www.deepl.com/en/translator): accurate translator
    * Available as a website and app, if using the latter you can press ctrl+c twice to directly open the app and send the clipboard to be translated
* Benchmarking [PresentMon](https://github.com/GameTechDev/PresentMon) via [CapFrameX](https://www.capframex.com/) or directly graphed with [Frame Time Analysis](https://boringboredom.github.io/Frame-Time-Analysis/)
    * PowerShell script I made back when I used it:
        ```ps1
        $T = Get-Date

        $CSV = "C:\PresentMon\PM-$Process $($T.Date -replace ' 00:00:00','' -replace '/','_') @ $($T.Hour).$($T.Minute).csv"

        @('javaw','r5apex','VALORANT')
        ForEach-Object {
            if (Get-Process -Name $_ -Ea Ignore){
                $script:ID = (Get-Process $_).ID
                break
            }
        }

        sudo PresentMon.exe -process_id $ID -output_file $CSV -hotkey 'ALT+SHIFT+X' -timed 15
        ```
* [Nirsoft](https://www.nirsoft.net/) and [Sysinternals](https://learn.microsoft.com/en-us/sysinternals/) NT software toolkits
    * Open With View: discard programs you never open apps with that bloat up your field (also see [ContextMenuManager](https://github.com/BluePointLilac/ContextMenuManager))
    * RegistryChangesView: create registry snapshots to compare what programs store on your computer when e.g. installing them also see [ProcMon](https://learn.microsoft.com/en-us/sysinternals/downloads/procmon)
    * ShellExView lets you disable custom shell extensions (e.g TeraCopy, QTTabBar, Visual Studio..)
* [linkshellextension](https://schinagl.priv.at/nt/hardlinkshellext/linkshellextension.html): easily make filesystem links (you can also powershell `New-Item -ItemType SymbolicLink -Path ./original -Target ./link`)
* [Zellij](https://github.com/zellij-org/zellij): a new cool alternative to tmux
* [Playit.gg](https://playit.gg) / [Minekube](https://connect.minekube.com/): programs that let you do port forwarding/tunneling without touching your router's open ports, useful for self-hosting minecraft servers