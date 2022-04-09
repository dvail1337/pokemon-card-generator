<script>
    export let name;
    export let hpValue;
    export let image;
    export let species;
    export let lengthFeet;
    export let lengthInches;
    export let firstAttackElement;
    export let firstAttackName;
    export let firstAttackDescription;
    export let firstAttackDamage;
    export let secondAttackElement;
    export let secondAttackName;
    export let secondAttackDescription;
    export let secondAttackDamage;
    export let weakness;
    export let resistance;
    export let retreatCost;
    export let funFact;
    export let lv;

    export let left = 30;
    export let top = 30;
    export let moving = false;

    export function start() {
        moving = true;
    }

    export function stop() {
        moving = false;
    }

    export function move(e) {
        if (moving) {
            left += e.movementX;
            top += e.movementY;
        }
    }
</script>

<div class="input-values">
    <img class="image" src={image} alt="Something." />
    <div class="name">{name}</div>
    <div class="hp">{hpValue} HP</div>
    <div class="species">{species} Pokemon.</div>
    <div class="length">Length: {lengthFeet}' {lengthInches}",</div>
    <div class="first-attack-element">{firstAttackElement}</div>
    <div class="first-attack-name">{firstAttackName}</div>
    <div class="first-attack-description">{firstAttackDescription}</div>
    <div class="first-attack-damage">{firstAttackDamage}</div>
    <div class="second-attack-element">{secondAttackElement}</div>
    <div class="second-attack-name">{secondAttackName}</div>
    <div class="second-attack-description">
        {secondAttackDescription}
    </div>
    <div class="second-attack-damage">{secondAttackDamage}</div>
    <div class="weakness">{weakness}</div>
    <div class="resistance">{resistance}</div>
    <div class="retreat-cost">{retreatCost}</div>
    <div class="fun-fact">{funFact}</div>
    <div class="lv">LV. {lv}</div>
</div>
