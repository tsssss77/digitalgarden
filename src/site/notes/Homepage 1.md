---
{"dg-publish":true,"permalink":"/Homepage 1/","contentClasses":"editor-full"}
---


// 主页配置
const config = {
    author: "天水",
    slogan: "世界上最高贵的艺术是使人快乐的艺术", // 修正后的 slogan
    projectsPath: "03 Projects",
    clippingsPath: "01 Clippings/时间戳笔记",
    draftsPath: "00 Drafts",
    progressField: "笔记进度",
    
    // 置顶笔记配置 - 直接指定路径
    pinnedNotes: [
		"03 Projects/03 dc/02 进行中/【蝙蝠乙女】当蝙蝠侠能看到你对他的好感度-2.md",
		"03 Projects/03 dc/02 进行中/【蝙中心】唉不是你说谁通共？！.md",
		"03 Projects/03 dc/02 进行中/【蝙中心】这个哥谭到底有救没救了？.md",
		"03 Projects/03 dc/02 进行中/【超蝙】联盟与……呃，猫猫联盟.md",
		"03 Projects/03 dc/02 进行中/【超蝙】人间之……？.md",
		"03 Projects/03 dc/02 进行中/【正联】迪克·格雷森的瞭望塔大冒险.md",
		"03 Projects/03 dc/02 进行中/【batfam】什么叫哥谭穿越了？.md"
    ],
    
    // Material Design 主题色
    primaryColor: "#181E34",
    secondaryColor: "#F1CE54",
    backgroundColor: "#F4F2ED",
    cardColor: "#DAD5CF",
    textColor: "#2d0d18",
    textSecondary: "#181E34",
    accentColor: "#CF4626"
};

