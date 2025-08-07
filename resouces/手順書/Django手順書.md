# プログラムを書くにあたって、どういう順番でやったのかを示します。
## 仮想環境を作成する

``` bash
python -m venv ll_env
```

## 仮想環境を有効化する

``` bash
source ll_env/bin/activate
```

Windowsの場合

``` bash
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser 
ll_env\Scripts\activate
```

## Djangoをインストールする

```bash
pip install --upgrade pip
pip install django
```

## Djangoプロジェクトを作成する

```bash
django-admin startproject ll_project .
```

## データベースを作成する


```bash
python manage.py migrate
```

## 管理サイトの日本語化
settings.pyを、以下に変更する
```python
# Internationalization
# https://docs.djangoproject.com/en/5.2/topics/i18n/

LANGUAGE_CODE = 'ja'

TIME_ZONE = 'Asia/Tokyo'

USE_I18N = True

USE_TZ = True


# Static files (CSS, JavaScript, Images)
```