<template>
    <section style="overflow-x: auto; width: 100%; scrollbar-width: none">
        <table style="width: 100%;">
            <tr>
                <td>Source</td>
                <td>
                    <ui-address v-if="source" v-bind:address="source"/>
                    <span v-else>empty</span>
                </td>
            </tr>
            <tr>
                <td>Destination</td>
                <td>
                    <ui-address v-if="destination" v-bind:address="destination"/>
                    <span v-else>empty</span>
                </td>
            </tr>
            <tr>
                <td>Value</td>
                <td>{{$ton(value, false)}} TON</td>
            </tr>
            <tr>
                <td>Forward fee</td>
                <td>{{$fee(fwd_fee)}} TON</td>
            </tr>
            <tr>
                <td>IHR fee</td>
                <td>{{$fee(ihr_fee)}} TON</td>
            </tr>
            <tr>
                <td>Creation LT</td>
                <td>{{created_lt}}</td>
            </tr>
            <tr>
                <td>Body hash</td>
                <td>{{body_hash}}</td>
            </tr>
            <tr>
                <td>Message</td>
                <td>{{message || 'empty'}}</td>
            </tr>
        </table>
    </section>
</template>

<script>
export default {
    props: {
        source: String,
        destination: String,
        value: String,
        fwd_fee: String,
        ihr_fee: String,
        created_lt: String,
        body_hash: String,
        message: String,
    },
};
</script>
