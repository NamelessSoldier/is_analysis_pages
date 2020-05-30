# 用例规约表设计

## table_student_maintain.md（维护学生账号用例规约表）

<table>
    <caption>“维护学生账号”用例规约</caption>
    <tr>
        <td>用例名称</td>
        <td>维护学生账号</td>
    </tr>
    <tr>
        <td>参与者</td>
        <td>教师</td>
    </tr>
    <tr>
        <td>前置条件</td>
        <td>教师已登录，并已查看学生列表</td>
    </tr>
    <tr>
        <td>后置条件</td>
        <td>系统跳转至学生列表页面</td>
    </tr>
    <tr>
        <td colspan="2">主事件流</td>
    </tr>
    <tr>
        <td>参与者动作</td>
        <td>系统行为</td>
    </tr>
    <tr>
        <td>
            1. 教师选择需要维护的学生；<br><br><br><br><br>
            6. 教师填写学生信息；<br>
            7. 教师点击提交按钮；<br><br><br><br>
        <td>
            <br>
            2. 系统验证教师登录状态是否有效；<br>
            3. 系统检索被选择学生的信息；<br>
            4. 系统返回该学生信息；<br>
            5. 系统跳转至维护学生页面；<br><br><br>
            8. 系统检验学生信息是否合法；<br>
            9. 系统存储学生信息；<br>
            10.系统提示维护学生账号成功。
        </td>
    </tr>
    <tr>
        <td colspan="2">备选事件流</td>
    </tr>
    <tr>
        <td colspan="2">
            2a. 系统验证教师登录状态已失效<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示验证教师登录状态失败，转第1步；<br>
            3a. 系统检索学生时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示检索学生失败，转第1步；<br>
            7a. 教师选择返回，放弃维护学生账号<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统跳转至学生列表页面，转第1步；<br>
            8a. 系统检验到提交的学生信息非法<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示提交的学生信息非法，转第6步；<br>
            9a. 系统存储维护后的学生信息时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示维护学生账号失败，转第7步。
    </tr>
    <tr>
        <td colspan="2">业务规则</td>
    </tr>
    <tr>
        <td colspan="2">
            <ol>
                <li>教师评一次只能维护一个学生账号；</li>
                <li>教师只能维护有对应权限的学生。</li>
            </ol>
        </td>
    </tr>
</table>