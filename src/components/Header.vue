<template>
  <header>
    <nav>
      <ul class="navBar">
        <li>
          <i class="fa fa-phone" aria-hidden="true"></i>
          <a class="info" href="tel:0980202092">098-02-02-092</a>
        </li>
        <li>
          <i class="fa fa-phone" aria-hidden="true"></i>
          <a class="info" href="tel:0730202090">073-02-02-090</a>
        </li>
        <li>
          <i class="fa fa-envelope" aria-hidden="true"></i>
          <a class="info" href="mailto:info@indresser.com">info@indresser.com</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
.navBar {
  display: flex;
  justify-content: space-around;
  min-height: 50px;
  align-items: center;
}
.navBar i {
  margin-right: .5rem;
  font-size: 1.5rem;
  color: #fff;
}
.info {
  color: #fff;
  text-shadow: 1px 1px 1px #333;
  font-size: responsive 1rem 1.4rem;
}

@media (max-width: 540px) {
  .navBar {
    flex-direction: column;
    font-size: 1.1rem;
  }
  .navBar li {
    padding: 0.3rem 0;
  }
}
</style>