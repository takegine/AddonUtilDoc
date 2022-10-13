## Table of contents

### Classes

- [ProgressBar](./classes/ProgressBar)

### Interfaces

- [IncomeProps](./interfaces/IncomeProps)
- [OutPutProps](./interfaces/OutPutProps)
- [xmlProps](./interfaces/xmlProps)

### Type Aliases

- [dotaEXE](./Exports#dotaexe)
- [ydweEXE](./Exports#ydweexe)

### Functions

- [connect](./Exports#connect)
- [content\_compiler](./Exports#content_compiler)
- [convert](./Exports#convert)
- [dotaTool](./Exports#dotatool)
- [fromBytesInt32](./Exports#frombytesint32)
- [getAddonPath](./Exports#getaddonpath)
- [getDotaPath](./Exports#getdotapath)
- [images\_compiler](./Exports#images_compiler)
- [keyInColumn](./Exports#keyincolumn)
- [keyInRow](./Exports#keyinrow)
- [mkjoin](./Exports#mkjoin)
- [read\_all\_files](./Exports#read_all_files)
- [toBytesInt32](./Exports#tobytesint32)
- [vite](./Exports#vite)
- [w2l](./Exports#w2l)
- [war3](./Exports#war3)
- [watch](./Exports#watch)
- [write](./Exports#write)
- [ydwe](./Exports#ydwe)
- [ydweTool](./Exports#ydwetool)

## Type Aliases

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

### connect

▸ **connect**(`quick`, `source`): `string`

硬链接两个目录 相对目录 或绝对目录均可

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `quick` | `string` | 快捷方式 |
| `source` | `string` | 源目录 |

#### Returns

`string`

mklink /J quick source

#### Defined in

connect.ts:16

___

### content\_compiler

▸ **content_compiler**(`addonName`): `Promise`<`undefined`\>

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

### getAddonPath

▸ **getAddonPath**(`addonName`): `Promise`<{ `client`: `string` ; `server`: `string`  }\>

获取addon目录

#### Parameters

| Name | Type |
| :------ | :------ |
| `addonName` | `string` |

#### Returns

`Promise`<{ `client`: `string` ; `server`: `string`  }\>

#### Defined in

dota2.ts:29

___

### getDotaPath

▸ **getDotaPath**(): `Promise`<`string`\>

获取dota2目录

#### Returns

`Promise`<`string`\>

#### Defined in

dota2.ts:9

___

### images\_compiler

▸ **images_compiler**(`addonName`): `Promise`<`string`\>

获取目录下全部css

#### Parameters

| Name | Type |
| :------ | :------ |
| `addonName` | `string` |

#### Returns

`Promise`<`string`\>

#### Defined in

dota2.ts:70

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

### vite

▸ **vite**(`data`, `panorama`, `client`): `Object`

创建所有的xml 监听并编译tsx

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | [`xmlProps`](./interfaces/xmlProps)[] |
| `panorama` | `string` |
| `client` | `string` |

#### Returns

`Object`

| Name | Type |
| :------ | :------ |
| `compiler` | () => `Promise`<`RollupOutput`\>[] |
| `data` | (`publish`: `boolean`) => `RollupOptions`[] |
| `watcher` | () => `RollupWatcher` |

#### Defined in

rollup.ts:95

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
