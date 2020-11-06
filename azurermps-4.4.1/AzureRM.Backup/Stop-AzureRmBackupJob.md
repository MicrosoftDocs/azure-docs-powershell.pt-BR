---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 44C5AF58-ADC1-4BC6-9771-3FD8F0480106
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
ms.openlocfilehash: d502596b8c5ddde576b5fd22ee31398b2c4e869a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440696"
---
# <span data-ttu-id="64ebd-101">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="64ebd-101">Stop-AzureRmBackupJob</span></span>

## <span data-ttu-id="64ebd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="64ebd-103">Cancela um trabalho de backup existente.</span><span class="sxs-lookup"><span data-stu-id="64ebd-103">Cancels an existing Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64ebd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64ebd-104">SYNTAX</span></span>

### <span data-ttu-id="64ebd-105">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="64ebd-105">IdFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Vault <AzureRMBackupVault> -JobID <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64ebd-106">JobFiltersSet</span><span class="sxs-lookup"><span data-stu-id="64ebd-106">JobFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64ebd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64ebd-107">DESCRIPTION</span></span>
<span data-ttu-id="64ebd-108">O cmdlet **Stop-AzureRmBackupJob** cancela um trabalho de backup do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="64ebd-108">The **Stop-AzureRmBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="64ebd-109">Use esse parâmetro para interromper um trabalho que leve muito tempo e bloqueie outras atividades.</span><span class="sxs-lookup"><span data-stu-id="64ebd-109">Use this parameter to stop a job that takes too long and blocks other activities.</span></span>

<span data-ttu-id="64ebd-110">Você só pode cancelar os seguintes tipos de trabalho:</span><span class="sxs-lookup"><span data-stu-id="64ebd-110">You can cancel only the following types of jobs:</span></span> 

- <span data-ttu-id="64ebd-111">Fazer</span><span class="sxs-lookup"><span data-stu-id="64ebd-111">Backup</span></span>
- <span data-ttu-id="64ebd-112">Restaurar</span><span class="sxs-lookup"><span data-stu-id="64ebd-112">Restore</span></span>

## <span data-ttu-id="64ebd-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64ebd-113">EXAMPLES</span></span>

### <span data-ttu-id="64ebd-114">Exemplo 1: parar um trabalho de backup usando uma ID do trabalho</span><span class="sxs-lookup"><span data-stu-id="64ebd-114">Example 1: Stop a backup job by using a job ID</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Job = Get-AzureRmBackupJob -Vault $Vault -Operation Backup
PS C:\> Stop-AzureRmBackupJob -Vault $Vault -JobID $Job.InstanceId
```

<span data-ttu-id="64ebd-115">O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="64ebd-115">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="64ebd-116">O comando armazena esse objeto na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="64ebd-116">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="64ebd-117">O segundo comando obtém um trabalho de backup do cofre no $Vault usando o cmdlet **Get-AzureRmBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="64ebd-117">The second command gets a backup job from the vault in $Vault by using the **Get-AzureRmBackupJob** cmdlet.</span></span>
<span data-ttu-id="64ebd-118">O comando armazena o trabalho na variável $Job.</span><span class="sxs-lookup"><span data-stu-id="64ebd-118">The command stores the job in the $Job variable.</span></span>
<span data-ttu-id="64ebd-119">Neste exemplo, há apenas uma operação de backup no cofre especificado.</span><span class="sxs-lookup"><span data-stu-id="64ebd-119">In this example, there is only one backup operation in the specified vault.</span></span>

<span data-ttu-id="64ebd-120">O comando final interrompe o trabalho que tem a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="64ebd-120">The final command stops the job that has the specified ID.</span></span>

### <span data-ttu-id="64ebd-121">Exemplo 2: interromper todas as operações de restauração</span><span class="sxs-lookup"><span data-stu-id="64ebd-121">Example 2: Stop all Restore operations</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Operation Restore | Stop-AzureRmBackupJob
```

<span data-ttu-id="64ebd-122">Esse comando obtém todas as operações de restauração no cofre no $Vault e, em seguida, passa-as para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="64ebd-122">This command gets all the restore operations in the vault in $Vault, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="64ebd-123">O cmdlet atual interrompe cada trabalho.</span><span class="sxs-lookup"><span data-stu-id="64ebd-123">The current cmdlet stops each job.</span></span>

## <span data-ttu-id="64ebd-124">OS</span><span class="sxs-lookup"><span data-stu-id="64ebd-124">PARAMETERS</span></span>

### <span data-ttu-id="64ebd-125">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="64ebd-125">-Job</span></span>
<span data-ttu-id="64ebd-126">Especifica um trabalho cancelado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64ebd-126">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="64ebd-127">Para obter um objeto **AzureRmBackupJob** , use o cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="64ebd-127">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64ebd-128">-JobID</span><span class="sxs-lookup"><span data-stu-id="64ebd-128">-JobID</span></span>
<span data-ttu-id="64ebd-129">Especifica um trabalho cancelado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64ebd-129">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="64ebd-130">Para obter um objeto **AzureRmBackupJob** , use o cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="64ebd-130">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ebd-131">-Cofre</span><span class="sxs-lookup"><span data-stu-id="64ebd-131">-Vault</span></span>
<span data-ttu-id="64ebd-132">Especifica o cofre de backup em que esse cmdlet cancela um trabalho.</span><span class="sxs-lookup"><span data-stu-id="64ebd-132">Specifies the Backup vault in which this cmdlet cancels a job.</span></span>
<span data-ttu-id="64ebd-133">Para obter um objeto **AzureRmBackupVault** , use o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="64ebd-133">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ebd-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64ebd-134">-DefaultProfile</span></span>
<span data-ttu-id="64ebd-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64ebd-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64ebd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64ebd-136">CommonParameters</span></span>
<span data-ttu-id="64ebd-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64ebd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64ebd-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64ebd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64ebd-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64ebd-139">INPUTS</span></span>

### <span data-ttu-id="64ebd-140">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="64ebd-140">AzureRmBackupJob</span></span>

## <span data-ttu-id="64ebd-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64ebd-141">OUTPUTS</span></span>

### <span data-ttu-id="64ebd-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="64ebd-142">None</span></span>

## <span data-ttu-id="64ebd-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64ebd-143">NOTES</span></span>

## <span data-ttu-id="64ebd-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64ebd-144">RELATED LINKS</span></span>

[<span data-ttu-id="64ebd-145">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="64ebd-145">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="64ebd-146">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="64ebd-146">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="64ebd-147">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="64ebd-147">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


