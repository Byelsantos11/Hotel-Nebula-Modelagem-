//Quartos com vista para o mar e banheira:

db.quartos.find({
  "comodidades": { $all: ["vista para o mar", "banheira"] }
});

// Buscar todos os quartos do tipo "Suíte Master" para verificar o inventário:
db.quartos.find({
  "tipo": "Suíte Master"
});

// Localizar todos os consumos de "Frigobar" dentro das hospedagens para reposição de estoque:

db.hospedagens.find({
  "consumo.categoria": "Frigobar"
});

// Identificar hóspedes fiéis (que possuem mais de uma reserva no sistema):

db.reservas.aggregate([
  { $group: { _id: "$hospede_id", total_reservas: { $sum: 1 } } },
  { $match: { total_reservas: { $gt: 1 } } }
]);



