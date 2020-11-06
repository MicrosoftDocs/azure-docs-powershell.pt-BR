---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 42ccd34e299439d3288a8a587ce9d62abe198847
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441131"
---
# <span data-ttu-id="842d7-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="842d7-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="842d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="842d7-102">SYNOPSIS</span></span>
<span data-ttu-id="842d7-103">Obtém chaves para um tempo de execução de integração de hospedagem interna.</span><span class="sxs-lookup"><span data-stu-id="842d7-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="842d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="842d7-104">SYNTAX</span></span>

### <span data-ttu-id="842d7-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="842d7-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="842d7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="842d7-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String>
```

### <span data-ttu-id="842d7-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="842d7-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="842d7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="842d7-108">DESCRIPTION</span></span>
<span data-ttu-id="842d7-109">Obter chaves para um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="842d7-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="842d7-110">As chaves são usadas para registrar um nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="842d7-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="842d7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="842d7-111">EXAMPLES</span></span>

### <span data-ttu-id="842d7-112">Exemplo 1: obter chaves de tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="842d7-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="842d7-113">O cmdlet recupera chaves para um tempo de execução de integração chamado "Test-selfhost-IV".</span><span class="sxs-lookup"><span data-stu-id="842d7-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="842d7-114">OS</span><span class="sxs-lookup"><span data-stu-id="842d7-114">PARAMETERS</span></span>

### <span data-ttu-id="842d7-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="842d7-115">-DataFactoryName</span></span>
<span data-ttu-id="842d7-116">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="842d7-116">The data factory name.</span></span>

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

### <span data-ttu-id="842d7-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="842d7-117">-InputObject</span></span>
<span data-ttu-id="842d7-118">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="842d7-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="842d7-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="842d7-119">-Name</span></span>
<span data-ttu-id="842d7-120">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="842d7-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="842d7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="842d7-121">-ResourceGroupName</span></span>
<span data-ttu-id="842d7-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="842d7-122">The resource group name.</span></span>

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

### <span data-ttu-id="842d7-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="842d7-123">-ResourceId</span></span>
<span data-ttu-id="842d7-124">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="842d7-124">The Azure resource ID.</span></span>

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

## <span data-ttu-id="842d7-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="842d7-125">INPUTS</span></span>

### <span data-ttu-id="842d7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="842d7-126">System.String</span></span>
<span data-ttu-id="842d7-127">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="842d7-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 


## <span data-ttu-id="842d7-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="842d7-128">OUTPUTS</span></span>

### <span data-ttu-id="842d7-129">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="842d7-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>


## <span data-ttu-id="842d7-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="842d7-130">NOTES</span></span>

## <span data-ttu-id="842d7-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="842d7-131">RELATED LINKS</span></span>
[<span data-ttu-id="842d7-132">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="842d7-132">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
