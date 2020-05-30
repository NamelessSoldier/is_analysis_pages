# 用例规约表设计

## table_logout.md（登出用例规约表）

<table>
    <caption>“登出”用例规约</caption>
    <tr>
        <td>用例名称</td>
        <td>登出</td>
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
            1. 用户点击登出按钮；<br><br>
            3. 用户点击确认登出按钮；<br><br><br><br>
        </td>
        <td>
            <br>
            2. 系统提示是否确认登出；<br><br>
            4. 系统清除用户的登录信息；<br>
            5. 系统清除客户端登录信息cookie;<br>
            6. 系统提示用户登出成功。
        </td>
    </tr>
    <tr>
        <td colspan="2">备选事件流</td>
    </tr>
    <tr>
        <td colspan="2">
            1a. 用户登录之后，长时间不操作界面<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统默认登出，转第4步；<br>
            3a. 用户选择取消登出<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统返回用户个人主页，转第1步；<br>
            4a. 系统清楚用户登录信息时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示登出失败，转第1步；<br>
            5a. 系统清楚cookie信息时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示清楚cookie信息失败，转第1步。
        </td>
    </tr>
    <tr>
        <td colspan="2">业务规则</td>
    </tr>
    <tr>
        <td colspan="2">
            <ol>
                <li>用户对于已经登录的账户只能登出一次。</li>
            </ol>
        </td>
    </tr>
</table>