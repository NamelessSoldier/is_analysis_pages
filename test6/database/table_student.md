# 数据库设计

## table_student.md（学生表）

<table>
    <tr>
        <td>字段</td>
        <td>类型</td>
        <td>主键，外键</td>
        <td>可以为空</td>
        <td>默认值</td>
        <td>约束</td>
        <td>说明</td>
    </tr>
    <tr>
        <td>student_id</td>
        <td>varchar(50)</td>
        <td>主键</td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>学生的学号，为student表的主键。</td>
    </tr>
    <tr>
        <td>user_id</td>
        <td>int</td>
        <td>外键</td>
        <td>是</td>
        <td>null</td>
        <td>$user.user_id</td>
        <td>用户的id，为user表的外键。</td>
    </tr>
    <tr>
        <td>class_id</td>
        <td>int</td>
        <td>外键</td>
        <td>是</td>
        <td>null</td>
        <td>$class.class_id</td>
        <td>班级的id，为class表的外键。</td>
    </tr>
    <tr>
        <td>student_average</td>
        <td>int</td>
        <td>外键</td>
        <td>是</td>
        <td>0</td>
        <td>无符号, student_average <= 100</td>
        <td>学生所有课程平均分。</td>
    </tr>
</table>