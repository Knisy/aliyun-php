####使用教程

```

    放到thinkphp  Think\Upload\Driver目录下  
    $oss_config = array(
        'region'=>'bucket.oss-cn-shenzhen',//节点
        'access_id'  => '', //阿里云Access Key ID
        'access_key' => '', //阿里云Access Key Secret
        'bucket'     => 'bucket'//bucket
     );  
    $upload = new Upload($config, 'Oss', $oss_config);

```