- dashboard: inventory_management_dashboard__deepto_moitra_
  title: 'Inventory Management Dashboard - Deepto Moitra '
  layout: newspaper
  preferred_viewer: dashboards-next
  elements:
  - title: Warehouse Locations
    name: Warehouse Locations
    model: e_commerce
    explore: distribution_centers
    type: looker_map
    fields: [distribution_centers.location, distribution_centers.latitude, distribution_centers.longitude]
    sorts: [distribution_centers.location]
    limit: 500
    column_limit: 50
    map_plot_mode: points
    heatmap_gridlines: false
    heatmap_gridlines_empty: false
    heatmap_opacity: 0.5
    show_region_field: true
    draw_map_labels_above_data: true
    map_tile_provider: light
    map_position: custom
    map_scale_indicator: 'off'
    map_pannable: true
    map_zoomable: true
    map_marker_type: circle
    map_marker_icon_name: default
    map_marker_radius_mode: proportional_value
    map_marker_units: meters
    map_marker_proportional_scale_type: linear
    map_marker_color_mode: fixed
    show_view_names: false
    show_legend: true
    quantize_map_value_colors: false
    reverse_map_value_colors: false
    series_types: {}
    defaults_version: 1
    map_latitude: 36.03133177633189
    map_longitude: -96.04248046875001
    map_zoom: 4
    listen: {}
    row: 0
    col: 0
    width: 8
    height: 6
  - title: Orders Shipped By Product Category - Past Quarter
    name: Orders Shipped By Product Category - Past Quarter
    model: e_commerce_advanced
    explore: order_items_warehouse
    type: looker_column
    fields: [products.category, order_items.count, order_items.shipped_quarter]
    filters:
      order_items.shipped_quarter: 1 quarters
    sorts: [order_items.count desc]
    limit: 500
    column_limit: 50
    x_axis_gridlines: false
    y_axis_gridlines: true
    show_view_names: false
    show_y_axis_labels: true
    show_y_axis_ticks: true
    y_axis_tick_density: default
    y_axis_tick_density_custom: 5
    show_x_axis_label: true
    show_x_axis_ticks: true
    y_axis_scale_mode: linear
    x_axis_reversed: false
    y_axis_reversed: false
    plot_size_by_field: false
    trellis: ''
    stacking: ''
    limit_displayed_rows: false
    legend_position: center
    point_style: none
    show_value_labels: false
    label_density: 25
    x_axis_scale: auto
    y_axis_combined: true
    ordering: none
    show_null_labels: false
    show_totals_labels: false
    show_silhouette: false
    totals_color: "#808080"
    defaults_version: 1
    listen: {}
    row: 6
    col: 0
    width: 8
    height: 6
  - title: Remaining Inventory Per Category  - Tops and Tees Brands
    name: Remaining Inventory Per Category  - Tops and Tees Brands
    model: e_commerce
    explore: products
    type: looker_column
    fields: [products.brand, products.count, products.category]
    filters:
      products.category: Tops & Tees
    sorts: [products.category]
    limit: 500
    column_limit: 50
    x_axis_gridlines: false
    y_axis_gridlines: true
    show_view_names: false
    show_y_axis_labels: true
    show_y_axis_ticks: true
    y_axis_tick_density: default
    y_axis_tick_density_custom: 5
    show_x_axis_label: true
    show_x_axis_ticks: true
    y_axis_scale_mode: linear
    x_axis_reversed: false
    y_axis_reversed: false
    plot_size_by_field: false
    trellis: ''
    stacking: ''
    limit_displayed_rows: false
    legend_position: center
    point_style: none
    show_value_labels: false
    label_density: 25
    x_axis_scale: auto
    y_axis_combined: true
    ordering: none
    show_null_labels: false
    show_totals_labels: false
    show_silhouette: false
    totals_color: "#808080"
    defaults_version: 1
    listen: {}
    row: 6
    col: 8
    width: 8
    height: 6
  - title: Customer Proximity to Warehouses
    name: Customer Proximity to Warehouses
    model: e_commerce_advanced
    explore: order_items_warehouse
    type: looker_map
    fields: [distribution_centers.location, users.city, users.count, users.state]
    filters:
      users.country: USA
    sorts: [distribution_centers.location]
    limit: 500
    column_limit: 50
    map_plot_mode: points
    heatmap_gridlines: false
    heatmap_gridlines_empty: false
    heatmap_opacity: 0.5
    show_region_field: true
    draw_map_labels_above_data: true
    map_tile_provider: light
    map_position: custom
    map_scale_indicator: 'off'
    map_pannable: true
    map_zoomable: true
    map_marker_type: circle
    map_marker_icon_name: default
    map_marker_radius_mode: proportional_value
    map_marker_units: meters
    map_marker_proportional_scale_type: linear
    map_marker_color_mode: fixed
    show_view_names: false
    show_legend: true
    quantize_map_value_colors: false
    reverse_map_value_colors: false
    show_row_numbers: true
    transpose: false
    truncate_text: true
    hide_totals: false
    hide_row_totals: false
    size_to_fit: true
    table_theme: white
    limit_displayed_rows: false
    enable_conditional_formatting: false
    header_text_alignment: left
    header_font_size: 12
    rows_font_size: 12
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    defaults_version: 1
    series_types: {}
    map_latitude: 29.759757809109562
    map_longitude: -95.36424636840822
    map_zoom: 12
    x_axis_gridlines: false
    y_axis_gridlines: true
    show_y_axis_labels: true
    show_y_axis_ticks: true
    y_axis_tick_density: default
    y_axis_tick_density_custom: 5
    show_x_axis_label: true
    show_x_axis_ticks: true
    y_axis_scale_mode: linear
    x_axis_reversed: false
    y_axis_reversed: false
    plot_size_by_field: false
    trellis: ''
    stacking: ''
    legend_position: center
    point_style: none
    show_value_labels: false
    label_density: 25
    x_axis_scale: auto
    y_axis_combined: true
    show_null_points: true
    interpolation: linear
    show_totals_labels: false
    show_silhouette: false
    totals_color: "#808080"
    ordering: none
    show_null_labels: false
    listen: {}
    row: 0
    col: 8
    width: 8
    height: 6
  - title: Order Delivery Duration By State - Past Quarter
    name: Order Delivery Duration By State - Past Quarter
    model: getting_started_with_lookml
    explore: order_items
    type: looker_map
    fields: [order_items.days_fulfillment, users.state, order_items.count]
    filters:
      order_items.shipped_quarter: 1 quarters
    sorts: [order_items.days_fulfillment desc]
    limit: 5000
    column_limit: 50
    map_plot_mode: points
    heatmap_gridlines: false
    heatmap_gridlines_empty: false
    heatmap_opacity: 0.5
    show_region_field: true
    draw_map_labels_above_data: true
    map_tile_provider: light
    map_position: custom
    map_scale_indicator: 'off'
    map_pannable: true
    map_zoomable: true
    map_marker_type: circle
    map_marker_icon_name: default
    map_marker_radius_mode: proportional_value
    map_marker_units: meters
    map_marker_proportional_scale_type: linear
    map_marker_color_mode: fixed
    show_view_names: false
    show_legend: true
    quantize_map_value_colors: false
    reverse_map_value_colors: false
    defaults_version: 1
    map_latitude: 42.94033923363183
    map_longitude: -61.61132812500001
    map_zoom: 3
    series_types: {}
    x_axis_gridlines: false
    y_axis_gridlines: true
    show_y_axis_labels: true
    show_y_axis_ticks: true
    y_axis_tick_density: default
    y_axis_tick_density_custom: 5
    show_x_axis_label: true
    show_x_axis_ticks: true
    y_axis_scale_mode: linear
    x_axis_reversed: false
    y_axis_reversed: false
    plot_size_by_field: false
    trellis: ''
    stacking: ''
    limit_displayed_rows: false
    legend_position: center
    point_style: none
    show_value_labels: false
    label_density: 25
    x_axis_scale: auto
    y_axis_combined: true
    ordering: none
    show_null_labels: false
    show_totals_labels: false
    show_silhouette: false
    totals_color: "#808080"
    show_row_numbers: true
    transpose: false
    truncate_text: true
    hide_totals: false
    hide_row_totals: false
    size_to_fit: true
    table_theme: white
    enable_conditional_formatting: false
    header_text_alignment: left
    header_font_size: 12
    rows_font_size: 12
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    row: 12
    col: 8
    width: 8
    height: 6
  - title: Inventory Sold by Gender & Ad Channel - Past Quarter
    name: Inventory Sold by Gender & Ad Channel - Past Quarter
    model: getting_started_with_lookml
    explore: order_items
    type: looker_waterfall
    fields: [users.gender, order_items.count, users.traffic_source]
    filters:
      inventory_items.sold_quarter: 1 quarters
    sorts: [order_items.count desc]
    limit: 500
    column_limit: 50
    up_color: "#EA8A2F"
    down_color: "#8D7FB9"
    total_color: "#EA8A2F"
    show_value_labels: true
    show_x_axis_ticks: true
    show_x_axis_label: true
    x_axis_scale: auto
    show_y_axis_labels: true
    show_y_axis_ticks: true
    y_axis_gridlines: true
    color_application:
      collection_id: 2357cb1d-483e-418d-bd5a-4b47327aba12
      palette_id: 6bf9285b-02f0-4eb5-a3a7-4ba3a4cbf7a9
      options:
        steps: 5
    label_color: [black]
    leftAxisLabelVisible: true
    leftAxisLabel: ''
    rightAxisLabelVisible: true
    rightAxisLabel: ''
    smoothedBars: false
    orientation: automatic
    labelPosition: left
    percentType: total
    percentPosition: inline
    valuePosition: right
    labelColorEnabled: false
    labelColor: "#FFF"
    x_axis_gridlines: false
    show_view_names: false
    y_axis_tick_density: default
    y_axis_tick_density_custom: 5
    y_axis_scale_mode: linear
    x_axis_reversed: false
    y_axis_reversed: false
    plot_size_by_field: false
    trellis: ''
    stacking: ''
    limit_displayed_rows: false
    legend_position: center
    point_style: none
    label_density: 25
    y_axis_combined: true
    ordering: none
    show_null_labels: false
    show_totals_labels: false
    show_silhouette: false
    totals_color: "#808080"
    defaults_version: 1
    series_types: {}
    show_null_points: true
    value_labels: legend
    label_type: labPer
    interpolation: linear
    show_row_numbers: true
    truncate_column_names: false
    hide_totals: false
    hide_row_totals: false
    table_theme: editable
    enable_conditional_formatting: false
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    row: 0
    col: 16
    width: 8
    height: 6
  - title: Cost of Inventory - Past Quarter
    name: Cost of Inventory - Past Quarter
    model: getting_started_with_lookml
    explore: order_items
    type: single_value
    fields: [inventory_items.sold_quarter, inventory_items.total_cost]
    fill_fields: [inventory_items.sold_quarter]
    filters:
      inventory_items.sold_quarter: 1 quarters
    sorts: [inventory_items.sold_quarter desc]
    limit: 500
    column_limit: 50
    custom_color_enabled: true
    show_single_value_title: true
    show_comparison: false
    comparison_type: value
    comparison_reverse_colors: false
    show_comparison_label: true
    enable_conditional_formatting: false
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    custom_color: "#64518A"
    single_value_title: ''
    series_types: {}
    defaults_version: 1
    row: 12
    col: 0
    width: 8
    height: 6
  - title: Returned Shipments - Past Quarter
    name: Returned Shipments - Past Quarter
    model: getting_started_with_lookml
    explore: order_items
    type: looker_grid
    fields: [order_items.count, products.category, products.department, products.brand,
      users.city, users.state]
    filters:
      order_items.status: Returned
      order_items.created_quarter: 1 quarters
      users.country: USA
    sorts: [order_items.count desc]
    limit: 5000
    show_view_names: false
    show_row_numbers: true
    transpose: false
    truncate_text: true
    hide_totals: false
    hide_row_totals: false
    size_to_fit: true
    table_theme: white
    limit_displayed_rows: false
    enable_conditional_formatting: false
    header_text_alignment: left
    header_font_size: '12'
    rows_font_size: '12'
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    color_application:
      collection_id: 7c56cc21-66e4-41c9-81ce-a60e1c3967b2
      palette_id: 5d189dfc-4f46-46f3-822b-bfb0b61777b1
    show_sql_query_menu_options: false
    show_totals: true
    show_row_totals: true
    series_cell_visualizations:
      order_items.count:
        is_active: true
        palette:
          palette_id: d4591e85-64e5-d4c5-09f0-eb722c780282
          collection_id: 7c56cc21-66e4-41c9-81ce-a60e1c3967b2
          custom_colors:
          - "#a2b9e6"
          - "#6337e8"
    series_types: {}
    custom_color_enabled: true
    show_single_value_title: true
    show_comparison: false
    comparison_type: value
    comparison_reverse_colors: false
    show_comparison_label: true
    defaults_version: 1
    row: 12
    col: 16
    width: 8
    height: 6
  - title: Purchase Volume by Customer Age Group - Past Quarter
    name: Purchase Volume by Customer Age Group - Past Quarter
    model: getting_started_with_lookml
    explore: order_items
    type: looker_funnel
    fields: [orders.count, users.age_tier]
    fill_fields: [users.age_tier]
    filters:
      users.country: USA
      inventory_items.sold_quarter: 1 quarters
    sorts: [orders.count desc]
    limit: 500
    leftAxisLabelVisible: true
    leftAxisLabel: ''
    rightAxisLabelVisible: false
    rightAxisLabel: ''
    smoothedBars: false
    orientation: automatic
    labelPosition: left
    percentType: total
    percentPosition: inline
    valuePosition: right
    labelColorEnabled: false
    labelColor: "#FFF"
    color_application:
      collection_id: 2357cb1d-483e-418d-bd5a-4b47327aba12
      palette_id: 6bf9285b-02f0-4eb5-a3a7-4ba3a4cbf7a9
      options:
        steps: 5
    series_types: {}
    defaults_version: 1
    row: 6
    col: 16
    width: 8
    height: 6
