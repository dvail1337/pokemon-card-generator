<script>
    const pokemonCard = {
        name: "",
        type: "",
        hpValue: "",
        image: "",
        species: "",
        length: "",
        weight: "",
        firstAttackName: "",
        firstAttackElement: "",
        firstAttackDamage: "",
        secondAttackName: "",
        secondAttackElement: "",
        secondAttackDescription: "",
        secondAttackDamage: "",
        weakness: "",
        resistance: "",
        retreatCost: "",
        funFact: "",
        lv: "",
    };

    const fire = "./fire.png";
    const water = "./water.png";
    const grass = "./grass.png";
    const ice = "./ice.png";
</script>

<div class="container">
    <div class="card-container">
        <img
            id="pokemon-template"
            class="pokemon-template"
            src="./cardtemplate.png"
            alt="A blank Pokemon card."
        />
        <div class="input-values">
            <img
                src="./{pokemonCard.image}"
                class="image"
                id="image"
                alt="wtf"
            />
            <div id="name">{pokemonCard.name}</div>
            <img src={pokemonCard.type} alt="" id="type" />
            <div id="hp">{pokemonCard.hpValue} HP</div>
            <div id="species">{pokemonCard.species} Pokemon.</div>
            <div id="length">Length: {pokemonCard.length},</div>
            <div id="weight">Weight: {pokemonCard.weight} lbs.</div>
            <img
                src={pokemonCard.firstAttackElement}
                alt=""
                id="first-attack-element"
            />

            <div id="first-attack-name">{pokemonCard.firstAttackName}</div>
            <div id="first-attack-damage">{pokemonCard.firstAttackDamage}</div>
            <div id="line" />
            <img
                src={pokemonCard.secondAttackElement}
                alt=""
                id="second-attack-element"
            />
            <div id="second-attack-name">{pokemonCard.secondAttackName}</div>
            <div id="second-attack-description">
                {pokemonCard.secondAttackDescription}
            </div>
            <div id="second-attack-damage">
                {pokemonCard.secondAttackDamage}
            </div>
            <img src={pokemonCard.weakness} alt="" id="weakness" />
            <img src={pokemonCard.resistance} alt="" id="resistance" />
            <img src={pokemonCard.retreatCost} alt="" id="retreat-cost" />
            <div id="fun-fact">{pokemonCard.funFact}</div>
            <div id="lv">LV. {pokemonCard.lv}</div>
        </div>
    </div>

    <form class="user-inputs">
        <label for="image">Image URL:</label>
        <input
            id="img-upload"
            name="image"
            type="file"
            bind:value={pokemonCard.image}
        />

        <label for="name">Name:</label>
        <input
            name="name"
            type="text"
            bind:value={pokemonCard.name}
            placeholder="Name"
        />

        <label for="type">Type:</label>
        <select name="type" bind:value={pokemonCard.type}>
            <option value={fire}>Fire</option>
            <option value={water}>Water</option>
            <option value={grass}>Grass</option>
            <option value={ice}>Ice</option>
        </select>

        <label for="hpValue">HP:</label>
        <input
            name="hpValue"
            type="text"
            bind:value={pokemonCard.hpValue}
            placeholder="HP"
        />

        <label for="species">Species:</label>
        <input
            name="species"
            type="text"
            bind:value={pokemonCard.species}
            placeholder="Species"
        />

        <label for="length">Length:</label>
        <input
            type="text"
            bind:value={pokemonCard.length}
            placeholder="Length"
        />

        <label for="weight">Weight:</label>
        <input
            type="text"
            bind:value={pokemonCard.weight}
            placeholder="Weight"
        />

        <label for="firstAttackElement">First Attack Element:</label>
        <select
            name="firstAttackElement"
            bind:value={pokemonCard.firstAttackElement}
        >
            <option value={fire}>Fire</option>
            <option value={water}>Water</option>
            <option value={grass}>Grass</option>
            <option value={ice}>Ice</option>
        </select>

        <label for="firstAttackName">First Attack Name:</label>
        <input
            type="text"
            bind:value={pokemonCard.firstAttackName}
            placeholder="Attack Name"
        />

        <label for="firstAttackDamage">First Attack Damage:</label>
        <input
            type="text"
            bind:value={pokemonCard.firstAttackDamage}
            placeholder="Attack Damage"
        />

        <label for="secondAttackElement">Second Attack Element:</label>
        <select
            name="secondAttackElement"
            bind:value={pokemonCard.secondAttackElement}
        >
            <option value={fire}>Fire</option>
            <option value={water}>Water</option>
            <option value={grass}>Grass</option>
            <option value={ice}>Ice</option>
        </select>

        <label for="secondAttackName">Second Attack Name:</label>
        <input
            type="text"
            bind:value={pokemonCard.secondAttackName}
            placeholder="Attack Name"
        />

        <label for="secondAttackDescription">Second Attack Description:</label>
        <textarea
            rows="3"
            bind:value={pokemonCard.secondAttackDescription}
            placeholder="Attack Description"
        />

        <label for="secondAttackDamage">Second Attack Damage:</label>
        <input
            type="text"
            bind:value={pokemonCard.secondAttackDamage}
            placeholder="Attack Damage"
        />

        <label for="weakness">Weakness:</label>
        <select name="weakness" bind:value={pokemonCard.weakness}>
            <option value={fire}>Fire</option>
            <option value={water}>Water</option>
            <option value={grass}>Grass</option>
            <option value={ice}>Ice</option>
        </select>

        <label for="resistance">Resistance:</label>
        <select name="resistance" bind:value={pokemonCard.resistance}>
            <option value={fire}>Fire</option>
            <option value={water}>Water</option>
            <option value={grass}>Grass</option>
            <option value={ice}>Ice</option>
        </select>

        <label for="retreatCost">RetreatCost:</label>
        <select name="retreatCost" bind:value={pokemonCard.retreatCost}>
            <option value={fire}>Fire</option>
            <option value={water}>Water</option>
            <option value={grass}>Grass</option>
            <option value={ice}>Ice</option>
        </select>

        <label for="funFact">Fun Fact:</label>
        <textarea
            rows="3"
            bind:value={pokemonCard.funFact}
            placeholder="Fun Fact"
        />

        <label for="lv">Level:</label>
        <input type="text" bind:value={pokemonCard.lv} placeholder="Level" />
    </form>
