# 本項目

基於 vue3 和 element-plus 的後台解決方案，包含 mock 方案、組件二次封裝、cli，使用 pnpm 和 monorepo 進行管理。



## 為什麼要使用 monorepo

Monorepo 架構常見於 Vue、React、Webpack 等大型開源庫，也適用於商業項目，儘管增加了一些複雜性，但能提升程式碼組織性與重用性。例如，在 Saas 服務的後台開發中，可能需要面向內部業務人員、經銷商、開發者等不同角色，而這些後台通常會共用組件與函式庫。

傳統做法是將共用庫發布到 npm 私有倉庫，但在頻繁開發階段，這種方式較為繁瑣。Monorepo 則透過 workspace 機制，讓專案內部共享程式碼，並可使用 Lerna 等工具快速管理與發佈，提高開發效率。


## 啟動

本項目使用 pnpm 進行管理，請先確保已經在全局中安裝 pnpm：

```shell
npm i -g pnpm
```

依賴安裝：

```shell
pnpm i
```

啟動範例項目：

```shell
pnpm run -C example serve
```

啟動項目文檔：

```shell
pnpm run -C docs dev
```



## 目錄

- /docs：項目文檔，使用 vuepress 進行開發。
- /example：基於 Vue3 和 TypeScript 的開發範例。
- /packages/vonor-cli：對業務開發有幫助的 command line 腳本。
- /packages/vonor-eslint-config：項目中的 eslint 方案。
- /packages/vonor-mock：前端的 mock 方案函式庫。
- /packages/vonor-ui：基於 element-plus 二次封裝的組件庫，以配置的型式進行參數傳遞。

