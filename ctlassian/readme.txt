confluence 安装记录

1. 安装confluence时，创建 data db 目录，给775权限，记得-R
2. 当第一次遇到要求覆盖表时，页面样式会缺失，基本就可以确定要报错了，确定覆盖之后报错
3. 接着down掉所有容器，删除data/confluence/var/ 目录下的 confluence.cfg.xml 文件
4. 然后重新给所有的文件及目录755权限，记得-R
5. 然后启动，等到了要求覆盖页面时，发现样式正常，则基本可以确定可以安装成功了
6. 如果还不行，删除掉所有非自己创建的目录，镜像，重新build。接着仍会从1开始，或有可能成功。
7. 成功具有偶然性

参考链接：
* https://confluence.atlassian.com/confkb/confluence-does-not-start-due-to-spring-application-context-has-not-been-set-218278311.html
* https://community.atlassian.com/t5/Confluence-questions/Spring-Application-context-has-not-been-set/qaq-p/1367730
