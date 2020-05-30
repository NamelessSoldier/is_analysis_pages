# 用例规约表设计

## table_user_update.md（修改用户信息用例规约表）

<table>
    <caption>“修改用户信息”用例规约</caption>
    <tr>
        <td>用例名称</td>
        <td>修改用户信息</td>
    </tr>
    <tr>
        <td>参与者</td>
        <td>学生/教师</td>
    </tr>
    <tr>
        <td>前置条件</td>
        <td>用户已登录，并进入个人信息页面</td>
    </tr>
    <tr>
        <td>后置条件</td>
        <td>系统跳转至用户个人信息页面</td>
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
            1. 用户点击修改用户信息按钮；<br><br><br><br>
            5. 用户填写需要修改的信息；<br>
            6. 用户点击提交按钮；<br><br><br><br>
        </td>
        <td>
            <br>
            2. 系统验证用户登录状态是否有效；<br>
            3. 系统获取用户信息；<br>
            4. 系统跳转至修改用户信息页面；<br><br><br>
            7. 系统检测用户提交的修改信息是否合法；<br>
            8. 系统存储修改后的用户信息；<br>
            9. 系统提示用户信息修改成功。
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
            3a. 系统获取用户信息时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示获取用户信息失败，转第1步；<br>
            6a. 用户选择返回，放弃修改<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统跳转至用户个人信息主页，转第1步；<br>
            7a. 系统检测到用户提交的修改信息非法<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示用户提交信息非法，转第5步；<br>
            8a. 系统存储信息时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示修改用户信息失败，转第6步。
        </td>
    </tr>
    <tr>
        <td colspan="2">业务规则</td>
    </tr>
    <tr>
        <td colspan="2">
            <ol>
                <li>用户只能修改用户自己的信息；</li>
                <li>用户提交的修改信息必须合法。</li>
            </ol>
        </td>
    </tr>
</table>