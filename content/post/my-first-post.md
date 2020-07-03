---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "My First Post"
subtitle: ""
summary: ""
authors: [Thomas]
tags: [test]
categories: [testing]
date: 2020-06-30T22:32:41+08:00
lastmod: 2020-06-30T22:32:41+08:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

# Testing for my first post

* 1
* 2
* 3
* 4
* 5

Diagram as Code.

Diagrams lets you draw the cloud system architecture in Python code. It was born for prototyping a new system architecture design without any design tools. You can also describe or visualize the existing system architecture as well. Diagrams currently supports main major providers including: AWS, Azure, GCP, Kubernetes, Alibaba Cloud, Oracle Cloud etc... It also supports On-Premise nodes, SaaS and major Programming frameworks and languages.

Diagram as Code also allows you to track the architecture diagram changes in any version control system.


NOTE: It does not control any actual cloud resources nor does it generate cloud formation or terraform code. It is just for drawing the cloud system architecture diagrams.


Hugo 的教學文件有提供一個簡單的 script 來讓你快速執行發布這件事情，他也是使用 git submodule 來達成這件事，但我不太喜歡 git submodule，所以我稍微改了一下，讓他變成一般的獨立 project，可參考以下的 script，第一次執行我建議先一行一行手動執行看看。

---

準備 Base Image
===

這個 Base Image 會用在安裝 Master / Worker Node.

* 虛擬環境：
    * 在 VMWare 上，將 Guest OS 的網路設定為 Bridge Mode。
    * Proxmox  上，同樣將 Guest OS 的網路設定為 Bridge Mode
* 安裝 ubuntu 16.04 or ubuntu 18.04
    * 關閉 swap: swapoff -a
    * 註解 /etc/fstab
* 注意：
    * LAN 裡面的 DHCP Lease Time 可以調大一點，避免太早過期，下次 Cluster 跑不起來。
    * 如果要使用 PV 的話，Disk Size 不能太小，建議 80GiB 以上。
    ** VMWare 如果使用 Linked Clone 會造成 Disk Size 無法調整。

---

GGGGG
---

