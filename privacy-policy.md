---
title: Privacy Policy — YT Translate Studio
---

# Privacy Policy — YT Translate Studio

_Last updated: 29 October 2026_
_Contact: lexuanhieu@gmail.com_

YT Translate Studio is a browser extension for Google Chrome that helps YouTube
creators translate the titles, descriptions and subtitles (captions) of their
own videos into multiple languages, directly inside YouTube Studio.

This policy describes what data the extension accesses, why, and what happens
to it. It is written to match the actual behavior of the extension and its
companion components.

## 1. Google account data and OAuth scopes

When you sign in, Google asks you to grant the extension the following
permissions (OAuth scopes):

| Scope | Why the extension needs it |
|---|---|
| `https://www.googleapis.com/auth/youtube.force-ssl` | To read and update **your own** videos' titles, descriptions and subtitle tracks through the official YouTube Data API v3: listing your channels and videos, reading existing localizations and caption tracks, writing translated titles/descriptions, and inserting or deleting translated caption tracks that you request. |
| `https://www.googleapis.com/auth/userinfo.email` | To read the email address of the signed-in Google account. The email is used only as your identity for license/approval checks (see section 4) and to show you which account is signed in. |

Sign-in is handled entirely by Google through Chrome's identity API. The
extension never sees or stores your Google password.

