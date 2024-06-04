# 设置python全局http代理
由于raw.githubusercontent.com被ban，从它上面访问资源就必须使用代理。

而我买的代理是http代理，不是网卡全局代理，所以，python脚本发起的访问不走代理。

于是需要手动设置。
```python
from datasets import load_dataset

dataset = load_dataset("conll2003")
```
这里是无论如何都没法下载的。


必须手动设置socket。

```python
import socket
import socks
socks.set_default_proxy(socks.SOCKS5, "127.0.0.1", 7890)
socket.socket = socks.socksocket

from datasets import load_dataset
dataset = load_dataset("conll2003")
```

从此，huggingface和spacy的所有内容我都可以使用啦！！！