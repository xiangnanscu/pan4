<template>
  <Page>
    <ActionBar>
      <Label text="Home" />
    </ActionBar>

    <GridLayout>
      <Label class="info">
        <FormattedString>
          <Span class="fas" text.decode="&#xf135; " />
          <Span :text="message" />
          <Button @click="add">add</Button>
        </FormattedString>
      </Label>
    </GridLayout>
  </Page>
</template>

<script>
export default {
  data() {
    return {
      cnt:0
    }
  },
  methods: {
    add() {
      this.cnt++
    }
  },
  computed: {
    message() {
      return `Blank {N}-Vue app? ${this.cnt}`;
    }
  }
};
</script>

<style scoped lang="scss">
@import '@nativescript/theme/scss/variables/blue';

// Custom styles
.fas {
  @include colorize($color: accent);
}

.info {
  font-size: 20;
  horizontal-align: center;
  vertical-align: center;
}
</style>

