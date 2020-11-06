---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: a66ed7e910b5b9fbd1057d50e2fa3e5058400855
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429830"
---
# <span data-ttu-id="38b2c-101">Update-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="38b2c-101">Update-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="38b2c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38b2c-102">SYNOPSIS</span></span>
<span data-ttu-id="38b2c-103">Atualiza um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="38b2c-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38b2c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38b2c-104">SYNTAX</span></span>

### <span data-ttu-id="38b2c-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="38b2c-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38b2c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="38b2c-106">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38b2c-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="38b2c-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38b2c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38b2c-108">DESCRIPTION</span></span>
<span data-ttu-id="38b2c-109">O cmdlet **Update-AzureRmDataFactoryV2IntegrationRuntime** atualiza as propriedades do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="38b2c-109">The **Update-AzureRmDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="38b2c-110">Atualmente, o cmdlet só dá suporte à atualização de ' AutoUpdate ' e ' AutoUpdateDelayOffset ' para o tempo de execução de integração de hospedagem automática.</span><span class="sxs-lookup"><span data-stu-id="38b2c-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="38b2c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38b2c-111">EXAMPLES</span></span>

### <span data-ttu-id="38b2c-112">Exemplo 1: atualiza um tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="38b2c-112">Example 1: Updates an integration runtime</span></span>
```
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzureRmDataFactoryV2IntegrationRuntime `
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

<span data-ttu-id="38b2c-113">O cmdlet atualiza o tempo de execução de integração de hospedagem interna chamado ' test-selfhost-IV '.</span><span class="sxs-lookup"><span data-stu-id="38b2c-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="38b2c-114">OS</span><span class="sxs-lookup"><span data-stu-id="38b2c-114">PARAMETERS</span></span>

### <span data-ttu-id="38b2c-115">-Atualização automática</span><span class="sxs-lookup"><span data-stu-id="38b2c-115">-AutoUpdate</span></span>
<span data-ttu-id="38b2c-116">Habilite ou desabilite a atualização automática do tempo de execução de integração de hospedagem interna.</span><span class="sxs-lookup"><span data-stu-id="38b2c-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b2c-117">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="38b2c-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="38b2c-118">O tempo em hora do dia da atualização automática do tempo de execução de integração de hospedagem interna.</span><span class="sxs-lookup"><span data-stu-id="38b2c-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b2c-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="38b2c-119">-DataFactoryName</span></span>
<span data-ttu-id="38b2c-120">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="38b2c-120">The data factory name.</span></span>

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

### <span data-ttu-id="38b2c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b2c-121">-DefaultProfile</span></span>
<span data-ttu-id="38b2c-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38b2c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b2c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38b2c-123">-InputObject</span></span>
<span data-ttu-id="38b2c-124">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="38b2c-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="38b2c-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="38b2c-125">-Name</span></span>
<span data-ttu-id="38b2c-126">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="38b2c-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="38b2c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38b2c-127">-ResourceGroupName</span></span>
<span data-ttu-id="38b2c-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="38b2c-128">The resource group name.</span></span>

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

### <span data-ttu-id="38b2c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38b2c-129">-ResourceId</span></span>
<span data-ttu-id="38b2c-130">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="38b2c-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="38b2c-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="38b2c-131">-Confirm</span></span>
<span data-ttu-id="38b2c-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38b2c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38b2c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38b2c-133">-WhatIf</span></span>
<span data-ttu-id="38b2c-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="38b2c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38b2c-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38b2c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38b2c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b2c-136">CommonParameters</span></span>
<span data-ttu-id="38b2c-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38b2c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b2c-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38b2c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b2c-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38b2c-139">INPUTS</span></span>

### <span data-ttu-id="38b2c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="38b2c-140">System.String</span></span>
<span data-ttu-id="38b2c-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="38b2c-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="38b2c-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38b2c-142">OUTPUTS</span></span>

### <span data-ttu-id="38b2c-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="38b2c-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="38b2c-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38b2c-144">NOTES</span></span>
<span data-ttu-id="38b2c-145">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, data, fábricas, Copy, Activities, tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="38b2c-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="38b2c-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38b2c-146">RELATED LINKS</span></span>

<span data-ttu-id="38b2c-147">[Set-AzureRmDataFactoryV2IntegrationRuntime]() 
 [Get-AzureRmDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="38b2c-147">[Set-AzureRmDataFactoryV2IntegrationRuntime]()
[Get-AzureRmDataFactoryV2IntegrationRuntime]()</span></span>
