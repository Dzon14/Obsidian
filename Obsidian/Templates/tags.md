<%*
const variable = "tags" // CHANGE THIS TO AFFECT ANOTHER VARIBLE IN THE YAML

let content = tp.file.content;
let frontmatterExists = false;
if(content.startsWith("---")) {
	frontmatterExists = true;
} 
let newContent = content;
if(frontmatterExists) {
	const regex = new RegExp(variable+": \\[");
	let match = content.match(regex);
	console.log(match);
	// if varable isn’t a part of the frontmatter, add it at the end
	if(!match){
		var i = 0;
		newContent = content.replace(/---/g, function (match, pos, original) {
		i++;
		return (i ==2 ) ? variable+": [<%tp.file.cursor(1)%"+">]\n---" : match;
		
		});
	} else {
		newContent = content.replace(match[0], variable+": [<%tp.file.cursor(1)%"+">"); //add tag at beginning of variable
	}
} else {
	newContent = "---\n"+variable+": [<%tp.file.cursor(1)%"+">]\n---\n"+content;
	console.log(newContent);
}
var file = app.workspace.activeLeaf.view.file; //get current file
app.vault.modify(file, newContent); //replace file content
_%>