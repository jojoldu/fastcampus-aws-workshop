# 패스트캠퍼스 AWS 운영 서버 관리 마스터 워크샵

매주 토요일 오후 2 ~ 6시까지 AWS 워크샵

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
:set number
:set et
:set ts=2
:set shiftwidth=4
:set autoindent
:set smartindent
:set paste
:syntax on
:au BufRead,BufNewFile *.conf set ft=nginx
:set fileencodings=utf-8

# 저장
:wq

# Nginx highlight 추가
mkdir -p ~/.vim/syntax/
cd ~/.vim/syntax/
wget https://gist.githubusercontent.com/jadeno/368c04bf61a1eb858d3774e25f2085fc/raw/30527f399bbf31cfb902b3fdd4eb024f901b30db/nginx.vim
# bash shell script 리로드
source ~/.bashrc
```
