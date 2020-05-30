# 接口设计

## api_setStudentScore.md（查看成绩接口）

<ul>
    <li>权限：学生：只能查看自己的成绩，即接口参数student_id必须等于登录学生的student_id。</li>
    <li>功能：用于学生查看成绩</li>
    <li>请求地址：http://NamelessSolider.github.io/is_analysis/v1/api/student/score/.get</li>
    <li>请求方法：GET</li>
    <li>
        请求实例：  
            
```
{
    "access_token": $access_token,
    "method": "GET",
    "student_id": "201710414305"
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
                <td>student_id</td>
                <td>是</td>
                <td>学生的学号，对应表student.student_id的值。</td>
            </tr>
        </table>
    </li>
    <li>
        返回实例：  
            
```
{
    "information": "查看成绩成功",
    "status": true,
    "average": 75,
    "test_score_list": [
        [
            {"name": "概念分数", "test_score":"99"},
            {"name": "结构分数", "test_score":"99"},
            {"name": "逻辑分数", "test_score":"99"},
            {"name": "语言分数", "test_score":"99"},
            {"name": "条理分数", "test_score":"99"}
        ]
        [
            {"name": "xxx", "test_score":"99"},
            {"name": "xxx", "test_score":"99"},
            {"name": "xxx", "test_score":"99"},
            {"name": "xxx", "test_score":"99"},
            {"name": "xxx", "test_score":"99"}
        ]
    ],
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
                <td>average</td>
                <td>否</td>
                <td>学生所有课程的平均成绩，对应表student.student_average的值。</td>
            </tr>
            <tr>
                <td>test_score_list</td>
                <td>否</td>
                <td>学生实验的成绩列表。</td>
            </tr>
            <tr>
                <td>code</td>
                <td>是</td>
                <td>返回码。</td>
            </tr>
        </table>
    </li>
</ul>