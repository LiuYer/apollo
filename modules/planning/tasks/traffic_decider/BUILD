load("//tools:cpplint.bzl", "cpplint")

package(default_visibility = ["//visibility:public"])

cc_library(
    name = "traffic_rules",
    srcs = [
        "backside_vehicle.cc",
        "change_lane.cc",
        "clear_zone.cc",
        "crosswalk.cc",
        "destination.cc",
        "object_priority.cc",
        "reference_line_end.cc",
        "rerouting.cc",
        "sidepass_vehicle.cc",
        "signal_light.cc",
        "stop_sign.cc",
    ],
    hdrs = [
        "backside_vehicle.h",
        "change_lane.h",
        "clear_zone.h",
        "crosswalk.h",
        "destination.h",
        "object_priority.h",
        "reference_line_end.h",
        "rerouting.h",
        "sidepass_vehicle.h",
        "signal_light.h",
        "stop_sign.h",
        "traffic_rule.h",
    ],
    deps = [
        "//modules/common/adapters:adapter_manager",
        "//modules/common/util:dropbox",
        "//modules/common/util:factory",
        "//modules/common/util:map_util",
        "//modules/perception/proto:perception_proto",
        "//modules/planning/common:frame",
        "//modules/planning/common:planning_gflags",
        "//modules/planning/common:reference_line_info",
        "//modules/planning/proto:planning_config_proto",
        "//modules/planning/proto:planning_proto",
    ],
)

cc_library(
    name = "traffic_decider",
    srcs = [
        "traffic_decider.cc",
    ],
    hdrs = [
        "traffic_decider.h",
    ],
    deps = [
        ":traffic_rules",
        "//modules/common/status",
        "//modules/common/vehicle_state:vehicle_state_provider",
        "//modules/planning/common:frame",
        "//modules/planning/common:reference_line_info",
        "//modules/planning/tasks:task",
    ],
)

cpplint()
