# Zapisy na kurs

Formularz z ośmioma polami: EditText, przycisk z DatePickerDialog, Spinner,
RadioGroup, SeekBar, Switch, CheckBox. Walidacja z setError, potwierdzenie
w AlertDialog i Snackbar z cofnięciem.


## Dlaczego przy SeekBar nie dało się użyć lambdy, a przy CheckBox tak?

Lambda działa tylko wtedy, gdy interfejs ma dokładnie jedną metodę.
CheckBox używa OnCheckedChangeListener z jedną metodą (onCheckedChanged),
więc można ją zastąpić lambdą. SeekBar używa OnSeekBarChangeListener,
który ma trzy metody (onProgressChanged, onStartTrackingTouch,
onStopTrackingTouch), więc trzeba napisać klasę anonimową i zaimplementować
wszystkie trzy, nawet jeśli dwie zostają puste.