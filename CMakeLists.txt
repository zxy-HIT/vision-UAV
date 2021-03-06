cmake_minimum_required(VERSION 3.1)
project(UAVs_uart_interface)

set(CMAKE_CXX_STANDARD 11)

find_package(OpenCV REQUIRED)
add_executable(UAVs_uart_interface
        ${OpenCV_INCLUDE_DIRS}
        mavlink/ardupilotmega/ardupilotmega.h
        mavlink/ardupilotmega/mavlink.h
        mavlink/ardupilotmega/mavlink_msg_ahrs.h
        mavlink/ardupilotmega/mavlink_msg_ahrs2.h
        mavlink/ardupilotmega/mavlink_msg_airspeed_autocal.h
        mavlink/ardupilotmega/mavlink_msg_ap_adc.h
        mavlink/ardupilotmega/mavlink_msg_battery2.h
        mavlink/ardupilotmega/mavlink_msg_camera_feedback.h
        mavlink/ardupilotmega/mavlink_msg_camera_status.h
        mavlink/ardupilotmega/mavlink_msg_compassmot_status.h
        mavlink/ardupilotmega/mavlink_msg_data16.h
        mavlink/ardupilotmega/mavlink_msg_data32.h
        mavlink/ardupilotmega/mavlink_msg_data64.h
        mavlink/ardupilotmega/mavlink_msg_data96.h
        mavlink/ardupilotmega/mavlink_msg_digicam_configure.h
        mavlink/ardupilotmega/mavlink_msg_digicam_control.h
        mavlink/ardupilotmega/mavlink_msg_fence_fetch_point.h
        mavlink/ardupilotmega/mavlink_msg_fence_point.h
        mavlink/ardupilotmega/mavlink_msg_fence_status.h
        mavlink/ardupilotmega/mavlink_msg_hwstatus.h
        mavlink/ardupilotmega/mavlink_msg_limits_status.h
        mavlink/ardupilotmega/mavlink_msg_meminfo.h
        mavlink/ardupilotmega/mavlink_msg_mount_configure.h
        mavlink/ardupilotmega/mavlink_msg_mount_control.h
        mavlink/ardupilotmega/mavlink_msg_mount_status.h
        mavlink/ardupilotmega/mavlink_msg_radio.h
        mavlink/ardupilotmega/mavlink_msg_rally_fetch_point.h
        mavlink/ardupilotmega/mavlink_msg_rally_point.h
        mavlink/ardupilotmega/mavlink_msg_rangefinder.h
        mavlink/ardupilotmega/mavlink_msg_sensor_offsets.h
        mavlink/ardupilotmega/mavlink_msg_set_mag_offsets.h
        mavlink/ardupilotmega/mavlink_msg_simstate.h
        mavlink/ardupilotmega/mavlink_msg_wind.h
        mavlink/ardupilotmega/testsuite.h
        mavlink/ardupilotmega/version.h
        mavlink/ASLUAV/ASLUAV.h
        mavlink/ASLUAV/mavlink.h
        mavlink/ASLUAV/mavlink_msg_aslctrl_data.h
        mavlink/ASLUAV/mavlink_msg_aslctrl_debug.h
        mavlink/ASLUAV/mavlink_msg_asluav_status.h
        mavlink/ASLUAV/mavlink_msg_sens_mppt.h
        mavlink/ASLUAV/mavlink_msg_sens_power.h
        mavlink/ASLUAV/testsuite.h
        mavlink/ASLUAV/version.h
        mavlink/autoquad/autoquad.h
        mavlink/autoquad/mavlink.h
        mavlink/autoquad/mavlink_msg_aq_telemetry_f.h
        mavlink/autoquad/testsuite.h
        mavlink/autoquad/version.h
        mavlink/common/common.h
        mavlink/common/mavlink.h
        mavlink/common/mavlink_msg_attitude.h
        mavlink/common/mavlink_msg_attitude_quaternion.h
        mavlink/common/mavlink_msg_attitude_quaternion_cov.h
        mavlink/common/mavlink_msg_attitude_target.h
        mavlink/common/mavlink_msg_auth_key.h
        mavlink/common/mavlink_msg_autopilot_version.h
        mavlink/common/mavlink_msg_battery_status.h
        mavlink/common/mavlink_msg_change_operator_control.h
        mavlink/common/mavlink_msg_change_operator_control_ack.h
        mavlink/common/mavlink_msg_command_ack.h
        mavlink/common/mavlink_msg_command_int.h
        mavlink/common/mavlink_msg_command_long.h
        mavlink/common/mavlink_msg_data_stream.h
        mavlink/common/mavlink_msg_data_transmission_handshake.h
        mavlink/common/mavlink_msg_debug.h
        mavlink/common/mavlink_msg_debug_vect.h
        mavlink/common/mavlink_msg_distance_sensor.h
        mavlink/common/mavlink_msg_encapsulated_data.h
        mavlink/common/mavlink_msg_file_transfer_protocol.h
        mavlink/common/mavlink_msg_global_position_int.h
        mavlink/common/mavlink_msg_global_position_int_cov.h
        mavlink/common/mavlink_msg_global_vision_position_estimate.h
        mavlink/common/mavlink_msg_gps2_raw.h
        mavlink/common/mavlink_msg_gps2_rtk.h
        mavlink/common/mavlink_msg_gps_global_origin.h
        mavlink/common/mavlink_msg_gps_inject_data.h
        mavlink/common/mavlink_msg_gps_raw_int.h
        mavlink/common/mavlink_msg_gps_rtk.h
        mavlink/common/mavlink_msg_gps_status.h
        mavlink/common/mavlink_msg_heartbeat.h
        mavlink/common/mavlink_msg_highres_imu.h
        mavlink/common/mavlink_msg_hil_controls.h
        mavlink/common/mavlink_msg_hil_gps.h
        mavlink/common/mavlink_msg_hil_optical_flow.h
        mavlink/common/mavlink_msg_hil_rc_inputs_raw.h
        mavlink/common/mavlink_msg_hil_sensor.h
        mavlink/common/mavlink_msg_hil_state.h
        mavlink/common/mavlink_msg_hil_state_quaternion.h
        mavlink/common/mavlink_msg_local_position_ned.h
        mavlink/common/mavlink_msg_local_position_ned_cov.h
        mavlink/common/mavlink_msg_local_position_ned_system_global_offset.h
        mavlink/common/mavlink_msg_log_data.h
        mavlink/common/mavlink_msg_log_entry.h
        mavlink/common/mavlink_msg_log_erase.h
        mavlink/common/mavlink_msg_log_request_data.h
        mavlink/common/mavlink_msg_log_request_end.h
        mavlink/common/mavlink_msg_log_request_list.h
        mavlink/common/mavlink_msg_manual_control.h
        mavlink/common/mavlink_msg_manual_setpoint.h
        mavlink/common/mavlink_msg_memory_vect.h
        mavlink/common/mavlink_msg_mission_ack.h
        mavlink/common/mavlink_msg_mission_clear_all.h
        mavlink/common/mavlink_msg_mission_count.h
        mavlink/common/mavlink_msg_mission_current.h
        mavlink/common/mavlink_msg_mission_item.h
        mavlink/common/mavlink_msg_mission_item_int.h
        mavlink/common/mavlink_msg_mission_item_reached.h
        mavlink/common/mavlink_msg_mission_request.h
        mavlink/common/mavlink_msg_mission_request_list.h
        mavlink/common/mavlink_msg_mission_request_partial_list.h
        mavlink/common/mavlink_msg_mission_set_current.h
        mavlink/common/mavlink_msg_mission_write_partial_list.h
        mavlink/common/mavlink_msg_named_value_float.h
        mavlink/common/mavlink_msg_named_value_int.h
        mavlink/common/mavlink_msg_nav_controller_output.h
        mavlink/common/mavlink_msg_optical_flow.h
        mavlink/common/mavlink_msg_optical_flow_rad.h
        mavlink/common/mavlink_msg_param_request_list.h
        mavlink/common/mavlink_msg_param_request_read.h
        mavlink/common/mavlink_msg_param_set.h
        mavlink/common/mavlink_msg_param_value.h
        mavlink/common/mavlink_msg_ping.h
        mavlink/common/mavlink_msg_position_target_global_int.h
        mavlink/common/mavlink_msg_position_target_local_ned.h
        mavlink/common/mavlink_msg_power_status.h
        mavlink/common/mavlink_msg_radio_status.h
        mavlink/common/mavlink_msg_raw_imu.h
        mavlink/common/mavlink_msg_raw_pressure.h
        mavlink/common/mavlink_msg_rc_channels.h
        mavlink/common/mavlink_msg_rc_channels_override.h
        mavlink/common/mavlink_msg_rc_channels_raw.h
        mavlink/common/mavlink_msg_rc_channels_scaled.h
        mavlink/common/mavlink_msg_request_data_stream.h
        mavlink/common/mavlink_msg_safety_allowed_area.h
        mavlink/common/mavlink_msg_safety_set_allowed_area.h
        mavlink/common/mavlink_msg_scaled_imu.h
        mavlink/common/mavlink_msg_scaled_imu2.h
        mavlink/common/mavlink_msg_scaled_pressure.h
        mavlink/common/mavlink_msg_serial_control.h
        mavlink/common/mavlink_msg_servo_output_raw.h
        mavlink/common/mavlink_msg_set_attitude_target.h
        mavlink/common/mavlink_msg_set_gps_global_origin.h
        mavlink/common/mavlink_msg_set_mode.h
        mavlink/common/mavlink_msg_set_position_target_global_int.h
        mavlink/common/mavlink_msg_set_position_target_local_ned.h
        mavlink/common/mavlink_msg_sim_state.h
        mavlink/common/mavlink_msg_statustext.h
        mavlink/common/mavlink_msg_sys_status.h
        mavlink/common/mavlink_msg_system_time.h
        mavlink/common/mavlink_msg_terrain_check.h
        mavlink/common/mavlink_msg_terrain_data.h
        mavlink/common/mavlink_msg_terrain_report.h
        mavlink/common/mavlink_msg_terrain_request.h
        mavlink/common/mavlink_msg_timesync.h
        mavlink/common/mavlink_msg_v2_extension.h
        mavlink/common/mavlink_msg_vfr_hud.h
        mavlink/common/mavlink_msg_vicon_position_estimate.h
        mavlink/common/mavlink_msg_vision_position_estimate.h
        mavlink/common/mavlink_msg_vision_speed_estimate.h
        mavlink/common/testsuite.h
        mavlink/common/version.h
        mavlink/matrixpilot/matrixpilot.h
        mavlink/matrixpilot/mavlink.h
        mavlink/matrixpilot/mavlink_msg_airspeeds.h
        mavlink/matrixpilot/mavlink_msg_altitudes.h
        mavlink/matrixpilot/mavlink_msg_flexifunction_buffer_function.h
        mavlink/matrixpilot/mavlink_msg_flexifunction_buffer_function_ack.h
        mavlink/matrixpilot/mavlink_msg_flexifunction_command.h
        mavlink/matrixpilot/mavlink_msg_flexifunction_command_ack.h
        mavlink/matrixpilot/mavlink_msg_flexifunction_directory.h
        mavlink/matrixpilot/mavlink_msg_flexifunction_directory_ack.h
        mavlink/matrixpilot/mavlink_msg_flexifunction_read_req.h
        mavlink/matrixpilot/mavlink_msg_flexifunction_set.h
        mavlink/matrixpilot/mavlink_msg_serial_udb_extra_f13.h
        mavlink/matrixpilot/mavlink_msg_serial_udb_extra_f14.h
        mavlink/matrixpilot/mavlink_msg_serial_udb_extra_f15.h
        mavlink/matrixpilot/mavlink_msg_serial_udb_extra_f16.h
        mavlink/matrixpilot/mavlink_msg_serial_udb_extra_f2_a.h
        mavlink/matrixpilot/mavlink_msg_serial_udb_extra_f2_b.h
        mavlink/matrixpilot/mavlink_msg_serial_udb_extra_f4.h
        mavlink/matrixpilot/mavlink_msg_serial_udb_extra_f5.h
        mavlink/matrixpilot/mavlink_msg_serial_udb_extra_f6.h
        mavlink/matrixpilot/mavlink_msg_serial_udb_extra_f7.h
        mavlink/matrixpilot/mavlink_msg_serial_udb_extra_f8.h
        mavlink/matrixpilot/testsuite.h
        mavlink/matrixpilot/version.h
        mavlink/minimal/mavlink.h
        mavlink/minimal/mavlink_msg_heartbeat.h
        mavlink/minimal/minimal.h
        mavlink/minimal/testsuite.h
        mavlink/minimal/version.h
        mavlink/pixhawk/mavlink.h
        mavlink/pixhawk/mavlink_msg_attitude_control.h
        mavlink/pixhawk/mavlink_msg_brief_feature.h
        mavlink/pixhawk/mavlink_msg_detection_stats.h
        mavlink/pixhawk/mavlink_msg_image_available.h
        mavlink/pixhawk/mavlink_msg_image_trigger_control.h
        mavlink/pixhawk/mavlink_msg_image_triggered.h
        mavlink/pixhawk/mavlink_msg_marker.h
        mavlink/pixhawk/mavlink_msg_onboard_health.h
        mavlink/pixhawk/mavlink_msg_pattern_detected.h
        mavlink/pixhawk/mavlink_msg_point_of_interest.h
        mavlink/pixhawk/mavlink_msg_point_of_interest_connection.h
        mavlink/pixhawk/mavlink_msg_position_control_setpoint.h
        mavlink/pixhawk/mavlink_msg_raw_aux.h
        mavlink/pixhawk/mavlink_msg_set_cam_shutter.h
        mavlink/pixhawk/mavlink_msg_set_position_control_offset.h
        mavlink/pixhawk/mavlink_msg_watchdog_command.h
        mavlink/pixhawk/mavlink_msg_watchdog_heartbeat.h
        mavlink/pixhawk/mavlink_msg_watchdog_process_info.h
        mavlink/pixhawk/mavlink_msg_watchdog_process_status.h
        mavlink/pixhawk/pixhawk.h
        mavlink/pixhawk/testsuite.h
        mavlink/pixhawk/version.h
        mavlink/slugs/mavlink.h
        mavlink/slugs/mavlink_msg_boot.h
        mavlink/slugs/mavlink_msg_control_surface.h
        mavlink/slugs/mavlink_msg_cpu_load.h
        mavlink/slugs/mavlink_msg_ctrl_srfc_pt.h
        mavlink/slugs/mavlink_msg_data_log.h
        mavlink/slugs/mavlink_msg_diagnostic.h
        mavlink/slugs/mavlink_msg_gps_date_time.h
        mavlink/slugs/mavlink_msg_isr_location.h
        mavlink/slugs/mavlink_msg_mid_lvl_cmds.h
        mavlink/slugs/mavlink_msg_novatel_diag.h
        mavlink/slugs/mavlink_msg_ptz_status.h
        mavlink/slugs/mavlink_msg_sensor_bias.h
        mavlink/slugs/mavlink_msg_sensor_diag.h
        mavlink/slugs/mavlink_msg_slugs_camera_order.h
        mavlink/slugs/mavlink_msg_slugs_configuration_camera.h
        mavlink/slugs/mavlink_msg_slugs_mobile_location.h
        mavlink/slugs/mavlink_msg_slugs_navigation.h
        mavlink/slugs/mavlink_msg_status_gps.h
        mavlink/slugs/mavlink_msg_uav_status.h
        mavlink/slugs/mavlink_msg_volt_sensor.h
        mavlink/slugs/slugs.h
        mavlink/slugs/testsuite.h
        mavlink/slugs/version.h
        mavlink/test/mavlink.h
        mavlink/test/mavlink_msg_test_types.h
        mavlink/test/test.h
        mavlink/test/testsuite.h
        mavlink/test/version.h
        mavlink/ualberta/mavlink.h
        mavlink/ualberta/mavlink_msg_nav_filter_bias.h
        mavlink/ualberta/mavlink_msg_radio_calibration.h
        mavlink/ualberta/mavlink_msg_ualberta_sys_status.h
        mavlink/ualberta/testsuite.h
        mavlink/ualberta/ualberta.h
        mavlink/ualberta/version.h
        mavlink/checksum.h
        mavlink/mavlink_conversions.h
        mavlink/mavlink_helpers.h
        mavlink/mavlink_types.h
        mavlink/protocol.h
        autopilot_interface.cpp
        autopilot_interface.h
        mavlink_control.cpp
        mavlink_control.h
        serial_port.cpp
        serial_port.h
        ellipse/EllipseDetectorYaed.cpp
        ellipse/EllipseDetectorYaed.h
        ellipse/common.cpp
        ellipse/common.h
        )
target_link_libraries(UAVs_uart_interface
        pthread
        ${OpenCV_LIBRARIES}
        )