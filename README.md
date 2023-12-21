# Template__CSS__Starter
This is template css starter for initial project's step


data.forEach((item) => {
    // Create "li" element and added class name also.
    const elStatsItem = document.createElement("li");
    elStatsItem.classList.add(
      "stats-list__item",
      `stats-list__item--${item.category.toLowerCase()}`
    );
    // Create "img" element and added class name also.
    const elStatsItemImg = document.createElement("img");
    elStatsItemImg.classList.add("stats-list__item-icon");
    elStatsItemImg.src = item.icon;
    elStatsItemImg.alt = "";
    elStatsItemImg.width = "20";
    elStatsItemImg.height = "20";
    elStatsItemImg.ariaHidden = true;

    // Create "span" element for title and added class name also.
    const elStatsItemTitle = document.createElement("span");
    elStatsItemTitle.classList.add("stats-list__item-title");
    elStatsItemTitle.textContent = item.category;

    // Create "span" element for result and added class name also.
    const elStatsItemResult = document.createElement("span");
    elStatsItemResult.classList.add("stats-list__item-result");
    elStatsItemResult.textContent = item.score;

    // Create "span" element for percent-label and added class name also.
    const elStatsItemPercent = document.createElement("span");
    elStatsItemPercent.classList.add("stats-list__item-percent-label");
    elStatsItemPercent.textContent = "%";

    // Create "span" element for max-result(100) and added class name also.
    const elStatsItemMax = document.createElement("span");
    elStatsItemMax.classList.add("stats-list__item-max");
    elStatsItemMax.textContent = "/ 100";

    // We choose li element, and then append to Fragments
    elStatsItem.appendChild(elStatsItemImg);
    elStatsItem.appendChild(elStatsItemTitle);
    elStatsItem.appendChild(elStatsItemResult);
    elStatsItem.appendChild(elStatsItemPercent);
    elStatsItem.appendChild(elStatsItemMax);

    elStatsContentFragment.appendChild(elStatsItem);
  });

  //Then we should choose this fragment element, that append to ul element, it means elStatsList
  elStatsList.appendChild(elStatsContentFragment);