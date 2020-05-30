# 数据库设计

## table_class.md（班级表）

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
        <td>class_id</td>
        <td>int</td>
        <td>主键</td>
        <td>否</td>
        <td></td>
        <td>自动递增，无符号</td>
        <td>班级的id，为class表的主键。</td>
    </tr>
    <tr>
        <td>grade</td>
        <td>int</td>
        <td></td>
        <td>否</td>
        <td></td>
        <td>无符号，grade <= system.time.year</td>
        <td>班级所在的年级。</td>
    </tr>
    <tr>
        <td>major</td>
        <td>varchar(50)</td>
        <td></td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>班级所在的专业。</td>
    </tr>
    <tr>
        <td>number</td>
        <td>int</td>
        <td></td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>班级的顺序，即几班。</td>
    </tr>
</table>