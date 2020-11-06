---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 67cffe7f0cdaebc655eb98321166bb7805844a5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439956"
---
# <span data-ttu-id="c3f09-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="c3f09-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="c3f09-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3f09-102">SYNOPSIS</span></span>
<span data-ttu-id="c3f09-103">Atualiza uma regra de política de computação do data Lake Analytics para uma entidade AAD específica.</span><span class="sxs-lookup"><span data-stu-id="c3f09-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3f09-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3f09-104">SYNTAX</span></span>

```
Update-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxDegreeOfParallelismPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3f09-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3f09-105">DESCRIPTION</span></span>
<span data-ttu-id="c3f09-106">O **Update-AzureRmDataLakeAnalyticsComputePolicy** atualiza a regra de política de computação especificada para uma entidade AAD específica em uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c3f09-106">The **Update-AzureRmDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="c3f09-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3f09-107">EXAMPLES</span></span>

### <span data-ttu-id="c3f09-108">Exemplo 1: atualizar uma regra em uma política de computação</span><span class="sxs-lookup"><span data-stu-id="c3f09-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxDegreeOfParallelismPerJob 5
```

<span data-ttu-id="c3f09-109">Esse comando atualiza uma política chamada "MyPolicy" na conta "contosoadla" para garantir que o usuário não possa enviar qualquer trabalho com mais de 5 paralelismo.</span><span class="sxs-lookup"><span data-stu-id="c3f09-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 parallelism.</span></span>

### <span data-ttu-id="c3f09-110">Exemplo 2: criar uma política de computação com as duas regras Update</span><span class="sxs-lookup"><span data-stu-id="c3f09-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxDegreeOfParallelismPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="c3f09-111">Esse comando cria uma política chamada "MyPolicy" na conta "contosoadla" para garantir que o usuário não possa enviar qualquer trabalho com mais de 5 paralelismo ou com uma prioridade inferior a 100</span><span class="sxs-lookup"><span data-stu-id="c3f09-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 parallelism or with a priority lower than 100</span></span>

## <span data-ttu-id="c3f09-112">OS</span><span class="sxs-lookup"><span data-stu-id="c3f09-112">PARAMETERS</span></span>

### <span data-ttu-id="c3f09-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="c3f09-113">-Account</span></span>
<span data-ttu-id="c3f09-114">Nome da conta na qual atualizar a política de computação.</span><span class="sxs-lookup"><span data-stu-id="c3f09-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="c3f09-115">-MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="c3f09-115">-MaxDegreeOfParallelismPerJob</span></span>
<span data-ttu-id="c3f09-116">O grau máximo de suporte de paralelismo por trabalho para esta política.</span><span class="sxs-lookup"><span data-stu-id="c3f09-116">The maximum supported degree of parallelism per job for this policy.</span></span> <span data-ttu-id="c3f09-117">É preciso especificar o MinPriorityPerJob, a ou os dois parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c3f09-117">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="c3f09-118">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="c3f09-118">-MinPriorityPerJob</span></span>
<span data-ttu-id="c3f09-119">A prioridade mínima com suporte por trabalho para esta política.</span><span class="sxs-lookup"><span data-stu-id="c3f09-119">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="c3f09-120">É preciso especificar o MaxDegreeOfParallelismPerJob, a ou os dois parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c3f09-120">Either this, MaxDegreeOfParallelismPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="c3f09-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3f09-121">-Name</span></span>
<span data-ttu-id="c3f09-122">Nome da política de computação a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="c3f09-122">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="c3f09-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3f09-123">-ResourceGroupName</span></span>
<span data-ttu-id="c3f09-124">Nome do grupo de recursos sob o qual a conta existe.</span><span class="sxs-lookup"><span data-stu-id="c3f09-124">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="c3f09-125">Opcional e tentará descobrir, se não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="c3f09-125">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="c3f09-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c3f09-126">-Confirm</span></span>
<span data-ttu-id="c3f09-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3f09-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3f09-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3f09-128">-WhatIf</span></span>
<span data-ttu-id="c3f09-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c3f09-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3f09-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c3f09-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3f09-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3f09-131">-DefaultProfile</span></span>
<span data-ttu-id="c3f09-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3f09-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3f09-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3f09-133">CommonParameters</span></span>
<span data-ttu-id="c3f09-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3f09-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3f09-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3f09-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3f09-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3f09-136">INPUTS</span></span>

### <span data-ttu-id="c3f09-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c3f09-137">System.String</span></span>
<span data-ttu-id="c3f09-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c3f09-138">System.Int32</span></span>

## <span data-ttu-id="c3f09-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3f09-139">OUTPUTS</span></span>

### <span data-ttu-id="c3f09-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="c3f09-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="c3f09-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3f09-141">NOTES</span></span>

## <span data-ttu-id="c3f09-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3f09-142">RELATED LINKS</span></span>

