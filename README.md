# SimpleCalendar
日历标记节假日。。。
引入资源

# 使用日历插件前首先要引用资源：JS CSS

<link rel="stylesheet" type="text/css" href="css/simple-calendar.css">
<script type="text/jacascrip" src="js/simple-calendar.js"></script>

# 初始化一个日历

首先为calendar准备一个容器，可以设置大小，也可以在options中设置，不设置的话自动设为默认
<div id='container'></div>
<script>
    var myCalendar = new SimpleCalendar('#container');
</script>

# 配置项说明

var options = {
      width: '500px',
      height: '500px',
      language: 'CH', //语言
      showLunarCalendar: true, //阴历
      showHoliday: true, //休假
      showFestival: true, //节日
      showLunarFestival: true, //农历节日
      showSolarTerm: true, //节气
      showMark: true, //标记
      timeRange: {
        startYear: 1900,
        endYear: 2049
      },
      mark: {
        '2016-5-5': '上学'
      },
      theme: {
        changeAble: false,
        weeks: {
          backgroundColor: '#FBEC9C',
          fontColor: '#4A4A4A',
          fontSize: '20px',
        },
        days: {
          backgroundColor: '#ffffff',
          fontColor: '#565555',
          fontSize: '24px'
        },
        todaycolor: 'orange',
        activeSelectColor: 'orange',
      }
    }
    
    
  #   国际化

language： 语言的话目前只支持中文和英文，分别对应'CH','EN'
如果想要加更多的语言或者更改现在的显示，可以直接更改languageData内容

# 节日显示配置
showLunarCalendar: true, //是否显示阴历日期
showHoliday: true,       //是否显示休假休假
showFestival: true,      //是否显示国际节日
showLunarFestival: true, //是否显示农历节日
showSolarTerm: true,     //是否显示节气
showMark: true,          //是否显示标记日期



# 时间范围

这个时间范围设置的是下拉框中的年数范围

timeRange: {
    startYear: 1900,
    endYear: 2049
}
# 标记日期

# 标记日期配置只有在 showMark 为 true 时才会生效
mark: {
        '2016-5-5': '上学'
    }


这样就会在日历的对应日期上面添加标记，当鼠标停留时显示输入的信息

# 主题配置
theme: {
    changeAble: false,
    weeks: {
        backgroundColor: '#FBEC9C',
        fontColor: '#4A4A4A',
        fontSize: '20px',
    },
    days: {
        backgroundColor: '#ffffff',
        fontColor: '#565555',
        fontSize: '24px'
    },
    todaycolor: 'orange',
    activeSelectColor: 'orange',
    
}
主题配置只有在changeAble 为 true 时才会生效 
weeks 设置的是星期一栏的主题，分别对应背景颜色，字体颜色，字体大小 
days 设置的是日期的主题，参数同上 
todaycolor 设置的是当天的日期背景颜色 
activeSelectColor 设置的是鼠标滑过事件对应日期的边框颜色

# 事件接口说明

myCalendar.updateSize('500px', '500px');
myCalendar.addMark('2016-3-7', 'test');
myCalendar.setLanguage('EN')
myCalendar.showFestival(false);
myCalendar.showLunarCalendar(false);
myCalendar.showHoliday(false);
myCalendar.showSolarTerm(false);
myCalendar.showLunarFestival(false);
myCalendar.showMark(false);
updateSize(width,height)


# 调整日历大小，会自动根据大小调整对应的样式

# addMark(day, info)
day 是一个可以确定一个日期的字符串 info 是要显示的信息

# setLenguage(languageStr)
设置语言，目前支持的语言有'CH','EN' 如果想要增加语言，请在languageData中修改

# 其他
//关闭或者显示国际节日
showFestival(false); 
//关闭或者显示阴历日期
showLunarCalendar(false);
//关闭或者显示假期
showHoliday(false);
//关闭或者显示二十四节气
showSolarTerm(false);
//关闭或者显示阴历节日
showLunarFestival(false);
//关闭或者显示标记
showMark(false)
