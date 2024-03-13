
<template>

  <v-main>
    <link
      rel="stylesheet"
      href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200"
    />

    <div>
      <main class="table" id="customers_table">
        <section class="table__header">
          <img src="../assets/Profile.png" alt="" />
          <h1>
            Class Adviser’s Name <br />
            <p>Section</p>
          </h1>
          <div class="input-group">
            <span class="material-symbols-outlined">search</span>
            <input type="search" placeholder="Search Data..." />
          </div>
          <div class="export__file">
            <label
              for="export-file"
              class="export__file-btn"
              title="Export File"
            ></label>
            <input type="checkbox" id="export-file" />
            <div class="export__file-options">
              <label>Export As &nbsp; &#10140;</label>
              <label for="export-file" id="toPDF"
                >PDF <img src="../assets/Profile.png" alt=""
              /></label>
              <label for="export-file" id="toJSON"
                >JSON <img src="../assets//json.png" alt=""
              /></label>
              <label for="export-file" id="toCSV"
                >CSV <img src="../assets/csv.png" alt=""
              /></label>
              <label for="export-file" id="toEXCEL"
                >EXCEL <img src="../assets/excel.png" alt=""
              /></label>
            </div>
          </div>
        </section>
        <section class="table__body">
          <table>
            <thead>
              <tr>
                <th>S.NO <span class="icon-arrow">&UpArrow;</span></th>
                <th>Name</th>
                <th>LRN</th>
                <th>Grade level</th>
                <th>Section</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="(student, index) in students" :key="index">
                <td>{{ index + 1 }}</td>
                <td>
                  <img src="../assets/Profile.png" alt="" />{{ student.name }}
                </td>
                <td>{{ student.lrn }}</td>
                <td>{{ student.gradeLevel }}</td>
                <td>{{ student.section }}</td>
              </tr>
            </tbody>
          </table>
        </section>
      </main>
    </div>
  </v-main>
</template>


<script>


export default {
  data() {
    return {
      students: [
        {
          name: "Zinzu Chan Lee",
          lrn: "12331123321",
          gradeLevel: "1",
          section: "OAK",
        },
        {
          name: "Zinzu Chan Lee",
          lrn: "12331123321",
          gradeLevel: "1",
          section: "OAK",
        },
        {
          name: "Zinzu Chan Lee",
          lrn: "12331123321",
          gradeLevel: "1",
          section: "OAK",
        },
        {
          name: "Zinzu Chan Lee",
          lrn: "12331123321",
          gradeLevel: "1",
          section: "OAK",
        },
        { name: "Naruto", lrn: "12331123321", gradeLevel: "1", section: "OAK" },
        {
          name: "Zinzu Chan Lee",
          lrn: "12331123321",
          gradeLevel: "1",
          section: "OAK",
        },
        {
          name: "Zinzu Chan Lee",
          lrn: "12331123321",
          gradeLevel: "1",
          section: "OAK",
        },
        {
          name: "Zinzu Chan Lee",
          lrn: "12331123321",
          gradeLevel: "1",
          section: "OAK",
        },
        {
          name: "Zinzu Chan Lee",
          lrn: "12331123321",
          gradeLevel: "1",
          section: "OAK",
        },
        {
          name: "Zinzu Chan Lee",
          lrn: "12331123321",
          gradeLevel: "1",
          section: "OAK",
        },
        {
          name: "Zinzu Chan Lee",
          lrn: "12331123321",
          gradeLevel: "1",
          section: "OAK",
        },
        {
          name: "Joshua Padilia",
          lrn: "12331123321",
          gradeLevel: "1",
          section: "OAK",
        },
        {
          name: "Ramon Chan Lee",
          lrn: "12331123321",
          gradeLevel: "1",
          section: "OAK",
        },
        {
          name: "Zinzu Chan Lee",
          lrn: "12331123321",
          gradeLevel: "1",
          section: "OAK",
        },
      ],
    };
  },
};




</script>





<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap");

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}

@media print {
  .table,
  .table__body {
    overflow: visible;
    height: auto !important;
    width: auto !important;
  }
}

body {
  min-height: 100vh;
  /* background: url(images/html_table.jpg) center / cover; */
  display: flex;
  justify-content: center;
  align-items: center;
}

main.table {
  width: 100vw;
  height: 100vh;
  background-color: rgba(255, 255, 255, 0.333);
  overflow: hidden;
}

.table__header h1 {
  margin-right: 100px;
}

.table__header p {
  font-size: 15px;
}

.table__header img {
  width: 100px;
  height: 100px;
}

