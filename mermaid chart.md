gitGraph
    commit id: "初始提交"
    commit id: "功能 A"
    
    % 使用 -b 参数创建并切换分支（替代 branch + checkout）
    branch feature-branch
    checkout feature-branch
    commit id: "实验性功能 B"
    commit id: "完善功能 B"
    
    % 切换回 main 进行紧急修复
    checkout main
    commit id: "紧急修复"
    
    % 切换回 feature 分支继续工作
    checkout feature-branch
    commit id: "功能 B 完成"
    
    % 切换回 main 准备合并
    checkout main
    
    % 合并功能分支
    merge feature-branch id: "合并功能B" tag: "v1.0"
    
    % 关键步骤：使用 -u 参数推送主分支
    commit id: "功能 C" tag: "使用 git push -u origin main"