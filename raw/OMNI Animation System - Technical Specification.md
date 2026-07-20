# **OMNI Animation System - Technical Specification**

## **Overview**

The OMNI Animation System is a Unity-to-web export pipeline that enables designers to create animations in Unity and export them to a custom web-based game engine. The system supports multiple animation types and provides a seamless workflow from design to implementation.

## **Architecture**

### **Core Components**

1. **Unity Exporter** - Custom Unity script that converts Unity scenes/animations to JSON format
2. **PIXI.js Engine** - Web-based rendering engine that interprets and plays animations
3. **Animation Controller** - State machine system for managing animation transitions
4. **Format Converters** - Handles conversion between Unity and web formats

## **Animation Types**

### **1. Spine Animations**

- **Source**: Created using Spine animation tool
- **Integration**: Direct import into Unity editor
- **Export**: Converted to custom JSON format
- **Playback**: Rendered via PIXI.js Spine plugin
- **Performance**: High performance, recommended for character animations

### **2. Video Animations**

- **Source**: Standard video files (MP4, WebM)
- **Integration**: Unity video player component
- **Export**: Video files + metadata JSON
- **Playback**: Browser-native video playback with custom sprite integration
- **Implementation**: Each video frame becomes a texture applied to sprites
- **Use Cases**: Cinematic sequences, complex visual effects

### **3. Unity Native Animations (Deprecated)**

- **Source**: Unity's built-in animation system
- **Method**: Bezier curve-based property animations
- **Performance**: Slower than Spine animations
- **Status**: Being phased out in favor of Spine animations
- **Legacy Support**: Still functional but not recommended for new projects

## **Export Pipeline**

### **Unity to JSON Conversion**

The system converts Unity scenes to a custom JSON format containing scene objects, animations, controllers, and assets.

### **Export Process**

1. **Scene Analysis**: Unity script traverses scene components
2. **Component Mapping**: Maps Unity components to custom format
3. **Asset Bundling**: Packages textures, animations, and metadata
4. **JSON Generation**: Creates structured data files
5. **Validation**: Ensures export integrity

### **Custom Elements Support**

The system supports custom elements not available in Unity:

- **Spinner Elements**: Rotating UI components
- **Custom Containers**: Specialized layout containers
- **Interactive Elements**: Button states, hover effects

## **Animation Controller System**

### **State Machine Architecture**

The Animation Controller implements a finite state machine pattern with variables, states, and transitions defined in JSON format.

### **Controller Features**

- **Variable Management**: Boolean, string, and float parameters
- **State Transitions**: Condition-based state changes
- **Parallel Animations**: Multiple animations per state
- **Event System**: Callbacks for state changes and transition completion
- **Designer Control**: Full configuration through Unity interface

## **Implementation Details**

### **Engine Integration**

#### **PIXI.js Components**

- **Sprite Management**: Dynamic texture loading and rendering
- **Animation Playback**: Frame-based and timeline-based animation
- **Video Integration**: Browser video API integration
- **Performance Optimization**: Efficient rendering pipeline

#### **Video Playback System**

Video elements are integrated as textures that update frame-by-frame automatically within the PIXI.js rendering pipeline.

### **API Interface**

All animation types implement a common interface with methods for start, stop, pause, resume, time control, and duration queries.

## **Workflow**

### **Designer Workflow**

1. Create animations in Unity using supported tools (Spine, Video, Unity Animator)
2. Configure Animation Controllers with states and transitions
3. Export scene using custom Unity exporter script
4. Test in Unity editor (limited preview functionality)
5. Deploy to web engine for full testing

### **Developer Integration**

1. Load exported JSON files
2. Initialize animation controller
3. Set controller variables to trigger state changes
4. Subscribe to animation events for game logic integration

## **Performance Considerations**

### **Optimization Strategies**

- **Spine Preferred**: Use Spine animations for best performance
- **Video Limitations**: Video animations have higher memory overhead
- **Controller Complexity**: Keep state machines relatively simple
- **Asset Management**: Efficient texture loading and caching

### **Current Limitations**

- Unity native animations are slower than Spine
- Complex state machines may have performance impact
- Video animations require significant bandwidth

## **Current Status**

### **Active Components**

- Spine animation system (primary)
- Video animation system
- Animation controller with state machine
- Unity exporter pipeline

### **Deprecated/Planned Changes**

- Unity native animations being phased out
- Animation controller improvements in progress
- Better event system implementation planned

## **Dependencies**

### **Unity Side**

- Unity Editor 2020.3+ (recommended)
- Custom export scripts
- Spine Unity Plugin (for Spine animations)

### **Web Side**

- PIXI.js (latest stable)
- PIXI Spine plugin
- Modern web browser with video support
- WebGL support required

## **Future Roadmap**

1. **Performance Improvements**: Optimize animation controller system
2. **Enhanced Events**: Better callback and event management
3. **Tool Improvements**: Enhanced Unity editor integration
4. **Documentation**: Comprehensive usage examples and best practices
5. **Migration Tools**: Assist in moving from Unity native to Spine animations