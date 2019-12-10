<script>
  // Modules
  import headerConfig from "./components/header/HeaderConfig";
  import ModalConfig from "./components/form/modal/ModalConfig";

  // Components
  import Header from "./components/header/Header.svelte";
  import Main from "./components/Main.svelte";
  import Section from "./components/Section.svelte";
  import Form from "./components/form/Form.svelte";
  import Modal from "./components/form/modal/Modal.svelte";

  // Variables
  let valueModal;
</script>

<Header {...headerConfig} />
<Main>
  <Section>
    <Form bind:selectionFromModal={valueModal} />
    <br />
    <br />
    <p>Value from modal:{valueModal}</p>
  </Section>
</Main>
<Modal {...ModalConfig} />
