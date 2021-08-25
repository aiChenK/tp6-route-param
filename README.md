# tp6-route-param
tp6支持url参数顺序解析，可用于tp5升级兼容(不建议)
tp6将路由参数绑定方式更改为仅使用`route->param`

## 运行环境
- PHP 7.1+
- ThinkPHP 6

## 安装方法
        composer require aichenk/tp6-route-param
        
## 使用
### 路由参数绑定支持顺序绑定
- `config/route.php`增加参数`'url_param_type' => 1`
### 更改路由绑定参数来源（不使用request->param())
- `config/route.php`增加参数`'only_route_param' => true`

## 更新日志
2021-07-20 - v1.1.0
- 支持路由参数分发仅使用`route`中`param`(忽略`request->param()`)

2021-08-25 - v1.2.0
- 增加`Request`类支持修改路由解析参数