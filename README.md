# Cpp_Primer_Studing_Road
# Git使用流程

1. 安装git，配置信息

   ```
   git config --global user.name "youname" //配置GitHub名称
   git config --global user.email "youemail" // 配置GitHub邮箱
   ```

2. 生成密钥并存储到GitHub中

   * 生成ssh key

   ```
   ssh-keygen -t rsa -C "youremail" 
   ```

   * 在.ssh的文件夹(会保存到你指定的位置)下会出现两个文件 ***id_rsa*** 和 ***id_rsa.pub***，打开后面那个文件，将其中的内容复制到GitHub的New SSH key中

   * 连接本地和远程

     ```
     git remote add origin yourSSH
     ```

3. 在GitHub上建立仓库

4. 在本地建立仓库

   ```
   cd 要建立仓库的位置
   git init
   ```

5. 本地仓库和远程仓库建立通信

   ```
   git remote add origin yourSSH
   ```

6. 如果远程仓库不为空，需要先把远程的文件pull到本地，本地才能上传到远程

   ```
   git pull  origin master
   ```

7. 推送操作

   ``` 
   git add . // 工作区推送到暂存区
   git commit -m "描述文字" // 暂存区推送到本地仓库
   git push -u origin master // 本地仓库推送到远程仓库
   ```

8. GitHub存储逻辑

   ![在这里插入图片描述](https://img-blog.csdnimg.cn/20190514182153955.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjQ5MDM5OA==,size_16,color_FFFFFF,t_70)