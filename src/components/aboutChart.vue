
<script>
// hi
import { 	Line } from 'vue-chartjs'
import store from '@/store'

export default {

  extends: Line,
  data() {
  		return {
  				chartData: {
			        labels: ['Vue.js', 'Node.js', 'Javascript', 'Python', 'C++', 'R', 'Postgres','Data structures/algorithms'],
			        datasets: [{
			        		label: "hello",
			            data: [60,50,60,50,50, 40, 40, 70],
			            backgroundColor: [
			            		'#B5EAEA',
			            		'#B5EAEA',
			            		'#B5EAEA',
			            		'#B5EAEA',
			            		'#B5EAEA',
			            		'#B5EAEA',
			            		'#B5EAEA',
			            		'#B5EAEA',
			            ],
			            borderColor: [

			                'rgba(54, 162, 235, 1)',		
			                'rgba(54, 162, 235, 1)',
			                'rgba(54, 162, 235, 1)',
			                'rgba(54, 162, 235, 1)',
			                'rgba(54, 162, 235, 1)',
			                'rgba(54, 162, 235, 1)',
			                'rgba(54, 162, 235, 1)',
			                'rgba(54, 162, 235, 1)'
			            ],
			            borderWidth: 1
			        }]
			    },

			    options: {
			        scales: {
			            yAxes: [{
			                beginAtZero: true,
			                gridLines: {
			                		display:false,
			                },
			                ticks:{
			                		fontSize:22,
			                		callback: function(value, index, values){
			                			  return value 
			                		}
			                },
			            }],
			            xAxes: [{
			                beginAtZero: true,
			                gridLines: {
			                		display:true
			                },
			                ticks: {
			                    display: true, //this will remove only the label
			                    suggestedMin:0,
                    			suggestedMax: 100
			                },			                
				            }],			            
			        },
			        legend: {
			        		labels: {
			        				// fontColor:'black',
			        				// fontSize: 30,
			        				// boxWidth: 0,
			        				display:false,
			        		}
			        },
			        tooltips: {
		            callbacks: {
		                label: function(tooltipItem, data) {
		                    var dataset = data.datasets[tooltipItem.datasetIndex];
		                    var index = tooltipItem.index;
		                    return dataset.labels[index] + ': ' + dataset.data[index];
		                }
		            }
		        	},


			    },			    
  		};
  },
  mounted() {
  		this.renderChart(this.chartData, this.options);
  		
  },
  methods: {

  },

};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">


</style>