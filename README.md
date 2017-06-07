### select

  ```
  select * from employee where empid = '1001';
  db.employee.find({'empid':'1001'})
  ```
  
  ```
  select empname,empdob from employee where empid = '1001';
  db.employee.find({'empid':'1001'},{empname:1,empdob:1,_id:0)
  ```

### bulk update


  ```
  var bulk = db.<collectionname>.initializeUnorderedBulkOp();
  bulk.find( { <column:value> } ).update( { $set: { <column:value>  } } );
  bulk.find( { <column:value>  } ).update( { $set: { <column:value>  } } );
  ...
  bulk.execute();
  ```
  
  
### like (regex)

  ```
  select * from employee where username like '%kumar'
  db.employee.find({'empname':{ $regex: /kumar/i}}
  ```
