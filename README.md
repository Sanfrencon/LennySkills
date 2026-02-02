# LennySkills 🚀

> **LennySkills：重新定义 AI 的技能边界，开启智能体进化的“核动力”引擎。**

---

## 🌟 为什么选择 LennySkills？

在这里向 [Refound Lenny Skills](https://refoundai.com/lenny-skills/) 致以最崇高的敬意——正是这些沉淀了无数实战经验、闪耀着顶级方法论光芒的技能包，为本项目注入了不朽的灵魂。

通过将这些顶级的专家技能与最前沿的 MCP 架构深度融合，LennySkills 赋予了 AI：

*   **真正的专家级视野**：站在 [Refound](https://refoundai.com/lenny-skills/) 的巨人肩膀上，AI 不再局限于模糊的预训练知识，而是瞬间习得 PRD 撰写、增长实验、组织架构设计等工业级方法论。
*   **极致的生产力释放**：自动化扫描、零配置聚合，让你从繁琐的 Prompt 拼接中彻底解放，专注于创造本身。
*   **跨时代的智能架构**：基于高性能 SSE 传输与容器化部署，无论是本地桌面还是云端智能集群，LennySkills 都能提供稳如泰山的技能输出。

**LennySkills，让每一个 AI 都能拥有顶级专家的思维模型。**

---

## 项目总结

**核心特性：**
*   **自动化聚合**：自动读取 `skills/` 下的 Markdown 文档并合并上下文。
*   **SSE 传输模式**：采用 HTTP SSE 协议，支持远程连接和 Web 部署。
*   **高性能后端**：基于 `FastMCP` 框架，支持快速扩展。
*   **容器化支持**：内置 Docker 配置，实现一键环境隔离部署。

---

## 安装与运行指南

### 1. 本地开发环境安装
适用于 Windows/macOS/Linux 本地直接运行。

**前提条件：**
*   安装 Python 3.10+
*   安装 [uv](https://github.com/astral-sh/uv) (推荐) 或 `pip`

**安装步骤：**
1.  **进入项目目录：**
    ```bash
    cd LennySkills
    ```
2.  **安装依赖：**
    ```bash
    pip install fastmcp pathlib
    # 或者使用 uv
    uv sync
    ```
3.  **启动服务：**
    ```bash
    python MCPserver.py
    ```
    *服务默认运行在：`http://0.0.0.0:10080/sse`*

---

### 2. Docker 容器化安装
适用于服务器部署或需要环境隔离的场景。

**前提条件：**
*   安装 Docker 和 Docker Compose

**安装步骤：**
1.  **启动容器：**
    在项目根目录下执行：
    ```bash
    docker-compose up -d
    ```
2.  **查看状态：**
    ```bash
    docker ps  # 确认名为 LennySkills 的容器正在运行
    docker logs -f LennySkills  # 查看启动日志
    ```

**配置说明：**
*   **端口映射**：默认使用 `10080` 端口。
*   **挂载卷**：本地目录挂载至容器 `/app`，修改技能文件可实时生效。

---

## 验证服务
服务启动后，可以通过访问 `http://localhost:10080/sse` 检查响应，或在 MCP 客户端中配置该地址。
