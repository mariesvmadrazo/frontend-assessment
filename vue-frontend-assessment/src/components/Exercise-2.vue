<template>
  <main class="p-5 my-0 mx-auto bg-white">
    <input id="tab1" type="radio" name="tabs" checked>
    <label for="tab1">Section 1</label>
    <section id="content1" class="w-90"><p>Maecenas nec semper ante, pellentesque posuere lorem. Nullam ipsum massa, consequat eget urna ut, pulvinar dignissim lorem. Nulla facilisi. Nam mattis eleifend metus. Fusce at commodo lorem. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Phasellus pellentesque elit sem, vel blandit posuere.</p></section>

    <input id="tab2" type="radio" name="tabs">
    <label for="tab2">Section 2</label>
    <section id="content2" class="w-90"><p>Mauris a orci sodales, scelerisque velit vitae, gravida nisl. Ut non laoreet eros, vel laoreet nisi. Praesent sed dolor dui. Proin non fringilla quam. Aliquam erat volutpat. Vestibulum vel arcu semper, lobortis turpis ac, ultricies nisi. Praesent id.</p></section>

    <input id="tab3" type="radio" name="tabs">
    <label for="tab3">Section 3</label>
    <section id="content3" class="w-90"><p>Sed elementum sapien ut sapien imperdiet, eu venenatis enim rhoncus. Praesent euismod tincidunt rhoncus. Duis cras amet:</p><ul><li>List item one</li><li>List item two</li><li>List item three</li></ul></section>

    <input id="tab4" type="radio" name="tabs">
    <label for="tab4">Section 4</label>
    <section id="content4" class="w-90"><p>Cras dictum. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Aenean lacinia mauris vel est.</p><p>Suspendisse eu nisl. Nullam ut libero. Integer dignissim consequat lectus. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.</p></section>
  </main>
</template>

<script>
export default {
}
</script>

<style scoped>
::v-deep #content3 ul li {
    list-style-position: inside;
}

.tabArea {
  border-bottom: 1px solid #ccc;
}
section {
  display: none;
  padding: 20px 0 0;
  position: absolute;
  width: calc(100% - 6rem);
}
input {
  display: none;
}
label {
  display: inline-block;
  margin: 0 0 -1px;
  padding: 15px 25px;
  font-weight: 600;
  text-align: center;
  color: #bbb;
  border: 1px solid transparent;
}
label:hover {
  color: #888;
  cursor: pointer;
}
input:checked + label {
  color: #555;
  border: 1px solid #ddd;
  border-top: 2px solid orange;
  border-bottom: 1px solid #fff;
}
#tab1:checked ~ #content1,
#tab2:checked ~ #content2,
#tab3:checked ~ #content3,
#tab4:checked ~ #content4 {
  display: block;
}
@media screen and (max-width: 650px) {
  label {
    text-align: left;
    display: block;
  }
  label:before {
    margin: 0;
    font-size: 18px;
  }
  section {
    position: relative;
  }
  .tabArea {
    border: none;
  }
}
@media screen and (max-width: 400px) {
  label {
    padding: 15px;
  }
}
</style>