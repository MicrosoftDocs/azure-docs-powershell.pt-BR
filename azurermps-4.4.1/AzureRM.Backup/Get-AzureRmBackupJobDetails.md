---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6187F603-5298-4854-94F3-0C38FCF3125F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
ms.openlocfilehash: f9f0808db919ad5d1d38b29daa720fb9b8a5baee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428291"
---
# <span data-ttu-id="2ecc0-101">Get-AzureRmBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="2ecc0-101">Get-AzureRmBackupJobDetails</span></span>

## <span data-ttu-id="2ecc0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2ecc0-102">SYNOPSIS</span></span>
<span data-ttu-id="2ecc0-103">Obtém os detalhes de um trabalho de backup.</span><span class="sxs-lookup"><span data-stu-id="2ecc0-103">Gets the details of a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ecc0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ecc0-104">SYNTAX</span></span>

### <span data-ttu-id="2ecc0-105">JobsFiltersSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2ecc0-105">JobsFiltersSet (Default)</span></span>
```
Get-AzureRmBackupJobDetails -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ecc0-106">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="2ecc0-106">IdFiltersSet</span></span>
```
Get-AzureRmBackupJobDetails -Vault <AzureRMBackupVault> -JobId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ecc0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2ecc0-107">DESCRIPTION</span></span>
<span data-ttu-id="2ecc0-108">O cmdlet **Get-AzureRmBackupJobDetails** Obtém os detalhes de um trabalho de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="2ecc0-108">The **Get-AzureRmBackupJobDetails** cmdlet gets the details of an Azure Backup job.</span></span>
<span data-ttu-id="2ecc0-109">Você pode usar esse cmdlet para coletar informações sobre um trabalho que falha.</span><span class="sxs-lookup"><span data-stu-id="2ecc0-109">You can use this cmdlet to gather information about a job that fails.</span></span>

## <span data-ttu-id="2ecc0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ecc0-110">EXAMPLES</span></span>

### <span data-ttu-id="2ecc0-111">Exemplo 1: exibir os detalhes de um trabalho com falha</span><span class="sxs-lookup"><span data-stu-id="2ecc0-111">Example 1: Display the details of a failed job</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Jobs = Get-AzureRmBackupJob -Vault $Vault -Status Failed
PS C:\> $JobDetails = Get-AzureRmBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
ErrorCode ErrorMessage                            Recommendations
--------- ------------                            ---------------
   400001 Command execution failed.               {Another operation is currently in p...
```

<span data-ttu-id="2ecc0-112">O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="2ecc0-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="2ecc0-113">O comando armazena esse objeto na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="2ecc0-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="2ecc0-114">O segundo comando obtém trabalhos com falha do cofre no $Vault e, em seguida, os armazena na variável de matriz $Jobs.</span><span class="sxs-lookup"><span data-stu-id="2ecc0-114">The second command gets failed jobs from the vault in $Vault, and then stores them in the $Jobs array variable.</span></span>

<span data-ttu-id="2ecc0-115">O terceiro trabalho obtém detalhes do primeiro trabalho na variável $Jobs e, em seguida, armazena esses detalhes na variável $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="2ecc0-115">The third job gets details for the first job in the $Jobs variable, and then stores those details in the $JobDetails variable.</span></span>

<span data-ttu-id="2ecc0-116">O comando final exibe a propriedade **ErrorDetails** de $JobDetails usando a sintaxe de pontos padrão.</span><span class="sxs-lookup"><span data-stu-id="2ecc0-116">The final command displays the **ErrorDetails** property of $JobDetails by using standard dot syntax.</span></span>

### <span data-ttu-id="2ecc0-117">Exemplo 2: exibir a ação recomendada para um trabalho com falha</span><span class="sxs-lookup"><span data-stu-id="2ecc0-117">Example 2: Display the recommended action for a failed job</span></span>
```
PS C:\>$JobDetails.ErrorDetails.Recommendations
Another operation is currently in progress on this item. Please wait until the previous operation is completed, and then retry.
```

<span data-ttu-id="2ecc0-118">Esse comando exibe a ação recomendada da variável $JobDetails que foi criada no primeiro exemplo.</span><span class="sxs-lookup"><span data-stu-id="2ecc0-118">This command displays the recommended action from the $JobDetails variable that was created in the first example.</span></span>

## <span data-ttu-id="2ecc0-119">OS</span><span class="sxs-lookup"><span data-stu-id="2ecc0-119">PARAMETERS</span></span>

### <span data-ttu-id="2ecc0-120">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="2ecc0-120">-Job</span></span>
<span data-ttu-id="2ecc0-121">Especifica um trabalho para o qual este cmdlet obtém detalhes.</span><span class="sxs-lookup"><span data-stu-id="2ecc0-121">Specifies a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="2ecc0-122">Para obter um objeto **AzureRmBackupJob** , use o cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="2ecc0-122">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ecc0-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="2ecc0-123">-JobId</span></span>
<span data-ttu-id="2ecc0-124">Especifica a ID de um trabalho para o qual esse cmdlet obtém detalhes.</span><span class="sxs-lookup"><span data-stu-id="2ecc0-124">Specifies the ID of a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="2ecc0-125">A ID é a propriedade **InstanceId** de um objeto **AzureRmBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="2ecc0-125">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="2ecc0-126">Para obter um objeto **AzureRmBackupJob** , use Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="2ecc0-126">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

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

### <span data-ttu-id="2ecc0-127">-Cofre</span><span class="sxs-lookup"><span data-stu-id="2ecc0-127">-Vault</span></span>
<span data-ttu-id="2ecc0-128">Especifica o cofre de backup para o qual este cmdlet obtém detalhes do trabalho.</span><span class="sxs-lookup"><span data-stu-id="2ecc0-128">Specifies the Backup vault for which this cmdlet gets job details.</span></span>
<span data-ttu-id="2ecc0-129">Para obter um objeto **AzureRmBackupVault** , use o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="2ecc0-129">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="2ecc0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ecc0-130">-DefaultProfile</span></span>
<span data-ttu-id="2ecc0-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2ecc0-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ecc0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ecc0-132">CommonParameters</span></span>
<span data-ttu-id="2ecc0-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ecc0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ecc0-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ecc0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ecc0-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2ecc0-135">INPUTS</span></span>

### <span data-ttu-id="2ecc0-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2ecc0-136">None</span></span>

## <span data-ttu-id="2ecc0-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2ecc0-137">OUTPUTS</span></span>

### <span data-ttu-id="2ecc0-138">AzureRmBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="2ecc0-138">AzureRmBackupJobDetails</span></span>

## <span data-ttu-id="2ecc0-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2ecc0-139">NOTES</span></span>
* <span data-ttu-id="2ecc0-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2ecc0-140">None</span></span>

## <span data-ttu-id="2ecc0-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ecc0-141">RELATED LINKS</span></span>

[<span data-ttu-id="2ecc0-142">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="2ecc0-142">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="2ecc0-143">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="2ecc0-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


