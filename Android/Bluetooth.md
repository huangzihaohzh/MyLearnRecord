# 安卓蓝牙开发

应用框架中的Android Bluetooth API为访问蓝牙功能提供了途径

使用 Bluetooth API，Android 应用可执行以下操作：

* 扫描其他蓝牙设备
* 查询本地蓝牙适配器的配对蓝牙设备
* 建立 RFCOMM 通道
* 通过服务发现连接到其他设备
* 与其他设备进行双向数据传输
* 管理多个连接

## 基础知识

使用蓝牙通信的四项主要任务：

* 设置蓝牙
* 查找局部区域内的配对设备或可用设备
* 连接设备
* 在设备之间传输数据

android怕.bluetooth 包提供了所有的Bluetooth API，一下为创建蓝牙连接所需的类和接口：

* BluetoothAdaptor：表示本地蓝牙适配器（蓝牙无线装置）。 BluetoothAdapter 是所有蓝牙交互的入口点。 利用它可以发现其他蓝牙设备，查询绑定（配对）设备的列表，使用已知的 MAC 地址实例化 BluetoothDevice，以及创建 BluetoothServerSocket 以侦听来自其他设备的通信。

* BluetoothDevice：表示远程蓝牙设备。利用它可以通过 BluetoothSocket 请求与某个远程设备建立连接，或查询有关该设备的信息，例如设备的名称、地址、类和绑定状态等。

* BluetoothSocket：表示蓝牙套接字接口（与 TCP Socket 相似）。这是允许应用通过 InputStream 和 OutputStream 与其他蓝牙设备交换数据的连接点。

* BluetoothServerSocket：表示用于侦听传入请求的开放服务器套接字（类似于 TCP ServerSocket）。 要连接两台 Android 设备，其中一台设备必须使用此类开放一个服务器套接字。 当一台远程蓝牙设备向此设备发出连接请求时， BluetoothServerSocket 将会在接受连接后返回已连接的 BluetoothSocket。

* BluetoothClass：描述蓝牙设备的一般特征和功能。 这是一组只读属性，用于定义设备的主要和次要设备类及其服务。 不过，它不能可靠地描述设备支持的所有蓝牙配置文件和服务，而是适合作为设备类型提示。

* BluetoothProfile：表示蓝牙配置文件的接口。 蓝牙配置文件是适用于设备间蓝牙通信的无线接口规范。 免提配置文件便是一个示例。 如需了解有关配置文件的详细讨论，请参阅使用配置文件


