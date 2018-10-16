##第一次实验：
#查询1：

![image](https://github.com/wk-king/Oracle/blob/master/1.PNG)
有优化建议

#查询2：
![image](https://github.com/wk-king/Oracle/blob/master/2.PNG)
无优化建议

由此可知，结果表明，查询2更优

#新查询语句：
SELECT d.department_name，count(e.job_id)as "部门总人数"，
avg(e.salary)as "平均工资"
FROM hr.departments d，hr.employees e
WHERE d.department_id = e.department_id
and d.department_name = 'IT' or d.department_name = 'Sales'
GROUP BY department_name