# Construindo Aplicações Web com Angular (4,5 e 6)

## Conteúdo do curso
  - Criar uma aplicação usando recursos do Angular como Componentes, Diretivas e Pipes

  - Consumir Web Services REST usando os serviços Http e HttpClient
    Diretivas são uma das principais características do Angular. Elas são classes que adicionam comportamentos adicionais aos elementos do DOM. Existem três tipos de diretivas no Angular:

    Diretivas de Componentes: São diretivas com um template. Elas são essencialmente classes Angular anotadas com o decorator @Component.

    Diretivas Estruturais: Elas alteram o layout adicionando, removendo e substituindo elementos no DOM. Exemplos de diretivas estruturais incluem *ngFor e *ngIf.

    Diretivas de Atributo: Elas alteram a aparência ou comportamento de um elemento, componente ou outra diretiva. Exemplos incluem ngStyle e ngClass.
```typescript
import { Directive, ElementRef, OnInit } from '@angular/core';

@Directive({
  selector: '[appHighlight]'
})
export class HighlightDirective implements OnInit {
  constructor(private el: ElementRef) { }

  ngOnInit() {
    this.el.nativeElement.style.backgroundColor = 'yellow';
  }
}
```
```html
<p appHighlight>Texto destacado</p>
```
  - Usar eventos para Comunicação entre Componentes
  - Usar HttpInterceptors para Enviar Headers de Autorização automaticamente
  - Usar Route Guards para Proteger Componentes na Aplicação
  - Criar Formulários com Template Forms e Reactive Forms
  - Usar Validadores Padrões e Personalizados para Formulários
  - Criar Módulos e Carregá-los de Forma Tardia (Lazy-Loading)
  - Usar Operadores de RxJS para Implementar Buscas Sofisticadas de Forma Simples
  - Realizar Autenticação Simples em uma Aplicação Angular
  - RxJS 6 e o novo operador "pipe" (Angular 6)
  - Criar Componentes com Angular Elements (Angular 6)