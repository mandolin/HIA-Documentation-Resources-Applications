# HIA-Documentation-Resources-Applications

HIA Documentation System generated JSON resource reference. This repository publishes pinned, verified snapshots produced by [HIA Documentation](https://github.com/mandolin/HIA-Documentation).

## Reference

- [文档化配置规范 (zh-CN)](https://mandolin.github.io/HIA-Documentation-Resources-Applications/profiles/zh-CN/)
- [Documentation profiles (en)](https://mandolin.github.io/HIA-Documentation-Resources-Applications/profiles/en/)
- [业务流程、语言、呈现与质量模式 (zh-CN)](https://mandolin.github.io/HIA-Documentation-Resources-Applications/schemas/business-localization-presentation-and-quality/zh-CN/)
- [Business flow, localization, presentation and quality schemas (en)](https://mandolin.github.io/HIA-Documentation-Resources-Applications/schemas/business-localization-presentation-and-quality/en/)

Each partition provides its own bilingual interface, project index, static pages, original JSON snapshots, source maps and source previews. Resource text retains its original language. The code reference navigation opens the [core API site](https://mandolin.github.io/HIA-Documentation-API/zh-CN/).

The application-schema partition includes `@hia-doc/schemas/command-documentation.schema.json`, documenting the shared command-description structure.

中文。应用模式分区包含统一命令描述模式，原始JSON、逐值文档、源码映射和授权源码完整保留。

## Publication and maintenance

`snapshot.json` pins the source commit, partition registry, release archive and exhaustive build report by SHA-256. Release assets contain generated content. Git history contains publication metadata and maintenance files. The Pages workflow reads the pinned source commit and runs the shared archive-validator tests before verifying and publishing every file.

Generate a fresh snapshot with `pnpm reference:resources:build` in the source repository. Review the measured file count, uncompressed bytes, largest index and expected growth before updating this publication. Related content families can use separate publication repositories when their combined size would exceed a site budget.

Run `python3 -m unittest discover -s scripts -p test_resource_reference_publication.py` in the source repository to check validator regressions. Validate the release locally using `python3 scripts/prepare_resource_reference.py <snapshot.json> <archive.tar.gz> <build-report.json> <new-output-directory>`. Dispatch Resource Reference Pages after the pinned public release assets are available.

The displayed system version is a preview identity until the corresponding product release is published.

## License

MIT.
