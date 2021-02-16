---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 6cfda34b1718cfd73108362ee81fbe9c638310c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117746"
---
# <span data-ttu-id="61e3e-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="61e3e-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="61e3e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61e3e-102">SYNOPSIS</span></span>
<span data-ttu-id="61e3e-103">Obtém chaves para um tempo de execução de integração auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="61e3e-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="61e3e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61e3e-104">SYNTAX</span></span>

### <span data-ttu-id="61e3e-105">ByIntegrationRuntimeName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="61e3e-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61e3e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="61e3e-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61e3e-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="61e3e-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61e3e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="61e3e-108">DESCRIPTION</span></span>
<span data-ttu-id="61e3e-109">Obter chaves para um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="61e3e-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="61e3e-110">As teclas são usadas para registrar um nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="61e3e-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="61e3e-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="61e3e-111">EXAMPLES</span></span>

### <span data-ttu-id="61e3e-112">Exemplo 1: Obter chaves de tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="61e3e-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="61e3e-113">O cmdlet recupera chaves para um tempo de execução de integração chamado "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="61e3e-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="61e3e-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61e3e-114">PARAMETERS</span></span>

### <span data-ttu-id="61e3e-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="61e3e-115">-DataFactoryName</span></span>
<span data-ttu-id="61e3e-116">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="61e3e-116">The data factory name.</span></span>

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

### <span data-ttu-id="61e3e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61e3e-117">-DefaultProfile</span></span>
<span data-ttu-id="61e3e-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="61e3e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61e3e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61e3e-119">-InputObject</span></span>
<span data-ttu-id="61e3e-120">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="61e3e-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="61e3e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="61e3e-121">-Name</span></span>
<span data-ttu-id="61e3e-122">O nome de tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="61e3e-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="61e3e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61e3e-123">-ResourceGroupName</span></span>
<span data-ttu-id="61e3e-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="61e3e-124">The resource group name.</span></span>

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

### <span data-ttu-id="61e3e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61e3e-125">-ResourceId</span></span>
<span data-ttu-id="61e3e-126">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="61e3e-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="61e3e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e3e-127">CommonParameters</span></span>
<span data-ttu-id="61e3e-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61e3e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e3e-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61e3e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e3e-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="61e3e-130">INPUTS</span></span>

### <span data-ttu-id="61e3e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="61e3e-131">System.String</span></span>

### <span data-ttu-id="61e3e-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="61e3e-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="61e3e-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="61e3e-133">OUTPUTS</span></span>

### <span data-ttu-id="61e3e-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="61e3e-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="61e3e-135">Notas</span><span class="sxs-lookup"><span data-stu-id="61e3e-135">NOTES</span></span>

## <span data-ttu-id="61e3e-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61e3e-136">RELATED LINKS</span></span>

[<span data-ttu-id="61e3e-137">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="61e3e-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
