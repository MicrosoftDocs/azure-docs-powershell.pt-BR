---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: eda4cb403381bd41f7be471b91b2cbba3a6d2ad3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118114"
---
# <span data-ttu-id="81814-101">Set-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="81814-101">Set-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="81814-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81814-102">SYNOPSIS</span></span>
<span data-ttu-id="81814-103">Atualize a conexão de ponto de extremidade particular para o serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="81814-103">Update the private endpoint connection to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="81814-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81814-104">SYNTAX</span></span>

### <span data-ttu-id="81814-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="81814-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81814-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81814-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection -ParentObject <PSSearchService> [-Name] <String>
 -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81814-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81814-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection [-ResourceId] <String> -Status <PSPrivateLinkServiceConnectionStatus>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81814-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81814-108">InputObjectParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 -InputObject <PSPrivateEndpointConnection> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81814-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="81814-109">DESCRIPTION</span></span>
<span data-ttu-id="81814-110">O **Set-AzSearchPrivateEndpointConnection** atualiza a conexão de ponto de extremidade particular para o serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="81814-110">The **Set-AzSearchPrivateEndpointConnection** updates the private endpoint connection to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="81814-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="81814-111">EXAMPLES</span></span>

### <span data-ttu-id="81814-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="81814-112">Example 1</span></span>
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

<span data-ttu-id="81814-113">Este exemplo atualiza o status de uma conexão de ponto de extremidade particular do serviço de Pesquisa Cognitiva do Azure para ser "Rejeitado".</span><span class="sxs-lookup"><span data-stu-id="81814-113">This example updates a private endpoint connection's status of the Azure Cognitive Search service to be "Rejected".</span></span>

## <span data-ttu-id="81814-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81814-114">PARAMETERS</span></span>

### <span data-ttu-id="81814-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81814-115">-DefaultProfile</span></span>
<span data-ttu-id="81814-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81814-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81814-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="81814-117">-Description</span></span>
<span data-ttu-id="81814-118">Descrição da conexão privada do ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="81814-118">Private endpoint connection description</span></span>

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

### <span data-ttu-id="81814-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81814-119">-InputObject</span></span>
<span data-ttu-id="81814-120">Objeto de entrada de conexão de ponto de extremidade particular</span><span class="sxs-lookup"><span data-stu-id="81814-120">Private endpoint connection input object</span></span>

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

### <span data-ttu-id="81814-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="81814-121">-Name</span></span>
<span data-ttu-id="81814-122">Nome de conexão privada do Serviço de Pesquisa Cognitiva do Azure</span><span class="sxs-lookup"><span data-stu-id="81814-122">Azure Cognitive Search Service private endpoint connection name</span></span>

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

### <span data-ttu-id="81814-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="81814-123">-ParentObject</span></span>
<span data-ttu-id="81814-124">Objeto de entrada do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="81814-124">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="81814-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81814-125">-ResourceGroupName</span></span>
<span data-ttu-id="81814-126">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="81814-126">Resource Group name.</span></span>

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

### <span data-ttu-id="81814-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81814-127">-ResourceId</span></span>
<span data-ttu-id="81814-128">ID do recurso de serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="81814-128">Private link service resource id</span></span>

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

### <span data-ttu-id="81814-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="81814-129">-ServiceName</span></span>
<span data-ttu-id="81814-130">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="81814-130">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="81814-131">-Status</span><span class="sxs-lookup"><span data-stu-id="81814-131">-Status</span></span>
<span data-ttu-id="81814-132">Status da conexão do serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="81814-132">Private link service connection status</span></span>

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

### <span data-ttu-id="81814-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="81814-133">-Confirm</span></span>
<span data-ttu-id="81814-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81814-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81814-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81814-135">-WhatIf</span></span>
<span data-ttu-id="81814-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="81814-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81814-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="81814-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81814-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81814-138">CommonParameters</span></span>
<span data-ttu-id="81814-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81814-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81814-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81814-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81814-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="81814-141">INPUTS</span></span>

### <span data-ttu-id="81814-142">System.String</span><span class="sxs-lookup"><span data-stu-id="81814-142">System.String</span></span>

## <span data-ttu-id="81814-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="81814-143">OUTPUTS</span></span>

### <span data-ttu-id="81814-144">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="81814-144">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span></span>

## <span data-ttu-id="81814-145">Notas</span><span class="sxs-lookup"><span data-stu-id="81814-145">NOTES</span></span>

## <span data-ttu-id="81814-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81814-146">RELATED LINKS</span></span>

[<span data-ttu-id="81814-147">Get-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="81814-147">Get-AzSearchPrivateEndpointConnection.md</span></span>](./Get-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="81814-148">Remove-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="81814-148">Remove-AzSearchPrivateEndpointConnection.md</span></span>](./Remove-AzSearchPrivateEndpointConnection.md)
