# DSR_25
### DSR选项头格式如下：  
它的首部采用扩展性良好的TLV格式。除固定部分外，不同类型的选项(option)以TLV格式附加在固定部分之后。   
选项的种类包括：  
路由请求(Route Request)  
路由应答(Route Reply)  
确认请求(ACK Request)  
确认(ACK)  
源路由(Source Route)  



	dsr.h	dsr_node定义，结构，初始化，配置变量  
	dsr-srt.h  Source route options srt选项结构，srt结构，打印srt,下一跳，上一跳，增加，新建，分割，接收  
	dsr-srt.c   对srt一通操作  
	dsr-rerr.h rerr:路由出错报文，错误分组。 错误分组选项结构，未抵达节点信息，
	dsr-rerr.c  add send recv
	dsr-module.c  接收ip iperro  ipforward 读写配置程序
	dsr-dev.c  dsr的网络设备 启动、初始化、触发事件、接收包、运送、停止、清空
	dsr-opt.h  dsr-opt, dsr-opt-hdr, 结构
	dsr-opt.c 增删查接收分析dsr opt  build IP 
	dsr-ack.h  ack请求选项以及ack选项的构成 
	dsr-ack.c  添加ack，发送ack，产生请求，发送请求，接收请求，接收ack
	dsr-io.c     接收dsr opt 开始发送
	dsr-pkt.h	  产生内部的dsr pkt
	dsr-pkt.c 	  pkt以及pkt opt的产生，扩展，删除
	dsr-rrep.h  rrep路由应答，rrep选项结构，发送接收，rrep table操作
	dsr-rrep.c  对rrep包和table的操作
	dsr-rreq.h  rreq请求的opt的结构
	dsr-rreq.c  rreq加入table中，entry结果，一通操作
	dsr-rtc.h  DSR route cache API 查增删冲洗
	dsr-rtc-simple.c rtc entry一通操作
	link-cache.c lc的node link 增删改查，更新开销，垃圾回收，输出cost
	maint-buf.c 用于处理pre hop -> next hop之间时的信息传送所用buf
	neigh.c 邻节点的结构、增删改查、系统崩溃恢复时间，邻节点表的维护
	send-buf.c 增删改查send buf 

	
	

