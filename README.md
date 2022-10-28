<a href="https://github.com/anuraghazra/github-readme-stats">
  <img align="left" src="https://github-readme-stats.vercel.app/api?username=uehoho18&count_private=true&show_icons=true"　/>
</a>
<a href="https://github.com/anuraghazra/github-readme-stats">
  <img align="left" src="https://github-readme-stats.vercel.app/api/top-langs/?username=uehoho18"/>　   
</a>　


// Flutter imports:
import 'package:flutter/material.dart';

// Package imports:
import 'package:flutter_riverpod/flutter_riverpod.dart';

// Project imports:
import 'package:base_app/riverpod/screen_index_provider.dart';
import 'package:base_app/riverpod/tab_index_provider.dart';
import 'package:base_app/ui/common_components/base_main_app_bar.dart';
import 'package:base_app/ui/pages/home/components/home_button.dart';
import 'package:base_app/ui/pages/home/components/home_carousel.dart';

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      //resizeToAvoidBottomInsetはキーボードが開かれた際にbodyのサイズが変わらないための設定
      //デフォルトではtrueになっているため、falseにしない限り、Flutter側でbodyサイズを変更してしまう。
      resizeToAvoidBottomInset: false,
      appBar: BaseMainAppBar(context),
      body: SingleChildScrollView(
        child: Column(
          children: [
            HomeCarousel(),
            Padding(
              padding: const EdgeInsets.all(8),
              child: Column(
                children: [
                  HomeButton(
                    label: '会員証',
                    subLabel: 'MEMBER ID',
                    onPressed: () => context.read(tabIndexProvider).state = 2,
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: '最新情報　　',
                          subLabel: 'TOPICS',
                          onPressed: () =>
                              context.read(screenIndexProvider).state = 6,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '店舗検索　　',
                          subLabel: 'SHOP SEARCH',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 3,
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'クーポン　　',
                          subLabel: 'COUPON',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 1,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: 'WEB 屋台　  ',
                          subLabel: 'ONLINE SHOP',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'マイクーポン',
                          subLabel: 'MY COUPON',
                          onPressed: () {
                          },
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '採用情報　　',
                          subLabel: 'RECRUIT',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}

// Flutter imports:
import 'package:flutter/material.dart';

// Package imports:
import 'package:flutter_riverpod/flutter_riverpod.dart';

// Project imports:
import 'package:base_app/riverpod/screen_index_provider.dart';
import 'package:base_app/riverpod/tab_index_provider.dart';
import 'package:base_app/ui/common_components/base_main_app_bar.dart';
import 'package:base_app/ui/pages/home/components/home_button.dart';
import 'package:base_app/ui/pages/home/components/home_carousel.dart';

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      //resizeToAvoidBottomInsetはキーボードが開かれた際にbodyのサイズが変わらないための設定
      //デフォルトではtrueになっているため、falseにしない限り、Flutter側でbodyサイズを変更してしまう。
      resizeToAvoidBottomInset: false,
      appBar: BaseMainAppBar(context),
      body: SingleChildScrollView(
        child: Column(
          children: [
            HomeCarousel(),
            Padding(
              padding: const EdgeInsets.all(8),
              child: Column(
                children: [
                  HomeButton(
                    label: '会員証',
                    subLabel: 'MEMBER ID',
                    onPressed: () => context.read(tabIndexProvider).state = 2,
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: '最新情報　　',
                          subLabel: 'TOPICS',
                          onPressed: () =>
                              context.read(screenIndexProvider).state = 6,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '店舗検索　　',
                          subLabel: 'SHOP SEARCH',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 3,
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'クーポン　　',
                          subLabel: 'COUPON',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 1,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: 'WEB 屋台　  ',
                          subLabel: 'ONLINE SHOP',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'マイクーポン',
                          subLabel: 'MY COUPON',
                          onPressed: () {
                          },
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '採用情報　　',
                          subLabel: 'RECRUIT',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}

// Flutter imports:
import 'package:flutter/material.dart';

// Package imports:
import 'package:flutter_riverpod/flutter_riverpod.dart';

// Project imports:
import 'package:base_app/riverpod/screen_index_provider.dart';
import 'package:base_app/riverpod/tab_index_provider.dart';
import 'package:base_app/ui/common_components/base_main_app_bar.dart';
import 'package:base_app/ui/pages/home/components/home_button.dart';
import 'package:base_app/ui/pages/home/components/home_carousel.dart';

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      //resizeToAvoidBottomInsetはキーボードが開かれた際にbodyのサイズが変わらないための設定
      //デフォルトではtrueになっているため、falseにしない限り、Flutter側でbodyサイズを変更してしまう。
      resizeToAvoidBottomInset: false,
      appBar: BaseMainAppBar(context),
      body: SingleChildScrollView(
        child: Column(
          children: [
            HomeCarousel(),
            Padding(
              padding: const EdgeInsets.all(8),
              child: Column(
                children: [
                  HomeButton(
                    label: '会員証',
                    subLabel: 'MEMBER ID',
                    onPressed: () => context.read(tabIndexProvider).state = 2,
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: '最新情報　　',
                          subLabel: 'TOPICS',
                          onPressed: () =>
                              context.read(screenIndexProvider).state = 6,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '店舗検索　　',
                          subLabel: 'SHOP SEARCH',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 3,
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'クーポン　　',
                          subLabel: 'COUPON',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 1,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: 'WEB 屋台　  ',
                          subLabel: 'ONLINE SHOP',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'マイクーポン',
                          subLabel: 'MY COUPON',
                          onPressed: () {
                          },
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '採用情報　　',
                          subLabel: 'RECRUIT',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}

// Flutter imports:
import 'package:flutter/material.dart';

// Package imports:
import 'package:flutter_riverpod/flutter_riverpod.dart';

// Project imports:
import 'package:base_app/riverpod/screen_index_provider.dart';
import 'package:base_app/riverpod/tab_index_provider.dart';
import 'package:base_app/ui/common_components/base_main_app_bar.dart';
import 'package:base_app/ui/pages/home/components/home_button.dart';
import 'package:base_app/ui/pages/home/components/home_carousel.dart';

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      //resizeToAvoidBottomInsetはキーボードが開かれた際にbodyのサイズが変わらないための設定
      //デフォルトではtrueになっているため、falseにしない限り、Flutter側でbodyサイズを変更してしまう。
      resizeToAvoidBottomInset: false,
      appBar: BaseMainAppBar(context),
      body: SingleChildScrollView(
        child: Column(
          children: [
            HomeCarousel(),
            Padding(
              padding: const EdgeInsets.all(8),
              child: Column(
                children: [
                  HomeButton(
                    label: '会員証',
                    subLabel: 'MEMBER ID',
                    onPressed: () => context.read(tabIndexProvider).state = 2,
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: '最新情報　　',
                          subLabel: 'TOPICS',
                          onPressed: () =>
                              context.read(screenIndexProvider).state = 6,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '店舗検索　　',
                          subLabel: 'SHOP SEARCH',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 3,
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'クーポン　　',
                          subLabel: 'COUPON',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 1,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: 'WEB 屋台　  ',
                          subLabel: 'ONLINE SHOP',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'マイクーポン',
                          subLabel: 'MY COUPON',
                          onPressed: () {
                          },
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '採用情報　　',
                          subLabel: 'RECRUIT',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}
// Flutter imports:
import 'package:flutter/material.dart';

// Package imports:
import 'package:flutter_riverpod/flutter_riverpod.dart';

// Project imports:
import 'package:base_app/riverpod/screen_index_provider.dart';
import 'package:base_app/riverpod/tab_index_provider.dart';
import 'package:base_app/ui/common_components/base_main_app_bar.dart';
import 'package:base_app/ui/pages/home/components/home_button.dart';
import 'package:base_app/ui/pages/home/components/home_carousel.dart';

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      //resizeToAvoidBottomInsetはキーボードが開かれた際にbodyのサイズが変わらないための設定
      //デフォルトではtrueになっているため、falseにしない限り、Flutter側でbodyサイズを変更してしまう。
      resizeToAvoidBottomInset: false,
      appBar: BaseMainAppBar(context),
      body: SingleChildScrollView(
        child: Column(
          children: [
            HomeCarousel(),
            Padding(
              padding: const EdgeInsets.all(8),
              child: Column(
                children: [
                  HomeButton(
                    label: '会員証',
                    subLabel: 'MEMBER ID',
                    onPressed: () => context.read(tabIndexProvider).state = 2,
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: '最新情報　　',
                          subLabel: 'TOPICS',
                          onPressed: () =>
                              context.read(screenIndexProvider).state = 6,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '店舗検索　　',
                          subLabel: 'SHOP SEARCH',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 3,
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'クーポン　　',
                          subLabel: 'COUPON',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 1,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: 'WEB 屋台　  ',
                          subLabel: 'ONLINE SHOP',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'マイクーポン',
                          subLabel: 'MY COUPON',
                          onPressed: () {
                          },
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '採用情報　　',
                          subLabel: 'RECRUIT',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}
// Flutter imports:
import 'package:flutter/material.dart';

// Package imports:
import 'package:flutter_riverpod/flutter_riverpod.dart';

// Project imports:
import 'package:base_app/riverpod/screen_index_provider.dart';
import 'package:base_app/riverpod/tab_index_provider.dart';
import 'package:base_app/ui/common_components/base_main_app_bar.dart';
import 'package:base_app/ui/pages/home/components/home_button.dart';
import 'package:base_app/ui/pages/home/components/home_carousel.dart';

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      //resizeToAvoidBottomInsetはキーボードが開かれた際にbodyのサイズが変わらないための設定
      //デフォルトではtrueになっているため、falseにしない限り、Flutter側でbodyサイズを変更してしまう。
      resizeToAvoidBottomInset: false,
      appBar: BaseMainAppBar(context),
      body: SingleChildScrollView(
        child: Column(
          children: [
            HomeCarousel(),
            Padding(
              padding: const EdgeInsets.all(8),
              child: Column(
                children: [
                  HomeButton(
                    label: '会員証',
                    subLabel: 'MEMBER ID',
                    onPressed: () => context.read(tabIndexProvider).state = 2,
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: '最新情報　　',
                          subLabel: 'TOPICS',
                          onPressed: () =>
                              context.read(screenIndexProvider).state = 6,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '店舗検索　　',
                          subLabel: 'SHOP SEARCH',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 3,
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'クーポン　　',
                          subLabel: 'COUPON',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 1,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: 'WEB 屋台　  ',
                          subLabel: 'ONLINE SHOP',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'マイクーポン',
                          subLabel: 'MY COUPON',
                          onPressed: () {
                          },
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '採用情報　　',
                          subLabel: 'RECRUIT',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}
// Flutter imports:
import 'package:flutter/material.dart';

// Package imports:
import 'package:flutter_riverpod/flutter_riverpod.dart';

// Project imports:
import 'package:base_app/riverpod/screen_index_provider.dart';
import 'package:base_app/riverpod/tab_index_provider.dart';
import 'package:base_app/ui/common_components/base_main_app_bar.dart';
import 'package:base_app/ui/pages/home/components/home_button.dart';
import 'package:base_app/ui/pages/home/components/home_carousel.dart';

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      //resizeToAvoidBottomInsetはキーボードが開かれた際にbodyのサイズが変わらないための設定
      //デフォルトではtrueになっているため、falseにしない限り、Flutter側でbodyサイズを変更してしまう。
      resizeToAvoidBottomInset: false,
      appBar: BaseMainAppBar(context),
      body: SingleChildScrollView(
        child: Column(
          children: [
            HomeCarousel(),
            Padding(
              padding: const EdgeInsets.all(8),
              child: Column(
                children: [
                  HomeButton(
                    label: '会員証',
                    subLabel: 'MEMBER ID',
                    onPressed: () => context.read(tabIndexProvider).state = 2,
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: '最新情報　　',
                          subLabel: 'TOPICS',
                          onPressed: () =>
                              context.read(screenIndexProvider).state = 6,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '店舗検索　　',
                          subLabel: 'SHOP SEARCH',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 3,
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'クーポン　　',
                          subLabel: 'COUPON',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 1,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: 'WEB 屋台　  ',
                          subLabel: 'ONLINE SHOP',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'マイクーポン',
                          subLabel: 'MY COUPON',
                          onPressed: () {
                          },
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '採用情報　　',
                          subLabel: 'RECRUIT',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}
// Flutter imports:
import 'package:flutter/material.dart';

// Package imports:
import 'package:flutter_riverpod/flutter_riverpod.dart';

// Project imports:
import 'package:base_app/riverpod/screen_index_provider.dart';
import 'package:base_app/riverpod/tab_index_provider.dart';
import 'package:base_app/ui/common_components/base_main_app_bar.dart';
import 'package:base_app/ui/pages/home/components/home_button.dart';
import 'package:base_app/ui/pages/home/components/home_carousel.dart';

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      //resizeToAvoidBottomInsetはキーボードが開かれた際にbodyのサイズが変わらないための設定
      //デフォルトではtrueになっているため、falseにしない限り、Flutter側でbodyサイズを変更してしまう。
      resizeToAvoidBottomInset: false,
      appBar: BaseMainAppBar(context),
      body: SingleChildScrollView(
        child: Column(
          children: [
            HomeCarousel(),
            Padding(
              padding: const EdgeInsets.all(8),
              child: Column(
                children: [
                  HomeButton(
                    label: '会員証',
                    subLabel: 'MEMBER ID',
                    onPressed: () => context.read(tabIndexProvider).state = 2,
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: '最新情報　　',
                          subLabel: 'TOPICS',
                          onPressed: () =>
                              context.read(screenIndexProvider).state = 6,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '店舗検索　　',
                          subLabel: 'SHOP SEARCH',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 3,
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'クーポン　　',
                          subLabel: 'COUPON',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 1,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: 'WEB 屋台　  ',
                          subLabel: 'ONLINE SHOP',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'マイクーポン',
                          subLabel: 'MY COUPON',
                          onPressed: () {
                          },
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '採用情報　　',
                          subLabel: 'RECRUIT',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}
// Flutter imports:
import 'package:flutter/material.dart';

// Package imports:
import 'package:flutter_riverpod/flutter_riverpod.dart';

// Project imports:
import 'package:base_app/riverpod/screen_index_provider.dart';
import 'package:base_app/riverpod/tab_index_provider.dart';
import 'package:base_app/ui/common_components/base_main_app_bar.dart';
import 'package:base_app/ui/pages/home/components/home_button.dart';
import 'package:base_app/ui/pages/home/components/home_carousel.dart';

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      //resizeToAvoidBottomInsetはキーボードが開かれた際にbodyのサイズが変わらないための設定
      //デフォルトではtrueになっているため、falseにしない限り、Flutter側でbodyサイズを変更してしまう。
      resizeToAvoidBottomInset: false,
      appBar: BaseMainAppBar(context),
      body: SingleChildScrollView(
        child: Column(
          children: [
            HomeCarousel(),
            Padding(
              padding: const EdgeInsets.all(8),
              child: Column(
                children: [
                  HomeButton(
                    label: '会員証',
                    subLabel: 'MEMBER ID',
                    onPressed: () => context.read(tabIndexProvider).state = 2,
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: '最新情報　　',
                          subLabel: 'TOPICS',
                          onPressed: () =>
                              context.read(screenIndexProvider).state = 6,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '店舗検索　　',
                          subLabel: 'SHOP SEARCH',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 3,
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'クーポン　　',
                          subLabel: 'COUPON',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 1,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: 'WEB 屋台　  ',
                          subLabel: 'ONLINE SHOP',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'マイクーポン',
                          subLabel: 'MY COUPON',
                          onPressed: () {
                          },
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '採用情報　　',
                          subLabel: 'RECRUIT',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}
// Flutter imports:
import 'package:flutter/material.dart';

// Package imports:
import 'package:flutter_riverpod/flutter_riverpod.dart';

// Project imports:
import 'package:base_app/riverpod/screen_index_provider.dart';
import 'package:base_app/riverpod/tab_index_provider.dart';
import 'package:base_app/ui/common_components/base_main_app_bar.dart';
import 'package:base_app/ui/pages/home/components/home_button.dart';
import 'package:base_app/ui/pages/home/components/home_carousel.dart';

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      //resizeToAvoidBottomInsetはキーボードが開かれた際にbodyのサイズが変わらないための設定
      //デフォルトではtrueになっているため、falseにしない限り、Flutter側でbodyサイズを変更してしまう。
      resizeToAvoidBottomInset: false,
      appBar: BaseMainAppBar(context),
      body: SingleChildScrollView(
        child: Column(
          children: [
            HomeCarousel(),
            Padding(
              padding: const EdgeInsets.all(8),
              child: Column(
                children: [
                  HomeButton(
                    label: '会員証',
                    subLabel: 'MEMBER ID',
                    onPressed: () => context.read(tabIndexProvider).state = 2,
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: '最新情報　　',
                          subLabel: 'TOPICS',
                          onPressed: () =>
                              context.read(screenIndexProvider).state = 6,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '店舗検索　　',
                          subLabel: 'SHOP SEARCH',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 3,
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'クーポン　　',
                          subLabel: 'COUPON',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 1,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: 'WEB 屋台　  ',
                          subLabel: 'ONLINE SHOP',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'マイクーポン',
                          subLabel: 'MY COUPON',
                          onPressed: () {
                          },
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '採用情報　　',
                          subLabel: 'RECRUIT',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}
// Flutter imports:
import 'package:flutter/material.dart';

// Package imports:
import 'package:flutter_riverpod/flutter_riverpod.dart';

// Project imports:
import 'package:base_app/riverpod/screen_index_provider.dart';
import 'package:base_app/riverpod/tab_index_provider.dart';
import 'package:base_app/ui/common_components/base_main_app_bar.dart';
import 'package:base_app/ui/pages/home/components/home_button.dart';
import 'package:base_app/ui/pages/home/components/home_carousel.dart';

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      //resizeToAvoidBottomInsetはキーボードが開かれた際にbodyのサイズが変わらないための設定
      //デフォルトではtrueになっているため、falseにしない限り、Flutter側でbodyサイズを変更してしまう。
      resizeToAvoidBottomInset: false,
      appBar: BaseMainAppBar(context),
      body: SingleChildScrollView(
        child: Column(
          children: [
            HomeCarousel(),
            Padding(
              padding: const EdgeInsets.all(8),
              child: Column(
                children: [
                  HomeButton(
                    label: '会員証',
                    subLabel: 'MEMBER ID',
                    onPressed: () => context.read(tabIndexProvider).state = 2,
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: '最新情報　　',
                          subLabel: 'TOPICS',
                          onPressed: () =>
                              context.read(screenIndexProvider).state = 6,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '店舗検索　　',
                          subLabel: 'SHOP SEARCH',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 3,
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'クーポン　　',
                          subLabel: 'COUPON',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 1,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: 'WEB 屋台　  ',
                          subLabel: 'ONLINE SHOP',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'マイクーポン',
                          subLabel: 'MY COUPON',
                          onPressed: () {
                          },
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '採用情報　　',
                          subLabel: 'RECRUIT',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}
// Flutter imports:
import 'package:flutter/material.dart';

// Package imports:
import 'package:flutter_riverpod/flutter_riverpod.dart';

// Project imports:
import 'package:base_app/riverpod/screen_index_provider.dart';
import 'package:base_app/riverpod/tab_index_provider.dart';
import 'package:base_app/ui/common_components/base_main_app_bar.dart';
import 'package:base_app/ui/pages/home/components/home_button.dart';
import 'package:base_app/ui/pages/home/components/home_carousel.dart';

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      //resizeToAvoidBottomInsetはキーボードが開かれた際にbodyのサイズが変わらないための設定
      //デフォルトではtrueになっているため、falseにしない限り、Flutter側でbodyサイズを変更してしまう。
      resizeToAvoidBottomInset: false,
      appBar: BaseMainAppBar(context),
      body: SingleChildScrollView(
        child: Column(
          children: [
            HomeCarousel(),
            Padding(
              padding: const EdgeInsets.all(8),
              child: Column(
                children: [
                  HomeButton(
                    label: '会員証',
                    subLabel: 'MEMBER ID',
                    onPressed: () => context.read(tabIndexProvider).state = 2,
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: '最新情報　　',
                          subLabel: 'TOPICS',
                          onPressed: () =>
                              context.read(screenIndexProvider).state = 6,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '店舗検索　　',
                          subLabel: 'SHOP SEARCH',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 3,
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'クーポン　　',
                          subLabel: 'COUPON',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 1,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: 'WEB 屋台　  ',
                          subLabel: 'ONLINE SHOP',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'マイクーポン',
                          subLabel: 'MY COUPON',
                          onPressed: () {
                          },
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '採用情報　　',
                          subLabel: 'RECRUIT',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}
// Flutter imports:
import 'package:flutter/material.dart';

// Package imports:
import 'package:flutter_riverpod/flutter_riverpod.dart';

// Project imports:
import 'package:base_app/riverpod/screen_index_provider.dart';
import 'package:base_app/riverpod/tab_index_provider.dart';
import 'package:base_app/ui/common_components/base_main_app_bar.dart';
import 'package:base_app/ui/pages/home/components/home_button.dart';
import 'package:base_app/ui/pages/home/components/home_carousel.dart';

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      //resizeToAvoidBottomInsetはキーボードが開かれた際にbodyのサイズが変わらないための設定
      //デフォルトではtrueになっているため、falseにしない限り、Flutter側でbodyサイズを変更してしまう。
      resizeToAvoidBottomInset: false,
      appBar: BaseMainAppBar(context),
      body: SingleChildScrollView(
        child: Column(
          children: [
            HomeCarousel(),
            Padding(
              padding: const EdgeInsets.all(8),
              child: Column(
                children: [
                  HomeButton(
                    label: '会員証',
                    subLabel: 'MEMBER ID',
                    onPressed: () => context.read(tabIndexProvider).state = 2,
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: '最新情報　　',
                          subLabel: 'TOPICS',
                          onPressed: () =>
                              context.read(screenIndexProvider).state = 6,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '店舗検索　　',
                          subLabel: 'SHOP SEARCH',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 3,
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'クーポン　　',
                          subLabel: 'COUPON',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 1,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: 'WEB 屋台　  ',
                          subLabel: 'ONLINE SHOP',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'マイクーポン',
                          subLabel: 'MY COUPON',
                          onPressed: () {
                          },
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '採用情報　　',
                          subLabel: 'RECRUIT',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}
// Flutter imports:
import 'package:flutter/material.dart';

// Package imports:
import 'package:flutter_riverpod/flutter_riverpod.dart';

// Project imports:
import 'package:base_app/riverpod/screen_index_provider.dart';
import 'package:base_app/riverpod/tab_index_provider.dart';
import 'package:base_app/ui/common_components/base_main_app_bar.dart';
import 'package:base_app/ui/pages/home/components/home_button.dart';
import 'package:base_app/ui/pages/home/components/home_carousel.dart';

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      //resizeToAvoidBottomInsetはキーボードが開かれた際にbodyのサイズが変わらないための設定
      //デフォルトではtrueになっているため、falseにしない限り、Flutter側でbodyサイズを変更してしまう。
      resizeToAvoidBottomInset: false,
      appBar: BaseMainAppBar(context),
      body: SingleChildScrollView(
        child: Column(
          children: [
            HomeCarousel(),
            Padding(
              padding: const EdgeInsets.all(8),
              child: Column(
                children: [
                  HomeButton(
                    label: '会員証',
                    subLabel: 'MEMBER ID',
                    onPressed: () => context.read(tabIndexProvider).state = 2,
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: '最新情報　　',
                          subLabel: 'TOPICS',
                          onPressed: () =>
                              context.read(screenIndexProvider).state = 6,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '店舗検索　　',
                          subLabel: 'SHOP SEARCH',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 3,
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'クーポン　　',
                          subLabel: 'COUPON',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 1,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: 'WEB 屋台　  ',
                          subLabel: 'ONLINE SHOP',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'マイクーポン',
                          subLabel: 'MY COUPON',
                          onPressed: () {
                          },
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '採用情報　　',
                          subLabel: 'RECRUIT',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}
// Flutter imports:
import 'package:flutter/material.dart';

// Package imports:
import 'package:flutter_riverpod/flutter_riverpod.dart';

// Project imports:
import 'package:base_app/riverpod/screen_index_provider.dart';
import 'package:base_app/riverpod/tab_index_provider.dart';
import 'package:base_app/ui/common_components/base_main_app_bar.dart';
import 'package:base_app/ui/pages/home/components/home_button.dart';
import 'package:base_app/ui/pages/home/components/home_carousel.dart';

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      //resizeToAvoidBottomInsetはキーボードが開かれた際にbodyのサイズが変わらないための設定
      //デフォルトではtrueになっているため、falseにしない限り、Flutter側でbodyサイズを変更してしまう。
      resizeToAvoidBottomInset: false,
      appBar: BaseMainAppBar(context),
      body: SingleChildScrollView(
        child: Column(
          children: [
            HomeCarousel(),
            Padding(
              padding: const EdgeInsets.all(8),
              child: Column(
                children: [
                  HomeButton(
                    label: '会員証',
                    subLabel: 'MEMBER ID',
                    onPressed: () => context.read(tabIndexProvider).state = 2,
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: '最新情報　　',
                          subLabel: 'TOPICS',
                          onPressed: () =>
                              context.read(screenIndexProvider).state = 6,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '店舗検索　　',
                          subLabel: 'SHOP SEARCH',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 3,
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'クーポン　　',
                          subLabel: 'COUPON',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 1,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: 'WEB 屋台　  ',
                          subLabel: 'ONLINE SHOP',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'マイクーポン',
                          subLabel: 'MY COUPON',
                          onPressed: () {
                          },
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '採用情報　　',
                          subLabel: 'RECRUIT',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}
// Flutter imports:
import 'package:flutter/material.dart';

// Package imports:
import 'package:flutter_riverpod/flutter_riverpod.dart';

// Project imports:
import 'package:base_app/riverpod/screen_index_provider.dart';
import 'package:base_app/riverpod/tab_index_provider.dart';
import 'package:base_app/ui/common_components/base_main_app_bar.dart';
import 'package:base_app/ui/pages/home/components/home_button.dart';
import 'package:base_app/ui/pages/home/components/home_carousel.dart';

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      //resizeToAvoidBottomInsetはキーボードが開かれた際にbodyのサイズが変わらないための設定
      //デフォルトではtrueになっているため、falseにしない限り、Flutter側でbodyサイズを変更してしまう。
      resizeToAvoidBottomInset: false,
      appBar: BaseMainAppBar(context),
      body: SingleChildScrollView(
        child: Column(
          children: [
            HomeCarousel(),
            Padding(
              padding: const EdgeInsets.all(8),
              child: Column(
                children: [
                  HomeButton(
                    label: '会員証',
                    subLabel: 'MEMBER ID',
                    onPressed: () => context.read(tabIndexProvider).state = 2,
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: '最新情報　　',
                          subLabel: 'TOPICS',
                          onPressed: () =>
                              context.read(screenIndexProvider).state = 6,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '店舗検索　　',
                          subLabel: 'SHOP SEARCH',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 3,
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'クーポン　　',
                          subLabel: 'COUPON',
                          onPressed: () =>
                              context.read(tabIndexProvider).state = 1,
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: 'WEB 屋台　  ',
                          subLabel: 'ONLINE SHOP',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                  const SizedBox(height: 10),
                  Row(
                    children: [
                      Expanded(
                        child: HomeButton(
                          label: 'マイクーポン',
                          subLabel: 'MY COUPON',
                          onPressed: () {
                          },
                        ),
                      ),
                      const SizedBox(width: 10),
                      Expanded(
                        child: HomeButton(
                          label: '採用情報　　',
                          subLabel: 'RECRUIT',
                          onPressed: () {
                          },
                        ),
                      ),
                    ],
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}
