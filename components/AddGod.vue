<template>
    <form class="add-entity-form" action="/" method="POST">
        <div class="input-container">
            <label for="name">Name</label>
            <input type="text" id="name" placeholder="Zeus" v-model="name">
        </div>

        <div class="input-container">
            <label for="nickname">Nickname</label>
            <input type="text" id="nickname" placeholder="God of thunder" v-model="nickname">
        </div>
        <div class="input-container">
            <label for="description">Description</label>
            <input type="text" id="description" placeholder="Ubergod that rules over all other gods, resides on mount olympus" v-model="description">
        </div>
        <div class="input-container">
            <label for="commandments">Commandments</label>
            <input type="text" id="commandments" placeholder="Hump many women and lightning is cool. Cheat on waifu's for new waifu's. Create demihumans cuz of thirst" v-model="commandments">
        </div>
        <div class="input-container">
            <label for="alignment">Alignment</label>
            <input type="text" id="alignment" placeholder="Good" v-model="alignment">
        </div>
        <div class="input-container">
            <label for="followers">Followers</label>
            <input type="text" id="followers" placeholder="Ancient greek people" v-model="followers">
        </div>
        <div class="input-container">
            <label for="domain">Domain</label>
            <div v-for="(domain, key) in domains" :key="key">
                <input type="text" id="domain" placeholder="Thunder, lightning and pikachu" v-model="domains[key]">
            </div>
            <button type="button" @click="addDomain">add domain</button>
        </div>
        <button type="button" @click="storeGod">Submit god</button>
    </form>
</template>
<script>
import axios from "axios";

export default {
    data() {
        return {
            name: "",
            nickname: "",
            description: "",
            commandments: "",
            alignment: "",
            followers: "",
            domains: [""]
        }
    },
    methods: {
        storeGod() {
            axios.post("localhost:8000/api/gods", {
                name: this.name,
                nickname: this.nickname,
                description: this.description,
                commandments: this.commandments,
                alignment: this.alignment,
                followers: this.followers,
                domain: this.domain
            }).then((data) => {
                //yoyo
            }).catch((error) => {
                //nono
            })
        },
        addDomain() {
            this.domains.push("")
        }
    }
}
</script>