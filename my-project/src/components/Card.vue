<template>
    <div>
        <div v-for="bitcoinInfo in bitcoinInfoArray"  :key="bitcoinInfo.CoinInfo.Name"
         class="card__wrapper">
             <card-header 
            :bitcoin-info="bitcoinInfo"
            ></card-header>
            <card-footer :bitcoin-info="bitcoinInfo"></card-footer>
        </div>
    </div>
</template>

<script>
import axios from 'axios'
import CardHeader from './CardHeader.vue'
import CardFooter from './CardFooter.vue'

const INSERT_YOUR_API_KEY_HERE = process.env.npm_config_api_key;

export default {
    name: 'card-block',
    data() {
        return {
            bitcoinInfoArray: [],
        }
    },
    components: {
        CardHeader,
        CardFooter
    },
    mounted() {
    axios
      .get(`https://min-api.cryptocompare.com/data/top/totaltoptiervolfull?limit=10&tsym=USD&api_key=${INSERT_YOUR_API_KEY_HERE}`)
      .then(response => (this.bitcoinInfoArray = response.data.Data, console.log(this.bitcoinInfoArray)));
    }

}
</script>