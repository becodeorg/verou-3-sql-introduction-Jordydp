# verou-3-sql-introduction-Jordydp

## try the following selects 
    Get all data from the groups*
        SELECT * FROM `groups`;
    Get the name and email of the first learner, and alias the name to learner_name*
        select NAME, email from learners where id=1;
        select NAME AS learner_name
        from learners where id = 1;
## 💩 happens - a group needs to be postponed 
    Update the start date of the first_group (make it two months later)*
        UPDATE `groups`
        set start_date = '1992-03-10'
        where id = 1; 
    Introduce a new field status which can contain a long text indicating the reason for postponing (bonus points if it's a creative one)
        alter TABLE `groups`
        add Status TEXT;
        UPDATE `groups`
        set Status = 'coach is having a second baby and he left the country'
        WHERE id = 1;
    One of the learners changed his/her mind and decided to be an astronaut
    Delete someone from the learners table*
        delete from learners WHERE id = 2;
    A learner belongs to a group, and a group has a coach
    Find a technique to make this connection in the database (what of the field is unique to a record, so we can refer to it?) (WIP)
        alter TABLE coaches
        add group_id bigint(20) unsigned;
        alter table learners
        add group_id bigint(20) unsigned;
        alter table `groups`
        add coach_id;




