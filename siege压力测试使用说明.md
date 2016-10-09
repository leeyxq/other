###siege压力测试

siege -c 500 -t 1  -b -v --header="Cookie:JSESSIONID=D2480EC4DBF4F570823E2FBF8BB68A44" http://192.168.16.241:10080/atlasmaster/auth/list
<pre>
Usage: siege [options]
       siege [options] URL
       siege -g URL
Options:
  -V, --version           VERSION, prints the version number.
  -h, --help              HELP, prints this section.
  -C, --config            CONFIGURATION, show the current config.
  -v, --verbose           VERBOSE, prints notification to screen.         显示请求详细信息
  -g, --get               GET, pull down HTTP headers and display the     
                          transaction. Great for application debugging. 
  -c, --concurrent=NUM    CONCURRENT users, default is 10                 并发用户数
  -i, --internet          INTERNET user simulation, hits URLs randomly.   模拟用户随机访问url
  -b, --benchmark         BENCHMARK: no delays between requests.          请求之间没有延迟
  -t, --time=NUMm         TIMED testing where "m" is modifier S, M, or H  测试持续时长 不加单位默认分钟
                          ex: --time=1H, one hour test.
  -r, --reps=NUM          REPS, number of times to run the test.          重复测试次数，和-t只能使用一个
  -f, --file=FILE         FILE, select a specific URLS FILE.              指定访问url路径 默认 /etc/urls
  -R, --rc=FILE           RC, specify an siegerc file                         
  -l, --log[=FILE]        LOG to FILE. If FILE is not specified, the      测试日志文件
                          default is used: PREFIX/var/siege.log
  -m, --mark="text"       MARK, mark the log file with a string.
  -d, --delay=NUM         Time DELAY, random delay before each requst    每次请求间隔时长
                          between 1 and NUM. (NOT COUNTED IN STATS)
  -H, --header="text"     Add a header to request (can be many)          自定义头部，如添加Cookie等
  -A, --user-agent="text" Sets User-Agent in request
  
  </pre>
