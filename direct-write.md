# Direct-Write 解决方案

参考 / Reference：[http://silight.hatenablog.jp/entry/MacTypePatch](http://silight.hatenablog.jp/entry/MacTypePatch)

**(This is an untranslated version, welcome translation)**

## 简介
　　万能的 11 区技术宅终于研究出了修复 Direct Write 渲染效果的黑科技，我在 Insider Preview Build.14393 上试用，表示效果很惊艳。其一是修正了糟糕的字体畸形问题，其二就是启用/增强了灰阶抗锯齿。下方截图是在 Chromium 50 在 1440p 分辨率 150% 缩放下开启 Direct-Write 后的渲染效果：

![放个截图让大家感受一下](https://cloud.githubusercontent.com/assets/2133311/17010686/c5a335d8-4f38-11e6-95db-cae19fa2e7d3.png)

　　实际上渲染效果和原生 MacType 还是有一定的差别的，它更加的细，更接近于 macOS / Unity 的渲染效果。


## 使用方法

1. 先到相关 Repo 获取最新的 Release：[https://github.com/silight-jp/MacType-Patch/releases](https://github.com/silight-jp/MacType-Patch/releases)

2. 解压后，将 `EasyHK32.dll` 和 `EasyHK64.dll` 还有 `win8.1 or later` 文件夹内的 `UserParams.ini` 全部拷贝到 MacType 的程序目录并覆盖同名文件

3. 重启 MacType，开启 Chromium 的 Direct-Write 渲染。

4. 若是没有效果，尝试：

    将 `EasyHK32.dll` 复制到 `C:\Windows\SysWOW64` 目录下

    将 `EasyHK32.dll` 与 `EasyHK64.dll` 复制到 `C:\Windows\System32` 目录下，重启 MacType，测试是否生效。

5. 如果上面所有操作都执行完后还是没有效果，尝试重启系统，或者修改 MacType 的兼容性相关选项。


## 存在问题

1. 不支持 Edge 以及其他 UWP 应用，具体原因不详，按照作者的建议使用注册表模式也没有效果。

2. 在 Office 2016 下没有效果 / 效果不佳

3. Google Chrome 52+ 字体渲染风格有些不同，其实习惯以后还是比较良好的，下面是 Google Chrome 53 在 1440p 分辨率 150% 缩放下的渲染效果：
![Google Chrome 53 显示效果](https://cloud.githubusercontent.com/assets/2133311/17125030/95cf9b7e-5322-11e6-8cd2-b8899dc51427.png)
