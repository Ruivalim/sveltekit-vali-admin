<script>
	import { browser } from '$app/environment';
	import AppTitle from '$lib/components/AppTitle.svelte';

	$effect(() => {
		(async () => {
			if (!browser) return;
			const bootstrap = await import('bootstrap');

			// Enable all alerts on the page
			const alertList = document.querySelectorAll('.alert');
			const alerts = [...alertList].map((element) => new bootstrap.Alert(element));

			// Enable all popovers on the page
			const popoverTriggerList = document.querySelectorAll('[data-bs-toggle="popover"]');
			const popoverList = [...popoverTriggerList].map(
				(popoverTriggerEl) => new bootstrap.Popover(popoverTriggerEl)
			);

			// Enable all tooltips on the page
			const tooltipTriggerList = document.querySelectorAll('[data-bs-toggle="tooltip"]');
			const tooltipList = [...tooltipTriggerList].map(
				(tooltipTriggerEl) => new bootstrap.Tooltip(tooltipTriggerEl)
			);
		})();
	});
</script>

<svelte:head>
	<title>Bootstrap Elements - Vali Admin</title>
</svelte:head>

<AppTitle title="Bootstrap Elements" desc="Bootstrap Components" iconTitle="bi bi-laptop" />
<!-- Buttons-->
<div class="tile mb-4">
	<div class="page-header">
		<div class="row">
			<div class="col-lg-12">
				<h2 class="mb-3 line-head" id="buttons">Buttons</h2>
			</div>
		</div>
	</div>
	<div class="row">
		<div class="col-lg-7">
			<p class="bs-component">
				<button class="btn btn-primary" type="button">Primary</button>
				<button class="btn btn-secondary" type="button">Secondary</button>
				<button class="btn btn-success" type="button">Success</button>
				<button class="btn btn-info" type="button">Info</button>
				<button class="btn btn-warning" type="button">Warning</button>
				<button class="btn btn-danger" type="button">Danger</button>
				<button class="btn btn-link" type="button">Link</button>
			</p>
			<p class="bs-component">
				<button class="btn btn-primary" type="button" disabled>Primary</button>
				<button class="btn btn-secondary" type="button" disabled>Secondary</button>
				<button class="btn btn-success" type="button" disabled>Success</button>
				<button class="btn btn-info" type="button" disabled>Info</button>
				<button class="btn btn-warning" type="button" disabled>Warning</button>
				<button class="btn btn-danger" type="button" disabled>Danger</button>
				<button class="btn btn-link" type="button" disabled>Link</button>
			</p>
			<p class="bs-component">
				<button class="btn btn-outline-primary" type="button">Primary</button>
				<button class="btn btn-outline-secondary" type="button">Secondary</button>
				<button class="btn btn-outline-success" type="button">Success</button>
				<button class="btn btn-outline-info" type="button">Info</button>
				<button class="btn btn-outline-warning" type="button">Warning</button>
				<button class="btn btn-outline-danger" type="button">Danger</button>
			</p>
			<div class="mb-3 bs-component">
				<div class="btn-group" role="group" aria-label="Button group with nested dropdown">
					<button class="btn btn-primary" type="button">Primary</button>
					<div class="btn-group" role="group">
						<button
							class="btn btn-primary dropdown-toggle"
							id="btnGroupDrop1"
							type="button"
							data-bs-toggle="dropdown"
							aria-haspopup="true"
							aria-expanded="false"
							aria-label="dropdown"
						></button>
						<div class="dropdown-menu dropdown-menu-right">
							<a class="dropdown-item" href="/bootstrap-components">Dropdown link</a>
							<a class="dropdown-item" href="/bootstrap-components">Dropdown link</a>
						</div>
					</div>
				</div>
				<div class="btn-group" role="group" aria-label="Button group with nested dropdown">
					<button class="btn btn-success" type="button">Success</button>
					<div class="btn-group" role="group">
						<button
							class="btn btn-success dropdown-toggle"
							id="btnGroupDrop2"
							type="button"
							data-bs-toggle="dropdown"
							aria-haspopup="true"
							aria-expanded="false"
							aria-label="dropdown"
						></button>
						<div class="dropdown-menu dropdown-menu-right">
							<a class="dropdown-item" href="/bootstrap-components">Dropdown link</a>
							<a class="dropdown-item" href="/bootstrap-components">Dropdown link</a>
						</div>
					</div>
				</div>
				<div class="btn-group" role="group" aria-label="Button group with nested dropdown">
					<button class="btn btn-info" type="button">Info</button>
					<div class="btn-group" role="group">
						<button
							class="btn btn-info dropdown-toggle"
							id="btnGroupDrop3"
							type="button"
							data-bs-toggle="dropdown"
							aria-haspopup="true"
							aria-expanded="false"
							aria-label="dropdown"
						></button>
						<div class="dropdown-menu dropdown-menu-right">
							<a class="dropdown-item" href="/bootstrap-components">Dropdown link</a>
							<a class="dropdown-item" href="/bootstrap-components">Dropdown link</a>
						</div>
					</div>
				</div>
				<div class="btn-group" role="group" aria-label="Button group with nested dropdown">
					<button class="btn btn-danger" type="button">Danger</button>
					<div class="btn-group" role="group">
						<button
							class="btn btn-danger dropdown-toggle"
							id="btnGroupDrop4"
							type="button"
							data-bs-toggle="dropdown"
							aria-haspopup="true"
							aria-expanded="false"
							aria-label="dropdown"
						></button>
						<div class="dropdown-menu dropdown-menu-right">
							<a class="dropdown-item" href="/bootstrap-components">Dropdown link</a>
							<a class="dropdown-item" href="/bootstrap-components">Dropdown link</a>
						</div>
					</div>
				</div>
			</div>
			<div class="bs-component">
				<button class="btn btn-primary btn-lg" type="button">Large button</button>
				<button class="btn btn-primary" type="button">Default button</button>
				<button class="btn btn-primary btn-sm" type="button">Small button</button>
			</div>
		</div>
		<div class="col-lg-5">
			<p class="bs-component d-grid">
				<button class="btn btn-primary btn-lg btn-block" type="button">Block level button</button>
			</p>
			<div class="bs-component mb-3">
				<div class="btn-group">
					<input class="btn-check" id="btnCheck1" type="checkbox" checked autocomplete="off" />
					<label class="btn btn-primary" for="btnCheck1">Active</label>
					<input class="btn-check" id="btnCheck2" type="checkbox" autocomplete="off" />
					<label class="btn btn-primary" for="btnCheck2">Check</label>
					<input class="btn-check" id="btnCheck3" type="checkbox" autocomplete="off" />
					<label class="btn btn-primary" for="btnCheck3">Check</label>
				</div>
			</div>
			<div class="bs-component mb-3">
				<div class="btn-group">
					<input
						class="btn-check"
						id="option1"
						type="radio"
						name="options"
						autocomplete="off"
						checked
					/>
					<label class="btn btn-primary" for="option1">Active</label>
					<input class="btn-check" id="option2" type="radio" name="options" autocomplete="off" />
					<label class="btn btn-primary" for="option2">Radio</label>
					<input class="btn-check" id="option3" type="radio" name="options" autocomplete="off" />
					<label class="btn btn-primary" for="option3">Radio</label>
				</div>
			</div>
			<div class="bs-component mb-3">
				<div class="btn-group-vertical" data-bs-toggle="button">
					<button class="btn btn-primary" type="button">Button</button>
					<button class="btn btn-primary" type="button">Button</button>
					<button class="btn btn-primary" type="button">Button</button>
					<button class="btn btn-primary" type="button">Button</button>
					<button class="btn btn-primary" type="button">Button</button>
					<button class="btn btn-primary" type="button">Button</button>
				</div>
			</div>
			<div class="bs-component mb-3">
				<div class="btn-group" role="group" aria-label="Basic example">
					<button class="btn btn-secondary" type="button">Left</button>
					<button class="btn btn-secondary" type="button">Middle</button>
					<button class="btn btn-secondary" type="button">Right</button>
				</div>
			</div>
			<div class="bs-component mb-3">
				<div class="btn-toolbar" role="toolbar" aria-label="Toolbar with button groups">
					<div class="btn-group me-2" role="group" aria-label="First group">
						<button class="btn btn-secondary" type="button">1</button>
						<button class="btn btn-secondary" type="button">2</button>
						<button class="btn btn-secondary" type="button">3</button>
						<button class="btn btn-secondary" type="button">4</button>
					</div>
					<div class="btn-group me-2" role="group" aria-label="Second group">
						<button class="btn btn-secondary" type="button">5</button>
						<button class="btn btn-secondary" type="button">6</button>
						<button class="btn btn-secondary" type="button">7</button>
					</div>
					<div class="btn-group" role="group" aria-label="Third group">
						<button class="btn btn-secondary" type="button">8</button>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>

