<template>
 <form @submit="submitForm">
    <div>
      <h1 for="datosGenerales">CAPTURA DE DATOS PARA EMPRENDIMIENTO</h1>
    </div>
    <div>
      <h2 for="datosGenerales">DATOS GENERALES</h2>
    </div>
    <div>
      <label for="nombreCompania">¿Cuál es el nombre de su emprendimiento/Compañía?</label>
      <input type="text" id="nombreCompania" v-model="formValues.nombreCompania" >
    </div>
    <div>
      <label for="fechaCreacion">¿En qué fecha se fundó su empresa o comenzó su emprendimiento?</label>
      <datepicker v-model="formValues.fechaCreacion" inputFormat="yyyy-MM-dd" format="yyyy-MM-dd" />     
    </div>
    <div>
      <label for="etapaDesarrollo">¿En cuál etapa de desarrollo se encuentra su emprendimiento?</label>
      <select id="etapaDesarrollo" v-model="formValues.etapaDesarrollo" >
        <option value="">Seleccione una etapa</option>
        <option value="1">Etapa de Ideación</option>
        <option value="2">Etapa de Prototipado</option>
        <option value="3">Etapa de Mínimo Producto Viable</option>
        <option value="4">Etapa de Tracción real Inicial</option>
        <option value="5">Etapa de Punto de Equilibrio</option>
        <option value="6">Etapa de Consolidación</option>
        <option value="7">Etapa de Crecimiento</option>
        <option value="8">Etapa de Expansión</option>
      </select>
    </div>
    <div>
      <label for="sector">¿En cuál sector económico se desarrolla su negocio?</label>
      <select id="sector" v-model="formValues.sector" >
        <option value="">Seleccione un sector</option>
        <option value="1">Agropecuario</option>
        <option value="2">Comercio</option>
        <option value="3">Construcción</option>
        <option value="4">Industria</option>
        <option value="5">Medios</option>
        <option value="6">Minería</option>
        <option value="7">Servicios</option>
      </select>
    </div>    
    <div>
      <label for="industria">¿A qué industria pertenece su emprendimiento?</label>
      <select id="industria" v-model="formValues.industria">
        <option value="">Seleccione una industria</option>
        <option value="1">AGRICULTURA VARIOS</option>
        <option value="2">AVÍCOLA</option>
        <option value="3">BANANO</option>
        <option value="4">FLORES</option>
        <option value="5">GANADERÍA Y PORCICULTURA</option>
        <option value="6">PALMA</option>
        <option value="7">PESCA Y CAMARÓN</option>
        <option value="8">AL POR MAYOR</option>
        <option value="9">AL POR MENOR</option>
        <option value="10">COMBUSTIBLE PARA AUTOMOTORES</option>
        <option value="11">CONCESIONARIOS</option>
        <option value="12">PARTES, PIEZAS Y ACCESORIOS PARA VEHÍCULOS</option>
        <option value="13">ACONDICIONAMIENTO Y TERMINACIÓN DE EDIFICIOS</option>
        <option value="14">ACTIVIDADES DE ARQUITECTURA E INGENIERÍA</option>
        <option value="15">CONCESIONES DE TRANSPORTE</option>
        <option value="16">CONSTRUCCIÓN</option>
        <option value="17">INGENIERÍA CIVIL</option>
        <option value="18">PREPARACIÓN DE TERRENO</option>
        <option value="19">HIDROCARBUROS Y SERVICIOS PETROLEROS</option>
        <option value="20">ALIMENTOS</option>
        <option value="21">BEBIDAS</option>
        <option value="22">COSMÉTICOS Y ASEO</option>
        <option value="23">CUERO Y CALZADO</option>
        <option value="24">HIERRO, ACERO Y OTROS METALES</option>
        <option value="25">INDUSTRIA GRAFICA</option>
        <option value="26">MADERA</option>
        <option value="27">MANUFACTURAS VARIAS</option>  
        <option value="28">MAQUINARIA Y EQUIPO</option>  
        <option value="29">MUEBLES Y ACCESORIOS</option>  
        <option value="30">PLÁSTICOS Y CAUCHO</option>  
        <option value="31">PRODUCTOS PARA LA CONSTRUCCIÓN</option>  
        <option value="32">QUÍMICOS</option>                                                                                
        <option value="33">TABACO</option>
        <option value="34">TEXTIL, CONFECCIÓN, DISEÑO Y MODA</option>
        <option value="35">VEHÍCULOS Y PARTES</option>
        <option value="36">VIDRIO Y PRODUCTOS DE VIDRIO</option>
        <option value="37">CINE Y VIDEO</option>
        <option value="38">PERIÓDICOS, REVISTAS Y OTROS</option>
        <option value="39">TELEVISIÓN Y RADIO</option>
        <option value="40">ACTIVIDADES DE JUEGOS DE AZAR Y APUESTAS</option>
        <option value="41">CAJAS DE COMPENSACIÓN</option>
        <option value="42">CORREO</option>  
        <option value="43">EDUCACIÓN</option>  
        <option value="44">ENERGÍA ELÉCTRICA, BIENES Y SERVICIOS CONEXOS</option>  
        <option value="45">HOTELES</option>  
        <option value="46">OTROS SERVICIOS</option>  
        <option value="47">RESTAURANTES</option>  
        <option value="48">SALUD</option>  
        <option value="49">SERVICIOS PÚBLICOS</option>  
        <option value="50">SERVICIOS TERCERIZADOS A DISTANCIA (BPO&O)</option>  
        <option value="51">SOCIEDADES INVERSORAS</option>  
        <option value="52">TÉCNICOS Y PROFESIONALES</option>  
        <option value="53">TURISMO</option>  
        <option value="54">VIGILANCIA Y SEGURIDAD</option>  
        <option value="55">TELECOMUNICACIONES</option>
        <option value="56">TI SOFTWARE & SERVICIOS DE TECNOLOGÍAS DE LA INFORMACIÓN</option>
        <option value="57">AÉREO</option>
        <option value="58">MARÍTIMO Y FLUVIAL</option>
        <option value="59">OPERADORES, AGENTES Y TERMINALES</option>
        <option value="60">TERRESTRE</option>
      </select>
    </div>
    <div>
      <h2 for="situacionPrevia">SITUACIÓN PREVIA</h2>
    </div>    
    <div>
      <label for="inversionPrevia">¿La Compañía ha levantado fondos de capital previamente?</label>
      <select id="inversionPrevia" v-model="formValues.inversionPrevia" >
        <option value="">Seleccione</option>
        <option value="1">SI</option>
        <option value="2">NO</option>
      </select>
    </div>   
    <div>
      <label for="alistamientoMercado">¿El Producto Mínimo Viable (MVP) está listo para ser lanzado al mercado? 
