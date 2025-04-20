<!DOCTYPE html>
<html lang="zh-Hant">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>隨機飲料店抽選器</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin-top: 100px;
    }
    button {
      font-size: 24px;
      padding: 10px 20px;
      cursor: pointer;
      background-color: #4CAF50;
      color: white;
      border: none;
      border-radius: 10px;
    }
    button:hover {
      background-color: #45a049;
    }
    #result {
      margin-top: 50px;
      font-size: 32px;
      color: #333;
    }
  </style>
</head>
<body>
  <h1>今天喝哪一家？</h1>
  <button onclick="pickRandomStore()">抽一家飲料店！</button>
  <div id="result"></div>

  <script>
    const stores = ["永貞新村", "鮮茶道", "波比", "大師茶", "叮哥", "沐嵐"];

    function pickRandomStore() {
      const randomIndex = Math.floor(Math.random() * stores.length);
      const selectedStore = stores[randomIndex];
      document.getElementById("result").textContent = 你今天可以喝：${selectedStore};
    }
  </script>
</body>
</html>

