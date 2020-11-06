---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: cbdb60fb4ec139b1dae92b7dd8e2e54675ae1f90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429593"
---
# <span data-ttu-id="968c2-101">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="968c2-101">Get-AzureRmBackupJob</span></span>

## <span data-ttu-id="968c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="968c2-102">SYNOPSIS</span></span>
<span data-ttu-id="968c2-103">Obtém trabalhos de backup.</span><span class="sxs-lookup"><span data-stu-id="968c2-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="968c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="968c2-104">SYNTAX</span></span>

### <span data-ttu-id="968c2-105">Filterset (padrão)</span><span class="sxs-lookup"><span data-stu-id="968c2-105">FiltersSet (Default)</span></span>
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="968c2-106">JobsListFilter</span><span class="sxs-lookup"><span data-stu-id="968c2-106">JobsListFilter</span></span>
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="968c2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="968c2-107">DESCRIPTION</span></span>
<span data-ttu-id="968c2-108">O cmdlet **Get-AzureRmBackupJob** Obtém trabalhos de backup do Azure para um cofre específico.</span><span class="sxs-lookup"><span data-stu-id="968c2-108">The **Get-AzureRmBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

## <span data-ttu-id="968c2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="968c2-109">EXAMPLES</span></span>

### <span data-ttu-id="968c2-110">Exemplo 1: obter todos os trabalhos em um cofre de backup</span><span class="sxs-lookup"><span data-stu-id="968c2-110">Example 1: Get all jobs in a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="968c2-111">O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="968c2-111">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="968c2-112">O comando armazena esse objeto na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="968c2-112">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="968c2-113">O segundo comando obtém todos os trabalhos do cofre em $Vault.</span><span class="sxs-lookup"><span data-stu-id="968c2-113">The second command gets all the jobs for the vault in $Vault.</span></span>

### <span data-ttu-id="968c2-114">Exemplo 2: obter trabalhos concluídos</span><span class="sxs-lookup"><span data-stu-id="968c2-114">Example 2: Get completed jobs</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="968c2-115">Este comando obtém trabalhos concluídos do cofre no $Vault.</span><span class="sxs-lookup"><span data-stu-id="968c2-115">This command gets completed jobs from the vault in $Vault.</span></span>

### <span data-ttu-id="968c2-116">Exemplo 3: obter trabalhos com falha na semana passada</span><span class="sxs-lookup"><span data-stu-id="968c2-116">Example 3: Get failed jobs for the last week</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

<span data-ttu-id="968c2-117">Esse comando obtém trabalhos com falha da semana passada do cofre em $Vault.</span><span class="sxs-lookup"><span data-stu-id="968c2-117">This command gets failed jobs from the last week from the vault in $Vault.</span></span>
<span data-ttu-id="968c2-118">O parâmetro *from* especifica um período de sete dias no passado.</span><span class="sxs-lookup"><span data-stu-id="968c2-118">The *From* parameter specifies a time seven days in the past.</span></span>
<span data-ttu-id="968c2-119">O comando não especifica um valor para o parâmetro *to* .</span><span class="sxs-lookup"><span data-stu-id="968c2-119">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="968c2-120">Portanto, ele usa o valor padrão do tempo atual.</span><span class="sxs-lookup"><span data-stu-id="968c2-120">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="968c2-121">Exemplo 4: sondar o backup para um trabalho em andamento que é concluído</span><span class="sxs-lookup"><span data-stu-id="968c2-121">Example 4: Poll Backup for an in progress job that finishes</span></span>
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

