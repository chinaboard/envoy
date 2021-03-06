# SUMMARY

### 说明

- [介绍](README.md)
- [关于本文档](about_docs.md)

### 简介
- [Envoy 是什么？](intro/what_is_envoy.md)
- [架构概览](intro/what_is_envoy.md)
  - [术语](intro/arch_overview/terminology.md)
  - [线程模型](intro/arch_overview/threading_model.md)
  - [Listener](intro/arch_overview/listeners.md)
  - [Listener filter](intro/arch_overview/listener_filters.md)
  - [Network (L3/L4) filter](intro/arch_overview/network_filters.md)
  - [HTTP 连接管理](intro/arch_overview/http_connection_management.md)
  - [HTTP filter](intro/arch_overview/http_filters.md)
  - [HTTP 路由](intro/arch_overview/http_routing.md)
  - [gRPC](intro/arch_overview/grpc.md)
  - [WebSocket 支持](intro/arch_overview/websocket.md)
  - [Cluster manager](intro/arch_overview/cluster_manager.md)
  - [服务发现](intro/arch_overview/service_discovery.md)
  - [健康检查](intro/arch_overview/health_checking.md)
  - [连接池](intro/arch_overview/connection_pooling.md)
  - [负载均衡](intro/arch_overview/load_balancing.md)
  - [异常点检测](intro/arch_overview/outlier.md)
  - [断路器](intro/arch_overview/circuit_breaking.md)
  - [全局速率限制](intro/arch_overview/global_rate_limiting.md)
  - [TLS](intro/arch_overview/ssl.md)
  - [统计](intro/arch_overview/statistics.md)
  - [运行时配置](intro/arch_overview/runtime.md)
  - [追踪](intro/arch_overview/tracing.md)
  - [TCP 代理](intro/arch_overview/tcp_proxy.md)
  - [访问记录](intro/arch_overview/access_logging.md)
  - [MongoDB](intro/arch_overview/mongo.md)
  - [DynamoDB](intro/arch_overview/dynamo.md)
  - [Redis](intro/arch_overview/redis.md)
  - [热重启](intro/arch_overview/hot_restart.md)
  - [动态配置](intro/arch_overview/dynamic_configuration.md)
  - [初始化](intro/arch_overview/init.md)
  - [排除](intro/arch_overview/draining.md)
  - [脚本](intro/arch_overview/scripting.md)
- [部署类型](intro/deployment_types/deployment_types.md)
  - [仅服务之间](intro/deployment_types/service_to_service.md)
  - [服务之间外加前端代理](intro/deployment_types/front_proxy.md)
  - [服务间、前端代理、双向代理](intro/deployment_types/double_proxy.md) 
- [与类似系统比较](intro/comparison.md)
- [获取帮助](intro/getting_help.md)
- [历史版本](intro/version_history.md)

### 入门指南

- [入门指南](start/start.md)
- Sandbox
  - [前端代理](start/sandboxes/front_proxy.md)
  - [Zipkin 追踪](start/sandboxes/zipkin_tracing.md)
  - [Jaeger 追踪](start/sandboxes/jaeger_tracing.md)
  - [Jaeger 原生追踪](start/sandboxes/jaeger_native_tracing.md)
- 其他用例
  - [Envoy 作为 Kubernetes 的 API 网关](start/distro/ambassador.md)

### 构建和安装

- [构建](install/building.md)
- [参考配置](install/ref_configs.md)
- 工具
  - [配置负载检查工具](install/tools/config_load_check_tool.md)
  - [路由表检查工具](install/tools/route_table_check_tool.md)
  - [Schema 验证器检查工具](install/tools/schema_validator_check_tool.md)

### 配置参考

- [v1 API 概览](configuration/overview/v1_overview.md)
- [v2 API 概览](configuration/overview/v2_overview.md)
- Listener
  - [统计](configuration/listeners/stats.md)
  - [运行时](configuration/listeners/runtime.md)
  - [Listener 发现服务（LDS）](configuration/listeners/lds.md)
- Listener filter
  - [原始目的地](configuration/listener_filters/original_dst_filter.md)
  - [TLS 检查器](configuration/listener_filters/tls_inspector.md)
