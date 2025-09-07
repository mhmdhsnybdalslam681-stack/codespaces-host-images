<html dir="rtl" lang="ar">
 <head>
  <meta charset="utf-8"/>
  <meta content="IE=edge" http-equiv="X-UA-Compatible"/>
  <meta content="width=device-width, initial-scale=1" name="viewport"/>
  <title>
   دوائي
  </title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&amp;display=swap" rel="stylesheet"/>
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" rel="stylesheet"/>
  <style>
   body {
      font-family: 'Poppins', sans-serif;
    }
    /* Scrollbar for filters menu */
    .filters_menu {
      scrollbar-width: thin;
      scrollbar-color: #a0aec0 transparent;
    }
    .filters_menu::-webkit-scrollbar {
      height: 6px;
    }
    .filters_menu::-webkit-scrollbar-track {
      background: transparent;
    }
    .filters_menu::-webkit-scrollbar-thumb {
      background-color: #a0aec0;
      border-radius: 3px;
    }
  </style>
 </head>
 <body class="bg-gray-50 min-h-screen flex flex-col">
  <!-- Hero Area with background image -->
  <div class="relative w-full h-64 sm:h-80 md:h-96 lg:h-[28rem] overflow-hidden">
   <img alt="صورة خلفية بطل تظهر داخل مطعم حديث مع إضاءة دافئة وديكور أنيق" class="w-full h-full object-cover" height="350" src="https://i.postimg.cc/gj8DrR24/pngtree-palestine-flag-design-on-smooth-fabric-background-picture-image-15914567.png" width="20"/>
   <header class="absolute top-0 left-0 w-full bg-black bg-opacity-50">
    <nav class="container mx-auto flex items-center justify-between py-4 px-4 sm:px-6 lg:px-8">
     <a id="home-link" class="text-white text-3xl font-semibold tracking-wide cursor-pointer">
      دوائي
     </a>
     <button aria-label="تبديل القائمة" class="text-white text-2xl md:hidden focus:outline-none" id="nav-toggle">
      <i class="fas fa-bars"></i>
     </button>
     <ul class="hidden md:flex space-x-8 text-white font-medium text-lg" id="nav-menu">
      <li>
       <a id="home-link-menu" class="hover:text-yellow-400 transition cursor-pointer">
        الرئيسية
       </a>
      </li>
      <li>
       <a id="menu-link" class="text-yellow-400 border-b-2 border-yellow-400 pb-1 cursor-pointer">
        القائمة
       </a>
      </li>
      <li>
       <a id="about-link" class="hover:text-yellow-400 transition cursor-pointer">
        من نحن
       </a>
      </li>
     </ul>
     <div class="hidden md:flex items-center space-x-6">
      <a aria-label="حساب المستخدم" class="text-white hover:text-yellow-400 transition text-xl" href="#">
       <i class="fas fa-user"></i>
      </a>
      <form aria-label="بحث في الموقع" class="relative" id="search-form" role="search">
       <input aria-label="حقل البحث" autocomplete="off" class="rounded-full pl-4 pr-10 py-1 text-black focus:outline-yellow-400 placeholder-gray-500" id="search-input" placeholder="ابحث في القائمة..." type="search"/>
       <button aria-label="إرسال البحث" class="absolute right-2 top-1.5 text-yellow-400 hover:text-yellow-600 focus:outline-none" type="submit">
        <i class="fas fa-search"></i>
       </button>
      </form>
      <a class="bg-yellow-400 hover:bg-yellow-500 text-black font-semibold px-4 py-2 rounded-full transition" href="#">
       اطلب الآن
      </a>
     </div>
    </nav>
   </header>
  </div>
  <!-- الكل -->
  <div class="md:hidden bg-black bg-opacity-90 text-white hidden" id="mobile-menu">
   <ul class="flex flex-col space-y-4 p-6 text-lg font-semibold">
    <li>
     <a id="home-link-mobile" class="block hover:text-yellow-400 cursor-pointer">
      الرئيسية
     </a>
    </li>
    <li>
     <a id="menu-link-mobile" class="block text-yellow-400 cursor-pointer">
      القائمة
     </a>
    </li>
    <li>
     <a id="about-link-mobile" class="block hover:text-yellow-400 cursor-pointer">
      من نحن
     </a>
    </li>
    <li>
     <a class="block bg-yellow-400 text-black text-center rounded-full py-2 font-semibold hover:bg-yellow-500" href="#">
      اطلب الآن
     </a>
    </li>
   </ul>
  </div>
  <main class="flex-grow container mx-auto px-4 sm:px-6 lg:px-8 py-12">
   <h2 class="text-4xl font-semibold text-center mb-6 text-gray-800">
    قائمة الادويه
   </h2>
   <div class="max-w-md mx-auto mb-10">
    <input aria-label="شريط البحث في القائمة" autocomplete="off" class="w-full rounded-full border border-gray-300 px-5 py-3 text-gray-700 placeholder-gray-400 focus:border-yellow-400 focus:ring-2 focus:ring-yellow-400 focus:outline-none transition" id="page-search" placeholder="ابحث عن أي شيء في الصفحة..." type="search"/>
   </div>
   <nav aria-label="قائمة الفلاتر" class="mb-8 overflow-x-auto">
    <ul class="filters_menu flex space-x-6 text-gray-700 font-semibold whitespace-nowrap" id="filters-menu">
     <li class="cursor-pointer px-4 py-2 rounded-full bg-yellow-400 text-black" data-filter="*">
      الكل
     </li>
     <li class="cursor-pointer px-4 py-2 rounded-full hover:bg-yellow-400 hover:text-black transition" data-filter=".burger">
      مستلزمات طبيه
     </li>
     <li class="cursor-pointer px-4 py-2 rounded-full hover:bg-yellow-400 hover:text-black transition" data-filter=".pizza">
      ادويه
     </li>
     <li class="cursor-pointer px-4 py-2 rounded-full hover:bg-yellow-400 hover:text-black transition" data-filter=".pasta">
      مستحضرات تجميل
     </li>
     <li class="cursor-pointer px-4 py-2 rounded-full hover:bg-yellow-400 hover:text-black transition" data-filter=".fries">
      حفضات
     </li>
    </ul>
   </nav>
   <section aria-label="عناصر القائمة" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8" id="menu-items">
    <article class="all pizza bg-white rounded-lg shadow-md overflow-hidden flex flex-col">
     <img alt="دواء مضاد لكورونا في عبوة زجاجية شفافة مع ملصق طبي على خلفية بيضاء" class="w-full h-48 object-cover" height="400" src="https://i.postimg.cc/yYnbNLyR/20250905-210855.png" width="600"/>
     <div class="p-6 flex flex-col flex-grow">
      <h3 class="text-xl font-semibold mb-2 text-gray-900">
       بانادول اكسترا
      </h3>
      <p class="text-gray-600 flex-grow">
       مسكن للألم وخافض للحرارة، فعال في تخفيف أنواع مختلفة من الألم مثل الصداع وآلام الجسم والعضلات وآلام الأسنان وآلام الدورة الشهرية. 
      </p>
      <div class="mt-4 flex items-center justify-between">
       <span class="text-yellow-500 font-bold text-lg">
        $108
       </span>
       <button aria-label="إضافة دواء مضاد لكورونا إلى عربة التسوق" class="add-to-cart bg-yellow-400 hover:bg-yellow-500 text-black font-semibold px-4 py-2 rounded-full transition flex items-center space-x-2 rtl:space-x-reverse">
        <i class="fas fa-shopping-cart"></i>
        <span>إضافة إلى عربة التسوق</span>
       </button>
      </div>
     </div>
    </article>
    <article class="all pizza bg-white rounded-lg shadow-md overflow-hidden flex flex-col">
     <img alt="عبوة دواء معبأة بشكل أنيق مع ملصق طبي على خلفية بيضاء" class="w-full h-48 object-cover" height="400" src="https://i.postimg.cc/3RjrPM5V/congestal-tab-11668935221.webp" width="600"/>
     <div class="p-6 flex flex-col flex-grow">
      <h3 class="text-xl font-semibold mb-2 text-gray-900">
       کونچیستال
      </h3>
      <p class="text-gray-600 flex-grow">
       
