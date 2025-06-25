Our analysis focuses on the
panda-stack-platforms-texture dataset from the PhysicalAI-Robotics-Manipula
tion-SingleArm collection, which records low-level control signals from a Franka
Panda robot performing stacking tasks. The original dataset, consisting of frame-
level observations, is transformed into a higher-level episode table by aggregating and
engineering new features that capture temporal dynamics, kinematics, and spatial rela-
tionships between the robot and manipulated objects. We consider two main learning
tasks: (i) regression of the episode duration, and (ii) binary classification of whether
a given episode is ”fast” or ”slow” relative to the median duration. Feature construc-
tion includes computation of total displacements, average velocities, normalized joint
changes, distances to boxes, and angular differences derived from quaternion data.
These features are selected to capture physical intuition while maintaining model in-
terpretability. Our exploratory data analysis highlights relationships between the en-
gineered features and target variables. For the regression task, we evaluate linear
models with forward selection, Lasso regularization, and non-linear models like Ran-
dom Forests, validated using out-of-bag error. For classification, we examine feature
separability through distributional plots and apply models including Support Vector
Machines (SVMs) with multiple kernels, Random Forests, and Gradient Boosting, all
assessed via cross-validation. The proposed methodology demonstrates the ability of
statistical learning methods to model robot performance based on task-level summaries
of control data
