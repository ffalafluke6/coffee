<template>
  <div id="app">
    <b-navbar type="dark" variant="dark">
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <h5>
            <router-link to="/">Home</router-link>|
            <router-link to="/about">About</router-link>|
          </h5>
        </b-navbar-nav>

        <b-navbar-nav class="ml-auto">
          <b-nav-form>
            <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
            <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
          </b-nav-form>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
    <br />

    <h2>Please select a product</h2>

    <main class="container">
      <div class="pricing-header px-3 py-3 pt-md-5 pb-md-4 mx-auto text-center">
        <div class="row row-cols-1 row-cols-md-3 mb-3 text-center">
          <div class="col">
            <div class="card mb-4 shadow-sm">
              <div class="card-header">
                <h4 class="my-0 fw-normal">{{ data1.name }}</h4>
              </div>
              <div class="card-body">
                <img src="https://cdn.sogoodweb.com/Preview/106/images/te0106-004.png" />
                <ul class="list-unstyled text-small">
                  1325 THB
                </ul>
                <div id="example-1">
                  <b-button variant="outline-warning" v-on:click="data1.amount += 1"
                    >Add to basket</b-button
                  >&nbsp;
                  <b-button variant="outline-danger" v-on:click="data1.amount -= 1"
                    >Take out basket</b-button
                  >
                  <p>จำนวน {{ data1.amount }} ถุง</p>
                </div>
              </div>
            </div>
          </div>
          <div class="col">
            <div class="card mb-4 shadow-sm">
              <div class="card-header">
                <h4 class="my-0 fw-normal">{{ product2.name }}</h4>
              </div>
              <div class="card-body">
                <img src="https://cdn.sogoodweb.com/Preview/106/images/te0106-005.png" />
                <ul class="list-unstyled text-small">
                  2479 THB
                </ul>
                <div id="example-2">
                  <b-button variant="outline-warning" v-on:click="product2.amount += 1"
                    >Add to basket</b-button
                  >&nbsp;
                  <b-button variant="outline-danger" v-on:click="product2.amount -= 1"
                    >Take out basket</b-button
                  >
                  <p>จำนวน {{ product2.amount }} ถุง</p>
                </div>
              </div>
            </div>
          </div>
          <div class="col">
            <div class="card mb-4 shadow-sm">
              <div class="card-header">
                <h4 class="my-0 fw-normal">{{ product3.name }}</h4>
              </div>
              <div class="card-body">
                <img src="https://cdn.sogoodweb.com/Preview/106/images/te0106-006.png" />
                <ul class="list-unstyled text-small">
                  1067 THB
                </ul>
                <div id="example-3">
                  <b-button variant="outline-warning" v-on:click="product3.amount += 1"
                    >Add to basket</b-button
                  >&nbsp;
                  <b-button variant="outline-danger" v-on:click="product3.amount -= 1"
                    >Take out basket</b-button
                  >
                  <p>จำนวน {{ product3.amount }} ถุง</p>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="row row-cols-1 row-cols-md-3 mb-3 text-center">
          <div class="col">
            <div class="card mb-4 shadow-sm">
              <div class="card-header">
                <h4 class="my-0 fw-normal">{{ product4.name }}</h4>
              </div>
              <div class="card-body">
                <img src="https://cdn.sogoodweb.com/Preview/106/images/te0106-007.png" />
                <ul class="list-unstyled text-small">
                  1359 THB
                </ul>
                <div id="example-4">
                  <b-button variant="outline-warning" v-on:click="product4.amount += 1"
                    >Add to basket</b-button
                  >&nbsp;
                  <b-button variant="outline-danger" v-on:click="product4.amount -= 1"
                    >Take out basket</b-button
                  >
                  <p>จำนวน {{ product4.amount }} ถุง</p>
                </div>
              </div>
            </div>
          </div>
          <div class="col">
            <div class="card mb-4 shadow-sm">
              <div class="card-header">
                <h4 class="my-0 fw-normal">{{ product5.name }}</h4>
              </div>
              <div class="card-body">
                <img src="https://cdn.sogoodweb.com/Preview/106/images/te0106-008.png" />
                <ul class="list-unstyled text-small">
                  950 THB
                </ul>
                <div id="example-5">
                  <b-button variant="outline-warning" v-on:click="product5.amount += 1"
                    >Add to basket</b-button
                  >&nbsp;
                  <b-button variant="outline-danger" v-on:click="product5.amount -= 1"
                    >Take out basket</b-button
                  >
                  <p>จำนวน {{ product5.amount }} ถุง</p>
                </div>
              </div>
            </div>
          </div>
          <div class="col">
            <div class="card mb-4 shadow-sm">
              <div class="card-header">
                <h4 class="my-0 fw-normal">{{ product6.name }}</h4>
              </div>
              <div class="card-body">
                <img src="https://cdn.sogoodweb.com/Preview/106/images/te0106-009.png" />
                <ul class="list-unstyled text-small">
                  1699 THB
                </ul>
                <div id="example-6">
                  <b-button variant="outline-warning" v-on:click="product6.amount += 1"
                    >Add to basket</b-button
                  >&nbsp;
                  <b-button variant="outline-danger" v-on:click="product6.amount -= 1"
                    >Take out basket</b-button
                  >
                  <p>จำนวน {{ product6.amount }} ถุง</p>
                </div>
              </div>
            </div>
          </div>
        </div>

        <h4>
          All prices
          {{
            sum +
            data1.amount * data1.price +
            product2.amount * product2.price +
            product3.amount * product3.price +
            product4.amount * product4.price +
            product5.amount * product5.price +
            product6.amount * product6.price
          }}
          THB
        </h4>
        <button
          type="button"
          class="w-50 btn btn-lg btn-outline-primary"
          v-on:click="say('Order finished')"
          style="max-width: 25rem"
        >
          Confirm purchase
        </button>
        <br />
        <br />
        <b-button
          variant="danger"
          onclick="javascript:location.reload();"
          style="max-width: 25rem"
          >Cancel all products</b-button
        >
      </div>
    </main>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      data1: {
        name: "SENSEO COFFEE",
        price: 1325,
        amount: 0,
      },
      product2: {
        name: "STARBUCKS COFFEE",
        price: 2479,
        amount: 0,
      },
      product3: {
        name: "YUBAN COFFEE",
        price: 1067,
        amount: 0,
      },
      product4: {
        name: "MAXWELL COFFEE",
        price: 1359,
        amount: 0,
      },
      product5: {
        name: "STARBUCKS PODS",
        price: 950,
        amount: 0,
      },
      product6: {
        name: "SENSEO COFFEE",
        price: 1699,
        amount: 0,
      },
      sum: 0,
      count: 0,
      say: function (message) {
        alert(message);
      },
    };
  },
};
</script>
