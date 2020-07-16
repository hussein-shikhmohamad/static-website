<template>
    <section>
        <a @click="error">{{ aaa }}</a>
    </section>
</template>

<script>
    import setMeta from '../util/set_meta';

    const meta = {
        title: '',
        breadcrumb: '',
        classes: [''],
    };

    export default {
        name: 'Error',
        meta,
        head () {
            return setMeta(meta, this);
        },
        data () {
            return {
                aaa: 'aaa',
                bbb: 'bbb',
                ccc: 'ccc',
            };
        },
        mounted () {
            this.$data.aaa = 'hello';
            this.$data.ccc = null;
        },
        methods: {
            error () {
                this.$data.bbb = this.$data.ccc.slice(0, 1);
            },
        },
    };
</script>
