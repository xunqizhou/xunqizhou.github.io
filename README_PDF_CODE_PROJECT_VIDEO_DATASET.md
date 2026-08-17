# PRISM Publications Button Patch

把本压缩包中的 4 个文件覆盖到 PRISM 项目对应位置：

- `src/components/publications/PublicationsList.tsx`
- `src/lib/bibtexParser.ts`
- `src/types/publication.ts`
- `src/lib/i18n/messages.ts`

## BibTeX 写法示例

每个字段都必须用英文逗号 `,` 分隔。只有填写了对应字段，页面才会显示对应按钮。

```bibtex
@article{example2026,
  title = {Example paper title},
  author = {Xunqi Zhou and Yongjie Zhai},
  journal = {Information Fusion},
  year = {2026},
  doi = {10.1016/xxxx},
  pdf = {/papers/IF2026.pdf},
  code = {https://github.com/xxx/xxx},
  project = {https://xxx.github.io/project},
  video = {https://www.youtube.com/watch?v=xxxx},
  dataset = {https://huggingface.co/datasets/xxx/xxx},
  preview = {IF2026.jpg},
  ccf = {CCF-B},
  cas = {中科院-Q1},
  jcr = {JCR-Q1},
  venueShort = {IF'26}
}
```

本地 PDF 放置路径示例：

```text
public/papers/IF2026.pdf
```

BibTeX 中对应写：

```bibtex
pdf = {/papers/IF2026.pdf},
```

支持字段：

- `pdf` / `pdfurl` / `pdf_url`
- `code` / `github` / `repo` / `repository`
- `project` / `projecturl` / `project_url` / `website` / `homepage`
- `video` / `videourl` / `video_url` / `youtube`
- `dataset` / `dataseturl` / `dataset_url` / `data`

英文页面中，`中科院-Q1` 等会显示为 `CAS-Q1`。
