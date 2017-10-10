<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md6>
      <div class="text-xs-center">
        <img src="/v.png" alt="" class="mb-5" />
      </div>
      <v-card>
        <v-card-title class="headline">Welcome to Vueler</v-card-title>
        <v-card-text>
          <p>Vueler is a way to teach web fundamentals with new and fun ways to reason about code.</p>
          
          <p>Take on ideas using pseudocode, and encounter all the tools available to connect your reasoning to the computer.</p>
          <p>For more information on the tools used check out the <a href="/faq">Frequently Asked Questions</a>.</p>
          <p>Start learning how to reason with machines in just 10 minutes.</p>
          <div class="text-xs-right">
            <em><small>&mdash; Vueler</small></em>
          </div>
          <hr class="my-3">
          <a href="https://projecteuler.net/" target="_blank">Project Euler</a>
          <br>
          <a href="https://github.com/Vueler" target="_blank">Vueler Github</a>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="primary" flat nuxt to="/start">Get Started!</v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>
