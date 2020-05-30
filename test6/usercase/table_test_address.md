# 用例规约表设计

## table_test_address.md（修改实验地址用例规约表）

<table>
    <caption>“修改实验地址”用例规约</caption>
    <tr>
        <td>用例名称</td>
        <td>修改实验地址</td>
    </tr>
    <tr>
        <td>参与者</td>
        <td>学生</td>
    </tr>
    <tr>
        <td>前置条件</td>
        <td>学生已登录，并进入课程主页</td>
    </tr>
    <tr>
        <td>后置条件</td>
        <td>系统跳转至课程页面</td>
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
            1. 学生选择正在进行的课程；<br><br><br><br><br>
            6. 学生选择实验；<br>
            7. 学生填写实验结果的github地址；<br>
            8. 学生点击提交按钮；<br><br><br><br>
        </td>
        <td>
            <br>
            2. 系统验证学生登录状态是否有效；<br>
            3. 系统检索课程正在进行的实验；<br>
            4. 系统返回实验列表；<br>
            5. 系统跳转至实验列表页面；<br><br><br><br>
            9. 系统检验学生提交的github地址是否合法；<br>
            10.系统存储实验的github地址；<br>
            11.系统提示修改实验地址成功。
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
            3a. 系统未检索到课程正在进行的实验<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示无实验正在进行，转第1步；<br>
            3b. 系统在检索课程时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示检索课程失败，转第1步；<br>
            6a. 学生选择返回，放弃选择实验<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统跳转至实验管理平台首页，转第1步；<br>
            8a. 学生选择返回，放弃修改实验github地址<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统跳转至实验列表，转第6步；<br>
            9a. 系统检测到github地址非法<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示github地址非法，转第7步；<br>
            10a.系统储存github地址时出现系统故障<br>
                &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
                1. 系统提示修改github地址失败，转第8步。
        </td>
    </tr>
    <tr>
        <td colspan="2">业务规则</td>
    </tr>
    <tr>
        <td colspan="2">
            <ol>
                <li>学生一次只能选择一个课程的一个实验；</li>
                <li>学生一次只能填写一个github地址；</li>
                <li>学生可以重复修改一个实验的github地址。</li>
            </ol>
        </td>
    </tr>
</table>