<!-- Typography-->
<div class="tile mb-4">
	<div class="row">
		<div class="col-lg-12">
			<div class="page-header">
				<h2 class="mb-3 line-head" id="typography">Typography</h2>
			</div>
		</div>
	</div>
	<!-- Headings-->
	<div class="row">
		<div class="col-lg-4">
			<div class="bs-component">
				<h1>Heading 1</h1>
				<h2>Heading 2</h2>
				<h3>Heading 3</h3>
				<h4>Heading 4</h4>
				<h5>Heading 5</h5>
				<h6>Heading 6</h6>
				<h3>Heading<small class="text-muted"> with muted text</small></h3>
				<p class="lead">Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor.</p>
			</div>
		</div>
		<div class="col-lg-4">
			<div class="bs-component">
				<h2>Example body text</h2>
				<p>
					Nullam quis risus eget <a href="/bootstrap-components">urna mollis ornare</a> vel eu leo. Cum
					sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Nullam id
					dolor id nibh ultricies vehicula.
				</p>
				<p><small>This line of text is meant to be treated as fine print.</small></p>
				<p>The following is <strong>rendered as bold text</strong>.</p>
				<p>The following is <em>rendered as italicized text</em>.</p>
				<p>An abbreviation of the word attribute is <abbr title="attribute">attr</abbr>.</p>
			</div>
		</div>
		<div class="col-lg-4">
			<div class="bs-component">
				<h2>Emphasis classes</h2>
				<p class="text-muted">Fusce dapibus, tellus ac cursus commodo, tortor mauris nibh.</p>
				<p class="text-primary">Nullam id dolor id nibh ultricies vehicula ut id elit.</p>
				<p class="text-warning">Etiam porta sem malesuada magna mollis euismod.</p>
				<p class="text-danger">Donec ullamcorper nulla non metus auctor fringilla.</p>
				<p class="text-success">Duis mollis, est non commodo luctus, nisi erat porttitor ligula.</p>
				<p class="text-info">Maecenas sed diam eget risus varius blandit sit amet non magna.</p>
			</div>
		</div>
	</div>
	<!-- Blockquotes-->
	<div class="row">
		<div class="col-lg-12">
			<h2 class="mb-3 line-head" id="type-blockquotes">Blockquotes</h2>
		</div>
	</div>
	<div class="row">
		<div class="col-lg-6">
			<div class="bs-component">
				<blockquote class="blockquote">
					<p>
						Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.
					</p>
					<footer class="blockquote-footer">
						Someone famous in
						<cite title="Source Title">Source Title</cite>
					</footer>
				</blockquote>
			</div>
		</div>
		<div class="col-lg-6">
			<div class="bs-component">
				<blockquote class="blockquote blockquote-reverse">
					<p>
						Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.
					</p>
					<footer class="blockquote-footer">
						Someone famous in
						<cite title="Source Title">Source Title</cite>
					</footer>
				</blockquote>
			</div>
		</div>
	</div>
