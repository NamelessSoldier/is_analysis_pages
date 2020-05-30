# 接口设计

## api_getUser.md（查看用户信息接口）

<ul>
    <li>权限：学生/教师：查看自己的信息，必须先登录，不能查看其他用户的信息，即接口参数user_id必须等于登录用户的user_id。</li>
    <li>功能：用于用户查看用户信息</li>
    <li>请求地址：http://NamelessSoldier.github.io/is_analysis/v1/api/user/.get</li>
    <li>请求方法：GET</li>
    <li>
        请求实例：  
            
```
{
    "access_token": $access_token,
    "method": "GET",
    "user_id": 1
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
                <td>用户的id，对应表user.user_id的值。</td>
            </tr>
        </table>
    </li>
    <li>
        返回实例：  
            
```
{
    "information": "查看用户信息成功",
    "status": true,
    "user_id": 1,
    "type": "学生"
    "student_id": "201710414305",
    "teacher_id": null,
    "user_name": "胡宏坤",
    "class_id": 1,
    "github_name": "NamelessSoldier",
    "password": "AF#W@#AAAASDF",
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
                <td>user_id</td>
                <td>是</td>
                <td>用户的id，对应表user.user_id的值。</td>
            </tr>
            <tr>
                <td>type</td>
                <td>是</td>
                <td>用户的类型，用户为学生则为“学生”，用户为教师则为“教师”。</td>
            </tr>
            <tr>
                <td>student_id</td>
                <td>否</td>
                <td>学生的学号，若用户类型为“教师”则为空，对应表student.student_id的值。</td>
            </tr>
            <tr>
                <td>teacher_id</td>
                <td>否</td>
                <td>教师的教职工号，若用户类型为“学生”则为空，对应表teacher.teacher_id的值。</td>
            </tr>
            <tr>
                <td>user_name</td>
                <td>是</td>
                <td>用户的真实姓名，对应表user.user_name的值。</td>
            </tr>
            <tr>
                <td>class_id</td>
                <td>是</td>
                <td>班级的id，对应表class.class_id的值。</td>
            </tr>
            <tr>
                <td>github_name</td>
                <td>否</td>
                <td>用户的github用户名，对应表user.github的值。</td>
            </tr>
            <tr>
                <td>password</td>
                <td>是</td>
                <td>用户的密码，不能为空，必须经过加密，不能是密码的原文，对应表user.password的值。</td>
            </tr>
            <tr>
                <td>code</td>
                <td>是</td>
                <td>返回码。</td>
            </tr>
        </table>
    </li>
</ul>