يستخدم دواء كونجستال للحد من أعراض البرد والأنفلونزا مثل سيلان الأنف وتدميع العيون.
      </p>
      <div class="mt-4 flex items-center justify-between">
       <span class="text-yellow-500 font-bold text-lg">
        $50
       </span>
       <button aria-label="إضافة دواء مارجريتا إلى عربة التسوق" class="add-to-cart bg-yellow-400 hover:bg-yellow-500 text-black font-semibold px-4 py-2 rounded-full transition flex items-center space-x-2 rtl:space-x-reverse">
        <i class="fas fa-shopping-cart"></i>
        <span>إضافة إلى عربة التسوق</span>
       </button>
      </div>
     </div>
    </article>
    <article class="all pizza bg-white rounded-lg shadow-md overflow-hidden flex flex-col">
     <img alt="عبوة دواء بيبروني مع ملصق طبي على خلفية بيضاء" class="w-full h-48 object-cover" height="400" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRJHO-8adPDZi268dIxHk84xCVRH8-Q36MNdA&usqp=CAU" width="600"/>
     <div class="p-6 flex flex-col flex-grow">
      <h3 class="text-xl font-semibold mb-2 text-gray-900">
       بروفين 600g
      </h3>
      <p class="text-gray-600 flex-grow">
       مسكن للآلام.
