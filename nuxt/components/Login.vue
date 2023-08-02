<template>
    <v-conatiner style="height: 100vh; color: white;">
        <v-row style="height: 100vh;" justify="center" align-content="center">
            <v-col cols="10" class="shrink">
                <v-row dense no-gutters>
                    <v-col cols="12">
                        <h1 style="color: white; text-align: center;">Larp Dangerous</h1>
                    </v-col>
                    <v-col cols="12">
                        <h5 style="color: grey; text-align: center;">An AI powered "Larping" Simulator for story telling
                            enthusiasts made by internet artisans.</h5>
                    </v-col>
                    <v-col>
                        <v-tabs v-model="tab" fixed-tabs>
                            <v-tab value="one">Guest Play</v-tab>
                            <v-tab value="two">Login</v-tab>
                        </v-tabs>
                        <v-window v-model="tab">
                            <v-window-item value="one">
                                <v-container>
                                    <v-row dense no-gutters align-content="start" justify="space-between">
                                        <v-col cols="12">
                                            <v-text-field label="Host Name" />
                                        </v-col>
                                        <v-col cols="12">
                                            <v-text-field label="Game Title" />
                                        </v-col>
                                        <v-col cols="4" class="shrink">
                                            <h4>Private</h4>
                                        </v-col>
                                        <v-col cols="4" class="shrink">
                                            <v-switch :color="private ? 'success' : ''" v-model="private" />
                                        </v-col>
                                        <v-col v-if="private" class="shrink">
                                            <v-text-field label="4 digit code" />
                                        </v-col>
                                        <v-col cols="12">
                                            <v-btn x-large block color="success">create</v-btn>
                                        </v-col>
                                    </v-row>
                                </v-container>
                            </v-window-item>
                            <v-window-item value="two">
                                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis id, non consectetur,
                                    qui nisi nam, eum laboriosam similique ipsum facere esse incidunt debitis cum quia quod
                                    totam? Voluptatum, vero at.</p>
                            </v-window-item>
                        </v-window>
                    </v-col>
                </v-row>
            </v-col>
        </v-row>
    </v-conatiner>
</template>

<script>
export default {
    data: () => ({
        tab: null,
        private: false
    })
}
</script>

<style lang="scss"></style>