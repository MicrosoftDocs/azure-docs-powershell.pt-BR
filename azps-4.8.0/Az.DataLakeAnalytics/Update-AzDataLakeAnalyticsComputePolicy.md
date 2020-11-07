---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 5dd36c9dbd263dc2e5c72cc6d57f95e29c456c41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947859"
---
# <span data-ttu-id="7f860-101">Update-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="7f860-101">Update-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="7f860-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f860-102">SYNOPSIS</span></span>
<span data-ttu-id="7f860-103">Atualiza uma regra de política de computação do data Lake Analytics para uma entidade AAD específica.</span><span class="sxs-lookup"><span data-stu-id="7f860-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="7f860-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f860-104">SYNTAX</span></span>

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f860-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f860-105">DESCRIPTION</span></span>
<span data-ttu-id="7f860-106">O **Update-AzDataLakeAnalyticsComputePolicy** atualiza a regra de política de computação especificada para uma entidade AAD específica em uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7f860-106">The **Update-AzDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="7f860-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f860-107">EXAMPLES</span></span>

### <span data-ttu-id="7f860-108">Exemplo 1: atualizar uma regra em uma política de computação</span><span class="sxs-lookup"><span data-stu-id="7f860-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="7f860-109">Esse comando atualiza uma política chamada "MyPolicy" na conta "contosoadla" para garantir que o usuário não possa enviar nenhum trabalho com mais de 5 unidades de análise.</span><span class="sxs-lookup"><span data-stu-id="7f860-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="7f860-110">Exemplo 2: criar uma política de computação com as duas regras Update</span><span class="sxs-lookup"><span data-stu-id="7f860-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="7f860-111">Esse comando cria uma política chamada "MyPolicy" na conta "contosoadla" para garantir que o usuário não possa enviar nenhum trabalho com mais de 5 unidades de análise ou com uma prioridade inferior a 100</span><span class="sxs-lookup"><span data-stu-id="7f860-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="7f860-112">OS</span><span class="sxs-lookup"><span data-stu-id="7f860-112">PARAMETERS</span></span>

### <span data-ttu-id="7f860-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="7f860-113">-Account</span></span>
<span data-ttu-id="7f860-114">Nome da conta na qual atualizar a política de computação.</span><span class="sxs-lookup"><span data-stu-id="7f860-114">Name of the account to update the compute policy in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f860-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f860-115">-DefaultProfile</span></span>
<span data-ttu-id="7f860-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7f860-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f860-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="7f860-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="7f860-118">O número máximo de unidades de análise permitidas por trabalho para esta política.</span><span class="sxs-lookup"><span data-stu-id="7f860-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="7f860-119">É preciso especificar o MinPriorityPerJob, a ou os dois parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7f860-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelismPerJob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f860-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="7f860-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="7f860-121">A prioridade mínima com suporte por trabalho para esta política.</span><span class="sxs-lookup"><span data-stu-id="7f860-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="7f860-122">É preciso especificar o MaxAnalyticsUnitsPerJob, a ou os dois parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7f860-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f860-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f860-123">-Name</span></span>
<span data-ttu-id="7f860-124">Nome da política de computação a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="7f860-124">Name of the compute policy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f860-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f860-125">-ResourceGroupName</span></span>
<span data-ttu-id="7f860-126">Nome do grupo de recursos sob o qual a conta existe.</span><span class="sxs-lookup"><span data-stu-id="7f860-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="7f860-127">Opcional e tentará descobrir, se não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="7f860-127">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f860-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7f860-128">-Confirm</span></span>
<span data-ttu-id="7f860-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f860-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f860-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f860-130">-WhatIf</span></span>
<span data-ttu-id="7f860-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7f860-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f860-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7f860-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f860-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f860-133">CommonParameters</span></span>
<span data-ttu-id="7f860-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f860-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f860-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f860-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f860-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f860-136">INPUTS</span></span>

### <span data-ttu-id="7f860-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7f860-137">System.String</span></span>

### <span data-ttu-id="7f860-138">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7f860-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7f860-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f860-139">OUTPUTS</span></span>

### <span data-ttu-id="7f860-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="7f860-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="7f860-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f860-141">NOTES</span></span>

## <span data-ttu-id="7f860-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f860-142">RELATED LINKS</span></span>
