---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 91694efaeaf1a24018269706f3ee388feb7218ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262421"
---
# <span data-ttu-id="c14e4-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="c14e4-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="c14e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c14e4-102">SYNOPSIS</span></span>
<span data-ttu-id="c14e4-103">Lista todos os aprimoramentos de mensagens ou uma mensagem específica encompletada para o seu hub IoT.</span><span class="sxs-lookup"><span data-stu-id="c14e4-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="c14e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c14e4-104">SYNTAX</span></span>

### <span data-ttu-id="c14e4-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c14e4-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c14e4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c14e4-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c14e4-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="c14e4-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c14e4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c14e4-108">DESCRIPTION</span></span>
<span data-ttu-id="c14e4-109">Para obter uma explicação detalhada dos aprimoramentos de mensagens no Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="c14e4-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="c14e4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c14e4-110">EXAMPLES</span></span>

### <span data-ttu-id="c14e4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c14e4-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="c14e4-112">Listar todas as mensagens aprimoradas no MyIotHub</span><span class="sxs-lookup"><span data-stu-id="c14e4-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="c14e4-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c14e4-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="c14e4-114">Mostrar detalhes sobre o "newKey" da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c14e4-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="c14e4-115">OS</span><span class="sxs-lookup"><span data-stu-id="c14e4-115">PARAMETERS</span></span>

### <span data-ttu-id="c14e4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c14e4-116">-DefaultProfile</span></span>
<span data-ttu-id="c14e4-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c14e4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c14e4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c14e4-118">-InputObject</span></span>
<span data-ttu-id="c14e4-119">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="c14e4-119">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c14e4-120">-Chave</span><span class="sxs-lookup"><span data-stu-id="c14e4-120">-Key</span></span>
<span data-ttu-id="c14e4-121">A chave do encompletamento.</span><span class="sxs-lookup"><span data-stu-id="c14e4-121">The enrichment's key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14e4-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c14e4-122">-Name</span></span>
<span data-ttu-id="c14e4-123">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="c14e4-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14e4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c14e4-124">-ResourceGroupName</span></span>
<span data-ttu-id="c14e4-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c14e4-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14e4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c14e4-126">-ResourceId</span></span>
<span data-ttu-id="c14e4-127">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="c14e4-127">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c14e4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c14e4-128">CommonParameters</span></span>
<span data-ttu-id="c14e4-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c14e4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c14e4-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c14e4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c14e4-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c14e4-131">INPUTS</span></span>

### <span data-ttu-id="c14e4-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c14e4-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c14e4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c14e4-133">System.String</span></span>

## <span data-ttu-id="c14e4-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c14e4-134">OUTPUTS</span></span>

### <span data-ttu-id="c14e4-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="c14e4-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="c14e4-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSEnrichmentProperties []</span><span class="sxs-lookup"><span data-stu-id="c14e4-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="c14e4-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c14e4-137">NOTES</span></span>

## <span data-ttu-id="c14e4-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c14e4-138">RELATED LINKS</span></span>
