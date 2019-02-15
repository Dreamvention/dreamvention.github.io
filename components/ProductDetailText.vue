<template>
    <div>
        <h2>{{icon_thumb.title}}</h2>
        <div class="mt-1">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris ultricies at neque eleifend consequat.
            Proin auctor enim quis magna tempor ornare. Curabitur blandit gravida vehicula. Fusce accumsan placerat
            velit id gravida.
            <ul v-for="item in li">
                <li>{{item}}</li>
            </ul>
        </div>
    </div>
</template>

<script>
	  export default {
        name: "ProductDetailText",
        props: ['icon_thumb'],
        data() {
            return {
				        li: ['First', 'Second', 'Third']
            }
        }
	  };
</script>

<style scoped>

</style>