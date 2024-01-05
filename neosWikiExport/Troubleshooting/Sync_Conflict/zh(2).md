<languages/>
当本地资源与存储在云上的数据不同步时，就可能会发生同步冲突。这可能由多种原因造成。您可以检查
[日志文件](Log_Files/zh "wikilink")
以了解哪些文件存在冲突，以及是本地还是云存储的内容较新。在文本编辑器中打开日志文件即可查看它们的内容。

# 确保您正在阅读正确的指南

在我们有多个关于同步问题的解决指南，在继续阅读**之前**，请确保你正阅读的是为你的问题准备的，要查看同步问题总览，请前往
[同步错误](Sync_Errors "wikilink")。

这些问题略有不同，可能需要不同的步骤，因此我们将它们分成单独的指南。

# 要做什么

## 找出未同步的内容

这个步骤是**可选的**，但是建议回忆一下在同步冲突发生之前你在做些什么、是否在做重要的事情。因为根据您如何进行后续的操作，可能会决定您之前的工作内容是否可以恢复。因此最好回忆一下您之前在做什么以及它的重要性。以下的步骤可以帮助到您。

1.  [找到你的日志文件](Log_Files/zh "wikilink")
    然后打开**最新的**那一个.
2.  打开日志文件之后，寻找"unsynced record"、"failed sync"、"Record
    preprocessing failed"等相关关键词。你可以使用"搜索"功能(通常快捷键是
    CTRL + F)
3.  当你找到了关键词，然后你可以阅读它们来搞清楚是什么内容没有同步。比如可能会有“Home”或“Avatar”之类的字样在关键词旁边。这将告诉你是什么内容同步失败了。
4.  根据具体同步失败的内容，评估一下它对你的重要性。

如果你不确定，可以在我们的 [discord](https://discord.gg/Resonite)
中问问，记得向别人提供日志文件，这样才好帮助你。

## 添加命令行参数

现在您已经有机会考虑/查看未同步的内容，您需要在**两个**选项之间做出选择：

1.  删除未同步的内容，这将丢失任何未成功保存至云端的内容。
2.  强制将本地内容覆盖到云端，如果你确定你电脑上的内容更新一些，这将是个不错的选择。

根据您的决定，您需要将以下命令行参数中的**其中一个**添加到您的 Resonite
副本中：

1.  `-DeleteUnsyncedCloudRecords`
    将从你的电脑上删除任何本地(你的电脑)未同步的文件/物品，然后重新下载云端的副本。请确定您从电脑中删除它们不会丢失重要的文件/物品时，再使用此命令。
2.  `-ForceSyncConflictingCloudRecords`
    将强制上传冲突的本地文件/物品至云端。这将使本地的副本覆盖云端已存在的文件/物品。这可能会用更早的/不正确的文件版本覆盖你的云端数据，所以请谨慎使用。

要将这些添加到 Resonite，请遵循以下步骤，无论是 Steam 还是独立版本：

### Steam 版本

### 独立版本

## 运行 Resonite

当你遵循以上步骤添加了**其中一个**参数，运行**一次**Resonite，运行后如果
Resonite 仪表盘上方显示着**已同步**，则表示同步问题已经解决了。

## 清理

当问题解决后，**移除你所添加的命令行参数**。参数仅当你在修复冲突的过程中才用得上。将参数一直留在那里将导致数据丢失。

## 其他问题

如果你相信同步问题是其他原因导致的，请再看看我们的
[同步错误指南](Sync_Errors/zh "wikilink")。

[Category:Troubleshooting](Category:Troubleshooting "wikilink")