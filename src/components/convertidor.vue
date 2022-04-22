// CODIGO HTML
<template>
    <div class="container">
        <div class="row">
            <h3 class="money">MONEDAS</h3>
            <div class="col-lg-12">
            <div class="mb-3">
              <label for="cantidad" class="form-label">Ingrese Cantidad</label>
              <input type="number" class="form-control form-control-lg" 
              v-model="cantidad"
              v-on:keyup="convertirMonedas"
              id="cantidad"  placeholder="Ingrese cantidad">
           </div>            
   </div>
        </div>
        <div class="row">
            <div class="col-lg 6">
               <div class="form-group">
                   <label for="tengo">Tengo</label>
                   <select class="form-select form-select-lg" id="tengo" v-model="tengo" 
                   v-on:change="convertirMonedas">
                   <option v-for="(moneda, index) in monedas" v-bind:key="index">
                       {{moneda}}
                   </option>
                
                   </select>
               </div>
            </div>
            <div class="col-lg-6">
                 <div class="form-group">
                   <label for="quiero">Quiero</label>
                   <select class="form-select form-select-lg" id="quiero" v-model="quiero"
                   v-on:change="convertirMonedas">
                    <option v-for="(moneda, index) in monedas" v-bind:key="index">
                  {{ moneda }} 
                    </option>
                   </select>
               </div>
            </div>
        </div>
        <div class="text-center pt-3">
            <h5>
                <span class="badge alert-success">{{cantidad}} {{tengo}} </span>
                <span class="badge alert-dark">SON</span>
                <span class="badge alert-success">
                     {{getTotal(total)}} {{quiero}} </span>
            </h5>
        </div>
    </div>

<!-- CONVERSOR DE LONGITUD -->
    <div class="container">
        <div class="row">
            <h3 class="long pt-4">LONGITUD</h3>
            <div class="col-lg-12">
            <div class="mb-3">
              <label for="cantidad2" class="form-label">Ingrese la medida</label>
              <input type="number" class="form-control form-control-lg" 
              v-model="cantidad2" v-on:keyup="convertirMedidas"
              id="cantidad2"  placeholder="Ingrese la medida">
           </div>            
   </div>
        </div>
        <div class="row">
            <div class="col-lg 6">
               <div class="form-group">
                   <label for="tengo2">Tengo</label>
                   <select class="form-select form-select-lg" id="tengo2" v-model="tengo2" 
                   v-on:change="convertirMedidas">
                   <option v-for="(medida, index) in medidas" v-bind:key="index">
                       {{medida}}
                   </option>
                
                   </select>
               </div>
            </div>
            <div class="col-lg-6">
                 <div class="form-group">
                   <label for="quiero2">Quiero</label>
                   <select class="form-select form-select-lg" id="quiero2" v-model="quiero2"
                   v-on:change="convertirMedidas">
                    <option v-for="(medida, index) in medidas" v-bind:key="index">
                  {{ medida }} 
                    </option>
                   </select>
               </div>
            </div>
        </div>
    </div>
     <div class="text-center pt-3">
            <h5>
                <span class="badge alert-success">{{cantidad2}} {{tengo2}} </span>
                <span class="badge alert-dark">SON</span>
                <span class="badge alert-success">
                     {{total2}} {{quiero2}} </span>
            </h5>



</div>

<!-- CONVERSOR DE MASA -->
        
         <div class="container">
        <div class="row">
            <h3 class="long pt-4">MASA</h3>
            <div class="col-lg-12">
            <div class="mb-3">
              <label for="cantidad3" class="form-label">Ingrese el dato</label>
              <input type="number" class="form-control form-control-lg" 
              v-model="cantidad3" v-on:keyup="convertirMasa"
              id="cantidad3"  placeholder="Ingrese el dato">
           </div>            
   </div>
        </div>

        <div class="row">
            <div class="col-lg 6">
               <div class="form-group">
                   <label for="tengo3">Tengo</label>
                   <select class="form-select form-select-lg" id="tengo3" v-model="tengo3" 
                   v-on:change="convertirMasa">
                   <option v-for="(masas, index) in masa" v-bind:key="index">
                       {{masas}}
                   </option>
                
                   </select>
               </div>
            </div>
            <div class="col-lg-6">
                 <div class="form-group">
                   <label for="quiero3">Quiero</label>
                   <select class="form-select form-select-lg" id="quiero3" v-model="quiero3"
                   v-on:change="convertirMasa">
                    <option v-for="(masas, index) in masa" v-bind:key="index">
                  {{ masas }} 
                    </option>
                   </select>
               </div>
            </div>
        </div>
    </div>
     <div class="text-center pt-3">
            <h5>
                <span class="badge alert-success">{{cantidad3}} {{tengo3}} </span>
                <span class="badge alert-dark">SON</span>
                <span class="badge alert-success">{{total3}} {{quiero3}} </span>
            </h5>
        </div>

