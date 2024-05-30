# my-python-visualization-examples
import matplotlib.pyplot as plt

#making line graph
views=(234,567,789,765,234,564,345)
days=range(1,8)
plt.plot(days,views,label="rate",color="m",linestyle='-.',marker='o',linewidth=2)
plt.xlabel('days')
plt.ylabel('views')
plt.title('days per view')
plt.legend(loc= 'upper right')

#making line graph for multiple y values
y_views=(234,567,789,765,234,564,745)
n_views=(534,767,189,345,274,164,345)
t_views=(834,767,489,365,634,164,145)
days=range(1,8)
plt.plot(days,y_views,label="y_rate",color="m",linestyle='-.',marker='o',linewidth=2)
plt.plot(days,n_views,label="n_rate",color="r",linestyle='-.',marker='o',linewidth=2)
plt.plot(days,t_views,label="t_rate",color="b",linestyle='-.',marker='o',linewidth=2)
plt.xlabel('days')
plt.ylabel('views')
plt.title('days per view')
plt.legend(loc= 'upper right')

#setting up grid lines
y_views=(234,567,789,765,234,564,745)
n_views=(534,767,189,345,274,164,345)
t_views=(834,767,489,365,634,164,145)
days=range(1,8)
plt.plot(days,y_views,label="y_rate",color="m",linestyle='-.',marker='o',linewidth=2)
plt.plot(days,n_views,label="n_rate",color="r",linestyle='-.',marker='o',linewidth=2)
plt.plot(days,t_views,label="t_rate",color="b",linestyle='-.',marker='o',linewidth=2)
plt.xlabel('days')
plt.ylabel('views')
plt.title('days per view')
plt.legend(loc= 'upper right')
#setting up grid lines
plt.grid(True,linewidth=1,color='black',linestyle='-.')

#x and y axis limits
y_views=(234,567,789,765,234,564,745)
n_views=(534,767,189,345,274,164,345)
t_views=(834,767,489,365,634,164,145)
days=range(1,8)
plt.plot(days,y_views,label="y_rate",color="m",linestyle='-.',marker='o',linewidth=2)
plt.plot(days,n_views,label="n_rate",color="r",linestyle='-.',marker='o',linewidth=2)
plt.plot(days,t_views,label="t_rate",color="b",linestyle='-.',marker='o',linewidth=2)
plt.xlabel('days')
plt.ylabel('views')
plt.title('days per view')
plt.legend(loc= 'upper right')
#x and y axis limits
plt.xlim(1,5)
plt.ylim(200,700)

#saving the graph
y_views=(234,567,789,765,234,564,745)
n_views=(534,767,189,345,274,164,345)
t_views=(834,767,489,365,634,164,145)
days=range(1,8)
plt.plot(days,y_views,label="y_rate",color="m",linestyle='-.',marker='o',linewidth=2)
plt.plot(days,n_views,label="n_rate",color="r",linestyle='-.',marker='o',linewidth=2)
plt.plot(days,t_views,label="t_rate",color="b",linestyle='-.',marker='o',linewidth=2)
plt.xlabel('days')
plt.ylabel('views')
plt.title('days per view')
plt.legend(loc= 'upper right')
plt.grid(True,linewidth=1,color='black',linestyle='-.')
plt.savefig('C:/Users/ISAK_ABR/Desktop/New folder (3)',dpi=500,facecolor='b')

#scatter plots

views=(234,567,789,765,234,564,345,564,1233,456,789,900,444,555)
days=range(1,15)
plt.scatter(days,views,label="rate",color="m",linestyle='-.',marker='o',linewidth=2)
plt.xlabel('days')
plt.ylabel('views')
plt.title('days per view')
plt.legend(loc= 'upper right')
plt.grid(True,linestyle='--',color='b',linewidth=1)

views = (234, 567, 789, 765, 234, 564, 345, 564, 1233, 456, 789, 900, 444, 555)
days = range(1, 7)

#bar graph
plt.bar(days, views, label="rate", color="m")
plt.xlabel('days')
plt.ylabel('views')
plt.title('days per view')
plt.legend(loc='upper right')
plt.grid(True, linestyle='--', color='b', linewidth=1)
plt.show()

#comparison with bar graph 
y_views=(234,567,789,765,234,564,745)
n_views=(534,767,189,345,274,164,345)
days = range(1, 8)

plt.bar([a-0.25 for a in days], y_views,width=0.25, label="rate", color="m",align='edge')
plt.bar([a+0.25 for a in days], n_views,width=-0.25, label="rate", color="r",align='edge')
plt.xlabel('days')
plt.ylabel('views')
plt.title('days per view')
plt.legend(loc='upper left')
plt.xticks(days)
plt.show()

#histograms
views = [234, 567, 789, 765, 234, 564, 345]
bins = [1,2,3,4,5,6, 7]
plt.hist(days, bins, label="rate", color="m")
plt.xlabel('days')
plt.ylabel('views')
plt.title('days per view')
plt.legend(loc='upper right')
plt.grid(True, linestyle='--', color='b', linewidth=1)
plt.show()

#pie chart
medias=('facebook','youtube','tiktok','instagram')
explode=(0,0.2,0,0)
views=(234,567,789,543)
plt.pie(views,labels=medias,explode=explode,autopct='%1.1f%%',shadow='True')
plt.savefig('C:/Users/ISAK_ABR/Desktop/New folder (6)')

#text annotations
views=(234,567,789,765,234,564,345)
days=range(1,8)
min_views=min(views)
days_co=days[views.index(min_views)]
plt.plot(days,views,label="rate",color="m",linestyle='-.',marker='o',linewidth=2)
plt.xlabel('days')
plt.ylabel('views')
plt.title('days per view')
plt.legend(loc= 'upper right')
plt.annotate('lowest value',
            xy=(days_co,min_views),
            xytext=(5,300),
            arrowprops=dict(facecolor='black',shrink=0.07))

#using style sheets
print(plt.style.available)

y_views=(234,567,789,765,234,564,745)
n_views=(534,767,189,345,274,164,345)
days = range(1, 8)
plt.style.use('Solarize_Light2')
plt.bar([a-0.25 for a in days], y_views,width=0.25, label="rate", color="m",align='edge')
plt.bar([a+0.25 for a in days], n_views,width=-0.25, label="rate", color="r",align='edge')
plt.xlabel('days')
plt.ylabel('views')
plt.title('days per view')
plt.legend(loc='upper left')
plt.xticks(days)
plt.show()





