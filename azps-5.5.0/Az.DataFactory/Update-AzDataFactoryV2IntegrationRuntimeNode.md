---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 0487794381e40db486df17cb9611191ac5d924d9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117735"
---
# <span data-ttu-id="63ee7-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="63ee7-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="63ee7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63ee7-102">SYNOPSIS</span></span>
<span data-ttu-id="63ee7-103">Atualiza o nó de tempo de execução de integração auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="63ee7-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="63ee7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63ee7-104">SYNTAX</span></span>

### <span data-ttu-id="63ee7-105">ByIntegrationRuntimeName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="63ee7-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63ee7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="63ee7-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63ee7-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="63ee7-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63ee7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="63ee7-108">DESCRIPTION</span></span>
<span data-ttu-id="63ee7-109">O cmdlet **Update-AzDataFactoryV2IntegrationRuntimeNode** atualiza as propriedades do nó de tempo de execução de integração auto-hospedado em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="63ee7-109">The **Update-AzDataFactoryV2IntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a data factory.</span></span> <span data-ttu-id="63ee7-110">Atualmente, só há suporte para a atualização de 'ConcurrentJobsLimit'.</span><span class="sxs-lookup"><span data-stu-id="63ee7-110">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="63ee7-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="63ee7-111">EXAMPLES</span></span>

### <span data-ttu-id="63ee7-112">Exemplo 1: atualiza o nó de tempo de execução de integração auto-hospedado</span><span class="sxs-lookup"><span data-stu-id="63ee7-112">Example 1: Updates self-hosted integration runtime node</span></span>
```
PS C:\> Update-AzDataFactoryV2IntegrationRuntimeNode `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -IntegrationRuntimeName 'test-selfhost-ir' `
    -Name 'Node_1' `
    -ConcurrentJobsLimit 3
```

<span data-ttu-id="63ee7-113">O cmdlet atualiza 'ConcurrentJobsLimit' para 3 para nó 'Node_1' em tempo de execução de integração hospedada auto-hospedado 'test-selfhost-ir'.</span><span class="sxs-lookup"><span data-stu-id="63ee7-113">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="63ee7-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63ee7-114">PARAMETERS</span></span>

### <span data-ttu-id="63ee7-115">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="63ee7-115">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="63ee7-116">O número de trabalhos simultâneos permitidos para execução no nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="63ee7-116">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="63ee7-117">Valores entre 1 e maxConcurrentJobs são permitidos.</span><span class="sxs-lookup"><span data-stu-id="63ee7-117">Values between 1 and maxConcurrentJobs are allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63ee7-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="63ee7-118">-DataFactoryName</span></span>
<span data-ttu-id="63ee7-119">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="63ee7-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63ee7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63ee7-120">-DefaultProfile</span></span>
<span data-ttu-id="63ee7-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="63ee7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63ee7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63ee7-122">-InputObject</span></span>
<span data-ttu-id="63ee7-123">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="63ee7-123">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63ee7-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="63ee7-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="63ee7-125">O nome de tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="63ee7-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63ee7-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="63ee7-126">-Name</span></span>
<span data-ttu-id="63ee7-127">O nome do nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="63ee7-127">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63ee7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63ee7-128">-ResourceGroupName</span></span>
<span data-ttu-id="63ee7-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="63ee7-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63ee7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63ee7-130">-ResourceId</span></span>
<span data-ttu-id="63ee7-131">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="63ee7-131">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63ee7-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="63ee7-132">-Confirm</span></span>
<span data-ttu-id="63ee7-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63ee7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63ee7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63ee7-134">-WhatIf</span></span>
<span data-ttu-id="63ee7-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="63ee7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63ee7-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="63ee7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63ee7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63ee7-137">CommonParameters</span></span>
<span data-ttu-id="63ee7-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63ee7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63ee7-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63ee7-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63ee7-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="63ee7-140">INPUTS</span></span>

### <span data-ttu-id="63ee7-141">System.String</span><span class="sxs-lookup"><span data-stu-id="63ee7-141">System.String</span></span>

### <span data-ttu-id="63ee7-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="63ee7-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="63ee7-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="63ee7-143">OUTPUTS</span></span>

### <span data-ttu-id="63ee7-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="63ee7-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="63ee7-145">Notas</span><span class="sxs-lookup"><span data-stu-id="63ee7-145">NOTES</span></span>
<span data-ttu-id="63ee7-146">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, keyword, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="63ee7-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="63ee7-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63ee7-147">RELATED LINKS</span></span>

<span data-ttu-id="63ee7-148">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="63ee7-148">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

