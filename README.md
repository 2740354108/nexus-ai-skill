# nexus-ai-skill

NEXUS AI 的技能包（供「从 GitHub 导入技能」使用）。

导入地址：

```
https://github.com/2740354108/nexus-ai-skill
```

## 这是什么

把本机运行的 **NEXUS AI** 当作私有 AI 后端来用：

- 对话（OpenAI 兼容接口）
- 识图
- 文生图 / 图生视频 / 文生视频
- 音乐生成
- 服务未启动时自动拉起

## 文件结构

```
SKILL.md                    技能入口（导入识别用）
skill/references/api.md     全部接口、请求字段与返回值
skill/references/config.md  安装、配置、端口与常见错误
skill/scripts/nexus.sh      一键调用脚本（零依赖）
```

## 用法

```bash
bash skill/scripts/nexus.sh health
bash skill/scripts/nexus.sh chat  "用一句话介绍你自己"
bash skill/scripts/nexus.sh image "赛博朋克风格的猫" cat.png
bash skill/scripts/nexus.sh music "轻快的钢琴曲" song.json
```

默认连 `http://localhost:3000`，可用环境变量覆盖：

```bash
NEXUS_API_BASE=http://192.168.1.10:3000 bash skill/scripts/nexus.sh health
NEXUS_API_TOKEN=<站长令牌或登录后的 JWT> bash skill/scripts/nexus.sh chat "你好"
```
