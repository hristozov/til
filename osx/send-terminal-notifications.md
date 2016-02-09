# Send terminal notifications (2016-02-09)

Just install the [terminal-notifier](https://github.com/julienXX/terminal-notifier) gem (available in `brew` as well). Then, it's easy:

`terminal-notifier -message "Took 3:21." -title "Task finished." -subtitle "1.flv is uploaded."`

The `-execute` flag can specify a command that should be ran when the user clicks the notification popup.
