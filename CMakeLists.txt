cmake_minimum_required(VERSION 3.10)
project(VulkanApp)

set(CMAKE_CXX_STANDARD 17)

find_package(Vulkan REQUIRED)
find_package(glfw3 3.3 REQUIRED)

add_executable(VulkanApp main.cpp)

target_include_directories(VulkanApp PRIVATE ${Vulkan_INCLUDE_DIR} ${GLFW_INCLUDE_DIRS})
target_link_libraries(VulkanApp PRIVATE ${Vulkan_LIBRARIES} glfw)
