---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/stop-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 405754afec3ff62eb59d385646df43f699557d18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891449"
---
# <span data-ttu-id="f48d5-101">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f48d5-101">Stop-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="f48d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f48d5-102">SYNOPSIS</span></span>
<span data-ttu-id="f48d5-103">Interrompe um tempo de execução de integração dedicado gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f48d5-103">Stops a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="f48d5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f48d5-104">SYNTAX</span></span>

### <span data-ttu-id="f48d5-105">ByIntegrationRuntimeName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f48d5-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f48d5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f48d5-106">ByResourceId</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f48d5-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="f48d5-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f48d5-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f48d5-108">DESCRIPTION</span></span>
<span data-ttu-id="f48d5-109">O cmdlet **Stop-AzDataFactoryV2IntegrationRuntime** interrompe um tempo de execução de integração dedicado gerenciado no estado 'Iniciado', iniciado pelo cmdlet Start-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="f48d5-109">The **Stop-AzDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="f48d5-110">Os recursos são liberados e o estado é transferido para 'Parado'.</span><span class="sxs-lookup"><span data-stu-id="f48d5-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="f48d5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f48d5-111">EXAMPLES</span></span>

### <span data-ttu-id="f48d5-112">Exemplo 1: pare um tempo de execução de integração gerenciada que está no estado 'Iniciado'.</span><span class="sxs-lookup"><span data-stu-id="f48d5-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="f48d5-113">O tempo de execução de integração gerenciada 'test-reserlved-ir' está no estado 'Iniciado'.</span><span class="sxs-lookup"><span data-stu-id="f48d5-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="f48d5-114">Depois de executar Stop-AzDataFactoryV2IntegrationRuntime cmdlet, os recursos são liberados e o estado é transferido para 'Stopped'.</span><span class="sxs-lookup"><span data-stu-id="f48d5-114">After running Stop-AzDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="f48d5-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f48d5-115">PARAMETERS</span></span>

### <span data-ttu-id="f48d5-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f48d5-116">-DataFactoryName</span></span>
<span data-ttu-id="f48d5-117">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="f48d5-117">The data factory name.</span></span>

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

### <span data-ttu-id="f48d5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f48d5-118">-DefaultProfile</span></span>
<span data-ttu-id="f48d5-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f48d5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f48d5-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f48d5-120">-Force</span></span>
<span data-ttu-id="f48d5-121">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="f48d5-121">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f48d5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f48d5-122">-InputObject</span></span>
<span data-ttu-id="f48d5-123">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f48d5-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="f48d5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f48d5-124">-Name</span></span>
<span data-ttu-id="f48d5-125">O nome do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f48d5-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f48d5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f48d5-126">-ResourceGroupName</span></span>
<span data-ttu-id="f48d5-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f48d5-127">The resource group name.</span></span>

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

### <span data-ttu-id="f48d5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f48d5-128">-ResourceId</span></span>
<span data-ttu-id="f48d5-129">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="f48d5-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f48d5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f48d5-130">-Confirm</span></span>
<span data-ttu-id="f48d5-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f48d5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f48d5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f48d5-132">-WhatIf</span></span>
<span data-ttu-id="f48d5-133">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f48d5-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="f48d5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f48d5-134">CommonParameters</span></span>
<span data-ttu-id="f48d5-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f48d5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f48d5-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f48d5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f48d5-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f48d5-137">INPUTS</span></span>

### <span data-ttu-id="f48d5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f48d5-138">System.String</span></span>

### <span data-ttu-id="f48d5-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f48d5-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="f48d5-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f48d5-140">OUTPUTS</span></span>

### <span data-ttu-id="f48d5-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="f48d5-141">System.Void</span></span>

## <span data-ttu-id="f48d5-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="f48d5-142">NOTES</span></span>
<span data-ttu-id="f48d5-143">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="f48d5-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="f48d5-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f48d5-144">RELATED LINKS</span></span>

[<span data-ttu-id="f48d5-145">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f48d5-145">Start-AzDataFactoryV2IntegrationRuntime</span></span>]()
