---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: 48c1a3c3b7422f76bfbea0fbff8c3df541764606
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427999"
---
# <span data-ttu-id="4bd16-101">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="4bd16-101">Get-AzureRmBackupJob</span></span>

## <span data-ttu-id="4bd16-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4bd16-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd16-103">Obtém trabalhos de backup.</span><span class="sxs-lookup"><span data-stu-id="4bd16-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bd16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4bd16-104">SYNTAX</span></span>

### <span data-ttu-id="4bd16-105">Filterset (padrão)</span><span class="sxs-lookup"><span data-stu-id="4bd16-105">FiltersSet (Default)</span></span>
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4bd16-106">JobsListFilter</span><span class="sxs-lookup"><span data-stu-id="4bd16-106">JobsListFilter</span></span>
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bd16-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4bd16-107">DESCRIPTION</span></span>
<span data-ttu-id="4bd16-108">O cmdlet **Get-AzureRmBackupJob** Obtém trabalhos de backup do Azure para um cofre específico.</span><span class="sxs-lookup"><span data-stu-id="4bd16-108">The **Get-AzureRmBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

## <span data-ttu-id="4bd16-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4bd16-109">EXAMPLES</span></span>

### <span data-ttu-id="4bd16-110">Exemplo 1: obter todos os trabalhos em um cofre de backup</span><span class="sxs-lookup"><span data-stu-id="4bd16-110">Example 1: Get all jobs in a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="4bd16-111">O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="4bd16-111">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="4bd16-112">O comando armazena esse objeto na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="4bd16-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="4bd16-113">O segundo comando obtém todos os trabalhos do cofre em $Vault.</span><span class="sxs-lookup"><span data-stu-id="4bd16-113">The second command gets all the jobs for the vault in $Vault.</span></span>

### <span data-ttu-id="4bd16-114">Exemplo 2: obter trabalhos concluídos</span><span class="sxs-lookup"><span data-stu-id="4bd16-114">Example 2: Get completed jobs</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="4bd16-115">Este comando obtém trabalhos concluídos do cofre no $Vault.</span><span class="sxs-lookup"><span data-stu-id="4bd16-115">This command gets completed jobs from the vault in $Vault.</span></span>

### <span data-ttu-id="4bd16-116">Exemplo 3: obter trabalhos com falha na semana passada</span><span class="sxs-lookup"><span data-stu-id="4bd16-116">Example 3: Get failed jobs for the last week</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

<span data-ttu-id="4bd16-117">Esse comando obtém trabalhos com falha da semana passada do cofre em $Vault.</span><span class="sxs-lookup"><span data-stu-id="4bd16-117">This command gets failed jobs from the last week from the vault in $Vault.</span></span>
<span data-ttu-id="4bd16-118">O parâmetro *from* especifica um período de sete dias no passado.</span><span class="sxs-lookup"><span data-stu-id="4bd16-118">The *From* parameter specifies a time seven days in the past.</span></span>
<span data-ttu-id="4bd16-119">O comando não especifica um valor para o parâmetro *to* .</span><span class="sxs-lookup"><span data-stu-id="4bd16-119">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="4bd16-120">Portanto, ele usa o valor padrão do tempo atual.</span><span class="sxs-lookup"><span data-stu-id="4bd16-120">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="4bd16-121">Exemplo 4: sondar o backup para um trabalho em andamento que é concluído</span><span class="sxs-lookup"><span data-stu-id="4bd16-121">Example 4: Poll Backup for an in progress job that finishes</span></span>
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

<span data-ttu-id="4bd16-122">Este script sonda o primeiro trabalho que está em andamento até que o trabalho seja concluído.</span><span class="sxs-lookup"><span data-stu-id="4bd16-122">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="4bd16-123">A primeira linha do script Obtém todos os trabalhos em $Vault que estão em andamento e armazena esses trabalhos na $Jobs variável de matriz.</span><span class="sxs-lookup"><span data-stu-id="4bd16-123">The first line of the script gets all the jobs in $Vault that are in progress, and then stores those jobs in the $Jobs array variable.</span></span>

<span data-ttu-id="4bd16-124">A segunda linha armazena o primeiro trabalho da matriz $Jobs na variável $Job.</span><span class="sxs-lookup"><span data-stu-id="4bd16-124">The second line stores the first job from the $Jobs array in the $Job variable.</span></span>

