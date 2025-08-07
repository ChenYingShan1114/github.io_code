---
title: "My Travel Log"
date: 2024-06-30
draft: false
description: "The world in my eye"
not_show_date: true
---

# Haven't done yet......

<!-- amCharts core and maps -->
<script src="https://cdn.amcharts.com/lib/5/index.js"></script>
<script src="https://cdn.amcharts.com/lib/5/map.js"></script>
<script src="https://cdn.amcharts.com/lib/5/geodata/worldLow.js"></script>
<script src="https://cdn.amcharts.com/lib/5/themes/Animated.js"></script>

<div id="worldMap" style="width: 100%; height: 500px; margin: 0 auto;"></div>


<script>
am5.ready(function() {
    var root = am5.Root.new("worldMap");
    root.setThemes([am5themes_Animated.new(root)]);

    var chart = root.container.children.push(
        am5map.MapChart.new(root, {
            panX: "none",
            panY: "none",
            wheelX: "none",
            wheelY: "none",
            projection: am5map.geoMercator()
        })
    );

    var polygonSeries = chart.series.push(
        am5map.MapPolygonSeries.new(root, {
            geoJSON: am5geodata_worldLow
        })
    );

    polygonSeries.mapPolygons.template.setAll({
        tooltipText: "{name}",
        interactive: true
    });

    // Emphasize on hover
    polygonSeries.mapPolygons.template.states.create("hover", {
        fill: am5.color(0x677935)
    });

    // On click, redirect to a page (e.g., /country/{id})
    polygonSeries.mapPolygons.template.events.on("click", function(ev) {
        var countryId = ev.target.dataItem.dataContext.id;
        // Example: redirect to /country/US for United States
        window.location.href = "/country/" + countryId;
    });

    // Optional: cursor pointer on hover
    polygonSeries.mapPolygons.template.events.on("pointerover", function(ev) {
        ev.target.set("cursorOverStyle", "pointer");
    });

    chart.appear(1000, 100);
});
</script>