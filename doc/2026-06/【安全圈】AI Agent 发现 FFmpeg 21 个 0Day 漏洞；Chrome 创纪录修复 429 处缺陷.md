#  【安全圈】AI Agent 发现 FFmpeg 21 个 0Day 漏洞；Chrome 创纪录修复 429 处缺陷  
 安全圈   2026-06-07 11:00  
  
![](https://mmbiz.qpic.cn/sz_mmbiz_png/aBHpjnrGylgOvEXHviaXu1fO2nLov9bZ055v7s8F6w1DD1I0bx2h3zaOx0Mibd5CngBwwj2nTeEbupw7xpBsx27Q/640?wx_fmt=other&from=appmsg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1 "")  
  
  
**关键词**  
  
  
  
漏洞  
  
  
![image](https://mmbiz.qpic.cn/sz_mmbiz_jpg/sbq02iadgfyHDsqY8oyxicUmme8KRZFl6rBpJarByNuibRhiapLicB6uORv0EM5OrtOAiaSoQhJuxRsD4f5Rg89WkWG3GQJrFiaO8mMMTtjgqMQtKU/640?wx_fmt=jpeg&from=appmsg "")  
  
本周接连发生两起重大安全事件。一家安全初创公司报告了 FFmpeg 媒体库中 21 个此前未知的漏洞，这些几乎存在于所有视频处理软件中的组件，其漏洞均由自主 AI Agent 发现。同一周，谷歌发布了 Chrome 149 版本，修复了创纪录的 429 个安全缺陷。  
## AI 驱动的漏洞挖掘  
  
FFmpeg 漏洞由深度优先（depthfirst）公司的自主安全 Agent 发现，该工具扫描了该项目约 150 万行 C 代码，最终确认了 21 个 0Day 漏洞，每个漏洞都附有可复现的 PoC。该公司表示此次扫描成本约为 q,000 美元。部分漏洞已潜伏 15 至 20 年，其中服务描述表代码中的栈溢出漏洞可追溯至 2003 年，存在时间长达 23 年。  
  
这些漏洞主要存在于解析器和解复用器中，涉及从 TS 解复用器到 VP9 解码器等多个组件。其中部分漏洞已获得 CVE 编号（CVE-2026-39210 至 CVE-2026-39218），其余漏洞虽已修复但尚未分配编号。该公司同时公开了相关 PoC。  
## Chrome 创纪录更新  
  
Chrome 149 版本修复的 429 个漏洞中，超过 100 个属于高危或严重级别，主要为释放后使用和输入验证不足类漏洞。其中最严重的 ANGLE 图形引擎越界读写漏洞（CVE-2026-10881，CVSS 9.6）可使恶意页面突破沙箱在主机执行代码，谷歌为此支付了 97,000 美元赏金。  
  
值得注意的是，约 90 个高危漏洞中仅 10 个来自外部研究人员，22 个严重漏洞中有 19 个由谷歌内部发现。虽然 AI 并非直接发现者，但其产生的海量报告促使谷歌在四月调整了漏洞赏金计划，要求提交简洁的复现步骤而非冗长报告。  
## 自动化工具崛起  
  
此前谷歌 Big Sleep Agent 曾发现一系列 FFmpeg 漏洞（标记为 BIGSLEEP），Anthropic 的 Mythos 模型也以约 q0,000 美元成本发现存在 16 年的 H.264 漏洞，其中三个已在 FFmpeg 8.1 中修复。近日另有自动化工具发现 Redis 自 7.2.0 版本起存在的认证远程代码执行漏洞，该漏洞潜伏超过两年未被察觉。  
## 紧急应对建议  
  
对于 FFmpeg 用户：  
- 立即获取上游修复版本或发行版安全更新  
  
- 优先处理涉及不可信 RTSP 或 AV1-over-RTP 的组件  
  
- 注意检查媒体处理管道、Python 包、容器镜像和设备固件中的嵌入式副本  
  
对于 Chrome 用户：  
- Linux 平台更新至 149.0.7827.53  
  
- Windows/macOS 平台更新至 149.0.7827.53/54  
  
- 确认自动更新已生效  
  
安全响应正面临新挑战：补丁周期缩短、自动更新普及、包含 CVE 修复的依赖项升级需视为安全任务。虽然漏洞发现成本降低，但报告分类、修复发布和部署安装的成本仍未减少，这些工作仍主要依赖志愿者和有限的人工分类员——他们现在需要与机器保持同步。  
  
  
  END    
  
  
阅读推荐  
  
  
[【安全圈】深夜，黑客潜入发薪后台！常州武进检察破获特大网络“金库”盗窃案](https://mp.weixin.qq.com/s?__biz=MzIzMzE4NDU1OQ==&mid=2652077275&idx=1&sn=4349cddd664a923edc74b9180a8a6d6d&scene=21#wechat_redirect)  
  
  
  
[【安全圈】黑客借山寨 Gemini、Claude 网站散播木马](https://mp.weixin.qq.com/s?__biz=MzIzMzE4NDU1OQ==&mid=2652077275&idx=2&sn=fa510bf0e0cb6b9eff54426e5f843e70&scene=21#wechat_redirect)  
  
  
  
[【安全圈】《GTA 5》外挂服务商遭黑客入侵，近 6.4 万玩家信息泄露](https://mp.weixin.qq.com/s?__biz=MzIzMzE4NDU1OQ==&mid=2652077275&idx=3&sn=bba6752e35480d1f014b0cef66eb7dd7&scene=21#wechat_redirect)  
  
  
  
[【安全圈】WeedHack 恶意木马曝光，专针对《我的世界》玩家发起攻击](https://mp.weixin.qq.com/s?__biz=MzIzMzE4NDU1OQ==&mid=2652077261&idx=1&sn=8411ab957afc2b4e41af24e6da821584&scene=21#wechat_redirect)  
  
  
  
  
![](https://mmbiz.qpic.cn/mmbiz_gif/aBHpjnrGylgeVsVlL5y1RPJfUdozNyCEft6M27yliapIdNjlcdMaZ4UR4XxnQprGlCg8NH2Hz5Oib5aPIOiaqUicDQ/640?wx_fmt=gif "")  
  
  
  
![](https://mmbiz.qpic.cn/mmbiz_png/aBHpjnrGylgeVsVlL5y1RPJfUdozNyCEDQIyPYpjfp0XDaaKjeaU6YdFae1iagIvFmFb4djeiahnUy2jBnxkMbaw/640?wx_fmt=png "")  
  
**安全圈**  
  
![](https://mmbiz.qpic.cn/mmbiz_gif/aBHpjnrGylgeVsVlL5y1RPJfUdozNyCEft6M27yliapIdNjlcdMaZ4UR4XxnQprGlCg8NH2Hz5Oib5aPIOiaqUicDQ/640?wx_fmt=gif "")  
  
  
←扫码关注我们  
  
**网罗圈内热点 专注网络安全**  
  
**实时资讯一手掌握！**  
  
  
![](https://mmbiz.qpic.cn/mmbiz_gif/aBHpjnrGylgeVsVlL5y1RPJfUdozNyCE3vpzhuku5s1qibibQjHnY68iciaIGB4zYw1Zbl05GQ3H4hadeLdBpQ9wEA/640?wx_fmt=gif "")  
  
**好看你就分享 有用就点个赞**  
  
**支持「****安全圈」就点个三连吧！**  
  
![](https://mmbiz.qpic.cn/mmbiz_gif/aBHpjnrGylgeVsVlL5y1RPJfUdozNyCE3vpzhuku5s1qibibQjHnY68iciaIGB4zYw1Zbl05GQ3H4hadeLdBpQ9wEA/640?wx_fmt=gif "")  
  
  
