highcharts-with-context-menu
============================

Current highcharts version: 2.3.2

Adds a context menu event to the highcharts object.

e.g.

var newChart = new Highcharts.Chart({
    plotOptions: {
        series: {
            events: {
                legendContextMenu: function(e) {
                    // use e.mousePageX and e.mousePageY for mouse coordinates
                }
            },
            point: {
                events: {
                    contextmenu: function(point) {
                        // use this.mousePageX and this.mousePageY for mouse coordinates
                    }
                }
            }
        }
    }
});

Current the legend context menu event does not fire for IE9+