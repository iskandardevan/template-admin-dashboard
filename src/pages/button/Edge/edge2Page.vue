<template>
<div class="card">
    <div class="card-header pb-0">
        <h3>Custom state buttons</h3>
        <settingPage /> <span>The <code>.btn</code> class used with <code>&lt;button&gt;</code>, <code>&lt;a&gt;</code> and <code>&lt;input&gt;</code> elements.</span>
    </div>
    <div class="card-body btn-showcase"><a class="btn btn-pill btn-primary" href="javascript:void(0)" data-toggle="tooltip" title="btn btn-primary" role="button">Link</a>
        <input class="btn btn-pill btn-secondary" type="button" value="Input" data-toggle="tooltip" title="btn btn-secondary">
        <input class="btn btn-pill btn-success" type="submit" value="Submit" data-toggle="tooltip" title="btn btn-success">
        <button class="btn btn-pill btn-info" type="submit" title="btn btn-info">Button</button>

    </div>
</div>
<div class="card">
    <div class="card-header pb-0">
        <h3>outline buttons</h3>
        <settingPage /><span>Add <code>.btn-pill</code> and <code>.btn-outline-*</code> class for button with outline</span>
    </div>
    <div class="card-body btn-showcase">
        <button class="btn btn-pill btn-outline-primary" type="button" title="btn btn-pill btn-outline-primary">Primary Button</button>
        <button class="btn btn-pill btn-outline-secondary" type="button" title="btn btn-pill btn-outline-secondary">Secondary Button</button>
        <button class="btn btn-pill btn-outline-success" type="button" title="btn btn-pill btn-outline-success">Success Button</button>
        <button class="btn btn-pill btn-outline-info" type="button" title="btn btn-pill btn-outline-info">Info Button</button>
        <button class="btn btn-pill btn-outline-warning" type="button" title="btn btn-pill btn-outline-warning">Warning Button</button>
        <button class="btn btn-pill btn-outline-danger" type="button" title="btn btn-pill btn-outline-danger">Danger Button</button>
        <button class="btn btn-pill btn-outline-light txt-dark" type="button" title="btn btn-pill btn-outline-light">Light Button</button>

    </div>
</div>
<div class="card">
    <div class="card-header pb-0">
        <h3>bold Border outline buttons</h3>
        <settingPage /><span>Add <code>.btn-pill</code> and <code>.btn-outline-*-2x</code> class for button with bold outline</span>
    </div>
    <div class="card-body btn-showcase">
        <button class="btn btn-pill btn-outline-primary-2x" type="button" title="btn btn-pill btn-outline-primary-2x">Primary Button</button>
        <button class="btn btn-pill btn-outline-secondary-2x" type="button" title="btn btn-pill btn-outline-secondary-2x">Secondary Button</button>
        <button class="btn btn-pill btn-outline-success-2x" type="button" title="btn btn-pill btn-outline-success-2x">Success Button</button>
        <button class="btn btn-pill btn-outline-info-2x" type="button" title="btn btn-pill btn-outline-info-2x">Info Button</button>
        <button class="btn btn-pill btn-outline-warning-2x" type="button" title="btn btn-pill btn-outline-warning-2x">Warning Button</button>
        <button class="btn btn-pill btn-outline-danger-2x" type="button" title="btn btn-pill btn-outline-danger-2x">Danger Button</button>
        <button class="btn btn-pill btn-outline-light-2x txt-dark" type="button" title="btn btn-pill btn-outline-light-2x">Light Button</button>

    </div>
</div>
<div class="card">
    <div class="card-header pb-0">
        <h3>outline Large buttons</h3>
        <settingPage /><span>Add <code>.btn-pill</code>,<code>.btn-outline-*</code> and <code>.btn-lg</code> class for large button</span>
    </div>
    <div class="card-body btn-showcase">
        <button class="btn btn-pill btn-outline-primary btn-lg" type="button" title="btn btn-pill btn-outline-primary btn-lg">Primary Button</button>
        <button class="btn btn-pill btn-outline-secondary btn-lg" type="button" title="btn btn-pill btn-outline-secondary btn-lg">Secondary Button</button>
        <button class="btn btn-pill btn-outline-success btn-lg" type="button" title="btn btn-pill btn-outline-success btn-lg">Success Button</button>
        <button class="btn btn-pill btn-outline-info btn-lg" type="button" title="btn btn-pill btn-outline-info btn-lg">Info Button</button>
        <button class="btn btn-pill btn-outline-warning btn-lg" type="button" title="btn btn-pill btn-outline-warning btn-lg">Warning Button</button>
        <button class="btn btn-pill btn-outline-danger btn-lg" type="button" title="btn btn-pill btn-outline-danger btn-lg">Danger Button</button>
        <button class="btn btn-pill btn-outline-light btn-lg txt-dark" type="button" title="btn btn-pill btn-outline-light btn-lg">Light Button</button>

    </div>
</div>
<div class="card">
    <div class="card-header pb-0">
        <h3>outline small buttons</h3>
        <settingPage /><span>Add <code>.btn-pill</code>,<code>.btn-outline-*</code> and <code>.btn-sm</code> class for small button</span>
    </div>
    <div class="card-body btn-showcase">
        <button class="btn btn-pill btn-outline-primary btn-sm" type="button" title="btn btn-pill btn-outline-primary btn-sm">Primary Button</button>
        <button class="btn btn-pill btn-outline-secondary btn-sm" type="button" title="btn btn-pill btn-outline-secondary btn-sm">Secondary Button</button>
        <button class="btn btn-pill btn-outline-success btn-sm" type="button" title="btn btn-pill btn-outline-success btn-sm">Success Button</button>
        <button class="btn btn-pill btn-outline-info btn-sm" type="button" title="btn btn-pill btn-outline-info btn-sm">Info Button</button>
        <button class="btn btn-pill btn-outline-warning btn-sm" type="button" title="btn btn-pill btn-outline-warning btn-sm">Warning Button</button>
        <button class="btn btn-pill btn-outline-danger btn-sm" type="button" title="btn btn-pill btn-outline-danger btn-sm">Danger Button</button>
        <button class="btn btn-pill btn-outline-light btn-sm txt-dark" type="button" title="btn btn-pill btn-outline-light btn-sm">Light Button</button>

    </div>
</div>
</template>

<script>
import {
    Tooltip
} from 'bootstrap/dist/js/bootstrap.esm.min'
export default {
    mounted() {
        new Tooltip(document.body, {
            selector: "[data-bs-toggle='tooltip']"
        })
    }
}
</script>
