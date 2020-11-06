---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/invoke-azurermdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: b83e6604e854260814a949885d26968542e84efc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428515"
---
# <span data-ttu-id="96a5c-101">Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="96a5c-101">Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="96a5c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96a5c-102">SYNOPSIS</span></span>
<span data-ttu-id="96a5c-103">Atualiza o tempo de execução de integração de hospedagem automática.</span><span class="sxs-lookup"><span data-stu-id="96a5c-103">Upgrades self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96a5c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96a5c-104">SYNTAX</span></span>

### <span data-ttu-id="96a5c-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="96a5c-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96a5c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="96a5c-106">ByResourceId</span></span>
```
Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96a5c-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="96a5c-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96a5c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="96a5c-108">DESCRIPTION</span></span>
<span data-ttu-id="96a5c-109">O cmdlet **Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade** atualiza o tempo de execução de integração de hospedagem interna se a nova versão estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="96a5c-109">The **Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="96a5c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96a5c-110">EXAMPLES</span></span>

### <span data-ttu-id="96a5c-111">Exemplo 1: atualiza um Runtime de integração de hospedagem interna</span><span class="sxs-lookup"><span data-stu-id="96a5c-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="96a5c-112">O cmdlet atualiza o tempo de execução de integração de hospedagem interna chamado "Test-selfhost-IV" no data Factory "Test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="96a5c-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="96a5c-113">OS</span><span class="sxs-lookup"><span data-stu-id="96a5c-113">PARAMETERS</span></span>

### <span data-ttu-id="96a5c-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="96a5c-114">-DataFactoryName</span></span>
<span data-ttu-id="96a5c-115">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="96a5c-115">The data factory name.</span></span>

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

### <span data-ttu-id="96a5c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96a5c-116">-DefaultProfile</span></span>
<span data-ttu-id="96a5c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96a5c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96a5c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96a5c-118">-InputObject</span></span>
<span data-ttu-id="96a5c-119">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="96a5c-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="96a5c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="96a5c-120">-Name</span></span>
<span data-ttu-id="96a5c-121">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="96a5c-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="96a5c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96a5c-122">-ResourceGroupName</span></span>
<span data-ttu-id="96a5c-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="96a5c-123">The resource group name.</span></span>

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

### <span data-ttu-id="96a5c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96a5c-124">-ResourceId</span></span>
<span data-ttu-id="96a5c-125">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="96a5c-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="96a5c-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="96a5c-126">-Confirm</span></span>
<span data-ttu-id="96a5c-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96a5c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96a5c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96a5c-128">-WhatIf</span></span>
<span data-ttu-id="96a5c-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="96a5c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96a5c-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="96a5c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96a5c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96a5c-131">CommonParameters</span></span>
<span data-ttu-id="96a5c-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96a5c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96a5c-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96a5c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96a5c-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="96a5c-134">INPUTS</span></span>

### <span data-ttu-id="96a5c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="96a5c-135">System.String</span></span>

### <span data-ttu-id="96a5c-136">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="96a5c-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="96a5c-137">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="96a5c-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="96a5c-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="96a5c-138">OUTPUTS</span></span>

### <span data-ttu-id="96a5c-139">System. void</span><span class="sxs-lookup"><span data-stu-id="96a5c-139">System.Void</span></span>

## <span data-ttu-id="96a5c-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="96a5c-140">NOTES</span></span>
<span data-ttu-id="96a5c-141">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, data, fábricas, Copy, Activities, tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="96a5c-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="96a5c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96a5c-142">RELATED LINKS</span></span>

<span data-ttu-id="96a5c-143">[Set-AzureRmDataFactoryV2IntegrationRuntime]() 
 [Get-AzureRmDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="96a5c-143">[Set-AzureRmDataFactoryV2IntegrationRuntime]()
[Get-AzureRmDataFactoryV2IntegrationRuntime]()</span></span>

