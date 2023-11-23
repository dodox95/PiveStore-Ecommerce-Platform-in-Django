# Użyj oficjalnego obrazu Pythona
FROM python:3.9

# Ustaw katalog roboczy w kontenerze
WORKDIR /app

# Skopiuj plik requirements.txt i zainstaluj zależności
COPY requirements.txt /app/
RUN pip install --no-cache-dir -r requirements.txt

# Skopiuj projekt do katalogu /app w kontenerze
COPY . /app/

# Uruchom polecenie collectstatic
# Możesz potrzebować ustawić zmienne środowiskowe lub pliki konfiguracyjne
RUN python manage.py collectstatic --noinput

# Uruchom serwer Django przy starcie kontenera
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