// Material Design 响应式CSS样式
const css = `
:root {
    --primary: ${config.primaryColor};
    --secondary: ${config.secondaryColor};
    --background: ${config.backgroundColor};
    --card: ${config.cardColor};
    --text: ${config.textColor};
    --text-secondary: ${config.textSecondary};
    --accent: ${config.accentColor};
    --completed: #58B185;
    --in-progress: #F4B04D;
    --not-applicable: #9E9E9E;
    --shadow: 0 4px 6px rgba(0,0,0,0.1), 0 1px 3px rgba(0,0,0,0.08);
    --radius: 8px;
    --transition: all 0.3s ease;
}

.homepage {
	font-family: var(--font-text);
    max-width: 1400px;
    margin: 0 auto;
    padding: 20px;
    background-color: var(--background);
    color: var(--text);
    box-sizing: border-box;
    line-height: 1.6;
}

/* 头部区域 */
.header {
    margin-bottom: 30px;
    padding: 25px;
    background: var(--primary);
    border-radius: var(--radius);
    box-shadow: var(--shadow);
    text-align: center;
    transition: var(--transition);
}

.author-info h1 {
	font-family: var(--font-header);
	margin: 0;
	font-size: 2.5rem;
	font-weight: 700;
	letter-spacing: 0.5px;
	color:var(--secondary)
}

.author-info .slogan {
    font-size: 1.2rem;
    opacity: 0.9;
    margin-top: 10px;
    color:var(--secondary);
}


/* 主内容区 */
.main-content {
    display: grid;
    grid-template-columns: 2fr;
    gap: 25px;
    margin-bottom: 30px;
}

@media (min-width: 768px) {
    .main-content {
        grid-template-columns: 1fr 1fr;
    }
}

@media (min-width: 1200px) {
    .main-content {
        grid-template-columns: 3fr 2fr;
    }
}

/* 卡片样式 */
.card {
    background: var(--card);
    border-radius: var(--radius);
    padding: 25px;
    box-shadow: var(--shadow);
    transition: var(--transition);
}

.card:hover {
    box-shadow: 0 10px 15px rgba(0,0,0,0.1), 0 4px 6px rgba(0,0,0,0.05);
}

.card-header {
	font-family: var(--font-interface);
	display: flex;
	justify-content: space-between;
	align-items: center;
	margin-bottom: 20px;
	padding-bottom: 15px;
	border-bottom: 1px solid rgba(0,0,0,0.1);
}

.card-header h2 {
    margin: 0;
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--primary);
}

/* 统计区 */
.stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 20px;
    margin-top: 15px;
}

.stat-card {
    background: var(--background);
    border-radius: var(--radius);
    padding: 20px;
    text-align: center;
    box-shadow: var(--shadow);
    transition: var(--transition);
}

.stat-card:hover {
    transform: translateY(-5px);
}

.stat-card h3 {
    margin: 0 0 15px 0;
    font-size: 1.1rem;
    font-weight: 600;
    color: var(--text);
}

.stat-card .count {
    font-size: 2.5rem;
    font-weight: bold;
    color: var(--primary);
    margin-bottom: 15px;
}

/* 新进度条样式 - 三部分 */
.stat-progress-container {
    height: 8px;
    background: #e0e0e0;
    border-radius: 4px;
    overflow: hidden;
    margin-bottom: 8px;
    display: flex;
}

.stat-progress-completed {
    height: 100%;
    background: var(--completed);
}

.stat-progress-in-progress {
    height: 100%;
    background: var(--in-progress);
}

.stat-progress-not-applicable {
    height: 100%;
    background: var(--not-applicable);
}

.stat-info {
    display: flex;
    justify-content: space-between;
    font-size: 0.9rem;
    color: var(--text-secondary);
}

.stat-info .completed {
    color: var(--completed);
}

.stat-info .in-progress {
    color: var(--in-progress);
}

.stat-info .not-applicable {
    color: var(--not-applicable);
}

/* 随机漫游区 */
.random-walk {
    display: flex;
    flex-direction: column;
    height: 100%;
}

.refresh-btn {
    background: var(--primary);
    border: none;
    color:var(--background);
    border-radius: 50px;
    padding: 8px 16px;
    cursor: pointer;
    font-size: 0.9rem;
    transition: var(--transition);
    display: flex;
    align-items: center;
    gap: 5px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.refresh-btn:hover {
    background: var(--accent);
    color:white;
    box-shadow: 0 4px 8px rgba(0,0,0,0.15);
}

.tags-container {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-bottom: 20px;
}

.tag {
    background: var(--background);
    color: var(--primary);
    border-radius: 16px;
    padding: 6px 12px;
    font-size: 0.85rem;
    white-space: nowrap;
    transition: var(--transition);
}

.tag:hover {
    background: var(--accent);
    color:white;
    transform: translateY(-2px);
}

.content-preview {
	font-family: var(--font-text);
    flex-grow: 1;
    overflow: auto;
    white-space: pre-wrap;
    line-height: 1.7;
    padding: 15px;
    background: var(--background);
    border-radius: var(--radius);
    margin-bottom: 15px;
    border-left: 3px solid var(--primary);
}

.content-preview blockquote {
    border-left: 3px solid var(--primary);
    padding-left: 15px;
    margin: 15px 0;
    color: var(--text-secondary);
}

.note-link {
    display: inline-flex;
    align-items: center;
    gap: 5px;
    color: var(--primary);
    text-decoration: none;
    font-weight: 500;
    transition: var(--transition);
    padding: 8px 15px;
    background: var(--background);
    border-radius: 50px;
}

.note-link:hover {
    border-radius: 50px;
    background:var(--accent);
    color:white;
    transform: translateY(-2px);
}

/* 文件列表区 */
.files-container {
    display: grid;
    grid-template-columns: 1fr;
    gap: 0;
    margin-bottom: 0;
}

@media (min-width: 768px) {
    .files-container {
        grid-template-columns: 1fr 1fr;
    }
}

.file-list {
    list-style: none;
    padding: 0;
    margin: 0;
}

.file-item {
    display: flex;
    align-items: center;
    padding: 0px;
    border-radius: var(--radius);
    margin-bottom: 10px;
    transition: var(--transition);
    background: var(--card);
    box-shadow: var(--shadow);
}

.file-item:hover {
    transform: translateY(-3px);
    box-shadow: 0 6px 12px rgba(0,0,0,0.1);
}

.file-icon {
    margin-right: 15px;
    color: var(--accent);
    font-size: 1.2rem;
    min-width: 24px;
    text-align: center;
}

.file-link {
    flex-grow: 1;
    text-decoration: none;
    color: var(--text);
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: pre-wrap;
    font-weight: 500;
    transition: var(--transition);
}

.file-link:hover {
    color: var(--accent);
}

.file-time {
    font-size: 0.7rem;
    color: var(--text-secondary);
    white-space: nowrap;
    margin-right: 15px; 
}

.pin-icon {
    color: var(--accent);
    margin-left: 10px;
}

/* 移动端优化 */
@media (max-width: 767px) {
    .homepage {
        padding: 15px;
    }
    
    .header {
        padding: 20px;
    }
    
    .author-info h1 {
        font-size: 2rem;
    }
    
    .author-info .slogan {
        font-size: 1rem;
    }
    
    .card {
        padding: 20px;
    }
    
    .stats-grid {
        grid-template-columns: 1fr;
    }
    
    .file-item {
        flex-wrap: wrap;
        padding: 12px;
    }
    
    .file-link {
        white-space: normal;
        word-break: break-word;
        flex-basis: 100%;
        margin-top: 10px;
        overflow: hidden;
        text-overflow: ellipsis;
        display: -webkit-box;
        -webkit-line-clamp: 2;
        -webkit-box-orient: vertical;
    }
    
    .file-time {
        margin-left: 0;
        margin-top: 5px;
        flex-basis: 100%;
    }
    
    .files-container {
        gap: 15px;
    }
}

/* 文件列表卡片优化 */
.file-list-card {
    display:flex;
    flex-direction:column;
    padding: 25px;
    margin: 15px;
    
}

.file-list-card .card-header {
    margin: 0;
    padding: 0;
    background: var(--card);
}

.file-list-card .file-item {
    margin: 10px 0px;
    padding-left: 10px;
    background:var(--background);
}
`;

