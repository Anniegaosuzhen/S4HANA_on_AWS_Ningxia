
2008年开始SAP成为AWS云服务的用户并使用AWS云服务来部署相关的SAP开发以及测试系统。2012年11月AWS宣布SAP Business Suite解决方案被认证在AWS上全面支持客户产品部署。 2017年SAP开始在HANA Enterprise Cloud、SAP Cloud Platform、S/4 HANA Cloud Edition等平台上基于AWS提供了多种方式支持客户运行他们的系统，客户可以采用按需实例的模式部署SAP DEV/QAS环境，也可以使用预留实例的方式使用SAP PRD环境。AWS帮助SAP客户在云端运行SAP S/4 HANA，客户当前只需要每小时很低的价格就可以运行被SAP官方认证的可以支持产品环境的实例，来安装SAP HANA软件。
客户使用AWS Cloudformation，AWS提供了SAP一键部署的代码，帮助SAP客户可以实现SAP系统IDES，以及开发测试环境的一键部署。 
FAQ
•	问：什么样的场景下会采用这个方案?
在SAP实施项目的前期，希望对SAP S/4系统有基本的了解和认识，亦或在产品选型阶段需要对SAP S/4系统进行重点功能验证工作。
•	问：该方案的优势和特点有哪些？ 
按照传统的SAP实施项目，在前期需要安装IDES系统进行初级培训和功能验证工作，由此产生的工作如准备IDES服务器,下载IDES安装介质以及系统安装部署等。采用这个方案，则仅需要开通在AWS账号情况下，通过AWS CloudFormation功能，采用向导式的方式就可以快速创建SAP S/4系统实例，基本不需要专业的SAP Basis技能即可轻松开始SAP之旅。
操作步骤(TODO)
1.	准备AWS宁夏区域账户和启动EC2实例
 	
	
2.	创建新的密钥对，以便能够通过安全的方式访问系统实例
 
3.	启动SAP S/4 HANA系统实例
A．启动CloudFormation，然后通过AMI模板来创建堆栈
 

 
4.	实例创建成功后，通过SSH工具登陆操作系统然后启动SAP HANA DB和SAP Application
 
5.	服务启动完成后，分别采用SAP GUI和Fiori客户端登陆系统进行测试（第一次登陆系统时间会比较长一点，请您耐心等待）
a.	SAP GUI参数配置
 
b.	SAP Fiori客户端地址（红色部分需要替换成EC2实例的公网IP地址）
https://xx.xx.xx.xx:44300/sap/bc/ui5_ui5/ui2/ushell/shells/abap/FioriLaunchpad.html#Shell-home 
