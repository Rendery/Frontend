<template>
    <div class="item">
        <div class="icon">
            <slot name="icon"></slot>
        </div>
        <div class="details">
            <h3 class="heading">
                <slot name="heading"></slot>
            </h3>
            <div class="content">
                <slot></slot>
            </div>
        </div>
    </div>
</template>
<style scoped>
.item {
    display: flex;
    margin-top: 2rem;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
}

.icon {
    display: flex;
    place-items: center;
    place-content: center;
    width: 80px;
    height: 100%;
    background-color: #00f7ff;
    color: #fff;
    font-size: 2.5rem;
}

.details {
    flex: 1;
    padding: 1.5rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.heading {
    font-size: 1.5rem;
    font-weight: 500;
    color: var(--color-heading);
    margin-bottom: 1rem;
}

.content {
    font-size: 1.2rem;
    color: var(--color-text);
}

@media (min-width: 1024px) {
    .item {
        margin-top: 0;
        padding: 2rem calc(var(--section-gap) / 2);
    }

    .icon {
        width: 120px;
        height: 120px;
        font-size: 3.5rem;
        position: relative;
        left: 0;
        top: 0;
        border-radius: 50%;
        background-color: #fff;
        color: #00f7ff;
        box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
    }

    .item:before,
    .item:after {
        content: '';
        border-left: 1px solid var(--color-border);
        position: absolute;
        left: 60px;
        height: 100%;
    }

    .item:before {
        top: 0;
    }

    .item:after {
        bottom: 0;
    }

    .item:first-of-type:before {
        display: none;
    }

    .item:last-of-type:after {
        display: none;
    }
}
</style>