<span data-ttu-id="4bd16-125">A terceira linha iniciará um loop **while** que verifica o status atual do trabalho até que o trabalho seja concluído.</span><span class="sxs-lookup"><span data-stu-id="4bd16-125">The third line starts a **while** loop that checks the current status of the job until the job is completed.</span></span>
<span data-ttu-id="4bd16-126">Para obter informações sobre a palavra-chave **while** , digite `Get-Help about_While` .</span><span class="sxs-lookup"><span data-stu-id="4bd16-126">For information about the **while** keyword, type `Get-Help about_While`.</span></span>

<span data-ttu-id="4bd16-127">O loop **while** grava uma mensagem no console, dorme por dez segundos e, em seguida, atualiza a variável $Job.</span><span class="sxs-lookup"><span data-stu-id="4bd16-127">The **while** loop writes a message to the console, sleeps for ten seconds, and then updates the $Job variable.</span></span>
<span data-ttu-id="4bd16-128">O script atualiza a variável $Job usando o valor existente do $Job e o cmdlet atual para obter o status atual do trabalho.</span><span class="sxs-lookup"><span data-stu-id="4bd16-128">The script updates the $Job variable by using existing value of $Job and the current cmdlet to get the current status of the job.</span></span>
<span data-ttu-id="4bd16-129">Para obter informações sobre os cmdlets do Windows PowerShell, digite `Get-Help Write-Host` e `Get-Help Start-Sleep` .</span><span class="sxs-lookup"><span data-stu-id="4bd16-129">For information about the Windows PowerShell cmdlets, type `Get-Help Write-Host` and `Get-Help Start-Sleep`.</span></span>

<span data-ttu-id="4bd16-130">A linha final do script informa que o script foi concluído.</span><span class="sxs-lookup"><span data-stu-id="4bd16-130">The final line of the script tells you that the script has finished.</span></span>

## <span data-ttu-id="4bd16-131">OS</span><span class="sxs-lookup"><span data-stu-id="4bd16-131">PARAMETERS</span></span>

### <span data-ttu-id="4bd16-132">-De</span><span class="sxs-lookup"><span data-stu-id="4bd16-132">-From</span></span>
<span data-ttu-id="4bd16-133">Especifica o início, como um objeto **DateTime** , de um intervalo de tempo para os trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="4bd16-133">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="4bd16-134">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="4bd16-134">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="4bd16-135">Para obter mais informações sobre objetos **DateTime** , digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="4bd16-135">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd16-136">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="4bd16-136">-Job</span></span>
<span data-ttu-id="4bd16-137">Especifica um trabalho que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="4bd16-137">Specifies a job that this cmdlet gets.</span></span>
<span data-ttu-id="4bd16-138">Para obter um objeto **AzureRmBackupJob** , use o cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="4bd16-138">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd16-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="4bd16-139">-JobId</span></span>
<span data-ttu-id="4bd16-140">Especifica a ID de um trabalho que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="4bd16-140">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="4bd16-141">A ID é a propriedade **InstanceId** de um objeto **AzureRmBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="4bd16-141">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="4bd16-142">Para obter um objeto **AzureRmBackupJob** , use Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="4bd16-142">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd16-143">-Operação</span><span class="sxs-lookup"><span data-stu-id="4bd16-143">-Operation</span></span>
<span data-ttu-id="4bd16-144">Especifica uma operação dos trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="4bd16-144">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="4bd16-145">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4bd16-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4bd16-146">Fazer</span><span class="sxs-lookup"><span data-stu-id="4bd16-146">Backup</span></span> 
- <span data-ttu-id="4bd16-147">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="4bd16-147">ConfigureBackup</span></span> 
- <span data-ttu-id="4bd16-148">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="4bd16-148">DeleteBackupData</span></span> 
- <span data-ttu-id="4bd16-149">Inscrição</span><span class="sxs-lookup"><span data-stu-id="4bd16-149">Register</span></span> 
- <span data-ttu-id="4bd16-150">Restaurar</span><span class="sxs-lookup"><span data-stu-id="4bd16-150">Restore</span></span> 
- <span data-ttu-id="4bd16-151">Desproteger</span><span class="sxs-lookup"><span data-stu-id="4bd16-151">UnProtect</span></span> 
- <span data-ttu-id="4bd16-152">Cancele</span><span class="sxs-lookup"><span data-stu-id="4bd16-152">Unregister</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd16-153">-Status</span><span class="sxs-lookup"><span data-stu-id="4bd16-153">-Status</span></span>
<span data-ttu-id="4bd16-154">Especifica um status dos trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="4bd16-154">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="4bd16-155">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4bd16-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4bd16-156">InProgress</span><span class="sxs-lookup"><span data-stu-id="4bd16-156">InProgress</span></span>
- <span data-ttu-id="4bd16-157">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="4bd16-157">Failed</span></span>
- <span data-ttu-id="4bd16-158">Cela</span><span class="sxs-lookup"><span data-stu-id="4bd16-158">Cancelled</span></span>
- <span data-ttu-id="4bd16-159">Cancelamento</span><span class="sxs-lookup"><span data-stu-id="4bd16-159">Cancelling</span></span>
- <span data-ttu-id="4bd16-160">Feito</span><span class="sxs-lookup"><span data-stu-id="4bd16-160">Completed</span></span>
- <span data-ttu-id="4bd16-161">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="4bd16-161">CompletedWithWarnings</span></span> 

