// Your recommended changes go here

## Visual to the UI (CSS, visual elements)

## Technical changes: HTML, CSS, Javascript, ARIA attributes

## Content

Old:
<input id="zip-code" class="bg form-control zipEntry ng-pristine ng-untouched ng-empty ng-invalid ng-invalid-required ng-valid-pattern ng-valid-maxlength" ng-pattern="/^\d{1,5}$/" required="" name="zip" ng-model="entry.zipcode" ng-class="{errorBorder: (form.$submitted || form.zip.$touched) &amp;&amp; (form.zip.$error.required || form.zip.$error.pattern || noCountiesFound)}" type="tel" placeholder="Example: 60647" autocorrect="off" autocapitalize="off" autocomplete="off" maxlength="5">

Updated:
<input id="zip-code" class="bg form-control zipEntry ng-pristine ng-untouched ng-empty ng-invalid ng-invalid-required ng-valid-pattern ng-valid-maxlength" ng-pattern="/^\d{1,5}$/" required="" name="zip" ng-model="entry.zipcode" ng-class="{errorBorder: (form.$submitted || form.zip.$touched) &amp;&amp; (form.zip.$error.required || form.zip.$error.pattern || noCountiesFound)}" type="tel" placeholder="Example: 60647" autocorrect="off" autocapitalize="off" autocomplete="off" maxlength="5" aria-required="true" >

Old: 
<div class="u-sm-table-cell u-sm-span-4 u-pr3 u-align-middle">
	<span class="u-m0 u-block">Choose</span>
</div>

updated:
<div class="u-sm-table-cell u-sm-span-4 u-pr3 u-align-middle" role="button">
	<span class="u-m0 u-block">Choose</span>
</div>

Old:
<button class="u-block u-span-12 btn btn-green btn-md btn-continue-lg" role="button" id="continue-btn" ng-disabled="form.buying.$invalid" disabled="disabled">CONTINUE</button>

Updated:
<button class="u-block u-span-12 btn btn-green btn-md btn-continue-lg" id="continue-btn" ng-disabled="form.buying.$invalid" disabled="disabled">CONTINUE</button>

Old:
<input age-validator="" aria-labelledby="item-description age" id="age-field" ng-pattern="/^\d{1,3}$/" required="" name="age" type="tel" ng-model="newEnrollee.age" placeholder="Enter age in years" class="ng-pristine ng-untouched ng-empty ng-invalid ng-invalid-required ng-valid-pattern">

Updated:
<input age-validator="" aria-labelledby="item-description age" id="age-field" ng-pattern="/^\d{1,3}$/" required="" name="age" type="tel" ng-model="newEnrollee.age" placeholder="Enter age in years" class="ng-pristine ng-untouched ng-empty ng-invalid ng-invalid-required ng-valid-pattern" aria-required="true" >

Old: 
<a role="button" class="col-xs-1 text-center" aria-label="Legal parent or guardian of a child under 109 claimed as a tax dependent " href="javascript:;" uib-tooltip="Legal parent or guardian of a child under 109 claimed as a tax dependent ">
<span class="glyphicon glyphicon-info-sign"></span>
</a>

Updated:
<a role="tooltip" class="col-xs-1 text-center" aria-label="Legal parent or guardian of a child under 109 claimed as a tax dependent " href="javascript:;" uib-tooltip="Legal parent or guardian of a child under 109 claimed as a tax dependent ">
<span class="glyphicon glyphicon-info-sign"></span>
</a>

Old:
<div class="hcapp-providerResult ng-scope" ng-repeat="coverable in household[coverableType]">
	
Updated:
<div class="hcapp-providerResult ng-scope" ng-repeat="coverable in household[coverableType]" aria-live="polite"> <!-- apply aria-live="polite" in javascript-->
