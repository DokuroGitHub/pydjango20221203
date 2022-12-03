# using pyenv
```bash
pyenv versions
pyenv global 3.11.0
pip list
```
# venv
```bash
python -m venv venv
./venv/Scripts/activate
python -m pip install --upgrade pip
# rm -r venv
```
# django
```bash
pipenv install django
pipenv install djangorestframework
django-admin startproject django20221203 .
cd django20221203
django-admin startapp api
cd ..
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
# cd django20221203/api; code django20221203/api/serializers.py
code django20221203/api/serializers.py
```

# run
```bash
python -m venv venv
./venv/Scripts/activate
pipenv install
python manage.py runserver localhost:8000
# django-admin runserver localhost:8000
```


### keys.py
```py
# keys.py

X_RapidAPI_Key = "abc"

# open file as a binary file
f = open('keys.bin', 'wb')

#c onvert string to bytes
strBytes = X_RapidAPI_Key.encode()
# hashBytes = hashlib.sha512(X_RapidAPI_Key.encode('utf-8')).digest()  # hash

#write bytes to binary file
f.write(strBytes)

f.close()

with open("keys.bin", encoding="utf-8") as binary_file:
    # Read the whole file at once
    api_key = binary_file.read()
key = str(api_key)
print("key:", key)
```