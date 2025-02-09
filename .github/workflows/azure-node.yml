<?php
$TOKEN = "7296290396:AAGbluCXttlmFGuGTN1LPvnMF_7wNBzSCHM"; // BotFather থেকে পাওয়া টোকেন এখানে বসাও
$API_URL = "https://api.telegram.org/bot$TOKEN/";

// JSON ডাটা রিসিভ করা
$update = json_decode(file_get_contents("php://input"), TRUE);

if (isset($update["message"])) {
    $chat_id = $update["message"]["chat"]["id"];
    $message = $update["message"]["text"];

    // যদি ইউজার "/start" পাঠায়
    if ($message == "/start") {
        $reply = "👋 হ্যালো! আমি তোমার টেলিগ্রাম বট। কিভাবে সাহায্য করতে পারি?";
    } else {
        $reply = "❓ তুমি কিছু টাইপ করেছো: " . $message;
    }

    // ইউজারকে রিপ্লাই পাঠানো
    file_get_contents($API_URL . "sendMessage?chat_id=$chat_id&text=" . urlencode($reply));
}
?>
