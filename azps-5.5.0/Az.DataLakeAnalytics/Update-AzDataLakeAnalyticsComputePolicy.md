---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 5dd36c9dbd263dc2e5c72cc6d57f95e29c456c41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111946"
---
# <span data-ttu-id="14ccb-101">Update-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="14ccb-101">Update-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="14ccb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="14ccb-103">Atualiza uma regra de política de computação do Data Lake Analytics para uma entidade AAD específica.</span><span class="sxs-lookup"><span data-stu-id="14ccb-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="14ccb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14ccb-104">SYNTAX</span></span>

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14ccb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="14ccb-105">DESCRIPTION</span></span>
<span data-ttu-id="14ccb-106">O **Update-AzDataLakeAnalyticsComputePolicy** atualiza a regra de política de computação especificada para uma entidade específica do AAD em uma conta do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="14ccb-106">The **Update-AzDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="14ccb-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="14ccb-107">EXAMPLES</span></span>

### <span data-ttu-id="14ccb-108">Exemplo 1: atualizar uma regra em uma política de computação</span><span class="sxs-lookup"><span data-stu-id="14ccb-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="14ccb-109">Esse comando atualiza uma política chamada "myPolicy" na conta "contosoadla" para garantir que o usuário não possa enviar nenhum trabalho com mais de 5 unidades de análise.</span><span class="sxs-lookup"><span data-stu-id="14ccb-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="14ccb-110">Exemplo 2: Criar uma política de computação com a atualização de ambas as regras</span><span class="sxs-lookup"><span data-stu-id="14ccb-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="14ccb-111">Esse comando cria uma política chamada "myPolicy" na conta "contosoadla" para garantir que o usuário não possa enviar nenhum trabalho com mais de 5 unidades de análise ou com uma prioridade inferior a 100</span><span class="sxs-lookup"><span data-stu-id="14ccb-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="14ccb-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14ccb-112">PARAMETERS</span></span>

### <span data-ttu-id="14ccb-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="14ccb-113">-Account</span></span>
<span data-ttu-id="14ccb-114">Nome da conta para atualizar a política de computação.</span><span class="sxs-lookup"><span data-stu-id="14ccb-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="14ccb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14ccb-115">-DefaultProfile</span></span>
<span data-ttu-id="14ccb-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="14ccb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14ccb-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="14ccb-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="14ccb-118">As unidades de análise máximas com suporte por trabalho para esta política.</span><span class="sxs-lookup"><span data-stu-id="14ccb-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="14ccb-119">Tanto isso, MinPriorityPerJob, quanto ambos os parâmetros devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="14ccb-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="14ccb-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="14ccb-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="14ccb-121">A prioridade mínima com suporte por trabalho para essa política.</span><span class="sxs-lookup"><span data-stu-id="14ccb-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="14ccb-122">Tanto isso, MaxAnalyticsUnitsPerJob, quanto ambos os parâmetros devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="14ccb-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="14ccb-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="14ccb-123">-Name</span></span>
<span data-ttu-id="14ccb-124">Nome da política de computação a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="14ccb-124">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="14ccb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14ccb-125">-ResourceGroupName</span></span>
<span data-ttu-id="14ccb-126">Nome do grupo de recursos no qual a conta existe.</span><span class="sxs-lookup"><span data-stu-id="14ccb-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="14ccb-127">Opcional e tentará descobrir se não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="14ccb-127">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="14ccb-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="14ccb-128">-Confirm</span></span>
<span data-ttu-id="14ccb-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14ccb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14ccb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14ccb-130">-WhatIf</span></span>
<span data-ttu-id="14ccb-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="14ccb-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14ccb-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14ccb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14ccb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14ccb-133">CommonParameters</span></span>
<span data-ttu-id="14ccb-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14ccb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14ccb-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14ccb-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14ccb-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="14ccb-136">INPUTS</span></span>

### <span data-ttu-id="14ccb-137">System.String</span><span class="sxs-lookup"><span data-stu-id="14ccb-137">System.String</span></span>

### <span data-ttu-id="14ccb-138">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="14ccb-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="14ccb-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="14ccb-139">OUTPUTS</span></span>

### <span data-ttu-id="14ccb-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="14ccb-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="14ccb-141">Notas</span><span class="sxs-lookup"><span data-stu-id="14ccb-141">NOTES</span></span>

## <span data-ttu-id="14ccb-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14ccb-142">RELATED LINKS</span></span>
