# 用例规约表设计

## table_score_plagiarize.md（检查是否抄袭用例规约表）

<table>
    <caption>“检查是否抄袭”用例规约</caption>
    <tr>
        <td>用例名称</td>
        <td>检查是否抄袭</td>
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
            4. 教师填写该实验是否抄袭；<br>
            5. 教师点击提交按钮；<br><br><br><br><br>
        </td>
        <td>
            <br>
            2. 系统验证教师登录状态是否有效；<br>
            3. 系统跳转至实验评分页面；<br><br><br>
            6. 系统存储实验是否抄袭的结果；<br>
            7. 系统提示评阅实验是否抄袭成功。
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
            5a. 教师选择返回，放弃检查实验是否抄袭<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统跳转至实验的学生列表页面，转第1步；<br>
            6a. 系统存储实验是否抄袭时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示检查是否抄袭失败，转第5步。
        </td>
    </tr>
    <tr>
        <td colspan="2">业务规则</td>
    </tr>
    <tr>
        <td colspan="2">
            <ol>
                <li>教师一次只能评阅一个课程中一个学生的一个实验；</li>
                <li>教师可以重复评阅一个实验是否抄袭。</li>
            </ol>
        </td>
    </tr>
</table>