</div>

<!-- Navs-->
<div class="tile mb-4">
	<div class="row">
		<div class="col-lg-12">
			<div class="page-header">
				<h2 class="mb-3 line-head" id="navs">Navs</h2>
			</div>
		</div>
	</div>
	<div class="row" style="margin-bottom: 2rem;">
		<div class="col-lg-6">
			<h3>Tabs</h3>
			<div class="bs-component">
				<ul class="nav nav-tabs">
					<li class="nav-item">
						<a class="nav-link active" data-bs-toggle="tab" href="#home">Home</a>
					</li>
					<li class="nav-item">
						<a class="nav-link" data-bs-toggle="tab" href="#profile">Profile</a>
					</li>
					<!-- svelte-ignore a11y_invalid_attribute -->
					<li class="nav-item"><a class="nav-link disabled" href="#">Disabled</a></li>
					<li class="nav-item dropdown">
						<!-- svelte-ignore a11y_invalid_attribute -->
						<a
							class="nav-link dropdown-toggle"
							data-bs-toggle="dropdown"
							href="#"
							role="button"
							aria-haspopup="true"
							aria-expanded="false">Dropdown</a
						>
						<div class="dropdown-menu">
							<a class="dropdown-item" href="/bootstrap-components">Action</a>
							<a class="dropdown-item" href="/bootstrap-components">Another action</a>
							<a class="dropdown-item" href="/bootstrap-components">Something else here</a>
							<div class="dropdown-divider"></div>
							<a class="dropdown-item" href="/bootstrap-components">Separated link</a>
						</div>
					</li>
				</ul>
				<div class="tab-content" id="myTabContent">
					<div class="tab-pane fade active show" id="home">
						<p>
							Raw denim you probably haven't heard of them jean shorts Austin. Nesciunt tofu
							stumptown aliqua, retro synth master cleanse. Mustache cliche tempor, williamsburg
							carles vegan helvetica. Reprehenderit butcher retro keffiyeh dreamcatcher synth. Cosby
							sweater eu banh mi, qui irure terry richardson ex squid. Aliquip placeat salvia cillum
							iphone. Seitan aliquip quis cardigan american apparel, butcher voluptate nisi qui.
						</p>
					</div>
					<div class="tab-pane fade" id="profile">
						<p>
							Food truck fixie locavore, accusamus mcsweeney's marfa nulla single-origin coffee
							squid. Exercitation +1 labore velit, blog sartorial PBR leggings next level wes
							anderson artisan four loko farm-to-table craft beer twee. Qui photo booth letterpress,
							commodo enim craft beer mlkshk aliquip jean shorts ullamco ad vinyl cillum PBR. Homo
							nostrud organic, assumenda labore aesthetic magna delectus mollit.
						</p>
					</div>
					<div class="tab-pane fade" id="dropdown1">
						<p>
							Etsy mixtape wayfarers, ethical wes anderson tofu before they sold out mcsweeney's
							organic lomo retro fanny pack lo-fi farm-to-table readymade. Messenger bag gentrify
							pitchfork tattooed craft beer, iphone skateboard locavore carles etsy salvia banksy
							hoodie helvetica. DIY synth PBR banksy irony. Leggings gentrify squid 8-bit cred
							pitchfork.
						</p>
					</div>
					<div class="tab-pane fade" id="dropdown2">
						<p>
							Trust fund seitan letterpress, keytar raw denim keffiyeh etsy art party before they
							sold out master cleanse gluten-free squid scenester freegan cosby sweater. Fanny pack
							portland seitan DIY, art party locavore wolf cliche high life echo park Austin. Cred
							vinyl keffiyeh DIY salvia PBR, banh mi before they sold out farm-to-table VHS viral
							locavore cosby sweater.
						</p>
					</div>
				</div>
			</div>
		</div>
		<div class="col-lg-6">
			<h3>Pills</h3>
			<div class="bs-component">
				<ul class="nav nav-pills">
					<!-- svelte-ignore a11y_invalid_attribute -->
					<li class="nav-item"><a class="nav-link active" href="#">Active</a></li>
					<li class="nav-item dropdown">
						<!-- svelte-ignore a11y_invalid_attribute -->
						<a
							class="nav-link dropdown-toggle"
							data-bs-toggle="dropdown"
							href="#"
							role="button"
							aria-haspopup="true"
							aria-expanded="false">Dropdown</a
						>
						<div class="dropdown-menu">
							<a class="dropdown-item" href="/bootstrap-components">Action</a>
							<a class="dropdown-item" href="/bootstrap-components">Another action</a>
							<a class="dropdown-item" href="/bootstrap-components">Something else here</a>
							<div class="dropdown-divider"></div>
							<a class="dropdown-item" href="/bootstrap-components">Separated link</a>
						</div>
					</li>
					<li class="nav-item"><a class="nav-link" href="/bootstrap-components">Link</a></li>
					<li class="nav-item">
						<a class="nav-link disabled" href="/bootstrap-components">Disabled</a>
					</li>
				</ul>
			</div>
			<br />
			<!-- svelte-ignore a11y_invalid_attribute -->
			<div class="bs-component">
				<ul class="nav nav-pills nav-stacked">
					<li class="nav-item"><a class="nav-link active" href="#">Active</a></li>
					<li class="nav-item dropdown">
						<a
							class="nav-link dropdown-toggle"
							data-bs-toggle="dropdown"
							href="#"
							role="button"
							aria-haspopup="true"
							aria-expanded="false">Dropdown</a
						>
						<div class="dropdown-menu">
							<a class="dropdown-item" href="#">Action</a><a class="dropdown-item" href="#"
								>Another action</a
							><a class="dropdown-item" href="#">Something else here</a>
							<div class="dropdown-divider"></div>
							<a class="dropdown-item" href="#">Separated link</a>
						</div>
					</li>
					<li class="nav-item"><a class="nav-link" href="#">Link</a></li>
					<li class="nav-item"><a class="nav-link disabled" href="#">Disabled</a></li>
				</ul>
			</div>
		</div>
	</div>
	<div class="row">
		<!-- svelte-ignore a11y_invalid_attribute -->
		<div class="col-lg-6">
			<h2 class="mb-3 line-head" id="nav-breadcrumbs">Breadcrumbs</h2>
			<div class="bs-component">
				<ol class="breadcrumb">
					<li class="breadcrumb-item active">Home</li>
				</ol>
				<ol class="breadcrumb">
					<li class="breadcrumb-item"><a href="#">Home</a></li>
					<li class="breadcrumb-item active">Library</li>
				</ol>
				<ol class="breadcrumb">
					<li class="breadcrumb-item"><a href="#">Home</a></li>
					<li class="breadcrumb-item"><a href="#">Library</a></li>
					<li class="breadcrumb-item active">Data</li>
				</ol>
			</div>
		</div>
		<div class="col-lg-6">
			<h2 class="mb-3 line-head" id="pagination">Pagination</h2>
			<div class="bs-component">
				<div>
					<!-- svelte-ignore a11y_invalid_attribute -->
					<ul class="pagination">
						<li class="page-item disabled"><a class="page-link" href="#">«</a></li>
						<li class="page-item active"><a class="page-link" href="#">1</a></li>
						<li class="page-item"><a class="page-link" href="#">2</a></li>
						<li class="page-item"><a class="page-link" href="#">3</a></li>
						<li class="page-item"><a class="page-link" href="#">4</a></li>
						<li class="page-item"><a class="page-link" href="#">5</a></li>
						<li class="page-item"><a class="page-link" href="#">»</a></li>
					</ul>
				</div>
				<div>
					<!-- svelte-ignore a11y_invalid_attribute -->
					<ul class="pagination pagination-lg">
						<li class="page-item disabled"><a class="page-link" href="#">«</a></li>
						<li class="page-item active"><a class="page-link" href="#">1</a></li>
						<li class="page-item"><a class="page-link" href="#">2</a></li>
						<li class="page-item"><a class="page-link" href="#">3</a></li>
						<li class="page-item"><a class="page-link" href="#">4</a></li>
						<li class="page-item"><a class="page-link" href="#">5</a></li>
						<li class="page-item"><a class="page-link" href="#">»</a></li>
					</ul>
				</div>
				<div>
					<!-- svelte-ignore a11y_invalid_attribute -->
					<ul class="pagination pagination-sm">
						<li class="page-item disabled"><a class="page-link" href="#">«</a></li>
						<li class="page-item active"><a class="page-link" href="#">1</a></li>
						<li class="page-item"><a class="page-link" href="#">2</a></li>
						<li class="page-item"><a class="page-link" href="#">3</a></li>
						<li class="page-item"><a class="page-link" href="#">4</a></li>
						<li class="page-item"><a class="page-link" href="#">5</a></li>
						<li class="page-item"><a class="page-link" href="#">»</a></li>
					</ul>
				</div>
			</div>
		</div>
	</div>
