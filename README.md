# ci-zap

## Notes for zap-baseline users

_May want to incorporate some of these ideas/options into default operation_

- There is a Progress file option that allows you to associated a ticket - this seems like a much better option for fixable issues: <https://www.zaproxy.org/docs/docker/baseline-scan/#progress-file>
- For false positives our best bet is to use the OUTOFSCOPE rule to exclude just the URLs that are alerting.
- Between these two, we should _not_ be using WARN/IGNORE at all, unless there is an issue that we have determined is (a) real but (b) not worth fixing. 
- The reports (html, markdown etc) appear to record all scan fails, regardless of the zap-baseline rule configs and progress file. Best to treat the text output zap-baseline as the primary artifact and the html (or other) report as a supplementary artifact to be used to describe the fails etc.
