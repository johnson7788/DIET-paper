# DIET: 对话系统的轻量级语言理解模型

论文 [paper](https://arxiv.org/pdf/2004.09936.pdf) 
"DIET: Lightweight Language Understanding for Dialogue Systems".

为了重现实验结果，请执行以下步骤

(1) 使用Rasa进行试验
clone rasa代码，checkout diet-paper 分支， 然后安装rasa

```bash
# clone the repository and checkout 'diet-paper' branch
git clone https://github.com/RasaHQ/rasa
cd rasa
git checkout diet-paper
# installation
curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python3
make install-full
```

(2)执行“run.sh”脚本进行训练和测试, 使用的数据是在ATIS，SNIPS和NLU。按论文中的表的名字作为参数产生结果，考虑在具有GPU的计算机上执行以加快实验速度。

```bash
./run.sh [table-1|table-2|table-3|table-4|table-5]
```

(3) 试验结果在 `experiments`文件夹下

要测试其他特性或超参数，请更新“ configs”文件夹中的配置文件。其中可以找到可用的特征化组件和可用的超参数列表。
[here](https://rasa.com/docs/rasa/nlu/components/).
