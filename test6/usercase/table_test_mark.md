# 用例规约表设计

## table_test_mark.md（评阅实验用例规约表）

<table>
    <caption>“评阅实验”用例规约</caption>
    <tr>
        <td>用例名称</td>
        <td>评阅实验</td>
    </tr>
    <tr>
        <td>参与者</td>
        <td>教师</td>
    </tr>
    <tr>
        <td>前置条件</td>
        <td>教师已登录，并进入课程实验页面，获取到学生列表</td>
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
             教师选择学生；<br>
             教师填写实验的概念分数；<br>
             教师填写实验的语言分数；<br>
             教师填写实验的结构分数；<br>
             教师填写实验的条理分数；<br>
             教师填写实验的逻辑分数；<br>
             教师填写对该实验的评语；<br>
             教师点击提交按钮；<br><br><br><br><br><br><br>
        </td>
        <td>
             系统验证教师登录状态是否有效；<br>
             系统跳转至实验评分页面；<br>
             系统检测评分项分数是否大于0；<br>
             系统检测评分项是否小于20；<br>
             系统将各评分项成绩相加得实验成绩；<br>
             系统存储实验成绩与评语；<br>
             系统提示评阅实验成绩成功。
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
            11a.教师选择返回，放弃评阅结构分数<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统跳转至实验的学生列表页面，转第1步；<br>
            12a.系统检测到评分项分数为负<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示评分项分数必须为正，转第4步；<br>
            13a.系统检测到评分项分数大于20<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示评分项分数必须小于20，转第4步；<br>
            14a.系统存储实验成绩与评语时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示评阅实验成绩失败，转第10步。
        </td>
    </tr>
    <tr>
        <td colspan="2">业务规则</td>
    </tr>
    <tr>
        <td colspan="2">
            <ol>
                <li>教师一次只能评阅一个课程中一个学生的一个实验；</li>
                <li>教师填写的评分项分数必须为正，且小于20；</li>
                <li>教师可评阅该实验抄袭则实验成绩直接计0；</li>
                <li>教师评阅的评分项分数由系统直接计算得实验总成绩；</li>
                <li>教师可以重复评阅一个实验的评分项分数。</li>
            </ol>
        </td>
    </tr>
</table>