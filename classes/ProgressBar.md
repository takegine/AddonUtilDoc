封装的 ProgressBar 工具，方便在控制台输出进度

## Table of contents

### Constructors

- [constructor](./ProgressBar#constructor)

### Properties

- [bar\_length](./ProgressBar#bar_length)
- [description](./ProgressBar#description)
- [error](./ProgressBar#error)

### Methods

- [render](./ProgressBar#render)

## Constructors

### constructor

• **new ProgressBar**(`description?`, `bar_length?`)

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `description` | `string` | `'Progress'` | 命令行开头的文字信息 |
| `bar_length` | `number` | `25` | 进度条的长度(单位：字符)，默认设为 25 |

#### Defined in

progressBar.ts:7

## Properties

### bar\_length

• **bar\_length**: `number` = `25`

进度条的长度(单位：字符)，默认设为 25

#### Defined in

progressBar.ts:11

___

### description

• **description**: `string` = `'Progress'`

命令行开头的文字信息

#### Defined in

progressBar.ts:9

___

### error

• **error**: `string` = `''`

#### Defined in

progressBar.ts:6

## Methods

### render

▸ **render**(`opts`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `opts` | `Object` |
| `opts.completed` | `number` |
| `opts.err?` | `string` |
| `opts.msg?` | `string` |
| `opts.total` | `number` |

#### Returns

`void`

#### Defined in

progressBar.ts:14
