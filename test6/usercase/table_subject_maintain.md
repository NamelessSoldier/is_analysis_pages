# 用例规约表设计

## table_subject_maintain.md（维护科目用例规约表）

<table>
    <caption>“维护科目”用例规约</caption>
    <tr>
        <td>用例名称</td>
        <td>维护科目</td>
    </tr>
    <tr>
        <td>参与者</td>
        <td>教师</td>
    </tr>
    <tr>
        <td>前置条件</td>
        <td>教师已登录</td>
    </tr>
    <tr>
        <td>后置条件</td>
        <td>系统跳转至实验管理系统首页</td>
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
            1. 教师点击设置科目按钮；<br><br><br>
            4. 教师选择科目或增加科目；<br>
            5. 教师点击提交按钮；<br><br><br><br><br>
        </td>
        <td>
            <br>
            2. 系统验证教师登录状态是否有效；<br>
            3. 系统跳转至设置科目页面；<br><br><br>
            6. 系统检测提交的科目是否与已存在的科目重复；<br>
            7. 系统检测提交的科目信息是否合法；<br>
            8. 系统存储科目信息；<br>
            9. 系统提示设置科目成功。
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
            5a. 教师选择返回，放弃设置科目<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统跳转至实验管理平台首页，转第1步；<br>
            6a. 系统检测到设置的科目与已存在的科目重复<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示设置的科目已存在，转第4步；<br>
            7a. 系统检测到设置的科目信息非法<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示设置的科目信息非法，转第4步；<br>
            8a. 系统储存科目信息时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示设置科目失败，转第5步。
        </td>
    </tr>
    <tr>
        <td colspan="2">业务规则</td>
    </tr>
    <tr>
        <td colspan="2">
            <ol>
                <li>教师一次只能设置一个科目；</li>
                <li>教师设置的科目不能与已存在的科目重复；</li>
                <li>教师设置的科目必须合法。</li>
            </ol>
        </td>
    </tr>
</table>