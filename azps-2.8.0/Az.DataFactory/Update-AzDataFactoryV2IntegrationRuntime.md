---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: d2177e2ca7705f579921b9e2eb9fc64ab0e0c33a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596941"
---
# <span data-ttu-id="da721-101">Update-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="da721-101">Update-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="da721-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da721-102">SYNOPSIS</span></span>
<span data-ttu-id="da721-103">Atualiza um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="da721-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="da721-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da721-104">SYNTAX</span></span>

### <span data-ttu-id="da721-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="da721-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da721-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="da721-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da721-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="da721-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da721-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da721-108">DESCRIPTION</span></span>
<span data-ttu-id="da721-109">O cmdlet **Update-AzDataFactoryV2IntegrationRuntime** atualiza as propriedades do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="da721-109">The **Update-AzDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="da721-110">Atualmente, o cmdlet só dá suporte à atualização de ' AutoUpdate ' e ' AutoUpdateDelayOffset ' para o tempo de execução de integração de hospedagem automática.</span><span class="sxs-lookup"><span data-stu-id="da721-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="da721-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da721-111">EXAMPLES</span></span>

### <span data-ttu-id="da721-112">Exemplo 1: atualiza um tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="da721-112">Example 1: Updates an integration runtime</span></span>
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

<span data-ttu-id="da721-113">O cmdlet atualiza o tempo de execução de integração de hospedagem interna chamado ' test-selfhost-IV '.</span><span class="sxs-lookup"><span data-stu-id="da721-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="da721-114">OS</span><span class="sxs-lookup"><span data-stu-id="da721-114">PARAMETERS</span></span>

### <span data-ttu-id="da721-115">-Atualização automática</span><span class="sxs-lookup"><span data-stu-id="da721-115">-AutoUpdate</span></span>
<span data-ttu-id="da721-116">Habilite ou desabilite a atualização automática do tempo de execução de integração de hospedagem interna.</span><span class="sxs-lookup"><span data-stu-id="da721-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="da721-117">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="da721-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="da721-118">O tempo em hora do dia da atualização automática do tempo de execução de integração de hospedagem interna.</span><span class="sxs-lookup"><span data-stu-id="da721-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="da721-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="da721-119">-DataFactoryName</span></span>
<span data-ttu-id="da721-120">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="da721-120">The data factory name.</span></span>

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

### <span data-ttu-id="da721-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da721-121">-DefaultProfile</span></span>
<span data-ttu-id="da721-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da721-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da721-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da721-123">-InputObject</span></span>
<span data-ttu-id="da721-124">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="da721-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="da721-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="da721-125">-Name</span></span>
<span data-ttu-id="da721-126">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="da721-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="da721-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da721-127">-ResourceGroupName</span></span>
<span data-ttu-id="da721-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="da721-128">The resource group name.</span></span>

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

### <span data-ttu-id="da721-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da721-129">-ResourceId</span></span>
<span data-ttu-id="da721-130">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="da721-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="da721-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="da721-131">-Confirm</span></span>
<span data-ttu-id="da721-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da721-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da721-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da721-133">-WhatIf</span></span>
<span data-ttu-id="da721-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="da721-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da721-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="da721-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da721-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da721-136">CommonParameters</span></span>
<span data-ttu-id="da721-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da721-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da721-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da721-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da721-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da721-139">INPUTS</span></span>

### <span data-ttu-id="da721-140">System. String</span><span class="sxs-lookup"><span data-stu-id="da721-140">System.String</span></span>

### <span data-ttu-id="da721-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="da721-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="da721-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da721-142">OUTPUTS</span></span>

### <span data-ttu-id="da721-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="da721-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="da721-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da721-144">NOTES</span></span>
<span data-ttu-id="da721-145">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, data, fábricas, Copy, Activities, tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="da721-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="da721-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da721-146">RELATED LINKS</span></span>

<span data-ttu-id="da721-147">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="da721-147">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

