# Trabjo-Final-modulo2
En mi trabajo final las variables principales son : address public propietario;(Guarda la direccion del dueño o de la persona que lo despliega) uint256 public fechaFinal;(indica el tiempo de la subasta) bool public estaActiva(indica si la subasta esta activa o ya finalizo);
/
Cada usuario tiene una oferta guardada en el mapping
/
Variables para la subasta: address public mejorOferente;(la direccion del usuario con la mejor oferta), uint256 public mejorOferta;(El monto mas alto), uint256 public comisionPorc = 2;(Es la comision que se queda el propietario de la subasta 2%)
/
Hay algunos modificadores el cual permite que ciertas funciones solo las pueda ejecutar el dueño
/
La funcion ofertar nos permite el hacer ofertas,que este activo y no haya terminado en caso de que la subasta haya terminado y quiera ofertar nos saldra que subasta finalizada, para mejorar una oferta obligatoriamente debe ser un 5% mas que la anterior oferta, 
/
Si el oferente ya había depositado más ETH del que vale su última oferta válida, le devuelve el exceso, actualiza la mejor oferta y la persona que lo hace y si queda menos de 10 minutos para el cierre de la oferta se lo extiende 10 minutos mas para evitar cierres rapidos}
/
Finalizar subasta: les devuelve el dinero a todos los participantes menos al ganador, se emite el vento de ganador y el monto final, calcula la comision y se lo envia al propietario
/
reembolso parcial: en caso de que el ofertante haya hecho un exceso se le devolvera el exceso ejemplo: ultimaoferta=1 totaldepositado=1.2 eth al llamar a la funcion reembolsarParcial se le devolvera el exceso = 0.2 eht, en palabras sencillas toma el total depositado y resta la ultima oferta  
