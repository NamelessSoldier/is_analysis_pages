# 用例规约表设计

## table_test_maintain.md（维护实验用例规约表）

<table>
    <caption>“维护实验”用例规约</caption>
    <tr>
        <td>用例名称</td>
        <td>维护实验</td>
    </tr>
    <tr>
        <td>参与者</td>
        <td>教师</td>
    </tr>
    <tr>
        <td>前置条件</td>
        <td>教师已登录，并进入课程主页</td>
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
            1. 教师点击开设实验按钮；<br><br><br>
            4. 教师填写实验信息；<br>
            5. 教师填写实验日期；<br>
            6. 教师点击提交按钮；<br><br><br><br><br>
        </td>
        <td>
            <br>
            2. 系统验证教师登录状态是否有效；<br>
            3. 系统跳转至开设实验页面；<br><br><br><br>
            7. 系统检测实验日期是否在当前时间之后；<br>
            8. 系统检测实验信息是否合法；<br>
            9. 系统存储实验信息；<br>
            10.系统提示开设实验成功。
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
            5a. 教师选择返回，放弃开设实验<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统跳转至课程实验页面，转第1步；<br>
            7a. 系统检测到实验日期在当前时间之后<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示实验日期在当前时间之后，转第5步；<br>
            8a. 系统检测到实验信息不合法<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示实验信息不合法，转第4步；<br>
            9a. 系统存储实验信息时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示开设实验失败，转第6步。
        </td>
    </tr>
    <tr>
        <td colspan="2">业务规则</td>
    </tr>
    <tr>
        <td colspan="2">
            <ol>
                <li>教师一次只能设置一门课程的一个实验；</li>
                <li>教师提交的实验信息必须合法；</li>
                <li>教师提交的实验日期必须在当前时间之后。</li>
            </ol>
        </td>
    </tr>
</table>