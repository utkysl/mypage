<template>
    <div class="container">
        <h2 class="title">My GitHub Projects</h2>
        <div v-if="repos.length" class="repo-container">
            <div v-for="repo in repos" :key="repo.id" class="repo-card">
                <h3>{{ repo.name }}</h3>
                <p>{{ repo.description || 'No description available' }}</p>
                <a :href="repo.html_url" target="_blank" rel="noopener noreferrer">View on GitHub</a>
            </div>
        </div>
        <p v-else>Loading...</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            repos: []
        }
    },
    mounted() {
        this.fetchRepos();
    },
    methods: {
        async fetchRepos() {
            try {
                const response = await fetch('https://api.github.com/users/utkysl/repos');
                const data = await response.json();
                this.repos = data;
            } catch (error) {
                console.error('Error fetching repos:', error);
            }
        }
    }
}
</script>

<style scoped>
body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    color: #333;
    margin: 0;
    padding: 0;
}

.title {
    text-align: center;
    color: #ffffff;
    text-decoration: underline;
    margin-top: 40px;
    margin-bottom: 20px;
    font-size: 3em;
}


.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
}


.repo-container {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
}


.repo-card {
    border: 1px solid #ddd;
    padding: 20px;
    border-radius: 12px;
    background-color: #fff;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s, box-shadow 0.3s;
    width: 300px;
    max-width: 100%;
    box-sizing: border-box;
    text-align: center;
}


.repo-card h3 {
    margin-top: 0;
    color: #333;
    font-size: 1.5em;
}

.repo-card p {
    color: #666;
    font-size: 1em;
    margin: 10px 0;
}


.repo-card a {
    color: #007bff;
    text-decoration: none;
    font-weight: bold;
}


@media (max-width: 768px) {
    .title {
        font-size: 1.5em;
    }

    .repo-card {
        width: 100%;
        max-width: 90%;
    }
}
</style>