### 测试模式  
如果勾选，文件将不会被删除和复制。 使用此模式可查看与同步任务同步时将复制或删除哪些文件。你可以在历史记录和消息中看到将被复制或删除的文件。 在测试模式下不能设置为自动同步任务。  

### 自动同步任务  
如果勾选，当您按下屏幕顶部的同步按钮时，同步将开始（您可以在组选项卡中更改任务以开始同步）。  

### 任务名称  
这是同步任务的名称。 这个名字不区分大小写。  

### 同步方法  
从镜像、复制、移动和存档中选择一种方法。 <span style="color: red;"><u>同步是在一个方向上进行的，从源文件夹到目标文件夹。</u></span>   

- 镜子  
将源端目录和文件差分复制(**<u>*1</u>**)到目的端，复制完成后删除目的端不存在于源端的文件和目录。  
- 移动  
移动将源目录和文件复制到目的地，并删除复制到目的地的源文件。 但是，如果源文件和目标文件的名称、文件大小、修改日期相同，则源文件不被复制，目标文件被删除。  
- 复制  
将源端目录中包含的文件进行差分复制到目的端。  
- 档案  
在拍摄日期早于存档执行日期7天或30天的条件下，将源目录中的照片和视频移动到目的地。 但是，目的地不能使用ZIP。  

**<u>*1</u>**当满足以下三个条件之一时，判断为差异文件，并进行复制和移动。 但是，文件大小和最后修改时间可以被同步任务的选项所忽略。   

1. 文件不存在  
2. 文件大小不同  
3. 最后修改的时间相差3秒以上（秒数可以通过同步任务的选项来更改)  

### 交换源头和目的地  
交换源文件夹和目标文件夹的内容。  

### 源文件夹  

点击显示源文件夹编辑界面。  

### 目的地文件夹  

点击显示目的地文件夹编辑界面。  

### 过滤器  
你可以通过文件名、文件大小、文件修改日期和目录名称选择要同步的文件。  

- 文件名过滤器  
您可以注册要同步的文件名称和扩展名。  
- 文件大小过滤器  
你可以按文件大小选择要同步的文件。  
- 文件更新日期过滤器  
你可以通过文件的最后修改日期选择要同步的文件。  
- 目录过滤器  
您可以选择要同步的目录。  

### 要对以下内容进行存档(仅在同步方法为存档时显示)  

选择您要存档的照片或视频的标准。  

- 立即所有  
- 7天以上  
- 30天以上  
- 60天以上  
- 90天以上  
- 超过180天  
- 1年以上  

### 只在充电时开始同步  
只有在充电时才能开始同步。 只有在设备充电时才能启动同步，如果您试图在设备未充电时启动同步，则会出现错误，后续同步任务将被中止。  

### 直接处理源文件夹中指定目录下的文件。  

如果不勾选，只有直接存在于源目录下的子目录会被同步。  

### 在覆盖复制或删除之前进行检查。   

如果勾选，则在删除和覆盖文件之前会显示确认对话框。  

### 错误选项  

您可以指定错误发生时的行为。  

- 停止同步  
- 忽略所有错误并开始后续任务  
如果您总是想执行后续任务，请使用此选项。  
- 如果网络选项错误，则启动后续任务  
如果您想在不是私有地址或不是指定 IP 地址时运行后续任务，则使用此选项。  

### 网络  
你可以设置是否可以通过网络状态启动同步。  

- 只有在充电时才开始同步  
您只能在充电时开始同步。 在未充电时启动动机将导致错误并中止后续同步任务的启动。  
- 当您连接到AP时  
如果你连接到一个接入点，你可以开始同步。  
- 仅限私人IP地址  
当IP地址是私人地址时，可以开始同步。  
- 在IP地址列表中注册  
在IP地址列表中注册了IP地址，就可以开始同步。   
您可以使用通配符作为过滤器。(例如：192.168.100.\*，192.168.\*。 \*)  

### 允许在所有IP地址上进行同步  

允许在所有IP地址上进行同步。 但不能进行SMB服务器扫描。  

### 显示高级选项   

勾选此框以显示高级选项。  

### 处理子目录  
它将递归地包含指定源文件夹下的子目录。  

### 处理空目录  
如果选中，空目录将被同步。 在目的地建立一个空目录）。  