</div>

<!-- Indicators-->
<!-- svelte-ignore a11y_invalid_attribute -->
<div class="tile mb-4">
	<div class="row">
		<div class="col-lg-12">
			<div class="page-header">
				<h2 class="mb-3 line-head" id="indicators">Indicators</h2>
			</div>
		</div>
	</div>
	<div class="row">
		<div class="col-lg-12">
			<h4>Alerts</h4>
			<div class="bs-component">
				<div class="alert alert-dismissible alert-warning">
					<button class="btn-close" type="button" data-bs-dismiss="alert" aria-label="close"
					></button>
					<h4>Warning!</h4>
					<p>
						Best check yo self, you're not looking too good. Nulla vitae elit libero, a pharetra
						augue. Praesent commodo cursus magna, <a class="alert-link" href="#"
							>vel scelerisque nisl consectetur et</a
						>.
					</p>
				</div>
			</div>
		</div>
	</div>
	<div class="row">
		<div class="col-lg-4">
			<div class="bs-component">
				<div class="alert alert-dismissible alert-danger">
					<button class="btn-close" type="button" data-bs-dismiss="alert" aria-label="close"
					></button><strong>Oh snap!</strong><a class="alert-link" href="#"
						>Change a few things up</a
					> and try submitting again.
				</div>
			</div>
		</div>
		<div class="col-lg-4">
			<div class="bs-component">
				<div class="alert alert-dismissible alert-success">
					<button class="btn-close" type="button" data-bs-dismiss="alert" aria-label="close"
					></button><strong>Well done!</strong>
					You successfully read <a class="alert-link" href="#">this important alert message</a>.
				</div>
			</div>
		</div>
		<div class="col-lg-4">
			<div class="bs-component">
				<div class="alert alert-dismissible alert-info">
					<button class="btn-close" type="button" data-bs-dismiss="alert" aria-label="close"
					></button><strong>Heads up!</strong>
					This <a class="alert-link" href="#">alert needs your attention</a>, but it's not super
					important.
				</div>
			</div>
		</div>
	</div>
	<div>
		<h4>Badges</h4>
		<div class="bs-component mb-40">
			<span class="me-1 badge bg-primary">Primary</span><span class="me-1 badge bg-secondary"
				>Secondary</span
			><span class="me-1 badge bg-success">Success</span><span class="me-1 badge bg-danger"
				>Danger</span
			><span class="me-1 badge bg-warning">Warning</span><span class="me-1 badge bg-info">Info</span
			><span class="me-1 badge bg-light">Light</span><span class="me-1 badge bg-dark">Dark</span>
		</div>
		<div class="bs-component">
			<span class="me-1 badge badge-pill bg-primary">Primary</span><span
				class="me-1 badge badge-pill bg-secondary">Secondary</span
			><span class="me-1 badge badge-pill bg-success">Success</span><span
				class="me-1 badge badge-pill bg-danger">Danger</span
			><span class="me-1 badge badge-pill bg-warning">Warning</span><span
				class="me-1 badge badge-pill bg-info">Info</span
			><span class="me-1 badge badge-pill bg-light">Light</span><span
				class="me-1 badge badge-pill bg-dark">Dark</span
			>
		</div>
	</div>
