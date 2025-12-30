<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Denver Hellhounds</title>
    <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Roboto', sans-serif;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a1a 100%);
            color: #ffffff;
            min-height: 100vh;
        }

        /* HEADER */
        header {
            background: linear-gradient(90deg, #8B0000, #000000, #8B0000);
            padding: 20px 0;
            text-align: center;
            border-bottom: 4px solid #ff0000;
        }

        .team-name {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 3.5rem;
            letter-spacing: 4px;
            text-shadow: 2px 2px 4px rgba(255, 0, 0, 0.5);
        }

        .team-name span {
            color: #ff0000;
        }

        .slogan {
            font-size: 1rem;
            letter-spacing: 8px;
            color: #888;
            margin-top: 5px;
        }

        /* ROSTER SECTION */
        .roster {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
        }

        .roster h2 {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 30px;
            color: #ff0000;
        }

        /* PLAYER CARDS GRID */
        .players-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 25px;
            justify-items: center;
        }

        /* PLAYER CARD */
        .player-card {
            background: linear-gradient(145deg, #1e1e1e, #2a2a2a);
            border: 2px solid #333;
            border-radius: 15px;
            width: 220px;
            padding: 20px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .player-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, #ff0000, #8B0000);
        }

        .player-card:hover {
            transform: translateY(-10px);
            border-color: #ff0000;
            box-shadow: 0 10px 30px rgba(255, 0, 0, 0.3);
        }

        .player-photo {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            background: #333;
            margin: 0 auto 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.5rem;
            border: 3px solid #ff0000;
        }

        .player-number {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 1.5rem;
            color: #ff0000;
        }

        .player-name {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 1.4rem;
            margin: 10px 0 5px;
        }

        .player-nickname {
            color: #ff0000;
            font-style: italic;
            font-size: 0.9rem;
        }

        .player-position {
            color: #888;
            font-size: 0.85rem;
            margin-top: 5px;
        }

        /* HOVER INFO */
        .player-traits {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease;
            margin-top: 10px;
        }

        .player-card:hover .player-traits {
            max-height: 100px;
        }

        .player-traits p {
            font-size: 0.8rem;
            color: #ccc;
            padding: 10px;
            background: rgba(255, 0, 0, 0.1);
            border-radius: 8px;
        }

        /* MODAL */
        .modal-overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.9);
            z-index: 1000;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .modal-overlay.active {
            display: flex;
        }

        .modal {
            background: linear-gradient(145deg, #1a1a1a, #252525);
            border: 2px solid #ff0000;
            border-radius: 20px;
            max-width: 600px;
            width: 100%;
            max-height: 90vh;
            overflow-y: auto;
            position: relative;
        }

        .modal-header {
            background: linear-gradient(90deg, #8B0000, #000000);
            padding: 20px;
            border-radius: 18px 18px 0 0;
            display: flex;
            align-items: center;
            gap: 20px;
        }

        .modal-photo {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background: #333;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            border: 3px solid #ff0000;
            flex-shrink: 0;
        }

        .modal-title h2 {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 1.8rem;
        }

        .modal-title p {
            color: #ccc;
            font-size: 0.9rem;
        }

        .close-btn {
            position: absolute;
            top: 15px;
            right: 20px;
            font-size: 2rem;
            color: #fff;
            cursor: pointer;
            transition: color 0.2s;
        }

        .close-btn:hover {
            color: #ff0000;
        }

        .modal-body {
            padding: 25px;
        }

        /* STATS TABLE */
        .stats-section h3 {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 1.3rem;
            color: #ff0000;
            margin-bottom: 15px;
            border-bottom: 1px solid #333;
            padding-bottom: 5px;
        }

        .stats-table {
            width: 100%;
            border-collapse: collapse;
            margin-bottom: 25px;
        }

        .stats-table th {
            background: #8B0000;
            padding: 10px;
            font-size: 0.85rem;
            text-transform: uppercase;
        }

        .stats-table td {
            background: #2a2a2a;
            padding: 12px;
            text-align: center;
            font-size: 1.1rem;
            font-weight: bold;
        }

        /* PLAYER INFO */
        .player-info {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
            margin-bottom: 25px;
        }

        .info-item {
            background: #2a2a2a;
            padding: 10px;
            border-radius: 8px;
        }

        .info-item span {
            color: #888;
            font-size: 0.8rem;
            display: block;
        }

        .info-item strong {
            font-size: 1rem;
        }

        /* BIOGRAPHY */
        .biography {
            background: #2a2a2a;
            padding: 15px;
            border-radius: 10px;
            border-left: 4px solid #ff0000;
            margin-bottom: 20px;
        }

        .biography p {
            color: #ccc;
            line-height: 1.6;
        }

        /* DOWNLOAD BUTTON */
        .download-btn {
            display: block;
            width: 100%;
            padding: 15px;
            background: linear-gradient(90deg, #8B0000, #ff0000);
            color: white;
            border: none;
            border-radius: 10px;
            font-family: 'Bebas Neue', sans-serif;
            font-size: 1.2rem;
            letter-spacing: 2px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .download-btn:hover {
            background: linear-gradient(90deg, #ff0000, #8B0000);
            box-shadow: 0 5px 20px rgba(255, 0, 0, 0.4);
        }

        /* FOOTER */
        footer {
            text-align: center;
            padding: 30px;
            color: #555;
            border-top: 1px solid #222;
            margin-top: 50px;
        }
    </style>
</head>
<body>

    <!-- HEADER -->
    <header>
        <h1 class="team-name">DENVER <span>HELLHOUNDS</span></h1>
        <p class="slogan">UNLEASH HELL</p>
    </header>

    <!-- ROSTER -->
    <section class="roster">
        <h2>🏒 TEAM ROSTER</h2>

        <div class="players-grid">

            <!-- PLAYER 1: Caleb Murphy -->
            <div class="player-card" onclick="openModal('caleb')">
                <div class="player-photo">🥅</div>
                <div class="player-number">#33</div>
                <div class="player-name">CALEB MURPHY</div>
                <div class="player-nickname">"Doctor Doom"</div>
                <div class="player-position">Goaltender</div>
                <div class="player-traits">
                    <p>Cynical • Wounded • Surprisingly Observant</p>
                </div>
            </div>

            <!-- PLAYER 2: Chase Sterling -->
            <div class="player-card" onclick="openModal('chase')">
                <div class="player-photo">⭐</div>
                <div class="player-number">#91</div>
                <div class="player-name">CHASE STERLING</div>
                <div class="player-nickname">"Golden Boy"</div>
                <div class="player-position">Center</div>
                <div class="player-traits">
                    <p>Charismatic • Self-Indulgent • Haunted by a Ghost</p>
                </div>
            </div>

            <!-- PLAYER 3: Miles Shaw -->
            <div class="player-card" onclick="openModal('miles')">
                <div class="player-photo">🛡️</div>
                <div class="player-number">#24</div>
                <div class="player-name">MILES SHAW</div>
                <div class="player-nickname">"Milo"</div>
                <div class="player-position">Defenseman</div>
                <div class="player-traits">
                    <p>Quiet • Intense • Secretly Romantic</p>
                </div>
            </div>

            <!-- PLAYER 4: Alexander Reed -->
            <div class="player-card" onclick="openModal('alexander')">
                <div class="player-photo">👑</div>
                <div class="player-number">#8</div>
                <div class="player-name">ALEXANDER REED</div>
                <div class="player-nickname">"Duke"</div>
                <div class="player-position">Right Wing • Captain</div>
                <div class="player-traits">
                    <p>Authoritative • Rigid • Unraveling</p>
                </div>
            </div>

            <!-- PLAYER 5: Leo Carter -->
            <div class="player-card" onclick="openModal('leo')">
                <div class="player-photo">🔥</div>
                <div class="player-number">#17</div>
                <div class="player-name">LEO CARTER</div>
                <div class="player-nickname">"Rookie"</div>
                <div class="player-position">Left Wing</div>
                <div class="player-traits">
                    <p>Talented • Anxious • Living a Double Life</p>
                </div>
            </div>

        </div>
    </section>

    <!-- MODALS -->

    <!-- CALEB MODAL -->
    <div class="modal-overlay" id="modal-caleb">
        <div class="modal">
            <span class="close-btn" onclick="closeModal('caleb')">×</span>
            <div class="modal-header">
                <div class="modal-photo">🥅</div>
                <div class="modal-title">
                    <h2>#33 CALEB MURPHY</h2>
                    <p>"Doctor Doom" • Goaltender</p>
                </div>
            </div>
            <div class="modal-body">
                <div class="stats-section">
                    <h3>📊 2023-24 SEASON STATS</h3>
                    <table class="stats-table">
                        <tr>
                            <th>GP</th>
                            <th>W</th>
                            <th>L</th>
                            <th>GAA</th>
                            <th>SV%</th>
                            <th>SO</th>
                        </tr>
                        <tr>
                            <td>58</td>
                            <td>34</td>
                            <td>16</td>
                            <td>2.41</td>
                            <td>.921</td>
                            <td>5</td>
                        </tr>
                    </table>
                </div>
                <div class="stats-section">
                    <h3>📋 PLAYER INFO</h3>
                    <div class="player-info">
                        <div class="info-item"><span>Height</span><strong>6'3"</strong></div>
                        <div class="info-item"><span>Weight</span><strong>205 lbs</strong></div>
                        <div class="info-item"><span>Age</span><strong>29</strong></div>
                        <div class="info-item"><span>Catches</span><strong>Left</strong></div>
                        <div class="info-item"><span>Birthplace</span><strong>Boston, MA</strong></div>
                        <div class="info-item"><span>Draft</span><strong>2014, R1 #18</strong></div>
                    </div>
                </div>
                <div class="stats-section">
                    <h3>📖 BIOGRAPHY</h3>
                    <div class="biography">
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Caleb Murphy has been the backbone of the Hellhounds defense since joining the team. Known for his unshakeable composure and sharp wit, he earned the nickname "Doctor Doom" for his ability to kill opposing teams' hopes. [PLACEHOLDER - добавь свой текст!]</p>
                    </div>
                </div>
                <button class="download-btn" onclick="downloadCard('caleb')">📥 DOWNLOAD FOR SILLYTAVERN</button>
            </div>
        </div>
    </div>

    <!-- CHASE MODAL -->
    <div class="modal-overlay" id="modal-chase">
        <div class="modal">
            <span class="close-btn" onclick="closeModal('chase')">×</span>
            <div class="modal-header">
                <div class="modal-photo">⭐</div>
                <div class="modal-title">
                    <h2>#91 CHASE STERLING</h2>
                    <p>"Golden Boy" • Center</p>
                </div>
            </div>
            <div class="modal-body">
                <div class="stats-section">
                    <h3>📊 2023-24 SEASON STATS</h3>
                    <table class="stats-table">
                        <tr>
                            <th>GP</th>
                            <th>G</th>
                            <th>A</th>
                            <th>PTS</th>
                            <th>+/-</th>
                            <th>PIM</th>
                        </tr>
                        <tr>
                            <td>82</td>
                            <td>38</td>
                            <td>54</td>
                            <td>92</td>
                            <td>+24</td>
                            <td>28</td>
                        </tr>
                    </table>
                </div>
                <div class="stats-section">
                    <h3>📋 PLAYER INFO</h3>
                    <div class="player-info">
                        <div class="info-item"><span>Height</span><strong>6'1"</strong></div>
                        <div class="info-item"><span>Weight</span><strong>195 lbs</strong></div>
                        <div class="info-item"><span>Age</span><strong>26</strong></div>
                        <div class="info-item"><span>Shoots</span><strong>Right</strong></div>
                        <div class="info-item"><span>Birthplace</span><strong>Toronto, ON</strong></div>
                        <div class="info-item"><span>Draft</span><strong>2016, R1 #2</strong></div>
                    </div>
                </div>
                <div class="stats-section">
                    <h3>📖 BIOGRAPHY</h3>
                    <div class="biography">
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Chase Sterling is the face of the franchise—charismatic, talented, and impossibly photogenic. But behind the million-dollar smile lies something darker. [PLACEHOLDER - добавь свой текст!]</p>
                    </div>
                </div>
                <button class="download-btn" onclick="downloadCard('chase')">📥 DOWNLOAD FOR SILLYTAVERN</button>
            </div>
        </div>
    </div>

    <!-- MILES MODAL -->
    <div class="modal-overlay" id="modal-miles">
        <div class="modal">
            <span class="close-btn" onclick="closeModal('miles')">×</span>
            <div class="modal-header">
                <div class="modal-photo">🛡️</div>
                <div class="modal-title">
                    <h2>#24 MILES SHAW</h2>
                    <p>"Milo" • Defenseman</p>
                </div>
            </div>
            <div class="modal-body">
                <div class="stats-section">
                    <h3>📊 2023-24 SEASON STATS</h3>
                    <table class="stats-table">
                        <tr>
                            <th>GP</th>
                            <th>G</th>
                            <th>A</th>
                            <th>PTS</th>
                            <th>+/-</th>
                            <th>PIM</th>
                        </tr>
                        <tr>
                            <td>78</td>
                            <td>12</td>
                            <td>41</td>
                            <td>53</td>
                            <td>+19</td>
                            <td>34</td>
                        </tr>
                    </table>
                </div>
                <div class="stats-section">
                    <h3>📋 PLAYER INFO</h3>
                    <div class="player-info">
                        <div class="info-item"><span>Height</span><strong>6'2"</strong></div>
                        <div class="info-item"><span>Weight</span><strong>210 lbs</strong></div>
                        <div class="info-item"><span>Age</span><strong>27</strong></div>
                        <div class="info-item"><span>Shoots</span><strong>Left</strong></div>
                        <div class="info-item"><span>Birthplace</span><strong>Minneapolis, MN</strong></div>
                        <div class="info-item"><span>Draft</span><strong>2015, R2 #38</strong></div>
                    </div>
                </div>
                <div class="stats-section">
                    <h3>📖 BIOGRAPHY</h3>
                    <div class="biography">
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Miles Shaw doesn't say much, but his presence on the ice speaks volumes. A shutdown defenseman with surprising offensive instincts, Milo is the quiet heart of the team. [PLACEHOLDER - добавь свой текст!]</p>
                    </div>
                </div>
                <button class="download-btn" onclick="downloadCard('miles')">📥 DOWNLOAD FOR SILLYTAVERN</button>
            </div>
        </div>
    </div>

    <!-- ALEXANDER MODAL -->
    <div class="modal-overlay" id="modal-alexander">
        <div class="modal">
            <span class="close-btn" onclick="closeModal('alexander')">×</span>
            <div class="modal-header">
                <div class="modal-photo">👑</div>
                <div class="modal-title">
                    <h2>#8 ALEXANDER REED (C)</h2>
                    <p>"Duke" • Right Wing • Captain</p>
                </div>
            </div>
            <div class="modal-body">
                <div class="stats-section">
                    <h3>📊 2023-24 SEASON STATS</h3>
                    <table class="stats-table">
                        <tr>
                            <th>GP</th>
                            <th>G</th>
                            <th>A</th>
                            <th>PTS</th>
                            <th>+/-</th>
                            <th>PIM</th>
                        </tr>
                        <tr>
                            <td>80</td>
                            <td>29</td>
                            <td>47</td>
                            <td>76</td>
                            <td>+21</td>
                            <td>52</td>
                        </tr>
                    </table>
                </div>
                <div class="stats-section">
                    <h3>📋 PLAYER INFO</h3>
                    <div class="player-info">
                        <div class="info-item"><span>Height</span><strong>6'4"</strong></div>
                        <div class="info-item"><span>Weight</span><strong>220 lbs</strong></div>
                        <div class="info-item"><span>Age</span><strong>31</strong></div>
                        <div class="info-item"><span>Shoots</span><strong>Right</strong></div>
                        <div class="info-item"><span>Birthplace</span><strong>Detroit, MI</strong></div>
                        <div class="info-item"><span>Draft</span><strong>2011, R1 #5</strong></div>
                    </div>
                </div>
                <div class="stats-section">
                    <h3>📖 BIOGRAPHY</h3>
                    <div class="biography">
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Alexander Reed has worn the "C" for five seasons, leading the Hellhounds with iron discipline and relentless drive. But lately, cracks have begun to show. [PLACEHOLDER - добавь свой текст!]</p>
                    </div>
                </div>
                <button class="download-btn" onclick="downloadCard('alexander')">📥 DOWNLOAD FOR SILLYTAVERN</button>
            </div>
        </div>
    </div>

    <!-- LEO MODAL -->
    <div class="modal-overlay" id="modal-leo">
        <div class="modal">
            <span class="close-btn" onclick="closeModal('leo')">×</span>
            <div class="modal-header">
                <div class="modal-photo">🔥</div>
                <div class="modal-title">
                    <h2>#17 LEO CARTER</h2>
                    <p>"Rookie" • Left Wing</p>
                </div>
            </div>
            <div class="modal-body">
                <div class="stats-section">
                    <h3>📊 2023-24 SEASON STATS</h3>
                    <table class="stats-table">
                        <tr>
                            <th>GP</th>
                            <th>G</th>
                            <th>A</th>
                            <th>PTS</th>
                            <th>+/-</th>
                            <th>PIM</th>
                        </tr>
                        <tr>
                            <td>67</td>
                            <td>22</td>
                            <td>28</td>
                            <td>50</td>
                            <td>+8</td>
                            <td>18</td>
                        </tr>
                    </table>
                </div>
                <div class="stats-section">
                    <h3>📋 PLAYER INFO</h3>
                    <div class="player-info">
                        <div class="info-item"><span>Height</span><strong>5'11"</strong></div>
                        <div class="info-item"><span>Weight</span><strong>185 lbs</strong></div>
                        <div class="info-item"><span>Age</span><strong>21</strong></div>
                        <div class="info-item"><span>Shoots</span><strong>Left</strong></div>
                        <div class="info-item"><span>Birthplace</span><strong>Seattle, WA</strong></div>
                        <div class="info-item"><span>Draft</span><strong>2021, R1 #12</strong></div>
                    </div>
                </div>
                <div class="stats-section">
                    <h3>📖 BIOGRAPHY</h3>
                    <div class="biography">
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Leo Carter burst onto the scene with electrifying speed and raw talent. The youngest player on the roster, he carries the weight of expectations—and secrets. [PLACEHOLDER - добавь свой текст!]</p>
                    </div>
                </div>
                <button class="download-btn" onclick="downloadCard('leo')">📥 DOWNLOAD FOR SILLYTAVERN</button>
            </div>
        </div>
    </div>

    <!-- FOOTER -->
    <footer>
        <p>🔴⚫ Denver Hellhounds • Unleash Hell • Est. 2024 ⚫🔴</p>
        <p style="margin-top: 10px; font-size: 0.8rem;">Cards for SillyTavern</p>
    </footer>

    <script>
        function openModal(player) {
            document.getElementById('modal-' + player).classList.add('active');
            document.body.style.overflow = 'hidden';
        }

        function closeModal(player) {
            document.getElementById('modal-' + player).classList.remove('active');
            document.body.style.overflow = 'auto';
        }

        // Закрытие по клику вне модалки
        document.querySelectorAll('.modal-overlay').forEach(overlay => {
            overlay.addEventListener('click', function(e) {
                if (e.target === this) {
                    this.classList.remove('active');
                    document.body.style.overflow = 'auto';
                }
            });
        });

        // Закрытие по Escape
        document.addEventListener('keydown', function(e) {
            if (e.key === 'Escape') {
                document.querySelectorAll('.modal-overlay').forEach(modal => {
                    modal.classList.remove('active');
                });
                document.body.style.overflow = 'auto';
            }
        });

        function downloadCard(player) {
            // Здесь будут ссылки на твои файлы карточек
            const cards = {
                'caleb': 'cards/caleb_murphy.png',
                'chase': 'cards/chase_sterling.png',
                'miles': 'cards/miles_shaw.png',
                'alexander': 'cards/alexander_reed.png',
                'leo': 'cards/leo_carter.png'
            };

            // Пока просто алерт, потом заменим на реальное скачивание
            alert('Скачивание карточки: ' + player + '\n\nДобавь файлы карточек в папку "cards" и раскомментируй код!');

            // Раскомментируй это когда добавишь файлы:
            // const link = document.createElement('a');
            // link.href = cards[player];
            // link.download = cards[player].split('/').pop();
            // link.click();
        }
    </script>

</body>
</html>
