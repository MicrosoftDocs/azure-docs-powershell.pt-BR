---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: eb248e1059da6dcab581e4fba8b3eac7f970bb30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431012"
---
# <span data-ttu-id="8c7b0-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="8c7b0-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="8c7b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c7b0-102">SYNOPSIS</span></span>
<span data-ttu-id="8c7b0-103">Obtém chaves para um tempo de execução de integração de hospedagem interna.</span><span class="sxs-lookup"><span data-stu-id="8c7b0-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c7b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c7b0-104">SYNTAX</span></span>

### <span data-ttu-id="8c7b0-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8c7b0-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c7b0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8c7b0-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c7b0-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="8c7b0-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c7b0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c7b0-108">DESCRIPTION</span></span>
<span data-ttu-id="8c7b0-109">Obter chaves para um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="8c7b0-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="8c7b0-110">As chaves são usadas para registrar um nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="8c7b0-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="8c7b0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c7b0-111">EXAMPLES</span></span>

### <span data-ttu-id="8c7b0-112">Exemplo 1: obter chaves de tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="8c7b0-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="8c7b0-113">O cmdlet recupera chaves para um tempo de execução de integração chamado "Test-selfhost-IV".</span><span class="sxs-lookup"><span data-stu-id="8c7b0-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="8c7b0-114">OS</span><span class="sxs-lookup"><span data-stu-id="8c7b0-114">PARAMETERS</span></span>

### <span data-ttu-id="8c7b0-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="8c7b0-115">-DataFactoryName</span></span>
<span data-ttu-id="8c7b0-116">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="8c7b0-116">The data factory name.</span></span>

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

### <span data-ttu-id="8c7b0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c7b0-117">-DefaultProfile</span></span>
<span data-ttu-id="8c7b0-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c7b0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c7b0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c7b0-119">-InputObject</span></span>
<span data-ttu-id="8c7b0-120">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="8c7b0-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="8c7b0-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c7b0-121">-Name</span></span>
<span data-ttu-id="8c7b0-122">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="8c7b0-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="8c7b0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c7b0-123">-ResourceGroupName</span></span>
<span data-ttu-id="8c7b0-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8c7b0-124">The resource group name.</span></span>

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

### <span data-ttu-id="8c7b0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c7b0-125">-ResourceId</span></span>
<span data-ttu-id="8c7b0-126">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="8c7b0-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8c7b0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c7b0-127">CommonParameters</span></span>
<span data-ttu-id="8c7b0-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c7b0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c7b0-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c7b0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c7b0-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c7b0-130">INPUTS</span></span>

### <span data-ttu-id="8c7b0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8c7b0-131">System.String</span></span>
<span data-ttu-id="8c7b0-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8c7b0-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 

## <span data-ttu-id="8c7b0-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c7b0-133">OUTPUTS</span></span>

### <span data-ttu-id="8c7b0-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="8c7b0-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="8c7b0-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c7b0-135">NOTES</span></span>

## <span data-ttu-id="8c7b0-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c7b0-136">RELATED LINKS</span></span>

[<span data-ttu-id="8c7b0-137">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="8c7b0-137">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
