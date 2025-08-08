<script>


    import Button from '../../Components/Button.svelte';
	import { onMount } from "svelte";


    let points = $state(0)
    let clickingpower = $state(1);
    let passiveIncome = $state(0);

    let upgradeClickCost = $state(50);
    let upgradePassiveCost = $state(100);


    onMount(() => {
        // Interval
        let passiveTimer = setInterval(() => {
            points+=passiveIncome;
        }, 1000)
        return () => clearInterval(passiveTimer);
    });



    function increment(){ 
        points += clickingpower
    }

    function upgradeClickingPower(amount){
        if(points-amount *upgradeClickCost >= 0){
            points-=amount *upgradeClickCost;
            clickingpower += amount
        }
    }

    function upgradePassiveIncomme(amount) {
        if(points-amount *upgradeClickCost >=0) {
            points-=amount *upgradeClickCost;
            passiveIncome+=amount;
        }
    }





</script>

<!-- conatiner -->
<div class = "text-red-600 h-screen bg-gray-200 flex flex-col justify-center items-center">
    <div>{points}</div>
    <!-- svelte-ignore a11y_consider_explicit_label -->
    <button onclick = {increment} class = "active:scale-110 transition-all rounded-full duration-250 h-48 w-48 bg-purple-900"></button>



    <!-- Options -->
    <div class = "border w-full text-center flex flex-row ">
        <div class = "w-1/2 flex flex-col">
            <div>Click Upgrades</div>
                <div> 
                    <Button text = "+1 -{1*upgradeClickCost}" fn = {() => upgradeClickingPower(1)}/>
                    <Button text = "+5 -{5*upgradeClickCost}" fn = {() => upgradeClickingPower(5)}/>
                    <Button text = "+10 -{10*upgradeClickCost}" fn = {() => upgradeClickingPower(10)}/>
                    
                </div>
                
        </div>
        <div class = "w-1/2 flex flex-col">
            <div>Passive Upgrades</div>
            <div>
                <Button text ="+1 -{0.5*upgradePassiveCost} " fn = {() => upgradePassiveIncomme(1)}/>
                <Button text ="+5 - {1*upgradePassiveCost} " fn = {() => upgradePassiveIncomme(5)}/>
                <Button text ="+10 - {2.5*upgradePassiveCost} " fn = {() => upgradePassiveIncomme(10)}/>
                
                
            </div>
        </div>
    </div>
</div>


