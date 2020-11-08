---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 63e78c0068d17986f845adaae9dbc5caf22b4b4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112832"
---
# <span data-ttu-id="de0f4-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="de0f4-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="de0f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de0f4-102">SYNOPSIS</span></span>
<span data-ttu-id="de0f4-103">Interrompe uma sessão de depuração do fluxo de dados no Azure data Factory</span><span class="sxs-lookup"><span data-stu-id="de0f4-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="de0f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de0f4-104">SYNTAX</span></span>

### <span data-ttu-id="de0f4-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="de0f4-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de0f4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="de0f4-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de0f4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="de0f4-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de0f4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de0f4-108">DESCRIPTION</span></span>
<span data-ttu-id="de0f4-109">Esse comando interrompe a sessão de depuração, caso contrário, a sessão será desativada automaticamente de acordo com a configuração de tempo de vida da sessão de depuração.</span><span class="sxs-lookup"><span data-stu-id="de0f4-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="de0f4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de0f4-110">EXAMPLES</span></span>

### <span data-ttu-id="de0f4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="de0f4-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="de0f4-112">Interrompe uma sessão de depuração do fluxo de dados "fd76cd0d-8b37-4DC0-A370-3f9d43ac686d" no data Factory "WikiADF"</span><span class="sxs-lookup"><span data-stu-id="de0f4-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="de0f4-113">OS</span><span class="sxs-lookup"><span data-stu-id="de0f4-113">PARAMETERS</span></span>

### <span data-ttu-id="de0f4-114">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="de0f4-114">-DataFactory</span></span>
<span data-ttu-id="de0f4-115">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="de0f4-115">The data factory object.</span></span>

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

### <span data-ttu-id="de0f4-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="de0f4-116">-DataFactoryName</span></span>
<span data-ttu-id="de0f4-117">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="de0f4-117">The data factory name.</span></span>

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

### <span data-ttu-id="de0f4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de0f4-118">-DefaultProfile</span></span>
<span data-ttu-id="de0f4-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de0f4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de0f4-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de0f4-120">-PassThru</span></span>
<span data-ttu-id="de0f4-121">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="de0f4-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="de0f4-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="de0f4-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="de0f4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de0f4-123">-ResourceGroupName</span></span>
<span data-ttu-id="de0f4-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="de0f4-124">The resource group name.</span></span>

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

### <span data-ttu-id="de0f4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de0f4-125">-ResourceId</span></span>
<span data-ttu-id="de0f4-126">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="de0f4-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="de0f4-127">-Identificação_da_sessão</span><span class="sxs-lookup"><span data-stu-id="de0f4-127">-SessionId</span></span>
<span data-ttu-id="de0f4-128">A ID da sessão de depuração do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="de0f4-128">The data flow debug session ID.</span></span>

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

### <span data-ttu-id="de0f4-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="de0f4-129">-Confirm</span></span>
<span data-ttu-id="de0f4-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de0f4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de0f4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de0f4-131">-WhatIf</span></span>
<span data-ttu-id="de0f4-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="de0f4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de0f4-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="de0f4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de0f4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de0f4-134">CommonParameters</span></span>
<span data-ttu-id="de0f4-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de0f4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de0f4-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de0f4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de0f4-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de0f4-137">INPUTS</span></span>

### <span data-ttu-id="de0f4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="de0f4-138">System.String</span></span>

### <span data-ttu-id="de0f4-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="de0f4-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="de0f4-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de0f4-140">OUTPUTS</span></span>

### <span data-ttu-id="de0f4-141">System. void</span><span class="sxs-lookup"><span data-stu-id="de0f4-141">System.Void</span></span>

### <span data-ttu-id="de0f4-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="de0f4-142">System.Boolean</span></span>

## <span data-ttu-id="de0f4-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de0f4-143">NOTES</span></span>
<span data-ttu-id="de0f4-144">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="de0f4-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="de0f4-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de0f4-145">RELATED LINKS</span></span>

[<span data-ttu-id="de0f4-146">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="de0f4-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="de0f4-147">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="de0f4-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="de0f4-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="de0f4-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="de0f4-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="de0f4-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)