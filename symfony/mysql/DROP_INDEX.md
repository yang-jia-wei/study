## drop index
- 删除索引

		ALTER TABLE table_name DROP INDEX IDX_29791883B30676A7;
- 删除外键

		SET FOREIGN_KEY_CHECKS=0;
        ALTER TABLE information DROP FOREIGN KEY FK_29791883B30676A7;
        SET FOREIGN_KEY_CHECKS=1;