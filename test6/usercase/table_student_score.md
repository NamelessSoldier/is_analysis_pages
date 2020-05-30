# 用例规约表设计

## table_student_score.md（查看成绩用例规约表）

<table>
    <caption>“查看成绩”用例规约</caption>
    <tr>
        <td>用例名称</td>
        <td>查看成绩</td>
    </tr>
    <tr>
        <td>参与者</td>
        <td>学生</td>
    </tr>
    <tr>
        <td>前置条件</td>
        <td>学生已登录</td>
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
            1. 学生点击查看成绩按钮；<br><br><br><br><br>
        <td>
            <br>
            2. 系统验证学生登录状态是否有效；<br>
            3. 系统检索学生的各课程成绩；<br>
            4. 系统计算学生的各课程平均成绩；<br>
            5. 系统返回该学生的各课程成绩及平均成绩。
        </td>
    </tr>
    <tr>
        <td colspan="2">备选事件流</td>
    </tr>
    <tr>
        <td colspan="2">
            2a. 系统验证学生登录状态已失效<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示验证学生登录状态失败，转第1步；<br>
            3a. 系统未检索到学生各课程成绩<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示暂未进行实验或教师暂未评阅，转第1步；<br>
            3b. 系统检索学生各课程成绩时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示检索学生成绩失败，转第1步。
    </tr>
    <tr>
        <td colspan="2">业务规则</td>
    </tr>
    <tr>
        <td colspan="2">
            <ol>
                <li>学生可以查看其它学生的成绩，</li>
                <li>学生的各课程平均成绩由系统自动计算。</li>
            </ol>
        </td>
    </tr>
</table>