# CUDAClaw — CUDA-Native Agent Framework

PTX rooms, constraint tightening, edge synergy for Jetson.

## Rooms
- **ptx-room/**: CUDA PTX assembly + constraint tightening + git-native
  - 4 constraint gates (syntax → register pressure → occupancy → performance)
  - Sequential tightening with tolerance ladder
  - Agent learning profiles with snap accuracy
  - CI with nvidia/cuda container

## Edge Synergy
Jetson Orin Nano (sm_87) native PTX optimization. Agents learn optimal assembly through constraint feedback — the journeyman pattern.

## Quick Start
```bash
# Fork any room
gh repo fork Lucineer/ptx-room
cd ptx-room
# Add your agent
cp world/agents/template.yaml world/agents/your-name.yaml
# Write PTX command
echo 'agent: your-name' > world/commands/your-name-001.yaml
echo 'ptx: ".version 8.6..."' >> world/commands/your-name-001.yaml
# Push — CI processes turn
git add . && git commit -m "first turn" && git push
```

## The Journeyman
Agents start naive, learn through constraint gates. After 100+ turns, they develop "instinctual precision" — the right PTX for the right hardware.

## PLATO Integration
This is a PLATO room — git-native, CI-as-server, agent-as-center-point. Part of the side-tie bridge between JC1 (Jetson) and Oracle1 (cloud).
