# Pose benchmark leaderboard

Source: avoptim-benchmark/reference/current. The supplied Original and MOISST++ pose sets cover five slots in each of four datasets. MOISST++ refines extrinsic calibration and trajectory. These are recorded results accompanying the supplied poses.

Dataset means retain the *_pose.csv values. Overall means use all twenty unrounded records per pose set in per_sequence.csv, with equal sequence weights. There is no scalar composite score.

The ten scores are Nerfacto and Splatfacto PSNR (dB, higher), SSIM (higher), LPIPS (lower), mean reprojection error (px, lower), mean track length (higher), P2M vertex precision (fraction, displayed as percent, higher), and mean triangle-surface distance (m, lower). Precision uses a 0.15 m threshold. Nerfacto uses LiDAR depth supervision; Splatfacto uses SfM and LiDAR initialization. Evaluation holds poses fixed.

These metrics measure reconstruction consistency rather than independent absolute pose ground truth.
