<html lang="ko">
<head>
</head>
<style>
    .wrapper {
        background-color: #EDF2EC;
        color: #438261;
    }

    .container {
        width: 100%;
        text-align: left;
        font-size: 8vh;
        display: flex;
        background-color: #EDF2EC;
        color: #438261;
    }
    
</style>
<body>
    <div class="wrapper">
        <div class="container">
            <h1> 총이와 청이🐸</h1>
            <h6></h6>
            
        </div> 
        <div id="count">D+??</div>
    </div>
</body>
</html>
<script>
    const goalDate = new Date("2024-12-09").getTime();

    function calcDate() {
        const now = new Date().getTime();
        const distance = now - goalDate;
        

        var days = Math.floor(distance / (1000*60*60*24))+2;
        //var hours = Math.floor((distance % (1000*60*60*24)) / (1000*60*60));
        //var minutes = Math.floor((distance % (1000*60*60)) / (1000*60));
        //var seconds = Math.floor((distance % (1000*60)) / 1000);
        document.getElementById('count').style.fontSize = "50vh";
        document.getElementById('count').style.textAlign = 'right';
        document.getElementById('count').style.vertialAlign = 'bottom';
        document.getElementById('count').style.fontWeight = '700'
        if (distance < 0) {
            return 'D+${days}';
        } else {
            return `D+${days}`;
        }
    }
    
    setInterval(() => {
        document.getElementById('count').innerText = calcDate();
    }, 1000);

</script>
