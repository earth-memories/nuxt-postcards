<template>
  <div>
    <nuxt />
  </div>
</template>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  padding: 2em;
  background: #333;
  color: #ddd;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 45px;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 20px;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.actions {
  padding-top: 15px;
}

.button {
  display: inline-block;
  border-radius: 2px;
  background: #444;
  color: #eee;
  text-decoration: none;
  padding: 10px 30px;
  box-shadow: 0 0 1rem black;
  border: none;
  transition: background 250ms, box-shadow 250ms;
}

.button:hover {
  background: #555;
  box-shadow: 0 0 3rem black;
}
</style>
