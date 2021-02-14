---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: aa838b24cc2410d9d699bac4dc8d4c00e3153174
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116865"
---
# <span data-ttu-id="babf6-101">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="babf6-101">Stop-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="babf6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="babf6-102">SYNOPSIS</span></span>
<span data-ttu-id="babf6-103">Interrompe um tempo de execução de integração dedicado gerenciado.</span><span class="sxs-lookup"><span data-stu-id="babf6-103">Stops a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="babf6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="babf6-104">SYNTAX</span></span>

### <span data-ttu-id="babf6-105">ByIntegrationRuntimeName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="babf6-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="babf6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="babf6-106">ByResourceId</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="babf6-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="babf6-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="babf6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="babf6-108">DESCRIPTION</span></span>
<span data-ttu-id="babf6-109">O cmdlet **Stop-AzDataFactoryV2IntegrationRuntime** interrompe um tempo de execução de integração dedicada gerenciado no estado 'Started', que foi iniciado pelo cmdlet Start-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="babf6-109">The **Stop-AzDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="babf6-110">Os recursos são liberados e o estado é transferido para "Parado".</span><span class="sxs-lookup"><span data-stu-id="babf6-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="babf6-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="babf6-111">EXAMPLES</span></span>

### <span data-ttu-id="babf6-112">Exemplo 1: Interromper um tempo de execução de integração gerenciada que está no estado "Iniciado".</span><span class="sxs-lookup"><span data-stu-id="babf6-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="babf6-113">O tempo de execução de integração gerenciada 'test-reserlved-ir' está no estado 'Iniciado'.</span><span class="sxs-lookup"><span data-stu-id="babf6-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="babf6-114">Depois de Stop-AzDataFactoryV2IntegrationRuntime cmdlet, os recursos são liberados e o estado é transferido para "Parado".</span><span class="sxs-lookup"><span data-stu-id="babf6-114">After running Stop-AzDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="babf6-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="babf6-115">PARAMETERS</span></span>

### <span data-ttu-id="babf6-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="babf6-116">-DataFactoryName</span></span>
<span data-ttu-id="babf6-117">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="babf6-117">The data factory name.</span></span>

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

### <span data-ttu-id="babf6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="babf6-118">-DefaultProfile</span></span>
<span data-ttu-id="babf6-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="babf6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="babf6-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="babf6-120">-Force</span></span>
<span data-ttu-id="babf6-121">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="babf6-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="babf6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="babf6-122">-InputObject</span></span>
<span data-ttu-id="babf6-123">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="babf6-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="babf6-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="babf6-124">-Name</span></span>
<span data-ttu-id="babf6-125">O nome de tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="babf6-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="babf6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="babf6-126">-ResourceGroupName</span></span>
<span data-ttu-id="babf6-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="babf6-127">The resource group name.</span></span>

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

### <span data-ttu-id="babf6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="babf6-128">-ResourceId</span></span>
<span data-ttu-id="babf6-129">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="babf6-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="babf6-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="babf6-130">-Confirm</span></span>
<span data-ttu-id="babf6-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="babf6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="babf6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="babf6-132">-WhatIf</span></span>
<span data-ttu-id="babf6-133">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="babf6-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="babf6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="babf6-134">CommonParameters</span></span>
<span data-ttu-id="babf6-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="babf6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="babf6-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="babf6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="babf6-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="babf6-137">INPUTS</span></span>

### <span data-ttu-id="babf6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="babf6-138">System.String</span></span>

### <span data-ttu-id="babf6-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="babf6-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="babf6-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="babf6-140">OUTPUTS</span></span>

### <span data-ttu-id="babf6-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="babf6-141">System.Void</span></span>

## <span data-ttu-id="babf6-142">Notas</span><span class="sxs-lookup"><span data-stu-id="babf6-142">NOTES</span></span>
<span data-ttu-id="babf6-143">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, keyword, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="babf6-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="babf6-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="babf6-144">RELATED LINKS</span></span>

[<span data-ttu-id="babf6-145">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="babf6-145">Start-AzDataFactoryV2IntegrationRuntime</span></span>]()