<span data-ttu-id="968c2-122">Este script sonda o primeiro trabalho que está em andamento até que o trabalho seja concluído.</span><span class="sxs-lookup"><span data-stu-id="968c2-122">This script polls the first job that is currently in progress until the job has completed.</span></span>
<span data-ttu-id="968c2-123">A primeira linha do script Obtém todos os trabalhos em $Vault que estão em andamento e armazena esses trabalhos na $Jobs variável de matriz.</span><span class="sxs-lookup"><span data-stu-id="968c2-123">The first line of the script gets all the jobs in $Vault that are in progress, and then stores those jobs in the $Jobs array variable.</span></span>
<span data-ttu-id="968c2-124">A segunda linha armazena o primeiro trabalho da matriz $Jobs na variável $Job.</span><span class="sxs-lookup"><span data-stu-id="968c2-124">The second line stores the first job from the $Jobs array in the $Job variable.</span></span>
<span data-ttu-id="968c2-125">A terceira linha iniciará um loop **while** que verifica o status atual do trabalho até que o trabalho seja concluído.</span><span class="sxs-lookup"><span data-stu-id="968c2-125">The third line starts a **while** loop that checks the current status of the job until the job is completed.</span></span>
<span data-ttu-id="968c2-126">Para obter informações sobre a palavra-chave **while** , digite `Get-Help about_While` .</span><span class="sxs-lookup"><span data-stu-id="968c2-126">For information about the **while** keyword, type `Get-Help about_While`.</span></span>
<span data-ttu-id="968c2-127">O loop **while** grava uma mensagem no console, dorme por dez segundos e, em seguida, atualiza a variável $Job.</span><span class="sxs-lookup"><span data-stu-id="968c2-127">The **while** loop writes a message to the console, sleeps for ten seconds, and then updates the $Job variable.</span></span>
<span data-ttu-id="968c2-128">O script atualiza a variável $Job usando o valor existente do $Job e o cmdlet atual para obter o status atual do trabalho.</span><span class="sxs-lookup"><span data-stu-id="968c2-128">The script updates the $Job variable by using existing value of $Job and the current cmdlet to get the current status of the job.</span></span>
<span data-ttu-id="968c2-129">Para obter informações sobre os cmdlets do Windows PowerShell, digite `Get-Help Write-Host` e `Get-Help Start-Sleep` .</span><span class="sxs-lookup"><span data-stu-id="968c2-129">For information about the Windows PowerShell cmdlets, type `Get-Help Write-Host` and `Get-Help Start-Sleep`.</span></span>
<span data-ttu-id="968c2-130">A linha final do script informa que o script foi concluído.</span><span class="sxs-lookup"><span data-stu-id="968c2-130">The final line of the script tells you that the script has finished.</span></span>

## <span data-ttu-id="968c2-131">OS</span><span class="sxs-lookup"><span data-stu-id="968c2-131">PARAMETERS</span></span>

### <span data-ttu-id="968c2-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="968c2-132">-DefaultProfile</span></span>
<span data-ttu-id="968c2-133">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="968c2-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="968c2-134">-De</span><span class="sxs-lookup"><span data-stu-id="968c2-134">-From</span></span>
<span data-ttu-id="968c2-135">Especifica o início, como um objeto **DateTime** , de um intervalo de tempo para os trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="968c2-135">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="968c2-136">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="968c2-136">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="968c2-137">Para obter mais informações sobre objetos **DateTime** , digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="968c2-137">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="968c2-138">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="968c2-138">-Job</span></span>
<span data-ttu-id="968c2-139">Especifica um trabalho que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="968c2-139">Specifies a job that this cmdlet gets.</span></span>
<span data-ttu-id="968c2-140">Para obter um objeto **AzureRmBackupJob** , use o cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="968c2-140">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="968c2-141">-JobId</span><span class="sxs-lookup"><span data-stu-id="968c2-141">-JobId</span></span>
<span data-ttu-id="968c2-142">Especifica a ID de um trabalho que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="968c2-142">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="968c2-143">A ID é a propriedade **InstanceId** de um objeto **AzureRmBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="968c2-143">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="968c2-144">Para obter um objeto **AzureRmBackupJob** , use Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="968c2-144">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

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

### <span data-ttu-id="968c2-145">-Operação</span><span class="sxs-lookup"><span data-stu-id="968c2-145">-Operation</span></span>
<span data-ttu-id="968c2-146">Especifica uma operação dos trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="968c2-146">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="968c2-147">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="968c2-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="968c2-148">Fazer</span><span class="sxs-lookup"><span data-stu-id="968c2-148">Backup</span></span> 
- <span data-ttu-id="968c2-149">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="968c2-149">ConfigureBackup</span></span> 
- <span data-ttu-id="968c2-150">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="968c2-150">DeleteBackupData</span></span> 
- <span data-ttu-id="968c2-151">Inscrição</span><span class="sxs-lookup"><span data-stu-id="968c2-151">Register</span></span> 
- <span data-ttu-id="968c2-152">Restaurar</span><span class="sxs-lookup"><span data-stu-id="968c2-152">Restore</span></span> 
- <span data-ttu-id="968c2-153">Desproteger</span><span class="sxs-lookup"><span data-stu-id="968c2-153">UnProtect</span></span> 
- <span data-ttu-id="968c2-154">Cancele</span><span class="sxs-lookup"><span data-stu-id="968c2-154">Unregister</span></span>

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