</div>

<style>
    .container {
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        width: 100%;
    }
    .input-values {
        width: 300px;
    }
    .user-inputs {
        border: 4px solid pink;
        display: flex;
        flex-direction: column;
        overflow-y: scroll;
        height: 420px;
        background-color: transparent;
        border-radius: 20px;
        padding: 20px;
        float: right;
    }
    .user-inputs::-webkit-scrollbar {
        display: none;
    }

    .card-container {
        position: relative;
        text-align: center;
    }
    .pokemon-template {
        display: flex;
        max-width: 425px;
        background-color: white;
        border-radius: 25px;
    }
    textarea {
        min-height: 100px;
    }
    #img-upload {
        min-height: 38px;
    }
    #name {
        font-family: Calibri Condensed;
        font-weight: bold;
        font-size: 30px;
        position: absolute;
        top: 30px;
        left: 43px;
    }
    #hp {
        font-family: Calibri Condensed;
        color: red;
        font-size: 30px;
        position: absolute;
        top: 30px;
        right: 72px;
    }
    #image {
        position: absolute;
        top: 75px;
        left: 51px;
        max-width: 325px;
        max-height: 231px;
    }
    #species {
        font-family: Calibri;
        font-weight: bold;
        font-style: italic;
        position: absolute;
        font-size: 12px;
        top: 323px;
        left: 95px;
    }
    #length {
        font-family: Calibri;
        font-weight: bold;
        font-style: italic;
        position: absolute;
        font-size: 12px;
        top: 323px;
        left: 177px;
    }
    #weight {
        font-family: Calibri;
        font-weight: bold;
        font-style: italic;
        position: absolute;
        font-size: 12px;
        top: 323px;
        left: 255px;
    }
    #first-attack-name {
        font-family: Calibri;
        font-weight: bold;
        position: absolute;
        font-size: 25px;
        top: 360px;
        left: 186px;
    }
    #line {
        position: absolute;
        width: 350px;
        top: 414px;
        left: 36px;
        border-bottom: 1px solid black;
    }
    #first-attack-damage {
        font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS",
            sans-serif;
        position: absolute;
        font-size: 35px;
        top: 355px;
        left: 340px;
    }
    #second-attack-damage {
        font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS",
            sans-serif;
        position: absolute;
        font-size: 35px;
        top: 430px;
        left: 340px;
    }
    #second-attack-name {
        font-family: Calibri;
        font-weight: bold;
        position: absolute;
        font-size: 23px;
        top: 420px;
        left: 73px;
    }
    #second-attack-description {
        font-family: Calibri;
        position: absolute;
        width: 200px;
        text-align: left;
        font-size: 12px;
        top: 422px;
        left: 130px;
    }
    #fun-fact {
        font-family: Calibri;
        font-style: italic;
        position: absolute;
        font-weight: bold;
        width: 320px;
        text-align: left;
        font-size: 12px;
        line-height: 13px;
        bottom: 37.5px;
        left: 47px;
    }
    #lv {
        font-family: Calibri;
        font-style: italic;
        position: absolute;
        font-weight: bold;
        width: 320px;
        text-align: left;
        font-size: 12px;
        line-height: 13px;
        bottom: 37.5px;
        left: 335px;
    }
    #first-attack-element {
        position: absolute;
        max-width: 22px;
        top: 365px;
        left: 44px;
    }
    #second-attack-element {
        position: absolute;
        max-width: 22px;
        top: 424px;
        left: 44px;
    }
    #weakness {
        position: absolute;
        max-width: 20px;
        top: 504px;
        left: 55px;
    }
    #resistance {
        position: absolute;
        max-width: 20px;
        top: 504px;
        left: 198px;
    }
    #retreat-cost {
        position: absolute;
        max-width: 20px;
        top: 504px;
        left: 340px;
    }
    #type {
        position: absolute;
        max-width: 28px;
        top: 31px;
        left: 355px;
    }
</style>
