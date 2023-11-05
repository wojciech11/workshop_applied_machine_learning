# Model API z FastAPI

## Przygotowanie projektu


```bash
python3 -m venv .venv

pip install -r requirements.txt
pip install -r test_requirements.txt
```

Zauważ: aby upewnić się, że używamy tych samych bibliotek, w produkcji, lepiej użyć [conda](../README.md).

Zauważ: możliwe, że będziesz musiał zmienić "przypięte" wersje w pliku [requirements.txt](requirements.txt).

## Przekopiowanie modelu i skalera:

```bash
ls ../models/

# model
cp -R ../models/*.pki ./models

# skaler
cp -R ../models/*.gz ./models

ls models/
```

## Uruchomienie aplikacji

```bash
uvicorn stocks_predict:app --reload
```

## Test lokalnie

Zainstaluj curl lub httpie, abyś mógł testować nasze API.

```bash
curl -s --fail -X POST -H "Content-Type: application/json" \
    -d '{
        "m12": 1.176725,
        "m11": 1.169317,
        "m10": 1.166861,
        "m09": 1.170056,
        "m08": 1.172622,
        "m07": 1.178550,
        "m06": 1.179523,
        "m05": 1.178398,
        "m04": 1.177413,
        "m03": 1.174826,
        "m02": 1.180777,
        "m01": 1.156658}' \
    http://127.0.0.1:8000/predict
```

```
{"result":1.23}
```

## Budowanie pakietu

W przypadku mniejszych modeli, często kod + model wrzucamy do produkcji razem jako Docker image:

```bash
make docker_build
```

Sprawdźmy czy wszystko działa:

```bash
make docker_run
```


Wykorzystaj curl albo http, aby upewnić się, że nasze API odpowiada prawidłowo.

## Uruchomienie aplikacji w chmurze z Google Run

...
