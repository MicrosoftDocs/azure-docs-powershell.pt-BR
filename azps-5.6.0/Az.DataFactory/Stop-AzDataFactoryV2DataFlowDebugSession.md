---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 21c8d30cfeec7e0138ec659074a94bd5914e5124
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892517"
---
# <span data-ttu-id="2bd14-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="2bd14-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="2bd14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bd14-102">SYNOPSIS</span></span>
<span data-ttu-id="2bd14-103">Interrompe uma sessão de depuração de fluxo de dados no Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="2bd14-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="2bd14-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2bd14-104">SYNTAX</span></span>

### <span data-ttu-id="2bd14-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2bd14-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2bd14-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2bd14-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bd14-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2bd14-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bd14-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2bd14-108">DESCRIPTION</span></span>
<span data-ttu-id="2bd14-109">Esse comando interrompe a sessão de depuração, caso não seja então que a sessão será automaticamente desligada de acordo com a configuração Tempo para a live da sessão de depuração.</span><span class="sxs-lookup"><span data-stu-id="2bd14-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="2bd14-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2bd14-110">EXAMPLES</span></span>

### <span data-ttu-id="2bd14-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2bd14-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="2bd14-112">Interrompe uma sessão de depuração de fluxo de dados "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" no fábrica de dados "WikiADF"</span><span class="sxs-lookup"><span data-stu-id="2bd14-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="2bd14-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2bd14-113">PARAMETERS</span></span>

### <span data-ttu-id="2bd14-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2bd14-114">-DataFactory</span></span>
<span data-ttu-id="2bd14-115">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="2bd14-115">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd14-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2bd14-116">-DataFactoryName</span></span>
<span data-ttu-id="2bd14-117">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="2bd14-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd14-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bd14-118">-DefaultProfile</span></span>
<span data-ttu-id="2bd14-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2bd14-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bd14-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2bd14-120">-PassThru</span></span>
<span data-ttu-id="2bd14-121">Se especificado, a gravação será true caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2bd14-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="2bd14-122">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="2bd14-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="2bd14-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bd14-123">-ResourceGroupName</span></span>
<span data-ttu-id="2bd14-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2bd14-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd14-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2bd14-125">-ResourceId</span></span>
<span data-ttu-id="2bd14-126">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="2bd14-126">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd14-127">-SessionId</span><span class="sxs-lookup"><span data-stu-id="2bd14-127">-SessionId</span></span>
<span data-ttu-id="2bd14-128">A ID da sessão de depuração do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="2bd14-128">The data flow debug session ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd14-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2bd14-129">-Confirm</span></span>
<span data-ttu-id="2bd14-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bd14-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bd14-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bd14-131">-WhatIf</span></span>
<span data-ttu-id="2bd14-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2bd14-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bd14-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2bd14-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bd14-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd14-134">CommonParameters</span></span>
<span data-ttu-id="2bd14-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bd14-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd14-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2bd14-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd14-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2bd14-137">INPUTS</span></span>

### <span data-ttu-id="2bd14-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2bd14-138">System.String</span></span>

### <span data-ttu-id="2bd14-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2bd14-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="2bd14-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2bd14-140">OUTPUTS</span></span>

### <span data-ttu-id="2bd14-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="2bd14-141">System.Void</span></span>

### <span data-ttu-id="2bd14-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2bd14-142">System.Boolean</span></span>

## <span data-ttu-id="2bd14-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="2bd14-143">NOTES</span></span>
<span data-ttu-id="2bd14-144">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="2bd14-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2bd14-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2bd14-145">RELATED LINKS</span></span>

[<span data-ttu-id="2bd14-146">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="2bd14-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="2bd14-147">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="2bd14-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="2bd14-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="2bd14-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="2bd14-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="2bd14-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)