- 网络 filter
  - [客户端 TLS 身份验证](configuration/network_filters/client_ssl_auth_filter.md)
  - [Echo](configuration/network_filters/echo_filter.md)
  - [Mongo 代理](configuration/network_filters/mongo_proxy_filter.md)
  - [速率限制](configuration/network_filters/rate_limit_filter.md)
  - [Redis 代理](configuration/network_filters/redis_proxy_filter.md)
  - [TCP 代理](configuration/network_filters/tcp_proxy_filter.md)
- HTTP 连接管理器
  - [路由匹配](configuration/http_conn_man/route_matching.md)
  - [流量转换/切分](configuration/http_conn_man/traffic_splitting.md)
  - [HTTP header 操作](configuration/http_conn_man/headers.md)
  - [HTTP header sanitizing](configuration/http_conn_man/header_sanitizing.md)
  - [统计](configuration/http_conn_man/stats.md)
  - [运行时](configuration/http_conn_man/runtime.md)
  - [路由发现服务（RDS）](configuration/http_conn_man/rds.md)
- HTTP filter
  - [Buffer](configuration/http_filters/buffer_filter.md)
  - [CORS](configuration/http_filters/cors_filter.md)
  - [DynamoDB](configuration/http_filters/dynamodb_filter.md)
  - [故障注入](configuration/http_filters/fault_filter.md)
  - [gRPC HTTP/1.1 bridge](configuration/http_filters/grpc_http1_bridge_filter.md)
  - [gRPC-JSON 转码](configuration/http_filters/grpc_json_transcoder_filter.md)
  - [gRPC-Web](configuration/http_filters/grpc_web_filter.md)
  - [Gzip](configuration/http_filters/gzip_filter.md)
  - [健康检查](configuration/http_filters/health_check_filter.md)
  - [IP Tagging](configuration/http_filters/ip_tagging_filter.md)
  - [Lua](configuration/http_filters/lua_filter.md)
  - [速率限制](configuration/http_filters/rate_limit_filter.md)
  - [路由](configuration/http_filters/router_filter.md)
  - [Squash](configuration/http_filters/squash_filter.md)
- Cluster Manager
  - [统计](configuration/cluster_manager/cluster_stats.md)
  - [运行时](configuration/cluster_manager/cluster_runtime.md)
  - [集群发现服务（CDS）](configuration/cluster_manager/cds.md)
  - [健康检查](configuration/cluster_manager/cluster_hc.md)
  - [断路](configuration/cluster_manager/cluster_circuit_breakers.md)
- 健康检查器
  - [Redis](configuration/health_checkers/redis.md)
- [访问记录](configuration/access_log.md)
- [速率限制服务](configuration/rate_limit.md)
- [运行时](configuration/runtime.md)
- [统计](configuration/statistics.md)
- [路由表检查工具](configuration/tools/router_check.md)

### 运维管理

- [命令行选项](operations/cli.md)
- [热重启 Python 包装器](operations/hot_restarter.md)
- [管理接口](operations/admin.md)
- [统计概览](operations/stats_overview.md)
- [运行时](operations/runtime.md)
- [文件系统标志](operations/fs_flags.md)
- [流量捕获](operations/traffic_capture.md)
- [为自定义用例扩展 Envoy](extending/extending.md)

### API 参考

- [v1 API 参考](https://www.envoyproxy.io/docs/envoy/latest/api-v1/api)
- [v2 API 参考](https://www.envoyproxy.io/docs/envoy/latest/api-v2/api)

### 常见问题

- [Envoy 有多快？](faq/how_fast_is_envoy.md)

- [从哪里能获得二进制文件？](faq/binaries.md)
- [如何设置 SNI？](faq/sni.md)
- [如何设置 zone 可感知路由？](faq/zone_aware_routing.md)
- [如何设置 Zipkin 追踪？](faq/zipkin_tracing.md)
- [我设置了健康检查，但是当有节点失败时，Envoy 又路由到那些节点，这是怎么回事？](faq/lb_panic_threshold.md)
- [为什么 Round Robin 负载均衡看起来不起作用？](faq/concurrency_lb.md)
