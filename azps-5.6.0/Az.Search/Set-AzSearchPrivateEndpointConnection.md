---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/set-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: d67108e935d4f3ef14522f792a06f975d98be803
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887955"
---
# <span data-ttu-id="81d4d-101">Set-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="81d4d-101">Set-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="81d4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="81d4d-103">Atualize a conexão de ponto de extremidade privada para o serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="81d4d-103">Update the private endpoint connection to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="81d4d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="81d4d-104">SYNTAX</span></span>

### <span data-ttu-id="81d4d-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="81d4d-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81d4d-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81d4d-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection -ParentObject <PSSearchService> [-Name] <String>
 -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81d4d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81d4d-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection [-ResourceId] <String> -Status <PSPrivateLinkServiceConnectionStatus>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81d4d-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81d4d-108">InputObjectParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 -InputObject <PSPrivateEndpointConnection> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81d4d-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="81d4d-109">DESCRIPTION</span></span>
<span data-ttu-id="81d4d-110">O **Set-AzSearchPrivateEndpointConnection** atualiza a conexão de ponto de extremidade privada com o serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="81d4d-110">The **Set-AzSearchPrivateEndpointConnection** updates the private endpoint connection to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="81d4d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81d4d-111">EXAMPLES</span></span>

### <span data-ttu-id="81d4d-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="81d4d-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266 -Status Rejected  -Description "Rejected" | ConvertTo-Json

{
  "Name": "arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "PrivateEndpoint": {
    "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann2/providers/Microsoft.Network/privateEndpoints/arjagann-test-cuseuap-pe"
  },
  "PrivateLinkServiceConnectionState": {
    "Status": 2,
    "Description": "Rejected",
    "ActionsRequired": "None"
  }
}
```

<span data-ttu-id="81d4d-113">Este exemplo atualiza o status de uma conexão de ponto de extremidade privada do serviço de Pesquisa Cognitiva do Azure para ser "Rejeitado".</span><span class="sxs-lookup"><span data-stu-id="81d4d-113">This example updates a private endpoint connection's status of the Azure Cognitive Search service to be "Rejected".</span></span>

## <span data-ttu-id="81d4d-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="81d4d-114">PARAMETERS</span></span>

### <span data-ttu-id="81d4d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d4d-115">-DefaultProfile</span></span>
<span data-ttu-id="81d4d-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81d4d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81d4d-117">-Description</span><span class="sxs-lookup"><span data-stu-id="81d4d-117">-Description</span></span>
<span data-ttu-id="81d4d-118">Descrição da conexão de ponto de extremidade privada</span><span class="sxs-lookup"><span data-stu-id="81d4d-118">Private endpoint connection description</span></span>

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

### <span data-ttu-id="81d4d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81d4d-119">-InputObject</span></span>
<span data-ttu-id="81d4d-120">Objeto de entrada de conexão de ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="81d4d-120">Private endpoint connection input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81d4d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="81d4d-121">-Name</span></span>
<span data-ttu-id="81d4d-122">Nome da conexão de ponto de extremidade privada do Serviço de Pesquisa Cognitiva do Azure</span><span class="sxs-lookup"><span data-stu-id="81d4d-122">Azure Cognitive Search Service private endpoint connection name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d4d-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="81d4d-123">-ParentObject</span></span>
<span data-ttu-id="81d4d-124">Objeto de entrada do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="81d4d-124">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81d4d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81d4d-125">-ResourceGroupName</span></span>
<span data-ttu-id="81d4d-126">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="81d4d-126">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d4d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81d4d-127">-ResourceId</span></span>
<span data-ttu-id="81d4d-128">ID do recurso de serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="81d4d-128">Private link service resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81d4d-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="81d4d-129">-ServiceName</span></span>
<span data-ttu-id="81d4d-130">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="81d4d-130">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d4d-131">-Status</span><span class="sxs-lookup"><span data-stu-id="81d4d-131">-Status</span></span>
<span data-ttu-id="81d4d-132">Status da conexão do serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="81d4d-132">Private link service connection status</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSPrivateLinkServiceConnectionStatus
Parameter Sets: (All)
Aliases:
Accepted values: Pending, Approved, Rejected, Disconnected

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d4d-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81d4d-133">-Confirm</span></span>
<span data-ttu-id="81d4d-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81d4d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81d4d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81d4d-135">-WhatIf</span></span>
<span data-ttu-id="81d4d-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="81d4d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81d4d-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="81d4d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81d4d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d4d-138">CommonParameters</span></span>
<span data-ttu-id="81d4d-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81d4d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d4d-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81d4d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d4d-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81d4d-141">INPUTS</span></span>

### <span data-ttu-id="81d4d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="81d4d-142">System.String</span></span>

## <span data-ttu-id="81d4d-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="81d4d-143">OUTPUTS</span></span>

### <span data-ttu-id="81d4d-144">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="81d4d-144">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span></span>

## <span data-ttu-id="81d4d-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="81d4d-145">NOTES</span></span>

## <span data-ttu-id="81d4d-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81d4d-146">RELATED LINKS</span></span>

[<span data-ttu-id="81d4d-147">Get-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="81d4d-147">Get-AzSearchPrivateEndpointConnection.md</span></span>](./Get-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="81d4d-148">Remove-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="81d4d-148">Remove-AzSearchPrivateEndpointConnection.md</span></span>](./Remove-AzSearchPrivateEndpointConnection.md)
