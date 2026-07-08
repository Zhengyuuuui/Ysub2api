完整关闭流程 ：
# 关闭 Redis
brew services stop redis

# 前端和后端终端分别按 Ctrl+C
# 或者用命令一次性关闭
pkill -f "vite"   # 关闭前端
pkill -f "server" # 关闭后端
下次启动：
# 启动 Redis
brew services start redis

# 启动后端
cd backend && go run ./cmd/server

# 启动前端
cd frontend && pnpm run dev