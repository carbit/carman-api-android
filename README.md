#亿连对讲 SDK Android 接入说明


---------------
##目录
[一、配置开发环境](#配置开发环境)

[二、SDK接入步骤](#SDK接入步骤)

------------------

<h2 id="配置开发环境">一、配置开发环境</h2>


<h2 id="SDK接入步骤">二、SDK接入步骤</h2>

1、 连接服务器
```java
TalkieManager.connect(String appid, String userid, new TalkieClient.Connectcallback(){
  /**
   * 对讲服务器连接成功
   * @param openid 
   */
  @Override
  public void onSuccess(String openid) {
  
  }
  
  /**
   * 对讲服务器连接失败
   * @param errorCode 错误码，查看错误码对应的注释
   */
  @Override
  public void onError(TalkieClient.ErrorCode errorCode) {
  
  }
});
```

2、 进入房间join
```java
TalkieManager.join();
```

3、 离开房间offline
```java
TalkieManager.offline();
```

4、 请求发言reqSpeak
```java
TalkieManager.reqSpeak()
```

5、 结束发言stopSpeak
```java
TalkieManager.stopSpeak()
```

6、 更新位置location
```java
TalkieManager.location(float lat, float lon, int speed, int direction)
```

7、 其它用户开始发言广播回调startSpeakCallBack
```java
TalkieManager.setStartSpeakCallback(new TalkieClient.StartSpeakCallback(){

});
```

8、 其它用户结束发言广播stopSpeakBcst
```java
TalkieManager.setStopSpeaCallback(new TalkieClient.StopSpeakCallback(){

});
```

9、 其它用户位置变更广播locationBcst
```java
TalkieManager.setLocationCallBack();
```