.table__header {
  width: 100%;
  height: 10%;
  background-color: rgb(255, 255, 255);
  padding: 0.8rem 5rem;
  margin-top: 3rem;
  margin-bottom: 30px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.table__header .input-group {
  width: 30%;
  height: 100%;
  background-color: rgb(238, 238, 238);
  padding: 0 0.8rem;
  border-radius: 2rem;

  display: flex;
  justify-content: center;
  align-items: center;

  transition: 0.2s;
}

.table__header .input-group input {
  width: 100%;
  padding: 0 0.5rem 0 0.3rem;
  background-color: transparent;
  border: none;
  outline: none;
}

.table__body::-webkit-scrollbar {
  width: 0.5rem;
  height: 0.5rem;
}

.table__body::-webkit-scrollbar-thumb {
  border-radius: 0.5rem;
  background-color: #0004;
  visibility: hidden;
}

.table__body:hover::-webkit-scrollbar-thumb {
  visibility: visible;
}

.table__body {
  width: 102%;
  max-height: calc(89% - 1.6rem);
  background-color: #fffb;
  overflow: auto;
  overflow: overlay;
}

table {
  width: 100%;
}

td img {
  width: 40px;
  height: 40px;
  margin-right: 0.5rem;
  vertical-align: middle;
  margin-right: 20px;
}

table,
th,
td {
  border-collapse: collapse;
  padding: 1rem;
  padding-right: 5px;
  text-align: left;
  background-color: #fffb;
}

thead th {
  position: sticky;
  background-color: #fff;
  font-size: 10px;
  top: 0;
  left: 0;
  cursor: pointer;
  text-transform: capitalize;
  padding-right: 5px;
}

tbody tr:nth-child(even) {
  background-color: #0000000b;
}

tbody tr {
  --delay: 0.1s;
  transition: 0.5s ease-in-out var(--delay), background-color 0s;
}

tbody tr.hide {
  opacity: 0;
  transform: translateX(100%);
}

tbody tr:hover {
  background-color: #b1b1b182 !important;
}

tbody tr td,
tbody tr td p,
tbody tr td img {
  transition: 0.2s ease-in-out;
}

tbody tr.hide td,
tbody tr.hide td p {
  padding: 0;
  font: 0 / 0 sans-serif;
  transition: 0.2s ease-in-out 0.5s;
}

tbody tr.hide td img {
  width: 0;
  height: 0;
  transition: 0.2s ease-in-out 0.5s;
}

@media (max-width: 1000px) {
  td:not(:first-of-type) {
    min-width: 12.1rem;
  }
}

thead th span.icon-arrow {
  display: inline-block;
  width: 1.3rem;
  height: 1.3rem;
  border-radius: 50%;
  border: 1.4px solid transparent;

  text-align: center;
  font-size: 1rem;

  margin-left: 0.5rem;
  transition: 0.2s ease-in-out;
}

thead th:hover span.icon-arrow {
  border: 1.4px solid #1f636f;
}

thead th:hover {
  color: #1f636f;
}

thead th.active span.icon-arrow {
  background-color: #1f636f;
  color: #fff;
}

thead th.asc span.icon-arrow {
  transform: rotate(180deg);
}

thead th.active,
tbody td.active {
  color: #1f636f;
}

.export__file {
  position: relative;
}

.export__file .export__file-btn {
  display: inline-block;
  width: 2rem;
  height: 2rem;
  background: #fff6 url(../assets/export.png) center / 80% no-repeat;
  border-radius: 50%;
  transition: 0.2s ease-in-out;
}

.export__file .export__file-btn:hover {
  background-color: #fff;
  transform: scale(1.15);
  cursor: pointer;
}

.export__file input {
  display: none;
}

.export__file .export__file-options {
  position: absolute;
  right: 0;
  width: 12rem;
  border-radius: 0.5rem;
  overflow: hidden;
  text-align: center;
  opacity: 0;
  transform: scale(0.8);
  transform-origin: top right;
  box-shadow: 0 0.2rem 0.5rem #0004;
  transition: 0.2s;
}

.export__file input:checked + .export__file-options {
  opacity: 1;
  transform: scale(1);
  z-index: 100;
}

.export__file .export__file-options label {
  display: block;
  width: 100%;
  padding: 0.6rem 0;
  background-color: #f2f2f2;

  display: flex;
  justify-content: space-around;
  align-items: center;

  transition: 0.2s ease-in-out;
}

.export__file .export__file-options label:first-of-type {
  padding: 1rem 0;
  background-color: #1f636f !important;
}

.export__file .export__file-options label:hover {
  transform: scale(1.05);
  background-color: #fff;
  cursor: pointer;
}

.export__file .export__file-options img {
  width: 2rem;
  height: auto;
}
</style>