// 添加CSS样式
const style = document.createElement('style');
style.textContent = css;
document.head.appendChild(style);

// 添加Material Design图标
const materialIcons = document.createElement('link');
materialIcons.href = "https://fonts.googleapis.com/icon?family=Material+Icons";
materialIcons.rel = "stylesheet";
document.head.appendChild(materialIcons);

// 添加字体
const fonts = document.createElement('link');
fonts.href = "https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&family=Merriweather:wght@300;400;700&display=swap";
fonts.rel = "stylesheet";
document.head.appendChild(fonts);

// 创建主页容器
const container = dv.el('div', '', { cls: 'homepage' });
F
// 头部区域
const header = container.createEl('div', { cls: 'header' });
const authorInfo = header.createEl('div', { cls: 'author-info' });
authorInfo.createEl('h1', { text: config.author });
authorInfo.createEl('p', { 
    text: config.slogan, // 使用修正后的 slogan
    cls: 'slogan' 
});

// 主内容区
const mainContent = container.createEl('div', { cls: 'main-content' });

// 作品统计区
const statsContainer = mainContent.createEl('div', { cls: 'card' });
const statsHeader = statsContainer.createEl('div', { cls: 'card-header' });
statsHeader.createEl('h2', { text: '作品统计' });

// 获取项目文件夹统计
const projects = dv.pages(`"${config.projectsPath}"`)
    .where(p => !p.file.path.includes(config.draftsPath))
    .groupBy(p => p.file.folder.split('/')[1])
    .sort(g => g.key);

const statsGrid = statsContainer.createEl('div', { cls: 'stats-grid' });

