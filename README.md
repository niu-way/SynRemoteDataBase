# SynRemoteDataBase
为解决 timesten 不同版本间的数据同步问题，进而也提供了对mysql以及oracle的支持，仅同步数据，数据模型等数据对象不提供同步
同时支持相同数据模型不同数据库间的同步问题，如mysql 与 oracle 数据库间的同步

 	 * args[0] 配置文件config.xml的路径
	 * args[1] 需要同步的表名，如果同步此用户下的所有的表记录，输入：ALLTABLES，如果是其他名称则只同步给定的表名，表名之间用逗号分割，如：doc,role
	 * args[2] 启动的同步线程个数，任务分配不精细到记录数来分配任务线程，直接根据表的个数来分配
	 * args[3] 单表单个线程最大的导入记录数，当单表的记录超过此值时，将启动多个线程进行操作，默认为100000
	 
内置了部分版本的oracle、mysql以及timesten 驱动，java -jar SynRemoteDataBase.jar f:/config.xml users,roles 20 30000

代码是很早之前写的很乱，欢迎大家优化

