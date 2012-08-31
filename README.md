#Polite

Polite是一个为前端开发者量身打造的Vim配置和插件精选集

##安装Polite

_windows && Cygwin || mac || linux:

    git clone https://github.com/wayfind/polite.git
    cd polite
    ./install

该脚本从github上clone代码后将文件拷贝到vim安装目录,与vim73目录平级，覆盖原来vimfiles目录即可。  
从github上clone代码后执行./install即可。install脚本将在用户目录下建立两个软链接到工程目录。

##更新Polite

Polite使用了Git submodule做工程管理，每次更新需要执行以下命令

    cd polite
    git pull
    ./install

更多细节，请了解git submodule

##卸载Polite

    cd polite
    ./uninstall

##为什么会有Polite

1. Vim是历史悠久特性丰富的编辑器。但插件质量良莠不齐,有的插件非常影响性能，插件之间存在冲突的情况也比较常见。对于初学者而言插件选择，以及解决插件安装后的冲突问题成为一个难以越过的门槛。Polite根据最小够用原则,多方面对比，精心选择了几个高质量基础插件来完成所需要的编辑功能。
2. 便于配置。降低Vim配置复杂度，通过github管理插件及配置文件，通过简单一个git clone命令提高Vim配置效率。
3. 便于更新。Polite通过git submodle的形式管理Vim插件。如果插件有更新，只需要执行git submodule update即可。
4. 灵活切换。借助Git强大的Branch机制，Polite可以根据语言场景切换插件和配置。目前Polite支持通用编辑场景(master)和前端开发(frontend)场景。frontend场景提供了更加丰富的代码高亮和自动完成特性。切换到前端开发场景通过git checkout frontend即可闪电完成。
5. 一致性。使用Polite，能在各种终端环境获得一致体验集。包括文件搜索。

##Polite插件
Polite采用了git submodule的形式管理插件，这样的机制保证Polite的配置的更新和插件更新分离。可以定期运行install脚本以便获取最新版本插件。除Vim中文文档以外的所有插件都安装在vimfiles/bundle中。如果需要详细了解插件使用，请进入插件项目了解。

###文档

Vim是一个需要不断查询帮助以积累经验的编辑器。Polite集成了中文Vim文档。方便中文开发人员。

###模块化

vim的在插件管理方面并未提供隔离性强的机制，通常是一个插件的文件被分散在各目录之间，引起管理上的不变。Polite使用pathogen做插件管理，在pathogen中，所有插件都可以安装在bundle子目录下，使得vim处理插件更加优雅。

###工程管理

引入NERDTree，controlP解决来解决这个问题。特别推荐controlp插件，原型来源于sublime ctrl+p或者eclipse ctrl+shift+r又或者TextMate command+t。

    激活或隐藏NerdTree：,nt (先按逗号','紧接着按字母'n',再接着按字母't')
    激活controlp: 在普通模式下ctrl+p,输入需要进行过滤的部分文件名。用上下键选择需要打开的文件即可。

注意：这两个插件都是根据Vim当前目录来决定搜索范围的，一般来说是是当下用vim所打开文件目录。如果有问题，请用:cd d:\命令设置Vim当前目录。
    

###代码片段

编辑器应该具备比较完善的自动完成能力,代码片段或者模板是一种不错的方式。选择了优秀插件snipmate来做片段管理。

    以js为例，打开一个js文件。到空行输入fun<tab>，即发现vim已经输入了完整的function模板信息，通过tab键在各输入域切换。

详细帮助请查阅help snipmate或者自行搜索。

##配色

Vim配色众多。Polite精心选择了Solarized作为默认颜色配置。该配色方案充分考虑了各平台、各字体下的颜色显示差别，提供了一个经过认真考量的配色环境。详情请猛击这里http://ethanschoonover.com/solarized

##字体

建议在Vim选择了平滑美观的Envy Code R字体。在17寸以上液晶显示器下显示效果不错。
该字体的特点是等宽、中英文区分明显、trueType字体、小巧。适合编程试用。Polite在配置了默认使用此字体，如果没有将使用系统默认字体。如果你需要此字体，请到http://damieng.com/blog/2008/05/26/envy-code-r-preview-7-coding-font-released下载并安装。 

##使用技巧

###行号

Polite使用了相对行号，在相对行号模式下，左侧行号将显示与当前光标所在行的相对距离，利用此特性配合h,j,k,l。可以飞速在行间切换。如输入5j，则向下跳到距离当前行距离为5的行。

后续使用技巧完善中.......
