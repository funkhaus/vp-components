<script>

    export default {
        inserted (el, binding) {

            const offset = binding.arg || 0

            window.addEventListener('scroll', () => {

                const rect = el.getBoundingClientRect()

                if (!rect) return

                top = rect.top
                if (top <= offset){
                    let translateDist = (top - offset) * -1
                    el.style['transform'] = 'translateY(' + translateDist + 'px)'
                }
                else {
                    el.style['transform'] = ""
                }
            })
        }
    }

</script>
