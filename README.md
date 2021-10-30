<!DOCTYPE html>
<html>
    <head>
        <title>LPTestbrand</title>
        <!-- BEGIN LivePerson Monitor. -->
        <script type="text/javascript">
            window.lpTag = window.lpTag || {},
            'undefined' == typeof window.lpTag._tagCount ? (window.lpTag = {
                wl: lpTag.wl || null,
                scp: lpTag.scp || null,
                site: '4867873' || '',
                section: lpTag.section || '',
                tagletSection: lpTag.tagletSection || null,
                autoStart: lpTag.autoStart !== !1,
                ovr: lpTag.ovr || {},
                _v: '1.10.0',
                _tagCount: 1,
                protocol: 'https:',
                events: {
                    bind: function(t, e, i) {
                        lpTag.defer(function() {
                            lpTag.events.bind(t, e, i)
                        }, 0)
                    },
                    trigger: function(t, e, i) {
                        lpTag.defer(function() {
                            lpTag.events.trigger(t, e, i)
                        }, 1)
                    }
                },
                defer: function(t, e) {
                    0 === e ? (this._defB = this._defB || [],
                    this._defB.push(t)) : 1 === e ? (this._defT = this._defT || [],
                    this._defT.push(t)) : (this._defL = this._defL || [],
                    this._defL.push(t))
                },
                load: function(t, e, i) {
                    var n = this;
                    setTimeout(function() {
                        n._load(t, e, i)
                    }, 0)
                },
                _load: function(t, e, i) {
                    var n = t;
                    t || (n = this.protocol + '//' + (this.ovr && this.ovr.domain ? this.ovr.domain : 'lptag.liveperson.net') + '/tag/tag.js?site=' + this.site);
                    var o = document.createElement('script');
                    o.setAttribute('charset', e ? e : 'UTF-8'),
                    i && o.setAttribute('id', i),
                    o.setAttribute('src', n),
                    document.getElementsByTagName('head').item(0).appendChild(o)
                },
                init: function() {
                    this._timing = this._timing || {},
                    this._timing.start = (new Date).getTime();
                    var t = this;
                    window.attachEvent ? window.attachEvent('onload', function() {
                        t._domReady('domReady')
                    }) : (window.addEventListener('DOMContentLoaded', function() {
                        t._domReady('contReady')
                    }, !1),
                    window.addEventListener('load', function() {
                        t._domReady('domReady')
                    }, !1)),
                    'undefined' === typeof window._lptStop && this.load()
                },
                start: function() {
                    this.autoStart = !0
                },
                _domReady: function(t) {
                    this.isDom || (this.isDom = !0,
                    this.events.trigger('LPT', 'DOM_READY', {
                        t: t
                    })),
                    this._timing[t] = (new Date).getTime()
                },
                vars: lpTag.vars || [],
                dbs: lpTag.dbs || [],
                ctn: lpTag.ctn || [],
                sdes: lpTag.sdes || [],
                hooks: lpTag.hooks || [],
                identities: lpTag.identities || [],
                ev: lpTag.ev || []
            },
            lpTag.init()) : window.lpTag._tagCount += 1;
        </script>
        <!-- END LivePerson Monitor. -->
        <link rel="stylesheet" href="/stylesheets/style.css">
    </head>
    <body>
        <h1>LPTestbrand</h1>
        <p>Welcome to LPTestbrand</p>
        <script>
            var f1 = function() {
                document.getElementById('myImage').src = 'https://images.unsplash.com/photo-1563422156298-c778a278f9a5';
                document.getElementById('myData').value = '1000';
                lpTag.sdes = lpTag.sdes || [];
                lpTag.sdes.push({
                    "type": "prodView",
                    //MANDATORY
                    "products": [{
                        //ARRAY OF PRODUCTS
                        "product": {
                            "name": "Product1",
                            //PRODUCT NAME
                            "category": "Prod_Category",
                            //PRODUCT CATEGORY NAME
                            "sku": "10305020",
                            //PRODUCT SKU OR UNIQUE IDENTIFIER
                            "price": document.getElementById('myData').value //PRODUCT PRICE
                        }
                    }]
                });
            }
        </script>
        <script>
            var f2 = function() {
                document.getElementById('myImage').src = 'https://images.unsplash.com/photo-1620173834206-c029bf322dba';
                document.getElementById('myData').value = '2000';
            }
        </script>
        <script>
            var f3 = function() {
                document.getElementById('myImage').src = 'https://images.unsplash.com/photo-1602491673980-73aa38de027a'
                document.getElementById('myData').value = '3000';
            }
        </script>
        <script>
            //var lpTag = {};
            //lpTag.identities = [];
            lpTag.identities.push(identityFn)
            function identityFn(callback) {
                console.log('Identity has been called');
                callback({
                    iss: "lp_brand",
                    acr: "loa1",
                    sub: "+972-3-5555-555"
                });
            }
        </script>
        <script>
            function lp_brand_auth_func(callback) {
                console.log('Authenticate has been called');
                const jwt = 'eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIrOTcyLTMtNTU1NS01NTUiLCJpc3MiOiJodHRwczovL2lkcC5saXZlcGVyc29uLm5ldCIsImF1ZCI6ImFjYzpxYTU3MjIxNjc2IiwiZXhwIjoxOTM0OTcxOTMwLCJpYXQiOjE1MjE2MDU1OTIsIm5hbWUiOiJFaXRhbiJ9.0g9ZMvdNelMc2BICMEep90gnnv9InORIhVb2XcD7DCQRInmyPRzBBGbXxJQeTqymbopGio4f9CE2zPvY0fgBVnWntsr3i_dng3nqYuNym5Sc-pU5EHqMuwmVI3sdRsTvBqe1T44qu3FXRkt-BhnzKXELtueGaBUNQz8k_30R1ms';
                callback(jwt);
            }
        </script>
        <button onclick="f1()">One!</button>
        <button onclick="f2()">Two!</button>
        <button onclick="f3()">Three!</button>
        <p></p>
        <a>
            <img id="myImage" height="50" width="100" src="">
        </a>
        <p>
            <strong>Value taken:</strong>
            ;  
        </p>
        <textarea id="myData" cols="5" rows="2"></textarea>
    </body>
</html>
