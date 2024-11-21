# Toastr & SweetAlert2

## Installation

Install ngx-toastr and sweetalert2 using one command with all necessary configurations

```bash
ng add @kalees64/toast
```

## Usage

app.component.ts

```typescript
import { Component } from "@angular/core";
import { ToastrService } from "ngx-toastr";
import Swal from "sweetalert2";

@Component({
  selector: "app-root",
  standalone: true,
  imports: [],
  templateUrl: "./app.component.html",
  styleUrl: "./app.component.css",
})
export class AppComponent {
  title = "test1";

  constructor(private toast: ToastrService) {}

  click() {
    this.toast.success("I am Fine");
    Swal.fire("I am Also in the same page");
  }
}
```

app.component.html

```typescript
<h1 class="text-7xl">I am Kalees</h1>
<button class="vk-btn-pink" (click)="click()">Click me</button>
```
