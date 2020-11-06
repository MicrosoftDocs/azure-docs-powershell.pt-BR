---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: 3402dc7018f094a5f95a967385d9bae8d70c68f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428988"
---
# <span data-ttu-id="b777e-101">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="b777e-101">Get-AzureRmBackupJob</span></span>

## <span data-ttu-id="b777e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b777e-102">SYNOPSIS</span></span>
<span data-ttu-id="b777e-103">Obtém trabalhos de backup.</span><span class="sxs-lookup"><span data-stu-id="b777e-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b777e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b777e-104">SYNTAX</span></span>

### <span data-ttu-id="b777e-105">Filterset (padrão)</span><span class="sxs-lookup"><span data-stu-id="b777e-105">FiltersSet (Default)</span></span>
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b777e-106">JobsListFilter</span><span class="sxs-lookup"><span data-stu-id="b777e-106">JobsListFilter</span></span>
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b777e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b777e-107">DESCRIPTION</span></span>
<span data-ttu-id="b777e-108">O cmdlet **Get-AzureRmBackupJob** Obtém trabalhos de backup do Azure para um cofre específico.</span><span class="sxs-lookup"><span data-stu-id="b777e-108">The **Get-AzureRmBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

## <span data-ttu-id="b777e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b777e-109">EXAMPLES</span></span>

### <span data-ttu-id="b777e-110">Exemplo 1: obter todos os trabalhos em um cofre de backup</span><span class="sxs-lookup"><span data-stu-id="b777e-110">Example 1: Get all jobs in a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="b777e-111">O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="b777e-111">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="b777e-112">O comando armazena esse objeto na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="b777e-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="b777e-113">O segundo comando obtém todos os trabalhos do cofre em $Vault.</span><span class="sxs-lookup"><span data-stu-id="b777e-113">The second command gets all the jobs for the vault in $Vault.</span></span>

### <span data-ttu-id="b777e-114">Exemplo 2: obter trabalhos concluídos</span><span class="sxs-lookup"><span data-stu-id="b777e-114">Example 2: Get completed jobs</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="b777e-115">Este comando obtém trabalhos concluídos do cofre no $Vault.</span><span class="sxs-lookup"><span data-stu-id="b777e-115">This command gets completed jobs from the vault in $Vault.</span></span>

### <span data-ttu-id="b777e-116">Exemplo 3: obter trabalhos com falha na semana passada</span><span class="sxs-lookup"><span data-stu-id="b777e-116">Example 3: Get failed jobs for the last week</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

