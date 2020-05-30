# 用例规约表设计

## table_login.md（登录用例规约表）

<table>
    <caption>“登录”用例规约</caption>
    <tr>
        <td>用例名称</td>
        <td>登录</td>
    </tr>
    <tr>
        <td>参与者</td>
        <td>访客</td>
    </tr>
    <tr>
        <td>前置条件</td>
        <td>访客进入实验管理平台首页</td>
    </tr>
    <tr>
        <td>后置条件</td>
        <td>系统跳转至用户个人主页</td>
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
            1. 访客进入登录界面；<br>
            2. 访客选择用户类型；<br>
            3. 访客输入用户名；<br>
            4. 访客输入密码；<br>
            5. 访客点击登录按钮；<br><br><br><br>
        </td>
        <td>
            <br><br><br><br><br>
            6. 系统判断用户名、密码、用户类型正确；<br>
            7. 系统在客户端以cookie形式存储登录用户信息；<br>
            8. 系统提示访客登录成功
        </td>
    </tr>
    <tr>
        <td colspan="2">备选事件流</td>
    </tr>
    <tr>
        <td colspan="2">
            2a. 访客未选择用户类型<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示选择用户类型，转第2步；<br>
            3a. 访客未输入用户名<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示输入用户名，转第3步；<br>
            4a. 访客未输入用户名<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示输入密码，转第4步；<br>
            5a. 访客选择返回<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统跳转至实验管理平台主页面，转第1步；<br>
            6a. 系统验证登录时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示登录失败，转第5步；<br>
            6b. 系统验证登录失败<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示用户名或密码错误，转第4步；<br>
            7a. 系统储存cookie时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示存储cookie失败，转第7步。
        </td>
    </tr>
    <tr>
        <td colspan="2">业务规则</td>
    </tr>
    <tr>
        <td colspan="2">
            <ol>
                <li>访客一次只能登录一个账号。</li>
            </ol>
        </td>
    </tr>
</table>