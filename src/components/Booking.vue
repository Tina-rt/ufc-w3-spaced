<script>
export default{
    
    data(){
        return {
            screenw: window.innerWidth
        }
    },
    mounted(){
        window.addEventListener('resize', ()=>{
            this.screenw = window.innerWidth
        })
    }
}
</script>


<template>
    <div class="booking">
        <div class="form-book">
            <table>
                <tr>
                    <td>
                        <div>LAUNCH PAD</div>
                        <select name="launch" id="">
                            <option value="SEA">SEA</option>
                            <option value="LAND">LAND</option>
                        </select>
                    </td>
                    <td>
                        <div for="">DESTINATION</div>
                        <select name="dest" id="">
                            <option value="MOON">MOON</option>
                            <option value="MARS">MARS</option>
                        </select>
                    </td>
                    <td>
                        <div for="">PASSENGERS</div>
                        <select name="passenger" id="">
                            <option value="1">1 ADULT</option>
                            <option value="2">2 ADULTS</option>
                        </select>
                    </td>
                    <td class="search-section">
                        <div class="btn-search">SEARCH</div>
                    </td>
                </tr>
                <tr class="search-section-resp" v-if="screenw < 600" >
                    <td colspan="3">
                        <div class="btn-search">SEARCH</div>

                    </td>
                </tr>
            </table>
        </div>
    </div>
</template>

<style scoped>
.booking{
    position: absolute;
    bottom: 0;
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: center;
    z-index: 11;
    transform: translateY(-50%);

}
.form-book{
    width: 100%;
    padding-inline: 100px;
}
.booking table{
    border-collapse: collapse;
    width: 100%;
}
.booking table, td{
    border: 0.5px solid rgba(255, 255, 255, 0.295);
    
}
.booking td{
    padding: 10px;
    width: 200px;
    height: 100px;
}
.booking td *{
    margin: 10px;
}

.booking select, .booking select:hover{
    width: 90%;
    background-color: transparent;
    color: white;
    padding: 10px;
    border: 0;
    border-color: transparent;
}

.btn-search{
    width: 100%;
    text-align: center;
}



@media (max-width: 600px) {
    .booking{
        /* transform: translateY(100%); */
        margin: 50px 0;
        position: unset;
    }
    .form-book{
        padding: 0;
    }
    .search-section{
        display: none;
    }
    
}

</style>