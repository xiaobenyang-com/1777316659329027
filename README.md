# 网页抓取服务器 

一个功能强大的MCP服务器，提供不受robots.txt限制的网页抓取功能，支持多种HTTP方法和自定义请求设置。
A powerful MCP server that offers web scraping capabilities unrestricted by robots.txt, supports multiple HTTP methods and custom request Settings.## 工具列表 Tool List

本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。 本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。

| 工具 Tool   | 描述 Description         |
|-------|--------------------|
| fetch | Fetch content from a URL without following robots.txt restrictions. Returns the response body as text. |


## 检查服务 ## Inspector

工具在线测试： [https://mcp.xiaobenyang.com/inspector/1777316659329027](https://mcp.xiaobenyang.com/inspector/1777316659329027)

Online Tool test [https://mcp.xiaobenyang.com/inspector/1777316659329027](https://mcp.xiaobenyang.com/inspector/1777316659329027)

## 服务配置 MCP Server Config


> #### 如何获取 XBY-APIKEY ？ How to get XBY-APIKEY ?
> 访问小笨羊科技网站 [https://xiaobenyang.com](https://xiaobenyang.com)，注册用户即可获得APIKEY
> Visit XiaoBenYang website [https://xiaobenyang.com](https://xiaobenyang.com), register and get the APIKEY.

### SSE
```json
{
  "mcpServers": {
    "网页抓取服务器": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "sse",
      "url": "https://mcp.xiaobenyang.com/1777316659329027/sse"
    }
  }
}
```
### STREAMABLE HTTP
```json
{
  "mcpServers": {
    "网页抓取服务器": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "streamable_http",
      "url": "https://mcp.xiaobenyang.com/1777316659329027/mcp"
    }
  }
}
```
### STDIO
```json
{
    "mcpServers": {
        "网页抓取服务器": {
          "command": "npx",
          "args": [
            "-y",
            "xiaobenyang-mcp"
          ],
          "env": {
            "XBY_APIKEY": "<YOUR_XBY_APIKEY>",
            "mcpId": "1777316659329027",
          },
          "transport": "stdio"
        }
      }
}

```
