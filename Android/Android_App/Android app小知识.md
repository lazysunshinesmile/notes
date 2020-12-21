Android app小知识

## 1. 重启Activity
```
Intent intent2 = getIntent();
overridePendingTransition(0, 0);
finish();
overridePendingTransition(0, 0);
startActivity(intent2);
```

## 2.多次启动service
service的onCreate只会执行一次，onBind也只会执行一次，onStartCommand可以执行多次

也就是说一旦service创建过了，而又没有被销毁的话，不管是再次调用bindService还是startService都不会再走onCreate， onBind也只会执行一次，多次调用startService会多次执行onstartCommand。

## 3. 检查某个Ip是否ping通
```
InetAddress.getByName(ipAddress).isReachable(timeOut);
```

## 4. 软键盘各种参数设置
[参考](https://juejin.im/entry/597ad8ac5188253df316f3c2)