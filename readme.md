urltype使用简介

用途：提供其他程序启动当前程序的入口

使用：

1.打开iOS工程，选择工程，切换到工程的infor栏，选择URLtype

2.添加URLtype

3.url传递参数
在程序AppDelegate 中实现
- (BOOL)application:(UIApplication *)application openURL:(NSURL *)url sourceApplication:(NSString *)sourceApplication annotation:(id)annotation{
   
  
   
     // sourceApplication 为 URLtype 中的 identifier
    //[url query]获取参数   
    return YES;
}
- (BOOL)application:(UIApplication *)application handleOpenURL:(NSURL *)url{
   
    return YES;
}

4.Safari中打开以URLscheme开头的URL 会启动程序，其他程序中打开当前程序的代码如下：
NSString *customURL = @"URLscheme://?token=123abct?istered=1";
 [[UIApplication sharedApplication] openURL:[NSURL URLWithString:customURL]];

本程序中URLscheme 为jawayURLSchemaUseDemo 即
NSString *customURL = @"jawayURLSchemaUseDemo://?token=123abct?istered=1";
    [[UIApplication sharedApplication] openURL:[NSURL URLWithString:customURL]x

敬请勘误：695886285@qq.com