<span data-ttu-id="b777e-117">Esse comando obtém trabalhos com falha da semana passada do cofre em $Vault.</span><span class="sxs-lookup"><span data-stu-id="b777e-117">This command gets failed jobs from the last week from the vault in $Vault.</span></span>
<span data-ttu-id="b777e-118">O parâmetro *from* especifica um período de sete dias no passado.</span><span class="sxs-lookup"><span data-stu-id="b777e-118">The *From* parameter specifies a time seven days in the past.</span></span>
<span data-ttu-id="b777e-119">O comando não especifica um valor para o parâmetro *to* .</span><span class="sxs-lookup"><span data-stu-id="b777e-119">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="b777e-120">Portanto, ele usa o valor padrão do tempo atual.</span><span class="sxs-lookup"><span data-stu-id="b777e-120">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="b777e-121">Exemplo 4: sondar o backup para um trabalho em andamento que é concluído</span><span class="sxs-lookup"><span data-stu-id="b777e-121">Example 4: Poll Backup for an in progress job that finishes</span></span>
```
PS C:\>$Jobs = Get-AzureRmBackupJob -Vault $Vault -Status InProgress
$Job = $Jobs[0] 
while ( $Job.Status -ne Completed ) 
{
   Write-Host "Waiting for completion..." 
   Start-Sleep -Seconds 10
   $job = Get-AzureRmBackupJob -Vault $Vault -Job $Job
}
Write-Host "Done!"
Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

<span data-ttu-id="b777e-122">Este script sonda o primeiro trabalho que está em andamento até que o trabalho seja concluído.</span><span class="sxs-lookup"><span data-stu-id="b777e-122">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="b777e-123">A primeira linha do script Obtém todos os trabalhos em $Vault que estão em andamento e armazena esses trabalhos na $Jobs variável de matriz.</span><span class="sxs-lookup"><span data-stu-id="b777e-123">The first line of the script gets all the jobs in $Vault that are in progress, and then stores those jobs in the $Jobs array variable.</span></span>

<span data-ttu-id="b777e-124">A segunda linha armazena o primeiro trabalho da matriz $Jobs na variável $Job.</span><span class="sxs-lookup"><span data-stu-id="b777e-124">The second line stores the first job from the $Jobs array in the $Job variable.</span></span>

<span data-ttu-id="b777e-125">A terceira linha iniciará um loop **while** que verifica o status atual do trabalho até que o trabalho seja concluído.</span><span class="sxs-lookup"><span data-stu-id="b777e-125">The third line starts a **while** loop that checks the current status of the job until the job is completed.</span></span>
<span data-ttu-id="b777e-126">Para obter informações sobre a palavra-chave **while** , digite `Get-Help about_While` .</span><span class="sxs-lookup"><span data-stu-id="b777e-126">For information about the **while** keyword, type `Get-Help about_While`.</span></span>

<span data-ttu-id="b777e-127">O loop **while** grava uma mensagem no console, dorme por dez segundos e, em seguida, atualiza a variável $Job.</span><span class="sxs-lookup"><span data-stu-id="b777e-127">The **while** loop writes a message to the console, sleeps for ten seconds, and then updates the $Job variable.</span></span>
<span data-ttu-id="b777e-128">O script atualiza a variável $Job usando o valor existente do $Job e o cmdlet atual para obter o status atual do trabalho.</span><span class="sxs-lookup"><span data-stu-id="b777e-128">The script updates the $Job variable by using existing value of $Job and the current cmdlet to get the current status of the job.</span></span>
<span data-ttu-id="b777e-129">Para obter informações sobre os cmdlets do Windows PowerShell, digite `Get-Help Write-Host` e `Get-Help Start-Sleep` .</span><span class="sxs-lookup"><span data-stu-id="b777e-129">For information about the Windows PowerShell cmdlets, type `Get-Help Write-Host` and `Get-Help Start-Sleep`.</span></span>

<span data-ttu-id="b777e-130">A linha final do script informa que o script foi concluído.</span><span class="sxs-lookup"><span data-stu-id="b777e-130">The final line of the script tells you that the script has finished.</span></span>

## <span data-ttu-id="b777e-131">OS</span><span class="sxs-lookup"><span data-stu-id="b777e-131">PARAMETERS</span></span>

### <span data-ttu-id="b777e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b777e-132">-DefaultProfile</span></span>
<span data-ttu-id="b777e-133">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b777e-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b777e-134">-De</span><span class="sxs-lookup"><span data-stu-id="b777e-134">-From</span></span>
<span data-ttu-id="b777e-135">Especifica o início, como um objeto **DateTime** , de um intervalo de tempo para os trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b777e-135">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="b777e-136">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="b777e-136">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="b777e-137">Para obter mais informações sobre objetos **DateTime** , digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="b777e-137">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b777e-138">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="b777e-138">-Job</span></span>
<span data-ttu-id="b777e-139">Especifica um trabalho que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b777e-139">Specifies a job that this cmdlet gets.</span></span>
<span data-ttu-id="b777e-140">Para obter um objeto **AzureRmBackupJob** , use o cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="b777e-140">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b777e-141">-JobId</span><span class="sxs-lookup"><span data-stu-id="b777e-141">-JobId</span></span>
<span data-ttu-id="b777e-142">Especifica a ID de um trabalho que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b777e-142">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="b777e-143">A ID é a propriedade **InstanceId** de um objeto **AzureRmBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="b777e-143">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="b777e-144">Para obter um objeto **AzureRmBackupJob** , use Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="b777e-144">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b777e-145">-Operação</span><span class="sxs-lookup"><span data-stu-id="b777e-145">-Operation</span></span>
<span data-ttu-id="b777e-146">Especifica uma operação dos trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b777e-146">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="b777e-147">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b777e-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b777e-148">Fazer</span><span class="sxs-lookup"><span data-stu-id="b777e-148">Backup</span></span> 
- <span data-ttu-id="b777e-149">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="b777e-149">ConfigureBackup</span></span> 
- <span data-ttu-id="b777e-150">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="b777e-150">DeleteBackupData</span></span> 
- <span data-ttu-id="b777e-151">Inscrição</span><span class="sxs-lookup"><span data-stu-id="b777e-151">Register</span></span> 
- <span data-ttu-id="b777e-152">Restaurar</span><span class="sxs-lookup"><span data-stu-id="b777e-152">Restore</span></span> 
- <span data-ttu-id="b777e-153">Desproteger</span><span class="sxs-lookup"><span data-stu-id="b777e-153">UnProtect</span></span> 
- <span data-ttu-id="b777e-154">Cancele</span><span class="sxs-lookup"><span data-stu-id="b777e-154">Unregister</span></span>

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b777e-155">-Status</span><span class="sxs-lookup"><span data-stu-id="b777e-155">-Status</span></span>
<span data-ttu-id="b777e-156">Especifica um status dos trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b777e-156">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="b777e-157">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b777e-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b777e-158">InProgress</span><span class="sxs-lookup"><span data-stu-id="b777e-158">InProgress</span></span>
- <span data-ttu-id="b777e-159">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="b777e-159">Failed</span></span>
- <span data-ttu-id="b777e-160">Cela</span><span class="sxs-lookup"><span data-stu-id="b777e-160">Cancelled</span></span>
- <span data-ttu-id="b777e-161">Cancelamento</span><span class="sxs-lookup"><span data-stu-id="b777e-161">Cancelling</span></span>
- <span data-ttu-id="b777e-162">Feito</span><span class="sxs-lookup"><span data-stu-id="b777e-162">Completed</span></span>
- <span data-ttu-id="b777e-163">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="b777e-163">CompletedWithWarnings</span></span> 

<span data-ttu-id="b777e-164">Você pode especificar esse parâmetro para localizar todos os trabalhos em andamento ou todos os trabalhos com falha.</span><span class="sxs-lookup"><span data-stu-id="b777e-164">You can specify this parameter to find all in progress jobs or all failed jobs.</span></span>

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b777e-165">-To</span><span class="sxs-lookup"><span data-stu-id="b777e-165">-To</span></span>
<span data-ttu-id="b777e-166">Especifica o fim, como um objeto **DateTime** , de um intervalo de tempo para os trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b777e-166">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="b777e-167">O valor padrão é a hora atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="b777e-167">The default value is the current system time.</span></span>
<span data-ttu-id="b777e-168">Se você especificar esse parâmetro, também deverá especificar o parâmetro *from* .</span><span class="sxs-lookup"><span data-stu-id="b777e-168">If you specify this parameter, you must also specify the *From* parameter.</span></span>

```yaml
Type: DateTime
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b777e-169">-Digite</span><span class="sxs-lookup"><span data-stu-id="b777e-169">-Type</span></span>
<span data-ttu-id="b777e-170">Especifica o tipo de contêiner para o qual esse cmdlet obtém trabalhos de backup.</span><span class="sxs-lookup"><span data-stu-id="b777e-170">Specifies the type of container for which this cmdlet gets backup jobs.</span></span>
<span data-ttu-id="b777e-171">Atualmente, o único valor com suporte é AzureVM.</span><span class="sxs-lookup"><span data-stu-id="b777e-171">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b777e-172">-Cofre</span><span class="sxs-lookup"><span data-stu-id="b777e-172">-Vault</span></span>
<span data-ttu-id="b777e-173">Especifica o cofre de backup para o qual este cmdlet recebe trabalhos.</span><span class="sxs-lookup"><span data-stu-id="b777e-173">Specifies the Backup vault for which this cmdlet gets jobs.</span></span>
<span data-ttu-id="b777e-174">Para obter um objeto **AzureRmBackupVault** , use o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="b777e-174">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b777e-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b777e-175">CommonParameters</span></span>
<span data-ttu-id="b777e-176">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b777e-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b777e-177">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b777e-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b777e-178">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b777e-178">INPUTS</span></span>

### <span data-ttu-id="b777e-179">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b777e-179">AzureRmBackupVault</span></span>

## <span data-ttu-id="b777e-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b777e-180">OUTPUTS</span></span>

### <span data-ttu-id="b777e-181">AzureRmBackupJob[]</span><span class="sxs-lookup"><span data-stu-id="b777e-181">AzureRmBackupJob[]</span></span>
<span data-ttu-id="b777e-182">Esse cmdlet retorna um ou mais trabalhos de backup.</span><span class="sxs-lookup"><span data-stu-id="b777e-182">This cmdlet returns one or more Backup jobs.</span></span>

## <span data-ttu-id="b777e-183">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b777e-183">NOTES</span></span>
* <span data-ttu-id="b777e-184">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b777e-184">None</span></span>

## <span data-ttu-id="b777e-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b777e-185">RELATED LINKS</span></span>

[<span data-ttu-id="b777e-186">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b777e-186">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="b777e-187">Parar-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="b777e-187">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)

[<span data-ttu-id="b777e-188">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="b777e-188">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


