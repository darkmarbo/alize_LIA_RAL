# alize_LIA_RAL
alize 的 LIA_RAL 部分。官网下载版本： http://mistral.univ-avignon.fr/#contribute

1.安装 automake 
    yum install automake
        which aclocal, autoconf, automake  已经存在 

2.运行  aclocal
    会生成  aclocal.m4 和 autom4te.cache

3.运行  automake
    更新或者生成文件如下:
        Makefile.in
        LIA_Utils
        LIA_SpkTools
        LIA_SpkSeg
        LIA_SpkDet

    log信息如下:
        automake: warning: autoconf input should be named 'configure.ac', not 'configure.in'
        configure.in:2: warning: AM_INIT_AUTOMAKE: two- and three-arguments forms are deprecated.  For more info, see:
        configure.in:2: http://www.gnu.org/software/automake/manual/automake.html#Modernize-AM_005fINIT_005fAUTOMAKE-invocation
        automake: warning: autoconf input should be named 'configure.ac', not 'configure.in'

4.运行  autoconf
    生成  configure 文件

5.准备  alize_core中构建出lib     /home/szm/cd/alize-core/alize-core/lib/libalize_Linux_x86_64.a 


6.运行   ./configure --with-alize=/home/szm/cd/alize-core/alize-core

        ATTENTION by default alize lib is search in ../ALIZE. 
        You can specify the ABSOLUTE path if different by using the --with-alize=ABSOUTE_PATH option.

创建目录: 用于存放最终结果  
    mkdir lib bin  

7.运行   make

结果:
    bin 目录下  36 个工具 
