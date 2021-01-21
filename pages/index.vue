<template>

<body>
  <div class="wrapper ">
    <Sidebar />
    <div class="main-panel">
      <!-- Navbar -->
      <nav class="navbar navbar-expand-lg navbar-transparent navbar-absolute fixed-top ">
        <div class="container-fluid">
          <div class="navbar-wrapper">
            <a class="navbar-brand" href="javascript:;">公共工事一覧</a>
          </div>
        </div>
      </nav>
      <div class="content">
        <div class="container-fluid">
          <div class="row">
            <div class="col-md-12">
              <div class="card">
                <div class="card-header card-header-primary">
                  <h4 class="card-title ">公共工事一覧</h4>
                  <p class="card-category">現在請け負っている案件の一覧です。</p>
                </div>
                <div class="card-body">
                  <div class="table-responsive">
                    <table class="table">
                      <thead class=" text-primary">
                        <th>ID</th>
                        <th>写真</th>
                        <th>請負年月日</th>
                        <th>地域</th>
                        <th>住所</th>
                        <th>単価</th>
                      </thead>
                      <tbody>
                        <tr>
                          <td>1</td>
                          <td><img src="~/assets/img/photo_01.jpg" alt="画像1" width="100"></td>
                          <td>2015年1月1日</td>
                          <td>関西</td>
                          <td>大阪府大阪市中央区1-1-1</td>
                          <td class="text-primary">1,000,000円</td>
                        </tr>
                        <tr>
                          <td>2</td>
                          <td><img src="~/assets/img/photo_02.jpg" alt="画像2" width="100"></td>
                          <td>2016年3月20日</td>
                          <td>関東</td>
                          <td>東京都中央区1-1-1</td>
                          <td class="text-primary">500,000円</td>
                        </tr>
                        <tr>
                          <td>3</td>
                          <td><img src="~/assets/img/photo_03.jpg" alt="画像3" width="100"></td>
                          <td>2018年7月12日</td>
                          <td>関西</td>
                          <td>大阪府大阪市中央区1-1-1</td>
                          <td class="text-primary">2,000,000円</td>
                        </tr>
                        <tr>
                          <td>4</td>
                          <td><img src="~/assets/img/photo_04.jpg" alt="画像4" width="100"></td>
                          <td>2010年11月1日</td>
                          <td>中部</td>
                          <td>岐阜県可児市姫ケ丘2丁目20番地</td>
                          <td class="text-primary">3,000,000円</td>
                        </tr>
                      </tbody>
                    </table>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</body>
</template>

<script>
import Sidebar from '@/components/Sidebar'
import Footer from '@/components/Footer'
export default {
  components: {
    Sidebar,
    Footer
  }
}
</script>