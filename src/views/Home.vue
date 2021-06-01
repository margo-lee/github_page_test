<script>
import TabContent from"@/components/TabContent.vue";
export default {
  name: 'Home',
  components: {
   TabContent
  }
}
</script>
<template>
 <a class="accesskey" href="#aC" id="aC" accesskey="C" title="主要內容區">:::</a>
        <section class="col-12">
          <div class="container">
            <TabContent/>
          </div>
        </section>
        <section class="col-12">
          <div class="container instruction_content">
            <h2 class="form_title"> <hr> <span> 申請人請詳細閱讀下列事項 </span><hr></h2>
            <form class="instruction_form" action="">
                <ul>
                  <li>(一)  本申請只適用於進出入烏來區桶后林道。林道開放車輛進出時間每日0600-1800。</li> 
                  <li>(二)  每次申請限填一輛，汽車限九人座以下小客車及機車。</li> 
                  <li>(三)  受理申請時間：民眾預定進入日期前3日至30日截止申請，以網路線上向新竹林區管理處申請，申請資料上傳後系統無提供修改功能，核准通行與否以電子郵件通知，亦可利用查詢系統自行查詢或下載許可單。</li> 
                  <li>(四)  請依許可時間進出入桶后林道並遵守「新北市烏來區桶后林道及鄰近區域生態維護管制措施」及相關規定，進入林道請持本處核准通知並於檢查哨主動出示受檢。未遵守相關規定者，將停止該車號半年內之申請權利。</li> 
                  <li>(五)  申請者核准後請依許可進入時間前往，如無法於申請時間前往，請於核准進入日期3天前，利用查詢系統註銷申請。</li> 
                  <li>(六)  林務局新竹林管處個人資料蒐集告知聲明</li> 
                </ul>
                <ol class="form_item">
                  <li>桶后林道車輛進入線上申辦系統(下稱本系統)係由林務局新竹林區管理處(下稱本處)建置維護，供一般民眾使用。</li>
                  <li>您應於提出申請時提供完整詳實且符合真實之個人資料，如有任何虛假或冒用他人名義登錄，應自負法律責任。若您提供之個人資料有填寫不實，或所登錄之資料已不符合真實而未更新，本處有權隨時註銷您的申請及使用各項服務之權利。</li>
                  <li>您有義務妥善保護自己的申請資料，並於每次使用完本系統後確實關閉視窗，以防他人盜用。為維護您自身權益，請勿將申請資料出借或轉讓他人使用。若您發現申請資料遭人非法使用或有其他任何安全問題發生時，應立即通知本處。</li>
                  <li>本處謹依據中華民國《個人資料保護法》及施行細則等相關規定，蒐集、處理及利用您於本系統所提供之資料，已依法採取適當安全維護措施，以避免您個人資料遭到外洩、竊取、竄改或其他不當利用；然依據中華民國《個人資料保護法》第28條規定，您的個人資料及權利倘因天災、事變或其他不可抗力、第三方不法蒐集等因素而遭致損害，中華民國政府無法負損害賠償責任。</li>
                  <li>本處保留隨時修改本同意書規範之權利，修改後的規範將於本系統首頁公告，不另作個別通知。如果您不同意修改的內容，請勿繼續使用本服務。倘若您繼續使用本處提供之服務，則表示您同意並接受本同意書規範之任何修改。</li>
                </ol>
            <div class="">
                <div class="check_grp">
                    <label><input name="checkSample" type="checkbox" value="">
                      以上說明，本人業已完全明瞭，並同意確實遵守相關規定。</label>
                </div>
            </div>
            <div class="form_text">
                <p>申請洽詢專線及網址：<br>
                    林務局新竹林區管理處育樂課　<br>
                    電話 (03)528-6629　傳真 (03)521-5454<br>
                    地址：300 新竹市中山路2號</p>
            </div>
            <div class="form_submit">
              <router-link to="/form"><button class="btn btn-submit">開始申請</button></router-link>
            </div>
            </form>
          </div>
        </section>
</template>