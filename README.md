دستور زیر را در termux (Android Shell)، لینوکس یا مک اجرا کنید تا بهترین IP/پورت های کاربردی Cloudflare Warp را بدست آورید
curl -sSL https://raw.githubusercontent.com/reza4292/CFwarp/main/endip.sh -o endip.sh && chmod +x endip.sh && ./endip.sh
دو IP/پورت فایل پیکربندی کپی شده (مرحله 1) را با یکی از IP/پورت حاصل از مرحله 2 قرار دهید.

 دستورالعمل زیر را دو بار اجرا کنید تا دو اکانت Warp رایگان بدست آورید.  هر بار که آن را اجرا می کنید، 3 خط شامل IPv6، کلید خصوصی و بایت های رزرو شده می نویسد.  می توانید مقادیر مربوط به پیکربندی کپی شده (مرحله 1) را با این مقادیر جایگزین کنید.
curl -sSL https://raw.githubusercontent.com/reza4292/CFwarp/main/configure -o configure && chmod +x configure && ./configure
اکنون می توانید از پیکربندی به دست آمده در برنامه Hiddify Next برای دور زدن سانسور استفاده کنید.