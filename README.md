# ABuildImmortalWrt
[![GitHub](https://img.shields.io/github/license/wukongdaily/AutoBuildImmortalWrt.svg?label=LICENSE&logo=github&logoColor=%20)](https://github.com/wukongdaily/AutoBuildImmortalWrt/blob/master/LICENSE)
![GitHub Stars](https://img.shields.io/github/stars/wukongdaily/AutoBuildImmortalWrt.svg?style=flat&logo=appveyor&label=Stars&logo=github)
![GitHub Forks](https://img.shields.io/github/forks/wukongdaily/AutoBuildImmortalWrt.svg?style=flat&logo=appveyor&label=Forks&logo=github) [![Github](https://img.shields.io/badge/RELEASE:AutoBuildImmortalWrt-123456?logo=github&logoColor=fff&labelColor=green&style=flat)](https://github.com/wukongdaily/AutoBuildImmortalWrt/releases) [![Bilibili](https://img.shields.io/badge/Bilibili-123456?logo=bilibili&logoColor=fff&labelColor=fb7299)](https://www.bilibili.com/video/BV1EG6VYCER3) [![操作步骤](https://img.shields.io/badge/YouTube-123456?logo=youtube&labelColor=ff0000)](https://youtu.be/xIVtUwZR6U0)

## 🤔 这是什么？
它是一个工作流。可快速构建 带docker且支持自定义固件大小的 immortalWrt
> 1、支持自定义固件大小 默认1GB <br>
> 2、支持预安装docker（可选）<br>
> 3、目前支持x86-64 和 rockchip 两个平台（后续会增加）<br>
> 4、新增支持MT3000/MT2500/MT6000（docker可选）<br>
> 5、新增全志平台R1S、香橙派Zero3等机型的工作流<br>
> 6、rockchip平台支持批量编译 使用逗号分隔机型<br>
> 7、新增树莓派①②③④⑤<br>
## 如何查询都有哪些插件?
https://mirrors.sjtug.sjtu.edu.cn/immortalwrt/releases/23.05.4/packages/aarch64_cortex-a53/luci/ <br>
https://mirrors.sjtug.sjtu.edu.cn/immortalwrt/releases/23.05.4/packages/x86_64/luci/ 

## 该固件默认属性？(必读)
- 该固件刷入单网口设备默认采用DHCP模式,自动获得ip。类似NAS的做法
- 该固件刷入多网口设备默认WAN口采用DHCP模式，LAN 口ip为 192.168.100.1
- 综合上述特点，单网口应该先接路由器，先在路由器查看一下它的ip 再访问。
- 上述特点 你都可以通过 `99-custom.sh` 配置和调整

## ❤️其它GitHub Action项目推荐🌟 （建议收藏）⬇️
https://github.com/wukongdaily/RunFilesBuilder<br>
https://github.com/wukongdaily/DockerTarBuilder

## 常见问题

### 编译正常,上传`releases`失败
#### 问题 介绍
一般在 `Create GitHub Release Info` 这个环节 出问题 , 下面有 错误 信息
```log
Run softprops/action-gh-release@v2.1.0
  with:
    tag_name: Autobuild-x86-64
    name: ImmortWrt-24.10-x86-64-efi 2025年01月08日-06时28分
    body_path: /home/runner/work/ABuildImmortalWrt/ABuildImmortalWrt/info.md
    draft: false
    prerelease: false
    token: ***
  env:
    current_date: 2025年01月08日-06时28分
    GITHUB_TOKEN: ***
👩‍🏭 Creating new GitHub release for tag Autobuild-x86-64...
⚠️ GitHub release failed with status: 403
{"message":"Resource not accessible by integration","documentation_url":"https://docs.github.com/rest/releases/releases#create-a-release","status":"403"}
Skip retry — your GitHub token/PAT does not have the required permission to create a release
Error: Resource not accessible by integration - https://docs.github.com/rest/releases/releases#create-a-release
```
#### 问题 解决
项目不同 解决方法的地址也不同 根据 `[]` 中的 信息进行填写 然后访问
```shell
https://github.com/[github用户名]/[github项目名称]]/settings/actions
```

进入网站和 就是 项目设置中的 `actions` 

然后 找到  `Workflow permissions` 

![img.png](images/Issue_1.png)

根据图片进行设置就好了

# 🌟鸣谢
### https://github.com/immortalwrt
### ![AutoBuildImmortalWrt](https://github.com/wukongdaily/AutoBuildImmortalWrt)
