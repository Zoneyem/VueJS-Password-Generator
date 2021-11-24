<template>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link
    href="https://fonts.googleapis.com/css2?family=Arvo:wght@700&display=swap"
    rel="stylesheet"
  />
  <div class="exercise">
    <h1>{{ title }}</h1>

    <div class="genpass">{{ generatedPassword }}</div>
    <div class="copy-to-clipboard">Copy to clipboard</div>
    <h3>{{ choose }}:</h3>
    <!-- FORM-->
    <form @input="generatePassword()" action="" class="form_wrapper">
      <div class="container button-row">
        <div class="lowercase inline-block">
          <input type="checkbox" name="characters" id="pw-lowercase" checked />
          <label for="pw-lowercase" class="char-category">Lowercase</label>
        </div>
        <div class="uppercase inline-block">
          <input type="checkbox" name="characters" id="pw-uppercase" checked />
          <label for="pw-uppercase" class="char-category">Uppercase</label>
        </div>
        <div class="numbers inline-block">
          <input type="checkbox" name="characters" id="pw-numbers" checked />
          <label for="pw-numbers" class="char-category">Numbers</label>
        </div>
        <div class="special inline-block">
          <input type="checkbox" name="characters" id="pw-symbols" checked />
          <label for="pw-symbols" class="char-category">Symbols </label>
        </div>
      </div>
      <div>
        <h3>{{ pl }}</h3>
        <input
          @input="updateValue()"
          type="range"
          name=""
          id="pw-length"
          min="8"
          max="35"
          :value="length"
        />
        <label for="pw-length">{{ length }}</label>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  props: ["welc"],
  data() {
    return {
      title: "PASSWORD GENERATOR",
      length: 8,
      generatedPassword: "abcdefgh",
      lowercasecharacters: "abcdefghijklmnopqrstuvwxyz",
      uppercasecharacters: "ABCDEFGHIJKLMNOPQRSTUVWXYZ",
      numbers: "0123456789",
      symbols: "!§,;.:-_#+*~§$%&?<>°^",
      choose: "Choose your character set",
      pl: "Password Length",
    };
  },

  methods: {
    updateValue() {
      this.length = document.querySelector("#pw-length").value;
      return this.length;
    },
    generatePassword() {
      this.generatedPassword = "";
      const lowerCase = document.querySelector("#pw-lowercase");
      const upperCase = document.querySelector("#pw-uppercase");
      const numbers = document.querySelector("#pw-numbers");
      const symbols = document.querySelector("#pw-symbols");
      let characters = "";

      if (lowerCase.checked) {
        characters += this.lowercasecharacters;
        console.log(characters);
      }
      if (upperCase.checked) {
        characters += this.uppercasecharacters;
        console.log(characters);
      }
      if (numbers.checked) {
        characters += this.numbers;
        console.log(characters);
      }
      if (symbols.checked) {
        characters += this.symbols;
        console.log(characters);
      }
      for (let i = 0; i < this.length; i++) {
        this.generatedPassword += characters.charAt(
          Math.floor(Math.random() * characters.length)
        );
      }
      return this.generatedPassword;
    },
  },
};
</script>

<style scoped>
@media (max-width: 768px) {
  .form_wrapper {
    display: block;
    margin: 0 auto;
  }
  h1 {
    color: #2292a4;
    margin-bottom: 70px;
    text-align: center;
  }

  .button-wrapper {
    justify-content: center;
    display: flex;

    flex-grow: 1;
    flex-shrink: 1;
  }

  .button-row {
    flex-basis: 100%;
  }

  div.button-col {
    display: inline-block;

    width: 50%;
    margin-top: 5px;
  }
}
h3 {
  color: white;
  margin-bottom: 20px;
}

.genpass {
  color: white;
  text-align: center;
  width: 60%;
  height: 50px;
  background-color: rosybrown;
  margin-bottom: 40px;
}

.newbutton {
  padding: 0.4em;

  border-radius: 5px;
  background-color: #0f0a0a;
  color: slategrey;
}

input {
  color: #f5efed;
  text-align: center;
  width: 80%;
  height: 30px;
  background-color: slategrey;
}
label {
  color: #f5efed;
  text-align: center;
  width: 80%;
  height: 30px;
}

.copy-to-clipboard {
  display: block;
  background: #2292a4;
  margin: 0 auto;
  padding: 0.6em;
  color: black;
  width: 10%;
  border-radius: 2px;
  margin-bottom: 150px;
}
#myCopy {
  display: block;
  margin: 0 auto;
  margin-bottom: 20px;
}

#lastcheck {
  display: block;
}

.isClicked {
  background: #2292a4;
  color: black;
}

.click-color {
  display: block;
  background: #2292a4;
  margin: 0 auto;
  padding: 0.6em;
}

@media (min-width: 768px) {
  h1 {
    margin-bottom: 50px;
  }
  .container {
    margin-bottom: 30px;
  }
  .button-wrapper {
    justify-content: center;
    display: flex;

    flex-grow: 1;
    flex-shrink: 1;
  }

  .button-row {
    flex-basis: 100%;
    display: flex;
    align-content: space-between;
    justify-content: center;
    margin-top: 10px;
  }

  div.button-col {
    display: inline-block;

    margin-top: 5px;
    margin: 5px;
  }
}
</style>
