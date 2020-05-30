# 用例规约表设计

## table_password_update.md（修改密码用例规约表）

<table>
    <caption>“修改密码信息”用例规约</caption>
    <tr>
        <td>用例名称</td>
        <td>修改密码</td>
    </tr>
    <tr>
        <td>参与者</td>
        <td>学生/教师</td>
    </tr>
    <tr>
        <td>前置条件</td>
        <td>用户已登录</td>
    </tr>
    <tr>
        <td>后置条件</td>
        <td>系统跳转至实验管理平台首页</td>
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
            1. 用户点击修改密码按钮；<br><br><br>
            4. 用户填写修改的密码；<br>
            5. 用户点击提交按钮；<br><br><br><br><br>
        </td>
        <td>
            <br>
            2. 系统验证用户登录状态是否有效；<br>
            3. 系统跳转至修改密码页面；<br><br><br>
            6. 系统检测用户提交的密码是否合法；<br>
            7. 系统存储修改后的密码；<br>
            8. 系统提示密码修改成功；<br>
            9. 系统强制登出用户。
        </td>
    </tr>
    <tr>
        <td colspan="2">备选事件流</td>
    </tr>
    <tr>
        <td colspan="2">
            2a. 系统验证用户登录状态已失效<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示验证用户登录状态失败，转第1步；<br>
            5a. 用户选择返回，放弃修改<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统跳转至用户个人信息主页，转第1步；<br>
            6a. 系统检测到用户提交的密码非法<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示用户提交密码非法，转第4步；<br>
            7a. 系统存储密码时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示修改密码失败，转第5步。
        </td>
    </tr>
    <tr>
        <td colspan="2">业务规则</td>
    </tr>
    <tr>
        <td colspan="2">
            <ol>
                <li>用户只能修改用户自己的密码；</li>
                <li>用户提交的密码必须合法。</li>
            </ol>
        </td>
    </tr>
</table>