# 什么是 PWA

Google 提出 PWA 的时候，并没有给它一个准确的定义，经过我们的实践和总结，
PWA 它不是特指某一项技术，而是应用多项技术来改善用户体验的 Web App，其核心技术包括 Web App Manifest，Service Worker，Web Push 等，用户体验才是 PWA 的核心。

PWA 主要特点如下：

* 可靠 - 即使在网络不稳定甚至断网的环境下，也能瞬间加载并展现
* 用户体验 - 快速响应，具有平滑的过渡动画及用户操作的反馈
* 用户黏性 - 和 Native App 一样，可以被添加到桌面，能接受离线通知，具有沉浸式的用户体验

PWA 本身强调**渐进式**（Progressive），可以从两个角度来理解渐进式，首先，PWA 还在不断进化，Service Worker，Web App Manifest，Device API 等标准每年都会有不小的进步；其次，标准的设计向下兼容，并且侵入性小，开发者使用新特性代价很小，只需要在原有站点上新增，让站点的用户体验渐进式的增强。

Google 在官网一篇名为《[Progressive Web App Checklist](https://developers.google.cn/web/progressive-web-apps/checklist)》的文章中给出了 PWA 的基准线，也给出了体验更好的示范性 PWA 的 Checklist，下面列出了 PWA 的最低要求。

* 站点需要使用 HTTPS
* 页面需要响应式，能够在平板和移动设备上都具有良好的浏览体验
* 所有的 URL 在断网的情况下有内容展现，不会展现浏览器默认页面
* 需要支持 Wep App Manifest，能被添加到桌面
* 即使在 3G 网络下，页面加载要快，可交互时间要短
* 在主流浏览器下都能正常展现
* 动画要流畅，有用户操作反馈
* 每个页面都有独立的 URL

## PWA 的特性

PWA 本质上还是 Web App，借助了新技术具备了一些 Native App 的特性，所以它兼具 Web App 和 Native App 的优点，同时在安全、体验和用户黏性三个方面都有很大的提升。总结下来，PWA 具有如下特性。

* **渐进式** - 适用于所有浏览器，因为它是以渐进式增强作为宗旨开发的
* **连接无关性** - 能够借助 Service Worker 在离线或者网络较差的情况下正常访问
* **类原生应用** - 由于是在 App Shell 模型基础上开发，因此应具有 Native App 的交互，给用户 Native App 的体验
* **持续更新** - 始终是最新的，无版本和更新问题
* **安全** - 通过 HTTPS 协议提供服务，防止窥探，确保内容不被篡改
* **可索引** - manifest 文件和 Service Worker 可以让搜索引擎索引到，从而将其识别为『应用』
* **黏性** - 通过推送离线通知等，可以让用户回流
* **可安装** - 用户可以添加常用的 Web App 到桌面，免去到应用商店下载的麻烦
* **可链接** - 通过链接即可分享内容，无需下载安装

PWA 的这些新特性给 Web App 注入了活力，而 Native App 却没能很好的弥补自己的劣势。对于 Native App来说，最大的痛点是由于其天生封闭的基因，内容无法被索引，这会导致 Native App 很难被分发，例如，用户想知道红烧肉的做法，还需要先知道应用的名称，下载应用之后才能获取内容，这个流程十分不合理，根据 Google 的统计，用户每个月安装的应用个数约等于 0，再加上用户 80% 的时间被 Top3 的超级应用占据，应用分发成本也因此越来越高。相对于 Native App 的封闭，PWA 完全是开放的，PWA 的所有技术都是遵循开放的标准，因此能够被浏览器快速支持，被开发者接受。

下表列出了传统 Web App，Native App 和 PWA 在各特性的对比。

|   |是否可安装|是否可链接访问|用户体验|用户黏性|
|---|---|---|---|---|
|传统 Web|无法安装|可链接访问|体验一般|黏性差|
|Native App|可安装|不可链接访问|体验好|黏性强|
|PWA|可安装|可链接访问|体验好|黏性强|

PWA 能给站点体验带来飞跃式的提升，我们可以用移动设备上的浏览器，如 Chrome， 访问 [LAVAS 官网](https://lavas.baidu.com) 体验一下，并添加到桌面，还可以在断网的情况下使用。现在在国内也有很多 PWA 站点，比如饿了么和新浪微博的移动版，不用耗费流量下载几十兆的应用，就能有和原生应用一样的体验，不妨尝试一下。

在后面的章节中，我们会从体验、安全和性能三个角度来分析如何打造一个好的 PWA。
