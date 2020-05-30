# 接口设计

## api_setTest.md（维护实验接口）

<ul>
    <li>权限：教师：只能维护自己开设课程的实验，即接口参数lesson_id所对应lesson表中的lesson.teacher_id必须等于登录教师的teacher_id。</li>
    <li>功能：用于教师维护实验</li>
    <li>请求地址：http://NamelessSoldier.github.io/is_analysis/v1/api/test/.set</li>
    <li>请求方法：POST</li>
    <li>
        请求实例：  
            
```
{
    "access_token": $access_token,
    "method": "POST",
    "lesson_id": 6,
    "test_name": "基于GitHub的实验管理平台",
    "test_time": 2020-05-26 08:30:00
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
                <td>lesson_id</td>
                <td>是</td>
                <td>课程的id，对应表lesson.lesson_id的值。</td>
            </tr>
            <tr>
                <td>test_name</td>
                <td>是</td>
                <td>实验的名字，对应表test.test_name的值。</td>
            </tr>
            <tr>
                <td>test_time</td>
                <td>是</td>
                <td>实验的开始时间，对应表test.test_time的值。</td>
            </tr>
        </table>
    </li>
    <li>
        返回实例：  
            
```
{
    "information": "维护实验成功",
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