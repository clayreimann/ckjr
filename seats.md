---
  layout: dynamic-list
---

<form method='POST' onsubmit='false;'>
  <input type='text' id='search'>
</form>

<div id='chart' markdown='1'>
* Table 1
  * Nate Griebel
  * Travis Iverson
  * Landon Iverson
  * Jaylin Iverson
  * Mike Malison
  * Anna Malison
  * Tammy Tauger
  * Matt Ziegler
* Table 2
  * Lain Barclay
  * Ben Davidson
  * John Gearheart
  * Lindsay Martin
  * Kelsey McLimans
  * Allan Muzilla
  * Brian Smith
  * Cole  Zwiefelhofer
* Table 3
  * Aaron Gary
  * Marion Kranzfelder
  * David Nashold
  * Raymond Nashold
  * Jennifer Nashold
  * James Tannler
  * Deb Zwiefelhofer
  * Arlene Zwiefelhofer
* Table 4
  * Randy Jensen
  * Christine Jensen
  * Dawson Jensen
  * Gatlin Joles
  * Lee Reimann
  * Chris Reimann
  * Art Zwiefelhofer
  * Anita Zwiefelhofer
* Table 5
  * Albie Barclay
  * Meredith Barclay
  * Carter Barclay
  * Robert Barclay
  * Ace Barlcay
  * Rosalie King
  * David King
  * Beth Livingston
* Table 6
  * Linda Odness
  * Jim Odness
  * Mark Rushmann
  * Rachel Rushmann
  * Ashleigh Voigtschild
  * Aaron Voigtschild
  * Conor Voigtschild
  * Logan Voigtschild
* Table 7
  * Dave Baier
  * Diane Baier
  * Michelle Hahn
  * Emily Hahn
  * Tony Kogut
  * John Yeager
  * Nancy Yeager
  * Jeff Zwiefelhofer
* Table 8
  * Jack Koppa
  * Kathy Kranzfelder
  * Paula Kranzfelder Gumpher
  * Denise McKay
  * Sean Nashold
  * Kieran Nashold
  * Declan Nashold
  * Hailey Sayegh
* Table 9
  * Mary Condon
  * Terrell Hyde
  * Steve Nashold
  * Brendan Nashold
  * Paul Schlumberger
  * Shelley Schlumberger
  * Peter VanBeek
  * Marjorie VanBeek
* Table 10
  * Elizabeth Connors
  * Katherine King
  * Gerard Kuhn
  * Madeleine Kuhn
  * Ramanathan  Meyyappan
  * Dave Reimann
  * Nancy Reimann
  * Laurence Ward
* Table 11
  * Larry Hable
  * Barb Hable
  * Betty Hable
  * Paul Hable
  * Carol Hable
  * Nancy Naas
* Table 12
  * Darrel Allen
  * Lea Board
  * Eric Colwell
  * Braulio Mauricio
  * Troy Meikle
  * Michaela Miller
  * Samm Sweitzer
  * Daisy Wedel
* Table 13
  * Leila Chatti
  * Monica Cooley
  * Elizabeth Garrett
  * Adam Kachelski
  * Ryley Karl
  * Henrick Mader
  * Hannah Mickelson
  * Morgan Weber
* Table 14
  * Mary McIquham
  * Tom  McIquham
  * Jane  Slupe
  * Tom  Slupe
  * Sheri Vandehaar
  * Kent Vandehaar
  * Sam Vandehaar
* Table 16
  * Torree Breen
  * Scott Breen
  * Rebecca Klinger
  * Janet Muller-Rossetti
  * Joe Rossetti
  * Mike Stephenson
  * Amy Stephenson
* Table 17
  * Kathy Becker
  * Kerri Daniels
  * Kevin Duggan
  * Patrick Duggan
  * Eileen Duggan Saracino
  * Shelia Lanz
  * Maureen Ouellette
  * Robert Reimann
* Table 18
  * Mary Addison
  * David Glenz
  * Sam Glenz
  * Evan Glenz
  * Peter Kakela
  * Pat Kastad
  * Julie Kastad
  * Karen Kastad-Glenz
* Table 19
  * Rita Sobotta
  * David Sobotta
  * Trisha Sobotta Splinter
  * Jeremy Splinter
  * Ava Splinter
  * Ella Splinter
  * Katie Stephens
  * Kyle Stephens
* Table 20
  * Julian Gary
  * Genevieve Nashold
  * Langston Nashold
  * Greta Nashold
  * Helena Nashold
  * Julia Nashold
  * Georgia Nashold
  * Rosabelle VanBeek
* Table 21
  * John Gutiérrez
  * Steve Miller
  * Faye Nashold
  * Karen Nashold
  * Lisa Nashold
  * Kevin Nashold
  * Kim Reid
  * Don Wegner
* Table 22
  * Jordan Cook
  * Ashlynn Mendoza-Schumann
  * Lori  Schumann
  * Tim Schumann
  * Alex Schumann
  * Danielle Schumann
  * Rachel Schumann
  * Kamryn Schumann
</div>

<script>
  var searchInput = document.querySelector('#search');
  var seatingList = document.querySelector('#chart').children[0];

  searchInput.onkeyup = function(e) {
    var val = e.target.value.toLowerCase();
    for (var i = 0; i < seatingList.children.length; i++) {
      var found = false;
      var people = seatingList.children[i].children[0];
      for (var j = 0; j < people.children.length; j++) {
        var person = people.children[j];
        if (person.innerHTML.toLowerCase().search(val) === -1) {
          person.style.display = 'none';
        } else {
          found = true;
          person.style.display = 'list-item';
        }
      }
      seatingList.children[i].style.display = found ? 'list-item' : 'none';
    }
  };
</script>
