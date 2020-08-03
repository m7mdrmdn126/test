<template>
    <div>
        <p> number of students {{ students_num }}</p>
    </div>
</template>

<script>
export default {
   props: [
       'students_num'
   ]
}
</script>