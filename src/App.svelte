<script>
  import { input } from "./lib/store";

  const onSubmit = (e) => {
    let prompt = JSON.stringify($input.prompt);
    if (prompt.length > 10) {
      console.log("ready to send off to api");
    } else {
      console.log("the prompt is not long enough");
    }
  };
</script>

<main>
  <section>
    <form on:submit|preventDefault={onSubmit}>
      <label for="prompt">Prompt:</label>
      <textarea type="text" id="prompt" bind:value={$input.prompt} />
      <button type="submit">Generate Cover letter</button>
    </form>
  </section>
</main>

<style>
  form {
    width: 70vw;
    height: 90vh;
    display: flex;
    flex-direction: column;
    background-color: whitesmoke;
    border-radius: 15px;
    align-items: center;
    justify-content: space-between;
  }

  label {
    color: grey;
    font-size: 3rem;
    margin: auto auto 0 1.5rem;
    font-weight: 600;
    text-decoration: underline 5px;
  }

  textarea {
    width: 90%;
    height: 60%;
    background-color: grey;
    border: rgba(70, 70, 70, 0.861);
    opacity: 50%;
    border-radius: 10px;
    margin: auto;
    margin-bottom: 1.5rem;
    font-size: 1.5rem;
    resize: none;
    padding: 1rem;
  }
</style>
