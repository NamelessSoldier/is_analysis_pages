# 接口设计

## api_setLesson.md（维护课程级接口）

<ul>
    <li>权限：教师：只能维护已存在学科的课程，即接口参数subject_id必须存在以其为主键的subject表，只能开设自己为任课老师的课程，即接口参数teacher_id必须等于登录教师的teacher_id。</li>
    <li>功能：用于教师维护课程</li>
    <li>请求地址：http://NamelessSoldier.github.io/is_analysis/v1/api/lesson/.set</li>
    <li>请求方法：POST</li>
    <li>
        请求实例：  
            
```
{
    "access_token": $access_token,
    "method": "POST",
    "subject_id": 1,
    "teacher_id": "201710414305",
    "choose": true,
    "year": 2020,
    "semester": "第二学期"
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
                <td>subject_id</td>
                <td>是</td>
                <td>科目的id，对应表subject.subject_id的值。</td>
            </tr>
            <tr>
                <td>teacher_id</td>
                <td>是</td>
                <td>教师的教职工号，对应表teacher.teahcer_id的值。</td>
            </tr>
            <tr>
                <td>choose</td>
                <td>是</td>
                <td>是否由学生自主选课，“是”表示由学生自主选课，“否”表示由教师直接选择上课班级，对应表lesson.choose的值。</td>
            </tr>
            <tr>
                <td>year</td>
                <td>是</td>
                <td>开课年份，对应表lesson.year的值。</td>
            </tr>
            <tr>
                <td>semester</td>
                <td>是</td>
                <td>开课学期，对应表lesson.semester的值。</td>
            </tr>
        </table>
    </li>
    <li>
        返回实例：  
            
```
{
    "information": "维护课程成功",
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