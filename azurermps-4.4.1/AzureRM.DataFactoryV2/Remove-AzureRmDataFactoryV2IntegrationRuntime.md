---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 81b05b8229530a8975be023a3b4a5e8c93d93c80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441124"
---
# <span data-ttu-id="fc9ed-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fc9ed-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="fc9ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc9ed-102">SYNOPSIS</span></span>
<span data-ttu-id="fc9ed-103">Remove um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="fc9ed-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc9ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc9ed-104">SYNTAX</span></span>

### <span data-ttu-id="fc9ed-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="fc9ed-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="fc9ed-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fc9ed-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="fc9ed-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="fc9ed-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="fc9ed-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc9ed-108">DESCRIPTION</span></span>
<span data-ttu-id="fc9ed-109">O cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime remove um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="fc9ed-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="fc9ed-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc9ed-110">EXAMPLES</span></span>

### <span data-ttu-id="fc9ed-111">Exemplo 1: remover um tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="fc9ed-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="fc9ed-112">Esse comando Remove o tempo de execução de integração chamado "Test-reservou-ir" da fábrica de dados chamado "Test-DF".</span><span class="sxs-lookup"><span data-stu-id="fc9ed-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="fc9ed-113">Esse comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="fc9ed-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="fc9ed-114">OS</span><span class="sxs-lookup"><span data-stu-id="fc9ed-114">PARAMETERS</span></span>

### <span data-ttu-id="fc9ed-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="fc9ed-115">-DataFactoryName</span></span>
<span data-ttu-id="fc9ed-116">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="fc9ed-116">The data factory name.</span></span>

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

### <span data-ttu-id="fc9ed-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fc9ed-117">-Force</span></span>
<span data-ttu-id="fc9ed-118">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="fc9ed-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="fc9ed-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc9ed-119">-InputObject</span></span>
<span data-ttu-id="fc9ed-120">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="fc9ed-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="fc9ed-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc9ed-121">-Name</span></span>
<span data-ttu-id="fc9ed-122">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="fc9ed-122">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc9ed-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc9ed-123">-ResourceGroupName</span></span>
<span data-ttu-id="fc9ed-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fc9ed-124">The resource group name.</span></span>

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

### <span data-ttu-id="fc9ed-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc9ed-125">-ResourceId</span></span>
<span data-ttu-id="fc9ed-126">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc9ed-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="fc9ed-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fc9ed-127">-Confirm</span></span>
<span data-ttu-id="fc9ed-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc9ed-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc9ed-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc9ed-129">-WhatIf</span></span>
<span data-ttu-id="fc9ed-130">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc9ed-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="fc9ed-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc9ed-131">INPUTS</span></span>

### <span data-ttu-id="fc9ed-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fc9ed-132">System.String</span></span>
<span data-ttu-id="fc9ed-133">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fc9ed-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="fc9ed-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc9ed-134">OUTPUTS</span></span>

### <span data-ttu-id="fc9ed-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="fc9ed-135">System.Object</span></span>

## <span data-ttu-id="fc9ed-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc9ed-136">NOTES</span></span>
<span data-ttu-id="fc9ed-137">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, data, fábricas, Copy, Activities, tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="fc9ed-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="fc9ed-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc9ed-138">RELATED LINKS</span></span>
[<span data-ttu-id="fc9ed-139">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fc9ed-139">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="fc9ed-140">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fc9ed-140">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

