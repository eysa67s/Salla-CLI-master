<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>{{ store.name }}</title>
  <style>
    body { font-family: Arial, sans-serif; direction: rtl; text-align: center; }
    h1 { color: #4CAF50; }
    .product { border: 1px solid #ddd; padding: 10px; margin: 10px; display: inline-block; width: 200px; }
  </style>
</head>
<body>
  <h1>{{ store.name }}</h1>
  <p>{{ store.description }}</p>

  <h2>منتجاتنا</h2>
  {% for product in products %}
    <div class="product">
      <img src="{{ product.image }}" alt="{{ product.name }}" width="150">
      <h3>{{ product.name }}</h3>
      <p>{{ product.price }} {{ store.currency }}</p>
    </div>
  {% endfor %}
</body>
</html>
