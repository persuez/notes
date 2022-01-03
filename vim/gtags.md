# gtags

```sh
sudo apt install python3-pygments

vim ~/.vimrc
# 新增以下两行
" gtags
let $GTAGSLABEL = 'native-pygments'
```



# LeaderF + gtags

通过 vim-plug 安装 leaderf

```sh
Plug 'Yggdroot/LeaderF', { 'do': ':LeaderfInstallCExtension' }
```

和 gtags 配合

```sh
vim ~/.vimrc

" LeaderF + gtags
" 自动生成 GTAGS 数据库，位置 $HOME/.LfCache/gtags/%PATH%OF%YOUR%PROJECT/
" 在项目根目录下要有 g:Lf_RootMarkers 指定的文件才会自动生成数据库，默认值是 ['.git', '.hg', '.svn']
let g:Lf_GtagsAutoGenerate = 1
" 映射快捷键 
noremap <leader>fr :<C-U><C-R>=printf("Leaderf! gtags -r %s --auto-jump", expand("<cword>"))<CR><CR>
noremap <leader>fd :<C-U><C-R>=printf("Leaderf! gtags -d %s --auto-jump", expand("<cword>"))<CR><CR>
noremap <leader>fo :<C-U><C-R>=printf("Leaderf! gtags --recall %s", "")<CR><CR>
noremap <leader>fn :<C-U><C-R>=printf("Leaderf gtags --next %s", "")<CR><CR>
noremap <leader>fp :<C-U><C-R>=printf("Leaderf gtags --previous %s", "")<CR><CR>
```





