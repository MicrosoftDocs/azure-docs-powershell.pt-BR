---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: e5bf7ca6951a78fc631b5bc2ffa96a2042423d9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439955"
---
# <span data-ttu-id="4ba16-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="4ba16-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="4ba16-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ba16-102">SYNOPSIS</span></span>
<span data-ttu-id="4ba16-103">Remover um nó com o nome fornecido em um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="4ba16-103">Remove a node with the given name on an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ba16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ba16-104">SYNTAX</span></span>

### <span data-ttu-id="4ba16-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4ba16-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf]
 [-Confirm]
```

### <span data-ttu-id="4ba16-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4ba16-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String> [-WhatIf]
 [-Confirm]
```

### <span data-ttu-id="4ba16-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="4ba16-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4ba16-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ba16-108">DESCRIPTION</span></span>
<span data-ttu-id="4ba16-109">O cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntimeNode remove um nó em um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="4ba16-109">The Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="4ba16-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ba16-110">EXAMPLES</span></span>

### <span data-ttu-id="4ba16-111">Exemplo 1: remover um nó de um tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="4ba16-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="4ba16-112">Esse comando Remove um nó chamado ' Node_1 ' no tempo de execução de integração chamado ' test-selfhost-IV ' na assinatura do grupo de recursos chamado ' RG-Test-dfv2 ' e data Factory chamado ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="4ba16-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="4ba16-113">OS</span><span class="sxs-lookup"><span data-stu-id="4ba16-113">PARAMETERS</span></span>

### <span data-ttu-id="4ba16-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4ba16-114">-Confirm</span></span>
<span data-ttu-id="4ba16-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ba16-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ba16-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="4ba16-116">-DataFactoryName</span></span>
<span data-ttu-id="4ba16-117">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="4ba16-117">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ba16-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4ba16-118">-Force</span></span>
<span data-ttu-id="4ba16-119">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="4ba16-119">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba16-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ba16-120">-InputObject</span></span>
<span data-ttu-id="4ba16-121">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="4ba16-121">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ba16-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="4ba16-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="4ba16-123">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="4ba16-123">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ba16-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="4ba16-124">-NodeName</span></span>
<span data-ttu-id="4ba16-125">O nome do nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="4ba16-125">The integration runtime node name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba16-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ba16-126">-ResourceGroupName</span></span>
<span data-ttu-id="4ba16-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4ba16-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ba16-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ba16-128">-ResourceId</span></span>
<span data-ttu-id="4ba16-129">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="4ba16-129">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ba16-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ba16-130">-WhatIf</span></span>
<span data-ttu-id="4ba16-131">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ba16-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="4ba16-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ba16-132">INPUTS</span></span>

### <span data-ttu-id="4ba16-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4ba16-133">System.String</span></span>
<span data-ttu-id="4ba16-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4ba16-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="4ba16-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ba16-135">OUTPUTS</span></span>

### <span data-ttu-id="4ba16-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="4ba16-136">System.Object</span></span>

## <span data-ttu-id="4ba16-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ba16-137">NOTES</span></span>

## <span data-ttu-id="4ba16-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ba16-138">RELATED LINKS</span></span>

