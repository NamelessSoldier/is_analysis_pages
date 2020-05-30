# 用例规约表设计

## table_lesson_maintain.md（维护课程用例规约表）

<table>
    <caption>“维护课程”用例规约</caption>
    <tr>
        <td>用例名称</td>
        <td>维护课程</td>
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
        <td>系统跳转至课程实验页面</td>
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
            1. 教师点击排课按钮；<br><br><br>
            4. 教师选择科目；<br>
            5. 教师填写课程开课年份；<br>
            6. 教师填写课程开课学期；<br>
            7. 教师选择课程由学生自主选课或直接选择上课班级；<br>
            8. 教师点击提交按钮；<br><br><br><br>
        </td>
        <td>
            <br>
            2. 系统验证教师登录状态是否有效；<br>
            3. 系统跳转至排课页面；<br><br><br><br><br><br>
            9. 系统检测提交的课程信息是否合法；<br>
            10.系统存储课程信息；<br>
            11.系统提示排课成功。
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
            5a. 教师未填写开课年份<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示填写开课年份，转第5步；<br>
            6a. 教师未填写开课学期<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示填写开课学期，转第6步；<br>
            7a. 教师选择直接选择班级<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示教师选择上课班级；<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                2. 教师选择上课班级，转第8步；<br>
            8a. 教师选择返回，放弃排课<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统跳转至实验管理平台首页，转第1步；<br>
            9a. 系统检测到提交的课程信息非法<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示提交的课程信息非法，转第4步；<br>
            9b. 系统检测到开课年份在当前时间之前<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示填写的开课年份错误，转第5步；<br>
            10a.系统存储排课信息时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示排课失败，转第8步。
        </td>
    </tr>
    <tr>
        <td colspan="2">业务规则</td>
    </tr>
    <tr>
        <td colspan="2">
            <ol>
                <li>教师可以设置课程为学生选课或直接选择班级；</li>
                <li>教师一次只能排一门课；</li>
                <li>教师安排的课程信息必须合法；</li>
                <li>教师设置的开课年份必须在当前时间之后；</li>
            </ol>
        </td>
    </tr>
</table>