<h1>One Crew</h1>
<h2>A Pirate Experience Game in Unreal Engine 5</h2>

![image](https://github-production-user-asset-6210df.s3.amazonaws.com/65015373/443797907-4e5ab56f-2e93-4ae3-97bf-c001bcb9595e.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250514%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250514T183452Z&X-Amz-Expires=300&X-Amz-Signature=3900cd2568054a1568a76a8a3a3ffd180845adf4223be3b9b56d0a31dda004c6&X-Amz-SignedHeaders=host)

<br>
<hr>
<h2>About it</h2>
<p>One Crew is an immersive 3D pirate-themed action game prototype developed in Unreal Engine 5 that simulates the pirate experience in naval battles and island exploration. The project represents a significant foray into developing intelligent NPC systems that behave in genuinely realistic ways, perceiving their environment, making contextual decisions, and reacting dynamically to player actions.</p>

<p>The game combines several artificial intelligence concepts such as state-based behaviors, environmental perception, and the simulation of simple physical interactions, all while maintaining a visually appealing low-poly art style. This approach not only reduces visual complexity, making important elements easier to identify but also stimulates the player's imagination by letting them fill in the visual gaps with their own expectations and interpretations.</p>

<h3>Key Features:</h3>
<ul>
    <li><strong>Advanced AI Behavior System</strong> - Non-player characters feature a sophisticated hierarchical decision-making process that mimics natural cognitive patterns</li>
    <li><strong>Dynamic Animation System</strong> - Custom-designed animation blending creates realistic reactions to impacts and player interactions</li>
    <li><strong>Atmospheric Low-Poly Visual Style</strong> - A deliberate artistic choice that creates an engaging yet clear visual environment</li>
    <li><strong>Interactive Floating Boat</strong> - Featuring a realistic buoyancy physics system using float points technology</li>
    <li><strong>Progressive Save Point System</strong> - Strategically placed checkpoints that encourage exploration without excessive penalties</li>
    <li><strong>Epic Boss Encounters</strong> - Culminating in a battle with a formidable shark-pirate enemy that tests player skills</li>
    <li><strong>Environmental Immersion</strong> - Giant animated tentacles surrounding the island create a mysterious atmosphere</li>
    <li><strong>Thematic Audio Experience</strong> - Pirate-themed ambient soundtrack enhances the gameplay experience</li>
</ul>

<br>
<hr>
<h2>How to use it</h2>

<h3>Prerequisites</h3>
<ul>
    <li>Unreal Engine 5 installed</li>
    <li>Capable GPU for physics simulation and rendering</li>
    <li>Windows operating system (preferred for optimal performance)</li>
    <li>Minimum 16GB RAM recommended</li>
</ul>

<h3>Installation</h3>
<ol>
    <li>Clone the repository:
        <pre><code>git clone https://github.com/yourusername/one-crew.git
cd one-crew</code></pre>
    </li>
    <li>Open the project in Unreal Engine 5</li>
    <li>Build and run the game through the Unreal Editor</li>
</ol>

<h3>Controls</h3>
<ul>
    <li><strong>WASD</strong>: Character movement</li>
    <li><strong>Mouse</strong>: Look/camera control</li>
    <li><strong>Left Mouse Button</strong>: Attack</li>
    <li><strong>Space</strong>: Jump</li>
</ul>

<h3>Gameplay Mechanics</h3>
<ol>
    <li><strong>Combat System</strong>: Engage in melee combat with skeleton pirates. The hitbox-based attack detection system registers hits when your attack animation intersects with enemy collision boxes.</li>
    <li><strong>Health Management</strong>: Monitor your health bar displayed on the UI. Different enemies inflict varying damage amounts - regular skeletons cause minor damage while the shark-pirate boss inflicts significant damage.</li>
    <li><strong>Save Point Activation</strong>: Interact with save points across the island to create respawn locations. These are strategically placed after enemy encounters.</li>
    <li><strong>Island Exploration</strong>: Navigate the mysterious island environment surrounded by giant tentacles, discovering new areas and enemy encampments.</li>
    <li><strong>Boat Interaction</strong>: Experience realistic boat physics as you explore the floating vessel. The boat responds dynamically to weight distribution and water movement.</li>
</ol>

<br>
<hr>
<h2>How it works</h2>

<h3>AI Architecture</h3>
<p>The game's AI system is built as a complex ecosystem that models believable, adaptive behaviors that create a convincing pirate experience:</p>

<h4>Behavior Tree System</h4>
<p>Rather than implementing a simple finite state machine, the AI uses a behavior tree that naturally prioritizes actions—similar to how a living being prioritizes its needs and responses. This creates a psychological model for enemies, not just a mechanical one.</p>

<p>For example, a patrolling pirate will abandon its routine when it spots the player, immediately prioritizing combat engagement. This adaptive prioritization creates a more realistic and dynamic enemy behavior.</p>

<h4>Blackboard System - Contextual Memory</h4>
<p>The Blackboard functions as a working memory for the AI, storing:</p>
<ul>
    <li><strong>Cognitive State</strong>: Not just position data, but interpretations of situations (alertness level, threat assessment)</li>
    <li><strong>Threat Memory</strong>: Last known player position is retained even when the player disappears from view</li>
    <li><strong>Behavioral Intentions</strong>: Short-term plans allowing continuity of actions despite changing circumstances</li>
</ul>

<p>This system enables "cognitive persistence" where enemies don't instantly forget player presence just because the player briefly hides.</p>

<h4>Perception Layers</h4>
<p>The enemy detection system is stratified, imitating biological perception complexity:</p>
<ul>
    <li><strong>Passive Vigilance</strong>: Constant low-level environmental scanning that consumes minimal computational resources</li>
    <li><strong>Active Focus</strong>: Increased resources allocated to investigation when anomalies are detected</li>
    <li><strong>Total Engagement</strong>: All cognitive resources redirected to conflict management once a threat is confirmed</li>
</ul>

<h4>State Transition Dynamics</h4>
<p>Transitions between behavioral states are gradual and contextual, not abrupt. When an enemy loses sight of the player, it doesn't immediately return to patrol but enters an "active search" state, checking last known positions and adjacent areas. This behavioral persistence creates authentic tension moments where the player knows they're actively being hunted.</p>

<h3>Animation System</h3>
<p>The animation system uses a state machine to manage transitions between different animations based on game context, creating fluid visual feedback:</p>

<h4>Basic Animation Framework</h4>
<ul>
    <li>Core animations (idle, run, attack) sourced from asset packs</li>
    <li>Animation state machine automatically transitions between animations based on gameplay context</li>
    <li>Animation events synchronized with game logic for timed effects (e.g., damage application)</li>
</ul>

<h4>Custom Blended Animations</h4>
<p>For skeleton enemies, a custom animation called <code>customHitReact</code> was created using skeletal animation techniques. This innovative approach combines two existing animations:</p>
<ul>
    <li>Lower body (from hip down) utilizes the idle animation to maintain foot stability</li>
    <li>Upper body (from hip up) employs the death animation to simulate a violent torso and arm reaction to impact</li>
</ul>

<p>This technique, known as animation blending on bone hierarchy, allows for efficient animation reuse while achieving realistic reaction effects without requiring completely new animations.</p>

<h3>Boat Buoyancy System</h3>
<p>The interactive floating boat implements a sophisticated physics system inspired by real-world buoyancy principles:</p>

<h4>Float Points Technique</h4>
<p>Multiple designated points are attached to the boat's structure. During each frame:</p>
<ul>
    <li>Each point checks if it's below the water surface level</li>
    <li>When submerged, an upward force is applied proportional to the depth of submersion</li>
    <li>Force distribution across multiple points creates natural tilting and balancing effects</li>
</ul>

<p>This approach produces a convincing physics simulation without requiring a complete fluid dynamics system. The boat can naturally rotate and tilt, maintaining visual realism even without advanced graphical post-processing or complex wave systems.</p>

<h3>Environmental Immersion</h3>
<p>The game creates an immersive atmosphere through a combination of visual style, ambient elements, and sound design:</p>
<ul>
    <li><strong>Low-Poly Visual Style</strong>: Characterized by fewer polygons and simple geometric shapes, this artistic choice creates a clear, expressive look without relying on realism</li>
    <li><strong>Giant Tentacles</strong>: Animated tentacles surrounding the island contribute to the mysterious atmosphere, simulating the presence of a hidden creature beneath the island</li>
    <li><strong>Ambient Audio</strong>: Pirate-themed soundtrack provides a coherent sonic background that enhances the island exploration experience</li>
</ul>

<br>
<hr>
<h2>Tech specs</h2>

<h3>Development Environment</h3>
<ul>
    <li><strong>Engine</strong>: Unreal Engine 5</li>
    <li><strong>Programming</strong>: Blueprint Visual Scripting</li>
    <li><strong>Development Platform</strong>: Windows</li>
    <li><strong>Art Style</strong>: Low-poly visuals</li>
    <li><strong>Audio System</strong>: Unreal Engine native audio system</li>
</ul>

<h3>AI System Technical Details</h3>
<ul>
    <li><strong>Decision Architecture</strong>: Behavior Tree system with hierarchical priority organization</li>
    <li><strong>Memory System</strong>: Blackboard for contextual data storage and retrieval</li>
    <li><strong>Perception Implementation</strong>: 
        <ul>
            <li>Layered detection with passive, active, and engagement states</li>
            <li>Line-of-sight calculations using raycasting</li>
            <li>Stimuli detection through collision volumes</li>
        </ul>
    </li>
    <li><strong>Processing Optimization</strong>: "Intelligence on demand" approach to maintain performance
        <ul>
            <li>Costly calculations (visibility checks, complex path planning) performed only when necessary</li>
            <li>Simplified processing for distant enemies</li>
            <li>Modular component design allowing selective feature activation</li>
        </ul>
    </li>
</ul>

<h3>Animation Technical Implementation</h3>
<ul>
    <li><strong>Animation Method</strong>: State machine with skeletal animations</li>
    <li><strong>Custom Techniques</strong>: Animation blending on bone hierarchy</li>
    <li><strong>Animation Events</strong>: Synchronized with gameplay logic for timing effects</li>
    <li><strong>Special Features</strong>: Custom hit reactions created by blending existing animations</li>
</ul>

<h3>Physics Implementations</h3>
<ul>
    <li><strong>Boat Physics</strong>: Float point-based buoyancy simulation
        <ul>
            <li>Multiple buoyancy points with depth-proportional force application</li>
            <li>Dynamic response to water surface without full fluid simulation</li>
        </ul>
    </li>
    <li><strong>Combat Physics</strong>: 
        <ul>
            <li>Hitbox-based collision detection for attacks</li>
            <li>Animation-driven impact reactions</li>
            <li>Physics-based knockback effects</li>
        </ul>
    </li>
</ul>

<h3>Performance Considerations and Limitations</h3>
<ul>
    <li>High hardware requirements, especially GPU resources for rendering and physics calculation</li>
    <li>Limited scalability due to the computational demands of physics simulation and advanced AI processing</li>
    <li>No specific performance optimizations implemented in the current prototype stage</li>
    <li>Requires POSIX-compliant operating system for optimal performance</li>
</ul>

<h3>Future Development Directions</h3>
<ul>
    <li><strong>Enhanced Naval Mechanics</strong>:
        <ul>
            <li>Fully navigable boat system</li>
            <li>Cannon combat implementation</li>
            <li>Destructible enemy ships</li>
        </ul>
    </li>
    <li><strong>Narrative Expansion</strong>:
        <ul>
            <li>Deeper storyline development</li>
            <li>Character progression systems</li>
            <li>Quest implementation</li>
        </ul>
    </li>
    <li><strong>Additional Applications</strong>:
        <ul>
            <li>Educational adaptations</li>
            <li>Integration with broader interactive simulation frameworks</li>
            <li>Potential for virtual learning environments</li>
        </ul>
    </li>
</ul>

<h3>Contributors</h3>
<ul>
    <li><a href="https://github.com/theoghn">Ghinea Theodor Traian</li>
    <li><a href="https://github.com/w-i-l">Ocnaru Mihai Octavian</a></li>
    <li><a href="https://github.com/Roby003">Acsente Robert</li>
</ul>
