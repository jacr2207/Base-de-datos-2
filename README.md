# Base-de-datos-2

begin;
create temporary table task_media as 
select * from tasks t where pid = 2;
select ta.tid,ta.title, p.p_name from task_media ta
join priorities p on ta.pid = p.pid 
commit;
