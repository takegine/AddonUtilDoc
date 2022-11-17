## Table of contents

### Interfaces

- [IncomeProps](./interfaces/IncomeProps)
- [OutPutProps](./interfaces/OutPutProps)
- [layoutFileType](./interfaces/layoutFileType)

### Type Aliases

- [ManifestEntryType](./Exports#manifestentrytype)
- [dotaEXE](./Exports#dotaexe)
- [ydweEXE](./Exports#ydweexe)

### Functions

- [CreateXml](./Exports#createxml)
- [RPGConfig](./Exports#rpgconfig)
- [compileX](./Exports#compilex)
- [content\_compiler](./Exports#content_compiler)
- [convert](./Exports#convert)
- [dotaLaunch](./Exports#dotalaunch)
- [dotaTool](./Exports#dotatool)
- [fromBytesInt32](./Exports#frombytesint32)
- [getAddonName](./Exports#getaddonname)
- [getAddonPath](./Exports#getaddonpath)
- [getDotaPath](./Exports#getdotapath)
- [getMainMap](./Exports#getmainmap)
- [images\_compiler](./Exports#images_compiler)
- [keyInColumn](./Exports#keyincolumn)
- [keyInRow](./Exports#keyinrow)
- [mkjoin](./Exports#mkjoin)
- [pack](./Exports#pack)
- [read\_all\_files](./Exports#read_all_files)
- [symlink](./Exports#symlink)
- [toBytesInt32](./Exports#tobytesint32)
- [w2l](./Exports#w2l)
- [war3](./Exports#war3)
- [watch](./Exports#watch)
- [write](./Exports#write)
- [ydwe](./Exports#ydwe)
- [ydweTool](./Exports#ydwetool)

## Type Aliases

### ManifestEntryType

Ƭ **ManifestEntryType**: ``"GameSetup"`` \| ``"HeroSelection"`` \| ``"Hud"`` \| ``"HudTopBar"`` \| ``"FlyoutScoreboard"`` \| ``"GameInfo"`` \| ``"EndScreen"``

#### Defined in

rollup.ts:19

___

### dotaEXE

Ƭ **dotaEXE**: ``"resourcecompiler"`` \| ``"dota2"`` \| ``"vconsole2"``

#### Defined in

dota2.ts:32

___

### ydweEXE

Ƭ **ydweEXE**: ``"ydwe"`` \| ``"bin/ydweconfig"``

#### Defined in

war3.ts:45

## Functions

### CreateXml

▸ **CreateXml**(`data`): `void`

创建所有的xml

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | [`layoutFileType`](./interfaces/layoutFileType)[] |

#### Returns

`void`

#### Defined in

rollup.ts:128

___

### RPGConfig

▸ **RPGConfig**(): `TsRPGConfigTypeBase` & `Partial`<`TsRPGConfigType`\>

获取dota2.config.json的配置
也可以配置在'package.json'.dota2

#### Returns

`TsRPGConfigTypeBase` & `Partial`<`TsRPGConfigType`\>

继承自 ./schema/dota2.json的表格

#### Defined in

dota2.ts:128

___

### compileX

▸ **compileX**(): `Promise`<`undefined`\>

一个X大的编译脚本

#### Returns

`Promise`<`undefined`\>

#### Defined in

dota2.ts:210

___

### content\_compiler

▸ **content_compiler**(`addonName?`): `Promise`<`undefined`\>

编译 地图 模型 特效等资源

#### Parameters

| Name | Type |
| :------ | :------ |
| `addonName` | `string` |

#### Returns

`Promise`<`undefined`\>

#### Defined in

dota2.ts:47

___

### convert

▸ **convert**(`fils`): `Promise`<[`OutPutProps`](./interfaces/OutPutProps)[]\>

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `fils` | `string`[] | 输入文件 |

#### Returns

`Promise`<[`OutPutProps`](./interfaces/OutPutProps)[]\>

#### Defined in

convert.ts:17

___

### dotaLaunch

▸ **dotaLaunch**(`addon_name?`, `map_name?`): `Promise`<`void`\>

启动dota2

#### Parameters

| Name | Type |
| :------ | :------ |
| `addon_name` | `string` |
| `map_name` | `string` |

#### Returns

`Promise`<`void`\>

#### Defined in

dota2.ts:196

___

### dotaTool

▸ **dotaTool**<`T`\>(`params`, `arg?`): `Promise`<`unknown`\>

运行win64目录下的工具

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `params` | `T` extends [`dotaEXE`](./Exports#dotaexe) ? `T` : `string` |
| `arg?` | `string`[] |

#### Returns

`Promise`<`unknown`\>

#### Defined in

dota2.ts:35

___

### fromBytesInt32

▸ **fromBytesInt32**(`ascii`): `number`

将 4字节的字符串 转译为 整数

#### Parameters

| Name | Type |
| :------ | :------ |
| `ascii` | `string` |

#### Returns

`number`

#### Defined in

data.ts:4

___

### getAddonName

▸ **getAddonName**(): `string`

获取项目名字

#### Returns

`string`

#### Defined in

dota2.ts:157

___

### getAddonPath

▸ **getAddonPath**(`addonName?`): `Object`

获取addon目录 或自动创建

#### Parameters

| Name | Type |
| :------ | :------ |
| `addonName` | `string` |

#### Returns

`Object`

| Name | Type |
| :------ | :------ |
| `client` | `string` |
| `server` | `string` |

#### Defined in

dota2.ts:28

___

### getDotaPath

▸ **getDotaPath**(): `string`

获取dota2目录

#### Returns

`string`

#### Defined in

dota2.ts:10

___

### getMainMap

▸ **getMainMap**(): `string`

获取启动地图的名字

#### Returns

`string`

#### Defined in

dota2.ts:162

___

### images\_compiler

▸ **images_compiler**(`addonName?`): `Promise`<`undefined`\>

DOTA的动态资产（加载屏幕除外）
正在查找版本号？它不再需要。
更改下面引用的任何文件都将导致重建，
无论它是内容中直接引用的图像还是游戏中的脚本。
对切图统一处理， 写入Panorama Dynamic Images
在资源管理器中手动编译

#### Parameters

| Name | Type |
| :------ | :------ |
| `addonName` | `string` |

#### Returns

`Promise`<`undefined`\>

#### Defined in

dota2.ts:80

___

### keyInColumn

▸ **keyInColumn**(`sheet`): [`OutPutProps`](./interfaces/OutPutProps)

纵向键值表 键在0列

#### Parameters

| Name | Type |
| :------ | :------ |
| `sheet` | [`IncomeProps`](./interfaces/IncomeProps) |

#### Returns

[`OutPutProps`](./interfaces/OutPutProps)

#### Defined in

convert.ts:28

___

### keyInRow

▸ **keyInRow**(`sheet`, `keyRow?`): [`OutPutProps`](./interfaces/OutPutProps)

横向键值表

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `sheet` | [`IncomeProps`](./interfaces/IncomeProps) | `undefined` | 表格对象 |
| `keyRow` | `number` | `1` | 键所在行数 默认为1 |

#### Returns

[`OutPutProps`](./interfaces/OutPutProps)

#### Defined in

convert.ts:51

___

### mkjoin

▸ **mkjoin**(...`files`): `string`

获取一个指定路径，如果没有目录就创建

#### Parameters

| Name | Type |
| :------ | :------ |
| `...files` | `string`[] |

#### Returns

`string`

#### Defined in

files.ts:28

___

### pack

▸ **pack**(`data`): `Object`

根据layout.config.json 提供编译的配置函数
rollup compiler().map(e => rollup(e).then(k => k.write(e)))

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | [`layoutFileType`](./interfaces/layoutFileType)[] |

#### Returns

`Object`

| Name | Type |
| :------ | :------ |
| `compiler` | () => `RollupOptions`[] |
| `watch` | () => `BuildOptions` |
| `webpack` | () => `Configuration` |

#### Defined in

rollup.ts:108

___

### read\_all\_files

▸ **read_all_files**(`path`): `string`[]

迭代返回子级文件

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `path` | `string` | 读取目录 |

#### Returns

`string`[]

全部子文件清单

#### Defined in

files.ts:13

___

### symlink

▸ **symlink**(): `void`

创建目录链接

#### Returns

`void`

#### Defined in

dota2.ts:167

___

### toBytesInt32

▸ **toBytesInt32**(`id`): `string`

将整数 转译为 4字节的字符串

#### Parameters

| Name | Type |
| :------ | :------ |
| `id` | `number` |

#### Returns

`string`

#### Defined in

data.ts:13

___

### w2l

▸ **w2l**(`mapPath`, `compiler`): `Promise`<`unknown`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `mapPath` | `string` |
| `compiler` | `string` |

#### Returns

`Promise`<`unknown`\>

#### Defined in

war3.ts:68

___

### war3

▸ **war3**(): `Promise`<`string`\>

获取默认的war3游戏目录

#### Returns

`Promise`<`string`\>

#### Defined in

war3.ts:6

___

### watch

▸ **watch**<`T`\>(`path`, `callback`, `target`): `void`

表格转化监听函数

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `path` | `string`[] | 表格所在路径 |
| `callback` | (`files`: `string`[]) => `Promise`<`T`\> | 数据处理函数 |
| `target` | (`v`: `T`) => `void` | 写入函数 |

#### Returns

`void`

#### Defined in

convert.ts:94

___

### write

▸ **write**(...`file`): (`str`: `string`) => `string`

传入路径写入文件

#### Parameters

| Name | Type |
| :------ | :------ |
| `...file` | `string`[] |

#### Returns

`fn`

▸ (`str`): `string`

##### Parameters

| Name | Type |
| :------ | :------ |
| `str` | `string` |

##### Returns

`string`

#### Defined in

convert.ts:82

___

### ydwe

▸ **ydwe**(): `Promise`<`string`\>

获取默认的YDWE工具目录

#### Returns

`Promise`<`string`\>

#### Defined in

war3.ts:26

___

### ydweTool

▸ **ydweTool**<`T`\>(`params`, `arg?`): `Promise`<`unknown`\>

运行win64目录下的工具

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `params` | `T` extends [`ydweEXE`](./Exports#ydweexe) ? `T` : `string` |
| `arg?` | `string`[] |

#### Returns

`Promise`<`unknown`\>

#### Defined in

war3.ts:47
