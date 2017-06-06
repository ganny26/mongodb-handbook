### select

  ```
  select * from employee where empid = '1001';
  db.employee.find({'empid':'1001'})
  ```
  
  ```
  select empname,empdob from employee where empid = '1001';
  db.employee.find({'empid':'1001'},{empname:1,empdob:1,_id:0)
  ```
