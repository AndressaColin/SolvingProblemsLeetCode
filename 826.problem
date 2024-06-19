class Solution(object):
    def maxProfitAssignment(self, difficulty, profit, worker):
        jobs = list(zip(difficulty, profit))
        jobs.sort()
        worker.sort()
        #Inicializar variáveis para rastrear o lucro máximo e o lucro total
        max_profit = 0
        total_profit = 0
        #ponteiro para percorrer a lista jobs
        i = 0
        #armazena o comprimento da lista jobs
        n = len(jobs)
        for j in range(len(worker)):
            skills = worker[j]
            while i < n and skills >= jobs[i][0]:
                # Atualizar o maior lucro possível até agora
                max_profit = max(max_profit, jobs[i][1])
                # Avançar para o próximo trabalho
                i += 1

            # Adicionar o melhor lucro para este trabalhador ao lucro total
            total_profit += max_profit
        return total_profit

# Exemplo de uso:
difficulty = [2, 4, 6, 8, 10]
profit = [10, 20, 30, 40, 50]
worker = [4, 5, 6, 7]

solution = Solution()
print(solution.maxProfitAssignment(difficulty, profit, worker))  

