name: Bug 报告
description: 发现了程序错误？请填写以下信息帮助我们复现和修复。
title: "[Bug] "
labels: ["bug"]
assignees: []

body:
  - type: markdown
    attributes:
      value: |
        感谢您提交 Bug 报告！请尽可能详细地填写以下信息，这将帮助我们更快地定位和修复问题。

  - type: dropdown
    id: version
    attributes:
      label: cqlib 版本
      description: 您使用的 cqlib 版本是？（运行 `pip show cqlib` 查看）
      options:
        - 0.1.0（最新）
        - 0.0.x（旧版本）
        - 从源码安装
    validations:
      required: true

  - type: dropdown
    id: os
    attributes:
      label: 操作系统
      options:
        - Windows
        - macOS
        - Linux (Ubuntu/Debian)
        - Linux (其他)
    validations:
      required: true

  - type: input
    id: python-version
    attributes:
      label: Python 版本
      description: 运行 `python --version` 查看
      placeholder: "例如：Python 3.11.2"
    validations:
      required: true

  - type: textarea
    id: description
    attributes:
      label: 问题描述
      description: 清晰简洁地描述您遇到的问题
      placeholder: 运行 circuit.run() 时报 AttributeError...
    validations:
      required: true

  - type: textarea
    id: steps
    attributes:
      label: 复现步骤
      description: 描述复现问题的具体步骤
      placeholder: |
        1. 安装 cqlib（`pip install cqlib`）
        2. 运行以下代码...
        3. 出现报错...
    validations:
      required: true

  - type: textarea
    id: expected
    attributes:
      label: 期望结果
      description: 您期望程序应该做什么？
    validations:
      required: true

  - type: textarea
    id: actual
    attributes:
      label: 实际结果（含完整报错信息）
      description: 请粘贴完整的报错信息或异常栈
      render: shell
    validations:
      required: true

  - type: textarea
    id: additional
    attributes:
      label: 补充信息
      description: 任何其他相关信息（截图、日志等）
