---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/update-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 176a23a1909d5e7d1498add0e394311703106a7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431011"
---
# <span data-ttu-id="1f523-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="1f523-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="1f523-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f523-102">SYNOPSIS</span></span>
<span data-ttu-id="1f523-103">Atualiza uma regra de política de computação do data Lake Analytics para uma entidade AAD específica.</span><span class="sxs-lookup"><span data-stu-id="1f523-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f523-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f523-104">SYNTAX</span></span>

```
Update-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f523-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f523-105">DESCRIPTION</span></span>
<span data-ttu-id="1f523-106">O **Update-AzureRmDataLakeAnalyticsComputePolicy** atualiza a regra de política de computação especificada para uma entidade AAD específica em uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1f523-106">The **Update-AzureRmDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="1f523-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f523-107">EXAMPLES</span></span>

### <span data-ttu-id="1f523-108">Exemplo 1: atualizar uma regra em uma política de computação</span><span class="sxs-lookup"><span data-stu-id="1f523-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="1f523-109">Esse comando atualiza uma política chamada "MyPolicy" na conta "contosoadla" para garantir que o usuário não possa enviar nenhum trabalho com mais de 5 unidades de análise.</span><span class="sxs-lookup"><span data-stu-id="1f523-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="1f523-110">Exemplo 2: criar uma política de computação com as duas regras Update</span><span class="sxs-lookup"><span data-stu-id="1f523-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="1f523-111">Esse comando cria uma política chamada "MyPolicy" na conta "contosoadla" para garantir que o usuário não possa enviar nenhum trabalho com mais de 5 unidades de análise ou com uma prioridade inferior a 100</span><span class="sxs-lookup"><span data-stu-id="1f523-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="1f523-112">OS</span><span class="sxs-lookup"><span data-stu-id="1f523-112">PARAMETERS</span></span>

### <span data-ttu-id="1f523-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="1f523-113">-Account</span></span>
<span data-ttu-id="1f523-114">Nome da conta na qual atualizar a política de computação.</span><span class="sxs-lookup"><span data-stu-id="1f523-114">Name of the account to update the compute policy in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f523-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f523-115">-DefaultProfile</span></span>
<span data-ttu-id="1f523-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1f523-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f523-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="1f523-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="1f523-118">O número máximo de unidades de análise permitidas por trabalho para esta política.</span><span class="sxs-lookup"><span data-stu-id="1f523-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="1f523-119">É preciso especificar o MinPriorityPerJob, a ou os dois parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1f523-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelismPerJob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f523-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="1f523-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="1f523-121">A prioridade mínima com suporte por trabalho para esta política.</span><span class="sxs-lookup"><span data-stu-id="1f523-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="1f523-122">É preciso especificar o MaxAnalyticsUnitsPerJob, a ou os dois parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1f523-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f523-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f523-123">-Name</span></span>
<span data-ttu-id="1f523-124">Nome da política de computação a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="1f523-124">Name of the compute policy to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f523-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f523-125">-ResourceGroupName</span></span>
<span data-ttu-id="1f523-126">Nome do grupo de recursos sob o qual a conta existe.</span><span class="sxs-lookup"><span data-stu-id="1f523-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="1f523-127">Opcional e tentará descobrir, se não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="1f523-127">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f523-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1f523-128">-Confirm</span></span>
<span data-ttu-id="1f523-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f523-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f523-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f523-130">-WhatIf</span></span>
<span data-ttu-id="1f523-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1f523-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f523-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f523-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f523-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f523-133">CommonParameters</span></span>
<span data-ttu-id="1f523-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f523-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f523-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f523-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f523-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f523-136">INPUTS</span></span>

### <span data-ttu-id="1f523-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1f523-137">System.String</span></span>
<span data-ttu-id="1f523-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1f523-138">System.Int32</span></span>

## <span data-ttu-id="1f523-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f523-139">OUTPUTS</span></span>

### <span data-ttu-id="1f523-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="1f523-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="1f523-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f523-141">NOTES</span></span>

## <span data-ttu-id="1f523-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f523-142">RELATED LINKS</span></span>

