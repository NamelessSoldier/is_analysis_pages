# 接口设计

## api_chooseClass.md（选择上课班级接口）

<ul>
    <li>权限：教师：只能为自己开设的课程选择上课班级，即接口参数lesson_id所对应lesson表中的lesson.teacher_id必须等于登录教师的teacher_id。</li>
    <li>功能：用于选择上课班级</li>
    <li>请求地址：http://NamelessSoldier.github.io/is_analysis/v1/api/lesson/class/.choose</li>
    <li>请求方法：POST</li>
    <li>
        请求实例：  
            
```
{
    "access_token": $access_token,
    "method": "POST",
    "lesson_id": 1,
    "class_id": 11
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
                <td>class_id</td>
                <td>是</td>
                <td>班级的id，对应表class.class_id的值。</td>
            </tr>
        </table>
    </li>
    <li>
        返回实例：  
            
```
{
    "information": "设置班级成功",
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