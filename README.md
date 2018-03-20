DECLARE v_y bigint(1)/varchar()/... DEFAULT 0/"..."/... ;

DECLARE finished BOOL DEFAULT FALSE;

DECLARE x_iterater CURSOR FOR ( Select ... );

DECLARE CONTINUE HANDLER FOR NOT FOUND SET finished = TRUE;
  
OPEN x_iterater; 
repeat FETCH x_iterater INTO v_y ;

IF NOT finished THEN

Example//
update ...
set ...
where ... = v_y ;
//

END IF;
UNTIL finished END REPEAT;
CLOSE x_iterater;




