# 用例规约表设计

## table_class_choose.md（选择上课班级用例规约表）

<table>
    <caption>“选择上课班级”用例规约</caption>
    <tr>
        <td>用例名称</td>
        <td>选择上课班级</td>
    </tr>
    <tr>
        <td>参与者</td>
        <td>教师</td>
    </tr>
    <tr>
        <td>前置条件</td>
        <td>教师已登录，并进入排课流程，选择了直接选择上课班级</td>
    </tr>
    <tr>
        <td>后置条件</td>
        <td>系统跳转至课程实验页面</td>
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
            1. 教师对课程选择直接选择上课班级；<br><br><br><br><br>
            6. 教师选择上课班级；<br>
            7. 教师点击提交按钮；<br><br><br>
        </td>
        <td>
            <br>
            2. 系统验证教师登录状态是否有效；<br>
            3. 系统检索可以被选择的班级；<br>
            4. 系统返回检索到的班级；<br>
            5. 系统跳转至选择上课班级页面；<br><br><br>
            8. 系统存储课程的上课班级信息；<br>
            9. 系统提示选择上课班级成功。
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
            3a. 系统检索到没有可以被选择的班级<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示无班级可供选择，转第1步；<br>
            3b. 系统在检索班级时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示检索班级失败，转第1步；<br>
            7a. 教师选择返回，放弃选择上课班级<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统跳转至排课页面，转第1步；<br>
            8a. 系统存储上课班级信息时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示选择上课班级失败，转第6步。
        </td>
    </tr>
    <tr>
        <td colspan="2">业务规则</td>
    </tr>
    <tr>
        <td colspan="2">
            <ol>
                <li>教师可以为一门课程选择多个班级；</li>
                <li>教师只能选择可以被选择的班级。</li>
            </ol>
        </td>
    </tr>
</table>