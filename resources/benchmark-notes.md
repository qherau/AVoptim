# Pose benchmark leaderboard

Source: avoptim-benchmark/reference/current. The benchmark covers five slots in each of four datasets. Original poses and observation metadata are generated locally from authorized raw datasets; the repository supplies only optimized MOISST++ matrices. MOISST++ refines extrinsic calibration and trajectory. These are recorded reference results, not a claim that a fresh run reproduces every paper score.

Dataset means retain the *_pose.csv values. Overall means use all twenty unrounded records per pose set in per_sequence.csv, with equal sequence weights. There is no scalar composite score.

The ten scores are Nerfacto and Splatfacto PSNR (dB, higher), SSIM (higher), LPIPS (lower), mean reprojection error (px, lower), mean track length (higher), P2M vertex precision (fraction, displayed as percent, higher), and mean triangle-surface distance (m, lower). Precision uses a 0.15 m threshold. Nerfacto uses LiDAR depth supervision; Splatfacto uses SfM and LiDAR initialization. Evaluation holds poses fixed.

Waymo camera images retain their recorded lens distortion and are evaluated with a pinhole approximation using the supplied focal lengths and principal point. Original and refined pose sets use the same image convention.

These metrics measure reconstruction consistency rather than independent absolute pose ground truth.
