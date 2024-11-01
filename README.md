# Projektinstallation und -Ausführung

In dieser Anleitung werden alle Schritte beschrieben, um das Projekt zu installieren und in einem Docker-Container auszuführen.

## Installationsschritte

### 1. Repository klonen

Klonen Sie das Repository lokal und wechseln Sie in das Projektverzeichnis:

```bash
git clone <URL-des-Repositories>
cd <Projektverzeichnis>
```

> Ersetzen Sie `<URL-des-Repositories>` durch die URL des Repositories und `<Projektverzeichnis>` durch den Namen des Projektordners.

### 2. Notwendige Pakete installieren

Befehl im package.jason hinzufügen. (Im Bereich: "scripts")

```bash
"start": "node src/index.js"
```

### 3. Docker konfigurieren und installieren

Stellen Sie sicher, dass Docker auf Ihrem System installiert ist. Anweisungen zur Installation finden Sie auf der [Docker-Webseite](https://docs.docker.com/get-docker/).

### 4. Applikation in einem Docker-Container starten

Führen Sie die folgenden Befehle aus, um die Applikation in einem Docker-Container bereitzustellen und zu starten:

1. **Docker-Image erstellen**:

    ```bash
    docker build -t projekt-image .
    ```

2. **Docker-Container starten**:
    ```bash
    docker run -p 3000:3000 projekt-image
    ```

Die Applikation ist nun unter `http://localhost:3000` verfügbar.

## Anwendung starten

Nach dem Starten des Containers kann die Anwendung im Browser aufgerufen werden:

-   Gehen Sie zu `http://localhost:3000`, um die Applikation zu verwenden.