</div>

<!-- Progress-->
<div class="tile mb-4">
	<div class="row">
		<div class="col-lg-12">
			<div class="page-header">
				<h2 class="mb-3 line-head">Progress</h2>
			</div>
			<h5 id="progress-basic">Basic</h5>
			<div class="bs-component mb-2">
				<div class="progress">
					<div
						class="progress-bar"
						role="progressbar"
						style="width: 25%;"
						aria-valuenow="25"
						aria-valuemin="0"
						aria-valuemax="100"
					></div>
				</div>
			</div>
			<h5 id="progress-alternatives">Contextual alternatives</h5>
			<div class="bs-component">
				<div class="progress mb-2">
					<div
						class="progress-bar bg-success"
						role="progressbar"
						style="width: 25%"
						aria-valuenow="25"
						aria-valuemin="0"
						aria-valuemax="100"
					></div>
				</div>
				<div class="progress mb-2">
					<div
						class="progress-bar bg-info"
						role="progressbar"
						style="width: 50%"
						aria-valuenow="50"
						aria-valuemin="0"
						aria-valuemax="100"
					></div>
				</div>
				<div class="progress mb-2">
					<div
						class="progress-bar bg-warning"
						role="progressbar"
						style="width: 75%"
						aria-valuenow="75"
						aria-valuemin="0"
						aria-valuemax="100"
					></div>
				</div>
				<div class="progress mb-2">
					<div
						class="progress-bar bg-danger"
						role="progressbar"
						style="width: 100%"
						aria-valuenow="100"
						aria-valuemin="0"
						aria-valuemax="100"
					></div>
				</div>
			</div>
			<h5 id="progress-multiple">Multiple bars</h5>
			<div class="bs-component">
				<div class="progress mb-2">
					<div
						class="progress-bar"
						role="progressbar"
						style="width: 15%"
						aria-valuenow="15"
						aria-valuemin="0"
						aria-valuemax="100"
					></div>
					<div
						class="progress-bar bg-success"
						role="progressbar"
						style="width: 30%"
						aria-valuenow="30"
						aria-valuemin="0"
						aria-valuemax="100"
					></div>
					<div
						class="progress-bar bg-info"
						role="progressbar"
						style="width: 20%"
						aria-valuenow="20"
						aria-valuemin="0"
						aria-valuemax="100"
					></div>
				</div>
			</div>
			<h5 id="progress-striped">Striped</h5>
			<div class="bs-component">
				<div class="progress mb-2">
					<div
						class="progress-bar progress-bar-striped"
						role="progressbar"
						style="width: 10%"
						aria-valuenow="10"
						aria-valuemin="0"
						aria-valuemax="100"
					></div>
				</div>
				<div class="progress mb-2">
					<div
						class="progress-bar progress-bar-striped bg-success"
						role="progressbar"
						style="width: 25%"
						aria-valuenow="25"
						aria-valuemin="0"
						aria-valuemax="100"
					></div>
				</div>
				<div class="progress mb-2">
					<div
						class="progress-bar progress-bar-striped bg-info"
						role="progressbar"
						style="width: 50%"
						aria-valuenow="50"
						aria-valuemin="0"
						aria-valuemax="100"
					></div>
				</div>
				<div class="progress mb-2">
					<div
						class="progress-bar progress-bar-striped bg-warning"
						role="progressbar"
						style="width: 75%"
						aria-valuenow="75"
						aria-valuemin="0"
						aria-valuemax="100"
					></div>
				</div>
				<div class="progress mb-2">
					<div
						class="progress-bar progress-bar-striped bg-danger"
						role="progressbar"
						style="width: 100%"
						aria-valuenow="100"
						aria-valuemin="0"
						aria-valuemax="100"
					></div>
				</div>
			</div>
			<h5 id="progress-animated">Animated</h5>
			<div class="bs-component">
				<div class="progress mb-2">
					<div
						class="progress-bar progress-bar-striped progress-bar-animated"
						role="progressbar"
						aria-valuenow="75"
						aria-valuemin="0"
						aria-valuemax="100"
						style="width: 75%"
					></div>
				</div>
			</div>
		</div>
	</div>
