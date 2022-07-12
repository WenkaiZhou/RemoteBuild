# RemoteBuild

## 配置 `Android Studio`

1. `Run` -> `Edit Configuration` -> `+`
2. 选择 `Android App`，有意义的名字，如：`answer_main_remote_build`
3. 删除 `Before launch` 中默认的 `Gradle-aware Make`
4. `Before launch` 中添加 `Run External Tool`，取名 `remote assembleDebug`
    - Program 输入 `bash`
    - Arguments 输入 `./remotebuild ./gradlew assembleDebug`
    - Working director 选择 `$ProjectFileDir$`

5. ENJOY IT！

## THANKS TO

1. [yaml-parser](https://github.com/Minlison/yaml-parser/blob/master/parser_yaml.sh) yaml配置解析代码来源
2. [mainframer](https://github.com/buildfoundation/mainframer) 同步脚本基于mainframer
