<script setup>
    const bgColor= 'background-color:#F8F9FA'

    const packages = [
        {
            id:1,
            packageName: 'Basic',
            titleTag: 'Individual',
            packagePrice: '$0',
            packageDescription: "Some quick example text to build on the card title and make up the bulk of the card's content.",
            features: [
                        {symbol: '✓', line:"There live the blind texts"},
                        {symbol: '✓', line:"Far far away behind the word"},
                        {symbol: '✓', line:"Far from the countries Vokalia and Consonantia"}
                    ]
        },
        {
            id:2,
            packageName: 'Standard',
            titleTag: 'Small Business',
            packagePrice: '$19.99',
            packageDescription: "Some quick example text to build on the card title and make up the bulk of the card's content.",
            features: [
                        {symbol: '✓', line:"There live the blind texts"},
                        {symbol: '✓', line:"Far far away behind the word"},
                        {symbol: '✓', line:"Far from the countries Vokalia and Consonantia"}
                    ]
        },
        {
            id:3,
            packageName: 'Premium',
            titleTag: 'Large Companies',
            packagePrice: '$79.99',
            packageDescription: "Some quick example text to build on the card title and make up the bulk of the card's content.",
            features: [
                        {symbol: '✓', line:"There live the blind texts"},
                        {symbol: '✓', line:"Far far away behind the word"},
                        {symbol: '✓', line:"Far from the countries Vokalia and Consonantia"}
                    ]
        }
    ]

</script>
<template>
    <div class="container-fluid" :style="bgColor">
        <div class="container p-5">
            <div class="text-center my-5">
                <h1>Pricing</h1>
                <p>Pricing for everyone. Choose your plan now!</p>
            </div>
        <div class="row">
            <div class="col-lg-4 col-md-12 mb-4" v-for="pack in packages" :key="id">
                <div class="card rounded-5 h-100 shadow-lg">
                    <div class="card-body">
                    <div class="text-center p-3">
                        <h5 class="card-title">{{ pack.packageName }}</h5>
                        <small>{{ pack.titleTag }}</small>
                        <br><br>
                        <span class="h2">{{ pack.packagePrice }}</span>/month
                        <br><br>
                    </div>
                    <p class="card-text">{{ pack.packageDescription }}</p>
                    </div>
                    <ul class="list-group list-group-flush">
                        <li class="list-group-item" v-for="feature in pack.features" :key="index">
                            <span class="text-primary">{{ feature.symbol }}</span> {{ feature.line }}
                        </li>
                    </ul>
                    <div class="card-body text-center">
                        <button class="btn btn-outline-primary btn-lg" style="border-radius:30px">Get Started</button>
                    </div>
                </div>
            </div>
            <!-- <div class="col-lg-4 col-md-12 mb-4">
                <div class="card h-100 shadow-lg">
                    <div class="card-body">
                    <div class="text-center p-3">
                        <h5 class="card-title">Standard</h5>
                        <small>Small Business</small>
                        <br><br>
                        <span class="h2">$20</span>/month 
                        <br><br>
                    </div>
                    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                    </div>
                    <ul class="list-group list-group-flush">
                    <li class="list-group-item"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-check" viewBox="0 0 16 16">
                        <path d="M10.97 4.97a.75.75 0 0 1 1.07 1.05l-3.99 4.99a.75.75 0 0 1-1.08.02L4.324 8.384a.75.75 0 1 1 1.06-1.06l2.094 2.093 3.473-4.425a.267.267 0 0 1 .02-.022z"/>
                    </svg> Cras justo odio</li>
                    <li class="list-group-item"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-check" viewBox="0 0 16 16">
                        <path d="M10.97 4.97a.75.75 0 0 1 1.07 1.05l-3.99 4.99a.75.75 0 0 1-1.08.02L4.324 8.384a.75.75 0 1 1 1.06-1.06l2.094 2.093 3.473-4.425a.267.267 0 0 1 .02-.022z"/>
                    </svg> Dapibus ac facilisis in</li>
                    <li class="list-group-item"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-check" viewBox="0 0 16 16">
                        <path d="M10.97 4.97a.75.75 0 0 1 1.07 1.05l-3.99 4.99a.75.75 0 0 1-1.08.02L4.324 8.384a.75.75 0 1 1 1.06-1.06l2.094 2.093 3.473-4.425a.267.267 0 0 1 .02-.022z"/>
                    </svg> Vestibulum at eros</li>
                    </ul>
                    <div class="card-body text-center">
                    <button class="btn btn-outline-primary btn-lg" style="border-radius:30px">Get Started</button>
                    </div>
                </div>
            </div>
            <div class="col-lg-4 col-md-12 mb-4">
                <div class="card h-100 shadow-lg">
                    <div class="card-body">
                    <div class="text-center p-3">
                        <h5 class="card-title">Premium</h5>
                        <small>Large Companies</small>
                        <br><br>
                        <span class="h2">$40</span>/month
                        <br><br>
                    </div>
                    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                    </div>
                    <ul class="list-group list-group-flush">
                    <li class="list-group-item"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-check" viewBox="0 0 16 16">
                        <path d="M10.97 4.97a.75.75 0 0 1 1.07 1.05l-3.99 4.99a.75.75 0 0 1-1.08.02L4.324 8.384a.75.75 0 1 1 1.06-1.06l2.094 2.093 3.473-4.425a.267.267 0 0 1 .02-.022z"/>
                    </svg> Cras justo odio</li>
                    <li class="list-group-item"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-check" viewBox="0 0 16 16">
                        <path d="M10.97 4.97a.75.75 0 0 1 1.07 1.05l-3.99 4.99a.75.75 0 0 1-1.08.02L4.324 8.384a.75.75 0 1 1 1.06-1.06l2.094 2.093 3.473-4.425a.267.267 0 0 1 .02-.022z"/>
                    </svg> Dapibus ac facilisis in</li>
                    <li class="list-group-item"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-check" viewBox="0 0 16 16">
                        <path d="M10.97 4.97a.75.75 0 0 1 1.07 1.05l-3.99 4.99a.75.75 0 0 1-1.08.02L4.324 8.384a.75.75 0 1 1 1.06-1.06l2.094 2.093 3.473-4.425a.267.267 0 0 1 .02-.022z"/>
                    </svg> Vestibulum at eros</li>
                    </ul>
                    <div class="card-body text-center">
                    <button class="btn btn-outline-primary btn-lg" style="border-radius:30px">Get Started</button>
                    </div>
                </div>
            </div> -->
        </div>    
        </div>
    </div>
</template>

<style scoped>
.card {
      border:none;
      padding: 10px 50px;
    }

    .card::after {
      position: absolute;
      z-index: -1;
      opacity: 0;
      -webkit-transition: all 0.6s cubic-bezier(0.165, 0.84, 0.44, 1);
      transition: all 0.6s cubic-bezier(0.165, 0.84, 0.44, 1);
    }

    .card:hover {


      transform: scale(1.02, 1.02);
      -webkit-transform: scale(1.02, 1.02);
      backface-visibility: hidden; 
      will-change: transform;
      box-shadow: 0 1rem 3rem rgba(0,0,0,.75) !important;
    }

    .card:hover::after {
      opacity: 1;
    }

    .card:hover .btn-outline-primary{
      color:white;
      background:#007bff;
    }
</style>