# Sobrevivência — Alfa v1

Protótipo de sobrevivência isométrico (inspirado em Project Zomboid) feito em Godot 4.7.2.

## Como rodar
- **Editor**: abra `project.godot` no Godot 4.7.2 e aperte F5.
- **Web**: sirva a pasta `build/web/` (ex.: `python3 -m http.server -d build/web`) e abra `index.html`. Funciona no GitHub Pages (export sem threads).
- **Windows**: `build/windows/Sobrevivencia_Alfa_v1.exe`.

## Controles — PC
| Ação | Tecla |
|---|---|
| Andar | WASD ou setas |
| Correr (faz barulho!) | Shift |
| Interagir / pegar item / abrir e fechar porta ou janela | E (toque rápido) |
| Trancar / destrancar porta ou janela | **Segure** E |
| Largar item selecionado | Q |
| Inventário | Tab ou I |

## Controles — Celular
- **Joystick** no canto inferior esquerdo: andar.
- **Interagir**: toque rápido = pegar/abrir/fechar; segure = trancar/destrancar.
- **Correr**: segure enquanto anda.
- **Inventário**: abre ou fecha. Arraste os itens com o dedo entre o inventário e a área "Chão".

## O que tem nesta versão
- Rua e uma casa com 2 cômodos, 1 porta e 2 janelas.
- Fome e Cansaço sobem com o tempo. Quando estão altos, você fica mais lento.
- 3 itens no chão da casa: lata de comida, garrafa de água e martelo.
- Inventário de 8 espaços.
- 1 zumbi: vem atrás de você se estiver perto ou se você correr (raio de barulho amarelo). Se a porta ou a janela estiver fechada, ele fica batendo nela, mas não quebra nada.

## Testes
```
godot --headless --path . res://tests/testes.tscn      # 60 verificações
python3 tests/web_test.py http://localhost:PORTA/index.html   # Chrome headless (precisa de playwright)
```
