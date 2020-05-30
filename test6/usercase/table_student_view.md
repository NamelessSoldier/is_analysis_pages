# 用例规约表设计

## table_student_view.md（查看学生列表用例规约表）

<table>
    <caption>“查看学生列表”用例规约</caption>
    <tr>
        <td>用例名称</td>
        <td>查看学生列表</td>
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
        <td>系统跳转至实验的学生列表页面</td>
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
            1. 教师点击获取学生列表按钮；<br><br><br><br>
        <td>
            <br>
            2. 系统验证教师登录状态是否有效；<br>
            3. 系统检索该课程的所有学生列表；<br>
            4. 系统返回课程的所有学生列表。
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
            3a. 系统未检索到参加该课程的学生<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示未检索到学生，转第1步；<br>
            3b. 系统检索学生时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示检索学生失败，转第1步。
    </tr>
    <tr>
        <td colspan="2">业务规则</td>
    </tr>
    <tr>
        <td colspan="2">
            <ol>
                <li>教师评一次只能检索一个课程的所有学生；</li>
                <li>教师只能查看自己有评阅权限的课程的学生。</li>
            </ol>
        </td>
    </tr>
</table>