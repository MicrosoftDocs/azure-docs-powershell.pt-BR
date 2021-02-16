---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 91694efaeaf1a24018269706f3ee388feb7218ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113139"
---
# <span data-ttu-id="ca0a5-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ca0a5-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="ca0a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca0a5-102">SYNOPSIS</span></span>
<span data-ttu-id="ca0a5-103">Lista todos os enriquecimentos de mensagens ou um enriquecimento de mensagens específico para seu Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="ca0a5-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="ca0a5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca0a5-104">SYNTAX</span></span>

### <span data-ttu-id="ca0a5-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ca0a5-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca0a5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ca0a5-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca0a5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ca0a5-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca0a5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca0a5-108">DESCRIPTION</span></span>
<span data-ttu-id="ca0a5-109">Para uma explicação detalhada dos enriquecimentos de mensagens no Hub do Azure IoT, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="ca0a5-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="ca0a5-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ca0a5-110">EXAMPLES</span></span>

### <span data-ttu-id="ca0a5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ca0a5-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="ca0a5-112">Listar todos os enriquecimentos de mensagens no MyIotHub</span><span class="sxs-lookup"><span data-stu-id="ca0a5-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="ca0a5-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ca0a5-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="ca0a5-114">Mostrar detalhes sobre o enriquecimento de mensagens "newKey".</span><span class="sxs-lookup"><span data-stu-id="ca0a5-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="ca0a5-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca0a5-115">PARAMETERS</span></span>

### <span data-ttu-id="ca0a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca0a5-116">-DefaultProfile</span></span>
<span data-ttu-id="ca0a5-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca0a5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca0a5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca0a5-118">-InputObject</span></span>
<span data-ttu-id="ca0a5-119">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="ca0a5-119">IotHub object</span></span>

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

### <span data-ttu-id="ca0a5-120">-Tecla</span><span class="sxs-lookup"><span data-stu-id="ca0a5-120">-Key</span></span>
<span data-ttu-id="ca0a5-121">A chave do enriquecimento.</span><span class="sxs-lookup"><span data-stu-id="ca0a5-121">The enrichment's key.</span></span>

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

### <span data-ttu-id="ca0a5-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca0a5-122">-Name</span></span>
<span data-ttu-id="ca0a5-123">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="ca0a5-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ca0a5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca0a5-124">-ResourceGroupName</span></span>
<span data-ttu-id="ca0a5-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="ca0a5-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ca0a5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca0a5-126">-ResourceId</span></span>
<span data-ttu-id="ca0a5-127">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="ca0a5-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ca0a5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca0a5-128">CommonParameters</span></span>
<span data-ttu-id="ca0a5-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca0a5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca0a5-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca0a5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca0a5-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="ca0a5-131">INPUTS</span></span>

### <span data-ttu-id="ca0a5-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ca0a5-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ca0a5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ca0a5-133">System.String</span></span>

## <span data-ttu-id="ca0a5-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="ca0a5-134">OUTPUTS</span></span>

### <span data-ttu-id="ca0a5-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEntricmentMetadata</span><span class="sxs-lookup"><span data-stu-id="ca0a5-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="ca0a5-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEntricmentProperties[]</span><span class="sxs-lookup"><span data-stu-id="ca0a5-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="ca0a5-137">Notas</span><span class="sxs-lookup"><span data-stu-id="ca0a5-137">NOTES</span></span>

## <span data-ttu-id="ca0a5-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca0a5-138">RELATED LINKS</span></span>
