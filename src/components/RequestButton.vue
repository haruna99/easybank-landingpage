<template>
    <div class="button-div">
      <v-btn
        rounded
        class="request-btn"
      >
        Request Invite
      </v-btn>
    </div>
</template>

<style lang="scss">
    .button-div {
      margin-top: -.6rem;

      .request-btn {
        background-image: linear-gradient(to right, hsl(136, 65%, 51%), hsl(192, 70%, 51%));
        color: #fff !important;
        text-transform: capitalize;
        font-weight: 700;
        font-size: 1.1rem !important;

        &:hover {
            transform: scale(1.1);
        }
      }
    }
</style>