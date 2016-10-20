# CurrentHTMLNAVBG
JS 判断当前页面的选中状态
 ----------------------------
 <script type="text/javascript">
        var urlstr = location.href;
        //.alert((urlstr + '/').indexOf($(this).attr('href')));
        var urlstatus=false;
        $("#menu a").each(function () {
            if ((urlstr + '/').indexOf($(this).attr('href')) > -1&&$(this).attr('href')!='') {

                $(this).addClass('bg_a'); urlstatus = true;
            } else {

                $(this).removeClass('bg_a');
            }
        });
        if (!urlstatus) {$("#menu a").eq(0).addClass('bg_a'); }
    </script>
 -----------------------------------
 根据判断点击栏目后，增加或移除“bg_a”CSS
