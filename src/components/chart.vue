<script>
import Vue from "vue";
import "@carbon/charts/styles.css";
import chartsVue from "@carbon/charts-vue";

// IBM Plex should either be imported in your project by using Carbon
// or consumed manually through an import
import "../ibm-plex-font.css";

Vue.use(chartsVue);

export default {
	name: "Chart",
	components: {},
	data() {
		return {
			data: [
		{
				"group": "Dataset 1",
				"value": -75
		}
],
			options: {
		"title": "Meter Chart - statuses and custom color",
		"meter": {
				"peak": -70,
				"status": {
						"ranges": [
								{
										"range": [
												0,
												-40
										],
										"status": "success"
								},
								{
										"range": [
												-40,
												-60
										],
										"status": "warning"
								},
								{
										"range": [
												-60,
												-100
										],
										"status": "danger"
								}
						]
				}
		},
		"color": {
				"scale": {
						"Dataset 1": "#925699"
				}
		},
		"height": "100px"
}
		};
	},
	template: "<ccv-meter-chart :data='data' :options='options'></ccv-meter-chart>"
};
</script>
  