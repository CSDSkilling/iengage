---
layout: default
title:  " Line of Business -Architecture"
category: "Gamification123"
sub-category: "Digital and App Innovation"

---
# Introduction to the Line of Business Extension Game

Welcome to the **Line of Business Extension Game**! This interactive game is designed to help you understand the flow of data through a business solution using various Azure services. You'll be able to drag and drop icons representing different Azure services onto a canvas, simulating how data moves and is processed within a business environment.

## Steps to Play

1. **Start by understanding the data flow:**
   - Read the steps provided below the canvas to understand how data moves through the solution.

2. **Arrange the icons:**
   - Drag each icon from the top row and place it on the canvas in the order that represents the data flow steps.

3. **Review and adjust:**
   - Ensure that the icons are placed correctly to reflect the data flow accurately.


Enjoy the game and learn how these Azure services work together to streamline business processes! 

{% raw %}


<canvas id="myCanvas" width="1000" height="830" style="border:1px solid #000000;"></canvas>

## Data Flow Steps

1. Supplier data stored in Common Data Services (CDS) is moved to SQL via Data Factory.
2. Purchase order (PO) data stored in the ERP system is sent to the Azure SQL database.
3. Azure API Management is used to expose an Azure function to the Power Platform.
4. Power Apps retrieves data from the Azure SQL Database through the Azure Function being exposed by Azure API Management.
5. User reviews and updates POs in Power Apps and sends this data to suppliers through CSV exports.
6. Power BI reports trends in supplier status.


<button id="showSolutionButton" onclick="showSolution()">Show Solution</button>
<div id="solutionImageContainer"></div>

<script>
    const canvas = document.getElementById('myCanvas');
    const ctx = canvas.getContext('2d');
    const images = [
        { src: './images/adf.png', x: 50, y: 10, width: 50, height: 50, isDragging: false, name: 'Azure Data Factory' },
        { src: './images/func1.png', x: 200, y: 10, width: 50, height: 50, isDragging: false, name: 'Azure Function' },
        { src: './images/pbi.png', x: 350, y: 10, width: 50, height: 50, isDragging: false, name: 'Power BI' },
        { src: './images/apim.png', x: 500, y: 10, width: 50, height: 50, isDragging: false, name: 'API Management' }
    ];
    let dragIndex = -1;

    function loadImages(callback) {
        let loadedImages = 0;
        images.forEach((image, index) => {
            const img = new Image();
            img.src = image.src;
            img.onload = () => {
                images[index].img = img;
                loadedImages++;
                if (loadedImages === images.length) {
                    callback();
                }
            };
        });
    }

    function drawImages() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        images.forEach(image => {
            ctx.drawImage(image.img, image.x, image.y, image.width, image.height);
        });
        // Draw 3D divider line
        draw3DDivider();
    }

    function draw3DDivider() {
        const gradient = ctx.createLinearGradient(0, 80, canvas.width, 80);
        gradient.addColorStop(0, '#d3d3d3');
        gradient.addColorStop(0.5, '#ffffff');
        gradient.addColorStop(1, '#d3d3d3');

        ctx.strokeStyle = gradient;
        ctx.lineWidth = 4;
        ctx.beginPath();
        ctx.moveTo(0, 80); // Adjust the y-coordinate as needed
        ctx.lineTo(canvas.width, 80);
        ctx.stroke();

        ctx.strokeStyle = 'rgba(0, 0, 0, 0.2)';
        ctx.lineWidth = 2;
        ctx.beginPath();
        ctx.moveTo(0, 82); // Slightly below the main line for shadow effect
        ctx.lineTo(canvas.width, 82);
        ctx.stroke();
    }

    function getMousePos(canvas, evt) {
        const rect = canvas.getBoundingClientRect();
        return {
            x: evt.clientX - rect.left,
            y: evt.clientY - rect.top
        };
    }

    function isMouseInImage(mouse, image) {
        return mouse.x > image.x && mouse.x < image.x + image.width &&
               mouse.y > image.y && mouse.y < image.y + image.height;
    }

    canvas.addEventListener('mousedown', (evt) => {
        const mousePos = getMousePos(canvas, evt);
        images.forEach((image, index) => {
            if (isMouseInImage(mousePos, image)) {
                image.isDragging = true;
                dragIndex = index;
            }
        });
    });

    canvas.addEventListener('mousemove', (evt) => {
        if (dragIndex !== -1) {
            const mousePos = getMousePos(canvas, evt);
            const image = images[dragIndex];
            image.x = mousePos.x - image.width / 2;
            image.y = mousePos.y - image.height / 2;
            drawImages();
        } else {
            const mousePos = getMousePos(canvas, evt);
            let hoveredImage = null;
            images.forEach(image => {
                if (isMouseInImage(mousePos, image)) {
                    hoveredImage = image;
                }
            });
            if (hoveredImage) {
                canvas.title = hoveredImage.name;
            } else {
                canvas.title = '';
            }
        }
    });

    canvas.addEventListener('mouseup', () => {
        if (dragIndex !== -1) {
            images[dragIndex].isDragging = false;
            dragIndex = -1;
        }
    });

    canvas.addEventListener('mouseout', () => {
        if (dragIndex !== -1) {
            images[dragIndex].isDragging = false;
            dragIndex = -1;
        }
    });

    function showSolution() {
        const solutionImageContainer = document.getElementById('solutionImageContainer');
        const img = document.createElement('img');
        img.src = './images/soln1.png';
        img.alt = 'Solution';
        img.style.marginTop = '20px';
        solutionImageContainer.innerHTML = '';
        solutionImageContainer.appendChild(img);
    }

    loadImages(drawImages);
</script>

<style>
    body {
        background-color: #f0f0f0;
        font-family: Arial, sans-serif;
    }

    canvas {
        display: block;
        margin: 20px auto;
        background: url('./images/arc1.png') no-repeat center center;
        background-size: cover;
        border: 5px solid #333;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
    }

    .draggable-icon {
        margin: 10px 0;
        cursor: grab;
        /* border: 2px solid #333; */ /* Remove this line to remove the black border */
        border-radius: 10px;
        box-shadow: 0 0 5px rgba(0, 0, 0, 0.3);
        transition: transform 0.2s;
        background-color: rgba(255, 255, 255, 0.8); /* Light background to differentiate from canvas */
    }

    .draggable-icon:active {
        cursor: grabbing;
        transform: scale(1.1);
    }

    #iconContainer {
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: 10px;
        background-color: #fff;
        border: 2px solid #333;
        border-radius: 10px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
    }

    #showSolutionButton {
        display: block;
        margin: 20px auto;
        padding: 10px 20px;
        font-size: 16px;
        background-color: #007bff;
        color: white;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        transition: background-color 0.3s;
    }

    #showSolutionButton:hover {
        background-color: #0056b3;
    }

    #solutionImageContainer {
        text-align: center;
    }
</style>
{% endraw %}
