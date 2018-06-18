# 项目概述

基于 OWASP Mutillidae II Web Pen-Test Practice Application 的 CBC Bit-flipping Attack 学习 Docker 训练环境快速构建

# 快速上手

```bash
# Step 0. 准备好 Docker 环境
# https://github.com/c4pr1c3/ac-demo 依赖环境安装说明

# Step 1. 拉取镜像并直接在本地运行
sudo docker run -d --name mutillidae -p 8081:80 c4pr1c3/dockermutillidae

# Step 2. 打开浏览器（推荐 Google Chrome 或 Mozilla Firefox 最新版）访问 http://127.0.0.1:8081/
# Step 3. 点击页面上的超链接 setup/reset the DB 弹出提示选择「确定」完成数据库初始化
# Step 4. 在左侧导航栏中依次选择 OWASP 2017 -> A2 - Broken Authentication and Session Management -> Priviliege Escalation -> Via CBC-bit Flipping
# Step 5. 阅读实验说明，完成实验

# 重置实验环境（所有实验数据均被销毁）
sudo docker rm -f mutillidae && sudo docker run -d --name mutillidae -p 8081:80 c4pr1c3/dockermutillidae
```

# 推荐阅读

* [Learning CBC Bit-flipping Through Gamification by OWASP 2018.4](https://www.sans.org/reading-room/whitepapers/vpns/learning-cbc-bit-flipping-gamification-38375)
* Project Whitepaper: http://www.giac.org/paper/gwapt/3387/introduction-owasp-mutillidae-ii-web-pen-test-training-environment/126917
