SELECT 
    ship_state,
    SUM(AMOUNT) FILTER (WHERE category = 'Set') AS set_orders,
    SUM(AMOUNT) FILTER (WHERE category = 'kurta') AS kurta_orders,
    SUM(AMOUNT) FILTER (WHERE category = 'Western Dress') AS western_dress_orders,
    SUM(AMOUNT) FILTER (WHERE category = 'Top') AS top_orders,
    SUM(AMOUNT) FILTER (WHERE category = 'Ethnic Dress') AS ethnic_dress_orders,
    SUM(AMOUNT) FILTER (WHERE category = 'Blouse') AS blouse_orders,
    SUM(AMOUNT) FILTER (WHERE category = 'Bottom') AS bottom_orders,
    SUM(AMOUNT) FILTER (WHERE category = 'Saree') AS saree_orders,
    SUM(AMOUNT) FILTER (WHERE category = 'Dupatta') AS dupatta_orders,
    SUM(AMOUNT) AS total_city_orders_revenue
FROM amazon_sales
WHERE status = 'Shipped'
GROUP BY ship_state
ORDER BY total_city_orders_revenue DESC;