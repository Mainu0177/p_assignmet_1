1.What are some differences between interfaces and types in TypeScript?

TypeScript-এ interface এবং type—দুটির কাজ প্রায় একই মনে হলেও, বাস্তবে কিছু গুরুত্বপূর্ণ পার্থক্য রয়েছে।
১) Extend / Inherit করার নিয়ম
interface → extends ব্যবহার করে বাড়ানো যায়।
type → & (intersection) ব্যবহার করে বাড়ানো হয়।

২) Declaration Merging
interface → একাধিকবার declare করলে একত্রে merge হয়ে যায়।
type → একাধিকবার declare করলে error দেয়।

৩) ব্যবহারযোগ্যতা
interface → object shape নির্ধারণে বেশি ব্যবহৃত হয়।
type → primitive, union, tuple, function ইত্যাদি সবকিছু represent করতে পারে।


2.Explain the difference between any, unknown, and never types in TypeScript.
১) any — যেকোনো কিছু হতে পারে
যখন কোনো ভ্যালু কী টাইপ হবে তা জানি না, তখন any ব্যবহার করা হয়।
downside হলো — TypeScript এর type checking নষ্ট হয়ে যায়।

২) unknown — নিরাপদ any
unknown হলো safer version of any।
এটিতে মান রাখা যায়, কিন্তু ব্যবহার করার আগে টাইপ চেক করতে হয়।

৩) never — কখনোই ঘটে না এমন টাইপ
never সেই value নির্দেশ করে যা কখনো return হয় না।
error throw করা
infinite loop