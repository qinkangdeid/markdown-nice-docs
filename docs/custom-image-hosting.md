## 自定义图床接口示例

`POST /api/files/upload`

### Parameter

| Name | Type | Description |
| :----- | :----- | :----- |
| file | formdata | 图片格式文件 |

### Request

1. url

`https://imgkr.com/api/files/upload`

2. headers

```
{
  "Accept": "*/*"
}
```

### Response

1. body

```
status: 200 OK
{
    "code": 200,
    "data": "https://imgkr.cn-bj.ufileos.com/58b138b2-c7de-4d75-a06d-f79cd68c2ceb.png",
    "message": "请求成功",
    "success": true
}
```

2. headers

```
{
    "access-control-allow-origin": "*",
    "content-type": "application/json;charset=UTF-8",
    "date": "Wed, 27 Nov 2019 02:29:24 GMT",
    "server": "nginx/1.16.1",
    "vary": "Origin, Access-Control-Request-Method, Access-Control-Request-Headers"
}
```