<span data-ttu-id="4bd16-162">Você pode especificar esse parâmetro para localizar todos os trabalhos em andamento ou todos os trabalhos com falha.</span><span class="sxs-lookup"><span data-stu-id="4bd16-162">You can specify this parameter to find all in progress jobs or all failed jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd16-163">-To</span><span class="sxs-lookup"><span data-stu-id="4bd16-163">-To</span></span>
<span data-ttu-id="4bd16-164">Especifica o fim, como um objeto **DateTime** , de um intervalo de tempo para os trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="4bd16-164">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="4bd16-165">O valor padrão é a hora atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="4bd16-165">The default value is the current system time.</span></span>
<span data-ttu-id="4bd16-166">Se você especificar esse parâmetro, também deverá especificar o parâmetro *from* .</span><span class="sxs-lookup"><span data-stu-id="4bd16-166">If you specify this parameter, you must also specify the *From* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd16-167">-Digite</span><span class="sxs-lookup"><span data-stu-id="4bd16-167">-Type</span></span>
<span data-ttu-id="4bd16-168">Especifica o tipo de contêiner para o qual esse cmdlet obtém trabalhos de backup.</span><span class="sxs-lookup"><span data-stu-id="4bd16-168">Specifies the type of container for which this cmdlet gets backup jobs.</span></span>
<span data-ttu-id="4bd16-169">Atualmente, o único valor com suporte é AzureVM.</span><span class="sxs-lookup"><span data-stu-id="4bd16-169">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd16-170">-Cofre</span><span class="sxs-lookup"><span data-stu-id="4bd16-170">-Vault</span></span>
<span data-ttu-id="4bd16-171">Especifica o cofre de backup para o qual este cmdlet recebe trabalhos.</span><span class="sxs-lookup"><span data-stu-id="4bd16-171">Specifies the Backup vault for which this cmdlet gets jobs.</span></span>
<span data-ttu-id="4bd16-172">Para obter um objeto **AzureRmBackupVault** , use o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="4bd16-172">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd16-173">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd16-173">-DefaultProfile</span></span>
<span data-ttu-id="4bd16-174">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd16-174">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd16-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd16-175">CommonParameters</span></span>
<span data-ttu-id="4bd16-176">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bd16-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd16-177">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bd16-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd16-178">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4bd16-178">INPUTS</span></span>

### <span data-ttu-id="4bd16-179">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="4bd16-179">AzureRmBackupVault</span></span>

## <span data-ttu-id="4bd16-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4bd16-180">OUTPUTS</span></span>

### <span data-ttu-id="4bd16-181">AzureRmBackupJob[]</span><span class="sxs-lookup"><span data-stu-id="4bd16-181">AzureRmBackupJob[]</span></span>
<span data-ttu-id="4bd16-182">Esse cmdlet retorna um ou mais trabalhos de backup.</span><span class="sxs-lookup"><span data-stu-id="4bd16-182">This cmdlet returns one or more Backup jobs.</span></span>

## <span data-ttu-id="4bd16-183">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4bd16-183">NOTES</span></span>
* <span data-ttu-id="4bd16-184">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4bd16-184">None</span></span>

## <span data-ttu-id="4bd16-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4bd16-185">RELATED LINKS</span></span>

[<span data-ttu-id="4bd16-186">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="4bd16-186">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="4bd16-187">Parar-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="4bd16-187">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)

[<span data-ttu-id="4bd16-188">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="4bd16-188">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


