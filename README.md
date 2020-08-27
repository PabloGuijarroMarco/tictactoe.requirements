<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="generator" content="Asciidoctor 2.0.8">
<meta name="author" content="Santa Tecla">
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Open+Sans:300,300italic,400,400italic,600,600italic%7CNoto+Serif:400,400italic,700,700italic%7CDroid+Sans+Mono:400,700">

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
</head>
<body class="book">
<div id="header">
<h1>TicTacToe. Requisitos 5. <strong>Ficheros</strong></h1>
<div class="details">
<span id="author" class="author">Santa Tecla</span><br>
<span id="email" class="email"><a href="mailto:parqueNaturalSantaTecla@gmail.com">parqueNaturalSantaTecla@gmail.com</a></span><br>
<span id="revnumber">version 0.5.0</span>
</div>
<div id="toc" class="toc">
<div id="toctitle">Índice</div>
<ul class="sectlevel1">
<li><a href="#requisitos">Requisitos</a></li>
<li><a href="#vista-de-casos-de-uso">Vista de Casos de Uso</a>
<ul class="sectlevel2">
<li><a href="#prototipo-de-interfaz">Prototipo de Interfaz</a></li>
</ul>
</li>
</ul>
</div>
</div>
<div id="content">
<div class="sect1">
<h2 id="requisitos">Requisitos</h2>
<div class="sectionbody">
<table class="tableblock frame-all grid-all stretch">
<colgroup>
<col style="width: 50%;">
<col style="width: 50%;">
</colgroup>
<tbody>
<tr>
<td class="tableblock halign-left valign-top"><div class="content"><div class="ulist">
<ul>
<li>
<p><a href="https://en.wikipedia.org/wiki/Tic-tac-toe"><strong>Wiki</strong></a></p>
<div class="ulist">
<ul>
<li>
<p><em>Funcionalidad: <strong>Básica</strong> + <strong>undo/redo</strong></em></p>
</li>
<li>
<p><em>Interfaz: <strong class="line-through">Gráfica</strong> y <strong>Texto</strong></em></p>
</li>
<li>
<p><em>Distribución: <strong>Standalone</strong> + <strong>Client/Server</strong></em></p>
</li>
<li>
<p><em>Persistencia: <span class="lime-background"><strong>Ficheros</strong></span></em></p>
</li>
</ul>
</div>
</li>
</ul>
</div></div></td>
<td class="tableblock halign-left valign-top"><div class="content"><div class="imageblock">
<div class="content">
<img src="build/docs/asciidoc/images/Dibujo.jpg" alt="Dibujo" width="300" height="300">
</div>
</div></div></td>
</tr>
</tbody>
</table>
</div>
</div>
<div class="sect1">
<h2 id="vista-de-casos-de-uso">Vista de Casos de Uso</h2>
<div class="sectionbody">
<table class="tableblock frame-all grid-all stretch">
<colgroup>
<col style="width: 50%;">
<col style="width: 50%;">
</colgroup>
<thead>
<tr>
<th class="tableblock halign-left valign-top">Diagrama de Actores y Casos de Uso</th>
<th class="tableblock halign-left valign-top">Diagrama de Contexto</th>
</tr>
</thead>
<tbody>
<tr>
<td class="tableblock halign-left valign-top"><div class="content"><div class="imageblock">
<div class="content">
<img src="build/docs/asciidoc/images/diagramaActoresCasosUso.svg" alt="diagramaActoresCasosUso" width="380" height="201">
</div>
</div></div></td>
<td class="tableblock halign-left valign-top"><div class="content"><div class="imageblock">
<div class="content">
<img src="build/docs/asciidoc/images/diagramaContexto.svg" alt="diagramaContexto" width="364" height="504">
</div>
</div></div></td>
</tr>
</tbody>
</table>
<div class="sect3">
<h4 id="consola">Consola</h4>
<table class="tableblock frame-all grid-all stretch">
<colgroup>
<col style="width: 50%;">
<col style="width: 50%;">
</colgroup>
<tbody>
<tr>
<td class="tableblock halign-left valign-top"><div class="content"><div class="literalblock">
<div class="content">
<pre>-------------------- TIC TAC TOE --------------------
----- Choose one option -----
1) Start a new game
2) Open a saved game
1
Number of users [0-2] 1
----- Choose one option -----
1) Do a movement
2) Exit game
1
-----------------------------------------------------
| - | - | - |
| - | - | - |
| - | - | - | 
-----------------------------------------------------
Enter a coordinate to put a token:
Row: 1
Column: 1
-----------------------------------------------------
| X | - | - |
| - | - | - |
| - | - | - |
-----------------------------------------------------
----- Choose one option -----
1) Do a movement
2) Undo previous movement
3) Exit game
1
-----------------------------------------------------
| X | - | - |
| - | - | - |
| - | - | - |
-----------------------------------------------------
-----------------------------------------------------
| X | - | O |
| - | - | - |
| - | - | - | 
-----------------------------------------------------
----- Choose one option -----
1) Do a movement
2) Undo previous movement
3) Exit game
1
-----------------------------------------------------
| X | - | O |
| - | - | - |
| - | - | - |
-----------------------------------------------------
Enter a coordinate to put a token:
Row: 2
Column: 1
-----------------------------------------------------
| X | - | O |
| X | - | - | 
| - | - | - |
-----------------------------------------------------
----- Choose one option -----
1) Do a movement
2) Undo previous movement
3) Exit game
1
-----------------------------------------------------
| X | - | O |
| X | - | - |
| - | - | - |
-----------------------------------------------------
-----------------------------------------------------
| X | - | O |
| X | - | O |
| - | - | - |
-----------------------------------------------------
----- Choose one option -----
1) Do a movement
2) Undo previous movement
3) Exit game
3
Do you want to save the game?? (y/n): y
Name: juego2</pre>
</div>
</div></div></td>
<td class="tableblock halign-left valign-top"><div class="content"><div class="literalblock">
<div class="content">
<pre>------------------- TIC TAC TOE --------------------

----- Choose one option -----
1) Start a new game
2) Open a saved game
2

----- Choose one option -----
1) juego1.mm
2) juego2.mm
2
juego2.mm

----- Choose one option -----
1) Do a movement
2) Exit game
1
-----------------------------------------------------
| X | - | O |
| X | - | O |
| - | - | - | 
-----------------------------------------------------
Enter a coordinate to put a token:
Row: 1
Column: 4
The coordinates are wrong
Enter a coordinate to put a token:
Row: 3
Column: 1
-----------------------------------------------------
| X | - | O |
| X | - | O |
| X | - | - |
-----------------------------------------------------
Do you want to save the game?? (y/n): n
X Player: You win!!! :-)</pre>
</div>
</div></div></td>
</tr>
</tbody>
</table>
</div>
</div>
</div>
</div>
</div>
<div id="footer">
<div id="footer-text">
Version 0.5.0<br>
Last updated 2020-08-27 22:30:00 +0200
</div>
</div>
</html>