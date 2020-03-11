# jdziapp_talentmov APP说明书
  用到的开发工具android studio<br>

  先说对接文件改哪里<br>
  以下改的是后台的源码，也就是主机文件根目录<br>
  
# cms：<br>
## 1.\app\app\cms\config\dbs.php  17行开始 填你的苹果cms数据库账号密码<br>

## 2.注册金币、分享获得金币 ： <br>
+ /app/cms/src/app/Model/Model_User.php     第72行 $pass, 'user_points' => 改成你想要的注册金币数,<br>
+ /app/cms/src/app/Model/Model_User.php     第105行(int)$points + 改成你想要的分享金币数<br>
+ /app/cms/src/app/Api/Mov.php   版本更新 公告 广告位   470行开始<br>

# APP 修改:
## 1.前端源码要改的地方
+ 搜索：金豆子影视  替换成自己的app名
+ 搜索http://111.67.193.41:6061/  替换成自己的域名（后面必须带/）
+ 其他修改项自己搜索着找就好了

+ 分享的图片：\talentmov\app\src\main\res\drawable-xxhdpi\share.png
+ Logo地址：\talentmov\app\src\main\res\mipmap-xxhdpi\ticon2.png  自己替换
+ 对接网站 以及分享接口之类：<br>
\talentmov\app\src\main\java\com\movtalent\app\App_Config.java<br>
72行  对接的网站<br>
90行  对接的源码的地址<br>
121-123行  电视直播  小说  漫画的对应网址更改<br>
\talentmov\modules\playerlib\src\main\res\layout\layout_auth_cover.xml<br>
第59行  游客观看时间文字  <br>
\talentmov\modules\playerlib\src\main\java\com\media\playerlib\cover\AuthCover.java<br>
第103行  60*1000  就是60秒   时间自己改<br>

院线大片  推荐1
精挑好货  推荐2
热播鲜剧  推荐4
经典动漫  推荐5
热门综艺  推荐6  （名字源码我改了幻灯片推荐   名字你们自己搜索改）
幻灯片  推荐9	

品质好剧，必看榜单  推荐1 修改为：WEB端热播推荐 推荐1
正在上映  推荐7
火热更新，好剧不断  推荐2
最新电影  推荐3
最新电视剧  推荐4
最新动漫  推荐5
最新综艺  推荐6  （名字源码我改了幻灯片推荐   名字你们自己搜索改）
幻灯片  推荐9

## 2.广告位：<br>
+ ad_splash     开屏广告<br>
+ ad_home_1到ad_home_4   推荐页广告<br>
+ ad_detail   播放页广告<br>
+ ad_player   播放器广告<br>
+ ad_user_center   个人中心广告<br>

## 3.
+ HomeTabFragment 首页<br>
+ SelfTabFragment 个人中心<br>
+ OnlineDetailPageActivity 播放页<br>
+ PlayerPresenter 播放器<br>
+ ShareTabFragment 分享<br>
+ TopicTabFragment 专题推荐<br>

## 4.编译：
+ 右边点击 gradle --> app --> Tasks --> build --> assembleRelease
+ \talentmov\app\build\outputs\apk\  编译了在这个文件夹里