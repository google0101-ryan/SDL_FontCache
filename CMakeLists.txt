cmake_minimum_required(VERSION 3.10)
project(SDL_FontCache VERSION 0.10.0 LANGUAGES C)

find_package(SDL2 CONFIG REQUIRED)
find_package(SDL2_ttf CONFIG REQUIRED)


add_library(FontCache
    SDL_FontCache.h
    SDL_FontCache.c
)
target_link_libraries(FontCache SDL2::SDL2main)
target_link_libraries(FontCache SDL2::SDL2)
target_link_libraries(FontCache SDL2_ttf::SDL2_ttf)