---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
ms.openlocfilehash: e67d70f91e523cd46755035abe951682b1764cbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115793"
---
# <span data-ttu-id="47e8a-101">Remove-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="47e8a-101">Remove-AzEventHubCluster</span></span>

## <span data-ttu-id="47e8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="47e8a-103">Exclui o Cluster Eventhub Dedicado especificado do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="47e8a-103">Deletes the specified Dedicated Eventhub Cluster from the ResourceGroup</span></span>

## <span data-ttu-id="47e8a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47e8a-104">SYNTAX</span></span>

### <span data-ttu-id="47e8a-105">ClusterPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="47e8a-105">ClusterPropertiesSet (Default)</span></span>
```
Remove-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47e8a-106">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="47e8a-106">ClusterInputObjectSet</span></span>
```
Remove-AzEventHubCluster [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47e8a-107">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47e8a-107">ClusterResourceIdParameterSet</span></span>
```
Remove-AzEventHubCluster [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47e8a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="47e8a-108">DESCRIPTION</span></span>
<span data-ttu-id="47e8a-109">O Remove-AzEventHubCluster cmdlet exclui o determinado nome de Cluster eventhub dedicado do determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="47e8a-109">The Remove-AzEventHubCluster cmdlet deletes the given dedicated eventhub Cluster name from the given resourcegroup</span></span>

## <span data-ttu-id="47e8a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="47e8a-110">EXAMPLES</span></span>

### <span data-ttu-id="47e8a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="47e8a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557
```

<span data-ttu-id="47e8a-112">Exclui o Cluster Eventhub-Cluster-5557 RSG-Cluster27651 grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="47e8a-112">Deletes Eventhub-Cluster-5557 Cluster from RSG-Cluster27651 resourcegroup</span></span>

## <span data-ttu-id="47e8a-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47e8a-113">PARAMETERS</span></span>

### <span data-ttu-id="47e8a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47e8a-114">-AsJob</span></span>
<span data-ttu-id="47e8a-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="47e8a-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47e8a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47e8a-116">-DefaultProfile</span></span>
<span data-ttu-id="47e8a-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47e8a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47e8a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47e8a-118">-InputObject</span></span>
<span data-ttu-id="47e8a-119">Objeto cluster</span><span class="sxs-lookup"><span data-stu-id="47e8a-119">Cluster Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47e8a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="47e8a-120">-Name</span></span>
<span data-ttu-id="47e8a-121">Nome do Cluster</span><span class="sxs-lookup"><span data-stu-id="47e8a-121">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47e8a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47e8a-122">-PassThru</span></span>
<span data-ttu-id="47e8a-123">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="47e8a-123">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47e8a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47e8a-124">-ResourceGroupName</span></span>
<span data-ttu-id="47e8a-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="47e8a-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47e8a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47e8a-126">-ResourceId</span></span>
<span data-ttu-id="47e8a-127">ID do Recurso de Cluster</span><span class="sxs-lookup"><span data-stu-id="47e8a-127">Cluster Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47e8a-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="47e8a-128">-Confirm</span></span>
<span data-ttu-id="47e8a-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47e8a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47e8a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47e8a-130">-WhatIf</span></span>
<span data-ttu-id="47e8a-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="47e8a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47e8a-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47e8a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47e8a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47e8a-133">CommonParameters</span></span>
<span data-ttu-id="47e8a-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47e8a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47e8a-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47e8a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47e8a-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="47e8a-136">INPUTS</span></span>

### <span data-ttu-id="47e8a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="47e8a-137">System.String</span></span>

### <span data-ttu-id="47e8a-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="47e8a-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="47e8a-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="47e8a-139">OUTPUTS</span></span>

### <span data-ttu-id="47e8a-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="47e8a-140">System.Boolean</span></span>

## <span data-ttu-id="47e8a-141">Notas</span><span class="sxs-lookup"><span data-stu-id="47e8a-141">NOTES</span></span>

## <span data-ttu-id="47e8a-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47e8a-142">RELATED LINKS</span></span>
