# DLAIModelCards

随着ChatGPT的发布，AI技术带来的想象空间被打开。各种大模型也开始加速发展。为了更好地追踪各个模型的发展情况，建立本档案库，希望大家可以一起贡献关于全球发布的大模型信息，以便所有人可以更加容易清楚地追踪AI大模型的更新。

部分模型的内容使用`gpt-3.5-turbo`接口从模型介绍页面获取。使用的Prompt如下：

```
prompt = f"""
Your task is to extract AI model information from a model description text.

Extract the model information provided in the technical specifications delimited by 
triple backticks.

Show the model infomation with markdown table format. You need to show the model name, model type, parameter size, code opensource license, checkpoints opensource license, the base model. If no information provided, use empty string to replace.

Note that the model type should be filled by the following rules:
If the model is a language model which do not use any finetuned techniques, then this is a base language model.
If the model is finetuned for chat, then the model is chat-finetuned.
If the model is finetuned by instruction data, then the model is instruction-finetuned.
If the model is optimzied for coding, then the model is coding-finetuned.

Technical specifications: ```{input_text}```
"""
```
其中，`input_text`就是从模型页面拷贝的内容。因此，部分模型信息可能有误，也欢迎大家提出issue。

本文档中的`model_cards.md`文档将记录所有模型的概要信息，并在`model_info`目录下以表格的形式记录每一个模型的详细信息，欢迎大家一起贡献！
