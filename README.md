# RemoteBuild

## 配置项目

```Shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/xuehuayous/RemoteBuild/main/install)"
```

## 配置 `Android Studio`

1. `Run` -> `Edit Configuration` -> `+`
2. 选择 `Android App`，有意义的名字，如：`*_remote_build`
3. 删除 `Before launch` 中默认的 `Gradle-aware Make`
4. `Before launch` 中添加 `Run External Tool`，取名 `remote assembleDebug`
    - Program 输入 `bash`
    - Arguments 输入 `./remotebuild ./gradlew assembleDebug`
    - Working director 选择 `$ProjectFileDir$`

5. ENJOY IT！

## THANKS TO

1. yaml解析基于 [yaml-parser](https://github.com/Minlison/yaml-parser/blob/master/parser_yaml.sh)
2. 同步脚本基于 [mainframer](https://github.com/buildfoundation/mainframer)

## License

```text
Copyright 2022 Kevin zhou

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
