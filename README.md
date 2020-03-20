大学生专业学科竞赛项目过程管理系统  
 ============================  
**项目说明**  

``大学生专业学科竞赛项目过程管理系统 ``  

**构建项目**

1.运行命令:`mvn clean package`  
2.构建镜像:`docker build -t mikeyboom/pmsocspscs .`  
3.推送仓库:`docker push mikeyboom/pmsocspscs`  

**部署项目**  

1.下拉项目:`git clone https://github.com/mikeygithub/pmsocspscs.git`  
2.打开项目:`cd pmsocspscs`  
3.授权脚本:`chomd +x run.sh`  
4.起飞项目:`./run.sh`   



<details>
  <summary>业务需求</summary>
<br> 
   <ul>
      <li>
        <h2>某大学拟开发一套大学生专业学科竞赛项目过程管理系统,实现全校专业学 科竞赛项目从立项到结题的过程管理其需求描述如下:</h2>
      </li>
      <li>
        <h2>(一)项目立项过程:</h2></li>
        <li>
          <h3>1)填写项目立项申请</h3>
          二级学院作为组赛单位报送每年专业学科竞赛项目。
          组赛单位的指导老师每年在线填写参加专业学科竞赛项目立项申请信息,然后从系
          统导出并打印项目立项申请书,将签字盖章后的项目立项申请书扫描为 PDF 文档
          并作为佐证附件上传到系统,最后将立项申请提交给教务处实验实践科审核,项目
          立项申请信息分为项目基本信息和经费预算信息两部分,其中项目基本信息包括赛
          事名称、组赛单位、赛制(单人赛、团队赛)、项目负责人、联系电话、电子邮件、
          竞赛起始日期、竞赛结束日期、专业、竞赛主办单位、竞赛承办单位、申请立项日
          期、论证组赛的目的和意义、竞赛邀请函或通知附件;
        </li>
      <li>
        <h4>经费预算表</h4>
        <table>
          <tr>
            <th>参赛注册费</th>
            <th>差旅费</th>
            <th>培训费</th>
            <th>指导费</th>
            <th>耗材费</th>
            <th>教师奖金</th>
            <th>其它</th>
            <th>合计</th>
          </tr>
          <tr>
            <td>0</td>
            <td>5000</td>
            <td>0</td>
            <td>0</td>
            <td>0</td>
            <td>0</td>
            <td>2000</td>
            <td>7000</td>
          </tr>
        </table>
      </li>
      <li>
        <h3>2)审核项目立项申请</h3>教务处实验实践科工作人员可以在线审核项目立项
        申请内容。如果审核不通过,需填写审核意见并回退给指导老师。指导老师可以删
        除自己的项目立项申请,但是不能删除已经审核通过的立项申请。
      </li>
      <li>
        <h2>(二)填写报名过程:</h2>报名参赛方式分为个人赛和团队赛,指导老师填写参赛报名信息。参赛报名信
        息分为团队信息和团队成员信息,团队信息包括团队编号、项目编号、赛题、报名
        时间等,团队成员信息包括编号、团队编号、学号、姓名、学院、班级、年级、专
        业、邮箱、手机号等。
      </li>
      <li>
        <h2>(三)项目结题过程</h2>
        <h3>1)填写项目结题申请</h3>比赛结束后,指导老师需在线填写各参赛队伍的获
        奖情况和资金实际使用情况,并上传结题报告书 PDF 扫描件。获奖情况包括获奖
        名次(特等奖、一等奖、二等奖、三等奖、优秀奖、无)和级别(国家级、区级
        等);
      </li>
      <li><table>
      <tr>
        <th>参赛注册费</th>
        <th>差旅费</th>
        <th>培训费</th>
        <th>评审费</th>
        <th>指导费</th>
        <th>领队费</th>
        <th>组织费</th>
        <th>奖金</th>
        <th>耗材费</th>
        <th>合计</th>
      </tr>
        <tr>
          <td>0</td>
          <td>0</td>
          <td>0</td>
          <td>0</td>
          <td>0</td>
          <td>0</td>
          <td>0</td>
          <td>1000</td>
          <td>0</td>
          <td>1000</td>
      </tr>
      </table></li>
      <li>
        2)审核项目结题申请。教务处实验实践科工作人员审核结题申请内容,并填
        写审核意见。如果申请内容有问题则结题申请退回给组赛的指导老师,经组
        赛指导老师修改后重新提交。
        教务处实验实践科工作人员可以统计竞赛立项情况、获奖情况。
      </li>
    </ul>
</details>    

## 技术要求

### 必选技术: (封顶70分)

>1开发技 术必须采用SpringBoot  
2前端技 术采用Vue

### 可选技术(加分项，每项10分，封顶30分)

>1数据库采用集群技术 [已采用]   
2使用NaSQL技术 (非关系数据库，比如高速缓存，附件的管理) [已采用] 
3使用RestFul服务 (分布式改造)[已采用]  
4使用消息服务(构建第三方服务，并用消息中间件调用)  
5应用健康监控(各层的性能监控) [已采用] 
6应用微信小程序(结合Springboot/RestFul进行后台服务调用)  


### 技术架构

#### 后台

> springboot +  mybaits plus + druid + redis + mysql cluster + docker/docker-compose + shiro + swagger

#### 监控

> Prometheus + grafana + cadvisor + node-exporter

#### 前端

> vue 全家桶 + ElementUI + axios