<!-- CONVEROSR DE TIEMPO -->

 
         <div class="container">
        <div class="row">
            <h3 class="long pt-4">TIEMPO</h3>
            <div class="col-lg-12">
            <div class="mb-3">
              <label for="cantidad4" class="form-label">Ingrese el dato</label>
              <input type="number" class="form-control form-control-lg" 
              v-model="cantidad4" v-on:keyup="convertirTiempo"
              id="cantidad4"  placeholder="Ingrese el dato">
           </div>            
   </div>
        </div>

        <div class="row">
            <div class="col-lg 6">
               <div class="form-group">
                   <label for="tengo4">Tengo</label>
                   <select class="form-select form-select-lg" id="tengo4" v-model="tengo4" 
                   v-on:change="convertirTiempo">
                   <option v-for="(tiempox, index) in tiempo" v-bind:key="index">
                       {{tiempox}}
                   </option>
                
                   </select>
               </div>
            </div>
            <div class="col-lg-6">
                 <div class="form-group">
                   <label for="quiero4">Quiero</label>
                   <select class="form-select form-select-lg" id="quiero4" v-model="quiero4"
                   v-on:change="convertirTiempo">
                    <option v-for="(tiempox, index) in tiempo" v-bind:key="index">
                  {{ tiempox }} 
                    </option>
                   </select>
               </div>
            </div>
        </div>
    </div>
     <div class="text-center pt-3">
            <h5>
                <span class="badge alert-success">{{cantidad4}} {{tengo4}} </span>
                <span class="badge alert-dark">SON</span>
                <span class="badge alert-success">{{total4}} {{quiero4}} </span>
            </h5>
        </div>

<!-- CONVERSOR DE UNIDADES DE ALMACENAMIENTO         -->

         <div class="container">
        <div class="row">
            <h3 class="long pt-4">ALMACENAMIENTO</h3>
            <div class="col-lg-12">
            <div class="mb-3">
              <label for="cantidad5" class="form-label">Ingrese el dato</label>
              <input type="number" class="form-control form-control-lg" 
              v-model="cantidad5" v-on:keyup="convertirUnidades"
              id="cantidad5"  placeholder="Ingrese el dato">
           </div>            
   </div>
        </div>

        <div class="row">
            <div class="col-lg 6">
               <div class="form-group">
                   <label for="tengo5">Tengo</label>
                   <select class="form-select form-select-lg" id="tengo5" v-model="tengo5" 
                   v-on:change="convertirUnidades">
                   <option v-for="(unidadx, index) in almacen" v-bind:key="index">
                       {{unidadx}}
                   </option>
                
                   </select>
               </div>
            </div>
            <div class="col-lg-6">
                 <div class="form-group">
                   <label for="quiero5">Quiero</label>
                   <select class="form-select form-select-lg" id="quiero5" v-model="quiero5"
                   v-on:change="convertirUnidades">
                    <option v-for="(unidadx, index) in almacen" v-bind:key="index">
                  {{ unidadx }} 
                    </option>
                   </select>
               </div>
            </div>
        </div>
    </div>
     <div class="text-center pt-3">
            <h5>
                <span class="badge alert-success">{{cantidad5}} {{tengo5}} </span>
                <span class="badge alert-dark">SON</span>
                <span class="badge alert-success">{{total5}} {{quiero5}} </span>
            </h5>
        </div>

</template>

// CODIGO JAVASCRIPT

