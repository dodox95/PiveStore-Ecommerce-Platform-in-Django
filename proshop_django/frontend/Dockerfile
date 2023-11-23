# Użyj obrazu Node.js w wersji 16
FROM node:16

# Ustaw katalog roboczy w kontenerze
WORKDIR /app

# Skopiuj package.json i package-lock.json
COPY package.json /app/
COPY package-lock.json /app/

# Zainstaluj zależności
RUN npm install

# Skopiuj pozostałe pliki projektu
COPY . /app/

# Uruchom aplikację React na porcie 3000
EXPOSE 3000
CMD ["npm", "start"]
