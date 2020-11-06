---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 7bab6fb42e5d50cc0ede06a42540cf628a5ee4a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440203"
---
# <span data-ttu-id="53ad8-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="53ad8-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="53ad8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="53ad8-103">Obtém chaves para um tempo de execução de integração de hospedagem interna.</span><span class="sxs-lookup"><span data-stu-id="53ad8-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53ad8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53ad8-104">SYNTAX</span></span>

### <span data-ttu-id="53ad8-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="53ad8-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53ad8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="53ad8-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53ad8-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="53ad8-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53ad8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53ad8-108">DESCRIPTION</span></span>
<span data-ttu-id="53ad8-109">Obter chaves para um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="53ad8-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="53ad8-110">As chaves são usadas para registrar um nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="53ad8-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="53ad8-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53ad8-111">EXAMPLES</span></span>

### <span data-ttu-id="53ad8-112">Exemplo 1: obter chaves de tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="53ad8-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="53ad8-113">O cmdlet recupera chaves para um tempo de execução de integração chamado "Test-selfhost-IV".</span><span class="sxs-lookup"><span data-stu-id="53ad8-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="53ad8-114">OS</span><span class="sxs-lookup"><span data-stu-id="53ad8-114">PARAMETERS</span></span>

### <span data-ttu-id="53ad8-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="53ad8-115">-DataFactoryName</span></span>
<span data-ttu-id="53ad8-116">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="53ad8-116">The data factory name.</span></span>

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

### <span data-ttu-id="53ad8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53ad8-117">-InputObject</span></span>
<span data-ttu-id="53ad8-118">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="53ad8-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="53ad8-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="53ad8-119">-Name</span></span>
<span data-ttu-id="53ad8-120">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="53ad8-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="53ad8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53ad8-121">-ResourceGroupName</span></span>
<span data-ttu-id="53ad8-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="53ad8-122">The resource group name.</span></span>

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

### <span data-ttu-id="53ad8-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53ad8-123">-ResourceId</span></span>
<span data-ttu-id="53ad8-124">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="53ad8-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="53ad8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53ad8-125">-DefaultProfile</span></span>
<span data-ttu-id="53ad8-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53ad8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53ad8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53ad8-127">CommonParameters</span></span>
<span data-ttu-id="53ad8-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53ad8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53ad8-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53ad8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53ad8-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53ad8-130">INPUTS</span></span>

### <span data-ttu-id="53ad8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="53ad8-131">System.String</span></span>
<span data-ttu-id="53ad8-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="53ad8-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 

## <span data-ttu-id="53ad8-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53ad8-133">OUTPUTS</span></span>

### <span data-ttu-id="53ad8-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="53ad8-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="53ad8-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53ad8-135">NOTES</span></span>

## <span data-ttu-id="53ad8-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53ad8-136">RELATED LINKS</span></span>

[<span data-ttu-id="53ad8-137">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="53ad8-137">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()