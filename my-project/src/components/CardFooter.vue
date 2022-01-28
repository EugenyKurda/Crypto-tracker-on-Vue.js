<template>
    <div>
        <div class="card__footer">
            <div class="card__footer-info">
                <p class="daily_price">24h: <span>{{bitcoinInfo.DISPLAY.USD.CHANGEPCT24HOUR + '%'}}</span></p>
                <p class="weekly-price">1d: <span> {{bitcoinInfo.DISPLAY.USD.CHANGEPCTDAY + '%'}}</span></p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'card-footer',
    props: {
        bitcoinInfo: {
            type: Object
        }
    }
}
</script>