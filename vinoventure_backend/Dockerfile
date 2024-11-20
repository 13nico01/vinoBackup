# Basis-Image für Node.js
FROM node:18

# Arbeitsverzeichnis setzen
WORKDIR /app

# Nur package.json und package-lock.json kopieren (für effizientes Caching)
COPY package*.json ./

# Abhängigkeiten installieren
RUN npm install

# Restliche Dateien kopieren
COPY . .

# Anwendung bauen (z. B. bei TypeScript-Projekten oder Build-Schritt nötig)
RUN npm run build

# Container-Port freigeben
EXPOSE 3000

# Startbefehl für die Anwendung
CMD ["npm", "start"]
