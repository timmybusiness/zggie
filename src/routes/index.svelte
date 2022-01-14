<style>

    div 
    { 
        width: 1000px; height: 1000px;
    }
</style>

<script>
	let m = { x: 0, y: 0, pressure: '' };

    /*  
        Windows Firefox:    works
        Windows Chrome:     buggy (swipe left interrupts)
        Mac Firefox:        works
        Mac Chrome:         works
        Mac Safari:         no response
        iPad Safari:        buggy (scroll interrupts)
    */
	function handlePressure(event) {
		//m.x = event.clientX;
		//m.y = event.clientY;
        m.pressure = event.pressure;
	}
</script>

<div on:pointermove={handlePressure}>
	The pressure is {m.pressure}
</div>



