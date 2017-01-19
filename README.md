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
void TalkieManager.connect(String appid, String userid, new TalkieClient.ConnectCallback(){
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

2、 进入房间
```java
void TalkieManager.online(new TalkieClient.onlineCallback(){
      /**
       * 进入房间成功
       */
      @Override
      public void onSuccess() {

      }

      /**
       * 进入房间失败
       * @param errorCode 错误码，查看错误码对应的注释
       */
      @Override
      public void onError(TalkieClient.ErrorCode errorCode) {

      }
    });
```

3、 离开房间offline
```java
void TalkieManager.offline();
```

4、 请求发言reqSpeak
```java
void TalkieManager.reqSpeak(new TalkieClient.ReqSpeakCallback(){
      /**
       * 请求发言成功
       */
      @Override
      public void onSuccess() {

      }

      /**
       * 请求发言失败
       * @param errorCode 错误码，查看错误码对应的注释
       */
      @Override
      public void onError(TalkieClient.ErrorCode errorCode) {

      }
    })
```

5、 结束发言stopSpeak
```java
void TalkieManager.stopSpeak()
```

6、 更新位置location
```java
void TalkieManager.location(float lat, float lon, int speed, int direction)
```

7、 其它用户开始发言广播回调
```java
void TalkieManager.setOtherStartSpeakListener(new TalkieClient.StartSpeakListener(){
      /**
       * 对讲服务器连接成功
       * @param openid 
       */
      @Override
      public void onStartSpeak(String openid) {

      }
    });
```

8、 其它用户结束发言广播
```java
void TalkieManager.setOtherStopSpeakListener(new TalkieClient.StopSpeakListener(){
      /**
       * 对讲服务器连接成功
       * @param openid 
       */
      @Override
      public void onStopSpeak(String openid) {

      }
    });
```

9、 其它用户位置变更广播
```java
void TalkieManager.setOtherLocationListener(new TalkieClient.LocationListener(){
      /**
       * 对讲服务器连接成功
       * @param openid 
       */
      @Override
      public void onLocationListener(String openid, float lat, float lon, int speed, int direction) {

      }
    });
```

10、 连接状态回调
```java
void TalkieManager.setConnectStateListener(new TalkieClient.ConnectStateListener(){
      @Override
      public void onStateChange(int state){
      }
    });
```