for (const group of projects) {
    if (!group.key) continue;
    
    const statCard = statsGrid.createEl('div', { cls: 'stat-card' });
    statCard.createEl('h3', { text: group.key.replace(/^\d+\s/, '') });
    
    const total = group.rows.length;
    
    const completed = group.rows.where(p => {
        const progress = p[config.progressField];
        return progress && progress.includes("已完成");
    }).length;
    
    const inProgress = group.rows.where(p => {
        const progress = p[config.progressField];
        return progress && progress.includes("进行中");
    }).length;
    
    const notApplicable = total - completed - inProgress;
    
    statCard.createEl('div', { 
        text: total, 
        cls: 'count' 
    });
    
    // 新进度条 - 三部分
    const progressContainer = statCard.createEl('div', { cls: 'stat-progress-container' });
    
    if (total > 0) {
        const completedWidth = (completed / total) * 100;
        const inProgressWidth = (inProgress / total) * 100;
        const notApplicableWidth = (notApplicable / total) * 100;
        
        if (completedWidth > 0) {
            const progressCompleted = progressContainer.createEl('div', { 
                cls: 'stat-progress-completed',
                attr: { style: `width: ${completedWidth}%` }
            });
        }
        
        if (inProgressWidth > 0) {
            const progressInProgress = progressContainer.createEl('div', { 
                cls: 'stat-progress-in-progress',
                attr: { style: `width: ${inProgressWidth}%` }
            });
        }
        
        if (notApplicableWidth > 0) {
            const progressNotApplicable = progressContainer.createEl('div', { 
                cls: 'stat-progress-not-applicable',
                attr: { style: `width: ${notApplicableWidth}%` }
            });
        }
    }
    
    const statInfo = statCard.createEl('div', { cls: 'stat-info' });
    statInfo.createEl('span', { 
        text: `${completed} 已完成`, 
        cls: 'completed' 
    });
    statInfo.createEl('span', { 
        text: `${inProgress} 进行中`, 
        cls: 'in-progress' 
    });
    /*statInfo.createEl('span', { 
        text: `${notApplicable}不涉及`, 
        cls: 'not-applicable' 
    });*/
}

// 随机漫游区
const randomWalk = mainContent.createEl('div', { cls: 'card' });
const randomHeader = randomWalk.createEl('div', { cls: 'card-header' });
randomHeader.createEl('h2', { text: '随机回顾' });
const refreshBtn = randomHeader.createEl('button', { 
    text: '换一条', 
    cls: 'refresh-btn' 
});
refreshBtn.createEl('i', { 
    cls: 'material-icons',
    text: 'refresh'
});

// 获取随机笔记（带日期种子）
async function getRandomClipping(forceRefresh = false) {
    // 获取所有可用摘录
    const clippings = dv.pages(`"${config.clippingsPath}"`)
        .where(p => {
            const dgPublish = p.file.frontmatter?.["dg-publish"];
            return dgPublish !== false && dgPublish !== "false";
        })
        .array();
    
    if (clippings.length === 0) {
        return { content: "暂无可用摘录", tags: [] };
    }
    
    // 检查是否需要刷新
    const today = new Date().toISOString().split('T')[0]; // YYYY-MM-DD
    
    if (!forceRefresh) {
        // 生成基于日期的种子
        const seed = Array.from(today).reduce((acc, char) => 
            acc + char.charCodeAt(0), 0);
        
        // 使用种子选择随机笔记
        const randomIndex = Math.floor(seed % clippings.length);
        const randomNote = clippings[randomIndex];
        const content = await dv.io.load(randomNote.file.path);
        
        // 解析标签和内容
        const tags = [];
        let body = "";
        let inTags = true;
        
        for (const line of content.split('\n')) {
            if (inTags && line.trim().startsWith('#') && line.includes('/')) {
                const lineTags = line.trim().split(/\s+/).filter(tag => 
                    tag.startsWith('#') && tag.includes('/')
                );
                tags.push(...lineTags);
            } else if (line.trim() !== '') {
                inTags = false;
                body += line + '\n';
            }
        }
        
        return {
            title: randomNote.file.name,
            path: randomNote.file.path,
            tags: [...new Set(tags)],
            content: body.trim(),
            date: today
        };
    } else {
        // 手动刷新 - 随机选择一条笔记
        const randomNote = clippings[Math.floor(Math.random() * clippings.length)];
        const content = await dv.io.load(randomNote.file.path);
        
        // 解析标签和内容
        const tags = [];
        let body = "";
        let inTags = true;
        
        for (const line of content.split('\n')) {
            if (inTags && line.trim().startsWith('#') && line.includes('/')) {
                const lineTags = line.trim().split(/\s+/).filter(tag => 
                    tag.startsWith('#') && tag.includes('/')
                );
                tags.push(...lineTags);
            } else if (line.trim() !== '') {
                inTags = false;
                body += line + '\n';
            }
        }
        
        return {
            title: randomNote.file.name,
            path: randomNote.file.path,
            tags: [...new Set(tags)],
            content: body.trim(),
            date: "手动刷新"
        };
    }
}

