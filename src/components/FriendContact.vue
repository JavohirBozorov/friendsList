<template>
    <li>
        <h2>{{ friend.name }}</h2>
        <button @click="toggleDetails">Show Details</button>
        <ul v-show="detailsAreVisible">
            <li>
                <strong>Phone:</strong>
                {{ friend.phone }}
            </li>
            <li>
                <strong>Phone:</strong>
                {{ friend.email }}
            </li>
        </ul>
    </li>
</template>

<script>
export default {
    data() {
        return {
            detailsAreVisible: false,
            friend: {
                id: "manuel",
                name: "Manuel Lorenz",
                phone: "0123 45678 90",
                email: "manuel@localhost.com",
            },
        };
    },
    methods: {
        toggleDetails() {
            this.detailsAreVisible = !this.detailsAreVisible;
        }
    }
}
</script>