(A niveles tecnológico y de propuesta de valor adecuados)</label>
      <select id="alistamientoMercado" v-model="formValues.alistamientoMercado" >
        <option value="">Seleccione</option>
        <option value="1">SI</option>
        <option value="2">NO</option>
      </select>
    </div> 
    <div>
      <h2 for="experiencia">EXPERIENCIA</h2>
    </div> 
    <div>
      <label for="experienciaLaboral">Experiencia de los Emprendedores ¿Han trabajado en una gran corporación?</label>
      <select id="experienciaLaboral" v-model="formValues.experienciaLaboral" >
        <option value="">Seleccione</option>
        <option value="1">SI</option>
        <option value="2">NO</option>
      </select>
    </div>  
    <div>
      <label for="experienciaEmprendedores">¿Han emprendido previamente?</label>
      <select id="experienciaEmprendedores" v-model="formValues.experienciaEmprendedores" >
        <option value="">Seleccione</option>
        <option value="1">SI</option>
        <option value="2">NO</option>
      </select>
    </div>  
    <div>
      <label for="experienciaTema">¿Tienen experiencia en el tema  en el mercado o en la industria?</label>
      <select id="experienciaTema" v-model="formValues.experienciaTema" >
        <option value="">Seleccione</option>
        <option value="1">SI</option>
        <option value="2">NO</option>
      </select>
    </div>  
    <div>
      <label for="tipoExperiencia">¿En qué tienen experiencia afin al emprendimiento?</label>
      <select id="tipoExperiencia" v-model="formValues.tipoExperiencia" >
        <option value="">Seleccione</option>
        <option value="M">Mercado</option>
        <option value="S">Sector</option>
        <option value="I">Industria</option>
        <option value="T">Tecnología</option>
        <option value="N">Ninguna</option>
      </select>
    </div>
    <label for="equipo">¿Cuál es la trayectoria del equipo emprendedor?</label>
    <section>
    <div v-for="miembro in formValues.equipo" :key="miembro.id">
       <input type="text" v-model="miembro.nombre" placeholder="Nombre">
       <input type="text" v-model="miembro.tiempo" placeholder="Tiempo en años">
       <select id="trayectoria" v-model="miembro.trayectoria" >
        <option value="">Trayectoria</option>
        <option value="1">Laboral general</option>
        <option value="2">Laboral relacionada</option>
        <option value="3">Academica</option>
       </select>
    </div>      
    <button type="button" @click="AddField">
      Agregar miembro
    </button>
    </section>
    <div>
      <label for="experienciaEquipo">¿Tienen experiencia en el tema  en el mercado o en la industria?</label>
      <select id="experienciaEquipo" v-model="formValues.experienciaEquipo" >
        <option value="">Seleccione</option>
        <option value="1">SI</option>
        <option value="2">NO</option>
      </select>
    </div> 
    <div>
      <label for="experienciaEcosistema">¿Han participado en aceleradoras, incubadoras, o en espacios de coworking? </label>
      <select id="experienciaEcosistema" v-model="formValues.experienciaEcosistema" >
        <option value="">Seleccione</option>
        <option value="1">SI</option>
        <option value="2">NO</option>
      </select>
    </div> 
    <div>
      <h2 for="capacidadGestion">CAPACIDAD DE GESTIÓN</h2>
    </div> 
    <div>
      <label for="existeEquipoGestor">¿Ya existe un equipo gestor?</label>
      <select id="existeEquipoGestor" v-model="formValues.existeEquipoGestor" >
        <option value="">Seleccione</option>
        <option value="1">SI</option>
        <option value="2">NO</option>
      </select>
    </div> 
    <div>
      <h2 for="fundadoresInvolucrados">FUNDADORES INVOLUCRADOS</h2>
    </div>     
    <div>
      <label for="numeroMiembros">Número de Miembros del equipo trabajando tiempo completo en el emprendimiento</label>
      <input type="text" id="numeroMiembros" v-model="formValues.numeroMiembros" >
    </div>
    <div>
      <h2 for="participacionFundadores">PARTICIPACIÓN FUNDADORES</h2>
    </div>
    <div>
      <label for="paquetesAccionarios">¿Tienen planeado otorgar paquetes accionarios para los miembros del equipo clave? </label>
      <select id="paquetesAccionarios" v-model="formValues.paquetesAccionarios">
        <option value="">Seleccione</option>
        <option value="1">SI</option>
        <option value="2">NO</option>
      </select>
    </div>
    <div>
      <label for="numeroMiembrosConPaquetes">Número de Miembros del equipo con paquetes accionarios</label>
      <input type="text" id="numeroMiembrosConPaquetes" v-model="formValues.numeroMiembrosConPaquetes" >
    </div>
    <div>
      <button>Enviar</button>
    </div>  
    <div>
      {{ this.formValues.respuestaRegistro }}
    </div>     
 </form>
