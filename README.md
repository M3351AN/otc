# 🔮 OTC Loader [2.1]  / ![Windows](https://github.com/0x000cb/otc/workflows/Windows/badge.svg?branch=master&event=push) /

----------------------------------------------------

 Hello. This loader loads and initializes onetap crack in the CS:GO.

-----------------------------------------------------

# 📎 FAQ

  * 🔶 **How clone this repository ?**
     * ``` git clone https://github.com/0x000cb/otc.git  && cd otc && git submodule update --init --recursive ```
     
   -----------
  
  * ⭕ **PROBLEMS**

     * Everything worked out, but when i inject onetap, menu it does not render.
        * Enable multi-threaded rendering (in csgo) and then inject OTC. 
        * If everything still does not work before, add a flag to disable d3x9 in the CS: GO startup parameters.

     * I inject otc into the game but it freezes and doesn't respond. ```(And also the consumption of processor resources is reduced to 2-3%)```
       * Try to open the console before the injection. The problem most often lies in the injector.
       > p.s This issue is observed on Windows prior to version 10.

     * When you already fix what I need so much ??? I can’t play without it !!! (There should be a function name without which you cannot play)
        * First of all, we try to solve the most important problems. 
        * In TODO, you can see the order in which work is currently being performed.

     * The game crashes when I try inject OTC.
       * Make sure you have the latest version of OTC. 
       * If you inject an addon then try without it, very often it causes crashes.
       * Injector problems are also possible. (Try use process hacker)
       > p.s Injection through crashhandler spoofing can also cause crashes.

  -----------

  * 📑 **DEVELOPMENT**

     * I found this repository, but can't find OneTap source code.
       * Right. This is just a loader, that initializes & patch & invoke a binary file in game memory. 
       * You can watch/patch file [**here**](https://github.com/0x000cb/otc/blob/master/OTC/cpp/segment/Segment.cpp).

     * How update signatures, index's, and netvars?

       * Signatures.
         * Vector: [m_signatures](https://github.com/0x000cb/otc/blob/master/OTC/headers/frameworks/SegmentFramework.h#L112) 
         * FAQ: [#12](https://github.com/0x000cb/otc/issues/12) 

       * Index's
         * Function: [CustomVirtualCaller](https://github.com/0x000cb/otc/blob/master/OTC/cpp/frameworks/SegmentFramework.cpp#L79)
         * You just need to go to unknowncheats, find out which index the rest have shifted from, and how much, and set this as a rule in the method.
         * Example:
             * Shifting base: 179.
             * Shifting count: 2.
             * ```cpp
                if (index >= 179) {
                   index += 2;
                } 

        * Netvars:
          * Vector: [m_netvars](https://github.com/0x000cb/otc/blob/master/OTC/headers/frameworks/SegmentFramework.h#L106)
          * Just change the second argument in the structure to the current value. It's all. (Recommend use: hazedumper)

      * How to change the name in the watermark to your own?
         * We need to clone the project with git. To do this, see the first paragraph of the FAQ.
         * Then we need go to: dev -> dllmain.cpp, and edit this lines: https://github.com/0x000cb/otc/blob/master/OTC/dllmain.cpp#L103.
         * Compile and inject. Gl & Hf.
-----------------------------------------------------

 # 💊 Issues
 
  - [ ] Binds. (Key-non-trigger)
  - [ ] Attachments. (Chams) ([#75](https://github.com/0x000cb/otc/issues/75))
  - [ ] Animations. (Chams) ([#8](https://github.com/0x000cb/otc/issues/8))
  
-----------------------------------------------------

 # 🔧 In plans | Development
 
  - Add GUI. (+ Runtime staff support)
  - Rewrite with OOP + Only NativeAPI.

-----------------------------------------------------

# 📦 Build

   * [**DLL**](https://github.com/0x000cb/otc/releases/download/master/OTC.dll) 
     
------------------------------------------------------

# 📜 Configs
  * [Big collection #1 (827 configs)](https://yadi.sk/d/KZNcRdMSheLTfw)
  * [Big collection #2 (1150 configs)](https://anonfile.com/z8x6s9tcod/Big_Collection_2_rar)

------------------------------------------------------

# 💠 Credits

  * [Takanashi-Yae1337](https://github.com/M3351AN) - Kawaii me! (JPHVH's "Hikari")
  * [0x000cb](https://github.com/0x000cb) - God! (Project creator & reverse staff)
  * [HoShiMin](https://github.com/HoShiMin) - Legacy & Native help. (Easy hook with HookLib :d)
  * [playday3008](https://github.com/playday3008) - Help with github & frequent pull requests.

  ------

  *  ♥ Community - Thank you for helping to develop and improve the project.
  *  ♥ toast, wnz, d3x - The creators of OT crack.
  ------

  *  🛡️ flyingllama - Creator of skeet tier security.
