<script>
	let horas = 0 + " h";
	let minutos = 0 + " min";
	let tarifa = 0 + " €/h";
	let precioFinal = 0;

	function calcularFactura(horas, minutos, tarifa) {
		let tiempoHoras = horas * 60;
		console.log(tiempoHoras);
		let tiempoMinutos = parseFloat(tiempoHoras) + parseFloat(minutos);
		console.log(tiempoMinutos);
		let tiempoTotal = tiempoMinutos * tarifa;
		console.log(tiempoTotal);
		let precioFinal = tiempoTotal / 60;
		console.log(precioFinal);
		let tarificadorResultado = document.getElementById('tarificadorResultado');
		tarificadorResultado.textContent = precioFinal + "€";
	}
</script>

<section class="tarificador">
	<div class="tarificador__tiempo">
		<div class="tarificador__horas">
			<input bind:value={horas} type="datetime" name="horas" id="horas"/>
			<label for="horas">Horas trabajadas</label>
		</div>
		<div class="tarificador__minutos">
			<input bind:value={minutos} type="datetime" name="minutos" id="minutos"/>
			<label for="minutos">Minutos trabajados</label>
		</div>
        <div class="tarificador__tarifa">
            <input bind:value={tarifa} type="number" name="tarifa" id="tarifa" />
            <label for="tarifa">Tarifa por hora (€/h)</label>
        </div>
        <div class="tarificador__boton">
            <button class="tarificador__button" on:click={calcularFactura(horas, minutos, tarifa)}>ENTER</button>
        </div>
	</div>
	<div class="tarificador__resultado">
		<h4 class="tarificador__h4">Precio final del trabajo</h4>
		<h3 id="tarificadorResultado" class="tarficador__h3">
			{precioFinal.toFixed(3)+" €"}
		</h3>
	</div>
</section>

<style>

    .tarificador__tiempo{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .tarificador__horas{
        display: flex;
        flex-direction: column;
        margin: 15px 0px;
    }

    .tarificador__minutos{
        display: flex;
        flex-direction: column;
        margin: 15px 0px;
    }

    .tarificador__tarifa{
        display: flex;
        flex-direction: column;
        margin: 15px 0px;
    }

    .tarificador__button{
        background: var(--color-principal);
        color: white;
        font-family: var(--fuente-principal);
        width: 230px;
        text-align: center;
        padding: 10px 0px;
        border: 0px;
        border-radius: 12px;
        box-shadow: 0px 2px 4px 0px black;
    }

    .tarificador__button:hover{
        background: var(--color-secundario);
        color: white;
        font-family: var(--fuente-principal);
        width: 230px;
        text-align: center;
        padding: 10px 0px;
        border: 0px;
        border-radius: 12px;
        box-shadow: 0px 2px 4px 0px black;
    }

.tarificador__resultado{
    text-align: center;
    margin: 30px 0px;
}
</style>
