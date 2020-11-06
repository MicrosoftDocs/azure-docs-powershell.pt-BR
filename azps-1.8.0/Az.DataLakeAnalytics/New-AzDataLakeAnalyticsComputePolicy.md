---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 3fbf0d09b2307d96512c04e13521544a69fcde8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601092"
---
# <span data-ttu-id="52906-101">New-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="52906-101">New-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="52906-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52906-102">SYNOPSIS</span></span>
<span data-ttu-id="52906-103">Cria uma regra de política de computação do data Lake Analytics para uma entidade AAD específica.</span><span class="sxs-lookup"><span data-stu-id="52906-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="52906-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52906-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52906-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52906-105">DESCRIPTION</span></span>
<span data-ttu-id="52906-106">O **New-AzDataLakeAnalyticsComputePolicy** cria a regra de política de computação especificada para uma entidade AAD específica em uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="52906-106">The **New-AzDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="52906-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52906-107">EXAMPLES</span></span>

### <span data-ttu-id="52906-108">Exemplo 1: criar uma política de computação com apenas uma regra</span><span class="sxs-lookup"><span data-stu-id="52906-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="52906-109">Esse comando cria uma política chamada "MyPolicy" na conta "contosoadla" para o usuário com ID "83cb7ad2-3523-4b82-b909-d478b0d8aea3" que garante que eles não podem enviar nenhum trabalho com mais de 5 unidades analíticos.</span><span class="sxs-lookup"><span data-stu-id="52906-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="52906-110">Exemplo 2: criar uma política de computação com as duas regras definidas</span><span class="sxs-lookup"><span data-stu-id="52906-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="52906-111">Esse comando cria uma política chamada "MyPolicy" na conta "contosoadla" para o usuário com ID "83cb7ad2-3523-4b82-b909-d478b0d8aea3" que garante que eles não podem enviar nenhum trabalho com mais de 5 unidades de análise ou com uma prioridade inferior a 100</span><span class="sxs-lookup"><span data-stu-id="52906-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="52906-112">OS</span><span class="sxs-lookup"><span data-stu-id="52906-112">PARAMETERS</span></span>

### <span data-ttu-id="52906-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="52906-113">-Account</span></span>
<span data-ttu-id="52906-114">Nome da conta para a qual a política de computação será adicionada.</span><span class="sxs-lookup"><span data-stu-id="52906-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="52906-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52906-115">-DefaultProfile</span></span>
<span data-ttu-id="52906-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="52906-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52906-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="52906-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="52906-118">O número máximo de unidades de análise permitidas por trabalho para esta política.</span><span class="sxs-lookup"><span data-stu-id="52906-118">The maximum supported analytics units per job for this policy.</span></span>
<span data-ttu-id="52906-119">É preciso especificar o MinPriorityPerJob, a ou os dois parâmetros.</span><span class="sxs-lookup"><span data-stu-id="52906-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="52906-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="52906-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="52906-121">A prioridade mínima com suporte por trabalho para esta política.</span><span class="sxs-lookup"><span data-stu-id="52906-121">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="52906-122">É preciso especificar o MaxAnalyticsUnitsPerJob, a ou os dois parâmetros.</span><span class="sxs-lookup"><span data-stu-id="52906-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="52906-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="52906-123">-Name</span></span>
<span data-ttu-id="52906-124">Nome da política de computação a ser criada.</span><span class="sxs-lookup"><span data-stu-id="52906-124">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="52906-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="52906-125">-ObjectId</span></span>
<span data-ttu-id="52906-126">A ID de objeto do Azure Active Directory para o usuário ou grupo ao qual a política será aplicada.</span><span class="sxs-lookup"><span data-stu-id="52906-126">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

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

### <span data-ttu-id="52906-127">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="52906-127">-ObjectType</span></span>
<span data-ttu-id="52906-128">O tipo de objeto do Azure Active Directory para a identificação do objeto passado.</span><span class="sxs-lookup"><span data-stu-id="52906-128">The Azure Active Directory object type for the object ID passed in.</span></span>

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

### <span data-ttu-id="52906-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52906-129">-ResourceGroupName</span></span>
<span data-ttu-id="52906-130">Nome do grupo de recursos sob o qual a conta existe.</span><span class="sxs-lookup"><span data-stu-id="52906-130">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="52906-131">Opcional e tentará descobrir, se não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="52906-131">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="52906-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52906-132">-Confirm</span></span>
<span data-ttu-id="52906-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52906-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52906-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52906-134">-WhatIf</span></span>
<span data-ttu-id="52906-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52906-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52906-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52906-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52906-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52906-137">CommonParameters</span></span>
<span data-ttu-id="52906-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52906-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52906-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52906-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52906-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52906-140">INPUTS</span></span>

### <span data-ttu-id="52906-141">System. String</span><span class="sxs-lookup"><span data-stu-id="52906-141">System.String</span></span>

### <span data-ttu-id="52906-142">System. GUID</span><span class="sxs-lookup"><span data-stu-id="52906-142">System.Guid</span></span>

### <span data-ttu-id="52906-143">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="52906-143">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="52906-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52906-144">OUTPUTS</span></span>

### <span data-ttu-id="52906-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="52906-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="52906-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52906-146">NOTES</span></span>

## <span data-ttu-id="52906-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52906-147">RELATED LINKS</span></span>
