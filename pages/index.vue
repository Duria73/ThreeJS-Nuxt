<template>
  <div id="app">
    <div
      id="main"
      class="absolute text-white text-center max-w-2xl px-6"
      style="top: 50%; transform: translate(-50%, -50%); left: 50%;"
    >
      <h1
        id="name"
        class="font-space-mono text-4xl uppercase tracking-wide opacity-0"
        style="transform: translateY(30px)"
      >
        Alexander Duria
      </h1>
      <p
        id="desc"
        class="font-exo text-6xl opacity-0"
        style="transform: translateY(30px)"
      >
        Full Stack Developer
      </p>
      <a
        href="#"
        id="view"
        class="border px-6 py-2 rounded-lg text-sm font-space-mono uppercase mt-8 hover:bg-white hover:text-gray-800 inline-block opacity-0"
        style="transform: translateY(30px)"
      >
        View My Work
      </a>
    </div>
    <!-- Social -->
    <div class="twitter social-icon">
      <a href="#s" target="_blank"></a>
      <i class="fa fa-twitter fa-lg"></i>
    </div>

    <div class="youtube social-icon">
      <a href="#" target="_blank"></a>
      <i class="fa fa-youtube fa-lg"></i>
    </div>
  </div>
</template>

<script>
import gsap from "gsap";
import {
  PlaneGeometry,
  BufferAttribute,
  BufferGeometry,
  Raycaster,
  Scene,
  PerspectiveCamera,
  Points,
  PointLight,
  WebGLRenderer,
  MeshPhongMaterial,
  PlaneBufferGeometry,
  FlatShading,
  DoubleSide,
  Mesh,
  DirectionalLight,
  PointsMaterial,
  Float32BufferAttribute
} from "three";
import OrbitControls from "orbit-controls-es6";
export default {
  mounted() {
    // const loader = new THREE.TextureLoader()
    //     const alpha = loader.load("./images/alpha4.png")
    //     const texture = loader.load("./images/texture.png")
    const dat = require("dat.gui");

    const gui = new dat.GUI();
    const world = {
      plane: {
        width: 19,
        height: 19,
        widthSegments: 50,
        heightSegments: 50
      }
    };
    gui.add(world.plane, "width", 1, 20).onChange(generatePlane);
    gui.add(world.plane, "widthSegments", 1, 100).onChange(generatePlane);
    gui.add(world.plane, "height", 1, 20).onChange(generatePlane);
    gui.add(world.plane, "heightSegments", 1, 100).onChange(generatePlane);

    function generatePlane() {
      planeMesh.geometry.dispose();
      planeMesh.geometry = new PlaneGeometry(
        world.plane.width,
        world.plane.height,
        world.plane.widthSegments,
        world.plane.heightSegments
      );
      const { array } = planeMesh.geometry.attributes.position;

      for (let i = 0; i < array.length; i += 3) {
        const x = array[i];
        const y = array[i + 1];
        const z = array[i + 2];

        array[i + 2] = z + Math.random();
      }
      const colors = [];
      for (let i = 0; i < planeMesh.geometry.attributes.position.count; i++) {
        colors.push(0.31, 0.31, 0.31);
      }

      planeMesh.geometry.setAttribute(
        "color",
        new BufferAttribute(new Float32Array(colors), 3)
      );
    }

    const raycaster = new Raycaster();
    const scene = new Scene();

    const camera = new PerspectiveCamera(
      75,
      window.innerWidth / window.innerHeight,
      0.1,
      1000
    );

    const renderer = new WebGLRenderer();
    renderer.setSize(window.innerWidth, window.innerHeight);
    renderer.setPixelRatio(devicePixelRatio);
    document.body.appendChild(renderer.domElement);
    //Geometry

    const planeGeometry = new PlaneBufferGeometry(800, 800, 250, 250);
    const planeMaterial = new MeshPhongMaterial({
      // color: "gray",
      // side: DoubleSide,
      flatShading: FlatShading,
      vertexColors: true
      // alphaMap: alpha,
      //  displacementMap: texture,
      //   displacementScale: .6,
      // transparent: true,
      // depthTest: false
    });
    const planeMesh = new Mesh(planeGeometry, planeMaterial);

    new OrbitControls(camera, renderer.domElement);
    camera.position.z = 40;
    scene.add(planeMesh);

    //vertex position randomization
    const { array } = planeMesh.geometry.attributes.position;
    const randomValues = [];
    for (let i = 0; i < array.length; i++) {
      if (i % 3 === 0) {
        const x = array[i];
        const y = array[i + 1];
        const z = array[i + 2];

        array[i] = x + (Math.random() - 0.5) * 3;
        array[i + 1] = y + (Math.random() - 0.5) * 3;
        array[i + 2] = z + Math.random() * 3;
      }

      randomValues.push(Math.random() * Math.PI * 2);
    }

    planeMesh.geometry.attributes.position.randomValues = randomValues;
    planeMesh.geometry.attributes.position.originalPosition =
      planeMesh.geometry.attributes.position.array;

    //color attribute RGb
    const colors = [];
    for (let i = 0; i < planeMesh.geometry.attributes.position.count; i++) {
      colors.push(0.31, 0.31, 0.31);
    }

    planeMesh.geometry.setAttribute(
      "color",
      new BufferAttribute(new Float32Array(colors), 3)
    );

    //light front
    const light = new DirectionalLight(0xffffff, 1);
    light.position.set(0, 1, 1);
    scene.add(light);

    //light back
    const backLight = new DirectionalLight(0xffffff, 1);
    light.position.set(0, 0, -1);
    scene.add(backLight);

    //starfield
    const starGeo = new BufferGeometry();
    const starMaterial = new PointsMaterial({ color: 0xffffff });

    const starVerticies = [];
    for (let i = 0; i < 10000; i++) {
      const x = (Math.random() - 0.5) * 2000;
      const y = (Math.random() - 0.5) * 2000;
      const z = (Math.random() - 0.5) * 2000;
      starVerticies.push(x, y, z);
    }

    starGeo.setAttribute(
      "position",
      new Float32BufferAttribute(starVerticies, 3)
    );

    const stars = new Points(starGeo, starMaterial);
    scene.add(stars);

    //point Light
    const pointLight = new PointLight(0x114d7a, 2);
    pointLight.position.x = 2;
    pointLight.position.y = 3;
    pointLight.position.z = 4;
    scene.add(pointLight);

    gui.add(pointLight.position, "x");
    gui.add(pointLight.position, "y");
    gui.add(pointLight.position, "z");

    const col = { color: "#787878" };
    gui.addColor(col, "color").onChange(() => {
      pointLight.color.set(col.color);
    });

    renderer.render(scene, camera);

    const mouse = {
      x: undefined,
      y: undefined
    };

    let frame = 0;

    function animate() {
      requestAnimationFrame(animate);
      frame += 0.1;
      renderer.render(scene, camera);
      // planeMesh.rotation.z += 0.00001

      const {
        array,
        originalPosition,
        randomValues
      } = planeMesh.geometry.attributes.position;

      for (let i = 0; i < array.length; i += 3) {
        //x
        array[i] =
          originalPosition[i] + Math.cos(frame + randomValues[i]) * 0.003;

        //y
        array[i + 1] =
          originalPosition[i + 1] +
          Math.sin(frame + randomValues[i + 1]) * 0.003;

        // // //z
        // array[i + 2] = originalPosition[i] + Math.cos(frame + randomValues[i]) * 0.003
      }

      planeMesh.geometry.attributes.position.needsUpdate = true;

      raycaster.setFromCamera(mouse, camera);
      const intersects = raycaster.intersectObject(planeMesh);
      if (intersects.length > 0) {
        const { color } = intersects[0].object.geometry.attributes;

        // //vertex1
        // color.setX(intersects[0].face.a,0.71)
        // color.setY(intersects[0].face.a,0.71)
        // color.setZ(intersects[0].face.a,0.71)

        // //vertext 2
        // color.setX(intersects[0].face.b,0.71)
        // color.setY(intersects[0].face.b,0.71)
        // color.setZ(intersects[0].face.b,0.71)

        // //vertex 3
        // color.setX(intersects[0].face.c,0.71)
        // color.setY(intersects[0].face.c,0.71)
        // color.setZ(intersects[0].face.c,0.71)

        // intersects[0].object.geometry.attributes.color.needsUpdate = true

        const initialColor = {
          r: 0.31,
          g: 0.31,
          b: 0.31
        };
        const hoverColor = {
          r: 0.71,
          g: 0.71,
          b: 0.71
        };

        gsap.to(hoverColor, {
          r: initialColor.r,
          g: initialColor.g,
          b: initialColor.b,
          duration: 1,
          onUpdate: () => {
            //vertex1
            color.setX(intersects[0].face.a, hoverColor.r);
            color.setY(intersects[0].face.a, hoverColor.g);
            color.setZ(intersects[0].face.a, hoverColor.b);

            //vertext 2
            color.setX(intersects[0].face.b, hoverColor.r);
            color.setY(intersects[0].face.b, hoverColor.g);
            color.setZ(intersects[0].face.b, hoverColor.b);

            //vertex 3
            color.setX(intersects[0].face.c, hoverColor.r);
            color.setY(intersects[0].face.c, hoverColor.g);
            color.setZ(intersects[0].face.c, hoverColor.b);
            color.needsUpdate = true;
          }
        });
      }
      //stars rotation speed
      stars.rotation.x += 0.0005;
    }

    animate();

    addEventListener("mousemove", event => {
      mouse.x = (event.clientX / innerWidth) * 2 - 1;
      mouse.y = -(event.clientY / innerHeight) * 2 + 1;
    });

    gsap.to("#name", {
      opacity: 1,
      duration: 1.5,
      y: 0,
      ease: "expo"
    });
    gsap.to("#desc", {
      opacity: 1,
      duration: 1.5,
      delay: 0.4,
      y: 0,
      ease: "expo"
    });
    gsap.to("#view", {
      opacity: 1,
      duration: 1.5,
      delay: 0.6,
      y: 0,
      ease: "expo"
    });

    document.querySelector("#view").addEventListener("click", event => {
      event.preventDefault();
      gsap.to("#main", {
        opacity: 0
      });
      gsap.to(camera.position, {
        z: 25,
        ease: "power3.inOut",
        duration: 2
      });
      gsap.to(camera.rotation, {
        x: 1.57,
        ease: "power3.inOut",
        duration: 2
      });
      gsap.to(camera.position, {
        y: 1000,
        ease: "power3.in",
        duration: 1,
        delay: 2,
        onComplete: () => {
          window.location = "url";
        }
      });
    });

    addEventListener("resize", () => {
      camera.aspect = innerWidth / innerHeight;
      camera.updateProjectionMatrix();
      renderer.setSize(window.innerWidth, window.innerHeight);
    });
  }
};
</script>

<style></style>
