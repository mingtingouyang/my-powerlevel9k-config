# my-powerlevel9k-config
个人备份用，有兴趣的也可以拷贝走～

## 1  mac.bak.zshrc
环境：

1. zsh + [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)
2. 字体：[nerd-fonts](https://github.com/ryanoasis/nerd-fonts)
3. 主题：[Powerlevel9k](https://github.com/Powerlevel9k/powerlevel9k)
4. Mac os

预览图：

![mac p9k](https://github.com/mingtingouyang/my-powerlevel9k-config/blob/master/pic/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-08-28%2000.59.30.png)

## 2 linux.bak.zshrc
环境：

1. zsh + [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)
2. 字体：[nerd-fonts](https://github.com/ryanoasis/nerd-fonts)
3. 主题：[Powerlevel9k](https://github.com/Powerlevel9k/powerlevel9k)
4. Ubuntu 18.04.3 LTS + KDE

预览图：

![linux p9k](https://github.com/mingtingouyang/my-powerlevel9k-config/blob/master/pic/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE.png)

## 3 环境安装
### 3.1 oh-my-zsh
在安装好 zsh 后（ubuntu 可以直接用 apt-get 安装，mac os 自带 zsh），使用如下命令安装 oh-my-zsh 配置：

```shell
sh -c "$(wget -O- https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

脚本执行过程中问询问是否将 zsh 设置为默认 shell，输入 "y" 即可。

### 3.2 nerd-fonts
需要用 git 先克隆到本地，再用脚本安装。官方的 git 下载比较慢，建议挂梯子后再进行 clone，整个包有接近 1G。

```shell
git clone https://github.com/ryanoasis/nerd-fonts.git --depth 1
cd nerd-fonts 
./install.sh
cd ..
rm -rf nerd-fonts
```

安装完后，终端客户端需要选择名字带 nerd fonts 的字体。

### 3.3 powerlevel9k
powerlevel9k 是 zsh 的一个主题，安装方法也非常简单，一条命令即可，直接用 git 将包克隆到默认的 zsh 主题目录

```shell
 git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k
```

然后修改 `~/.zshrc` 文件更换主题，以及指定字体。

```
# 修改
ZSH_THEME="powerlevel9k/powerlevel9k"

# 添加
POWERLEVEL9K_MODE='nerdfont-complete'
```
