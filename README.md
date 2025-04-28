# Retina Cells

Simulates a neuron cells build with go channels.

![Neuron](https://cdn-prod.medicalnewstoday.com/content/images/articles/320/320289/neuron-diagram.jpg)
  
  //
	//  created with http://asciiflow.com/
	//
	//  in           out
	//      +------+     +---------+
	// ---->| Add1 o---->| Display |
	//      +------+     +---------+

	//          +-------+     +---------+
	// inX ---->|       | res |         |
	//          |  Add  o---->| Display |
	// inY ---->|       | res |         |
	//          +-------+     +---------+
	
	//
	// Cell with weighted Synapses, Body and Axon
	//

	//     dendride
	//   	          +----------+
	//   0 +------->w1|          |
	//   	          |          |
	//   1 +------->w2|   cell   |  axon
	//   	          |  (soma)  o------->
	//         ...    |   body   |
	//   	          |          |
	//   n +------->wn|          |
	//   	          +----------+
	//            synapses
	
		// -->(cell1)----->(cell2)--->Display

	//
	// Example with 3 cells from book Manfred Spitzer
	//

	//   +--------+                   +--------+
	//   |        o------------A--( 5)>        |    +-----------+
	//   | Emit_A o---+    +---B--( 3)> Cell_A o----> Display_C |
	//   |        o-+ |    | +-C--(~3)>        |    +-----------+
	//   +--------+ | |    | |        +--------+
	//
	//   +--------+   |    |         +--------+
	//   |        o---+    +---A--( 5)>        |    +-----------+
	//   | Emit_B o------------B--( 3)> Cell_B o----> Display_B |
	//   |        o---+    +---C--(10)>        |    +-----------+
	//   +--------+   |    |         +--------+
	//
	//   +--------+ | |    | |        +--------+
	//   |        o-+ |    | +-A--( 5)>        |    +-----------+
	//   | Emit_C o---+    +---B--( 3)> Cell_C o----> Display_C |
	//   |        o------------C--(~3)>        |    +-----------+
	//   +--------+                   +--------+
