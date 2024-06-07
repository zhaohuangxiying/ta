   // 统计代码
   window.onload = function () {
    // 统计代码
    // 正式：https://rmt-zuul.81.cn
    // 测试：https://zuul.cbf.k8s01.tikrnews.com:9000
    var channel_classify_idE = $("meta[name='catalogs']");
    var article_idE = $("meta[name='contentid']");
    var param = ''
    var channel_classify_id = ''
    var article_id = ''
    if (channel_classify_idE.length > 0) {
        channel_classify_id = channel_classify_idE.attr('content').replace('cbf-', '')
        param += '&channel_classify_id=' + channel_classify_id
    }
    if (article_idE.length > 0) {
        article_id = article_idE.attr('content').replace('cbf-', '')
        param += '&art_id=' + article_id
    }
    $.ajax({
        url: 'https://rmt-zuul.81.cn/api-traffic/web/pollAll?host=' + window.location.host + param,
        type: 'GET',
        success: function (res) {
        console.log('执行点击量监控')
        },
        error: function (error) {},
    })

    // 统计代码
    $.ajax({
        url:
        'https://rmt-zuul.81.cn/api-traffic/web/poll?u=' + window.location.href,
        type: 'GET',
        success: function (res) {
        console.log('执行点击量监控')
        },
        error: function (error) {},
    })
    if ($('.bdsharebuttonbox').length > 0) {
        $('.bdsharebuttonbox a').on('click', function () {
        // 分享代码
        $.ajax({
            url:
            'https://rmt-zuul.81.cn/api-traffic/web/share?u=' +
            window.location.href,
            type: 'GET',
            success: function (res) {
            console.log('执行分享量监控')
            },
            error: function (error) {},
        })
        })
    }
}