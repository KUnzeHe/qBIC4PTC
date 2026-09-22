# 仿真文件

本目录保存初步静态模型 `static_qBIC.fsp`、一次运行日志 `static_qBIC_p0.log` 和参数导出脚本 `export_fdtd_model_to_txt.lsf`。当前模型尚未完成数值收敛验证。

在 FDTD Solutions 中打开要检查的 `.fsp`，运行导出脚本。脚本不运行求解器，也不修改模型；默认在 Lumerical 当前工作目录生成 `fdtd_model_complete_export.txt`，再次运行会覆盖该文本文件。若找不到输出，可将脚本中的 `export_file` 改为明确的 Windows 绝对路径。

导出内容包括根目录对象的可读属性、全局光源与监视器设置，以及对象所用材料的数据库属性。`[READ FAILED]` 等标记表示该项没有成功读取；同名对象和结构组内的子对象需要另外核对。脚本按 Lumerical 文档改写，仍需在项目使用的 2020 R2.4 版本中实测。
