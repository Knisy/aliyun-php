
# 使用教程
这是基于thinkphp的  如果需要集成到其他框架 看看代码思路转换应该不难


## Oss.class.php

```

    放到thinkphp  Think\Upload\Driver目录下  
    
    C('FILE_UPLOAD_TYPE','Oss');

    $oss_config = array(
        'region'=>'bucket.oss-cn-shenzhen',//节点
        'access_id'  => '', //阿里云Access Key ID
        'access_key' => '', //阿里云Access Key Secret
        'bucket'     => 'bucket',//bucket
     );  
    $upload = new Upload($config, 'Oss', $oss_config);

```


## Alisms.class.php

```

    放到thinkphp  Library\Extend目录下  
    $sms_config = array(
        'accessKeyId'  => '', //阿里云Access Key ID
        'accessKeySecret' => '', //阿里云Access Key Secret
        'signName' => 'test',
        'templateCode' => 'SMS_00000002',
     );
    $sms= new Alisms($sms_config);
    $tel=15888888888;
    $code=1234;
    $status = $sms->send_verify($tel, $code);
    if (!$status){
        echo 'error';
    }

```
