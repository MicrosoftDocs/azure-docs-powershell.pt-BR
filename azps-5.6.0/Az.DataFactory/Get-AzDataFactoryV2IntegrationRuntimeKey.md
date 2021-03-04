---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: fc47b71b1546fe351f9d535da4ef9942af66f19e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888293"
---
# <span data-ttu-id="d3071-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="d3071-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="d3071-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3071-102">SYNOPSIS</span></span>
<span data-ttu-id="d3071-103">Obtém chaves para um tempo de execução de integração auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="d3071-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="d3071-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d3071-104">SYNTAX</span></span>

### <span data-ttu-id="d3071-105">ByIntegrationRuntimeName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d3071-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3071-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d3071-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3071-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="d3071-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3071-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d3071-108">DESCRIPTION</span></span>
<span data-ttu-id="d3071-109">Obter chaves para um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="d3071-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="d3071-110">As chaves são usadas para registrar um nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="d3071-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="d3071-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3071-111">EXAMPLES</span></span>

### <span data-ttu-id="d3071-112">Exemplo 1: Obter chaves de tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="d3071-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="d3071-113">O cmdlet recupera chaves para um tempo de execução de integração chamado 'test-selfhost-ir'.</span><span class="sxs-lookup"><span data-stu-id="d3071-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="d3071-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d3071-114">PARAMETERS</span></span>

### <span data-ttu-id="d3071-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d3071-115">-DataFactoryName</span></span>
<span data-ttu-id="d3071-116">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="d3071-116">The data factory name.</span></span>

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

### <span data-ttu-id="d3071-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3071-117">-DefaultProfile</span></span>
<span data-ttu-id="d3071-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d3071-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3071-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3071-119">-InputObject</span></span>
<span data-ttu-id="d3071-120">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="d3071-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="d3071-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d3071-121">-Name</span></span>
<span data-ttu-id="d3071-122">O nome do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="d3071-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="d3071-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3071-123">-ResourceGroupName</span></span>
<span data-ttu-id="d3071-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d3071-124">The resource group name.</span></span>

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

### <span data-ttu-id="d3071-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3071-125">-ResourceId</span></span>
<span data-ttu-id="d3071-126">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="d3071-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d3071-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3071-127">CommonParameters</span></span>
<span data-ttu-id="d3071-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3071-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3071-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3071-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3071-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3071-130">INPUTS</span></span>

### <span data-ttu-id="d3071-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d3071-131">System.String</span></span>

### <span data-ttu-id="d3071-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d3071-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d3071-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d3071-133">OUTPUTS</span></span>

### <span data-ttu-id="d3071-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="d3071-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="d3071-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="d3071-135">NOTES</span></span>

## <span data-ttu-id="d3071-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3071-136">RELATED LINKS</span></span>

[<span data-ttu-id="d3071-137">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="d3071-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
