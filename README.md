# hello-world
--testing procedure

CREATE OR REPLACE PROCEDURE FINEDING_IDENT (ident varchar2) IS

fullName varchar2(500);

BEGIN
  select ind.cr51_ind_name || ' ' || ind.cr51_ind_surname INTO fullName
  from tr51Ind ind
  where ind.cr51_ind_pin = ident;
  
  DBMS_OUTPUT.PUT_LINE('Name: '|| fullName);
END FINEDING_IDENT;

