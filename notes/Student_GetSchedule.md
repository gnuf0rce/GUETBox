*  [API NAME] 

    > 课程表获取接口

---
* [API DESCRIPTION]

    > url: /Student/GetStuTable
    > 
    > method: POST/GET
    > 
    > note: 
    <br> 根据输入的学期，给出这个学期已选理论课程的课程表

---
* [API ARGUMENTS]

    > Name | type | info | example
    > :---:|:---:|:---:|:---:
    > term | string | 学期 | 2018-2019_2

--- 
* [RETURN DATA]
  
    > type: json
    >
    > example: ```{"success":true,"total":0,"data":[]}```
    > 
    > format:
    > > Name | Type | Info | example
    > > :---:|:---:|:---:|:---:
    > > sucess | bool | 操作是否成功 | true <br> false
    > > total | int | 未知 | 0
    > > data | object[] | 上课安排记录 | 见下表
    >
    > object of data: <br>
    > ps: 只列出对象中的有用的属性
    > > Name | Type | Info | example
    > > :---:|:---:|:---:|:---:
    > > cname | string | 课程名称 | 体育4
    > > courseno | string | 课程序号 | 1821135
    > > courseid | string | 课程代号 | BG0000027X0
    > > teacherno | string | 教师代号 | 077786
    > > name | string | 教师姓名 | 温织琳 
    > > croomno | string | 上课教室 | 02203
    > > startweek | int | 开始周次 | 1
    > > endweek | int | 结束周次 | 16
    > > weeek | int | 上课星期 | 3
    > > seq | string | 上课节次 | "2"
    > > comm | string | 备注信息，一般为空| |
    > > term | srting | 学期 | 2018-2019_2
* [SUPPLEMENT]
    > A complete json: <br>
 ```
{ 
    "success":true, 
    "total":0, 
    "data":[ 
        { 
            "id":509902, 
            "ctype":"BG", 
            "tname":"公共必修", 
            "examt":"考查", 
            "dptname":null, 
            "dptno":"20", 
            "spname":null, 
            "spno":"080605", 
            "grade":"2017", 
            "cname":"体育4",
            "courseno":"1821135", 
            "teacherno":"077786",
            "name":"温织琳", 
            "term":"2018-2019_2", 
            "courseid":"BG0000027X0", 
            "croomno":null, 
            "comm":null, 
            "startweek":1, 
            "endweek":16, 
            "oddweek":null, 
            "week":3, 
            "seq":"2", 
            "maxcnt":0, 
            "xf":2, 
            "llxs":32, 
            "syxs":0, 
            "sjxs":0, 
            "qtxs":0, 
            "sctcnt":38, 
            "hours":0
        } 
    ] 
}
```