### 处理隐藏的目录   
勾选后，同步将包括隐藏的linux文件夹（名称以点开头的文件夹）。请注意，在Windows和Samba中，隐藏属性不是由文件夹名称设置的。因此，SMB/Windows目标上的同步文件夹不会有主机隐藏属性。  

### 处理隐藏文件  
勾选后，同步将包括隐藏的linux文件（名字以点开头的文件）。请注意，在Windows和Samba中，隐藏属性不是由文件名设置的。因此，SMB/Windows目标上的同步文件不会有主机的隐藏属性。  

### 覆盖文件  
如果不选中，即使按大小和时间比较的标准不同，目的地上的文件也不会被覆盖。  

### 如果在同步过程中发生网络错误，请重试   
只有在远端出现错误时，才会重新进行同步。 最多重试3次，每次重试都是在出错30秒后进行。  

### 向SMB文件夹写入时，IO缓冲区限制为16KB   
当写入PC/NAS文件夹时发生 "访问被拒绝 "的错误时，请尝试这样做。 如果勾选，当写入远程文件时，IO缓冲区被限制为16KB。 但是，性能会有所下降。  

### 镜像时先删除  

勾选后，将首先删除目标文件夹上存在的但源文件夹上不存在的目录和文件。之后，不同的文件和文件夹将被复制到目的地。  
如果源文件夹是SMB，则处理时间将更长，因为目录结构及其内容是通过网络扫描的。 强烈建议启用选项“使用SMB2协商”，因为SMB1会非常慢。  

### 删除被过滤器排除的目录/文件   

如果选中，被过滤器排除的目录/文件将从目标目录中删除。  

### 不要将目标文件的最后修改时间设置为与源文件相同   

如果出现SmbFile.setLastModified()/File.setLastModified()失败等错误，请启用。这意味着远程主机不允许设置文件的最后修改时间。如果不勾选，复制文件在目标机上的最后修改时间将被设置为复制/同步的时间。这意味着目标文件会比源文件更新。  

### 利用文件大小来判断差异   

勾选后，如果文件大小不同，则判断为差异文件。  
### 只有当源文件大小较大时，它才会判断为差异文件   
勾选后，只有当源文件大小较大时，才会使其成为同步的对象。  

### 使用文件的最后更新时间进行差异判断   
它检查时，当文件的最后更新时间不同时，就会判断为差异文件。  

### 使用最后修改的时间来判断差异   
选择1、3或10秒中的一个。 如果文件最后修改的时间差在选定的时间差内，则假设为不变。  

### 当目标文件比源文件新时，不要覆盖它   
如果勾选，即使文件大小和最后更新时间不同，只有当源文件比目标文件新时，文件才会被覆盖。请记住，如果你改变了时区，或者在夏令时改变的时间间隔期间修改文件，最后修改的文件可能会比未更新的文件显得更旧。这与文件系统的差异有关，只有在覆盖文件前手动检查才能避免数据丢失。如果要自动同步，一般建议不要在夏令时变化的间隔期修改文件。  

### 忽略夏令时和标准时之间的时差   
如果选中，则忽略指定时间的差异。  

### 跳过处理目录或文件名中含有不能使用的字符的目录或文件 (", :, \, *, <, >, |)  
如果勾选，则不会处理包含不可用字符的目录/文件，而是显示一条警告信息，并处理下一个目录/文件。  

### 当源目录为空时，删除源目录（仅当同步选项为移动时）  
(同步方式仅为移动)移动文件后源目录为空时，删除源目录。  

### 当无法从Exif中获得拍摄日期和时间时，显示一条确认信息   
勾选后，屏幕上会显示确认信息。 同步将被暂停，直到你回复确认信息。  

### 同步到SDCARD/USB存储时，忽略大于4GB的源文件  
如果勾选，当同步到本地存储时，忽略大于4GB的源文件，以防止同步到用exFat以外的格式化的MicroSD卡时出现I/O错误。  

### 忽略那些文件名长度超过指定长度的文件  
如果文件名的长度超过了屏幕右侧输入的数值，该文件将被忽略。  

### 使用说明书  
[FAQs](https://sentaroh.github.io/Documents/SMBSync3/SMBSync3_FAQ_EN.htm)  
[Description](https://sentaroh.github.io/Documents/SMBSync3/SMBSync3_Desc_EN.htm)  