为已经存在的github octopuses配置本地环境
========================================

1. 在本地安装RVM(Ruby Version Manager)和Ruby 1.9.2；

2. 从你的github得到你的octopress内容：

    git clone -b source git@github.com:username/username.github.com.git octopress # get the source code from your "source" branch of your octopress on github
    ＃ learn from: http://stackoverflow.com/questions/1911109/git-clone-a-specific-branch
    cd octopress
    git clone git@github.com:username/username.github.com.git _deploy # get your static pages content from your "master"branch of your cotopress on github

3. 安装依赖gems:

    gem install bundler # Install dependencies
    bundle install
    rake install # Install the default Octopress theme

4. 编写文章，预览部署：

    cd octopress
    rake new_post["Your Title of Your Article"]
    rake generate # generate your blog static pages content according to your input. 
    rake preview # start a web server on "http://localhost:4000", you can preview your blog content.
    rake deploy # push your static pages content to your github pages repo ("master" branch)

5. 提交你的文本修改到github:

    cd your_local_octopress_directory
    git add .
    git commit -m 'your message'
    git push origin source

注意：如果要从github得到最新的source内容，请运行以下命令：

    cd your_local_octopress_directory
    cd _deploy
    git pull origin master
    cd ..
    git pull origin source

原则很简单，只要记住“your_local_octopress_directory”对应的的remote source branch，而”_deploy”对应的是remote master branch即可。