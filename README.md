 
static void Main(string[] args)
        {
Console.WriteLine("Введите сумму в рублях");
 Console.Write(reshener( Convert.ToInt64(Console.ReadLine())));
}
private String reshener(Int64 text)
        {
            string[] Rus_Kup = { "5000 рублей", "1000 рублей", "500 рублей", "100 рублей", "50 рублей", "10 рублей", "5 рублей", "2 рубля", "1 рубль" };
            int[] Nominal = { 5000, 1000, 500, 100, 50, 10, 5, 2, 1 },
            Kol_Vo_Nominala = { 0, 0, 0, 0, 0, 0, 0, 0, 0 };
            Int64 arab = text;
            int i = 0;
            while (arab > 0)
            {
                if (arab >= Nominal[i])
                {
                    Kol_Vo_Nominala[i]++;
                    arab -= Nominal[i];
                }
                else
                    i++;
            }
            
 
            String Message = "";
 
            for (int ii = 0; ii < Kol_Vo_Nominala.Length; ii++)
            {
                if (Kol_Vo_Nominala[ii] != 0)
                {
                    Message += Rus_Kup[ii] + " x " + Kol_Vo_Nominala[ii] + "\r\n";
                }
            }
return  Message;
        }
