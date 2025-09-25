<script setup lang="ts">
import UiParentCard from '@/components/shared/UiParentCard.vue';
import { ref } from 'vue';

const heroData = ref({
    title: 'Welcome to Our Platform',
    subtitle: 'Experience the power of modern web applications',
    description: 'Build faster, scale better, and create amazing user experiences with our comprehensive suite of tools and components.',
});

const features = ref([
    {
        title: 'Modern Design',
        description: 'Beautiful, responsive design that works on all devices',
        icon: 'mdi-palette',
        color: 'primary'
    },
    {
        title: 'High Performance',
        description: 'Optimized for speed and performance with modern technologies',
        icon: 'mdi-rocket-launch',
        color: 'success'
    },
    {
        title: 'Easy Integration',
        description: 'Simple integration with existing systems and workflows',
        icon: 'mdi-puzzle',
        color: 'warning'
    },
    {
        title: '24/7 Support',
        description: 'Round-the-clock support from our dedicated team',
        icon: 'mdi-headset',
        color: 'info'
    }
]);

const stats = ref([
    { label: 'Active Users', value: '10K+', icon: 'mdi-account-group' },
    { label: 'Projects Completed', value: '500+', icon: 'mdi-check-circle' },
    { label: 'Countries Served', value: '50+', icon: 'mdi-earth' },
    { label: 'Customer Satisfaction', value: '98%', icon: 'mdi-heart' }
]);
</script>

<template>
    <div>
        <!-- Hero Section -->
        <v-row class="mb-8">
            <v-col cols="12">
                <UiParentCard>
                    <div class="text-center pa-8">
                        <h1 class="text-h2 mb-4 text-primary">{{ heroData.title }}</h1>
                        <h2 class="text-h4 mb-6 text-subtitle-1">{{ heroData.subtitle }}</h2>
                        <p class="text-body-1 mb-8 mx-auto" style="max-width: 600px;">
                            {{ heroData.description }}
                        </p>
                        <v-btn color="primary" size="large" class="me-4">
                            Get Started
                        </v-btn>
                        <v-btn variant="outlined" size="large">
                            Learn More
                        </v-btn>
                    </div>
                </UiParentCard>
            </v-col>
        </v-row>

        <!-- Features Section -->
        <v-row class="mb-8">
            <v-col cols="12">
                <h2 class="text-h3 text-center mb-8">Why Choose Us?</h2>
            </v-col>
            <v-col cols="12" sm="6" md="3" v-for="feature in features" :key="feature.title">
                <UiParentCard>
                    <div class="text-center pa-6">
                        <v-icon :color="feature.color" size="48" class="mb-4">
                            {{ feature.icon }}
                        </v-icon>
                        <h3 class="text-h5 mb-3">{{ feature.title }}</h3>
                        <p class="text-body-2">{{ feature.description }}</p>
                    </div>
                </UiParentCard>
            </v-col>
        </v-row>

        <!-- Stats Section -->
        <v-row class="mb-8">
            <v-col cols="12">
                <UiParentCard title="Our Impact">
                    <v-row class="pa-4">
                        <v-col cols="12" sm="6" md="3" v-for="stat in stats" :key="stat.label">
                            <div class="text-center">
                                <v-icon size="40" color="primary" class="mb-2">
                                    {{ stat.icon }}
                                </v-icon>
                                <h3 class="text-h4 text-primary mb-1">{{ stat.value }}</h3>
                                <p class="text-body-2">{{ stat.label }}</p>
                            </div>
                        </v-col>
                    </v-row>
                </UiParentCard>
            </v-col>
        </v-row>

        <!-- CTA Section -->
        <v-row>
            <v-col cols="12">
                <UiParentCard>
                    <div class="text-center pa-8">
                        <h2 class="text-h3 mb-4">Ready to Get Started?</h2>
                        <p class="text-body-1 mb-6 mx-auto" style="max-width: 500px;">
                            Join thousands of satisfied customers who trust our platform for their business needs.
                        </p>
                        <v-btn color="success" size="large" class="me-4">
                            Start Your Free Trial
                        </v-btn>
                        <v-btn variant="outlined" color="success" size="large">
                            Contact Sales
                        </v-btn>
                    </div>
                </UiParentCard>
            </v-col>
        </v-row>
    </div>
</template>

<style scoped>
.text-center {
    text-align: center;
}
</style>