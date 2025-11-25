
#string :=CONCAT(IN1 := "DB_Reader".Current_OUT_Read, IN2 := #help_byte);


#word := ATH(IN := "DB_Reader".Current_OUT_Read, N := 16, OUT => #help_word);

Strg_TO_Chars(Strg := "DB_Reader".Current_OUT_Read,
              pChars := "DB_LEARN"."pointer",
              Cnt => "DB_LEARN".count,
              Chars := "DB_LEARN".array_chars);


#Y := UINT_TO_INT(IN := "DB_LEARN".count);
"DB_LEARN".RESULT := '';
FOR #i := 1 TO #Y DO
    
  
    "DB_LEARN".HELP :=
    CHAR_TO_STRING("DB_LEARN".array_chars[#i]);
    
  
    "DB_LEARN".RESULT :=
    CONCAT(IN1 := "DB_LEARN".RESULT,
           IN2 := "DB_LEARN".HELP);
    
END_FOR;


	count	UInt	0.0	0	False	True	True	True	False	
	pointer	DInt	2.0	0	False	True	True	True	False	
	array_chars	Array[1..16] of Char	6.0		False	True	True	True	False	
	word	Word	22.0	16#0	False	True	True	True	False	
	string	String	24.0	''	False	True	True	True	False	
	help_char	Char	280.0	' '	False	True	True	True	False	
	help_word	Word	282.0	16#0	False	True	True	True	False	
	help_string	String	284.0	''	False	True	True	True	False	
	help_byte_	Byte	540.0	16#0	False	True	True	True	False	
	RESULT	String	542.0	''	False	True	True	True	False	
	HELP	String	798.0	''	False	True	True	True	False	
										
