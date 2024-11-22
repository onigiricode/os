# OnigiriCode OS Plugin

Plugin ufficiale per le operazioni di sistema in OnigiriCode.

## Installazione

Aggiungi il plugin al tuo progetto usando mizu:

```bash
mizu add os
```

## Utilizzo

```onigiri
# Importa il plugin
IMPORT os

# Esempi di utilizzo
FUNC main() {
    # File system
    write_file("test.txt", "Hello, OnigiriCode!")
    LET content = read_file("test.txt")
    PRINT content

    # Info di sistema
    LET os = get_os()
    LET user = get_username()
    PRINT "Running on " + os + " as " + user

    # Variabili d'ambiente
    set_env("ONIGIRI_TEST", "value")
    LET env_var = get_env("ONIGIRI_TEST")
    PRINT env_var

    # Processi
    LET output = execute("echo Hello from shell")
    PRINT output
}
```

## API Reference

### File System
- `read_file(path: String) -> String`: Legge il contenuto di un file
- `write_file(path: String, content: String) -> Bool`: Scrive contenuto in un file
- `delete_file(path: String) -> Bool`: Elimina un file
- `file_exists(path: String) -> Bool`: Verifica se un file esiste
- `create_dir(path: String) -> Bool`: Crea una directory
- `delete_dir(path: String) -> Bool`: Elimina una directory
- `list_dir(path: String) -> List`: Lista i contenuti di una directory

### Sistema
- `get_env(name: String) -> String`: Ottiene una variabile d'ambiente
- `set_env(name: String, value: String) -> Bool`: Imposta una variabile d'ambiente
- `get_os() -> String`: Ottiene il nome del sistema operativo
- `get_hostname() -> String`: Ottiene il nome dell'host
- `get_username() -> String`: Ottiene il nome utente
- `get_home_dir() -> String`: Ottiene la directory home dell'utente

### Processi
- `execute(command: String) -> String`: Esegue un comando di shell
- `get_pid() -> Number`: Ottiene il PID del processo corrente
- `sleep(ms: Number) -> Void`: Mette in pausa l'esecuzione per i millisecondi specificati

## Licenza

MIT License
