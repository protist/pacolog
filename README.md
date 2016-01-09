#paclog
List recent commits for Arch Linux packages. `paclog` can query packages from [official repositories](https://wiki.archlinux.org/index.php/Official_repositories) and the [AUR](http://aur.archlinux.org/).

##Usage
* Specify the package as the argument, e.g. `paclog vim`
* Optionally, specify the number of recent commits to view with `-l NUM`

```
$ paclog -l 3 vim
   Age                 Commit message (Collapse)              Author    Lines
9 hours    Use dynamic loading for language bindings         anatolik  -19/+24
           This allows to move Perl, Lua and Ruby into package optional
           dependencies. In the future it allows to eliminate vim-minimal
           package as its list of dependencies is the same as for vim.
           git-svn-id: file:///srv/repos/svn-packages/svn@257650
           eb2447ed-0c53-47e4-bac8-5bc4a241df78
2 days     FS#47500: merge python3 support into {g,}vim      anatolik  -186/
           package                                                     +20
           Now {g,}vim supports both python2 and python3 languages git-svn-id:
           file:///srv/repos/svn-packages/svn@257582
           eb2447ed-0c53-47e4-bac8-5bc4a241df78
11 days    Ruby 2.3.0 rebuild                                foutrelis -1/+1
           git-svn-id: file:///srv/repos/svn-packages/svn@257342
           eb2447ed-0c53-47e4-bac8-5bc4a241df78
```

##Dependencies
* `w3m`
* `sed` and `gawk` (both in `base-devel` for Arch Linux)
* Network access is required, since commit logs are not stored locally

##Acknowledgements
* Thanks to [dolik.rce](https://bbs.archlinux.org/profile.php?id=48434) for useful hints in the Arch Linux [forums](https://bbs.archlinux.org/viewtopic.php?pid=1591586)
