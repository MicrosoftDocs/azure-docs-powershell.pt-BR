---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: fa9e9e0b2de02a320cb5140aac21e30f7c2b5bbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892515"
---
# <span data-ttu-id="44955-101">Update-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="44955-101">Update-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="44955-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44955-102">SYNOPSIS</span></span>
<span data-ttu-id="44955-103">Atualiza um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="44955-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="44955-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="44955-104">SYNTAX</span></span>

### <span data-ttu-id="44955-105">ByIntegrationRuntimeName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="44955-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44955-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="44955-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44955-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="44955-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44955-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="44955-108">DESCRIPTION</span></span>
<span data-ttu-id="44955-109">O cmdlet **Update-AzDataFactoryV2IntegrationRuntime** atualiza as propriedades de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="44955-109">The **Update-AzDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="44955-110">Atualmente, o cmdlet só dá suporte à atualização de 'AutoUpdate' e 'AutoUpdateDelayOffset' para tempo de execução de integração auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="44955-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="44955-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44955-111">EXAMPLES</span></span>

### <span data-ttu-id="44955-112">Exemplo 1: atualiza um tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="44955-112">Example 1: Updates an integration runtime</span></span>
```
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzDataFactoryV2IntegrationRuntime `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -Name 'test-selfhost-ir' `
    -AutoUpdate Off `
    -AutoUpdateDelayOffset $ts

Nodes                     : {Node_1}
CreateTime                : 11/18/2017 2:45:38 PM
InternalChannelEncryption : 
Version                   : 3.2.6519.3
Capabilities              : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
ScheduledUpdateDate       : 
UpdateDelayOffset         : 
LocalTimeZoneOffset       : 
AutoUpdate                : Off
ServiceUrls               : {wu.frontend.int.clouddatahub-int.net, *.servicebus.windows.net}
State                     : Online
Id                        : /subscriptions/41fcbc45-c594-4152-a8f1-fcbcd6452aea/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
Type                      : SelfHosted
ResourceGroupName         : rg-test-dfv2
DataFactoryName           : test-df-eu2
Name                      : test-selfhost-ir
Description               : New 2 description
```

<span data-ttu-id="44955-113">O cmdlet atualiza o tempo de execução de integração auto-hospedado chamado 'test-selfhost-ir'.</span><span class="sxs-lookup"><span data-stu-id="44955-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="44955-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="44955-114">PARAMETERS</span></span>

### <span data-ttu-id="44955-115">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="44955-115">-AutoUpdate</span></span>
<span data-ttu-id="44955-116">Habilitar ou desabilitar a atualização automática do tempo de execução de integração auto-hospedada.</span><span class="sxs-lookup"><span data-stu-id="44955-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44955-117">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="44955-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="44955-118">A hora em hora do dia para a atualização automática do tempo de execução de integração auto-hospedada.</span><span class="sxs-lookup"><span data-stu-id="44955-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44955-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="44955-119">-DataFactoryName</span></span>
<span data-ttu-id="44955-120">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="44955-120">The data factory name.</span></span>

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

### <span data-ttu-id="44955-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44955-121">-DefaultProfile</span></span>
<span data-ttu-id="44955-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="44955-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44955-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44955-123">-InputObject</span></span>
<span data-ttu-id="44955-124">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="44955-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="44955-125">-Name</span><span class="sxs-lookup"><span data-stu-id="44955-125">-Name</span></span>
<span data-ttu-id="44955-126">O nome do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="44955-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="44955-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44955-127">-ResourceGroupName</span></span>
<span data-ttu-id="44955-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44955-128">The resource group name.</span></span>

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

### <span data-ttu-id="44955-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44955-129">-ResourceId</span></span>
<span data-ttu-id="44955-130">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="44955-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="44955-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44955-131">-Confirm</span></span>
<span data-ttu-id="44955-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44955-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44955-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44955-133">-WhatIf</span></span>
<span data-ttu-id="44955-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44955-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44955-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44955-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44955-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44955-136">CommonParameters</span></span>
<span data-ttu-id="44955-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44955-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44955-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44955-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44955-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44955-139">INPUTS</span></span>

### <span data-ttu-id="44955-140">System.String</span><span class="sxs-lookup"><span data-stu-id="44955-140">System.String</span></span>

### <span data-ttu-id="44955-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="44955-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="44955-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="44955-142">OUTPUTS</span></span>

### <span data-ttu-id="44955-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="44955-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="44955-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="44955-144">NOTES</span></span>
<span data-ttu-id="44955-145">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="44955-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="44955-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44955-146">RELATED LINKS</span></span>

<span data-ttu-id="44955-147">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="44955-147">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

