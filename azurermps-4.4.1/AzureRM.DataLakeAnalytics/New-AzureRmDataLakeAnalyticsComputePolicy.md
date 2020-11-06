---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 1dfd9c4d55c9898ce9f4b656f53d7606ced11359
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427958"
---
# <span data-ttu-id="53056-101">New-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="53056-101">New-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="53056-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53056-102">SYNOPSIS</span></span>
<span data-ttu-id="53056-103">Cria uma regra de política de computação do data Lake Analytics para uma entidade AAD específica.</span><span class="sxs-lookup"><span data-stu-id="53056-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53056-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53056-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxDegreeOfParallelismPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53056-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53056-105">DESCRIPTION</span></span>
<span data-ttu-id="53056-106">O **New-AzureRmDataLakeAnalyticsComputePolicy** cria a regra de política de computação especificada para uma entidade AAD específica em uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="53056-106">The **New-AzureRmDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="53056-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53056-107">EXAMPLES</span></span>

### <span data-ttu-id="53056-108">Exemplo 1: criar uma política de computação com apenas uma regra</span><span class="sxs-lookup"><span data-stu-id="53056-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5
```

<span data-ttu-id="53056-109">Esse comando cria uma política chamada "MyPolicy" na conta "contosoadla" para o usuário com ID "83cb7ad2-3523-4b82-b909-d478b0d8aea3" que garante que eles não podem enviar nenhum trabalho com mais de 5 paralelismo.</span><span class="sxs-lookup"><span data-stu-id="53056-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 parallelism.</span></span>

### <span data-ttu-id="53056-110">Exemplo 2: criar uma política de computação com as duas regras definidas</span><span class="sxs-lookup"><span data-stu-id="53056-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="53056-111">Esse comando cria uma política chamada "MyPolicy" na conta "contosoadla" para o usuário com ID "83cb7ad2-3523-4b82-b909-d478b0d8aea3" que garante que eles não podem enviar qualquer trabalho com mais de 5 paralelismo ou com uma prioridade inferior a 100</span><span class="sxs-lookup"><span data-stu-id="53056-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 parallelism or with a priority lower than 100</span></span>

## <span data-ttu-id="53056-112">OS</span><span class="sxs-lookup"><span data-stu-id="53056-112">PARAMETERS</span></span>

### <span data-ttu-id="53056-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="53056-113">-Account</span></span>
<span data-ttu-id="53056-114">Nome da conta para a qual a política de computação será adicionada.</span><span class="sxs-lookup"><span data-stu-id="53056-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="53056-115">-MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="53056-115">-MaxDegreeOfParallelismPerJob</span></span>
<span data-ttu-id="53056-116">O grau máximo de suporte de paralelismo por trabalho para esta política.</span><span class="sxs-lookup"><span data-stu-id="53056-116">The maximum supported degree of parallelism per job for this policy.</span></span>
<span data-ttu-id="53056-117">É preciso especificar o MinPriorityPerJob, a ou os dois parâmetros.</span><span class="sxs-lookup"><span data-stu-id="53056-117">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="53056-118">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="53056-118">-MinPriorityPerJob</span></span>
<span data-ttu-id="53056-119">A prioridade mínima com suporte por trabalho para esta política.</span><span class="sxs-lookup"><span data-stu-id="53056-119">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="53056-120">É preciso especificar o MaxDegreeOfParallelismPerJob, a ou os dois parâmetros.</span><span class="sxs-lookup"><span data-stu-id="53056-120">Either this, MaxDegreeOfParallelismPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="53056-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="53056-121">-Name</span></span>
<span data-ttu-id="53056-122">Nome da política de computação a ser criada.</span><span class="sxs-lookup"><span data-stu-id="53056-122">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="53056-123">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="53056-123">-ObjectId</span></span>
<span data-ttu-id="53056-124">A ID de objeto do Azure Active Directory para o usuário ou grupo ao qual a política será aplicada.</span><span class="sxs-lookup"><span data-stu-id="53056-124">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

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

### <span data-ttu-id="53056-125">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="53056-125">-ObjectType</span></span>
<span data-ttu-id="53056-126">O tipo de objeto do Azure Active Directory para a identificação do objeto passado.</span><span class="sxs-lookup"><span data-stu-id="53056-126">The Azure Active Directory object type for the object ID passed in.</span></span>

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

### <span data-ttu-id="53056-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53056-127">-ResourceGroupName</span></span>
<span data-ttu-id="53056-128">Nome do grupo de recursos sob o qual a conta existe.</span><span class="sxs-lookup"><span data-stu-id="53056-128">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="53056-129">Opcional e tentará descobrir, se não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="53056-129">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="53056-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="53056-130">-Confirm</span></span>
<span data-ttu-id="53056-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53056-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53056-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53056-132">-WhatIf</span></span>
<span data-ttu-id="53056-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="53056-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53056-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="53056-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53056-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53056-135">-DefaultProfile</span></span>
<span data-ttu-id="53056-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53056-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53056-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53056-137">CommonParameters</span></span>
<span data-ttu-id="53056-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53056-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53056-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53056-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53056-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53056-140">INPUTS</span></span>

### <span data-ttu-id="53056-141">System. String</span><span class="sxs-lookup"><span data-stu-id="53056-141">System.String</span></span>
<span data-ttu-id="53056-142">System. GUID System. Int32</span><span class="sxs-lookup"><span data-stu-id="53056-142">System.Guid System.Int32</span></span>

## <span data-ttu-id="53056-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53056-143">OUTPUTS</span></span>

### <span data-ttu-id="53056-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="53056-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="53056-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53056-145">NOTES</span></span>

## <span data-ttu-id="53056-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53056-146">RELATED LINKS</span></span>

