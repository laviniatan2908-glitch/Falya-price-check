[README_使用说明.md](https://github.com/user-attachments/files/29410256/README_.md)[Uploading README_使用说# Farfa Purse 直播查价器网站版

这是一个手机浏览器可打开的网站版查价器，不需要微信小程序认证。

## 文件说明

- `index.html`：网站页面，不需要经常改。
- `assets/logo.jpg`：品牌 Logo。
- `data/prices.json`：价格数据，后续更新价格主要改这个文件。
- `data/prices.csv`：给你查看和维护的数据表，字段和 JSON 一致。

## 推荐上线方式：GitHub Pages 免费部署

1. 注册 / 登录 GitHub。
2. 新建一个仓库，例如 `farfa-price`。
3. 上传本文件夹里的所有文件：`index.html`、`assets`、`data`。
4. 打开仓库 `Settings` → `Pages`。
5. Source 选择 `Deploy from a branch`，Branch 选择 `main` 和 `/root`。
6. 保存后等待 1-3 分钟，会生成一个网址。
7. 把网址发给朋友，手机点开就能查价。

如果你已经有域名，例如 `farfapurse.com`，可以把域名解析到 GitHub Pages，最后使用类似：

`https://price.farfapurse.com`

## 后续怎么更新价格

只改 `data/prices.json` 或先改 `data/prices.csv` 再转成 JSON。

每一条价格是一行数据：

```json
{
  "category": "大包系列",
  "product": "法宝水桶",
  "fabric": "平布",
  "price": "259"
}
```

### 修改价格

找到对应的 `category + product + fabric`，只改 `price`。

### 新增包型

复制几条同类别的数据，把 `product` 改成新包型名称，再填入不同布料价格。

例如新增「新款托特」：

```json
{
  "category": "大包系列",
  "product": "新款托特",
  "fabric": "平布",
  "price": "299"
},
{
  "category": "大包系列",
  "product": "新款托特",
  "fabric": "刺绣",
  "price": "329"
}
```

保存并上传新版 `data/prices.json` 后，网站会读取最新数据。

## 注意

- JSON 中英文标点要保持格式，最后一条数据后面不要多加逗号。
- 价格可以写数字，也可以写备注，例如 `259/加肩带299`、`没布`。
- 分类建议只用：`大包系列`、`日常收纳`。
明.md…]()
