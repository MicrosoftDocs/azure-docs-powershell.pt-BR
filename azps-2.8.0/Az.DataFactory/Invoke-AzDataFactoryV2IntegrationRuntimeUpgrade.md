---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: ff2b59310607e360af91e231e09fda60769f0e7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597044"
---
# <span data-ttu-id="07bc1-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="07bc1-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="07bc1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07bc1-102">SYNOPSIS</span></span>
<span data-ttu-id="07bc1-103">Atualiza o tempo de execução de integração de hospedagem automática.</span><span class="sxs-lookup"><span data-stu-id="07bc1-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="07bc1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07bc1-104">SYNTAX</span></span>

### <span data-ttu-id="07bc1-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="07bc1-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07bc1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="07bc1-106">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07bc1-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="07bc1-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07bc1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07bc1-108">DESCRIPTION</span></span>
<span data-ttu-id="07bc1-109">O cmdlet **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** atualiza o tempo de execução de integração de hospedagem interna se a nova versão estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="07bc1-109">The **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="07bc1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07bc1-110">EXAMPLES</span></span>

### <span data-ttu-id="07bc1-111">Exemplo 1: atualiza um Runtime de integração de hospedagem interna</span><span class="sxs-lookup"><span data-stu-id="07bc1-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="07bc1-112">O cmdlet atualiza o tempo de execução de integração de hospedagem interna chamado "Test-selfhost-IV" no data Factory "Test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="07bc1-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="07bc1-113">OS</span><span class="sxs-lookup"><span data-stu-id="07bc1-113">PARAMETERS</span></span>

### <span data-ttu-id="07bc1-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="07bc1-114">-DataFactoryName</span></span>
<span data-ttu-id="07bc1-115">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="07bc1-115">The data factory name.</span></span>

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

### <span data-ttu-id="07bc1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07bc1-116">-DefaultProfile</span></span>
<span data-ttu-id="07bc1-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07bc1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07bc1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07bc1-118">-InputObject</span></span>
<span data-ttu-id="07bc1-119">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="07bc1-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="07bc1-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="07bc1-120">-Name</span></span>
<span data-ttu-id="07bc1-121">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="07bc1-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="07bc1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07bc1-122">-ResourceGroupName</span></span>
<span data-ttu-id="07bc1-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="07bc1-123">The resource group name.</span></span>

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

### <span data-ttu-id="07bc1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07bc1-124">-ResourceId</span></span>
<span data-ttu-id="07bc1-125">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="07bc1-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="07bc1-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="07bc1-126">-Confirm</span></span>
<span data-ttu-id="07bc1-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07bc1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07bc1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07bc1-128">-WhatIf</span></span>
<span data-ttu-id="07bc1-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="07bc1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07bc1-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="07bc1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07bc1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07bc1-131">CommonParameters</span></span>
<span data-ttu-id="07bc1-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07bc1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07bc1-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07bc1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07bc1-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07bc1-134">INPUTS</span></span>

### <span data-ttu-id="07bc1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="07bc1-135">System.String</span></span>

### <span data-ttu-id="07bc1-136">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="07bc1-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="07bc1-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07bc1-137">OUTPUTS</span></span>

### <span data-ttu-id="07bc1-138">System. void</span><span class="sxs-lookup"><span data-stu-id="07bc1-138">System.Void</span></span>

## <span data-ttu-id="07bc1-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07bc1-139">NOTES</span></span>
<span data-ttu-id="07bc1-140">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, data, fábricas, Copy, Activities, tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="07bc1-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="07bc1-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07bc1-141">RELATED LINKS</span></span>

<span data-ttu-id="07bc1-142">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="07bc1-142">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