</template>

<script>

import Datepicker from 'vue3-datepicker'


export default {
  name: 'App',
  data(){
    return{
        formValues:{
          nombreCompania: '', 
          fechaCreacion: '', 
          etapaDesarrollo: '', 
          sector: '', 
          industria: '', 
          inversionPrevia: '', 
          alistamientoMercado: '', 
          experienciaLaboral: '',
          experienciaEmprendedores: '', 
          experienciaTema: '', 
          tipoExperiencia: '', 
          equipo: [{ nombre: '', tiempo: '', trayectoria: '' }], 
          experienciaEquipo: '', 
          experienciaEcosistema: '', 
          existeEquipoGestor: '', 
          numeroMiembros: '', 
          paquetesAccionarios: '', 
          numeroMiembrosConPaquetes: '', 
          respuestaRegistro: ''
        }
    }
  },
  components: {
    Datepicker
  }, 
  methods:{
    submitForm(event){
      event.preventDefault()
      console.log("form values", this.formValues)
      console.log(this.formValues.fechaCreacion.toISOString())
      fetch('http://52.15.96.25:8080/v1/graphql',  {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify({ query: 'mutation MyMutation { \
                  insert_kms_registrations( \
                    objects: {company_name: "' +  this.formValues.nombreCompania + '",  \
                        creation_date: "' + this.formValues.fechaCreacion.toISOString() + '", \
                        development_stage: "' + this.formValues.etapaDesarrollo + '", \
                        sector: "' + this.formValues.sector + '", \
                        industry: "' + this.formValues.industria + '", \
                        previous_investment: "' + this.formValues.inversionPrevia + '", \
                        market_enlistment: "' + this.formValues.alistamientoMercado + '", \
                        work_experience: "' + this.formValues.experienciaLaboral + '", \
                        entrepreneurs_experience: "' + this.formValues.experienciaEmprendedores + '", \
                        subject_experience: "' + this.formValues.experienciaTema + '", \
                        experience_type: "' + this.formValues.tipoExperiencia + '", \
                        experience_team: "' + this.formValues.experienciaEquipo + '", \
                        ecosystem_experience : "' + this.formValues.experienciaEcosistema + '", \
                        is_there_management_team  : "' + this.formValues.existeEquipoGestor  + '", \
                        members_number: "' + this.formValues.numeroMiembros  + '", \
                        stock_packages: "' + this.formValues.paquetesAccionarios  + '", \
                        number_of_members_with_packages: "' + this.formValues.numeroMiembrosConPaquetes  + '", \
                         }) { \
                    returning {  \
                      id   \
                    }  \
                  }   \
                }' }),
              })
      this.formValues.respuestaRegistro = "Se hizo el registro satisfactoriamente"
    }, 
    AddField: function () {
      this.formValues.equipo.push({ nombre: '', tiempo: '', trayectoria: '' });
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: #2c3e50;
  margin-top: 60px;
}
.underline {
  text-decoration: underline;
}
.promoted {
  font-style: italic;
}
.new {
  color: olivedrab;
}
.sold-out {
  color: red;
}
*, *:before, *:after {
  box-sizing: border-box;
}
h2, h1 {
  font-weight: bold;
  display: flex;
  color: #3F51B5;
  margin-bottom: 5px;
}
label {
  display: flex;
  color: #2678bb;
  margin-bottom: 5px;
}
input + label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}
input[type='text'],
textarea,
select {
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.42857143;
  color: #555;
  background-color: #fff;
  background-image: none;
  border:0; 
  border-bottom:2px solid rgb(92, 103, 138); 
  margin:9px 0;
}
button {

  /* remove default behavior */
  appearance:none;
  -webkit-appearance:none;

  /* usual styles */
  padding:10px;
  border:none;
  background-color:#3F51B5;
  color:#fff;
  font-weight:600;
  border-radius:5px;
  margin:10px 0;

}
</style>
