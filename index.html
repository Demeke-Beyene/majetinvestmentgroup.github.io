<?php
session_start();
require 'db.php'; // Include your database connection

if ($_SERVER['REQUEST_METHOD'] === 'POST') {
    $username = trim($_POST['username']);
    $password = $_POST['password'];

    try {
        // Prepare SQL query to fetch user details along with role name
        $stmt = $pdo->prepare("
            SELECT u.id, u.username, u.password_hash, r.role_name
            FROM users u
            JOIN roles r ON u.role_id = r.role_id
            WHERE u.username = ?
        ");
        $stmt->execute([$username]);
        $user = $stmt->fetch();

        if ($user && password_verify($password, $user['password_hash'])) {
            // Store user details in session
            $_SESSION['user_id'] = $user['id'];
            $_SESSION['username'] = $user['username'];
            $_SESSION['role'] = $user['role_name'];

            // Redirect to dashboard
            header("Location: dashboard.php");
            exit;
        } else {
            $error = "Invalid username or password";
        }
    } catch (PDOException $e) {
        $error = "Database error: " . $e->getMessage();
    }
}
?>


<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Login - Majet Investment Group (MIG)</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
<style>
    body {
        margin: 0;
        font-family: 'Poppins', sans-serif;
        background: linear-gradient(135deg, #4facfe, #00f2fe);
        min-height: 100vh;
        display: flex;
        justify-content: center;
        align-items: flex-start;
        gap: 30px;
        padding: 40px 20px;
        flex-wrap: wrap;
    }

    /* Glass effect for containers */
    .login-container, .info-container {
        background: rgba(255, 255, 255, 0.85);
        padding: 25px;
        border-radius: 16px;
        border: 1px solid rgba(255, 255, 255, 0.3);
        box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        backdrop-filter: blur(10px);
        transition: transform 0.3s ease;
    }

    .login-container:hover, .info-container:hover {
        transform: translateY(-3px);
    }

    /* Login Box */
    .login-container {
        width: 270px;
        text-align: center;
    }

    .login-container img {
        width: 140px;
        margin-bottom: 10px;
    }

    .login-container input {
        width: 90%;
        padding: 14px;
        margin: 12px 0;
        border: 1px solid #ccc;
        border-radius: 10px;
        font-size: 15px;
        background-color: rgba(255,255,255,0.7);
        transition: 0.3s;
    }

    .login-container input:focus {
        border-color: #4facfe;
        outline: none;
        box-shadow: 0 0 8px rgba(79,172,254,0.3);
    }

    .login-container button {
        width: 70%;
        padding: 12px;
        background: linear-gradient(135deg, #1abc9c, #16a085);
        color: #fff;
        border: none;
        border-radius: 8px;
        font-size: 15px;
        font-weight: 600;
        cursor: pointer;
        transition: 0.3s;
    }

    .login-container button:hover {
        background: linear-gradient(135deg, #16a085, #1abc9c);
        transform: scale(1.05);
    }

    .login-container .error {
        color: #e74c3c;
        margin-top: 10px;
        font-size: 13px;
    }

    /* Info Box */
    .info-container {
        max-width: 420px;
        font-size: 14px;
        line-height: 1.7;
    }

    .info-container h2 {
        color: #007bff;
        margin-bottom: 5px;
        font-weight: 600;
    }

    .info-container ol {
        padding-left: 20px;
    }

    /* Footer */
    footer {
        text-align: center;
        background: rgba(0, 123, 255, 0.85);
        color: #fff;
        padding: 10px 0;
        font-size: 14px;
        position: fixed;
        bottom: 0;
        left: 0;
        right: 0;
    }

    /* Responsive Design */
    @media (max-width: 768px) {
        body {
            flex-direction: column;
            align-items: center;
        }
        footer {
            position: static;
        }
    }
</style>
</head>
<body>

<!-- Login Section -->
<div class="login-container">
    <img src="IMAGE/Majet.JPG" alt="Majet Logo"/>
    <form method="POST" action="">
        <input type="text" name="username" placeholder="Enter Username" required>
        <input type="password" name="password" placeholder="Enter Password" required>
        <button type="submit">Login</button>
    </form>
    <?php if (!empty($error)): ?>
        <p class="error"><?= htmlspecialchars($error) ?></p>
    <?php endif; ?>
</div>

<!-- Vision, Mission & Core Values Section -->
<div class="info-container">
    <h2>Vision</h2>
    <p>To become a leading, inclusive group of entrepreneurs and investors empowering individuals and communities across Ethiopia.</p>

    <h2>Mission</h2>
    <ol>
        <li>Unite diverse skills and resources.</li>
        <li>Launch sustainable, impactful businesses.</li>
        <li>Promote ethical practices respecting culture and communities.</li>
        <li>Encourage lifelong learning and leadership.</li>
        <li>Apply innovation to solve real challenges.</li>
    </ol>

    <h2>Core Values</h2>
    <p>Integrity | Unity | Innovation | Accountability | Empowerment | Respect | Cultural Pride</p>
</div>

<footer>
    <p>&copy; <?= date('Y') ?> Majet Investment Group. All rights reserved.</p>
</footer>

</body>
</html>
