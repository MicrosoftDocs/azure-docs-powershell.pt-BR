---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 6cfda34b1718cfd73108362ee81fbe9c638310c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778373"
---
# <span data-ttu-id="09f4c-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="09f4c-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="09f4c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09f4c-102">SYNOPSIS</span></span>
<span data-ttu-id="09f4c-103">Obtém chaves para um tempo de execução de integração de hospedagem interna.</span><span class="sxs-lookup"><span data-stu-id="09f4c-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="09f4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09f4c-104">SYNTAX</span></span>

### <span data-ttu-id="09f4c-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="09f4c-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09f4c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="09f4c-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="09f4c-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="09f4c-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09f4c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09f4c-108">DESCRIPTION</span></span>
<span data-ttu-id="09f4c-109">Obter chaves para um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="09f4c-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="09f4c-110">As chaves são usadas para registrar um nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="09f4c-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="09f4c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09f4c-111">EXAMPLES</span></span>

### <span data-ttu-id="09f4c-112">Exemplo 1: obter chaves de tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="09f4c-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="09f4c-113">O cmdlet recupera chaves para um tempo de execução de integração chamado "Test-selfhost-IV".</span><span class="sxs-lookup"><span data-stu-id="09f4c-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="09f4c-114">OS</span><span class="sxs-lookup"><span data-stu-id="09f4c-114">PARAMETERS</span></span>

### <span data-ttu-id="09f4c-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="09f4c-115">-DataFactoryName</span></span>
<span data-ttu-id="09f4c-116">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="09f4c-116">The data factory name.</span></span>

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

### <span data-ttu-id="09f4c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f4c-117">-DefaultProfile</span></span>
<span data-ttu-id="09f4c-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09f4c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09f4c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09f4c-119">-InputObject</span></span>
<span data-ttu-id="09f4c-120">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="09f4c-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="09f4c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="09f4c-121">-Name</span></span>
<span data-ttu-id="09f4c-122">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="09f4c-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="09f4c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09f4c-123">-ResourceGroupName</span></span>
<span data-ttu-id="09f4c-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="09f4c-124">The resource group name.</span></span>

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

### <span data-ttu-id="09f4c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09f4c-125">-ResourceId</span></span>
<span data-ttu-id="09f4c-126">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="09f4c-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="09f4c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f4c-127">CommonParameters</span></span>
<span data-ttu-id="09f4c-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09f4c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f4c-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09f4c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f4c-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09f4c-130">INPUTS</span></span>

### <span data-ttu-id="09f4c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="09f4c-131">System.String</span></span>

### <span data-ttu-id="09f4c-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="09f4c-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="09f4c-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09f4c-133">OUTPUTS</span></span>

### <span data-ttu-id="09f4c-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="09f4c-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="09f4c-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09f4c-135">NOTES</span></span>

## <span data-ttu-id="09f4c-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09f4c-136">RELATED LINKS</span></span>

[<span data-ttu-id="09f4c-137">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="09f4c-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
