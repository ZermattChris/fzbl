<template>
    <v-card>
        <v-divider></v-divider>

        <v-card-actions>
            <v-btn
                :disabled="step === 1"
                text
                @click="step--"
            >
                Back
            </v-btn>
                <v-spacer></v-spacer>
            <v-btn
                :disabled="step === 3"
                color="primary"
                depressed
                @click="step++"
            >
                Next
        </v-btn>
        </v-card-actions>
    </v-card>
</template>

<script>
export default {

}
</script>

<style>

</style>
