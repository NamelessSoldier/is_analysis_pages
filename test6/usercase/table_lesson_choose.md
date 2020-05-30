# 用例规约表设计

## table_lesson_choose.md（选课用例规约表）

<table>
    <caption>“选课”用例规约</caption>
    <tr>
        <td>用例名称</td>
        <td>选课</td>
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
            1. 学生点击选课按钮；<br><br><br><br><br>
            6. 学生选择课程；<br>
            7. 学生点击提交按钮；<br><br><br>
        </td>
        <td>
            <br>
            2. 系统验证学生登录状态是否有效；<br>
            3. 系统检索能够被学生选择的课程；<br>
            4. 系统返回课程列表；<br>
            5. 系统跳转至选课页面；<br><br><br>
            8. 系统存储学生选择的课程；<br>
            9. 系统提示选课成功。
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
            4a. 系统未能检索到能够被学生选择的课程<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示无可选课程，转第1步；<br>
            4b. 系统在检索课程时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示检索课程失败，转第1步；<br>
            7a. 学生选择返回，放弃选课<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统跳转至实验管理平台首页，转第1步；<br>
            8a. 系统存储选课结果时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示提交选课失败，转第7步。
        </td>
    </tr>
    <tr>
        <td colspan="2">业务规则</td>
    </tr>
    <tr>
        <td colspan="2">
            <ol>
                <li>学生一次只能选择一个课程；</li>
                <li>学生只能选择其能够选择的课程。</li>
            </ol>
        </td>
    </tr>
</table>