// 渲染随机笔记
async function renderRandomNote(forceRefresh = false) {
    const clipping = await getRandomClipping(forceRefresh);
    
    // 清除现有内容
    const existingTags = randomWalk.querySelector('.tags-container');
    const existingContent = randomWalk.querySelector('.content-preview');
    const existingLink = randomWalk.querySelector('.note-link-container');
    const existingInfo = randomWalk.querySelector('.refresh-info');
    if (existingTags) existingTags.remove();
    if (existingContent) existingContent.remove();
    if (existingLink) existingLink.remove();
    if (existingInfo) existingInfo.remove();
    
    // 添加刷新信息
    /*const infoContainer = randomWalk.createEl('div', { cls: 'refresh-info' });
    infoContainer.createEl('span', {
        text: `随机笔记 (${clipping.date})`,
        cls: 'info-text'
    });*/
    
    // 渲染标签
    const tagsContainer = randomWalk.createEl('div', { cls: 'tags-container' });
    for (const tag of clipping.tags) {
        tagsContainer.createEl('span', { 
            text: tag, 
            cls: 'tag' 
        });
    }
    
    if (clipping.tags.length === 0) {
        tagsContainer.createEl('span', { 
            text: '未添加分类标签', 
            cls: 'tag' 
        });
    }
    
    // 渲染内容
    const contentPreview = randomWalk.createEl('div', { 
        cls: 'content-preview',
        attr: { style: 'white-space: pre-wrap;' }
    });
    
    if (clipping.content) {
        contentPreview.textContent = clipping.content;
    } else {
        contentPreview.textContent = "该笔记没有可显示的内容";
    }
    
    // 添加笔记链接
    const linkContainer = randomWalk.createEl('div', { cls: 'note-link-container' });
    const noteLink = linkContainer.createEl('a', {
        href: clipping.path,
        cls: 'note-link'
    });
    noteLink.createEl('span', { text: '查看完整笔记' });
    noteLink.createEl('i', { 
        cls: 'material-icons',
        text: 'arrow_forward',
        attr: { style: 'font-size: 1.2rem;' }
    });
    
    // 安全打开文件
    noteLink.addEventListener('click', async (event) => {
        event.preventDefault();
        event.stopPropagation();
        
        const file = app.vault.getAbstractFileByPath(clipping.path);
        if (file) {
            app.workspace.activeLeaf.openFile(file);
        }
    });
}

// 文件列表区
const filesContainer = container.createEl('div', { cls: 'files-container' });

// 最近修改文件
const recentFiles = filesContainer.createEl('div', { cls: 'card file-list-card' }); // 添加 file-list-card 类
const recentHeader = recentFiles.createEl('div', { cls: 'card-header' });
recentHeader.createEl('h2', { text: '最近修改' });

const recentList = recentFiles.createEl('ul', { cls: 'file-list' });
const recentNotes = dv.pages(`"${config.projectsPath}"`)
    .where(p => !p.file.path.includes(config.draftsPath))
    .sort(p => p.file.mtime, 'desc')
    .limit(5);

