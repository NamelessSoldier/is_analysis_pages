# 数据库设计

## table_teacher.md（教师表）

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
        <td>teacher_id</td>
        <td>varchar(50)</td>
        <td>主键</td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>教师的教职工号，为teacher表的主键。</td>
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
        <td>department</td>
        <td>varchar(255)</td>
        <td></td>
        <td>是</td>
        <td>null</td>
        <td></td>
        <td>老师所属的部门。</td>
    </tr>
</table>