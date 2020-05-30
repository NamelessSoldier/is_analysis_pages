# 用例规约表设计

## table_score_structure.md（评阅结构分数用例规约表）

<table>
    <caption>“评阅结构分数”用例规约</caption>
    <tr>
        <td>用例名称</td>
        <td>评阅结构分数</td>
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
            1. 教师选择学生；<br><br><br>
            4. 教师填写实验的结构分数；<br>
            5. 教师点击提交按钮；<br><br><br><br><br>
        </td>
        <td>
            <br>
            2. 系统验证教师登录状态是否有效；<br>
            3. 系统跳转至实验评分页面；<br><br><br>
            6. 系统检测结构分数是否大于0；<br>
            7. 系统检测结构分数是否小于20；<br>
            8. 系统存储评阅的结构分数；<br>
            9. 系统提示评阅实验的结构分数成功。
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
            5a. 教师选择返回，放弃评阅结构分数<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统跳转至实验的学生列表页面，转第1步；<br>
            6a. 系统检测到结构分数为负<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示结构分数必须为正，转第4步；<br>
            7a. 系统检测到结构分数大于20<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示结构分数必须小于20，转第4步；<br>
            8a. 系统存储实验的结构分数时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示评阅结构分数失败，转第5步。
        </td>
    </tr>
    <tr>
        <td colspan="2">业务规则</td>
    </tr>
    <tr>
        <td colspan="2">
            <ol>
                <li>教师一次只能评阅一个课程中一个学生的一个实验；</li>
                <li>教师填写的结构分数必须为正，且小于20；</li>
                <li>教师可以重复评阅一个实验的结构分数。</li>
            </ol>
        </td>
    </tr>
</table>