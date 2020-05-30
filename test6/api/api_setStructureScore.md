# 接口设计

## api_setStructureScore.md（评阅结构分数接口）

<ul>
    <li>权限：教师：只能评阅参加自己开设课程的学生的实验结构分数，即接口参数test_id对应的test表中的test.lesson_id所对应的lesson表中的lesson.teacher_id必须等于登录教师的teacher_id，接口参数student_id必须等于test_id对应的test表中的test.lesson_id所对应的choose表中的choose.student_id或所对应lesson.class_id必须等于对应student表中的student.class_id。</li>
    <li>功能：用于教师评阅结构分数</li>
    <li>请求地址：http://NamelessSpldier.github.io/is_analysis/v1/api/test/score/structure/.set</li>
    <li>请求方法：POST</li>
    <li>
        请求实例：  
            
```
{
    "access_token": $access_token,
    "method": "POST",
    "student_id": "201710414305",
    "test_id": 6,
    "structure": "15"
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
                <td>test_id</td>
                <td>是</td>
                <td>实验的id，对应表test.test_id的值。</td>
            </tr>
            <tr>
                <td>structure</td>
                <td>是</td>
                <td>结构的分数，对应表score.structure的值。</td>
            </tr>
        </table>
    </li>
    <li>
        返回实例：  
            
```
{
    "information": "评阅结构分数成功",
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