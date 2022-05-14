# Flask_test

## Flask
   
### サンプル

<a title="Gitpod" href="https://gitpod.io/#https://github.com/cti1650/Flask_test" target="_blank" class="btn btn-primary">Gitpodでサンプルを実行</a>

#### 本番リンク

[https://flask-test-cti-tl.herokuapp.com/](https://flask-test-cti-tl.herokuapp.com/)

```python
import os
from flask import Flask

app = Flask(__name__, static_folder='.', static_url_path='')

@app.route("/")
def index():
    return {"text": "Hello World!!"}

if __name__ == "__main__":
    port = int(os.environ.get("PORT", 5000))
    app.run(port=port, debug=True)
```

### サーバー立ち上げ

```
gunicorn main:app --log-file=-
```

### requirements.txt 作成

```plane:requirements.txt
Flask
gunicorn
```

### アプリ作成

```
django-admin startproject myapp .
django-admin startapp api
```

### マイグレーション
```
python manage.py makemigrations
```

### マイグレート
```
python manage.py migrate
```

## 参考にしたサイト

- [M1 Mac でできるだけ楽に Python 環境を構築する - Qiita](https://qiita.com/C2_now/items/c85be2ffeacd61cc7207)
- [tiangolo/fastapi: FastAPI framework, high performance, easy to learn, fast to code, ready for production](https://github.com/tiangolo/fastapi)
- [Deta にデプロイ - FastAPI](https://fastapi.tiangolo.com/ja/deployment/deta/)
- [Python Tutorial | Deta Docs](https://docs.deta.sh/docs/base/py_tutorial/?ref=fastapi)
- [DETA](https://web.deta.sh/home/cti1650/default/micros)
- [Python3.9 を Homebrew で M1 Mac にインストールする（2021 年 3 月 16 日時点） - ちゃぱブログ / エンジニアリング / マネジメント](https://as-chapa.hatenablog.com/entry/m1-python-install-20210316)
- [Python をローカルで利用できるようにする](https://zenn.dev/souq/articles/7d752c7a80c488cabd19)
- [brew でインストールに失敗する時の対処メモ](https://zenn.dev/souq/articles/3c0591a50f39269793c9)
- [Chrome ウェブストア - gitpod](https://chrome.google.com/webstore/search/gitpod?hl=ja)

- [Dockerではなくてheroku.ymlを使ってPython2とOpenCVの環境をHeroku上に整える - 猫でもわかるWebプログラミングと副業](https://www.utakata.work/entry/20180109/1515469885)  
- [Heroku に Flask で作った Web アプリをデプロイする | Simple is Best](https://oldbigbuddha.dev/posts/deploy-flask-app-to-heroku)  
- [【Python】Flaskとは？FlaskでWeb開発の基礎を学ぼう！ | AI Academy Media](https://aiacademy.jp/media/?p=57)  


## 参考にした動画

- [[Youtube編] React Hooks + Django RestFramework API でフルスタックWeb | Udemy](https://www.udemy.com/course/youtube-react-hooks-django-restframework-api-web/learn/lecture/20317547#overview)  

