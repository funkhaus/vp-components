<script>

    export default {
        inserted (el, binding) {

            const offset = binding.arg

            window.addEventListener('scroll', () => {

                if (!el.getBoundingClientRect) return

                const rect = el.getBoundingClientRect()
                top = rect.top
                if (top <= offset){
                    let translateDist = (top - offset) * -1
                    el.style['transform'] = 'translateY(' + tr + 'px)'
                }
                else {
                    el.style['transform'] = ""
                }
            })
        }
    }

</script>