</div>

<!-- svelte-ignore a11y_invalid_attribute -->
<!-- Containers-->
<div class="tile mb-4">
	<div class="row">
		<div class="col-lg-12">
			<div class="page-header">
				<h2 class="mb-3 line-head" id="containers">Containers</h2>
			</div>
		</div>
	</div>
	<div class="row">
		<div class="col-lg-12">
			<h3>List groups</h3>
		</div>
	</div>
	<div class="row">
		<div class="col-lg-4">
			<div class="bs-component">
				<ul class="list-group">
					<li class="list-group-item d-flex justify-content-between align-items-start">
						Cras justo odio<span class="badge bg-primary rounded-pill">14</span>
					</li>
					<li class="list-group-item d-flex justify-content-between align-items-start">
						Dapibus ac facilisis in<span class="badge bg-primary rounded-pill">2</span>
					</li>
					<li class="list-group-item d-flex justify-content-between align-items-start">
						Morbi leo risus<span class="badge bg-primary rounded-pill">1</span>
					</li>
				</ul>
			</div>
		</div>
		<div class="col-lg-4">
			<div class="bs-component">
				<div class="list-group">
					<a class="list-group-item list-group-item-action active" href="#">Cras justo odio</a><a
						class="list-group-item list-group-item-action"
						href="#">Dapibus ac facilisis in</a
					><a class="list-group-item list-group-item-action disabled" href="#">Morbi leo risus</a>
				</div>
			</div>
		</div>
		<div class="col-lg-4">
			<div class="bs-component">
				<div class="list-group">
					<a class="list-group-item list-group-item-action active" href="#">
						<h4 class="list-group-item-heading">List group item heading</h4>
						<p class="list-group-item-text">
							Donec id elit non mi porta gravida at eget metus. Maecenas sed diam eget risus varius
							blandit.
						</p></a
					><a class="list-group-item list-group-item-action" href="#">
						<h4 class="list-group-item-heading">List group item heading</h4>
						<p class="list-group-item-text">
							Donec id elit non mi porta gravida at eget metus. Maecenas sed diam eget risus varius
							blandit.
						</p></a
					>
				</div>
			</div>
		</div>
	</div>
	<div class="row">
		<div class="col-lg-12">
			<h3>Cards</h3>
		</div>
	</div>
	<div class="row">
		<div class="col-lg-4">
			<div class="bs-component">
				<div class="card mb-3 text-white bg-primary">
					<div class="card-body">
						<blockquote class="card-blockquote">
							<p>
								Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a
								ante.
							</p>
							<footer>
								Someone famous in
								<cite title="Source Title">Source Title</cite>
							</footer>
						</blockquote>
					</div>
				</div>
				<div class="card mb-3 text-white bg-success">
					<div class="card-body">
						<blockquote class="card-blockquote">
							<p>
								Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a
								ante.
							</p>
							<footer>
								Someone famous in
								<cite title="Source Title">Source Title</cite>
							</footer>
						</blockquote>
					</div>
				</div>
				<div class="card mb-3 text-white bg-info">
					<div class="card-body">
						<blockquote class="card-blockquote">
							<p>
								Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a
								ante.
							</p>
							<footer>
								Someone famous in
								<cite title="Source Title">Source Title</cite>
							</footer>
						</blockquote>
					</div>
				</div>
				<div class="card mb-3 text-white bg-warning">
					<div class="card-body">
						<blockquote class="card-blockquote">
							<p>
								Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a
								ante.
							</p>
							<footer>
								Someone famous in
								<cite title="Source Title">Source Title</cite>
							</footer>
						</blockquote>
					</div>
				</div>
				<div class="card mb-3 text-white bg-danger">
					<div class="card-body">
						<blockquote class="card-blockquote">
							<p>
								Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a
								ante.
							</p>
							<footer>
								Someone famous in
								<cite title="Source Title">Source Title</cite>
							</footer>
						</blockquote>
					</div>
				</div>
				<div class="card mb-3 text-black bg-light">
					<div class="card-body">
						<blockquote class="card-blockquote">
							<p>
								Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a
								ante.
							</p>
							<footer>
								Someone famous in
								<cite title="Source Title">Source Title</cite>
							</footer>
						</blockquote>
					</div>
				</div>
				<div class="card mb-3 text-white bg-dark">
					<div class="card-body">
						<blockquote class="card-blockquote">
							<p>
								Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a
								ante.
							</p>
							<footer>
								Someone famous in
								<cite title="Source Title">Source Title</cite>
							</footer>
						</blockquote>
					</div>
				</div>
			</div>
		</div>
		<div class="col-lg-4">
			<div class="bs-component">
				<div class="card mb-3 border-primary">
					<div class="card-body">
						<blockquote class="card-blockquote">
							<p>
								Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a
								ante.
							</p>
							<footer>
								Someone famous in
								<cite title="Source Title">Source Title</cite>
							</footer>
						</blockquote>
					</div>
				</div>
				<div class="card mb-3 border-success">
					<div class="card-body">
						<blockquote class="card-blockquote">
							<p>
								Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a
								ante.
							</p>
							<footer>
								Someone famous in
								<cite title="Source Title">Source Title</cite>
							</footer>
						</blockquote>
					</div>
				</div>
				<div class="card mb-3 border-info">
					<div class="card-body">
						<blockquote class="card-blockquote">
							<p>
								Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a
								ante.
							</p>
							<footer>
								Someone famous in
								<cite title="Source Title">Source Title</cite>
							</footer>
						</blockquote>
					</div>
				</div>
				<div class="card mb-3 border-warning">
					<div class="card-body">
						<blockquote class="card-blockquote">
							<p>
								Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a
								ante.
							</p>
							<footer>
								Someone famous in
								<cite title="Source Title">Source Title</cite>
							</footer>
						</blockquote>
					</div>
				</div>
				<div class="card mb-3 border-danger">
					<div class="card-body">
						<blockquote class="card-blockquote">
							<p>
								Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a
								ante.
							</p>
							<footer>
								Someone famous in
								<cite title="Source Title">Source Title</cite>
							</footer>
						</blockquote>
					</div>
				</div>
				<div class="card mb-3 border-light">
					<div class="card-body">
						<blockquote class="card-blockquote">
							<p>
								Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a
								ante.
							</p>
							<footer>
								Someone famous in
								<cite title="Source Title">Source Title</cite>
							</footer>
						</blockquote>
					</div>
				</div>
				<div class="card mb-3 border-dark">
					<div class="card-body">
						<blockquote class="card-blockquote">
							<p>
								Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a
								ante.
							</p>
							<footer>
								Someone famous in
								<cite title="Source Title">Source Title</cite>
							</footer>
						</blockquote>
					</div>
				</div>
			</div>
		</div>
		<div class="col-lg-4">
			<div class="bs-component">
				<div class="card">
					<h4 class="card-header">Card header</h4>
					<div class="card-body">
						<h5 class="card-title">Special title treatment</h5>
						<h6 class="card-subtitle text-muted">Support card subtitle</h6>
					</div>
					<img
						style="height: 200px; width: 100%; display: block;"
						src="data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%22318%22%20height%3D%22180%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20viewBox%3D%220%200%20318%20180%22%20preserveAspectRatio%3D%22none%22%3E%3Cdefs%3E%3Cstyle%20type%3D%22text%2Fcss%22%3E%23holder_158bd1d28ef%20text%20%7B%20fill%3Argba(255%2C255%2C255%2C.75)%3Bfont-weight%3Anormal%3Bfont-family%3AHelvetica%2C%20monospace%3Bfont-size%3A16pt%20%7D%20%3C%2Fstyle%3E%3C%2Fdefs%3E%3Cg%20id%3D%22holder_158bd1d28ef%22%3E%3Crect%20width%3D%22318%22%20height%3D%22180%22%20fill%3D%22%23777%22%3E%3C%2Frect%3E%3Cg%3E%3Ctext%20x%3D%22129.359375%22%20y%3D%2297.35%22%3EImage%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3C%2Fsvg%3E"
						alt="Card"
					/>
					<div class="card-body">
						<p class="card-text">
							Some quick example text to build on the card title and make up the bulk of the card's
							content.
						</p>
						<a class="card-link" href="/">Card link</a><a class="card-link" href="/">Another link</a
						>
					</div>
					<div class="card-footer text-muted">2 days ago</div>
				</div>
			</div>
		</div>
	</div>
