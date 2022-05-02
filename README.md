<?php
// connessione al DBMS
$conn = mysqli_connect("localhost", "pippo", "xxxxxx", "dbDati");
// controllo sullo stato della connessione
if (mysqli_connect_errno($conn))
echo "Errore, Impossibile effettuare la connessione".mysqli_connect_error($conn);

else
{
// query per la creazione di una tabella
$result = mysqli_query($conn, "CREATE TABLE prova (id INT(2), nome TEXT(50))")
if ($result)
echo "Tabella creata con successo";

}
// liberazione della memoria dal risultato della query
mysqli_free_result($result);
// chiusura della connessione
mysqli_close($conn);
?>
