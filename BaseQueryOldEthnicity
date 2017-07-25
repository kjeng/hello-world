 SELECT
 CASE WHEN stu.is_hispanic = 't' OR e.code_translation = 'Hispanic'
    THEN 'Hispanic'
  ELSE
    (CASE WHEN e.code_translation = 'Filipino'
               OR e.code_translation = 'Other Asian'
               OR e.code_translation = 'Cambodian'
               OR e.code_translation = 'Laotian'
               OR e.code_translation = 'Asian Indian'
               OR e.code_translation = 'Vietnamese'
               OR e.code_translation = 'Korean'
               OR e.code_translation = 'Japanese'
               OR e.code_translation = 'Chinese'
               OR e.code_translation = 'Hmong'
               OR e.code_translation = 'Other Pacific Islander'
               OR e.code_translation = 'Tahitian'
               OR e.code_translation = 'Samoan'
               OR e.code_translation = 'Guamanian'
               OR e.code_translation = 'Hawaiian'
      THEN 'Asian or Pacific Islander'
     ELSE e.code_translation END) END               AS ethnicity
     FROM public.students stu
     LEFT JOIN codes.ethnicity e ON e.code_id = stu.primary_ethnicity
