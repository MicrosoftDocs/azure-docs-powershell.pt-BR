---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 7cd9231134b7b78d51a9a86777c54dd99e1ffa90
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889988"
---
# <span data-ttu-id="4ef22-101">New-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="4ef22-101">New-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="4ef22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ef22-102">SYNOPSIS</span></span>
<span data-ttu-id="4ef22-103">Cria uma regra de política de computação do Data Lake Analytics para uma entidade AAD específica.</span><span class="sxs-lookup"><span data-stu-id="4ef22-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="4ef22-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4ef22-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ef22-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4ef22-105">DESCRIPTION</span></span>
<span data-ttu-id="4ef22-106">O **New-AzDataLakeAnalyticsComputePolicy** cria a regra de política de computação especificada para uma entidade AAD específica em uma conta do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4ef22-106">The **New-AzDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="4ef22-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ef22-107">EXAMPLES</span></span>

### <span data-ttu-id="4ef22-108">Exemplo 1: Criar uma política de computação com apenas uma regra</span><span class="sxs-lookup"><span data-stu-id="4ef22-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="4ef22-109">Este comando cria uma política chamada "myPolicy" na conta "contosoadla" para o usuário com a id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" que garante que ele não pode enviar qualquer trabalho com mais de 5 unidades de análise.</span><span class="sxs-lookup"><span data-stu-id="4ef22-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="4ef22-110">Exemplo 2: Criar uma política de computação com ambas as regras definidas</span><span class="sxs-lookup"><span data-stu-id="4ef22-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="4ef22-111">Este comando cria uma política chamada "myPolicy" na conta "contosoadla" para o usuário com id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" que garante que não possa enviar qualquer trabalho com mais de 5 unidades de análise ou com prioridade inferior a 100</span><span class="sxs-lookup"><span data-stu-id="4ef22-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="4ef22-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4ef22-112">PARAMETERS</span></span>

### <span data-ttu-id="4ef22-113">-Account</span><span class="sxs-lookup"><span data-stu-id="4ef22-113">-Account</span></span>
<span data-ttu-id="4ef22-114">Nome da conta para adicionar a política de computação.</span><span class="sxs-lookup"><span data-stu-id="4ef22-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="4ef22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ef22-115">-DefaultProfile</span></span>
<span data-ttu-id="4ef22-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4ef22-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ef22-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="4ef22-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="4ef22-118">As unidades de análise máximas suportadas por trabalho para esta política.</span><span class="sxs-lookup"><span data-stu-id="4ef22-118">The maximum supported analytics units per job for this policy.</span></span>
<span data-ttu-id="4ef22-119">Isso, MinPriorityPerJob ou ambos os parâmetros devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="4ef22-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="4ef22-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="4ef22-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="4ef22-121">A prioridade mínima suportada por trabalho para essa política.</span><span class="sxs-lookup"><span data-stu-id="4ef22-121">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="4ef22-122">Isso, MaxAnalyticsUnitsPerJob ou ambos os parâmetros devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="4ef22-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="4ef22-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4ef22-123">-Name</span></span>
<span data-ttu-id="4ef22-124">Nome da política de computação a ser criado.</span><span class="sxs-lookup"><span data-stu-id="4ef22-124">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="4ef22-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4ef22-125">-ObjectId</span></span>
<span data-ttu-id="4ef22-126">A ID de objeto do Azure Active Directory para o usuário ou grupo ao qual aplicar a política.</span><span class="sxs-lookup"><span data-stu-id="4ef22-126">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef22-127">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="4ef22-127">-ObjectType</span></span>
<span data-ttu-id="4ef22-128">O tipo de objeto do Azure Active Directory para a ID de objeto passada.</span><span class="sxs-lookup"><span data-stu-id="4ef22-128">The Azure Active Directory object type for the object ID passed in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, ServicePrincipal

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef22-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ef22-129">-ResourceGroupName</span></span>
<span data-ttu-id="4ef22-130">Nome do grupo de recursos no qual você a conta existe.</span><span class="sxs-lookup"><span data-stu-id="4ef22-130">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="4ef22-131">Opcional e tentará descobrir se não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="4ef22-131">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="4ef22-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ef22-132">-Confirm</span></span>
<span data-ttu-id="4ef22-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ef22-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ef22-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ef22-134">-WhatIf</span></span>
<span data-ttu-id="4ef22-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4ef22-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ef22-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4ef22-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ef22-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ef22-137">CommonParameters</span></span>
<span data-ttu-id="4ef22-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ef22-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ef22-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ef22-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ef22-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ef22-140">INPUTS</span></span>

### <span data-ttu-id="4ef22-141">System.String</span><span class="sxs-lookup"><span data-stu-id="4ef22-141">System.String</span></span>

### <span data-ttu-id="4ef22-142">System.Guid</span><span class="sxs-lookup"><span data-stu-id="4ef22-142">System.Guid</span></span>

### <span data-ttu-id="4ef22-143">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4ef22-143">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4ef22-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4ef22-144">OUTPUTS</span></span>

### <span data-ttu-id="4ef22-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="4ef22-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="4ef22-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="4ef22-146">NOTES</span></span>

## <span data-ttu-id="4ef22-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ef22-147">RELATED LINKS</span></span>
