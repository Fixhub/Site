title: Fixhub 0.2.1 发布， 基于 Laravel 5.5 开发的开源 Web 自动部署系统
---
首先提前祝大家中秋和国庆快乐。言归正传，Fixhub 是一款基于PHP Laravel 5.5框架开发的开源Web自动化部署系统。一年前，我在Laravel china发布了Fixhub第一版，请看链接： <https://laravel-china.org/topics/2722/fixhub-an-open-source-web-based-on-the-latest-version-of-laravel-53-automatic-deployment-system> 当时收获了很多来自这里的Github star。后来由于操作不慎，我把Fixhub的github仓库删除过一次，相当于star又重新归零，重新上路又收获了200+star。在此感谢Laravel china官方和网友对Fixhub的厚爱。

Fixhub一直是我们团队内部使用的部署系统(我们通过自托管的Gitlab和Fixhub进行无缝集成，完全实现了自动化部署)。

最近我对Fixhub的功能和程序结构方面做了一些更新，也把Laravel从5.3升级到了5.5。

## 近期更新内容
: +1 :
新功能:

- 实现多环境部署功能，项目和部署模板里都可以设置多个部署环境
- 集成OAuth2.0平台接入商，可通过后台进行管理
- 实现找回密码、新用户账号开通邮件通知功能
- 新增hooks功能，可实现Slack、邮件和Webhook等第三方服务的集成
- 新增项目分组的详情页
- 在管理后台首页显示相关环境变量和组件信息

改进:

- 重构Notification机制
- 优化部署详情页，明显区分内置步骤和自定义步骤
- Gravatar功能可进行关闭
- 新增 端砚黑 主题
- 清理issues、nofitySlacks和notifyEmails相关文件
- 将Laravel框架从5.3升级到5.5
- 优化API路由结构
- 升级dotenv、ioredis、socket.io等组件
- 在部署详情页，将内置部署步骤与手动设置的前、后置任务区分显示
- 简化部署步骤模板页，调整显示方式，可以更直观地分辨前置、当前、后置任务的执行顺序
- 调整部分icon

Bug修复:

- 修复JS内语言不一致的bug
- 修复部署模板页面的ace报错
- 修复表单可重复提交的bug
- 修复编辑项目时会报模板错误的bug
- 修复CI过程中的CS检查warning

以下是一些简单的系统截图：

一、部署环境
以往我们内部靠建多个项目达到多环境部署
{% asset_img 1.png %}
现在更方便了，在同一个项目创建多个环境即可
{% asset_img 2.png %}
{% asset_img 3.png %}
同样的，部署模板也支持多环境设置
{% asset_img 4.png %}

二、部署操作
创建上线单，可部署到多个环境
{% asset_img 5.png %}
上线单可以非常清楚地看到所部署的环境
{% asset_img 6.png %}
三、社交平台接入
后台管理
{% asset_img 7.png %}
登录页
{% asset_img 8.png %}



演示地址：<http://fixhub.org/> 感兴趣的朋友可以使用自己的Github账号或者我们提供的演示账号登录体验。
我们的演示账号信息如下：
用户名：fixhub
密码：fixhub