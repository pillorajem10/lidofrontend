<template>
    <footer class="footer">
      <div class="footer-content">
        <div class="footer-copyright">
          &copy; 2024 Lido Panciteria. All rights reserved.
        </div>
      </div>
    </footer>
  </template>

<script>
export default {
  name: 'Footer'
}
</script>

  <style scoped>
  .footer {
    text-align: center;
    color: #002030;
    background: #ffbb00;
    bottom: 0;
    font-weight: bold;
    margin-top: auto;
    padding: 1rem;
  }

  @media (max-width: 700px) {
    .footer {
      font-size: 10px;
    }
  }
  </style>
