# Rime
My own rime setup / 自建中州韵输入引擎输入方案

*2025/11/01：* 已改用 [雾凇拼音](https://github.com/iDvel/rime-ice) + 部分词库，此项目不再适用。存档做历史参考。

## Description
基本上是源于 [huaxianyan/Rime](https://github.com/huaxianyan/Rime) 和 [alswl/Rime](https://github.com/alswl/Rime) 二位的改版，略微调整了一下词库和 Weight。

## 使用方法
1. 安装 [Rime](https://rime.im/) 并使用 [东风破](https://github.com/rime/plum) 安装 [袖珍简化字拼音](https://github.com/rime/rime-pinyin-simp) 方案，修改 用户文件夹中的`default.custom.yaml` 文件加入该方案。
2. 将上述文件复制到 Rime 用户文件夹内。
3. 重新部署。
4. 打开 Rime 方案选单，切换至“简体中文”即可开始使用。

## Dict Description

*是复制来的，仅为介绍用途。*

- `pinyin_simp.custom.yaml` ：袖珍简化字拼音方案的自定义修改，包含初始输出状态、符号输入等功能修改，**同时指定了新词库中心文件**，如果需实现其他功能修改请自行增删。

- `pinyin_simp.main.dict.yaml` ：中心词库文件，主要功能为引用其他词库，需在输入方案中指定方可使用。词库内容为 [袖珍简化字拼音](https://github.com/rime/rime-pinyin-simp) 默认方案词库修改而来，一般不做修改。

- `cn_en.dict.yaml` ：英文及中英混输词库，由中心词库文件引用使用。如需添加新的英文或中英混输词汇，建议编辑此文件。文件内容大部分是纯英文，可以考虑在朙月拼音中使用以方便繁体中文输入场景。

- `pinyin_simp_custom.dict.yaml` ：自定义词语，由中心词库文件引用使用。如需添加自定义短语，建议编辑此文件。

- `pinyin_simp_pin.txt` ：候选固定，使用另一个翻译器并给极高权重来达到固定候选列表的目的，编辑时请记得给极高权重。

  请注意，有时此列表中的字或词在输入时临时组词，将不会录入用户词库。我个人发现此类问题会自行修改自定义词语文件去手动添加，如介意或不需要候选固定请自行修改关闭此功能。
  
- `xiandaihanyuchangyongcibiao.dict.yaml` ：教育部现代汉语常用词表，由中心词库文件引用使用，来源为项目 [https://github.com/alswl/Rime](https://github.com/alswl/Rime)，一般不做修改。
  
- `zhwiki.dict.yaml` ：肥猫词库，由中心词库文件引用使用，来源为项目 [https://github.com/felixonmars/fcitx5-pinyin-zhwiki](https://github.com/felixonmars/fcitx5-pinyin-zhwiki)，一般不做修改。

- `jisuanjicihuidaquan.dict.yaml`：计算机词汇大全（搜狗）

- `chengyusuyu.dict.yaml` 成语俗语（搜狗，40k）

- `emoji.cldr.dict.yaml`：Emoji parsed from [jolicode/emoji-search](https://github.com/jolicode/emoji-search)

## PS
1. plum这个安装逻辑属于是反人类了……每一次执行rime-install都是在执行目录下重新克隆一个plum也太难受，手动把它移到bin目录下还不老实……
2. Rime的自定义输入方案其实很吃个人手感，这里一是为了备份而是提供一些参考，而非开箱即用的选项，自己改改是最合适的；
3. 好吧其实是我用朙月拼音打不出“抬”（擡）才浪费的这一上午折腾输入法……
