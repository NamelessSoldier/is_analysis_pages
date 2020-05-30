# 接口设计

## api_chooseLesson.md（选课级接口）

<ul>
    <li>权限：学生：只能给自己选课，即接口参数student_id必须等于登录学生的student_id。</li>
    <li>功能：用于学生选课</li>
    <li>请求地址：http://NamelessSoldier.github.io/is_analysis/v1/api/lesson/.choose</li>
    <li>请求方法：POST</li>
    <li>
        请求实例：  
            
```
{
    "access_token": $access_token,
    "method": "POST",
    "student_id": "201710414305",
    "lesson_id": 11
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
                <td>固定为“POST”。</td>
            </tr>
            <tr>
                <td>student_id</td>
                <td>是</td>
                <td>学生的学号，对应表student.student_id的值。</td>
            </tr>
            <tr>
                <td>lesson_id</td>
                <td>是</td>
                <td>课程的id，对应表lesson.lesson_id的值。</td>
            </tr>
        </table>
    </li>
    <li>
        返回实例：  
            
```
{
    "information": "选课成功",
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