# 用例规约表设计

## table_lesson_score.md（计算课程平均成绩用例规约表）

<table>
    <caption>“计算课程平均成绩”用例规约</caption>
    <tr>
        <td>用例名称</td>
        <td>计算课程平均成绩</td>
    </tr>
    <tr>
        <td>参与者</td>
        <td>教师</td>
    </tr>
    <tr>
        <td>前置条件</td>
        <td>教师已登录，且已评阅完该课程至少一个实验的成绩</td>
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
            1. 教师提交实验的成绩；<br><br><br><br><br><br><br>
        </td>
        <td>
            <br>
            2. 系统验证教师登录状态是否有效；<br>
            3. 系统存储实验成绩；<br>
            4. 系统检索该学生已被评阅的实验成绩；<br>
            5. 系统计算学生已被评阅实验成绩的平均分；<br>
            6. 系统存储学生已被评阅实验成绩的平均分；<br>
            7. 系统提示计算课程平均成绩成功。
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
            3a. 系统存储实验成绩时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示存储实验成绩失败，转第1步；<br>
            4a. 系统检索学生已被评阅的实验成绩时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示检索实验成绩失败，转第1步；<br>
            6a. 系统存储课程平均成绩时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示计算课程平均成绩失败，转第1步。
    </tr>
    <tr>
        <td colspan="2">业务规则</td>
    </tr>
    <tr>
        <td colspan="2">
            <ol>
                <li>教师评阅各个实验评分项成绩由系统计算平均成绩；</li>
                <li>教师可以重复评阅一个实验的评分项分数，系统可以重复计算课程的平均成绩。</li>
            </ol>
        </td>
    </tr>
</table>