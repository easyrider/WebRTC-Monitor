exec = require('child_process').exec
task 'test', 'run all tests suites', ->
    console.log 'Running front-end tests'
    chrome_bin = "DISPLAY=:99"
    karma = "#{__dirname}/.node_modules/bin/karma"
    browsers = '.travis/chrome-start.sh'
    options = "--single-run --browsers=#{browsers}"
    exec "#{chrome_bin} #{karma} start #{__dirname}/.travis/karma.conf.js", (err, stdout, stderr) ->
        console.error err if err
        console.log stdout
