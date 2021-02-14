---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: c7ffe4348d11658da6e7c9caeccaa14f17a6329b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111008"
---
# <span data-ttu-id="66bee-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="66bee-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="66bee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66bee-102">SYNOPSIS</span></span>
<span data-ttu-id="66bee-103">Atualiza o tempo de execução da integração auto-hospedada.</span><span class="sxs-lookup"><span data-stu-id="66bee-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="66bee-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66bee-104">SYNTAX</span></span>

### <span data-ttu-id="66bee-105">ByIntegrationRuntimeName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="66bee-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66bee-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="66bee-106">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66bee-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="66bee-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66bee-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="66bee-108">DESCRIPTION</span></span>
<span data-ttu-id="66bee-109">O cmdlet **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** atualiza o tempo de execução de integração hospedada auto-hospedado se a nova versão estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="66bee-109">The **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="66bee-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="66bee-110">EXAMPLES</span></span>

### <span data-ttu-id="66bee-111">Exemplo 1: atualiza um tempo de execução de integração auto-hospedado</span><span class="sxs-lookup"><span data-stu-id="66bee-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="66bee-112">O cmdlet atualiza o tempo de execução de integração auto-hospedado chamado "test-selfhost-ir" no data factory 'test-df-eu2'.</span><span class="sxs-lookup"><span data-stu-id="66bee-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="66bee-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66bee-113">PARAMETERS</span></span>

### <span data-ttu-id="66bee-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="66bee-114">-DataFactoryName</span></span>
<span data-ttu-id="66bee-115">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="66bee-115">The data factory name.</span></span>

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

### <span data-ttu-id="66bee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66bee-116">-DefaultProfile</span></span>
<span data-ttu-id="66bee-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="66bee-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66bee-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66bee-118">-InputObject</span></span>
<span data-ttu-id="66bee-119">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="66bee-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="66bee-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="66bee-120">-Name</span></span>
<span data-ttu-id="66bee-121">O nome de tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="66bee-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="66bee-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66bee-122">-ResourceGroupName</span></span>
<span data-ttu-id="66bee-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="66bee-123">The resource group name.</span></span>

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

### <span data-ttu-id="66bee-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66bee-124">-ResourceId</span></span>
<span data-ttu-id="66bee-125">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="66bee-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="66bee-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="66bee-126">-Confirm</span></span>
<span data-ttu-id="66bee-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66bee-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66bee-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66bee-128">-WhatIf</span></span>
<span data-ttu-id="66bee-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="66bee-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66bee-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66bee-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66bee-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66bee-131">CommonParameters</span></span>
<span data-ttu-id="66bee-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66bee-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66bee-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66bee-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66bee-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="66bee-134">INPUTS</span></span>

### <span data-ttu-id="66bee-135">System.String</span><span class="sxs-lookup"><span data-stu-id="66bee-135">System.String</span></span>

### <span data-ttu-id="66bee-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="66bee-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="66bee-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="66bee-137">OUTPUTS</span></span>

### <span data-ttu-id="66bee-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="66bee-138">System.Void</span></span>

## <span data-ttu-id="66bee-139">Notas</span><span class="sxs-lookup"><span data-stu-id="66bee-139">NOTES</span></span>
<span data-ttu-id="66bee-140">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, keyword, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="66bee-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="66bee-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66bee-141">RELATED LINKS</span></span>

<span data-ttu-id="66bee-142">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="66bee-142">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

