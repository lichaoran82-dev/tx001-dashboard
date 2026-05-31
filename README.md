# TX001 Warehouse Performance Dashboard

一个适合直接托管到 GitHub Pages 的单页静态绩效看板。

## Features

- 单文件入口：`index.html`
- 零依赖：不需要构建工具或安装包
- 支持总览、岗位排名、员工卡片、效率热图
- 响应式布局，适配桌面和移动端
- 数据目前内嵌在页面脚本中，便于先快速部署和演示

## Preview Locally

直接双击 `index.html` 即可打开。

也可以在本目录启动本地服务：

```bash
python3 -m http.server 8765
```

然后访问：

```text
http://localhost:8765
```

## Deploy To GitHub Pages

1. 新建一个 GitHub 仓库。
2. 上传本目录里的全部文件。
3. 进入仓库 `Settings` -> `Pages`。
4. Source 选择 `Deploy from a branch`。
5. Branch 选择 `main`，目录选择 `/root`。
6. 保存后等待 GitHub Pages 完成发布。

## Update Data

当前数据在 `index.html` 底部的 `<script>` 中：

- `roles`: 岗位平均效率
- `people`: 员工绩效明细
- `heatRows`: 每日效率热图
- `dates`: 热图日期列

如果后续接入 CSV、JSON 或 API，可以把这些数组替换成异步加载逻辑。
