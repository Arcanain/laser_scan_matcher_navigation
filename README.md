# laser_scan_matcher_navigation
laser_scan_matcher_navigation

# テスト方法

```bash
source devel/setup.bash
roslaunch laser_scan_matcher_navigation navigation.launch
```
# システム構成

- **laser scan mather** : odom->base_link間のpose2D(geometry_msgs/Pose2D)やgeometry_msgs/PoseWithCovarianceStampedを算出
- **amcl** : map->odom間の自己位置推定の修正
- **movb base** : map->odom, odom->base_linkの情報を基にnavigationを行う

**move base内で計算される/cmd_velを/cmd_vel_movebaseにremapしている事に注意**

