// 获取当前页面的 URL
console.log("当前页面 URL:", window.location.href);

// 获取页面标题
console.log("页面标题:", document.title);

// 获取页面全部文本内容（去掉脚本和样式）
const textContent = document.body.innerText || document.body.textContent;
console.log("页面纯文本内容:", textContent.substring(0, 500) + "...");

// 获取页面 HTML（完整源码）
const htmlContent = document.documentElement.outerHTML;
console.log("页面 HTML 长度:", htmlContent.length);

// 检测页面是否包含某些关键词
function containsKeyword(keyword) {
    return textContent.toLowerCase().includes(keyword.toLowerCase());
}

if (containsKeyword("登录") || containsKeyword("password")) {
    console.log("检测到可能是登录页面");
}
