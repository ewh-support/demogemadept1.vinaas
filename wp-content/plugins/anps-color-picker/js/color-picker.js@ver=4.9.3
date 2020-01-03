'use-strict';

jQuery(function($) {
    /* Open/close color picker */
    $('.anps-cp-toggle').on('click', function() {
        $('body').toggleClass('anps-cp-open');
        $(this).blur();
    });

    /* Disable when vertical menu is active */
    if( $('.vertical-menu').length ) {
        $('#boxed, #sticky, [name="pattern"]').prop('disabled', 'disabled');
    }

    /*-----------------------------------------------------------------------------------*/
    /*  Demos
    /*-----------------------------------------------------------------------------------*/

    // var currentDemo = window.location.href.match(/demo-(.)/)[0];
    var currentDemo = window.location.href.match(/transport-new-demos\/(.)/)[0];
    if( currentDemo !== sessionStorage.getItem('currentDemo') ) {
        var options = ['style', 'boxed', 'sticky', 'pattern']

        /* Clear all options when switching demos */
        options.forEach(function(option) {
            sessionStorage.removeItem(option);
        });
    }

    sessionStorage.setItem('currentDemo', currentDemo);

    /*-----------------------------------------------------------------------------------*/
    /*  Sticky
    /*-----------------------------------------------------------------------------------*/

    /* Initial */
    if( sessionStorage.getItem('sticky') === 'false' ) {
        $('#sticky').prop('checked', null);
    } else if( $('.site-header-sticky').length || sessionStorage.getItem('sticky') === 'true' ) {
        $('#sticky').prop('checked', 'checked');
        sessionStorage.setItem('sticky', true);
    }

    function setSticky() {
        $stickyEl = $('.header-wrap');
        adminBarHeight = 0;
        if ($('#wpadminbar').length) {
            adminBarHeight = $('#wpadminbar').outerHeight();
        }
        topOffsetSticky = 0;
        topOffsetSticky = adminBarHeight;
        headerHeight = 0;
        headerHeight = $('.site-header').outerHeight();


        if( sessionStorage.getItem('sticky') === 'true' ) {
            $('body').addClass('stickyheader');
            $('.site-header').addClass('site-header-sticky');
            if( $(window).scrollTop() > 100 ) {
                $('.site-header').addClass('site-header-sticky-active');
                if (topOffsetSticky != '0') {
                    $stickyEl.css({
                        top: adminBarHeight + 'px'
                    });
                }
            }
        } else {
            $('body').removeClass('stickyheader');
            $('.site-header').removeClass('site-header-sticky-active');
            $('.site-header').removeClass('site-header-sticky');
            $('.site-main').css('padding-top', '0');
        }
    }

    $('#sticky').on('change', function() {
        sessionStorage.setItem('sticky', $(this).is(':checked'));
        setSticky();
    });

    setSticky();

    /*-----------------------------------------------------------------------------------*/
    /*  Boxed
    /*-----------------------------------------------------------------------------------*/

    function changePattern() {
        if( $('body').hasClass('boxed') ) {
            /* Remove old pattens */
            for(var i=1; i<=6; i++) {
                $('body').removeClass('pattern-' + i);
            }

            var stored = sessionStorage.getItem('pattern');
            var pattern = stored !== null ? stored : 'pattern-1';

            /* Set new pattern */
            $('body').addClass(pattern);
        }
    }

    /* Change layout */
    function changeLayout() {
        if( sessionStorage.getItem('boxed') !== null ) {
            if( sessionStorage.getItem('boxed') === 'true' ) {
                $('body').addClass('boxed');
                $('#patterns').slideDown();
            } else {
                $('body').removeClass('boxed');
                $('#patterns').slideUp();
            }

            $(window).trigger('resize');

            changePattern();
        }
    }

    /* Set Initial Values */
    if( sessionStorage.getItem('boxed') === 'false' ) {
        $('#boxed').prop('checked', null);
    } else if( $('body.boxed').length || sessionStorage.getItem('boxed') === 'true' ) {
        $('#boxed').prop('checked', 'checked');
        $('#patterns').slideDown();
    }

    if( sessionStorage.getItem('pattern') !== null ) {
        $('#' + sessionStorage.getItem('pattern')).prop('checked', 'checked');
    } else if( $('[class*="pattern"]').length ) {
        $('#' + $('body').attr('class').match(/pattern-(.)/)[0]).prop('checked', 'checked');
    }

    /* On layout & pattern change */
    $('#boxed, [name="pattern"]').on('change', function() {
        sessionStorage.setItem('boxed', $('#boxed').is(':checked'));
        sessionStorage.setItem('pattern', $('[name="pattern"]:checked').attr('id'))
        changeLayout();
    });

    /* Change layout on load */
    changeLayout();

    /*-----------------------------------------------------------------------------------*/
    /*  Styles (colors)
    /*-----------------------------------------------------------------------------------*/

    var old = 'style-1';
    if( $('#theme_wordpress_style-inline-css').html().indexOf('4ab9cf') > -1 ) {
        old = 'style-2';
        $('#style-2').prop('checked', 'checked');
    } else if (
        $('#theme_wordpress_style-inline-css').html().indexOf('86d33b') > -1 ) {
        old = 'style-3';
        $('#style-3').prop('checked', 'checked')
    } else if (
        $('#theme_wordpress_style-inline-css').html().indexOf('bf2626') > -1 ) {
        old = 'style-4';
        $('#style-4').prop('checked', 'checked')
    }

    if( sessionStorage.getItem('style') !== null ) {
        $('#' + sessionStorage.getItem('style')).prop('checked', 'checked')
    }

    function changeLogos(id) {
        if( $('.logo-background').length || $('.site-header-style-transparent').length) {
            $('.site-logo img:not(.logo-sticky)').attr('src', $('#plugin-path').val() + '/img/light-logos/' + id + '.png');
        } else {
            $('.site-logo img:not(.logo-sticky)').attr('src', $('#plugin-path').val() + '/img/logos/' + id + '.png');
        }

        $('.logo-sticky').attr('src', $('#plugin-path').val() + '/img/logos/' + id + '.png');

        $('.widget_anpsimages img').attr('src', $('#plugin-path').val() + '/img/footer-logos/' + id + '.png');
    }

    function changeMarkers(id) {
        if( typeof window.anpsMarkers === 'undefined' ) return false;

        if( typeof id === 'undefined' ) {
            id = sessionStorage.getItem('style');
        }

        window.anpsMarkers.forEach(function(marker) {
            marker.setIcon($('#plugin-path').val() + '/img/markers/' + id + '.png');
        });
    }

    window.anpsMapsLoaded = changeMarkers;

    function changeCode(el, schemes, id, addRev) {
        var code = $(el).html();
        for(var i=0; i<schemes['style-1'].length; i++) {
            code = code.replace(new RegExp(schemes[old][i], 'g'), schemes[id][i]);
        }

        if( addRev ) {
            code += '.anps-cp-rev:not(.no-bg) { background-color: #' + schemes[id][1] + ' !important; } \
            .anps-cp-rev:not(.no-bg) { border-color: #' + schemes[id][1] + ' !important; } \
            .anps-cp-rev:not(.no-bg):hover { background-color:  #' + schemes[id][3] + ' !important; } \
            .anps-cp-rev:not(.no-bg):hover { border-color:  #' + schemes[id][3] + ' !important; } \
            ';
        }

        $(el).html(code);
    }

    function changeRS(schemes, id) {
        if( !$('.rev-btn').length ) return false;

        // var str = $('.rev-btn').attr('data-style_hover');
        // var strColor = str.substring(str.lastIndexOf(':') + 1, str.lastIndexOf(';'));

        $('.rev-btn').each(function() {
            if( $(this).css('background-color') === 'rgb(255, 255, 255)' ) return true;

            $(this).addClass('anps-cp-rev');
        });
    }

    function changeStyle(fallback) {
        var id = $(this).attr('id') ? $(this).attr('id') : fallback;
        // console.log(currentDemo);
        if ( currentDemo == 'transport-new-demos/4' || currentDemo == 'transport-new-demos/3') {
            var schemes = {
                // hovers, default button bg color, shopping cart color,  revolution button hover bg
                'style-1': ['1874c1', '1874c2', '26507a', '175f9c'], // blue
                'style-2': ['4ab9cf', '4ab9cd', '4ab9ce', '42c7de'], //turquize
                'style-3': ['74b830', '86d33b', '86d33a', '64a224'], //green
                'style-4': ['bf2626', 'd82a2a', 'd82a2b', 'fd7062'], // red
            }
        } else if ( currentDemo == 'transport-new-demos/1') {
             var schemes = {
                // hovers, default button bg color, shopping cart color,  revolution button hover bg], shop elements, additional hover color
                'style-1': ['153d5c', '1874c1', '26507a', '175f9c', '94cfff' ], // blue
                'style-2': ['4ab9cf', '4ab9cd', '4ab9ce', '42c7de', '3498db'], //turquize
                'style-3': ['74b830', '86d33b', '86d33a', '74b831', '74b832' ], //green
                'style-4': ['d82a2b', 'd82a2a', 'd82a2a', 'bf2626', 'fd7061'], // red
            }
        } else if ( currentDemo == 'transport-new-demos/2') {
             var schemes = {
                // hovers, default button bg color, shopping cart color,  revolution button hover bg], shop elements, button 4 hover
                'style-1': ['153d5c', '1874c1', '26507a', '175f9c', '94cfff'], // blue
                'style-2': ['4ab9cf', '4ab9cd', '4ab9ce', '42c7de', '3498db'], //turquize
                'style-3': ['74b830', '86d33b', '86d33a', '74b831', '64a224'], //green
                'style-4': ['fd7062', 'd82a2a', 'd82a2b', 'bf2626', 'fd7061'], // red
            }
        } else { // demo 5, 6
            var schemes = {
                    // hovers (btn), default button bg color, shopping cart color,  revolution button hover bg], additional hover color
                    'style-1': ['153d5c', '1874c2', '26507a', '175f9c', '153d5d'], // blue
                    'style-2': ['42c7df', '4ab9cd', '4ab9ce', '42c7de', '42c7dd'], //turquize
                    'style-3': ['74b830', '86d33b', '86d33a', '74b831', '74b831'], //green
                    'style-4': ['fd7062', 'd82a2a', 'd82a2b', 'bf2626', 'c22727'], // red
            }
        }
        /* Change Google Maps Markers */
        changeMarkers(id);

        /* Revolution Slider */
        changeRS(schemes, id);

        /* Change Logos */
        changeLogos(id);

        /* Theme Colors */
        changeCode('#theme_wordpress_style-inline-css', schemes, id, true);

        if( $('.download').length ) {
            changeCode('.download', schemes, id);
        }

        /* Visual Composer */
        if( $('[data-type="vc_shortcodes-custom-css"]').length ) {
            changeCode('[data-type="vc_shortcodes-custom-css"]', schemes, id);
        }

        /* Store current style */
        old = id;
        sessionStorage.setItem('style', id);

        loadSpecificStyles(id, schemes);

    }

    $('[name="style"]').on('change', changeStyle);
    changeStyle(sessionStorage.getItem('style') ? sessionStorage.getItem('style'): old);

    /*-----------------------------------------------------------------------------------*/
    /*  Analytics
    /*-----------------------------------------------------------------------------------*/
    /* Toggle */
    $('.anps-cp-toggle').on('click', function() {
        if( typeof ga !== 'undefined' ) {
            // console.log('sent');
            ga('send', 'event', 'Transport Color Picker', 'Toggle');
        }
    });

    /* Style & Pattern */
    $('.anps-cp-select label').on('click', function() {
        if( typeof ga !== 'undefined' ) {
            var eventValue = $(this).attr('for').replace(/\-/g, ' ');
            eventValue = eventValue.charAt(0).toUpperCase() + eventValue.slice(1);

            var eventLabel = 'Style';
            if( $(this).attr('for').indexOf('pattern') > -1 ) {
                eventLabel = 'Pattern';
            }

            ga('send', 'event', 'Transport Color Picker', eventLabel, eventValue);
        }
    });

    /* Sticky & Boxed */
    $('#boxed, #sticky').on('change', function() {
        $el = $(this).next();

        var eventLabel = $el.attr('for');
        eventLabel = eventLabel.charAt(0).toUpperCase() + eventLabel.slice(1);

        var eventValue = 'OFF';
        if( $el.prev().is(':checked') ) {
            eventValue = 'ON';
        }

        if( typeof ga !== 'undefined' ) {
            ga('send', 'event', 'Transport Color Picker', eventLabel, eventValue);
        }
    });

    /* Demos */
    $('.anps-cp-demos').on('click', function() {
        if( typeof ga !== 'undefined' ) {
            ga('send', 'event', 'Transport Color Picker', 'Demos change', $(this).find('img').attr('alt'));
        }
    });

    /*-----------------------------------------------------------------------------------*/
    /*  Specific styles for specific demos
    /*-----------------------------------------------------------------------------------*/
    function loadSpecificStyles(id, schemes) {
        var mainColor = '#' + schemes[id][1];
        $('footer.site-footer .widget_anpstext > span.fa').css('color', mainColor);
        $('.large-above-menu-style-2 .widget_anpstext .fa, .large-above-menu-style-1 .widget_anpstext .fa, .large-above-menu-style-2 .widget_anpstext .fa').css('color', mainColor);
        $('.above-nav-bar .widget_anpstext .fa').css('color', mainColor);
        $('.site-footer .row .menu .current_page_item > a').css('color', mainColor);
        $('.site-logo img.logo-sticky').css('height', '30px');
        $('.site-search').css('background', '#292929');


        if (currentDemo == 'transport-new-demos/1') {
           if (id == 'style-1') {
            $('.site-footer').css('color', '#9bb3c7');
            $('.site-footer .row .menu .current_page_item > a').css('color', '#fff');
            } else {
                 $('.site-footer').css('color', '');
            }
        } else if (currentDemo == 'transport-new-demos/2') {
            if (id == 'style-1') {
                $('footer.site-footer .widget_anpstext > span.fa').css('color', '#c4c4c4');
            }
        } else if (currentDemo == 'transport-new-demos/3') {
            if (id == 'style-1') {
                $('.home .site-header .menu-item-depth-0.current-menu-item > a, .site-navigation .current-menu-item > a').css('color', '#1874c1');
            } else {
                $('.home .site-header .menu-item-depth-0.current-menu-item > a, .site-navigation .current-menu-item > a').css('color', '');
            }
         } else if (currentDemo == 'transport-new-demos/5') {
            if (id == 'style-1') {
                $('.site-footer').css('color', '#a3a3a3');
            } else {
                $('.site-footer').css('color', '');
            }
         }

    }
});
