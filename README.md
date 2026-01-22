# Chisel-HardwareThread


本仓库的核心是utils中的HardwareThread.scala库


feat.:
- entry， step， Call能让状态机用微码汇编的风格来实现
- startWhen abortWhen isAtive来控制，显示线程是否在running
- 加入了ownSignals存储外部作用域信号，使用driveManaged注册，使用write驱动，加入了静态检查（尚不完善）


examples：
- Fetch为目前ysyx npc中的fetch级，含有两个thread：`fetch thread` 和 `shoot thread`
- spi为ysyxSoC中的SPI模块，主要使用hardwarethread实现了xip的逻辑
