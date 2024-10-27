<script lang="ts" setup>
const rows: any[] = [];
for (let i = 1; i <= 1000; i++) {
  rows.push(`Row ${i}`);
}
</script>

<template>
  <Page actionBarHidden="true">
    <ActionBar>
      <Label text="Home" class="font-bold text-lg" />
    </ActionBar>

    <GridLayout rows="*" class="px-4">
      <ListView ref="collectionView" :items="rows" rowHeight="80">
        <template #default="{ item }">
          <Label :text="item" class="ml-1 text-xl v-center"></Label>
        </template>
      </ListView>
    </GridLayout>
  </Page>
</template>

<style>
/* .info {
    font-size: 20;
  } */
</style>
