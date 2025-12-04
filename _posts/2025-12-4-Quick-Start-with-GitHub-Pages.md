---
layout: post
title: Quick Start with GitHub Pages!
---


**GitHub Pages 个人博客搭建记录**


**系统环境版本：**
1. macOs Big Sur 11.2.3
2. Command Line Tools for Xcode 12.5
3. zsh 5.8 (x86_64-apple-darwin20.0)
4. rbenv 1.3.2
5. ruby 3.3.10 (2025-10-23 revision 343ea05002) [x86_64-darwin20]
6. gem jekyll 4.4.1
7. gem bundler 4.0.0
8. gem github-pages 232


**大体流程：**
1. 新建 ``<username>.github.io`` 存储库；
2. 在 ``设置`` & ``代码和自动化`` 等部署发布 GitHub Pages 网站；
3. 使用 Jekyll 向 GitHub Pages 站点添加内容


**1~2 见 [GitHub Pages 快速入门](https://docs.github.com/zh/pages/quickstart)**


**安装 Jekyll 主要步骤：**
1. macOs 内置 ``/usr/bin/ruby`` 2.6.3p62 版本过低；导致 jekyll & bundler 安装失败；
    ```
    sudo gem install jekyll bundler --source https://mirror.tuna.tsinghua.edu.cn/rubygems/
    ---
    ERROR:  Error installing jekyll:
        The last version of rouge (>= 3.0, < 5.0) to support your Ruby & RubyGems was 3.30.0. Try installing it with `gem install rouge -v 3.30.0` and then running the current command again
        rouge requires Ruby version >= 2.7. The current ruby version is 2.6.3.62.
    ERROR:  Error installing bundler:
        The last version of bundler (>= 0) to support your Ruby & RubyGems was 2.4.22. Try installing it with `gem install bundler -v 2.4.22`
        bundler requires Ruby version >= 3.2.0. The current ruby version is 2.6.3.62.
    ```
2. 因为 macOs 内置 ruby；所以 先安装 ``rbenv`` ruby env；再安装 ruby 3.3.10；又失败；
    ```
    brew install rbenv ruby-build
    ---
    Warning: You are using macOS 11.
    We (and Apple) do not provide support for this old version.
    You may have better luck with MacPorts which supports older versions of macOS:
    https://www.macports.org

    This is a Tier 3 configuration:
    https://docs.brew.sh/Support-Tiers#tier-3
    You can report Tier 3 unrelated issues to Homebrew/* repositories!
    Read the above document before opening any issues or PRs.

    ==> Installing dependencies for rbenv: m4, autoconf, ca-certificates, openssl@3, pkgconf, readline and ruby-build
    ==> Installing rbenv dependency: m4
    Error: Your Command Line Tools are too outdated.
    Update them from Software Update in System Preferences.

    If that doesn't show you any updates, run:
    sudo rm -rf /Library/Developer/CommandLineTools
    sudo xcode-select --install

    Alternatively, manually download them from:
    https://developer.apple.com/download/all/.
    You should download the Command Line Tools for Xcode 13.2.1.
    ```
3. 在 macOs ``系统偏好设置`` & ``软件更新`` 更新 Command Line Tools；
4. 通过 rbenv 安装 ruby；
    ```
    rbenv install -l
    rbenv install 3.3.10
    rbenv versions
        * system
        3.3.10

    rbenv global 3.3.10
    echo 'eval "$(rbenv init - zsh)"' >> ~/.zshrc
    ```
5. 通过 gem 安装 jekyll & bundler & github-pages；
    ```
    gem sources -l
        *** CURRENT SOURCES ***

        https://rubygems.org/
        https://mirrors.aliyun.com/rubygems/

    gem sources --add https://mirrors.aliyun.com/rubygems/

    gem install github-pages
        sass's executable "sass" conflicts with sass-embedded
        Overwrite the executable? [yN]  ERROR:  Error installing github-pages:
            "sass" from sass conflicts with installed executable from sass-embedded

    gem install github-pages --force
    ```


**``使用 Jekyll 向 GitHub Pages 站点添加内容`` 见 [Jekyll Now](https://github.com/barryclark/jekyll-now/)**

``Jekyll Now`` 上一次 commit 还是 2016；``README.md`` 也提到了 Jekyll 3 兼容性；现在已是 Jekyll 4；

    ```
    March, 2016: If you're on an old version of Jekyll Now and run into a) build warnings or b) syntax highlighting issues caused by Jekyll 3 and GitHub Pages updates, just ✨update your _config.yml✨ and you'll be set!
    ```

但是因为 [姚顺雨 GitHub Pages](https://ysymyth.github.io/) 与 ``Disqus commenting`` 特性；先这样；

以后看如何接入 GitHub 与微博等国内社媒平台；


**其他：**
1. 在印象里，仓库可见性必须是``public``；
2. GitHub Pages 自定义域名；无域名；未尝试；似乎与 ``DNS 提供商`` & ``CNAME`` 有关；
3. 免费域名存在域名劫持风险；Domain Hijacking；DNS Hijacking；
4. ``gem install jekyll``等安装慢，可能是因为镜像源（国外源）等网络状况“差”；ruby性能强弱应该不是主要因素吧~
5. gem 提示 “SSL 证书错误”；``sudo gem update --system``似乎无用；换为其他源、还是直接使用默认源 后可行；
6. Jekyll 只是 GitHub 推荐使用；
7. Jekyll Now 是基于 Jekyll 开发的模板（主题）之一；在 http://jekyllthemes.org/ 下载 Jekyll Now 后，``bundle install`` 与 ``jekyll new . --force`` 等命令均不可行；
   1. 前者 ``Could not locate Gemfile``；后者应该是新建项目；根据 [Jekyll Now](https://github.com/barryclark/jekyll-now/) 使用``jekyll serve``后可行；
8. ``bundle exec jekyll serve`` 等其他命令未尝试；


**References:**
1. [GitHub Pages 快速入门](https://docs.github.com/zh/pages/quickstart)
2. [关于自定义域名和 GitHub 页面](https://docs.github.com/zh/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages)
3. [如何在 GitHub 上写博客？](https://www.zhihu.com/question/20962496)
4. [github pages搭建自己的博客](https://www.jianshu.com/p/3f2afe2ae7fd)
5. [Jekyll Now](https://github.com/barryclark/jekyll-now/)
6. [姚顺雨 GitHub Pages](https://ysymyth.github.io/)


