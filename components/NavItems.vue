<template>
    <v-list>
        <v-list-item to="/" title="Home" prepend-icon="mdi-home"></v-list-item>

        <v-list-group in item value="subTitle">
            <template v-slot:activator="{ props }">
                <v-list-item
                    v-bind="props"
                    prepend-icon="mdi-account-circle"
                    title="BNM"
                ></v-list-item>
            </template>
            <v-list-item 
                to="/bnm/otherIndicators/msb51" 
                title="Other Indicators" 
            />

            <v-list-group>
                <template v-slot:activator="{ props }">
                    <v-list-item 
                        title="Rates and Volume" 
                        v-bind="props" 
                    />
                </template>
                <v-list-item 
                    title="Exchange Rates" 
                    to="/bnm/ratesAndVolume/ExchangeRates" 
                />
                <v-list-item 
                    to="/bnm/ratesAndVolume/FinancialConsumerAlert" 
                    title="Financial Consumer Alert" 
                />
            </v-list-group>

            <v-list-group>
                <template v-slot:activator="{ props }">
                    <v-list-item 
                        title="Payment Statistics" 
                        v-bind="props" 
                    />
                </template>
                <v-list-item 
                    to="/bnm/paymentStatistic/BasicPaymentIndicator" 
                    title="Basic Payment Indicator" 
                />
            </v-list-group>

            <v-list-group>
                <template v-slot:activator="{ props }">
                    <v-list-item 
                        title="Other Indicators" 
                        v-bind="props" 
                    />
                </template>
                <v-list-item 
                    to="/bnm/paymentStatistic/BasicPaymentIndicator" 
                    title="Basic Payment Indicator" 
                />
            </v-list-group>
        </v-list-group>
    </v-list>
</template>

<script setup>

</script>