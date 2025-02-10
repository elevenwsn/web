<!-- 纯 CSS 实现 -->
<div class="menu-container">
    <button id="menu-button">&#8942;</button>
    <div class="menu">
        <a href="#">选项1</a>
        <a href="#">选项2</a>
        <a href="#">选项3</a>
    </div>
</div>

<style>
    .menu-container {
        position: relative;
        display: inline-block;
        float: right;
        margin: 20px;
    }

    #menu-button {
        background: none;
        border: none;
        font-size: 24px;
        cursor: pointer;
        padding: 10px;
    }

    .menu {
        display: none;
        position: absolute;
        right: 0;
        background-color: #f9f9f9;
        min-width: 120px;
        box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
        z-index: 1;
        border-radius: 4px;
        overflow: hidden;
        opacity: 0;
        transform: translateY(-10px);
        transition: opacity 0.3s ease, transform 0.3s ease;
    }

    #menu-button:focus + .menu,
    .menu:hover {
        display: block;
        opacity: 1;
        transform: translateY(0);
    }

    .menu a {
        color: black;
        padding: 12px 16px;
        text-decoration: none;
        display: block;
        transition: background-color 0.3s ease;
    }

    .menu a:hover {
        background-color: #ddd;
    }
</style>