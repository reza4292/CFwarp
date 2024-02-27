کانفیگ


{
  "outbounds": 
  [
    {
      "type": "wireguard",
      "tag": "Warp-IR",
      "local_address": [
        "172.16.0.2/32",
        "2606:4700:110:8c91:4063:21d0:7dd5:f218/128"
      ],
      "private_key": "CBVIIWvXdLr4PbSrnm11ZJJ300IiPudRD4R62/IxV1g=",
      "server": "162.159.195.93",
      "server_port": 2506,
      "peer_public_key": "bmXOC+F1FxEMF9dyiK2H5/1SUtzH0JuVo51h2wPfgyo=",
      "reserved": "AAAA",
      "mtu": 1280,
      "fake_packets": "5-10"
    },
    {
      "type": "wireguard",
      "tag": "Warp-Main",
      "detour": "Warp-IR",
      "local_address": [
        "172.16.0.2/32",
        "2606:4700:110:8c15:3f90:ad2d:8810:77f3/128"
      ],
      "private_key": "CCC/TQTc82ub9i8f37Rpix2v425Sv/mxTzvE/iKRMkw=",
      "server": "162.159.195.93",
      "server_port": 2506,
      "peer_public_key": "bmXOC+F1FxEMF9dyiK2H5/1SUtzH0JuVo51h2wPfgyo=",
      "reserved": "AAAA",
      "mtu": 1280,
      "fake_packets": "5-10"
    }
  ]
}











دستور زیر را در termux (Android Shell)، لینوکس یا مک اجرا کنید تا بهترین IP/پورت های کاربردی Cloudflare Warp را بدست آورید


curl -sSL https://raw.githubusercontent.com/reza4292/CFwarp/main/endip.sh -o endip.sh && chmod +x endip.sh && ./endip.sh


دو IP/پورت فایل پیکربندی کپی شده (مرحله 1) را با یکی از IP/پورت حاصل از مرحله 2 قرار دهید.

 دستورالعمل زیر را دو بار اجرا کنید تا دو اکانت Warp رایگان بدست آورید.  هر بار که آن را اجرا می کنید، 3 خط شامل IPv6، کلید خصوصی و بایت های رزرو شده می نویسد.  می توانید مقادیر مربوط به پیکربندی کپی شده (مرحله 1) را با این مقادیر جایگزین کنید.


curl -sSL https://raw.githubusercontent.com/reza4292/CFwarp/main/configure -o configure && chmod +x configure && ./configure


اکنون می توانید از پیکربندی به دست آمده در برنامه Hiddify Next برای دور زدن سانسور استفاده کنید.