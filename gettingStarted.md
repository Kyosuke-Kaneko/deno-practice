# 2.Gettind started
## 2.3 First steps

You will see this program returns an error regarding network access so what did we do wrong? You might remember from the introduction that Deno is a runtime that is secure by default. This means you need to explicitly give programs permission to do certain 'privileged' actions, such as access the network.

Try it out again with the correct permission flag:
```
deno run --allow-net=deno.land first_steps.ts
```
Or, try this script hosted at https://deno.land/std@0.184.0/examples/curl.ts:

```
deno run --allow-net=deno.land https://deno.land/std@0.184.0/examples/curl.ts https://deno.land
```

パーミッションシステムにより、権限を与えないとファイルの読み込み等ができない。
例えば、ファイルの読み込みを行いたいときは--allow-read、ネットワークアクセスを行いたいときは--allow-netオプションを指定する必要がある。
以下のような処理はデフォルトでは一切実行することができない。
- ファイルの読み書き
- ネットワークアクセス
- 環境変数の参照
- サブプロセスの実行