### <span data-ttu-id="968c2-155">-Status</span><span class="sxs-lookup"><span data-stu-id="968c2-155">-Status</span></span>
<span data-ttu-id="968c2-156">Especifica um status dos trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="968c2-156">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="968c2-157">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="968c2-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="968c2-158">InProgress</span><span class="sxs-lookup"><span data-stu-id="968c2-158">InProgress</span></span>
- <span data-ttu-id="968c2-159">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="968c2-159">Failed</span></span>
- <span data-ttu-id="968c2-160">Cela</span><span class="sxs-lookup"><span data-stu-id="968c2-160">Cancelled</span></span>
- <span data-ttu-id="968c2-161">Cancelamento</span><span class="sxs-lookup"><span data-stu-id="968c2-161">Cancelling</span></span>
- <span data-ttu-id="968c2-162">Feito</span><span class="sxs-lookup"><span data-stu-id="968c2-162">Completed</span></span>
- <span data-ttu-id="968c2-163">CompletedWithWarnings você pode especificar esse parâmetro para localizar todos os trabalhos em andamento ou todos os trabalhos com falha.</span><span class="sxs-lookup"><span data-stu-id="968c2-163">CompletedWithWarnings You can specify this parameter to find all in progress jobs or all failed jobs.</span></span>

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

### <span data-ttu-id="968c2-164">-To</span><span class="sxs-lookup"><span data-stu-id="968c2-164">-To</span></span>
<span data-ttu-id="968c2-165">Especifica o fim, como um objeto **DateTime** , de um intervalo de tempo para os trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="968c2-165">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="968c2-166">O valor padrão é a hora atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="968c2-166">The default value is the current system time.</span></span>
<span data-ttu-id="968c2-167">Se você especificar esse parâmetro, também deverá especificar o parâmetro *from* .</span><span class="sxs-lookup"><span data-stu-id="968c2-167">If you specify this parameter, you must also specify the *From* parameter.</span></span>

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

### <span data-ttu-id="968c2-168">-Digite</span><span class="sxs-lookup"><span data-stu-id="968c2-168">-Type</span></span>
<span data-ttu-id="968c2-169">Especifica o tipo de contêiner para o qual esse cmdlet obtém trabalhos de backup.</span><span class="sxs-lookup"><span data-stu-id="968c2-169">Specifies the type of container for which this cmdlet gets backup jobs.</span></span>
<span data-ttu-id="968c2-170">Atualmente, o único valor com suporte é AzureVM.</span><span class="sxs-lookup"><span data-stu-id="968c2-170">Currently, the only supported value is AzureVM.</span></span>

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

### <span data-ttu-id="968c2-171">-Cofre</span><span class="sxs-lookup"><span data-stu-id="968c2-171">-Vault</span></span>
<span data-ttu-id="968c2-172">Especifica o cofre de backup para o qual este cmdlet recebe trabalhos.</span><span class="sxs-lookup"><span data-stu-id="968c2-172">Specifies the Backup vault for which this cmdlet gets jobs.</span></span>
<span data-ttu-id="968c2-173">Para obter um objeto **AzureRmBackupVault** , use o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="968c2-173">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="968c2-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="968c2-174">CommonParameters</span></span>
<span data-ttu-id="968c2-175">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="968c2-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="968c2-176">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="968c2-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="968c2-177">SENSORES</span><span class="sxs-lookup"><span data-stu-id="968c2-177">INPUTS</span></span>

### <span data-ttu-id="968c2-178">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="968c2-178">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="968c2-179">Parâmetros: cofre (ByValue)</span><span class="sxs-lookup"><span data-stu-id="968c2-179">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="968c2-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="968c2-180">OUTPUTS</span></span>

### <span data-ttu-id="968c2-181">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="968c2-181">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="968c2-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="968c2-182">NOTES</span></span>
* <span data-ttu-id="968c2-183">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="968c2-183">None</span></span>

## <span data-ttu-id="968c2-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="968c2-184">RELATED LINKS</span></span>

[<span data-ttu-id="968c2-185">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="968c2-185">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="968c2-186">Parar-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="968c2-186">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)

[<span data-ttu-id="968c2-187">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="968c2-187">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


