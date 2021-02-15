---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 3500cf71bb09bec4b204acc0bbf56f185f6ff647
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118725"
---
# <span data-ttu-id="47f3b-101">Get-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="47f3b-101">Get-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="47f3b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="47f3b-103">Obtém conexões privadas do ponto de extremidade com o serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="47f3b-103">Gets private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="47f3b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47f3b-104">SYNTAX</span></span>

### <span data-ttu-id="47f3b-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="47f3b-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47f3b-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47f3b-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ParentObject] <PSSearchService> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47f3b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47f3b-107">ResourceIdParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47f3b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="47f3b-108">DESCRIPTION</span></span>
<span data-ttu-id="47f3b-109">O cmdlet **Get-AzSearchPrivateEndpointConnection** obtém as conexões de ponto de extremidade particulares com o serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="47f3b-109">The **Get-AzSearchPrivateEndpointConnection** cmdlet gets the private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="47f3b-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="47f3b-110">EXAMPLES</span></span>

### <span data-ttu-id="47f3b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="47f3b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap

Name                                                          Id
----                                                          --
arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266 /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="47f3b-112">O exemplo obtém todas as conexões de ponto de extremidade particulares com o serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="47f3b-112">The example gets all the private endpoint connections to the Azure Cognitive Search service.</span></span>

### <span data-ttu-id="47f3b-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="47f3b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266  | ConvertTo-Json

{
  "Name": "arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "PrivateEndpoint": {
    "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann2/providers/Microsoft.Network/privateEndpoints/arjagann-test-cuseuap-pe"
  },
  "PrivateLinkServiceConnectionState": {
    "Status": 1,
    "Description": "Auto-approved",
    "ActionsRequired": "None"
  }
}
```

<span data-ttu-id="47f3b-114">O exemplo obtém uma conexão de ponto de extremidade particular específica por nome (convertida em JSON para facilitar a leitura) para o serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="47f3b-114">The example gets a specific private endpoint connection by name (converted to JSON for ease of reading) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="47f3b-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47f3b-115">PARAMETERS</span></span>

### <span data-ttu-id="47f3b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47f3b-116">-DefaultProfile</span></span>
<span data-ttu-id="47f3b-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47f3b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47f3b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="47f3b-118">-Name</span></span>
<span data-ttu-id="47f3b-119">Nome de conexão privada do Serviço de Pesquisa Cognitiva do Azure</span><span class="sxs-lookup"><span data-stu-id="47f3b-119">Azure Cognitive Search Service private endpoint connection name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f3b-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="47f3b-120">-ParentObject</span></span>
<span data-ttu-id="47f3b-121">Objeto de entrada do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="47f3b-121">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47f3b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47f3b-122">-ResourceGroupName</span></span>
<span data-ttu-id="47f3b-123">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="47f3b-123">Resource Group name.</span></span>

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

### <span data-ttu-id="47f3b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47f3b-124">-ResourceId</span></span>
<span data-ttu-id="47f3b-125">ID do recurso de serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="47f3b-125">Private link service resource id</span></span>

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

### <span data-ttu-id="47f3b-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="47f3b-126">-ServiceName</span></span>
<span data-ttu-id="47f3b-127">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="47f3b-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="47f3b-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="47f3b-128">-Confirm</span></span>
<span data-ttu-id="47f3b-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47f3b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47f3b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47f3b-130">-WhatIf</span></span>
<span data-ttu-id="47f3b-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="47f3b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47f3b-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47f3b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47f3b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47f3b-133">CommonParameters</span></span>
<span data-ttu-id="47f3b-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47f3b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47f3b-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47f3b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47f3b-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="47f3b-136">INPUTS</span></span>

### <span data-ttu-id="47f3b-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="47f3b-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="47f3b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="47f3b-138">System.String</span></span>

## <span data-ttu-id="47f3b-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="47f3b-139">OUTPUTS</span></span>

### <span data-ttu-id="47f3b-140">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="47f3b-140">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span></span>

## <span data-ttu-id="47f3b-141">Notas</span><span class="sxs-lookup"><span data-stu-id="47f3b-141">NOTES</span></span>

## <span data-ttu-id="47f3b-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47f3b-142">RELATED LINKS</span></span>

[<span data-ttu-id="47f3b-143">Remove-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="47f3b-143">Remove-AzSearchPrivateEndpointConnection.md</span></span>](./Remove-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="47f3b-144">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="47f3b-144">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)
