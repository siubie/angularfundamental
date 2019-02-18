# Add Todo Component

Selanjutnya kita akan menyelesaikan langkah selanjutnya yaitu membuat presentational component AddTodoComponent. Presentational component ini mempunyai tugas menerima input dari user untuk disimpan sebagai Item Todo. Untuk menyelesaikan component ini lakukanlah langkah percobaan dibawah ini.

Sesuai dengan desain pada chapter sebelumnya berdasarkan tabel dibawah ini

| Component          |  Input   | Output / Event Emitter |
| ------------------ | :------: | ---------------------: |
| TodoCountComponent | Todos[ ] |                      - |
| TodoItemComponent  |   Todo   |         ToggleFinished |
| AddTodoComponent   |    -     |                AddTodo |

AddTodoComponent memiliki output / event emitter yang bertujuan untuk menambahkan Todo. Selanjutnya mari kita isi file component yang sebelumnya sudah di buat pada file `add.todo.component.ts`. Bukalah file tersebut kemudian tambahkan import yang menjadi syarat untuk membuat sebuah file menjadi component.

```typescript
import { Component} from '@angular/core';
```
Component di import agar kita dapat menggunakan decorator @component. Kemudian kita dapat menggunakan decorator @Component.

```typescript
@Component({
  selector: 'add-todo',
  styleUrls: [],
  templateUrl: 'add.todo.html'
})
```
Pada kode program diatas kita menggunakan decorator @Component kemudian menggunakan selector, styleUrls dan templateUrl seperti pada kode program di atas. Dengan decorator diatas kita dapat menggunakan tag `<add-todo></add-todo>` di template html, untuk component ini tidak digunakan style dan template nya di pisah di file `add.todo.html`.

Selanjutnya setelah decorator buatlah class typescript dengan nama `AddTodoComponent` 

```typescript
export class AddTodoComponent {
  constructor() {}
}
```
Di kode program di atas kita membuat sebuah class typescript dengan nama `AddTodoComponent`, penting untuk diperhatikan ada statement export sebelum class ini diperlukan agar class ini dapat di import di file lain, jika tidak ada statement ini class ini tidak dapat di import dari file lain.

Selanjutnya lengkapilah file `add.todo.html`, di file ini kita isikan tampilan dari component add todo yang kita buat sebelumnya. 

```html
<form class="card p-2 todo-input" target="#">
  <div class="input-group">
    <input
      type="text"
      class="form-control"
      placeholder="Add Your Todo List Here"
      #task
    />
    <div class="input-group-append">
      <button
        type="submit"
        class="btn btn-secondary"
      >
        Add Todo
      </button>
    </div>
  </div>
</form>
```
Dengan menambahkan tampilan ini