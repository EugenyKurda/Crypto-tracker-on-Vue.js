<template>
    <div >
        <div class="card__header">
            <div class="card__header-info">
                <img class="header__info-img" :src="`http://cryptocompare.com${bitcoinInfo.CoinInfo.ImageUrl}`"  alt="BTC">
                <p class="bitcoin-name">{{ bitcoinInfo.CoinInfo.Name }}<span> | </span>{{ bitcoinInfo.CoinInfo.FullName }}</p>
            </div>
            <div class="card__header-price">
                <span class="price">{{bitcoinInfo.DISPLAY.USD.PRICE}}</span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'card-header',
    props: {
        bitcoinInfo: {
            type: Object
        }
    } 
}
</script>