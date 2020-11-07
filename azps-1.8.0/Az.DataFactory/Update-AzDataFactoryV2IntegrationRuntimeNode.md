---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 67ce6dab34f907babd11bf180b499d25cfe9a053
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770989"
---
# <span data-ttu-id="ef895-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="ef895-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="ef895-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef895-102">SYNOPSIS</span></span>
<span data-ttu-id="ef895-103">Atualiza o nó do tempo de execução de integração de hospedagem interna.</span><span class="sxs-lookup"><span data-stu-id="ef895-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="ef895-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef895-104">SYNTAX</span></span>

### <span data-ttu-id="ef895-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ef895-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef895-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ef895-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef895-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ef895-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef895-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ef895-108">DESCRIPTION</span></span>
<span data-ttu-id="ef895-109">O cmdlet **Update-AzDataFactoryV2IntegrationRuntimeNode** atualiza propriedades do nó de tempo de execução de integração de hospedagem interna em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="ef895-109">The **Update-AzDataFactoryV2IntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a data factory.</span></span> <span data-ttu-id="ef895-110">Atualmente só dá suporte à atualização de ' ConcurrentJobsLimit '.</span><span class="sxs-lookup"><span data-stu-id="ef895-110">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="ef895-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef895-111">EXAMPLES</span></span>

### <span data-ttu-id="ef895-112">Exemplo 1: atualiza o nó do tempo de execução de integração de hospedagem interna</span><span class="sxs-lookup"><span data-stu-id="ef895-112">Example 1: Updates self-hosted integration runtime node</span></span>
```
PS C:\> Update-AzDataFactoryV2IntegrationRuntimeNode `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -IntegrationRuntimeName 'test-selfhost-ir' `
    -Name 'Node_1' `
    -ConcurrentJobsLimit 3
```

<span data-ttu-id="ef895-113">O cmdlet atualiza ' ConcurrentJobsLimit ' para 3 para o nó ' Node_1 ' no tempo de execução de integração de hospedagem interna ' test-selfhost-IV '.</span><span class="sxs-lookup"><span data-stu-id="ef895-113">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="ef895-114">OS</span><span class="sxs-lookup"><span data-stu-id="ef895-114">PARAMETERS</span></span>

### <span data-ttu-id="ef895-115">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="ef895-115">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="ef895-116">O número de trabalhos simultâneos permitidos para executar no nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="ef895-116">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="ef895-117">Valores entre 1 e maxConcurrentJobs são permitidos.</span><span class="sxs-lookup"><span data-stu-id="ef895-117">Values between 1 and maxConcurrentJobs are allowed.</span></span>

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

### <span data-ttu-id="ef895-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ef895-118">-DataFactoryName</span></span>
<span data-ttu-id="ef895-119">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="ef895-119">The data factory name.</span></span>

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

### <span data-ttu-id="ef895-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef895-120">-DefaultProfile</span></span>
<span data-ttu-id="ef895-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef895-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef895-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef895-122">-InputObject</span></span>
<span data-ttu-id="ef895-123">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="ef895-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="ef895-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="ef895-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="ef895-125">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="ef895-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="ef895-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef895-126">-Name</span></span>
<span data-ttu-id="ef895-127">O nome do nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="ef895-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="ef895-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef895-128">-ResourceGroupName</span></span>
<span data-ttu-id="ef895-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ef895-129">The resource group name.</span></span>

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

### <span data-ttu-id="ef895-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef895-130">-ResourceId</span></span>
<span data-ttu-id="ef895-131">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="ef895-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ef895-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ef895-132">-Confirm</span></span>
<span data-ttu-id="ef895-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef895-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef895-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef895-134">-WhatIf</span></span>
<span data-ttu-id="ef895-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ef895-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef895-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ef895-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef895-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef895-137">CommonParameters</span></span>
<span data-ttu-id="ef895-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef895-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef895-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef895-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef895-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ef895-140">INPUTS</span></span>

### <span data-ttu-id="ef895-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ef895-141">System.String</span></span>

### <span data-ttu-id="ef895-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ef895-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ef895-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ef895-143">OUTPUTS</span></span>

### <span data-ttu-id="ef895-144">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="ef895-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="ef895-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ef895-145">NOTES</span></span>
<span data-ttu-id="ef895-146">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, data, fábricas, Copy, Activities, tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="ef895-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="ef895-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef895-147">RELATED LINKS</span></span>

<span data-ttu-id="ef895-148">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="ef895-148">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

