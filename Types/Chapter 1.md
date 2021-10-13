# Типы значения | Ссылочные типы
## Типы значений


#### Неявное преобразование<br>
Расширение*

| sbyte     | byte      | short     | ushort    | int       | uint      | long      | ulong     | nint      | nuint     |
|------     |-----      |------     |-------    |----       |-----      |-----      |------     |-----      |-----      |
| short     | short     | int       | int       | long      | long      | float     | float     | long      | ulong     |
| int       | ushort    | long      | uint      | float     | ulong     | double    | double    | float     | float     |
| long      | int       | float     | long      | double    | float     | decimal   | decimal   | double    | double    |
| float     | uint      | double    | ulong     | decimal   | double    |           |           | decimal   | decimal   |
| double    | long      | decimal   | float     | nint      | decimal   |           |           |           |           |
| decimal   | ulong     | nint      | double    |           | nuint     |           |           |           |           |
| nint      | float     |           | decimal   |           |           |           |           |           |           |
|           | double    |           | nint      |           |           |           |           |           |           |
|           | decimal   |           | nuint     |           |           |           |           |           |           |
|           | nint      |           |           |           |           |           |           |           |           |
|           | nuint     |           |           |           |           |           |           |           |           |



| char      | bool      | float     |   decimal | double    |
| ----      | ----      | ----      |    ----   |    ----   |
| ushort    |           | double    |           |           |
| int       |           |           |           |           |
| uint      |           |           |           |           |
| long      |           |           |           |           |
| ulong     |           |           |           |           |
| float     |           |           |           |           |
| double    |           |           |           |           |
| decimal   |           |           |           |           |



| enum | struct | (type,type) | null | 
|----- |------- |------------ |----- |
|      |        | (type,type) |      |


#### Явное преобразование<br>
Сужение*

| sbyte     | byte      | short     | ushort    | int       | uint      | long      | ulong     | nint      | nuint     |
|------     |-----      |------     |-------    |----       |-----      |-----      |------     |-----      |-----      |
| byte      | sbyte     | sbyte     | sbyte     | sbyte     | sbyte     | sbyte     | sbyte     | sbyte     | sbyte     |
| ushort    | char      | byte      | byte      | byte      | byte      | byte      | byte      | byte      | byte      |
| uint      |           | ushort    | short     | short     | short     | short     | short     | short     | short     |
| ulong     |           | uint      |           | ushort    | ushort    | ushort    | ushort    | ushort    | ushort    |
| nuint     |           | ulong     |           | uint      | int       | int       | int       | int       | int       |
| char      |           | nuint     |           | ulong     |           | uint      | uint      | uint      | uint      |
|           |           | char      |           | nuint     |           | ulong     | long      | ulong     | ulong     |
|           |           |           |           |           |           | nint      | nint      | nuint     | nint      |
|           |           |           |           |           |           | nuint     | nuint     |           |           |
|           |           |           |           |           |           |           |           |           |           |
|           |           |           |           |           |           |           |           |           |           |


| char      | bool | decimal | double  | float   |
| ----      | ---- | ----    | ----    | ----    |
| sbyte     |      | sbyte   | sbyte   | sbyte   |
| byte      |      | byte    | byte    | byte    |
| short     |      | short   | short   | short   |
|           |      | ushort  | ushort  | ushort  |
|           |      | int     | int     | int     |
|           |      | uint    | uint    | uint    |
|           |      | long    | long    | long    |
|           |      | ulong   | ulong   | ulong   |
|           |      | float   | float   | decimal |
|           |      | double  | decimal | nint    |
|           |      | nint    | nint    |  nuint  |
|           |      | nuint   | nuint   |         |


| enum | struct | (type,type) | null | 
|----- |------- |------------ |----- |
|      |        | (type,type) |      |


## Ссылочные типы

| enum | struct | (type,type) | null | 
|----- |------- |------------ |----- |
|      |        | (type,type) |      |


<br>
<br>
<br>
<br>


 ### Неявные преобразования
 
 | из \ в | sbyte | byte | short | ushort | int | uint | long | ulong | float | double | decimal | char | bool | object | string |
 | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: |
 | **sbyte** | + | - | + | - | + | - | + | - | + | + | + | - | - | + | - |
 | **byte** | - | + | + | + | + | + | + | + | + | + | + | - | - | + | - |
 | **short** | - | - | + | - | + | - | + | - | + | + | + | - | - | + | - |
 | **ushort** | - | - | - | + | + | + | + | + | + | + | + | - | - | + | - |
 | **int** | - | - | - | - | + | - | + | - | + | + | + | - | - | + | - |
 | **uint** | - | - | - | - | - | + | + | + | + | + | + | - | - | - | - |
 | **long** | - | - | - | - | - | - | + | - | + | + | + | - | - | - | - |
 | **ulong** | - | - | - | - | - | - | - | + | + | + | + | - | - | - | - |
 | **float** | - | - | - | - | - | - | - | - | + | + | - | - | - | - | - |
 | **double** | - | - | - | - | - | - | - | - | - | + | - | - | - | - | - |
 | **decimal** | - | - | - | - | - | - | - | - | - | - | + | - | - | - | - |
 | **char** | - | - | - | + | + | + | + | + | + | + | + | + | - | + | - |
 | **bool** | - | - | - | - | - | - | - | - | - | - | - | - | + | - | - |
 | **object** | - | - | - | - | + | - | + | - | + | + | + | - | - | + | - |
 | **string** | - | - | - | - | - | - | - | - | - | - | - | - | - | - | + |

 ### Явные преобразования

| из \ в | sbyte | byte | short | ushort | int | uint | long | ulong | float | double | decimal | char | bool | object | string |
| :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: |
| **sbyte** | + | + | + | + | + | + | + | + | + | + | + | + | - | + | - |
| **byte** | + | + | + | + | + | + | + | + | + | + | + | + | - | + | - |
| **short** | + | + | + | + | + | + | + | + | + | + | + | + | - | + | - |
| **ushort** | + | + | + | + | + | + | + | + | + | + | + | + | - | + | - |
| **int** | + | + | + | + | + | + | + | + | + | + | + | + | - | + | - |
| **uint** | + | + | + | + | + | + | + | + | + | + | + | + | - | + | - |
| **long** | + | + | + | + | + | + | + | + | + | + | + | + | - | + | - |
| **ulong** | + | + | + | + | + | + | + | + | + | + | + | + | - | + | - |
| **float** | + | + | + | + | + | + | + | + | + | + | - | + | - | + | - |
| **double** | + | + | + | + | + | + | + | + | + | + | - | + | - | + | - |
| **decimal** | - | - | - | - | - | - | - | - | + | + | + | - | - | - | - |
| **char** | + | + | + | + | + | + | + | + | + | + | + | + | - | + | - |
| **bool** | - | - | - | - | - | - | - | - | - | - | - | - | + | - | - |
| **object** | + | + | + | + | + | + | + | + | + | + | + | + | - | + | - |
| **string** | - | - | - | - | - | - | - | - | - | - | - | - | - | - | + |

