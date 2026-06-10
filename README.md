# RegionNameEditor
区域名称编辑器

## 操作方法
左键拖动，中键选择，右键填充。

## 文件格式
```JSON
{
    "table":[
        [1,2,3,4/*, ...(360列)*/],
        [1,2,3,4/*, ...(360列)*/]
        /*...(180行)*/
    ],
    "name":[
        "地名1",
        "地名2",
        "..."
    ]
}
```
获取经纬度对应的地名：(-90≤lat＜90, -180≤lon＜180)
```JS
const regions=JSON.parse("regions.json文件内容");
const name=regions.name[regions.table[Math.floor(lat)+90][Math.floor(lon)+180]];
```