for (const note of recentNotes) {
    const fileItem = recentList.createEl('li', { cls: 'file-item' });
    fileItem.createEl('i', { 
        cls: 'material-icons file-icon',
        text: 'description'
    });
    
    const fileLink = fileItem.createEl('a', { 
        text: note.file.name, 
        href: note.file.path,
        cls: 'file-link'
    });
    
    fileLink.addEventListener('click', async (event) => {
        event.preventDefault();
        event.stopPropagation();
        
        const file = app.vault.getAbstractFileByPath(note.file.path);
        if (file) {
            app.workspace.activeLeaf.openFile(file);
        }
    });
    
    fileItem.createEl('span', { 
        text: formatDate(note.file.mtime), 
        cls: 'file-time' 
    });
}

// 手动置顶文件 - 使用配置的路径
const pinnedFiles = filesContainer.createEl('div', { cls: 'card file-list-card' }); // 添加 file-list-card 类
const pinnedHeader = pinnedFiles.createEl('div', { cls: 'card-header' });
pinnedHeader.createEl('h2', { text: '手动置顶' });

const pinnedList = pinnedFiles.createEl('ul', { cls: 'file-list' });

if (config.pinnedNotes.length === 0) {
    const fileItem = pinnedList.createEl('li', { cls: 'file-item' });
    fileItem.textContent = '暂无置顶笔记，请在配置中添加';
} else {
    for (const notePath of config.pinnedNotes) {
        // 使用更可靠的方式获取文件
        const file = app.vault.getFiles().find(f => f.path === notePath);
        
        if (file) {
            const fileItem = pinnedList.createEl('li', { cls: 'file-item' });
            fileItem.createEl('i', { 
                cls: 'material-icons file-icon pin-icon',
                text: 'push_pin'
            });
            
            const fileLink = fileItem.createEl('a', { 
                text: file.basename, 
                href: file.path,
                cls: 'file-link'
            });
            
            fileLink.addEventListener('click', async (event) => {
                event.preventDefault();
                event.stopPropagation();
                app.workspace.activeLeaf.openFile(file);
            });
            
            // 获取文件修改时间
            const mtime = new Date(file.stat.mtime);
            fileItem.createEl('span', { 
                text: formatDate(mtime), 
                cls: 'file-time' 
            });
        } else {
            // 如果文件不存在，显示错误信息
            const fileItem = pinnedList.createEl('li', { cls: 'file-item' });
            fileItem.createEl('i', { 
                cls: 'material-icons file-icon',
                text: 'error',
                attr: { style: 'color: #f44336;' }
            });
            fileItem.createEl('span', { 
                text: `文件不存在: ${notePath}`, 
                cls: 'file-link',
                attr: { style: 'color: #f44336;' }
            });
        }
    }
}

// 辅助函数：格式化日期
function formatDate(date) {
    const now = new Date();
    const noteDate = new Date(date);
    const diffDays = Math.floor((now - noteDate) / (1000 * 60 * 60 * 24));
    
    if (diffDays === 0) {
        return '今天';
    } else if (diffDays === 1) {
        return '昨天';
    } else if (diffDays < 7) {
        return `${diffDays}天前`;
    } else {
        return noteDate.toLocaleDateString();
    }
}

// 初始化随机漫游区
(async function initRandomWalk() {
    // 初始渲染（使用日期种子）
    await renderRandomNote();
    
    // 刷新按钮事件
    refreshBtn.addEventListener('click', async (event) => {
        event.stopPropagation();
        event.preventDefault();
        
        // 强制刷新
        await renderRandomNote(true);
        
        // 添加刷新反馈
        /*const feedback = randomWalk.createEl('div', {
            text: '已刷新随机笔记',
            cls: 'refresh-feedback'
        });*/
        
        setTimeout(() => {
            feedback.remove();
        }, 2000);
    });
})();