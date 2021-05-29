<template>
    <div id="toolbar">
        <div class="toolbar-items">
            <i class="fas fa-columns"></i>
            <span>
                Template
            </span>
        </div>

        <div class="toolbar-items">
            <i class="fas fa-image"></i>
            <span>
                Photos
            </span>
        </div>

        <div class="toolbar-items">
            <i class="fas fa-shapes"></i>
            <span>
                Elements
            </span>
        </div>

        <div class="toolbar-items">
            <i class="fas fa-font"></i>
            <span>
                Texts
            </span>
        </div>

        <div class="toolbar-items">
            <i class="fas fa-music"></i>
            <span>
                Audio
            </span>
        </div>

        <div class="toolbar-items">
            <i class="fas fa-video"></i>
            <span>
                Video
            </span>
        </div>

        <div class="toolbar-items">
            <i class="fas fa-chalkboard"></i>
            <span>
                Background
            </span>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
    #toolbar{
        display: flex;
        padding: 10px;
        flex-direction: column;
        background: #222;
        color: #bbb;
        font-size: 12px;
        font-family:Verdana, 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, sans-serif;
    
    }

    .toolbar-items{
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: 17px 5px;
    }

    .toolbar-items > svg {
        font-size: 25px;
        margin-bottom: 5px;
        color: #bbb;
    }
</style>