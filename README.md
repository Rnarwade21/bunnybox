# bunnybox
#script.js#
function addReview() {
  const text = document.querySelector("textarea").value;
  if (!text) return;

  const review = document.createElement("div");
  review.innerText = text;
  review.style.marginTop = "10px";

  document.getElementById("reviewList").appendChild(review);
  document.querySelector("textarea").value = "";
}
