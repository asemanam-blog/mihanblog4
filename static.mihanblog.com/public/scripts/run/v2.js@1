var v2 = [];
var toobarArr = new Array();

$(document).ready(function()
{
    //return ;

    if(!v2.getCookie('v2.hideMihanTelegramBar') ) toobarArr.push( 'showMihanTelegramBar');
    if(!v2.getCookie('v2.hideMihanAppBar') && navigator.userAgent.toLowerCase().indexOf("android") !=-1) toobarArr.push( 'showMihanAppBar');
    if(toobarArr.length > 0){
        var rand = Math.floor(Math.random() +0.5)%toobarArr.length;
        eval('v2.'+toobarArr[rand]+'()');
    }

    $("body").on("click", "#v2-mihan-app-close", function(){
        $('body').removeClass("v2-has-app-bar");
        v2.setCookie('v2.hideMihanAppBar', 'true', 1);
    });
    $("body").on("click", "#v2-mihan-telegram-close", function(){
        $('body').removeClass("v2-has-app-bar");
        v2.setCookie('v2.hideMihanTelegramBar', 'true', 14);
    });

});

v2.showMihanAppBar = function(){
    //alert
    if(navigator.userAgent.toLowerCase().indexOf("android") == -1)
    {
        return false;
    }
    //return;
    if(this.getCookie('v2.hideMihanAppBar')) return false;
    $("body").addClass("v2-has-app-bar");
    $('<div id="v2-mihan-app-bar" >'
        + '<a href="#" id="v2-mihan-app-close">×</i></a>'
        + '<a href="http://www.mihanblog.com/android">'
        + '<div id="v2-mihan-app-icon"></div>'
        + '<div id="v2-mihan-app-info">'
        + '<div id="v2-mihan-app-title">میهن بلاگ</div>'
        + '<div id="v2-mihan-app-desc">نرم افزار اندروید را برای میهن بلاگ دانلود کنید.</div>'
        + '</div>'
        + '</a>'
        +'</div>').insertBefore("#wrapper");
};

v2.showMihanTelegramBar = function(){
    //alert

    return false;
    // if(!isMobileDevice)
    // {
    //     return false;
    // }
    //alert('vv');
    //return;
    if(this.getCookie('v2.hideMihanTelegramBar')) return false;
    $("body").addClass("v2-has-app-bar");
    $('<div id="v2-mihan-app-bar" class="telegram_bar">'
        + '<a href="#" id="v2-mihan-telegram-close">×</i></a>'
        + '<a href="http://telegram.me/mihanblog">'
        + '<div id="v2-mihan-telegram-icon"></div>'
        + '<div id="v2-mihan-app-info">'
        + '<div id="v2-mihan-app-desc">کانال میهن بلاگ در تلگرام را</div>'
        + '<div id="v2-mihan-app-follow">دنبال کنید</div>'
        + '</div>'
        + '</a>'
        +'</div>').insertBefore("#wrapper");
};

v2.setCookie = function (cName,value,exDays)
{
    if(!exDays) exDays = 365;
    var exDate=new Date() , cValue=encodeURI(value);

    exDate.setDate(exDate.getDate() + exDays);
    var expireDate = "; expires="+exDate.toUTCString();

    document.cookie=cName + "=" + cValue + expireDate;
};
v2.getCookie = function (cName)
{
    var i,x,y,arrCookies=document.cookie.split(";");
    for (i=0;i<arrCookies.length;i++)
    {
        x=arrCookies[i].substr(0,arrCookies[i].indexOf("="));
        y=arrCookies[i].substr(arrCookies[i].indexOf("=")+1);
        x=x.replace(/^\s+|\s+$/g,"");
        if (x==cName)
            return y;
    }
    return '';
};