**Access tokens.** The access token issued by Google is held by the browser
(Chrome identity API / the extension's local storage on your device) and is
used only to call Google APIs on your behalf, against your own channels. The
token is not sold, shared, or sent anywhere except as described in section 3.

## 2. Your YouTube content

The extension reads — and, only when you explicitly ask it to, writes — the
following data of videos you select: video titles, descriptions, subtitle
(caption) tracks, and basic channel/video metadata. All reads and writes go
through the official YouTube Data API v3 with your authorization. The
extension does not access videos of channels you do not own or manage, and
does not download or keep copies of your videos.

## 3. Optional local subtitle server (runs on your own computer)

Some subtitle features use an optional companion program (the "subtitle
server") that **you install and run on your own computer**. When the extension
needs that server to write subtitles to your channel, it attaches your current
Google access token to that single request so the server can perform the call
for you. **The subtitle server does not store your token** — it uses the
token for that request only and discards it. Communication between the
extension and this server happens only on your own machine (127.0.0.1 /
localhost). Subtitle files the server saves are stored in folders on your
computer, under your control.

## 4. License server (approval and plan management)

To manage approvals and subscription plans, the extension contacts a license
server operated by the developer (a Google Apps Script web app backed by a
Google Sheet). It sends and the server stores:

- your **email address** (or a license key you enter instead),
- a random **installation ID** generated on your device,
- the **extension version**,
- your **approval status and plan** (e.g. guest / approved, plan limits),
- if you submit a registration request: the plan length, number of machines
  and channels you request, and an optional note you write.

No video content, titles, descriptions or subtitles are ever sent to the
license server. License records are kept while your access is active so the
extension can check your status; see section 7 for deletion.

## 5. Translation providers (chosen by you)

The text you choose to translate (titles, descriptions, subtitle text) is sent
to the translation provider **you select or configure** — for example Google
Translate, MyMemory, DeepL, Google Cloud Translation, or a translation server
running on your own computer — solely to produce the translation you
requested. Translation API keys you enter are stored only in your browser's
extension storage on your device and are never sent to the developer.

## 6. What we do NOT do

- We do not sell or rent your personal data to third parties.
- We do not share your Google account data with anyone, except the services
  described above acting on your instruction.
- We do not use your data for advertising, profiling, or creditworthiness
  purposes.
- We do not collect data from people who do not use the extension.

## 7. Revoking access and deleting your data

- **Revoke access at any time:** visit
  https://myaccount.google.com/permissions and remove YT Translate Studio.
  This immediately stops the extension from accessing your Google account.
- **Local data:** your settings, drafts, queues and API keys are stored in
  your browser and are removed when you uninstall the extension or clear its
  storage.
- **License records:** to request deletion of your license record (email,
  installation IDs, plan and registration data), contact us at
  lexuanhieu@gmail.com. We will delete the record and confirm by email.

## 8. YouTube API Services — Limited Use disclosure

YT Translate Studio uses YouTube API Services. By using the extension you
also agree to the YouTube Terms of Service (https://www.youtube.com/t/terms),
and your use of Google services is covered by the Google Privacy Policy
(https://policies.google.com/privacy).

The extension's use and transfer of information received from Google APIs
adheres to the Google API Services User Data Policy, including the Limited
Use requirements: data obtained through Google APIs is used only to provide
the user-facing features described in this policy, is not transferred to
others except as necessary to provide those features, is not used for
advertising, and is not read by humans except with your consent, for security
purposes, or as required by law.

## 9. Changes to this policy

We may update this policy. The current version will always be available at
this address, with a new "last updated" date.

---

# Chính sách bảo mật — YT Translate Studio (bản tiếng Việt)

_Cập nhật lần cuối: 29/10/2026_
_Liên hệ: lexuanhieu@gmail.com_

YT Translate Studio là tiện ích mở rộng (extension) cho trình duyệt Chrome,
giúp người sáng tạo YouTube dịch tiêu đề, mô tả và phụ đề video của chính họ
sang nhiều ngôn ngữ, ngay trong YouTube Studio.

## Extension truy cập những dữ liệu nào, để làm gì

- **Quyền YouTube (`youtube.force-ssl`):** đọc và ghi tiêu đề, mô tả, phụ đề
  của **chính video của bạn** qua YouTube Data API v3 chính thức: xem kênh và
  video của bạn, đọc bản địa hóa/phụ đề hiện có, ghi tiêu đề/mô tả đã dịch,
  thêm hoặc xóa track phụ đề đã dịch theo yêu cầu của bạn.
- **Email (`userinfo.email`):** đọc địa chỉ email của tài khoản Google đang
  đăng nhập, chỉ dùng làm định danh để kiểm tra bản quyền/gói sử dụng và hiển
  thị cho bạn biết đang đăng nhập bằng tài khoản nào.
- Đăng nhập do Google xử lý toàn bộ qua Chrome identity API — extension
  **không bao giờ thấy hay lưu mật khẩu Google** của bạn. Access token do
  Google cấp được giữ trong trình duyệt của bạn và chỉ dùng để gọi API thay
  bạn, trên kênh của bạn.

## Máy chủ phụ đề (tùy chọn, chạy trên máy của bạn)

Một số tính năng phụ đề dùng chương trình companion chạy trên **chính máy
tính của bạn**. Khi cần máy chủ này ghi phụ đề lên kênh, extension đính kèm
access token hiện tại vào đúng lượt gọi đó; **máy chủ không lưu token** —
dùng xong là bỏ. Mọi trao đổi chỉ diễn ra trong máy của bạn (127.0.0.1).

## Máy chủ bản quyền

Để quản lý duyệt tài khoản và gói sử dụng, extension liên hệ máy chủ bản
quyền của nhà phát triển (Google Apps Script + Google Sheet). Máy chủ lưu:
email của bạn (hoặc license key bạn nhập), mã cài đặt ngẫu nhiên trên máy
bạn, phiên bản extension, trạng thái duyệt và gói của bạn; nếu bạn gửi yêu
cầu đăng ký: số ngày gói, số máy, số kênh bạn chọn và ghi chú bạn viết.
**Không có nội dung video nào được gửi tới máy chủ bản quyền.**

## Nhà cung cấp dịch

Văn bản bạn chọn dịch chỉ được gửi tới nhà cung cấp **bạn chọn hoặc cấu
hình** (Google Translate, MyMemory, DeepL, Google Cloud Translation, hoặc
máy chủ dịch trên máy của bạn) để tạo bản dịch bạn yêu cầu. API key bạn nhập
chỉ lưu trong trình duyệt của bạn, không gửi cho nhà phát triển.

## Cam kết

- Không bán, không cho thuê dữ liệu cá nhân; không chia sẻ dữ liệu tài khoản
  Google ngoài các dịch vụ nêu trên khi bạn yêu cầu.
- Không dùng dữ liệu cho quảng cáo, hồ sơ hóa hay đánh giá tín dụng.
- Việc dùng dữ liệu từ Google API tuân thủ Google API Services User Data
  Policy, gồm yêu cầu Limited Use.

## Thu hồi quyền và xóa dữ liệu

- **Thu hồi quyền bất cứ lúc nào:** vào https://myaccount.google.com/permissions
  và gỡ YT Translate Studio — extension lập tức mất quyền truy cập.
- **Dữ liệu cục bộ** (cài đặt, bản nháp, hàng đợi, API key) nằm trong trình
  duyệt và bị xóa khi bạn gỡ extension.
- **Hồ sơ bản quyền:** muốn xóa hồ sơ (email, mã cài đặt, gói, dữ liệu đăng
  ký), liên hệ lexuanhieu@gmail.com — chúng tôi sẽ xóa và xác nhận lại qua email.

Sử dụng extension đồng nghĩa bạn cũng đồng ý với Điều khoản dịch vụ YouTube
(https://www.youtube.com/t/terms); việc dùng dịch vụ Google của bạn tuân
theo Chính sách bảo mật của Google (https://policies.google.com/privacy).
