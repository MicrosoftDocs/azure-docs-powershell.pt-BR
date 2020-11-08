---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricreliability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
ms.openlocfilehash: a63bcfe0f807f36ffae5c10e644322b1fb612325
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115848"
---
# <span data-ttu-id="966e2-101">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="966e2-101">Update-AzServiceFabricReliability</span></span>

## <span data-ttu-id="966e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="966e2-102">SYNOPSIS</span></span>
<span data-ttu-id="966e2-103">Atualize a camada de confiabilidade do tipo de nó primário em um cluster.</span><span class="sxs-lookup"><span data-stu-id="966e2-103">Update the reliability tier of the primary node type in a cluster.</span></span>

## <span data-ttu-id="966e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="966e2-104">SYNTAX</span></span>

```
Update-AzServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="966e2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="966e2-105">DESCRIPTION</span></span>
<span data-ttu-id="966e2-106">Use **Update-AzServiceFabricReliability** para atualizar a confiabilidade do tipo de nó primário em um cluster.</span><span class="sxs-lookup"><span data-stu-id="966e2-106">Use **Update-AzServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="966e2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="966e2-107">EXAMPLES</span></span>

### <span data-ttu-id="966e2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="966e2-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="966e2-109">Esse comando altera a camada de confiabilidade do tipo de nó principal para prata.</span><span class="sxs-lookup"><span data-stu-id="966e2-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="966e2-110">OS</span><span class="sxs-lookup"><span data-stu-id="966e2-110">PARAMETERS</span></span>

### <span data-ttu-id="966e2-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="966e2-111">-AutoAddNode</span></span>
<span data-ttu-id="966e2-112">Adicionar contagem de nós automaticamente ao alterar a confiabilidade</span><span class="sxs-lookup"><span data-stu-id="966e2-112">Add node count automatically when changing reliability</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: Auto

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="966e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="966e2-113">-DefaultProfile</span></span>
<span data-ttu-id="966e2-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="966e2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="966e2-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="966e2-115">-Name</span></span>
<span data-ttu-id="966e2-116">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="966e2-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="966e2-117">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="966e2-117">-ReliabilityLevel</span></span>
<span data-ttu-id="966e2-118">Nível de confiabilidade</span><span class="sxs-lookup"><span data-stu-id="966e2-118">Reliability tier</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, Bronze, Silver, Gold, Platinum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="966e2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="966e2-119">-ResourceGroupName</span></span>
<span data-ttu-id="966e2-120">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="966e2-120">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="966e2-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="966e2-121">-Confirm</span></span>
<span data-ttu-id="966e2-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="966e2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="966e2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="966e2-123">-WhatIf</span></span>
<span data-ttu-id="966e2-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="966e2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="966e2-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="966e2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="966e2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="966e2-126">CommonParameters</span></span>
<span data-ttu-id="966e2-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="966e2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="966e2-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="966e2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="966e2-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="966e2-129">INPUTS</span></span>

### <span data-ttu-id="966e2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="966e2-130">System.String</span></span>

### <span data-ttu-id="966e2-131">Microsoft. Azure. Commands. imfabric. Models. ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="966e2-131">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>

### <span data-ttu-id="966e2-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="966e2-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="966e2-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="966e2-133">OUTPUTS</span></span>

### <span data-ttu-id="966e2-134">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="966e2-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="966e2-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="966e2-135">NOTES</span></span>

## <span data-ttu-id="966e2-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="966e2-136">RELATED LINKS</span></span>
