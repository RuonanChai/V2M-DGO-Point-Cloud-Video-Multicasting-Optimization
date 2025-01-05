# V2M-DGO-Point-Cloud-Video-Multicasting-Optimization
# **Point Cloud Optimization Using PPO and V-PCC**

## **Project Overview**
This project optimizes the transmission of point cloud data in a multi-user environment. It leverages **Proximal Policy Optimization (PPO)** and **V-PCC (Video-based Point Cloud Compression)** technologies to dynamically optimize user grouping, layered transmission, and video quality allocation. The aim is to balance bandwidth utilization and user experience (QoE - Quality of Experience).

## **Features**
1. **Compression**: Uses V-PCC to compress point cloud data into Base Atlas and Auxiliary Atlas.
2. **Dynamic Optimization**: Applies PPO reinforcement learning to optimize:
   - User grouping based on FoV, device performance, and bandwidth.
   - Base Atlas resolution and Auxiliary Atlas quality allocation.
3. **Baseline Comparison**: Includes three baselines:
   - **Static Transmission**: Fixed quality for all users.
   - **Bandwidth Priority**: Allocates quality based on bandwidth.
   - **No Optimization**: Directly transmits data based on user requirements.
4. **Metrics**: Evaluates strategies based on:
   - **QoE (Quality of Experience)**.
   - **Bandwidth Utilization**.
   - **Transmission Delay**.
   - **System Throughput**.

---

## **Project Structure**
PointCloudOptimization/
├── README.md                       # Project description and setup instructions
├── data/
│   ├── input_point_clouds/         # Original point cloud data
│   └── compressed_atlases/         # Compressed Base and Auxiliary Atlas files
├── env/
│   └── point_cloud_env.py          # Custom multi-user simulation environment
├── models/
│   ├── ppo_agent.py                # PPO reinforcement learning model
│   └── distillation_model.py       # Optional knowledge distillation model
├── compression/
│   └── v_pcc_compression.py        # V-PCC compression logic
├── baseline/
│   ├── static_transmission.py      # Static transmission strategy
│   ├── bandwidth_priority.py       # Bandwidth-priority baseline
│   └── no_optimization.py          # No optimization baseline
├── tests/
│   ├── test_compression.py         # Unit tests for compression
│   ├── test_ppo.py                 # Unit tests for PPO
│   ├── test_baselines.py           # Unit tests for baseline methods
├── main.py                         # Main script to run the experiment
└── requirements.txt                # List of Python dependencies

## **Setup Instructions**

### 1. Clone the repository
```bash
git clone https://github.com/your-repo/point-cloud-optimization.git
cd point-cloud-optimization



