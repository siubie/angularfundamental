# Service

Seperti yang sudah dijelaskan pada chapter sebelumnya bahwa sebuah container component dapat terhubung dengan sebuah service yang akan menghubungkan component tersebut dengan data yang digunakan baik melalui sebuah REST API, Local Storage, Json file atau datasource lainnya.

## buat file service

Langkah pertama untuk membuat service adalah dengan membuat sebuah file baru dengan nama `todo.dashboard.service` pada module `TodoDashboard`.

```
.
├── component
│   ├── add-todo
│   │   ├── add.todo.component.ts
│   │   └── add.todo.html
│   ├── todo-count
│   │   ├── todo.count.component.ts
│   │   └── todo.count.html
│   └── todo-item
│       ├── todo.item.component.ts
│       └── todo.item.html
├── containers
│   ├── todo.dashboard.component.ts
│   ├── todo.dashboard.css
│   └── todo.dashboard.html
├── models
│   └── todo.model.ts
├── todo.dashboard.module.ts
└── todo.dashboard.service.ts -> file service baru
```

pada file tersebut tambahkan kode program berikut ini.

```typescript
export class TodoDashboardService {
  constructor() {}

  getTodos() {}

  createTodo() {}

  updateTodo() {}
}
```

Kode program diatas berisi skeleton code untuk service yang dapat digunakan

## tambah provider di todo dasboard module

Setelah membuat file service, agar service ini dapat digunakan oleh module TodoDashboard service ini harus di import sebagai `provider` pada module TodoDashboard.

Untuk mengimport nya silahkan buka file todo.dashboard.module.ts, kemudian tambahkan import untuk file todo.dashboard.service.ts

```typescript
import { NgModule } from "@angular/core";
import { CommonModule } from "@angular/common";

import { TodoDashboardComponent } from "./containers/todo.dashboard.component";
import { AddTodoComponent } from "./component/add-todo/add.todo.component";
import { TodoCountComponent } from "./component/todo-count/todo.count.component";
import { TodoItemComponent } from "./component/todo-item/todo.item.component";
import { TodoDashboardService } from "./todo.dashboard.service";
@NgModule({
  declarations: [
    TodoDashboardComponent,
    AddTodoComponent,
    TodoCountComponent,
    TodoItemComponent
  ],
  imports: [CommonModule, HttpClientModule],
  exports: [TodoDashboardComponent],
  providers: [TodoDashboardService]
})
export class TodoDashboardModule {}
```

pada kode program diatas ditambahkan import TodoDashboardService dan provider pada decorator @NgModule

## dependency injection

Setelah menambahkan provider di TodoDashboardModule, TodoDashboardService dapat digunakan di component yang berada di dalam module Todo Dashboard.

Untuk mempermudah penggunannya digunakan sebuah teknik dependency injection di TodoDashboardComponent. Caranya dengan mengimport TodoDashboardService ke TodoDashboardComponent dan menjadikannya sebagai parameter di construktor component.

```typescript
import { Component, OnInit } from "@angular/core";
import { Todo } from "../models/todo.model";
import { TodoDashboardService } from "../todo.dashboard.service";
@Component({
  selector: "todo-dashboard",
  styleUrls: ["todo.dashboard.css"],
  templateUrl: "todo.dashboard.html"
})
export class TodoDashboardComponent implements OnInit {
  todoList: Todo[] = [];
  constructor(private todoDashboardService: TodoDashboardService) {}

  ngOnInit() {
      ...
  }

  handleAddTodo(task: string) {
      ...
  }

  handleToggleFinished(todo: Todo) {
      ...
  }
}

```

## ngOnInit

## import httpmodule

bedanya DI pake yang butuh import dengan yang gak, **injectable**

## observable subscribe safe navigation

## get

## post

## delete
