<template>
  <div class="page">
    <app-header title="浙医二院" class="noflex">
      <i slot="back"></i>
    </app-header>
    <div class="wrapper main flex" ref="main">
      <div ref="left" class="maindept flex0">
        <ul>
          <li :class="[index==currentDept?'cover':'']" @click="currentDept=index" v-for="(item,index) in dept">
            {{item.deptName}}
          </li>
        </ul>
      </div>
      <div ref="right" class="subdept flex0">
        <ul>
          <router-link tag="li" to="/home/server/book/doc" :key="index" v-for="(item,index) in subDept">{{item.deptName}}</router-link>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
  import AppHeader from "../../../../components/app-header.vue"

  import {mainHeightMixin} from "../../../../lib/mixin"

  export default {
    mixins: [mainHeightMixin],
    data() {
      return {
        currentDept: 0,
        dept: [{
          "deptCode": "03",
          "deptList": [{
            "bookDeptId": 803,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 10,
            "deptCode": "03",
            "deptDescription": "内分泌代谢科建于1964年，首任科主任宋作珪教授。现任科主任为谷卫主任，副主任为任跃忠主任。谷卫主任现任中华医学会糖尿病学会及中国医师协会内分泌分会委员、浙江中华医学会内分泌学会候任主委，浙江中西医结合糖尿病学会副主任委员，中华内分泌代谢杂志，中国糖尿病杂志，浙江医学杂志和浙江心脑血管防治杂志编委。任跃忠主任现任浙江医学会内分泌学会委员。\n主治疾病：下丘脑-垂体、甲状腺、甲状旁腺、肾上腺、胰腺内分泌及性腺疾病，肥胖、糖尿病、高尿酸血症、低血糖症、骨质疏松、血脂异常等。\n团队：医师19人，护士15人，技师2人、专科护士2人。主任医师4名，副主任医师3名。75%具有博士学位。\n",
            "deptName": "内分泌科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 820,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 40,
            "deptCode": "03",
            "deptDescription": "浙医二院呼吸内科成立于上世纪60年代，现为中华医学会呼吸分会副主任委员所在单位，是浙江省呼吸疾病科研、教学、诊断与治疗中心之一。现有教授，主任医师7名（其中教育部长江特聘教授1名），副教授、副研究员、副主任医师共10名，主治医师17人。学科专长为：慢性气道疾病的基础与临床防治研究；胸部疾病的介入诊断和治疗；肺癌的联合诊治；难治性、危重症的肺部感染性疾病治疗；睡眠呼吸障碍疾病的综合治疗；肺部少见病、罕见病和疑难病的诊治。近年来，学科获国家杰出青年科学基金、重点项目、国际(地区)合作与交流项目多项，承担国家十一五支撑项目、973课题、863子课题各多项。2010年获浙江省科技进步一等奖，2012年获教育部科学技术进步奖一等奖，2013年获国家科技进步奖二等奖。",
            "deptName": "呼吸内科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 831,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "03",
            "deptDescription": "暂无",
            "deptName": "干部保健科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 841,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 5,
            "deptCode": "03",
            "deptDescription": "浙江大学医学院附属第二医院心血管内科创建于1989年，是浙江省第一个独立从事心血管疾病预防和治疗的专门学科，已经成为浙江省心血管内科学临床、教学、科研中心之一，是浙江省卫生厅重点学科。现有教授（主任医师）8名，副教授（副主任医师）10名，主治医师4人，均具有博士或硕士学位。 \n开展目前国内外各项介入技术。是国内最早开展经皮球囊二尖瓣成形术和起搏器植入手术的单位之一。省率先开展经桡动脉途径行冠心病介入治疗，开展各类起搏器植入手术。引进国外最新的CARTO系统，每年完成各类射频消融手术，达国内先进水平。目前治疗的疾病包括：阵发性室上性心动过速、房性心动过速、心房扑动、室性心动过速和心房颤动。近年来，完成各类先心病介入治疗手术数百例。冠心病、干细胞研究等领域是浙医二院心血管内科研究的主攻方向。在干细胞移植治疗心血管疾病等方面取得了较大的成绩，发表一大批有影响的学术论文。\n",
            "deptName": "心血管内科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 856,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 8,
            "deptCode": "03",
            "deptDescription": "浙医二院放疗科创建于1957年7月，是浙江省综合性医院中规模最大的肿瘤放疗专科，所在浙医二院肿瘤学科是国家重点学科和国家临床重点专科，是硕士及博士学位授予点，承担临床教学科研任务，在国内享有很高的地位。目前，放疗科床位60张，现有在编医务人员42人，包括主任医师2名，副高职称5名。其中博导1名，硕导2名。",
            "deptName": "放疗科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 869,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 10,
            "deptCode": "03",
            "deptDescription": "浙医二院消化内科于1960年成立，目前拥有消化专科病房（包括解放路院区及滨江院区2个病区）、内镜中心、胃肠实验室和胃肠动力室，是浙江省消化病临床诊疗和教学科研的中心之一。科室有博士生导师4人，硕士生导师10人；承担浙江全省及其周边省市消化系统常见病及疑难、危重病的诊治工作。内镜中心拥有国际最先进的奥林巴斯、富士能胃肠镜系列，电子超声内镜以及单气囊小肠镜、胶囊内镜系统，在消化内镜的诊治方面处于领先水平。目前科室有以下几方面特色诊疗技术：ERCP（治疗胆总管结石、急性胰腺炎、梗阻性黄疸等）、ESD（应用于胃食管、结直肠癌前病变，无转移早期癌以及黏膜下肿瘤等）、超声内镜、胶囊内镜、小肠镜，并常规开展HP的各项检测包括呼气实验、HP培养等，此外还设有炎症性肠病、脂肪肝、胃食管反流病专科门诊。",
            "deptName": "消化内科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 897,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 2,
            "deptCode": "03",
            "deptDescription": "浙医二院皮肤科是集皮肤性病学临床、教学、科研于一体的国家级临床重点专科，设有皮肤病理、医学真菌、皮肤美容激光、皮肤外科、性传播疾病等皮肤亚专科，在银屑病、湿疹、系统性红斑狼疮、过敏、脱发以及疑难危重症皮肤病的诊治方面有着明显的学科优势和丰富的临床诊治经验，在国内省内皮肤病学界一直享有盛誉。我科作为浙江大学医学院皮肤性病学科点负责单位，至今已为国内外、省内外培养出各类皮肤病学专业人才超千人以上，在全国各地医院发挥着骨干作用。并与美国、德国、日本等大学有多项合作研究，承担多项国内外重点科研项目，在国内外顶级医学杂志上发表论文300余篇。 ",
            "deptName": "皮肤科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 909,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 2,
            "deptCode": "03",
            "deptDescription": "神经内科创建于1955年，目前开放床位150张，共有医师36名，其中在职教授2名，主任医师12名，副教授4名，副主任医师8名，主治医师7名。国外学习1年以上的医生有10名，博士生导师4名，硕士导师6名。本科室主要包括卒中单元（中风病房）、癫痫及神经系统感染病区、运动障碍性疾病等病房。\n专科特色门诊有：癫痫、老年神经病、帕金森病、神经遗传病、头痛、脑血管病、肌病周围神经病、记忆障碍痴呆等。神经内科一直全面担负着浙江省内各地、市、县的医疗会诊工作、神经科进修医师的培训和高级干部的保健工作，以及全省、周边省的神经科危重病和疑难病诊治。近来在基因分子研究基础上，开展了神经、肌肉活检，结合神经解剖和功能影像（核磁共振-MR、正电子发射断层扫描－PET）等，对周围神经、肌肉、大脑的变性、遗传、炎症、血管等疾病作了深入的研究，在临床上有着丰富的诊断和治疗经验。\n",
            "deptName": "神经内科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 918,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 1,
            "deptCode": "03",
            "deptDescription": "浙医二院精神科为三级甲等综合医院独立专科，集临床、教学、科研于一体。擅长收治各类精神障碍及心理疾病，设有精神科门诊、心理卫生病房、心理治疗室、心理研究室、精神病学教研室，开设心理保健、远程会诊和远程教育工作，同时开展针对患者和家属的疾病健康教育项目，延伸医疗服务。目前有主任医师2名（其中硕士生导师2名），副主任医师4名，主治医师5名，住院医师2名，副主任技师1名，均具有硕士及以上学位；护理人员10名，均具有大专以上学位。",
            "deptName": "精神科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 937,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "03",
            "deptDescription": "肾内科为卫生部肾脏病学专科医生培训基地及浙江省医学重点学科。拥有教授及主任医师4名，副主任医师2名，硕士生导师3名，医学博士7人，硕士6人。病房床位30张，血液净化中心床位50张（含滨江院区），自动腹膜透析机1台。年门诊量逾3万，出院人数逾千例。对肾脏科的常见病多发病有丰富的临床诊治经验，尤其擅长诊治疑难危重肾病，包括遗传性肾病如Gitelman综合征，以及各种不明原因急性肾衰。与肾移植中心合作，建立了从非透析治疗，血液透析、腹膜透析至肾移植的慢性肾脏病一体化治疗模式。近年大力发展腹膜透析技术，每年新增腹透患者近60例，率先进行腹膜透析患者管理的持续质量改进，在减少腹膜炎发生率，改善患者营养状态方面具有独特的优势。承担多项国家级省部级自然科学基金项目，科研成果发表于国内外TOP学术杂志。",
            "deptName": "肾脏内科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 963,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 3,
            "deptCode": "03",
            "deptDescription": "浙二医院血液内科成立于1970年，是省首批医学重点学科，卫生部首批造血干细胞移植认证单位，卫生部临床药物试验基地和浙江大学内科学血液病博士生培养点，集临床、科研和教学为一体。\n浙二血液是中华骨髓库、台湾慈济骨髓库和上海脐血库的协作单位。2008年加入全国关注骨髓瘤患者健康宣教的彩虹计划，开展靶向性药物联合造血干细胞移植的治疗方案。2010年借助UCLA病理诊断平台启动成人淋巴瘤精确诊断和规范化、个体化综合治疗。基础科研方面拥有高层次梯度团队，侧重于白血病发病机制的研究和靶向性抗肿瘤新药的研发。现设有普通门诊，专家门诊，名医馆VIP门诊，亚专业分组为：白血病治疗组、骨髓瘤/淋巴瘤治疗组和移植治疗组。 擅长诊治各种贫血、白血病、淋巴瘤 、骨髓瘤等恶性血液疾病。\n现设有微信公众号\"浙二血液\"面向大众科普宣教。\n",
            "deptName": "血液内科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 972,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 1,
            "deptCode": "03",
            "deptDescription": "由浙医二院与美国加州大学洛杉矶分校（UCLA）联合建立，美国专家Dr. Lin担任主任，主治范围为过敏性鼻炎、过敏性哮喘、过敏性结膜炎、异位性皮炎、荨麻疹、血管性水肿以及系统性过敏性疾病。过敏科引入美国标准化脱敏治疗流程，建立规范的脱敏治疗中心。至今已为400余例过敏性鼻炎、哮喘、异位性皮炎患者脱敏，疗效显著。",
            "deptName": "过敏科(变态反应科)",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 982,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 2,
            "deptCode": "03",
            "deptDescription": "浙医二院风湿科于2002年11月正式独立建科，拥有一支专业素质良好和不断进取的学术团队，在省内最早开展风湿病诊断治疗和风湿免疫实验室检查，在浙江省处于领先地位。科室医师共15人，其中教授及主任医师3人，副主任医师1人，主治医师6人，住院医师5人，均具有博士或硕士学位。科室主任吴华香现任浙江省医学会风湿病学分会主任委员，中华医学会风湿病学分会常务委员，《中华风湿病学杂志》、《浙江医学》编委。目前设专科门诊及病房，固定床位41张。",
            "deptName": "风湿免疫科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }],
          "deptName": "内科"
        }, {
          "deptCode": "04",
          "deptList": [{
            "bookDeptId": 834,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 1,
            "deptCode": "04",
            "deptDescription": "浙江大学医学院附属第二医院心脏大血管外科是省内第一家以心脏大血管外科建制的科室。经过心脏外科几代人的不懈努力和积极进取，浙医二院心脏大血管外科在许多方面达到国内先进水平，成为省内领先。",
            "deptName": "心脏大血管外科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 858,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "04",
            "deptDescription": "浙医二院整形外科是浙江省最早成立（1983年）的整形专科，医教研实力居省内领先地位，1996年设立硕士点。目前共有核定床位32张，医护人员20名，其中主任医师2名，副主任医师4名，主治医师3名。主要开展项目为：1.创伤的修复成形，包括各种类型的手外伤，断指（肢）再植及再造。2.各种良、恶性溃疡创面的修复。3.体表肿瘤的诊治：包括体表各种良恶性肿瘤，如基底细胞癌、鳞癌、恶性黑色素瘤、隆突性皮纤维肉瘤、纤维瘤、脂肪瘤、血管瘤等等。4.瘢痕的治疗：包括各种瘢痕的手术治疗，磨削术，放射治疗，激光治疗及功能重建等。5.各种先天性/继发性畸形，包括唇裂、腭裂、上睑下垂、半面萎缩症、面瘫、小口畸形、耳廓再造、眼窝再造、斜颈、多（并）指、血管瘤、两性畸形、乳房再造等等。6.美容外科：（1）面部整形：重睑、隆鼻、驼峰鼻矫正、除眼袋、面部除皱、面部轮廓成形等。（2）体形重塑：隆乳、巨乳缩小、脂肪抽吸，丰臀等。",
            "deptName": "整形科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 861,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 5,
            "deptCode": "04",
            "deptDescription": "浙医二院外科创建于1869年，历史悠久，底蕴深厚。目前学科带头人为梁廷波、吴育连教授，梁廷波教授为教育部长江学者，国家杰出青年基金获得者，两人均为浙江大学求是特聘教授、卫生部中青年突出贡献专家。学科目前共设8个病区， 280余张床位，分设肝胆胰、胃肠、甲状腺等六个亚专业。2012年外科凭借突出的临床、科研及创新能力获卫生部国家重点专科。",
            "deptName": "普外科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 865,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 1,
            "deptCode": "04",
            "deptDescription": "浙江大学医学院附属第二医院泌尿外科始建于1998年，分设泌尿外科住院部、泌尿外科门诊部、泌尿外科手术室、膀胱镜检查治疗室、男科检查实验室、尿动力检查室。泌尿外科以内窥镜手术技术应用为其特色，配备电子膀胱镜、经皮肾镜、纤维输尿管软镜、输尿管肾镜、等离子电切镜、泌尿外科检查床等国际最先进的内腔镜手术设备，开展经尿道前列腺切除术、钬激光碎石术以及各类腹腔镜手术，内腔镜手术占全部手术的比率高达 80% 左右，处国内前列水平。 尤其是经尿道钬激光前列腺剜除术为国内率先开展，迄今已成功实施该手术3000余例，为全国之最，也因此被全国医学会泌尿外科学会指定为唯一的前列腺增生症钬激光治疗指南制定单位。 \n浙二泌尿外科还开展了包括前列腺癌根治术、原位膀胱术、肾移植术、男科假体植入术等难度较大手术在内的所有泌尿外科常规手术，并开展了前列腺癌近距离放射治疗等一些新技术特色治疗。\n",
            "deptName": "泌尿外科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 876,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "04",
            "deptDescription": "我科成立于1958年，为国内最早成立的烧伤专科之一。被省卫生厅批准为\"浙江省烧伤救治技术指导中心\"。 2004年在国内率先创立\"伤口治疗中心\"， 2007年起，我科成为省卫生厅医学重点学科建设单位，并于2010年11月顺利通过验收。诊治范围包括：①各类烧伤：包括火焰烧伤、烫伤、电烧伤、化学烧伤、放射性烧伤、爆炸伤等，以及烧伤后功能康复及疤痕整形；②各类皮肤软组织缺损：包括皮肤撕脱伤、挤压伤、软组织缺损或坏死、骨外露等；③各类急慢性创面：包括压疮（褥疮）、糖尿病足等各种慢性溃疡及体表脓肿、甲沟炎、慢性骨髓炎等感染创口。半个多世纪来救治烧伤病人上万名，最大烧伤面积达100%，救治成功率（LA50）为94%。我科曾承担国家级、省部级课题10余项，在国内外发表论文100余篇，主编和参编出版专著10余部，获省科技厅奖项3项，培养硕士、博士研究生20余名，承担浙大医学院外科总论教学工作。",
            "deptName": "烧伤科(伤口治疗中心)",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 912,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 1,
            "deptCode": "04",
            "deptDescription": "浙医二院神经外科成立于1957年，是浙江省神经外科的发源地和龙头单位。\"看脑外，到浙二\"早已成为老百姓的共识。它还是我省神经外科医师的摇篮。建科以来共培养进修医师近700名，研究生160多名，遍布省内外，在各地发挥着重要的骨干作用。全省约70%的神经外科骨干经过\"浙二\"的进修和培训。浙医一院、邵逸夫医院和浙医四院神经外科主任均出自\"浙二\"。作为首批\"国家临床重点专科\"，其专科声誉排行榜位列全国前十。科主任张建民教授是我国著名神经外科专家，在脑血管病手术和垂体瘤领域享有盛誉。科室分布于解放路和滨江两个院区，开放床位230张，下辖6个病区，分别从事脑血管病、神经肿瘤、颅脑创伤、功能神经外科、脊柱脊髓外科、神经介入及小儿神经外科等8个亚专业，全面开展相应的核心和疑难手术。年手术量（含介入）5500余台。",
            "deptName": "神经外科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 948,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "04",
            "deptDescription": "暂无",
            "deptName": "胸外科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 953,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "04.03",
            "deptDescription": "脊柱微创专科",
            "deptName": "脊柱微创专科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 965,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "04",
            "deptDescription": "血管外科",
            "deptName": "血管外科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 987,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 2,
            "deptCode": "04",
            "deptDescription": "浙江大学医学院附属第二医院骨科，创建于1952年，成立时就是浙江省内成立最早、规模最大的骨科专科。经过几代人半个多世纪坚持不懈的努力，现已发展成为在国内外具有一定影响力，集医疗、教学、科研为一体协调发展的骨科临床和基础研究基地。科室目前分跨解放滨江两院区，合计固定病床288张（很快就要扩增到370张床位），年门急诊量达20万余人次，年手术量达1万例。关节及运动医学、脊柱、手与骨创伤、骨肿瘤及足踝外科四大临床治疗中心，七大专业方向，涵盖了现代主流的临床治疗手段与技术。",
            "deptName": "骨科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }],
          "deptName": "外科"
        }, {
          "deptCode": "05",
          "deptList": [{
            "bookDeptId": 825,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 1,
            "deptCode": "05",
            "deptDescription": "浙江大学医学院附属第二医院妇科现有医护人员40余人，其中医生20人，教授1名，主任医师4名，副主任医师3名，主治医师6名，其中博士生导师1名，硕士生导师3名。近年来，承担了国家863计划课题，国家自然科学基金，省自然基金等项目。发表多篇SCI论文。在卵巢癌、宫颈癌、子宫内膜癌、子宫内膜异位症、不孕不育和子宫肌瘤等妇科常见病及疑难病的治疗中有鲜明特色。90%以上的妇科手术在内镜下完成，定期举办子宫内膜异位症与不孕、妇科内窥镜手术学习班，接受来自全国各地的进修人员培训；引进了国际先进的高强度聚焦超声技术和射频子宫内膜消融技术，非手术无创治疗子宫肌瘤、子宫腺肌症、子宫出血等疾病。与美国UCLA里根医学中心建立了长期合作。",
            "deptName": "妇科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 881,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "05",
            "deptDescription": "中心目前主要开展以下特色诊疗活动：输卵管因素、排卵障碍、卵巢早衰、子宫内膜异位症以及多囊卵巢综合征等女性不孕症的诊治；男性精索静脉曲张、少弱精子症及畸形精子症等男性不育症的诊治。包括实施人工授精等辅助生殖技术，宫腹腔镜联用微创手术。习惯性流产，家族性、遗传性疾病的健康生育咨询，以及青春期、围绝经期等妇科内分泌疾病治疗。并定期举办不孕症患者义诊和生殖健康咨询活动。",
            "deptName": "生殖医学科(不孕不育)",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }],
          "deptName": "妇产科"
        }, {
          "deptCode": "07",
          "deptList": [{
            "bookDeptId": 801,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "07",
            "deptDescription": "浙江大学医学院附属第二医院儿科成立于2013年，立足于浙医二院综合医疗平台，是一个以研究小儿神经系统疾病为重点，兼顾新生儿疾病、儿童内分泌疾病及儿内科常见病、疑难病、基础医学及儿童保健为一体的医疗机构。儿科病房颇具现代儿科医院的特点，突出\"以人为本\"的新理念，为小患者营造了温馨、舒适、便利的就诊环境和就医条件。儿科病房为满足不同层次患者的需求，建有新生儿监护病房、普通双人病房、VIP单人病房，可收治各种儿科疾病的病人，尤其具有先进的诊治、抢救新生儿的仪器设备和经验。科室积极开展多科室合作，结合神经内外科，精神科的技术为儿童癫痫、多动症、抽动症、脑发育不全、脑炎、神经遗传性疾病等提供更全面，细致的诊治。",
            "deptName": "儿科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }],
          "deptName": "儿科"
        }, {
          "deptCode": "10",
          "deptList": [{
            "bookDeptId": 902,
            "bookHosId": 1,
            "deptAge": "0",
            "deptCode": "10",
            "deptDescription": "浙医二院眼科中心是浙江大学眼科研究所所在地和浙江大学眼科学依托单位，是国家重点（培育）学科。自1997年创立以来，在中心主任姚克教授的带领下，经过十几年精彩纷呈的创业历程，已经发展成为一所年门诊量达40万人次、年手术量4万余台，综合实力跻身国内前5位的大型现代化眼科中心。浙二眼科中心是一所集医疗、教学、科研为一体的具有鲜明专科特色的研究型的眼科中心。拥有总价值近1亿元的诊疗设备和仪器，绝大部分设备是从美国、德国、瑞士、日本等国进口的国际知名品牌，硬件设施达到了发达国家的先进水平。拥有15间现代化的眼科手术室，净化规格达到国际标准100级，是国内单体数量规模最大的眼科手术室。中心设有白内障、玻璃体视网膜病、青光眼、屈光手术、小儿与斜视弱视、肿瘤及眼整形、眼表及角膜病、眼视光等8大专业学组，开展全方位的眼科诊疗和手术。眼科诊疗和手术水平始终处于国内领先，国际先进水平。\n\n",
            "deptName": "眼科中心门诊",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }],
          "deptName": "眼科"
        }, {
          "deptCode": "11",
          "deptList": [{
            "bookDeptId": 927,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 2,
            "deptCode": "11",
            "deptDescription": "耳鼻咽喉科始建于1952年，在浙江省该学科领域建科最早。学科前辈蔡钺侯、王辉萼和邢昌全教授在我国耳鼻咽喉科学界享有很高声誉。上世纪70年代完成浙江省首例喉癌全喉切除发音重建手术，90年代率先开展内镜下鼻颅底和鼻眼相关手术，本世纪初率先开展人工耳蜗植入手术和喉显微激光手术。六十多年来，凭借耳显微外科手术、内镜下鼻颅底手术、喉肿瘤显微激光切除手术以及喉癌、喉咽癌等头颈部肿瘤根治性手术的优势，耳鼻咽喉科在省内外均享有盛誉。",
            "deptName": "耳鼻咽喉科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }],
          "deptName": "耳鼻咽喉科"
        }, {
          "deptCode": "12",
          "deptList": [{
            "bookDeptId": 814,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "12",
            "deptDescription": "暂无",
            "deptName": "口腔修复科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 815,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "12",
            "deptDescription": "浙二医院口腔内科创建于1947年。设牙周病、粘膜病和牙体牙髓病3个专科。 科室拥有国际先进的Clinview数字化牙科摄片机、根管显微镜、根尖定位仪、冷光牙齿美白仪、激光治疗仪、超声龈上龈下洁治仪、进口综合治疗椅等设备。同时，科室在省内首先设立了流程规范、仪器先进、专人负责操作的口腔消毒室。\n",
            "deptName": "口腔内科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 816,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 3,
            "deptCode": "12",
            "deptDescription": "浙医二院口腔颌面外科始建于1947年，是浙江省内成立最早、规模最大、技术力量最强的专业科室，拥有一支业务力量雄厚﹑结构合理﹑高素质的学科队伍，其中教授/主任医师5名，副教授/副主任医师5名，博/硕士研究生导师6名，先后主持承担国家自然科学基金、省自然科学基金、省科技厅、卫生厅、教育厅等多个科研项目。多次获得省科技进步奖和省医药卫生科技进步奖。现拥有浙江省最大的诊疗中心，核定床位73张，本科室医疗特色包括：口腔颌面颈部肿瘤诊治、口腔种植、口腔颌面部缺损及畸形整复、口腔颅颌面创伤、牙及牙槽外科、颞下颌关节疾病、正颌外科等，联合多学科开展鼾症和睡眠呼吸暂停低通气综合症的诊断和正颌外科手术治疗。2014年9月起在我院滨江院区成立新病区，进一步提升医疗环境与医疗质量。",
            "deptName": "口腔外科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 819,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "12",
            "deptDescription": "暂无",
            "deptName": "口腔正畸科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }],
          "deptName": "口腔科"
        }, {
          "deptCode": "19",
          "deptList": [{
            "bookDeptId": 939,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "19",
            "deptDescription": "浙医二院肿瘤内科是浙江省综合医院最早成立的化疗专科（1989），所在肿瘤学科是国家重点学科，全国著名肿瘤专家郑树教授和张苏展教授是学科点带头人。科室现有医师18名，其中主任医师3人，副主任医师5人，主治医师9人, 住院医师1人。科室在两个院区共60张床位；分设胸部肿瘤组和消化道肿瘤组。",
            "deptName": "肿瘤内科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 941,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "19",
            "deptDescription": "肿瘤外科突出了以乳腺肿瘤和大肠肿瘤为特色的综合治疗体系，开展了国际上先进的保留乳房的乳癌根治性手术，乳腺肿瘤的微创切除术，乳腺癌术后的整形再造术，低位直肠癌的保肛手术，大肠癌的微创外科治疗等治疗措施；对于肝转移癌和复发性肿瘤的再手术治疗以已形成了突出的治疗优势；高强度超声聚焦治疗为晚期肿瘤提供了有效的姑息治疗手段；在国内率先开展多学科综合治疗团队协作（ MDT）模式有计划地，合理地应用现有治疗手段进行肿瘤综合治疗，使治疗效果和病人利益达到最大化，多种肿瘤治疗效果已达到国际先进水平。",
            "deptName": "肿瘤外科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }],
          "deptName": "肿瘤科"
        }, {
          "deptCode": "50",
          "deptList": [{
            "bookDeptId": 794,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "50",
            "deptDescription": "浙医二院中医科建科50余年，经历了半个多世纪的发展和几代人的努力，科室已成为集临床、教学、科研为一体的综合学科。科室目前有医师12人，其中主任医师4人，副主任医师7人，硕士以上学历7人。\n科室人员努力继承和发扬祖国传统医学，汲取了伤寒、温病、金匮等各家学说的临证思维和用药精髓，不断创新，形成了各具特色的中医诊疗专长。对各系统疾病如心脑血管疾病、妇科疾病、消化系统疾病、风湿免疫系统疾病、呼吸系统疾病、泌尿系统疾病等治疗均积累了丰富的诊治经验，对各类肿瘤手术前后及放化疗后的治疗亦有丰富的临床经验。科室为浙江大学中西医结合临床硕士学位授予点。\n全科人员将坚持\"患者与服务对象至上\"的核心价值观，秉承\"大医精诚\"的医德医风，勤求古训 博采众方，竭诚为广大患者提供真诚、贴心的服务。\n",
            "deptName": "中医科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }],
          "deptName": "中医科"
        }, {
          "deptCode": "79",
          "deptList": [{
            "bookDeptId": 790,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 1,
            "deptCode": "79",
            "deptDescription": "PICC穿刺",
            "deptName": "PICC穿刺",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 791,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 2,
            "deptCode": "79",
            "deptDescription": "PICC维护",
            "deptName": "PICC维护",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 802,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "79",
            "deptDescription": "我院作为大型综合性三甲医院，早在1999年省内率先成立全科教研室，2000年及2007年成为首批省级、国家级全科住院医师规范化培训基地，并开放全科门诊，2008年获得全科医学博士招生资格，2013年成立集医疗、教学、培训和社区指导为一体的全科医学中心，旗下正式设立临床全科医学科，同期开放全科住院病房，2015年初起将承担滨江院区国际医疗服务从而全面改善医疗服务质量与提高医疗服务效率。近年来我科积极开展全科医学的国际合作（如英国、美国、香港等），与美国凯斯西储大学家庭医学系建立较长期培训及科研合作关系。我科多年为省内培训大量的全科医学师资骨干学员、规范化培训学员等。并与周边街道社区卫生服务中心密切合作，共建示范性全科医师社区培训基地。",
            "deptName": "全科医学科门诊",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 850,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "79",
            "deptDescription": "暂无",
            "deptName": "推拿科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 854,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "79",
            "deptDescription": "暂无",
            "deptName": "放射科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 863,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "79",
            "deptDescription": "浙医二院核医学科现有工作人员16名，博士学位医师和科研人员多名，主任医师1名，教授博导1名，形成了一支高素质、高水平的中青年临床和科研团队。有1人担任中华医学会核医学分会全国中青年委员，2人担任浙江省核医学理事、浙江省核医学会委员，1人担任浙江省核医学会副主任委员等职。科室人员还担任着《世界核医学杂志》、《英国核医学杂志》、《日本核医学英文杂志》等多个国际有影响的英文专业杂志编委工作。目前，浙江大学医学院附属第二医院核医学科和浙江大学医学PET中心是浙江省唯一的核医学博士研究生培养单位。以附属第二医院、医学院基础医学、光仪系、 化学系等学科为支撑，浙江大学医学院附属第二医院核医学科和浙江大学医学PET中心形成了一个基础医学与临床医学联合、医学与工科联合的学科团队。",
            "deptName": "核医学科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 880,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "79",
            "deptDescription": "  浙医二院理疗科是全省最早建立的理疗科之一，近几年更是快速发展，拥有大量先进而完善的物理治疗设备，有牵引区，高频区，低频区，光疗区，及运动治疗区，现有工作人员5名，年门诊量达1.3万人次，年治疗量近5万人次。我科目前开展的治疗：各类颈，腰，肩，腿痛的治疗，关节运动损伤，面神经麻痹，带状疱疹神经痛，各类运动系统和神经系统疾病及损伤所造成的功能障碍进行康复治疗，特色治疗：利用高频电容场技术治疗肛肠疾病，效果明显，能为各类疾病患者提供全面的诊疗服务。",
            "deptName": "理疗科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 888,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "79",
            "deptDescription": "本院麻醉手术部下设的麻醉科作为本省首家独立建制的单位，牵头成立了浙江省医学会麻醉学分会、疼痛学分会和浙江省麻醉质控中心。在临床医疗方面，以医疗质量为核心，科学管理为纽带，建立并完善了安全高效的临床麻醉管理制度。每年开展超过五万余例临床麻醉及急危重症患者的抢救，并通过创建多模式镇痛为特色的围术期急性疼痛管理体系和与国际接轨的无痛内镜中心。\n 该部下设的疼痛科现为浙江省疼痛医学重点创新学科牵头单位及浙江省中西医结合疼痛医学重点学科。目前已开展CT引导下胸/腰交感神经射频调制、神经导航下半月神经节射频毁损、经皮脊髓电刺激植入、鞘内药物输注系统植入等国际先进疼痛治疗方法，以及慢性顽固性疼痛的多学科协作诊治；在颈肩腰腿痛、晚期癌痛、各类神经病理性疼痛、慢性疼痛综合征等疼痛疾病诊治方面具有丰富的经验。\n",
            "deptName": "疼痛门诊(麻醉科)",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 921,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "79",
            "deptDescription": "糖尿病护理专科，是全国首批糖尿病教育培训基地，每周三下午开诊\"糖尿病护理\"门诊，为患者提供相关的健康资讯、饮食规范、胰岛素使用注意事项、日常保健等知识，拥有全国优秀教育者、教育标兵、教育先锋奖等多项奖项，为院内外患者提供多种形式的教育资讯与患教活动，收到社会大众的一致好评。",
            "deptName": "糖尿病专科护理门诊(仅限咨询)",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 926,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "79",
            "deptDescription": "浙二医院干部保健科暨老年病科系浙江省首批干部医疗保健基地、浙江省老年医学重点学科群建设单位之一，多年致力于健康保健及老年疾病的防治和衰老机制的研究，现已发展为集老年病医疗、教学、科研、康复为一体的综合学科。目前设有三个保健病区以及保健门诊和老年综合门诊，具有全科性、综合性之特点。医疗主体团队大多为来自老年病相关专业的医学博士，具备各种常见病、多发病的综合救治能力。病区施行整体化护理，服务意识强，对老龄患者的心理护理及康复训练积累了丰富的临床经验。依托医院强大的的综合实力，科室尤其在老年心脑血管病，老年神经变性病，老年代谢疾病的防治及老年肿瘤的综合性治疗和老年危重症的抢救等方面处省内领先水平，享有较高的社会知名度和优良的学术声誉。",
            "deptName": "老年病综合门诊",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 960,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "79",
            "deptDescription": "浙医二院营养科为医疗技术科室。浙江省临床营养中心、浙江省营养学会先后挂靠我科，中国营养学会临床营养分会副主任委员单位。现有营养专业人员11人，高级职称2人，中级职称4人。主要负责全院病人饮食配制,肠内、肠外营养支持会诊，营养门诊，营养健康教育以及临床营养科研、医用食品开发等。门诊重点开展肥胖的管理、消瘦人员增重方案设计等。",
            "deptName": "营养科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 970,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "79",
            "deptDescription": "超声医学科为浙江省超声医学分会主任委员单位及浙江省超声技术指导中心挂靠单位，Bracco全国超声造影培训中心。每年开展超声造影5000多例和超声介入7000多例，目前超声造影主要应用领域在腹部肿瘤及其他部位肿瘤常规鉴别诊断，肿瘤介入术前术后评估，颈动脉斑块造影评估，胃肠双重造影，甲状腺多模态诊断，前列腺穿刺造影评估和定位，乳腺及浅表淋巴结造影，心脏超声造影评估及诊断，TAVI/MitralClip/左心耳封堵术/左室减容术等术中监测，实体瘤新辅助放化疗疗效超声造影评估，输卵管造影等十多项领域；开展超声介入项目齐全，涉及肝癌的消融治疗、甲状腺消融及FNA，PTCD、实质性占位穿刺活检等等；超声医学科目前在研科研项目有国家自然科学基金4项(其中面上项目2项,青年基金1项,国际重大合作项目1项)，浙江省科技重大专项1项，省部级项目课题5项，浙大创新技术研究院科研合作项目1项目,中央国有资本经营预算支出项目1项。",
            "deptName": "超声医学科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 975,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "79",
            "deptDescription": "压疮/造口/伤口专科护理团队拥有4位国际造口治疗师，在压疮防护、伤口愈合、造口护理上拥有极其丰富的经验，每周二、五下午开诊\"造口护理\"门诊，为患者解决疑难伤口与造口并发症，得到患者与医生的高度认可。",
            "deptName": "造口护理",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 977,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "79",
            "deptDescription": "暂无",
            "deptName": "针灸科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 984,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptBookCount": 1,
            "deptCode": "79",
            "deptDescription": "浙医二院骨伤科积极促进医疗模式的转变，以病人为中心，以质量为核心，努力使服务质量和工作模式更上一层，向国际先进水平靠拢； 加强对危重复杂创伤和各类疑难杂症的治疗，使诊治水平达到全国一流水准； 大力开展对老年性骨关节病、脊柱退行性变的基础研究，以适应社会老龄化的趋势；巩固已有学术优势，增强发展后劲，成立骨科专业中心，扩大省内和国内影响力。",
            "deptName": "骨伤科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }, {
            "bookDeptId": 990,
            "bookHosId": 1,
            "bookType": "0",
            "deptAge": "0",
            "deptCode": "79",
            "deptDescription": "本院麻醉手术部下设的麻醉科作为本省首家独立建制的单位，牵头成立了浙江省医学会麻醉学分会、疼痛学分会和浙江省麻醉质控中心。在临床医疗方面，以医疗质量为核心，科学管理为纽带，建立并完善了安全高效的临床麻醉管理制度。每年开展超过五万余例临床麻醉及急危重症患者的抢救，并通过创建多模式镇痛为特色的围术期急性疼痛管理体系和与国际接轨的无痛内镜中心。",
            "deptName": "麻醉科",
            "sort": 99999,
            "superDeptId": 0,
            "topDeptCode": "9999999"
          }],
          "deptName": "其它"
        }]
      };
    },
    computed: {
      subDept() {
        return this.dept[this.currentDept].deptList
      }
    },
    components: {
      AppHeader
    },
    mounted() {
      this._init();

    },
    beforeDestroy() {

    },
    methods: {
      _init() {
        setTimeout(() => {
          if (this.$refs.left) {
            this.$refs.left.style.height = `${window.innerHeight - 45}px`;
          }

          if (this.$refs.right) {
            this.$refs.right.style.height = `${window.innerHeight - 45}px`;
          }

        }, 20)
      }
    }
  };
</script>

<style scoped lang="scss">
  @import "../../../../common/common";

  .main {
    overflow: hidden;
    > div {
      overflow-y: auto;
      background-color: white;
      ul {
        li {
          font-size: 30px;
          padding: 30px 0 30px 50px;
        }
      }
    }
    .maindept {
      background-color: #f5f5f9;
      width: 240px;
      li {
        color: #666666;
        &.cover {
          color: $mainColor;
          background-color: white;
          @include border(left, $mainColor, after, solid, 12px);

        }
      }
    }
    .subdept {
      width: 750px - 240px;
      li {
        color: #333;
      }
    }
  }
</style>