</div>

<!-- Dialogs-->
<div class="tile mb-4">
	<div class="row">
		<div class="col-lg-12">
			<div class="page-header">
				<h2 class="mb-3 line-head" id="dialogs">Dialogs</h2>
			</div>
		</div>
	</div>
	<div class="row">
		<div class="col-lg-6">
			<h4>Modals</h4>
			<div class="bs-component">
				<div
					class="modal"
					style="position: relative; top: auto; right: auto; left: auto; bottom: auto; z-index: 1; display: block;"
				>
					<div class="modal-dialog" role="document">
						<div class="modal-content">
							<div class="modal-header">
								<h5 class="modal-title">Modal title</h5>
								<button class="btn-close" type="button" data-bs-dismiss="modal" aria-label="Close"
									><span aria-hidden="true"></span></button
								>
							</div>
							<div class="modal-body">
								<p>Modal body text goes here.</p>
							</div>
							<div class="modal-footer">
								<button class="btn btn-primary" type="button">Save changes</button>
								<button class="btn btn-secondary" type="button" data-bs-dismiss="modal"
									>Close</button
								>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
		<div class="col-lg-6">
			<h4>Popovers</h4>
			<div class="bs-component" style="margin-bottom: 3em;">
				<button
					class="btn btn-secondary"
					type="button"
					data-bs-container="body"
					data-bs-toggle="popover"
					data-bs-placement="left"
					data-bs-content="Vivamus sagittis lacus vel augue laoreet rutrum faucibus."
					data-bs-title="Popover Title">Left</button
				>
				<button
					class="btn btn-secondary"
					type="button"
					data-bs-container="body"
					data-bs-toggle="popover"
					data-bs-placement="top"
					data-bs-content="Vivamus sagittis lacus vel augue laoreet rutrum faucibus."
					data-bs-title="Popover Title">Top</button
				>
				<button
					class="btn btn-secondary"
					type="button"
					data-bs-container="body"
					data-bs-toggle="popover"
					data-bs-placement="bottom"
					data-bs-content="Vivamussagittis lacus vel augue laoreet rutrum faucibus."
					data-bs-title="Popover Title">Bottom</button
				>
				<button
					class="btn btn-secondary"
					type="button"
					data-bs-container="body"
					data-bs-toggle="popover"
					data-bs-placement="right"
					data-bs-content="Vivamus sagittis lacus vel augue laoreet rutrum faucibus."
					data-bs-title="Popover Title">Right</button
				>
			</div>
			<h4>Tooltips</h4>
			<div class="bs-component">
				<button
					class="btn btn-secondary"
					type="button"
					data-bs-toggle="tooltip"
					data-bs-placement="left"
					data-bs-title="Tooltip on left">Left</button
				>
				<button
					class="btn btn-secondary"
					type="button"
					data-bs-toggle="tooltip"
					data-bs-placement="top"
					data-bs-title="Tooltip on top">Top</button
				>
				<button
					class="btn btn-secondary"
					type="button"
					data-bs-toggle="tooltip"
					data-bs-placement="bottom"
					data-bs-title="Tooltip on bottom">Bottom</button
				>
				<button
					class="btn btn-secondary"
					type="button"
					data-bs-toggle="tooltip"
					data-bs-placement="right"
					data-bs-title="Tooltip on right">Right</button
				>
			</div>
		</div>
	</div>
</div>