<script>
   export default {
    data(){
        return{
            monedas: ['USD', 'EUR', 'LIBRA'],
            cantidad: 0,
            tengo: 'USD',
            quiero: 'EUR',
            total: 0,

            medidas: ['Centimetros', 'Metros', 'Kilometros', 'Milimetros'],
            cantidad2: 0,
            tengo2: 'Centimetros',
            quiero2: 'Metros',
            total2: 0,

            masa: ['Kilogramos', 'Hectogramos', 'Decagramos', 'Gramos', 'Decigramos', 'Centigramos', 'Miligramos'],
            cantidad3: 0,
            tengo3: 'Kilogramos',
            quiero3: 'Gramos',
            total3: 0,

            tiempo: ['Segundos', 'Minutos', 'Horas', 'Días', 'Años'],
            cantidad4: 0,
            tengo4: 'Minutos',
            quiero4: 'Horas',
            total4: 0,

            almacen: ['Gigabytes', 'Terabytes', 'Megabytes', 'Kilobytes'],
            cantidad5: 0,
            tengo5: 'Gigabytes',
            quiero5: 'Megabytes',
            total5:  0

        }
    },
    methods:{
        // ESTRUCTURA IF DEL CONVERSOR DE MONEDAS, LONGITUD, MASA....
         
              convertirUnidades(){
         switch(this.tengo5){
             case 'Gigabytes':
                 if(this.quiero5 === 'Gigabytes'){
                     this.total5 = this.cantidad5
                 }
                 if(this.quiero5 === 'Megabytes'){
                     this.total5 = this.cantidad5 * (1024/1)
                 }
                 if(this.quiero5 === 'Terabytes'){
                     this.total5 = this.cantidad5 * (1/1024)
                 }
                 if(this.quiero5 === 'Kilobytes'){
                     this.total5 = this.cantidad5 * (1024/1)* (1024/1)
                 }
                 break;
                  case 'Megabytes':
                 if(this.quiero5 === 'Megabytes'){
                     this.total5 = this.cantidad5
                 }
                 if(this.quiero5 === 'Gigabytes'){
                     this.total5 = this.cantidad5 * (1/1024)
                 }
                 if(this.quiero5 === 'Terabytes'){
                     this.total5 = this.cantidad5 * (1/1024)* (1/1024)
                 }
                 if(this.quiero5 === 'Kilobytes'){
                     this.total5 = this.cantidad5 * (1024/1)
                 }
                 break;
                    case 'Terabytes':
                 if(this.quiero5 === 'Terabytes'){
                     this.total5 = this.cantidad5
                 }
                 if(this.quiero5 === 'Gigabytes'){
                     this.total5 = this.cantidad5 * (1024/1)* (1024/1)* (1024/1)
                 }
                 if(this.quiero5 === 'Megabytes'){
                     this.total5 = this.cantidad5 * (1024/1)* (1024/1)
                 }
                 if(this.quiero5 === 'Kilobytes'){
                     this.total5 = this.cantidad5 * (1024/1)* (1024/1)* (1024/1)
                 }
                 break;
                    case 'Kilobytes':
                 if(this.quiero5 === 'Kilobytes'){
                     this.total5 = this.cantidad5
                 }
                 if(this.quiero5 === 'Gigabytes'){
                     this.total5 = this.cantidad5 * (1/1024)* (1/1024)
                 }
                 if(this.quiero5 === 'Megabytes'){
                     this.total5 = this.cantidad5 * (1/1024)
                 }
                 if(this.quiero5 === 'Terabytes'){
                     this.total5 = this.cantidad5 * (1/1024)* (1/1024)* (1/1024)
                 }
                 break;
                 } },
            
            convertirTiempo(){
         switch(this.tengo4){
             case 'Minutos':
                 if(this.quiero4 === 'Minutos'){
                     this.total4 = this.cantidad4
                 }
                 if(this.quiero4 === 'Segundos'){
                     this.total4 = this.cantidad4 * 60 / 1
                 }
                 if(this.quiero4 === 'Horas'){
                     this.total4 = this.cantidad4 * 1 /60
                 }
                 if(this.quiero4 === 'Días'){
                     this.total4 = this.cantidad4 * 1 / 1440
                 }
                 if(this.quiero4 === 'Años'){
                     this.total4 = this.cantidad4 * 1 /60 * 1 /24 * 1/365
                 }
                 break;
                
                case 'Horas':
                 if(this.quiero4 === 'Horas'){
                     this.total4 = this.cantidad4
                 }
                 if(this.quiero4 === 'Segundos'){
                     this.total4 = this.cantidad4 * 3600 /1
                 }
                 if(this.quiero4 === 'Minutos'){
                     this.total4 = this.cantidad4 * 60 /1
                 }
                 if(this.quiero4 === 'Días'){
                     this.total4 = this.cantidad4 * 1 /24
                 }
                 if(this.quiero4 === 'Años'){
                     this.total4 = this.cantidad4 * (1 / 24) * (1/365)
                 }
                 break;
                   case 'Segundos':
                 if(this.quiero4 === 'Segundos'){
                     this.total4 = this.cantidad4
                 }
                 if(this.quiero4 === 'Horas'){
                     this.total4 = this.cantidad4 * (1/3600)
                 }
                 if(this.quiero4 === 'Minutos'){
                     this.total4 = this.cantidad4 * (1/60)
                 }
                 if(this.quiero4 === 'Días'){
                     this.total4 = this.cantidad4 * (1/86400)
                 }
                 if(this.quiero4 === 'Años'){
                     this.total4 = this.cantidad4 * (1/60) * (1/60) * (1/240)* (1/365)
                 }
                break;
                  case 'Días':
                 if(this.quiero4 === 'Días'){
                     this.total4 = this.cantidad4
                 }
                 if(this.quiero4 === 'Segundos'){
                     this.total4 = this.cantidad4 * (24/1)
                 }
                 if(this.quiero4 === 'Minutos'){
                     this.total4 = this.cantidad4 * (1440/1)
                 }
                 if(this.quiero4 === 'Horas'){
                     this.total4 = this.cantidad4 * (24/1)
                 }
                 if(this.quiero4 === 'Años'){
                     this.total4 = this.cantidad4 * (1/365)
                 }
                 break;
                   case 'Años':
                 if(this.quiero4 === 'A{os'){
                     this.total4 = this.cantidad4
                 }
                 if(this.quiero4 === 'Segundos'){
                     this.total4 = this.cantidad4 * (365/1)* (24/1)* (3600/1)
                 }
                 if(this.quiero4 === 'Minutos'){
                     this.total4 = this.cantidad4 * (365/1)* (24/1)* (60/1)
                 }
                 if(this.quiero4 === 'Días'){
                     this.total4 = this.cantidad4 * (365/1)
                 }
                 if(this.quiero4 === 'Horas'){
                     this.total4 = this.cantidad4 * (365/1)* (24/1) 
                 }
              
         }    
         },
         
         
         convertirMasa(){
         switch(this.tengo3){
             case 'Kilogramos':
                 if(this.quiero3 === 'Kilogramos'){
                     this.total3 = this.cantidad3
                 }
                 if(this.quiero3 === 'Hectogramos'){
                     this.total3 = this.cantidad3 * 10 / 1
                 }
                 if(this.quiero3 === 'Decagramos'){
                     this.total3 = this.cantidad3 * 100.0 / 1
                 }
                 if(this.quiero3 === 'Gramos'){
                     this.total3 = this.cantidad3 * 1000 / 1
                 }
                 if(this.quiero3 === 'Decigramos'){
                     this.total3 = this.cantidad3 * 10000 / 1
                 }
                 if(this.quiero3 === 'Centigramos'){
                     this.total3 = this.cantidad3 * 100000 /1
                 }
                 if(this.quiero3 === 'Miligramos'){
                     this.total3 = this.cantidad3 * 1000000 /1
                 }
                 break;
                 case 'Hectogramos':
                 if(this.quiero3 === 'Hectogramos'){
                     this.total3 = this.cantidad3
                 }
                 if(this.quiero3 === 'Kilogramos'){
                     this.total3 = this.cantidad3 *1.0 /10.0
                 }
                 if(this.quiero3 === 'Decagramos'){
                     this.total3 = this.cantidad3 * 10 /1
                 }
                 if(this.quiero3 === 'Gramos'){
                     this.total3 = this.cantidad3 * 100 /1
                 }
                 if(this.quiero3 === 'Decigramos'){
                     this.total3 = this.cantidad3 * 1000 /1
                 }
                 if(this.quiero3 === 'Centigramos'){
                     this.total3 = this.cantidad3 * 10000 /1
                 }
                 if(this.quiero3 === 'Miligramos'){
                     this.total3 = this.cantidad3 * 100000 /1
                 }
                 break;
                 case 'Gramos':
                 if(this.quiero3 === 'Gramos'){
                     this.total3 = this.cantidad3
                 }
                 if(this.quiero3 === 'Hectogramos'){
                     this.total3 = this.cantidad3 * 1 /100
                 }
                 if(this.quiero3 === 'Decagramos'){
                     this.total3 = this.cantidad3 * 1 / 10
                 }
                 if(this.quiero3 === 'Kilogramos'){
                     this.total3 = this.cantidad3 * 1 / 1000
                 }
                 if(this.quiero3 === 'Decigramos'){
                     this.total3 = this.cantidad3 * 10 /1
                 }
                 if(this.quiero3 === 'Centigramos'){
                     this.total3 = this.cantidad3 * 100 / 1
                 }
                 if(this.quiero3 === 'Miligramos'){
                     this.total3 = this.cantidad3 *1000 /1
                 }
                 break;
         }    
         },





         convertirMedidas(){
        switch(this.tengo2){
            case 'Centimetros':
                if(this.quiero2 === 'Centimetros'){ 
                this.total2 = this.cantidad2
                }
                if(this.quiero2 === 'Metros'){ 
                this.total2 = this.cantidad2 / 100  
                }
                if (this.quiero2 === 'Kilometros'){
                    this.total2 = this.cantidad2 / 100000
                }
                if (this.quiero2 === 'Milimetros'){
                    this.total2 = this.cantidad2 * 10 / 1
                }
                break;
                case 'Metros':
                if(this.quiero2 === 'Metros'){ 
                this.total2 = this.cantidad2
                }
                if(this.quiero2 === 'Centimetros'){ 
                this.total2 = this.cantidad2 * 100 / 1 
                }
                if (this.quiero2 === 'Kilometros'){
                    this.total2 = this.cantidad2 * 1 / 1000
                }
                if (this.quiero2 === 'Milimetros'){
                    this.total2 = this.cantidad2 * 1000 / 1
                }
                break;
                case 'Kilometros':
                if(this.quiero2 === 'Kilometros'){ 
                this.total2 = this.cantidad2
                }
                if(this.quiero2 === 'Metros'){ 
                this.total2 = this.cantidad2 * 1000  / 1  
                }
                if (this.quiero2 === 'Centimetros'){
                    this.total2 = this.cantidad2 * 1000 / 1 *100 / 1
                }
                if (this.quiero2 === 'Milimetros'){
                    this.total2 = this.cantidad2 * 1000 / 1 *1000 /1
                }
                break;
         
     }
    },
        convertirMonedas(){
            switch(this.tengo) {
            case 'USD':
                if(this.quiero === 'USD'){
                    this.total = this.cantidad 
                }
                if(this.quiero === 'EUR'){
                    this.total = this.cantidad * 0.88
                }
                if(this.quiero === 'LIBRA'){
                    this.total = this.cantidad * 0.74
                }

             break;

            case 'EUR':
                 if(this.quiero === 'USD'){
                    this.total = this.cantidad * 1.13
                }
                if(this.quiero === 'EUR'){
                    this.total = this.cantidad 
                }
                if(this.quiero === 'LIBRA'){
                    this.total = this.cantidad * 0.83
                }

            break;

            case 'LIBRA':
                if(this.quiero === 'USD'){
                    this.total = this.cantidad * 1.36
                }
                if(this.quiero === 'EUR'){
                    this.total = this.cantidad * 1.20
                }
                if(this.quiero === 'LIBRA'){
                    this.total = this.cantidad 
                }

            break;    
}
        },
        getTotal(valor){
            return Math.round(valor)
        }
    },
     
};
</script>


// CODIGO CSS

<style scoped>
label{
    font-weight: 600;
    font-size: 120%;
}
.badge{
    margin: 2px;
    size: 150%;
}
.money{
    text-align: center;
}
.long{
    text-align: center;
}

</style>