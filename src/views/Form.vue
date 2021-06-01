<script>
export default {

}
</script>

<template>
  <section class="col-12">
          <div class="container application_content">
            <div class="form_title">
              <h2 class=""><span>/</span>申請表<span>/</span></h2>
              <p class="form_date">申請日期: 2021-05-02</p> 
            </div>   
            <form action="" class="application_form">
              <h3>申請人資料</h3>
              <div class="flex-form form_grid">
                  <div class="form_grp">
                      <label for="username" class="form_title">姓名 :</label>
                      <div class="form_content form_col-6-6 form_inline">
                        <input type="text" id="username" value="">
                      </div>
                  </div>
                  <div class="form_grp">
                      <label for="email" class="form_title">電子郵件信箱 :</label>
                      <div class="form_content form_col-6-6 form_inline">
                        <input name="email" type="email" id="email">
                      </div>
                  </div>
                  <div class="form_grp">
                    <label for="selectSample" class="form_title">居住縣市 :</label>
                    <div class="form_content form_col-6-6 form_inline">
                        <select id="selectSample" name="">
                            <option value="">臺北市</option>
                            <option value="">新北市</option>
                            <option value="">桃園市</option>
                            <option value="">臺中市</option>
                            <option value="">臺南市</option>
                            <option value="">高雄市</option>
                            <option value="">基隆市</option>
                            <option value="">新竹市</option>
                            <option value="">嘉義市</option>
                            <option value="">新竹縣</option>
                            <option value="">苗栗縣</option>
                            <option value="">彰化縣</option>
                            <option value="">南投縣</option>
                            <option value="">雲林縣</option>
                            <option value="">嘉義縣</option>
                            <option value="">屏東縣</option>
                            <option value="">宜蘭縣</option>
                            <option value="">花蓮縣</option>
                            <option value="">臺東縣</option>
                            <option value="">澎湖縣</option>
                            <option value="">金門縣</option>
                            <option value="">連江縣</option>
                        </select>
                    </div>
                  </div>                  
                  <div class="form_grp ">
                      <label for="phone" class="form_title">手機 :</label>
                      <div class="form_content form_col-6-6 form_inline">
                          <input name="phone" id="phone" type="tel">
                      </div>
                  </div>
                  <div class="form_grp">
                    <label for="phone" class="form_title">電話 :</label>
                    <div class="form_content form_col-3-5-4 form_inline">
                      <input name="phone" type="tel">
                      <input name="phone" type="tel">
                      <input name="phone" type="tel">
                    </div>
                  </div>
              </div>
              <!--  -->
              <h3>車輛資料</h3>
              <div class="form_grid flex-form">
                <div class="form_grp" role="group" aria-labelledby="fake-legend">
                  <label class="form_title">車種 :</label>
                  <div class="form_content" id="fake-legend">
                      <div class="radio_grp form_inline">
                          <label>
                              <input type="radio" name="sampleRadio5" value="" checked="">汽車</label>
                          <label>
                              <input type="radio" name="sampleRadio5" value="">機車</label>
                      </div>
                  </div>
                </div>
                <div class="form_grp ">
                      <div class="form_title ">預計進入日期 :</div>
                      <div class="form_content form_col-6-6 form_inline ">
                        <div class="calendar_div"></div>
                        <button>可申請餘額查詢</button>
                      </div>
                </div>
                <div class="form_grp">
                  <div class="form_title">車牌號碼 :</div>
                  <div class="form_content form_col-6-6 form_inline">
                      <label for="inputSample" class="label_hidden">雙欄1</label>
                      <input name="username" id="inputSample" type="text"><span>例如: ABC-123</span>
                  </div>
                </div>
                <div class="form_grp last-input">
                  <div class="form_title">乘坐人數(含駕駛) :</div>
                  <div class="form_content form_col-6-6 form_inline">
                      <label for="inputSample" class="label_hidden">雙欄1</label>
                      <input name="username" id="inputSample" type="text">
                  </div>
                </div>
              </div>
            </form>
          </div>
        </section>
</template>
<style lang="scss">
</style>
