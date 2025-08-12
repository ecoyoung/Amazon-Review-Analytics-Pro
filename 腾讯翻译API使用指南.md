# 腾讯翻译API使用指南

## 问题解决

如果您遇到 `local variable 'TencentCloudSDKException' referenced before assignment` 错误，这是因为腾讯云SDK没有正确安装或导入。请按照以下步骤解决：

## 1. 安装腾讯云SDK

### 方法一：使用pip安装
```bash
pip install tencentcloud-sdk-python>=3.0.0
```

### 方法二：使用安装脚本
```bash
python install_dependencies.py
```

### 方法三：使用requirements.txt
```bash
pip install -r requirements.txt
```

## 2. 获取腾讯云API密钥

1. 登录 [腾讯云控制台](https://console.cloud.tencent.com/)
2. 进入"访问管理" → "访问密钥" → "API密钥管理"
3. 创建新的API密钥
4. 复制SecretId和SecretKey
5. 确保已开通机器翻译服务

## 3. 使用步骤

1. 在翻译工具中选择"腾讯翻译API"
2. 输入您的SecretId和SecretKey
3. 选择要翻译的列
4. 点击"开始翻译"

## 4. 常见问题

### Q: 提示"腾讯云SDK未安装"
**A:** 请按照上述步骤安装腾讯云SDK

### Q: 提示"API密钥无效"
**A:** 请检查：
- SecretId和SecretKey是否正确
- 是否已开通机器翻译服务
- API密钥是否有足够的权限

### Q: 翻译速度慢
**A:** 这是正常现象，腾讯翻译API有调用频率限制，建议：
- 减小批次大小
- 增加延迟时间
- 使用缓存功能

## 5. 技术说明

- 支持英文到中文翻译
- 自动缓存翻译结果
- 支持批量翻译
- 智能错误重试机制

## 6. 费用说明

腾讯翻译API按调用次数收费，具体费用请参考腾讯云官方定价。

## 7. 联系支持

如果遇到其他问题，请检查：
1. 网络连接是否正常
2. API密钥是否有效
3. 是否已开通相关服务 