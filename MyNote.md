##使用

```
1.修改src/HowToOptimizeGemm/makefile
OLD  := MMult1
NEW  := MMult2
修改这两个配置需要注意，按照顺序依次修改，否则会报错，找不到上一个输出文件。
比如：如果我直接 OLD  := MMult1
               NEW  := MMult2
make run 后，会报错，找不到cp: output_MMult1.m: No such file or directory.
```

```
2.测试MMult_1x4_3.c，需要把MMult_1x4_3.c复制到makefile文件同目录
```

```
3.octave 图示性能数据
1.在命令行中进入到HowToOptimizeGemm目录，输入命令octave
2.进入actave程序，输入PlotAll ,输出：version_new = MMult_1x4_3 ，表示正常
```
