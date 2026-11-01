# MetaCode · Discord 加好友客户端（dc-auto）

> Windows 桌面客户端，配合 [MetaCode 网站](https://metacode.top/data/discord) 使用：在网站上配置好 Discord 账号和要添加的好友名单，客户端连接后自动批量发送好友请求。
>
> *English: a Windows desktop client for [MetaCode](https://metacode.top/data/discord). Configure your Discord accounts and friend list on the website, then this client connects with an API Key and sends friend requests automatically. Download the `.exe` from [Releases](../../releases).*

本仓库只发布打包好的程序，不包含源码。

## 下载

到 [**Releases**](../../releases) 页面，下载最新版本里的 `.exe` 文件，双击即可运行，无需安装 Python。

## 运行条件

- Windows 10 / 11
- 电脑上已安装 **Discord 桌面版**，并且能正常访问 Discord
- MetaCode 网站账号（钱包）已被开通「Discord 自动化」权限，没有开通请联系我们
- 一个 **API Key**（在网站上生成，见下）

## 快速开始

1. 打开 [MetaCode · Discord 自动化](https://metacode.top/data/discord)，连接钱包登录。
2. 在 **账号库** 里添加 Discord 账号：账号名、邮箱、密码、两步验证（2FA）密钥，三项缺一不可。
3. 新建一个 **任务**，进入任务，把账号分配给它。
4. 在任务的 **好友池** 里批量添加要加的好友（Discord 用户名，一行一个）。
5. 在 **API Key** 里点「生成新 Key」。**Key 只显示一次**，请立即复制保存。
6. 打开本客户端，粘贴 API Key，点「连接」。
7. 在「任务」下拉里选择要运行的任务，设置账号切换间隔，点「开始运行」。

每个账号跑完会标记为「已跑」，下次运行同一任务会自动跳过；想重新跑一遍，到网站的任务页点「重置本轮」。
更详细的图文步骤见网站页面右上角的「加好友使用说明」。

## 常见问题

**一个 API Key 能在几台电脑上用？**
默认只能绑定 1 台，首次运行成功后就固定在那台电脑上。需要更多请联系我们，或在网站「API Key」里删掉旧 Key 重新生成。

**提示「需要更新客户端」？**
版本过旧时服务器会拒绝连接，请到 Releases 下载最新版本。

**账号在列表里显示「失效」？**
说明该账号登录失败，请检查网站上保存的密码和 2FA 密钥是否正确，修改后重新运行。

**运行时我需要做什么？**
保持客户端开着，不要手动去操作被自动化控制的 Discord 窗口。

**杀毒软件报毒 / Windows 提示「已保护你的电脑」？**
本程序是用 PyInstaller 打包的单文件程序，又会启动并控制 Discord，部分杀毒软件和 Windows SmartScreen 会误报。
请只从本仓库的 Releases 下载，核对 Release 说明里的 SHA-256 校验值；确认无误后可在杀毒软件中添加信任，SmartScreen 点「更多信息 → 仍要运行」。

## 注意事项

- 本工具使用你提供的 Discord 账号密码自动登录，**建议使用小号**，并妥善保管账号信息。
- 加好友不要过于频繁，账号切换间隔和每个账号的发送数量请循序渐进，以免触发 Discord 的风控限制。
- 自动化操作可能违反 Discord 的服务条款，由此造成的账号限制或封禁，需要你自行承担。

## 联系我们

使用中遇到问题，请通过 [MetaCode 网站](https://metacode.top) 上的联系方式找到我们。
