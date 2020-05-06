# 插件管理

    git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim

vundle 环境设置

    " vundle 环境设置
    set nocompatible 
    filetype off
    " ##################
    " linux 配置
    " vundle 管理的插件列表必须位于 vundle#begin() 和 vundle#end() 之间
    set rtp+=~/.vim/bundle/Vundle.vim
    call vundle#begin()
    " ##################
    " windows 配置
    " 设置缓存文件夹  C:\windows\Temp  属性可读，完全控制
    " 管理员身份打开 gvim ，安装插件
    " set rtp+=$HOME/gvimfiles/bundle/Vundle.vim
    " let path='$HOME/gvimfiles/bundle/'
    " call vundle#begin(path)
    " ##################
    Plugin 'VundleVim/Vundle.vim'
    " 插件列表结束
    call vundle#end()
    filetype plugin indent on

windows 下放在安装目录的设置 `$VIM`  (安装目录下 `vimrc` 文件)

#### 1. 需要将 gvim 目录加入系统环境变量
#### 2. 需要将 git 目录加入系统环境变量
#### 3. 设置缓存文件夹  C:\windows\Temp  属性可读，完全控制

    "需要先设置好 bundle 目录  下载好 vundle.vim 文件
    set nocompatible              " be iMproved, required
    filetype off                  " required

    " set the runtime path to include Vundle and initialize
    set rtp+=$VIM/gvimfiles/bundle/Vundle.vim
    "call vundle#begin()
    call vundle#begin('$VIM/gvimfiles/bundle/')

    " gvim 配置文件 在 $HOME 新建插件目录
    " 设置缓存文件夹  C:\windows\Temp  属性可读，完全控制
    " 管理员身份打开 gvim ，安装插件
    " set rtp+=$HOME/gvimfiles/bundle/Vundle.vim
    " let path='$HOME/gvimfiles/bundle'
    " call vundle#begin(path)


进入 vim 执行

    :PluginInstall

要卸载插件，先在 .vimrc 中注释或者删除对应插件配置信息，然后在 vim 中执行

    :PluginClean
    

即可删除对应插件。插件更新频率较高，差不多每隔一个月你应该看看哪些插件有推出新版本，批量更新，只需执行

    :PluginUpdate
    

即可。

