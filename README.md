# 패스트캠퍼스 AWS 운영 서버 관리 마스터 워크샵

매주 토요일 오후 2 ~ 6시까지 AWS 워크샵

## 과정

* [1주차 - 운영서버 구성하기](./1주차.md)
 
## 개발환경 세팅

VIM Syntax highlighting

```bash
# vim alias 설정
vi ~/.bashrc
# 다음 내용 입력
alias vi='vim'

# 저장
:wq

# vimrc 설정
vi ~/.vimrc
# 다음 내용 입력
set hlsearch " 검색어 하이라이팅
set nu " 줄번호
set autoindent " 자동 들여쓰기
set scrolloff=2
set wildmode=longest,list
set ts=4 "tag select
set sts=4 "st select
set sw=1 " 스크롤바 너비
set autowrite " 다른 파일로 넘어갈 때 자동 저장
set autoread " 작업 중인 파일 외부에서 변경됬을 경우 자동으로 불러옴
set cindent " C언어 자동 들여쓰기
set bs=eol,start,indent
set history=256
set laststatus=2 " 상태바 표시 항상
"set paste " 붙여넣기 계단현상 없애기
set shiftwidth=4 " 자동 들여쓰기 너비 설정
set showmatch " 일치하는 괄호 하이라이팅
set smartcase " 검색시 대소문자 구별
set smarttab
set smartindent
set softtabstop=4
set tabstop=4
set ruler " 현재 커서 위치 표시
set incsearch
set statusline=\ %<%l:%v\ [%P]%=%a\ %h%m%r\ %F\
" 마지막으로 수정된 곳에 커서를 위치함
au BufReadPost *
\ if line("'\"") > 0 && line("'\"") <= line("$") |
\ exe "norm g`\"" |
\ endif
" Nginx Syntax Highlight
:au BufRead,BufNewFile *.conf set ft=nginx
" 파일 인코딩을 UTF-8
:set fileencodings=utf-8
" 구문 강조 사용
if has("syntax")
 syntax on
endif

# 저장
:wq

# Nginx highlight 추가
mkdir -p ~/.vim/syntax/
cd ~/.vim/syntax/
wget https://gist.githubusercontent.com/jadeno/368c04bf61a1eb858d3774e25f2085fc/raw/30527f399bbf31cfb902b3fdd4eb024f901b30db/nginx.vim
# bash shell script 리로드
source ~/.bashrc
```
