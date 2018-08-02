代码补全插件，下载后，直接在vim73安装目录解压，会自动覆盖
http://www.vim.org/scripts/script.php?script_id=2540

 E576: viminfo: Missing '>' in line: 
这种错误，是因为操作历史里面有语法错误，去删除或修改~/.viminfo文件就可以解决
 

20171011 解决鼠标中键粘贴以后的vimrc文件

set nocompatible
source $VIMRUNTIME/vimrc_example.vim
source $VIMRUNTIME/mswin.vim
behave mswin

set diffexpr=MyDiff()
function MyDiff()
  let opt = '-a --binary '
  if &diffopt =~ 'icase' | let opt = opt . '-i ' | endif
  if &diffopt =~ 'iwhite' | let opt = opt . '-b ' | endif
  let arg1 = v:fname_in
  if arg1 =~ ' ' | let arg1 = '"' . arg1 . '"' | endif
  let arg2 = v:fname_new
  if arg2 =~ ' ' | let arg2 = '"' . arg2 . '"' | endif
  let arg3 = v:fname_out
  if arg3 =~ ' ' | let arg3 = '"' . arg3 . '"' | endif
  let eq = ''
  if $VIMRUNTIME =~ ' '
    if &sh =~ '\<cmd'
      let cmd = '""' . $VIMRUNTIME . '\diff"'
      let eq = '"'
    else
      let cmd = substitute($VIMRUNTIME, ' ', '" ', '') . '\diff"'
    endif
  else
    let cmd = $VIMRUNTIME . '\diff'
  endif
  silent execute '!' . cmd . ' ' . opt . arg1 . ' ' . arg2 . ' > ' . arg3 . eq
endfunction

set tags=tags
set autochdir
" without BOM 
set nobomb

set expandtab


filetype plugin indent on
set completeopt=longest,menu
let g:SuperTabRetainCompletionType=2
let g:SuperTabDefaultCompletionType="<C-X><C-O>"
:inoremap ( ()<ESC>i
:inoremap ) <c-r>=ClosePair(')')<CR>
:inoremap { {}<ESC>i
:inoremap } <c-r>=ClosePair('}')<CR>
:inoremap [ []<ESC>i
:inoremap ] <c-r>=ClosePair(']')<CR>
:inoremap < <><ESC>i
:inoremap > <c-r>=ClosePair('>')<CR>

function ClosePair(char)
    if getline('.')[col('.') - 1] == a:char
        return "\<Right>"
    else
        return a:char
    endif
endfunction

autocmd FileType javascript set omnifunc=javascriptcomplete#CompleteJS
autocmd FileType c set omnifunc=ccomplete#Complete
autocmd FileType css set omnifunc=csscomplete#CompleteCSS
autocmd FileType html set omnifunc=htmlcomplete#CompleteTags 
autocmd FileType php set omnifunc=phpcomplete#CompletePHP
autocmd FileType make set noexpandtab
autocmd FileType python set omnifunc=pythoncomplete#Complete
autocmd FileType xml set omnifunc=xmlcomplete#CompleteTags

set spell 

"let g:SuperTabMappingForward = '<tab>'


set tabstop=4
set softtabstop=4
set shiftwidth=4
set autoindent
"set cindent
set nu
set nobackup
set fileencodings=utf-8,gb2312,gbk,gb18030,big5
set fenc=utf-8
"set enc=utf-8
set guifont=Consolas:h12:cANSI

map <MiddleMouse> <F7><ESC>i
imap <MiddleMouse> <ESC>i


Vimrc文件结束
