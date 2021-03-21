public class Score_System : MonoBehaviour
{
    [SerializeField] Glow_Punch glow_Punch;
    [SerializeField] Text scoreText;

    private void OnEnable()
    {
        glow_Punch.onScoring += addScore;
    }
    private void OnDisble()
    {
        glow_Punch.onScoring -= addScore;
    }
    private void addScore(int Score)
    {
        Score = glow_Punch.score;
        scoreText.text = Score.ToString();
    }
}
