
参数：
配置项	说明
mode	 可能的取值为 'day', 'week',两种不同的模式。week每次显示一周，day每格显示一天。
startParam	 'start' 标志每个时间开始的参数。
endParam	 'end' 标志每个时间结束的参数。
headerFormat	 显示的时间格式
theme	 false：表示是否采用jquery ui的样式。
editable	 true：是否可以拖拽事件。
events	 [ { id : 1234, title: 'All Day Event', start: new Date(y, m, 1), top: 100, //离top的位置 } ]
接口：
refetchEvents	 重新获取事件并渲染
rerenderEvents(eventid)	 重新渲染事件,可以单独渲染某一个事件，没有参数则渲染全部事件。
select(start, end)	 选择特定的时间，但是没有生成事件。
gotoDate(date)	 跳转(滚动)到某个时间。
formatDate(format, date)	 按照format格式化时间。
getView()	 获取当前视图
setStartDate(date)	 设置甘特图的开始时间
setEndDate(date)	 设置甘特图的结束时间
changeMode(mode)	 改变视图的方式，day 或者 week
updateEvent(eventID)	 更新一个事件
renderEvent(eventObj)	 渲染一个事件
removeEvents(filter)	 删除满足条件的事件
addEventSource(eventSource)	 增加一个事件源，可以是一个数组 也可以是个url
removeEventSource(source)	 删除事件源，根据source判断相等
clientEvents()	 获取当前所有的事件
normalizeEvent(event)	 格式化事件，将事件的相关属性进行设置
事件：
windowResize(view)	 窗口大小发生变化。
dayContextmenu(date, allDay, jsEvent, view)	 在日期上触发右键时间jsEvent：是原生的js事件
normalizeEvent(event)	 格式化事件，将事件的相关属性进行设置
select: function(start, end)	 选择某段时间后触发
eventContextmenu(event,jsEvent,view)	 在事件上触发右击事件
eventClick(event, jsEvent, view)	 在事件上触发单击事件。
dayClick(date, allDay, jsEvent, view)	 在某天上触发单击
eventMouseover(event, jsEvent, view )	 在事件上触发mouseover事件
eventMouseout(event, jsEvent, view )	 在事件上触发mouseout事件
eventDragStart(event, jsEvent, ui, view)	 开始拖拽事件，可以通过返回false结束拖拽事件
eventDragStop(event, jsEvent, ui, view )	 结束拖拽
eventDrop(event, dayDelta, minuteDelta, allDay, revertFunc, jsEvent, ui, view)	 完成拖拽，可以通过调用revertFunc 返回调用之前的状态
eventResizeStart(event, jsEvent, ui, view)	 开始调整事件的大小，可以通过返回false阻止事件继续进行。
eventResizeStop(event, jsEvent, ui, view )	 结束拖拽
eventResize(event, dayDelta, minuteDelta, revertFunc, jsEvent, ui, view )	 完成调整，daydelta表示调整的天数，revertFunc返回调整之前的状态
