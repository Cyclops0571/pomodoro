# pomodoro

Create a database with Pomodoro name and create record and user tables 
with these sqls and edit config.php file for database authentication: 

DROP TABLE IF EXISTS `record`;

CREATE TABLE `record` (
  `username` varchar(255) NOT NULL DEFAULT '',
  `date` date NOT NULL DEFAULT '2017-01-01',
  `success` int(11) DEFAULT NULL,
  `fail` int(11) DEFAULT NULL,
  PRIMARY KEY (`username`,`date`)
) ENGINE=MyISAM DEFAULT CHARSET=utf8;

DROP TABLE IF EXISTS `user`;

CREATE TABLE `user` (
  `username` varchar(255) NOT NULL,
  `status` varchar(10) DEFAULT NULL,
  `begin` int(11) DEFAULT NULL,
  PRIMARY KEY (`username`)
) ENGINE=MyISAM DEFAULT CHARSET=utf8;
