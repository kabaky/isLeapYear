function isLeapYear(year) {
  return (year % 4 === 0 && year % 100 !== 0) || (year % 400 === 0);
}

function countLeapYearsInRange(startYear, endYear) {
  let count = 0;
  for (let year = startYear; year <= endYear; year++) {
    if (isLeapYear(year)) {
      count++;
    }
  }
  return count;
}

function listLeapYearsInRange(startYear, endYear) {
  const leapYears = [];
  for (let year = startYear; year <= endYear; year++) {
    if (isLeapYear(year)) {
      leapYears.push(year);
    }
  }
  return leapYears;
}

const yearToCheck = 2023;
const result = isLeapYear(yearToCheck);

if (result) {
  console.log(`${yearToCheck} is a leap year.`);
} else {
  console.log(`${yearToCheck} is not a leap year.`);
}

const startYear = 2000;
const endYear = 2025;
const countLeap = countLeapYearsInRange(startYear, endYear);
const leapYearsList = listLeapYearsInRange(startYear, endYear);

console.log(`Number of leap years between ${startYear} and ${endYear}: ${countLeap}`);
console.log(`List of leap years between ${startYear} and ${endYear}: ${leapYearsList.join(", ")}`);
