<template>
  <nu-block
    id="preview"
    :is-show="show || null"
    interactive="no"
    fill="#clear||#clear :show[#dark.50]"
    theme
    place="fixed cover"
  >
    <nu-card
      :is-show="show || null"
      interactive="yes"
      place="fixed right"
      radius="2r left"
      clear
      border="top left bottom"
      fill="#subtle"
      height="100wh - 4x"
      width="41x||40x (100% - 6x) 78x"
      transition="move"
      move="0 0||100% 0 :show[0 0]"
      display="flex"
      flow="column"
      z="0"
    >
      <nu-flow>
        <nu-pane content="space-between">
          <nu-h2>Preview</nu-h2>
          <ThemeSwitch/>
        </nu-pane>
        <nu-line/>
      </nu-flow>

      <nu-flow
        v-show="props.disabled"
        gap="2x" overflow="auto hidden" padding="2x" space="0 2x 2x 2x" grow="1">
        <nu-ph static size="h4" width="50%" opacity=".25"/>
        <nu-ph static/>
        <nu-ph static/>
        <nu-ph static/>
        <nu-ph static/>
        <nu-ph static size="h4" width="50%" opacity=".25"/>
        <nu-ph static/>
        <nu-ph static/>
        <nu-ph static/>
        <nu-ph static/>
        <nu-ph static size="h4" width="50%" opacity=".25"/>
        <nu-ph static/>
        <nu-ph static/>
        <nu-ph static/>
        <nu-ph static/>
        <nu-ph static size="h4" width="50%" opacity=".25"/>
        <nu-ph static/>
        <nu-ph static/>
        <nu-ph static/>
        <nu-ph static/>
      </nu-flow>

      <nu-flow
        v-show="!props.disabled"
        gap="2x" overflow="hidden auto" padding="2x" space="0 2x 2x 2x" grow="1">
        <nu-pane content="space-between">
          <nu-h5>Numl.Design</nu-h5>
        </nu-pane>

        <nu-pane>
          <nu-block>
            Paragraph text
          </nu-block>

          <nu-line orient="v"/>

          <nu-block color="#special">
            Special paragraph text
          </nu-block>
        </nu-pane>

        <nu-pane>
          <nu-card>
            Basic Card
          </nu-card>
          <nu-card clear>
            Clear Card
          </nu-card>
        </nu-pane>

        <nu-pane flow="row wrap">
          <nu-badge>Basic badge</nu-badge>
          <nu-badge special>Special badge</nu-badge>
        </nu-pane>

        <nu-flow gap>
          <nu-h5>Basic button states</nu-h5>
          <nu-pane flow="row wrap">
            <nu-btn use-action="n">Default</nu-btn>
            <nu-btn use-action="n" is-hover mark>Hover</nu-btn>
            <nu-btn use-action="n" is-active>Pressed</nu-btn>
            <nu-btn use-action="n" is-pressed>Toggled</nu-btn>
            <nu-btn use-action="n" outline="focus" is-focus>Focused</nu-btn>
            <nu-btn use-action="n" disabled>Disabled</nu-btn>
          </nu-pane>
        </nu-flow>

        <nu-flow gap>
          <nu-h5>Clear button states</nu-h5>
          <nu-pane flow="row wrap">
            <nu-btn clear use-action="n">Default</nu-btn>
            <nu-btn clear use-action="n" is-hover mark>Hover</nu-btn>
            <nu-btn clear use-action="n" is-active>Pressed</nu-btn>
            <nu-btn clear use-action="n" is-pressed>Toggled</nu-btn>
            <nu-btn clear use-action="n" outline="focus" is-focus>Focused</nu-btn>
            <nu-btn clear use-action="n" disabled>Disabled</nu-btn>
          </nu-pane>
        </nu-flow>

        <nu-flow gap>
          <nu-h5>Special button states</nu-h5>
          <nu-pane flow="row wrap">
            <nu-btn special use-action="n">Default</nu-btn>
            <nu-btn special use-action="n" is-hover mark>Hover</nu-btn>
            <nu-btn special use-action="n" is-active>Pressed</nu-btn>
            <nu-btn special use-action="n" is-pressed>Toggled</nu-btn>
            <nu-btn special use-action="n" outline="focus" is-focus
            >Focused
            </nu-btn
            >
            <nu-btn special use-action="n" disabled>Disabled</nu-btn>
          </nu-pane>
        </nu-flow>

        <nu-h5>Various widgets</nu-h5>

        <nu-pane gap="2x">
          <nu-radiogroup value="one" gap="2x">
            <nu-pane>
              <nu-radio value="one"></nu-radio>
              <nu-label>1</nu-label>
            </nu-pane>
            <nu-pane>
              <nu-radio value="two"></nu-radio>
              <nu-label>2</nu-label>
            </nu-pane>
          </nu-radiogroup>
          <nu-line orient="v"></nu-line>
          <nu-radiogroup value="three" gap="2x" disabled>
            <nu-pane>
              <nu-radio value="three"></nu-radio>
              <nu-label>3</nu-label>
            </nu-pane>
            <nu-pane>
              <nu-radio value="four"></nu-radio>
              <nu-label>4</nu-label>
            </nu-pane>
          </nu-radiogroup>
        </nu-pane>

        <nu-pane gap="2x">
          <nu-switch></nu-switch>
          <nu-switch checked></nu-switch>
          <nu-switch disabled></nu-switch>
          <nu-switch checked disabled></nu-switch>
        </nu-pane>

        <nu-pane gap="2x">
          <nu-checkbox></nu-checkbox>
          <nu-checkbox checked></nu-checkbox>
          <nu-checkbox disabled></nu-checkbox>
          <nu-checkbox checked disabled></nu-checkbox>
        </nu-pane>

        <nu-listbox value="one">
          <nu-option value="one">
            Option 1
          </nu-option>
          <nu-option value="two">
            Option 2
          </nu-option>
          <nu-option value="three">
            Option 3
          </nu-option>
        </nu-listbox>

        <nu-tablist value="one" border="bottom inside">
          <nu-tab value="one">One</nu-tab>
          <nu-tab value="two">Two</nu-tab>
          <nu-tab value="three">Three</nu-tab>
        </nu-tablist>

        <nu-menu border>
          <nu-menuitem>Menuitem 1</nu-menuitem>
          <nu-menuitem>Menuitem 2</nu-menuitem>
          <nu-menuitem>Menuitem 3</nu-menuitem>
        </nu-menu>

        <nu-slider value="50"></nu-slider>
        <nu-slider value="50" disabled></nu-slider>
        <nu-slider2d min="0 0" max="100 100" step="1 1" value="50 50"></nu-slider2d>

        <nu-input placeholder="Default input"/>
        <nu-input placeholder="Disabled default input" disabled/>
        <nu-input placeholder="Special input" special/>
        <nu-input placeholder="Disabled special input" special disabled/>

        <nu-datepicker mode="range"/>

        <nu-h5>Indicators</nu-h5>

        <nu-block>
          <nu-spin/> Loading...
        </nu-block>

        <nu-ph></nu-ph>

        <nu-progressbar value="50"/>
        <nu-progressbar/>

        <nu-h5>Areas</nu-h5>

        <nu-card fill="#dark" color="#light">
          Dark area
        </nu-card>

        <nu-card fill="#light" color="#dark">
          Light area
        </nu-card>

        <nu-h5>Code converter</nu-h5>

        <nu-card padding="0" overflow="auto">
          <nu-code padding="1x 2x" :value="codeExample"></nu-code>
        </nu-card>

        <nu-markdown :value="markdownExample"></nu-markdown>
      </nu-flow>

      <nu-btn
        show="n||y"
        place="outside-left top 3x 0"
        special
        padding
        radius="99x 0 0 99x"
        toggle
        border="top left bottom"
        width="auto"
        inset="n :active[y]"
        :checked="show"
        @tap="show = !show"
        label="Toggle Preview"
      >
        <nu-icon name="^ eye-outline :checked[chevron-forward-circle-outline]"/>
      </nu-btn>
    </nu-card>
  </nu-block>
</template>

<script setup>
import { computed, defineProps, ref } from 'vue';
import LZString from 'lz-string';
import { convertThemeToMarkup } from '../helpers/nude';
import replMarkup from '../data/repl-markup';
import Placeholder from './Placeholder.vue';
import ThemeSwitch from './ThemeSwitch.vue';

const show = ref(false);
const props = defineProps({
  theme: Object,
  show: Boolean,
  disabled: Boolean,
});
const themeMarkup = computed(() => {
  return convertThemeToMarkup(props.theme);
});
const replHash = computed(() => {
  return LZString.compressToEncodedURIComponent(
    JSON.stringify({
      markup: replMarkup(themeMarkup.value),
    }),
  );
});
// Original: https://numl.tenphi.me/repl#6038e9246cd202483f3a87a4
const replLink = computed(() => `!https://numl.tenphi.me/repl#${replHash.value}`);
const codeExample = `var str = 'String';
var num = 1234;
var regexp = /^RegExp$/

function(arg) {
  return arg * 2;
}`;
const markdownExample = `##### Markdown Converter

Paragraph text with **bold** and *italic* text.

- List item 1
- List item 2`;
</script>
