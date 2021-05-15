<template>
  <pre>
    {{ JSON.stringify(formValues, null, 2) }}
  </pre>
 <form @submit="submitForm">
    <div>
      <label for="datosGenerales">Datos Generales</label>
    </div>
    <div>
      <label for="nombreCompania">¿Cuál es el nombre de su emprendimiento/Compañía?</label>
      <input type="text" id="nombreCompania" v-model="formValues.nombreCompania" >
    </div>
    <div>
      <label for="fechaCreacion">¿En qué fecha se fundó su empresa o comenzó su emprendimiento?</label>
      <input type="text" id="fechaCreacion" >
    </div>
    <div>
      <label for="etapaDesarrollo">¿En cuál etapa de desarrollo se encuentra su emprendimiento?</label>
      <select id="etapaDesarrollo">
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
      <select id="sector">
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
      <select id="industria">
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
      <label for="situacionPrevia">Situación previa</label>
    </div>    
    <div>
      <label for="inversionPrevia">¿La Compañía ha levantado fondos de capital previamente?</label>
      <select id="inversionPrevia">
        <option value="">Seleccione</option>
        <option value="1">SI</option>
        <option value="2">NO</option>
      </select>
    </div>   
    <div>
      <label for="alistamientoMercado">¿El Producto Mínimo Viable (MVP) está listo para ser lanzado al mercado? 
(A niveles tecnológico y de propuesta de valor adecuados)</label>
      <select id="alistamientoMercado">
        <option value="">Seleccione</option>
        <option value="1">SI</option>
        <option value="2">NO</option>
      </select>
    </div> 
    <div>
      <label for="experiencia">Experiencia</label>
    </div> 
    <div>
      <label for="experienciaLaboral">Experiencia de los Emprendedores ¿Han trabajado en una gran corporación?</label>
      <select id="experienciaLaboral">
        <option value="">Seleccione</option>
        <option value="1">SI</option>
        <option value="2">NO</option>
      </select>
    </div>  
    <div>
      <label for="experienciaEmprendedores">¿Han emprendido previamente?</label>
      <select id="experienciaEmprendedores">
        <option value="">Seleccione</option>
        <option value="1">SI</option>
        <option value="2">NO</option>
      </select>
    </div>  
    <div>
      <label for="experienciaTema">¿Tienen experiencia en el tema  en el mercado o en la industria?</label>
      <select id="experienciaTema">
        <option value="">Seleccione</option>
        <option value="1">SI</option>
        <option value="2">NO</option>
      </select>
    </div>  
    <div>
      <label for="tipoExperiencia">¿En qué tienen experiencia afin al emprendimiento?</label>
      <select id="tipoExperiencia">
        <option value="">Seleccione</option>
        <option value="M">Mercado</option>
        <option value="S">Sector</option>
        <option value="I">Industria</option>
        <option value="T">Tecnología</option>
        <option value="N">Ninguna</option>
      </select>
    </div>      
    <div>
      <label for="experienciaEquipo">¿Tienen experiencia en el tema  en el mercado o en la industria?</label>
      <select id="experienciaEquipo">
        <option value="">Seleccione</option>
        <option value="1">SI</option>
        <option value="2">NO</option>
      </select>
    </div> 
    <div>
      <label for="experienciaEcosistema">¿Han participado en aceleradoras, incubadoras, o en espacios de coworking? </label>
      <select id="experienciaEcosistema">
        <option value="">Seleccione</option>
        <option value="1">SI</option>
        <option value="2">NO</option>
      </select>
    </div> 
    <div>
      <label for="capacidadGestion">Capacidad de Gestion</label>
    </div> 
    <div>
      <label for="existeEquipoGestor">¿Ya existe un equipo gestor?</label>
      <select id="existeEquipoGestor">
        <option value="">Seleccione</option>
        <option value="1">SI</option>
        <option value="2">NO</option>
      </select>
    </div> 
    <div>
      <label for="fundadoresInvolucrados">Fundadores Involucrados</label>
    </div>     
    <div>
      <label for="numeroMiembros">Número de Miembros del equipo trabajando tiempo completo en el emprendimiento</label>
      <input type="text" id="numeroMiembros" >
    </div>
    <div>
      <label for="participacionFundadores">Participación Fundadores</label>
    </div>
    <div>
      <label for="paquetesAccionarios">¿Tienen planeado otorgar paquetes accionarios para los miembros del equipo clave? </label>
      <select id="paquetesAccionarios">
        <option value="">Seleccione</option>
        <option value="1">SI</option>
        <option value="2">NO</option>
      </select>
    </div>
    <div>
      <label for="numeroMiembrosConPaquetes">Número de Miembros del equipo trabajando tiempo completo en el emprendimiento</label>
      <input type="text" id="numeroMiembrosConPaquetes" >
    </div>
    <div>
      <button>Enviar</button>
    </div>     
 </form>
</template>

<script>


export default {
  name: 'App',
  data(){
    return{
        formValues:{
          nombreCompania: ''
        }
    }
  },
  components: {
    
  }, 
  methods:{
    submitForm(event){
      event.preventDefault()
      console.log("form values", this.formValues)
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
label {
  font-weight: bold;
  display: flex;
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
  border: 1px solid #ccc;
  border-radius: 4px;
}
</style>