خافض للحرارة.
مضاد للالتهابات.
      </p>
      <div class="mt-4 flex items-center justify-between">
       <span class="text-yellow-500 font-bold text-lg">
        $99
       </span>
       <button aria-label="إضافة دواء بيبروني إلى عربة التسوق" class="add-to-cart bg-yellow-400 hover:bg-yellow-500 text-black font-semibold px-4 py-2 rounded-full transition flex items-center space-x-2 rtl:space-x-reverse">
        <i class="fas fa-shopping-cart"></i>
        <span>إضافة إلى عربة التسوق</span>
       </button>
      </div>
     </div>
    </article>
    <article class="all pizza bg-white rounded-lg shadow-md overflow-hidden flex flex-col">
     <img alt="عبوة دواء بيبروني مع ملصق طبي على خلفية بيضاء" class="w-full h-48 object-cover" height="400" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQcXKpKFhqbtw2b-6ifsJPK53oY-55dRbbxXg&usqp=CAU" width="600"/>
     <div class="p-6 flex flex-col flex-grow">
      <h3 class="text-xl font-semibold mb-2 text-gray-900">
       سبيريكس
      </h3>
      <p class="text-gray-600 flex-grow">
       لعلاج امراض الجهاز التنفسي.
      </p>
      <div class="mt-4 flex items-center justify-between">
       <span class="text-yellow-500 font-bold text-lg">
        $108
       </span>
       <button aria-label="إضافة دواء بيبروني إلى عربة التسوق" class="add-to-cart bg-yellow-400 hover:bg-yellow-500 text-black font-semibold px-4 py-2 rounded-full transition flex items-center space-x-2 rtl:space-x-reverse">
        <i class="fas fa-shopping-cart"></i>
        <span>إضافة إلى عربة التسوق</span>
       </button>
      </div>
     </div>
    </article>
    <article class="all burger bg-white rounded-lg shadow-md overflow-hidden flex flex-col">
     <img alt="مستلزمات طبية مثل سماعة طبية، قفازات، وكمامات على خلفية بيضاء" class="w-full h-48 object-cover" height="400" src="https://i.postimg.cc/sg5LP3pk/20250905-213310.png" width="600"/>
     <div class="p-6 flex flex-col flex-grow">
      <h3 class="text-xl font-semibold mb-2 text-gray-900">
       قن طبي
      </h3>
      <p class="text-gray-600 flex-grow">
        قطن طبي ماص للسوئل
      </p>
      <div class="mt-4 flex items-center justify-between">
       <span class="text-yellow-500 font-bold text-lg">
        $10
       </span>
       <button aria-label="إضافة مستلزمات طبية أساسية إلى عربة التسوق" class="add-to-cart bg-yellow-400 hover:bg-yellow-500 text-black font-semibold px-4 py-2 rounded-full transition flex items-center space-x-2 rtl:space-x-reverse">
        <i class="fas fa-shopping-cart"></i>
        <span>إضافة إلى عربة التسوق</span>
       </button>
      </div>
     </div>
    </article>
    <article class="all burger bg-white rounded-lg shadow-md overflow-hidden flex flex-col">
     <img alt="معدات طبية مثل محاقن وأدوات تعقيم على خلفية بيضاء" class="w-full h-48 object-cover" height="400" src="https://storage.googleapis.com/a1aa/image/de70f0bf-3975-49fc-23e5-7b99688f827a.jpg" width="600"/>
     <div class="p-6 flex flex-col flex-grow">
      <h3 class="text-xl font-semibold mb-2 text-gray-900">
       معدات طبية متقدمة
      </h3>
      <p class="text-gray-600 flex-grow">
       معدات طبية متقدمة للاستخدام في المستشفيات والعيادات.
      </p>
      <div class="mt-4 flex items-center justify-between">
       <span class="text-yellow-500 font-bold text-lg">
        $14
       </span>
       <button aria-label="إضافة معدات طبية متقدمة إلى عربة التسوق" class="add-to-cart bg-yellow-400 hover:bg-yellow-500 text-black font-semibold px-4 py-2 rounded-full transition flex items-center space-x-2 rtl:space-x-reverse">
        <i class="fas fa-shopping-cart"></i>
        <span>إضافة إلى عربة التسوق</span>
       </button>
      </div>
     </div>
    </article>
    <article class="all burger bg-white rounded-lg shadow-md overflow-hidden flex flex-col">
     <img alt="أدوات طبية مثل القفازات والكمامات على خلفية بيضاء" class="w-full h-48 object-cover" height="400" src="https://storage.googleapis.com/a1aa/image/c8829b5d-7c88-4e38-8054-363a026623f1.jpg" width="600"/>
     <div class="p-6 flex flex-col flex-grow">
      <h3 class="text-xl font-semibold mb-2 text-gray-900">
       أدوات طبية للاستخدام اليومي
      </h3>
      <p class="text-gray-600 flex-grow">
       أدوات طبية للاستخدام اليومي للحماية والسلامة.
      </p>
      <div class="mt-4 flex items-center justify-between">
       <span class="text-yellow-500 font-bold text-lg">
        $13
       </span>
       <button aria-label="إضافة أدوات طبية للاستخدام اليومي إلى عربة التسوق" class="add-to-cart bg-yellow-400 hover:bg-yellow-500 text-black font-semibold px-4 py-2 rounded-full transition flex items-center space-x-2 rtl:space-x-reverse">
        <i class="fas fa-shopping-cart"></i>
        <span>إضافة إلى عربة التسوق</span>
       </button>
      </div>
     </div>
    </article>
    <article class="all pasta bg-white rounded-lg shadow-md overflow-hidden flex flex-col">
     <img alt="منتجات تجميل مثل كريمات وزجاجات عطر على خلفية بيضاء" class="w-full h-48 object-cover" height="400" src="https://storage.googleapis.com/a1aa/image/000d4b7d-8b1c-4a6e-e356-b52bebdbd17b.jpg" width="600"/>
     <div class="p-6 flex flex-col flex-grow">
      <h3 class="text-xl font-semibold mb-2 text-gray-900">
       مستحضرات تجميل طبيعية
      </h3>
      <p class="text-gray-600 flex-grow">
       مستحضرات تجميل طبيعية للعناية بالبشرة والشعر.
      </p>
      <div class="mt-4 flex items-center justify-between">
       <span class="text-yellow-500 font-bold text-lg">
        $16
       </span>
       <button aria-label="إضافة مستحضرات تجميل طبيعية إلى عربة التسوق" class="add-to-cart bg-yellow-400 hover:bg-yellow-500 text-black font-semibold px-4 py-2 rounded-full transition flex items-center space-x-2 rtl:space-x-reverse">
        <i class="fas fa-shopping-cart"></i>
        <span>إضافة إلى عربة التسوق</span>
       </button>
      </div>
     </div>
    </article>
    <article class="all pasta bg-white rounded-lg shadow-md overflow-hidden flex flex-col">
     <img alt="زجاجة كريم تجميل مع وردة على خلفية بيضاء" class="w-full h-48 object-cover" height="400" src="https://storage.googleapis.com/a1aa/image/b8587606-58a9-4526-12cc-848d9a734990.jpg" width="600"/>
     <div class="p-6 flex flex-col flex-grow">
      <h3 class="text-xl font-semibold mb-2 text-gray-900">
       كريم تجميل طبيعي
      </h3>
      <p class="text-gray-600 flex-grow">
       كريم تجميل طبيعي لترطيب البشرة وحمايتها.
      </p>
      <div class="mt-4 flex items-center justify-between">
       <span class="text-yellow-500 font-bold text-lg">
        $18
       </span>
       <button aria-label="إضافة كريم تجميل طبيعي إلى عربة التسوق" class="add-to-cart bg-yellow-400 hover:bg-yellow-500 text-black font-semibold px-4 py-2 rounded-full transition flex items-center space-x-2 rtl:space-x-reverse">
        <i class="fas fa-shopping-cart"></i>
        <span>إضافة إلى عربة التسوق</span>
       </button>
      </div>
     </div>
    </article>
    <article class="all pasta bg-white rounded-lg shadow-md overflow-hidden flex flex-col">
     <img alt="مجموعة مستحضرات تجميل طبيعية على خلفية بيضاء" class="w-full h-48 object-cover" height="400" src="https://storage.googleapis.com/a1aa/image/c72b1870-2538-4874-ea58-f331cac74b50.jpg" width="600"/>
     <div class="p-6 flex flex-col flex-grow">
      <h3 class="text-xl font-semibold mb-2 text-gray-900">
       مجموعة مستحضرات تجميل
      </h3>
      <p class="text-gray-600 flex-grow">
       مجموعة مستحضرات تجميل طبيعية للعناية اليومية.
      </p>
      <div class="mt-4 flex items-center justify-between">
       <span class="text-yellow-500 font-bold text-lg">
        $17
       </span>
       <button aria-label="إضافة مجموعة مستحضرات تجميل إلى عربة التسوق" class="add-to-cart bg-yellow-400 hover:bg-yellow-500 text-black font-semibold px-4 py-2 rounded-full transition flex items-center space-x-2 rtl:space-x-reverse">
        <i class="fas fa-shopping-cart"></i>
        <span>إضافة إلى عربة التسوق</span>
       </button>
      </div>
     </div>
    </article>
    <article class="all fries bg-white rounded-lg shadow-md overflow-hidden flex flex-col">
     <img alt="حفاظات أطفال مع تصميم لطيف على خلفية بيضاء" class="w-full h-48 object-cover" height="400" src="https://storage.googleapis.com/a1aa/image/7b9520a2-c09c-467c-1ba2-4a2c013df4d9.jpg" width="600"/>
     <div class="p-6 flex flex-col flex-grow">
      <h3 class="text-xl font-semibold mb-2 text-gray-900">
       حفاظات أطفال ناعمة
      </h3>
      <p class="text-gray-600 flex-grow">
       حفاظات أطفال ناعمة ومريحة مع امتصاص عالي.
      </p>
      <div class="mt-4 flex items-center justify-between">
       <span class="text-yellow-500 font-bold text-lg">
        $7
       </span>
       <button aria-label="إضافة حفاظات أطفال ناعمة إلى عربة التسوق" class="add-to-cart bg-yellow-400 hover:bg-yellow-500 text-black font-semibold px-4 py-2 rounded-full transition flex items-center space-x-2 rtl:space-x-reverse">
        <i class="fas fa-shopping-cart"></i>
        <span>إضافة إلى عربة التسوق</span>
       </button>
      </div>
     </div>
    </article>
    <article class="all fries bg-white rounded-lg shadow-md overflow-hidden flex flex-col">
     <img alt="حفاظات أطفال مع رسومات كرتونية ملونة على خلفية بيضاء" class="w-full h-48 object-cover" height="400" src="https://storage.googleapis.com/a1aa/image/99f5ba72-bdda-49af-6513-b0b40cb4a495.jpg" width="600"/>
     <div class="p-6 flex flex-col flex-grow">
      <h3 class="text-xl font-semibold mb-2 text-gray-900">
       حفاظات أطفال ملونة
      </h3>
      <p class="text-gray-600 flex-grow">
       حفاظات أطفال مع رسومات كرتونية ملونة وجذابة.
      </p>
      <div class="mt-4 flex items-center justify-between">
       <span class="text-yellow-500 font-bold text-lg">
        $10
       </span>
       <button aria-label="إضافة حفاظات أطفال ملونة إلى عربة التسوق" class="add-to-cart bg-yellow-400 hover:bg-yellow-500 text-black font-semibold px-4 py-2 rounded-full transition flex items-center space-x-2 rtl:space-x-reverse">
        <i class="fas fa-shopping-cart"></i>
        <span>إضافة إلى عربة التسوق</span>
       </button>
      </div>
     </div>
    </article>
    <article class="all fries bg-white rounded-lg shadow-md overflow-hidden flex flex-col">
     <img alt="حفاظات أطفال مع تصميم بسيط على خلفية بيضاء" class="w-full h-48 object-cover" height="400" src="https://storage.googleapis.com/a1aa/image/461b1e61-0497-423f-1216-85782d280472.jpg" width="600"/>
     <div class="p-6 flex flex-col flex-grow">
      <h3 class="text-xl font-semibold mb-2 text-gray-900">
       حفاظات أطفال بسيطة
      </h3>
      <p class="text-gray-600 flex-grow">
       حفاظات أطفال بتصميم بسيط وفعالية عالية.
      </p>
      <div class="mt-4 flex items-center justify-between">
       <span class="text-yellow-500 font-bold text-lg">
        $8
       </span>
       <button aria-label="إضافة حفاظات أطفال بسيطة إلى عربة التسوق" class="add-to-cart bg-yellow-400 hover:bg-yellow-500 text-black font-semibold px-4 py-2 rounded-full transition flex items-center space-x-2 rtl:space-x-reverse">
        <i class="fas fa-shopping-cart"></i>
        <span>إضافة إلى عربة التسوق</span>
       </button>
      </div>
     </div>
    </article>
   </section>
   <div class="text-center mt-12">
    <a class="inline-block bg-yellow-400 hover:bg-yellow-500 text-black font-semibold px-8 py-3 rounded-full transition" href="#">
     عرض المزيد
    </a>
   </div>
  </main>

  <!-- عربة التسوق الذكية -->
  <div id="cart-sidebar" class="fixed top-0 left-0 h-full w-80 bg-white shadow-lg transform -translate-x-full transition-transform duration-300 z-50 flex flex-col">
   <div class="flex items-center justify-between p-4 border-b border-gray-200">
    <h3 class="text-xl font-semibold text-gray-900">عربة التسوق</h3>
    <button id="close-cart" aria-label="إغلاق عربة التسوق" class="text-gray-600 hover:text-gray-900 focus:outline-none text-2xl">&times;</button>
   </div>
   <div id="cart-items" class="flex-grow overflow-y-auto p-4 space-y-4">
    <p class="text-gray-500 text-center">لم يتم إضافة أي منتجات بعد.</p>
   </div>
   <div class="p-4 border-t border-gray-200">
    <div class="flex justify-between items-center mb-4">
     <span class="font-semibold text-lg text-gray-900">الإجمالي:</span>
     <span id="cart-total" class="font-bold text-yellow-500 text-lg">$0</span>
    </div>
    <button id="checkout-btn" class="w-full bg-yellow-400 hover:bg-yellow-500 text-black font-semibold py-3 rounded-full transition">
     إتمام الشراء
    </button>
   </div>
  </div>

  <!-- Overlay -->
  <div id="cart-overlay" class="fixed inset-0 bg-black bg-opacity-50 hidden z-40"></div>

  <!-- Modal -->
  <div id="order-modal" class="fixed inset-0 bg-black bg-opacity-50 hidden z-50 flex items-center justify-center px-4">
   <div class="bg-white rounded-lg max-w-md w-full p-6 relative">
    <button id="close-modal" aria-label="إغلاق النافذة" class="absolute top-3 left-3 text-gray-600 hover:text-gray-900 text-2xl focus:outline-none">&times;</button>
    <h3 class="text-xl font-semibold mb-4 text-gray-900 text-center">تفاصيل الطلب</h3>
    <div id="order-summary" class="max-h-64 overflow-y-auto mb-4 text-gray-700"></div>
    <form id="order-form" class="space-y-4">
     <div>
      <label for="customer-name" class="block mb-1 font-semibold text-gray-800">الاسم الكامل</label>
      <input type="text" id="customer-name" name="customerName" required class="w-full border border-gray-300 rounded-md px-4 py-2 focus:outline-yellow-400 focus:ring-2 focus:ring-yellow-400"/>
     </div>
     <div>
      <label for="customer-phone" class="block mb-1 font-semibold text-gray-800">رقم الهاتف</label>
      <input type="tel" id="customer-phone" name="customerPhone" required pattern="^\+?\d{7,15}$" placeholder="+20xxxxxxxxxx" class="w-full border border-gray-300 rounded-md px-4 py-2 focus:outline-yellow-400 focus:ring-2 focus:ring-yellow-400"/>
     </div>
     <div>
      <label for="customer-address" class="block mb-1 font-semibold text-gray-800">العنوان (اختياري)</label>
      <textarea id="customer-address" name="customerAddress" rows="3" class="w-full border border-gray-300 rounded-md px-4 py-2 focus:outline-yellow-400 focus:ring-2 focus:ring-yellow-400"></textarea>
     </div>
     <button type="submit" class="w-full bg-yellow-400 hover:bg-yellow-500 text-black font-semibold py-3 rounded-full transition flex items-center justify-center space-x-2 rtl:space-x-reverse">
      <i class="fas fa-paper-plane"></i>
      <span>إرسال الطلب</span>
     </button>
    </form>
   </div>
  </div>

  <!-- About Modal -->
  <div id="about-modal" class="fixed inset-0 bg-black bg-opacity-50 hidden z-50 flex items-center justify-center px-4">
   <div class="bg-white rounded-lg max-w-lg w-full p-6 relative">
    <button id="close-about-modal" aria-label="إغلاق النافذة" class="absolute top-3 left-3 text-gray-600 hover:text-gray-900 text-2xl focus:outline-none">&times;</button>
    <h3 class="text-2xl font-semibold mb-4 text-gray-900 text-center">من نحن</h3>
    <p class="text-gray-700 leading-relaxed text-center">
      مرحبًا بكم في دوائي، وجهتكم الموثوقة للحصول على أفضل الأدوية والمستلزمات الطبية ومستحضرات التجميل. نحن نؤمن بأهمية الصحة والعناية الشخصية، ونسعى لتوفير منتجات عالية الجودة بأسعار مناسبة مع خدمة عملاء متميزة. هدفنا هو تسهيل وصولكم إلى ما تحتاجونه من منتجات طبية وصحية بكل سهولة وأمان.
    </p>
   </div>
  </div>

  <footer class="bg-gray-900 text-gray-300 py-12 mt-auto">
   <div class="container mx-auto px-4 sm:px-6 lg:px-8 grid grid-cols-1 md:grid-cols-1 gap-10 text-center">
    <p>
     <span id="displayYear"></span>
     <span class="font-semibold text-yellow-400">
      دوائي © جميع الحقوق محفوظة
     </span>
    </p>
   </div>
  </footer>
  <script>
   // Mobile menu toggle
    const navToggle = document.getElementById('nav-toggle');
    const mobileMenu = document.getElementById('mobile-menu');

    navToggle.addEventListener('click', () => {
      mobileMenu.classList.toggle('hidden');
    });

    // Filter menu functionality
    const filtersMenu = document.getElementById('filters-menu');
    const menuItems = document.getElementById('menu-items');
    const filterButtons = filtersMenu.querySelectorAll('li');

    filterButtons.forEach(button => {
      button.addEventListener('click', () => {
        // Remove active styles from all buttons
        filterButtons.forEach(btn => {
          btn.classList.remove('bg-yellow-400', 'text-black');
          btn.classList.add('hover:bg-yellow-400', 'hover:text-black');
        });
        // Add active styles to clicked button
        button.classList.add('bg-yellow-400', 'text-black');
        button.classList.remove('hover:bg-yellow-400', 'hover:text-black');

        const filter = button.getAttribute('data-filter');

        const items = menuItems.querySelectorAll('article');

        items.forEach(item => {
          if (filter === '*' || item.classList.contains(filter.slice(1))) {
            item.classList.remove('hidden');
          } else {
            item.classList.add('hidden');
          }
        });
      });
    });

    // Set current year in footer
    document.getElementById('displayYear').textContent = new Date().getFullYear();

    // Page-wide search filter
    const pageSearchInput = document.getElementById('page-search');
    pageSearchInput.addEventListener('input', () => {
      const query = pageSearchInput.value.trim().toLowerCase();
      const items = menuItems.querySelectorAll('article');

      items.forEach(item => {
        // Search in title and description text
        const title = item.querySelector('h3').textContent.toLowerCase();
        const desc = item.querySelector('p').textContent.toLowerCase();
        if (title.includes(query) || desc.includes(query)) {
          item.classList.remove('hidden');
        } else {
          item.classList.add('hidden');
        }
      });

      // If a filter is active other than "All", keep that filter applied as well
      const activeFilterBtn = Array.from(filterButtons).find(btn => btn.classList.contains('bg-yellow-400') && btn.getAttribute('data-filter') !== '*');
      if (activeFilterBtn) {
        const filter = activeFilterBtn.getAttribute('data-filter');
        items.forEach(item => {
          if (!item.classList.contains(filter.slice(1))) {
            item.classList.add('hidden');
          }
        });
      }
    });

    // Prevent form submission on search form in header
    const searchForm = document.getElementById('search-form');
    searchForm.addEventListener('submit', e => {
      e.preventDefault();
      // Optionally, you can trigger the page-wide search input event here
      pageSearchInput.focus();
    });

    // Cart functionality
    const addToCartButtons = document.querySelectorAll('.add-to-cart');
    const cartSidebar = document.getElementById('cart-sidebar');
    const cartOverlay = document.getElementById('cart-overlay');
    const closeCartBtn = document.getElementById('close-cart');
    const cartItemsContainer = document.getElementById('cart-items');
    const cartTotalEl = document.getElementById('cart-total');
    const checkoutBtn = document.getElementById('checkout-btn');

    // Modal elements
    const orderModal = document.getElementById('order-modal');
    const closeModalBtn = document.getElementById('close-modal');
    const orderSummary = document.getElementById('order-summary');
    const orderForm = document.getElementById('order-form');

    // About modal elements
    const aboutModal = document.getElementById('about-modal');
    const closeAboutModalBtn = document.getElementById('close-about-modal');
    const aboutLink = document.getElementById('about-link');
    const aboutLinkMobile = document.getElementById('about-link-mobile');

    // Menu link elements
    const menuLink = document.getElementById('menu-link');
    const menuLinkMobile = document.getElementById('menu-link-mobile');

    // Home link elements
    const homeLink = document.getElementById('home-link');
    const homeLinkMenu = document.getElementById('home-link-menu');
    const homeLinkMobile = document.getElementById('home-link-mobile');

    // Cart data structure
    let cart = [];

    // Format price helper
    function formatPrice(price) {
      return `$${price.toFixed(2)}`;
    }

    // Render cart items
    function renderCart() {
      cartItemsContainer.innerHTML = '';
      if (cart.length === 0) {
        cartItemsContainer.innerHTML = '<p class="text-gray-500 text-center">لم يتم إضافة أي منتجات بعد.</p>';
        cartTotalEl.textContent = '$0';
        checkoutBtn.disabled = true;
        checkoutBtn.classList.add('opacity-50', 'cursor-not-allowed');
        return;
      }
      checkoutBtn.disabled = false;
      checkoutBtn.classList.remove('opacity-50', 'cursor-not-allowed');

      let total = 0;
      cart.forEach(item => {
        total += item.price * item.quantity;
        const itemEl = document.createElement('div');
        itemEl.className = 'flex items-center space-x-4 rtl:space-x-reverse border-b border-gray-200 pb-3';

        itemEl.innerHTML = `
          <img src="${item.image}" alt="${item.title} صورة المنتج في عربة التسوق" class="w-16 h-16 object-cover rounded-md flex-shrink-0"/>
          <div class="flex-grow">
            <h4 class="font-semibold text-gray-900">${item.title}</h4>
            <p class="text-yellow-500 font-bold">${formatPrice(item.price)}</p>
            <div class="flex items-center mt-1 space-x-2 rtl:space-x-reverse">
              <button aria-label="إنقاص كمية ${item.title}" class="decrease-qty text-gray-600 hover:text-gray-900 focus:outline-none text-lg px-2 rounded border border-gray-300">−</button>
              <span class="text-gray-700 font-semibold">${item.quantity}</span>
              <button aria-label="زيادة كمية ${item.title}" class="increase-qty text-gray-600 hover:text-gray-900 focus:outline-none text-lg px-2 rounded border border-gray-300">+</button>
            </div>
          </div>
          <button aria-label="حذف ${item.title} من عربة التسوق" class="remove-item text-red-500 hover:text-red-700 focus:outline-none text-xl">&times;</button>
        `;

        // Increase quantity
        itemEl.querySelector('.increase-qty').addEventListener('click', () => {
          item.quantity++;
          renderCart();
        });

        // Decrease quantity
        itemEl.querySelector('.decrease-qty').addEventListener('click', () => {
          if (item.quantity > 1) {
            item.quantity--;
          } else {
            // Remove item if quantity reaches 0
            cart = cart.filter(ci => ci.id !== item.id);
          }
          renderCart();
        });

        // Remove item
        itemEl.querySelector('.remove-item').addEventListener('click', () => {
          cart = cart.filter(ci => ci.id !== item.id);
          renderCart();
        });

        cartItemsContainer.appendChild(itemEl);
      });
      cartTotalEl.textContent = formatPrice(total);
    }

    // Open cart sidebar
    function openCart() {
      cartSidebar.classList.remove('-translate-x-full');
      cartOverlay.classList.remove('hidden');
      document.body.style.overflow = 'hidden';
    }

    // Close cart sidebar
    function closeCart() {
      cartSidebar.classList.add('-translate-x-full');
      cartOverlay.classList.add('hidden');
      document.body.style.overflow = '';
    }

    // Add to cart button click handler
    addToCartButtons.forEach(button => {
      button.addEventListener('click', (e) => {
        const article = e.target.closest('article');
        if (!article) return;

        const id = article.querySelector('h3').textContent.trim();
        const title = article.querySelector('h3').textContent.trim();
        const priceText = article.querySelector('span.text-yellow-500').textContent.trim();
        const price = parseFloat(priceText.replace('$', '')) || 0;
        const image = article.querySelector('img').src;

        // Check if item already in cart
        const existingItem = cart.find(item => item.id === id);
        if (existingItem) {
          existingItem.quantity++;
        } else {
          cart.push({ id, title, price, quantity: 1, image });
        }

        renderCart();
        openCart();
      });
    });

    // Close cart button and overlay
    closeCartBtn.addEventListener('click', closeCart);
    cartOverlay.addEventListener('click', closeCart);

    // Show order modal with summary
    function showOrderModal() {
      if (cart.length === 0) return;
      // Build order summary HTML
      let summaryHTML = '<ul class="divide-y divide-gray-300">';
      cart.forEach(item => {
        summaryHTML += `
          <li class="py-2 flex items-center space-x-4 rtl:space-x-reverse">
            <img src="${item.image}" alt="${item.title} صورة المنتج في ملخص الطلب" class="w-12 h-12 object-cover rounded-md flex-shrink-0"/>
            <div class="flex-grow">
              <p class="font-semibold text-gray-900">${item.title}</p>
              <p>الكمية: ${item.quantity} × ${formatPrice(item.price)}</p>
              <p class="font-bold text-yellow-500">الإجمالي: ${formatPrice(item.price * item.quantity)}</p>
            </div>
          </li>
        `;
      });
      summaryHTML += '</ul>';
      const total = cart.reduce((sum, item) => sum + item.price * item.quantity, 0);
      summaryHTML += `<p class="mt-4 font-semibold text-lg text-gray-900 text-center">الإجمالي الكلي: ${formatPrice(total)}</p>`;

      orderSummary.innerHTML = summaryHTML;
      orderModal.classList.remove('hidden');
      document.body.style.overflow = 'hidden';
    }

    // Close order modal
    function closeOrderModal() {
      orderModal.classList.add('hidden');
      document.body.style.overflow = '';
      orderForm.reset();
    }

    // Checkout button click - open order modal instead of WhatsApp
    checkoutBtn.addEventListener('click', () => {
      showOrderModal();
    });

    // Close modal button
    closeModalBtn.addEventListener('click', closeOrderModal);

    // Close modal on overlay click (optional)
    orderModal.addEventListener('click', (e) => {
      if (e.target === orderModal) {
        closeOrderModal();
      }
    });

    // Handle order form submission
    orderForm.addEventListener('submit', (e) => {
      e.preventDefault();
      if (cart.length === 0) return;

      const name = orderForm.customerName.value.trim();
      const phone = orderForm.customerPhone.value.trim();
      const address = orderForm.customerAddress.value.trim();

      if (!name || !phone) {
        alert('يرجى ملء الاسم ورقم الهاتف.');
        return;
      }

      // Prepare order message
      let message = `طلب جديد من دوائي:%0Aالاسم: ${encodeURIComponent(name)}%0Aرقم الهاتف: ${encodeURIComponent(phone)}`;
      if(address) {
        message += `%0Aالعنوان: ${encodeURIComponent(address)}`;
      }
      message += `%0A%0Aتفاصيل الطلب:%0A`;
      cart.forEach(item => {
        message += `- ${encodeURIComponent(item.title)} (الكمية: ${item.quantity}) - السعر: $${(item.price * item.quantity).toFixed(2)}%0A`;
        message += `صورة المنتج: ${encodeURIComponent(item.image)}%0A`;
      });
      const total = cart.reduce((sum, item) => sum + item.price * item.quantity, 0);
      message += `%0Aالإجمالي: $${total.toFixed(2)}`;

      // WhatsApp Business number (with country code, Egypt +20)
      const phoneNumber = '201019964505';

      // WhatsApp URL
      const whatsappURL = `https://wa.me/${phoneNumber}?text=${message}`;

      // Open WhatsApp in new tab
      window.open(whatsappURL, '_blank');

      // Clear cart and close modal and sidebar
      cart = [];
      renderCart();
      closeOrderModal();
      closeCart();
    });

    // About modal open/close handlers
    function openAboutModal() {
      aboutModal.classList.remove('hidden');
      document.body.style.overflow = 'hidden';
      if(!mobileMenu.classList.contains('hidden')) {
        mobileMenu.classList.add('hidden');
      }
    }
    function closeAboutModal() {
      aboutModal.classList.add('hidden');
      document.body.style.overflow = '';
    }

    aboutLink.addEventListener('click', openAboutModal);
    aboutLinkMobile.addEventListener('click', openAboutModal);
    closeAboutModalBtn.addEventListener('click', closeAboutModal);
    aboutModal.addEventListener('click', (e) => {
      if (e.target === aboutModal) {
        closeAboutModal();
      }
    });

    // Menu link click handlers to scroll to menu section
    function scrollToMenu() {
      if(!mobileMenu.classList.contains('hidden')) {
        mobileMenu.classList.add('hidden');
      }
      // Scroll smoothly to menu section
      const menuSection = document.getElementById('menu-items');
      if(menuSection) {
        menuSection.scrollIntoView({ behavior: 'smooth' });
      }
    }
    menuLink.addEventListener('click', scrollToMenu);
    menuLinkMobile.addEventListener('click', scrollToMenu);

    // Home link click handlers to scroll to menu section
    homeLink.addEventListener('click', scrollToMenu);
    homeLinkMenu.addEventListener('click', scrollToMenu);
    homeLinkMobile.addEventListener('click', scrollToMenu);

    // Initialize cart
    renderCart();
  </script>
 </body>
</html>
