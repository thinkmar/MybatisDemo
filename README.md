# Mybatis例子
# 建表语句
```sql
CREATE TABLE `command` (
  `ID` int(11) NOT NULL AUTO_INCREMENT COMMENT '主键',
  `NAME` varchar(16) DEFAULT NULL COMMENT '指令名称',
  `DESCRIPTION` varchar(32) DEFAULT NULL COMMENT '描述',
  PRIMARY KEY (`ID`)
) ENGINE=InnoDB AUTO_INCREMENT=11 DEFAULT CHARSET=utf8;
INSERT INTO `command` VALUES ('9', '段子', '精彩段子');
INSERT INTO `command` VALUES ('10', '新闻', '中央新闻');

CREATE TABLE `command_content` (
  `ID` int(11) NOT NULL AUTO_INCREMENT COMMENT '主键',
  `CONTENT` varchar(256) DEFAULT NULL COMMENT '内容',
  `COMMAND_ID` int(11) DEFAULT NULL,
  PRIMARY KEY (`ID`)
) ENGINE=InnoDB AUTO_INCREMENT=13 DEFAULT CHARSET=utf8;

INSERT INTO `command_content` VALUES ('9', '小明的故事：小明家门口有条河，很难过。', '9');
INSERT INTO `command_content` VALUES ('10', '据可靠消息：大纪元。', '10');
INSERT INTO `command_content` VALUES ('11', '录音：“小明，今晚上有思修课呢！你去不去？”“我去！！你有病啊！！”——问：小明去不去思修课？', '9');
INSERT INTO `command_content` VALUES ('12', '录音：“小明，你饿不饿？我们晚上吃什么好呢？”“呃……我不饿……”——问：小明饿不饿？', '9');

CREATE TABLE `message` (
  `ID` int(11) NOT NULL AUTO_INCREMENT COMMENT '主键',
  `COMMAND` varchar(16) DEFAULT NULL COMMENT '指令名称',
  `DESCRIPTION` varchar(32) DEFAULT NULL COMMENT '描述',
  `CONTENT` varchar(2048) DEFAULT NULL COMMENT '内容',
  PRIMARY KEY (`ID`)
) ENGINE=InnoDB AUTO_INCREMENT=9 DEFAULT CHARSET=utf8;
```
