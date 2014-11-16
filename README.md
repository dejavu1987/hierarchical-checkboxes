# Hierarchical checkboxes
=======================

>jQuery for hierarchical checkboxes 


##Hierarchical Checkboxes
author: Anil Maharjan


###USAGE:
Template Construction:
User ROOT template and Nest as many NODE templates 

####ROOT:
```HTML
		<div class="hierarchy-checkboxes" rel="test">
		  <input class="hierarchy-root-checkbox" type="checkbox">
		  <label class="hierarchy-root-label">Root</label>
		  <div class="hierarchy-root-child hierarchy-node">
		   {{ NODE TEMPLATE HERE }}
		  </div>
		</div>
```
####NODE:
```HTML
		<div class="hierarchy-node [leaf]">
		  <input class="hierarchy-checkbox" type="checkbox">
		  <label class="hierarchy-label">[Title]</label>
		  {{ NODE TEMPLATE HERE }}
		</div> 
```

###Basic Example Template
```html
		<div class="hierarchy-checkboxes" rel="test">
		  <input class="hierarchy-root-checkbox" type="checkbox">
		  <label class="hierarchy-root-label">Root</label>
		  <div class="hierarchy-root-child hierarchy-node">
		   <div class="hierarchy-node leaf">
		      <input class="hierarchy-checkbox" type="checkbox">
		      <label class="hierarchy-label">Markets</label>
		      <div class="hierarchy-node leaf">
		        <input class="hierarchy-checkbox" type="checkbox">
		        <label class="hierarchy-label">Markets</label>
		      </div> 
		    </div> 
		    <div class="hierarchy-node leaf">
		      <input class="hierarchy-checkbox" type="checkbox">
		      <label class="hierarchy-label">Markets</label>
		    </div> 
		  </div>
		</div>
```


###API:

####EVENTS:

#####1. checkboxesUpdate:

  Triggers whenever the check/uncheck tasks complete withing the hierarchical checkboxes

Example:
```javascript
		jQuery('.hierarchy-checkboxes[rel=IDENTIFIER]').on('checkboxesUpdate',function(){
		  console.log("Changed!");
		});
```