---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 36cad62f67be4273d363277e52f4dc8d2c91373c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440030"
---
# <span data-ttu-id="1c608-101">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="1c608-101">Remove-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="1c608-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c608-102">SYNOPSIS</span></span>
<span data-ttu-id="1c608-103">Remover um tipo de nó completo de um cluster.</span><span class="sxs-lookup"><span data-stu-id="1c608-103">Remove a complete node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c608-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c608-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c608-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c608-105">DESCRIPTION</span></span>
<span data-ttu-id="1c608-106">Use **Remove-AzureRmServiceFabricNodeType** para remover todos os nós de um tipo de nó específico e o tipo de nó de um cluster.</span><span class="sxs-lookup"><span data-stu-id="1c608-106">Use the **Remove-AzureRmServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="1c608-107">Este comando não pode ser usado para excluir o tipo de nó primário.</span><span class="sxs-lookup"><span data-stu-id="1c608-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="1c608-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c608-108">EXAMPLES</span></span>

### <span data-ttu-id="1c608-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1c608-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="1c608-110">Esse comando removerá o NodeType ' NT1 ' do cluster.</span><span class="sxs-lookup"><span data-stu-id="1c608-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="1c608-111">OS</span><span class="sxs-lookup"><span data-stu-id="1c608-111">PARAMETERS</span></span>

### <span data-ttu-id="1c608-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c608-112">-DefaultProfile</span></span>
<span data-ttu-id="1c608-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c608-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c608-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c608-114">-Name</span></span>
<span data-ttu-id="1c608-115">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="1c608-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="1c608-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="1c608-116">-NodeType</span></span>
<span data-ttu-id="1c608-117">O nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="1c608-117">The node type name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c608-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c608-118">-ResourceGroupName</span></span>
<span data-ttu-id="1c608-119">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1c608-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1c608-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1c608-120">-Confirm</span></span>
<span data-ttu-id="1c608-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c608-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c608-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c608-122">-WhatIf</span></span>
<span data-ttu-id="1c608-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1c608-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c608-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1c608-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c608-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c608-125">CommonParameters</span></span>
<span data-ttu-id="1c608-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c608-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c608-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c608-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c608-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c608-128">INPUTS</span></span>

### <span data-ttu-id="1c608-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1c608-129">System.String</span></span>
<span data-ttu-id="1c608-130">Parâmetros: NodeType (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1c608-130">Parameters: NodeType (ByValue)</span></span>

## <span data-ttu-id="1c608-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c608-131">OUTPUTS</span></span>

### <span data-ttu-id="1c608-132">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="1c608-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="1c608-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c608-133">NOTES</span></span>

## <span data-ttu-id="1c608-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c608-134">RELATED LINKS</span></span>
