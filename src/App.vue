<template>
  <div class="employee-list-container">
    <h2>Liste des Employés</h2>
    <ol class="employee-list">
      <li v-for="employee in employees" :key="employee.id" class="employee-item">
        {{ employee.name }}
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  name: 'EmployeeList',
  data() {
    return {
      employees: [
        { id: 1, name: 'Aida patra' },
        { id: 2, name: 'Ouzin keita' },
        { id: 3, name: 'Chams aidara' },
        { id: 4, name: 'Diana bouli' },
        { id: 5, name: 'Eve marichou' }
      ]
    };
  }
};
</script>

<style scoped>
/* Conteneur principal */
.employee-list-container {
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
  background-color: #1d1f20;
  border-radius: 12px;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.5);
  text-align: center;
  font-family: 'Arial', sans-serif;
  color: #fff;
  background-image: radial-gradient(circle, #ff00ff, #ff4500, #ff00ff, #ff4500);
}

/* Titre */
h2 {
  font-size: 32px;
  margin-bottom: 20px;
  color: #fff;
  text-transform: uppercase;
  letter-spacing: 2px;
}

/* Liste ordonnée */
.employee-list {
  list-style-type: decimal;
  padding-left: 0;
  margin: 0;
}

/* Éléments de la liste */
.employee-item {
  font-size: 24px;
  margin: 10px 0;
  padding: 10px;
  transition: transform 0.2s ease, background-color 0.2s ease;
  cursor: pointer;
  background-color: #282828;
  border-radius: 8px;
}

/* Effet de survol */
.employee-item:hover {
  background-color: #ff00ff;
  transform: scale(1.05);
  color: #000;
}
</style>
