# 接口设计

## api_login.md（登录接口）

<ul>
    <li>权限：访客。</li>
    <li>功能：用于用户登录</li>
    <li>请求地址：http://NamelessSoldier.github.io/is_analysis/v1/api/user/login/.set</li>
    <li>请求方法：GET</li>
    <li>
        请求实例：  
            
```
{
    "access_token": $access_token,
    "method": "GET",
    "user_id":"201710414305",
    "password":"1",
    "type":"student"
}
```
   </li>
    <li>
        请求参数：
        <table>
            <tr>
                <td>参数名称</td>
                <td>必填</td>
                <td>说明</td>
            </tr>
            <tr>
                <td>access_token</td>
                <td>是</td>
                <td>用于验证请求合法性的认证信息。</td>
            </tr>
            <tr>
                <td>method</td>
                <td>是</td>
                <td>固定为“GET”。</td>
            </tr>
            <tr>
                <td>user_id</td>
                <td>是</td>
                <td>学生的学号或者老师的教职工号，由type决定，对应表user.user_id的值。</td>
            </tr>
            <tr>
                <td>password</td>
                <td>是</td>
                <td>用户的密码，不是原文，是加密后的字符串，对应表user.password的值。</td>
            </tr>
            <tr>
                <td>type</td>
                <td>是</td>
                <td>用户类型，学生或者老师。</td>
            </tr>
        </table>
    </li>
    <li>
        返回实例：  
            
```
{
    "information": "登录成功",
    "status": true,
    "code": 200
}
```
   </li>
    <li>
        返回参数说明：
        <table>
            <tr>
                <td>参数名称</td>
                <td>必填</td>
                <td>说明</td>
            </tr>
            <tr>
                <td>information</td>
                <td>是</td>
                <td>返回的说明信息。</td>
            </tr>
            <tr>
                <td>status</td>
                <td>是</td>
                <td>返回的结果，boolean类型，true表示正确的返回，false表示有错误。</td>
            </tr>
            <tr>
                <td>code</td>
                <td>是</td>
                <td>返回码。</td>
            </tr>
        </table>
    </li>
</ul>