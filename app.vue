<script setup lang="ts">
import { Pool } from "pg";

const db = new Pool({
  user: "postgres",
  host: "localhost",
  database: "postgres",
  password: "12345",
  port: 5432,
  max: 10,
})

const connectToDB = async () => {
  try {
    await db.connect();
  } catch (err) {
    console.log(err);
  }
};
connectToDB();
</script>

<template>
  <div>
  </div>
</template>
