<style>
  h4 { background-color: #64b5f6; padding: 0.2rem; margin-bottom: 1px; margin-right: 1px; font-weight: 300}
</style>

<template>
  <v-app >
    <v-app-bar
      app
      dark
      color="blue lighten-2"
    >
      <v-select
        dense           
        v-model="view"
        :items="items"
        item-text="text"
        item-value="value"
        color="blue lighten-2"
      />
    </v-app-bar>
    <v-main app >
      <div :is="view" ></div>
    </v-main>
  </v-app>
</template>

<script>
import autogenerate from '@/components/autogenerate.vue'
import simple from '@/components/simple.vue'
import textfields from '@/components/textfields.vue'
import emptymodel from '@/components/emptymodel.vue'
import basic from '@/components/basic.vue'
import grouping from '@/components/grouping.vue'
import async from '@/components/async.vue'
import grid from '@/components/grid.vue'
import dragdrop from '@/components/dragdrop.vue'
import css from '@/components/css.vue'
import displayhelpers from '@/components/displayhelpers.vue'
import deep from '@/components/deep.vue'
import partial from '@/components/partial.vue'
import multisourcedata from '@/components/multisourcedata.vue'
import complex from '@/components/complex.vue'
import arrayease from '@/components/arrayease.vue'
import array from '@/components/array.vue'
import selection from '@/components/selection.vue'
import selectioncascading from '@/components/selectioncascading.vue'
import treeview from '@/components/treeview.vue'
import conditional from '@/components/conditional.vue'
import list from '@/components/list.vue'
import pickers from '@/components/pickers.vue'
import images from '@/components/images.vue'
import dynamic from '@/components/dynamicattributes.vue'
import typehandling from '@/components/typehandling.vue'

const items = [
  { value: 'simple', text: 'Textfields' }, 
  { value: 'textfields', text: 'Textfields with HTML Type Attribute' }, 
  { value: 'autogenerate', text: 'Missing Schema Definition' }, 
  { value: 'emptymodel', text: 'Empty Model Object' }, 
  { value: 'basic', text: 'Missing Properties in Model or Schema'}, 
  { value: 'typehandling', text: `Handling special Schema-Key 'type' occuring in Model-Data `}, 
  { value: 'dynamic', text: 'Work with Dynamic Attributes Schema, Model and Grid' }, 
  { value: 'grouping', text: 'Group Controls'}, 
  { value: 'async', text: 'Async Loading of Form-Base Attributes'}, 
  { value: 'css', text: 'CSS, Slots, Tooltips & Buttons'}, 
  { value: 'dragdrop', text: 'Drag & Drop'}, 
  { value: 'displayhelpers', text: 'Display, Typo & Layout control with Vuetify display helpers'}, 
  { value: 'deep', text: 'Deep nested Model-Data including Objects & Arrays'}, 
  { value: 'selection', text: 'Selection, Combobox, Autocomplete from Schema-Array'}, 
  { value: 'selectioncascading', text: 'Cascading Selection using computed Schema-Array'}, 
  { value: 'list', text: 'List from Model-Data'}, 
  { value: 'treeview', text: 'Treeviews from Model-Data'}, 
  { value: 'arrayease', text: 'Dynamic Array from Model-Data '}, 
  { value: 'array', text: 'Add, Edit and Drag to Remove Items from Array in Model-Data'}, 
  { value: 'multisourcedata', text: 'Integrate Multi-Source Data by using Form-Base as Slot in Form-Base'}, 
  { value: 'pickers', text: 'Date, Time, Color as native HTML-Type, Menu and Pickers'},
  { value: 'images', text: 'Images'},
  { value: 'grid', text: 'Responsive Grid using Flex, Order and Offset'}, 
  { value: 'partial', text: 'Partial & Linked Model-Data Object'}, 
  { value: 'conditional', text: 'Conditional Form'}, 
  { value: 'complex', text: 'Form-Base with Rules and Validation'}, 
]

export default {
  components: {
    autogenerate, dynamic, simple, textfields, emptymodel, basic, grouping, async, grid, dragdrop, css, displayhelpers, deep, partial, multisourcedata, 
    complex, treeview, arrayease, array, selection, selectioncascading, conditional, list, pickers, images, typehandling 
  },
  data () {
    return {
      items,
      view: items[0].value
    }
  },  
}
</script>