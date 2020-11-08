---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 1a406ad937a545c9b2599966909809c7552ad7db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113300"
---
# <span data-ttu-id="0b8ef-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="0b8ef-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="0b8ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b8ef-102">SYNOPSIS</span></span>
<span data-ttu-id="0b8ef-103">Atualize a camada de durabilidade ou o VmSku de um tipo de nó no cluster.</span><span class="sxs-lookup"><span data-stu-id="0b8ef-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="0b8ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b8ef-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b8ef-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b8ef-105">DESCRIPTION</span></span>
<span data-ttu-id="0b8ef-106">Use **Update-AzServiceFabricDurability** para atualizar a durabilidade ou a SKU do cluster.</span><span class="sxs-lookup"><span data-stu-id="0b8ef-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="0b8ef-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b8ef-107">EXAMPLES</span></span>

### <span data-ttu-id="0b8ef-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0b8ef-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="0b8ef-109">Esse comando altera o nível de durabilidade do NodeType ' NT1 ' para prata.</span><span class="sxs-lookup"><span data-stu-id="0b8ef-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="0b8ef-110">OS</span><span class="sxs-lookup"><span data-stu-id="0b8ef-110">PARAMETERS</span></span>

### <span data-ttu-id="0b8ef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b8ef-111">-DefaultProfile</span></span>
<span data-ttu-id="0b8ef-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b8ef-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b8ef-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="0b8ef-113">-DurabilityLevel</span></span>
<span data-ttu-id="0b8ef-114">Especifique o nível de durabilidade.</span><span class="sxs-lookup"><span data-stu-id="0b8ef-114">Specify durability level.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: Bronze, Silver, Gold

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b8ef-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b8ef-115">-Name</span></span>
<span data-ttu-id="0b8ef-116">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="0b8ef-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="0b8ef-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="0b8ef-117">-NodeType</span></span>
<span data-ttu-id="0b8ef-118">Especifique o nome do tipo de nó do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="0b8ef-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="0b8ef-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b8ef-119">-ResourceGroupName</span></span>
<span data-ttu-id="0b8ef-120">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b8ef-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0b8ef-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="0b8ef-121">-Sku</span></span>
<span data-ttu-id="0b8ef-122">Especifique a SKU do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="0b8ef-122">Specify the SKU of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b8ef-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0b8ef-123">-Confirm</span></span>
<span data-ttu-id="0b8ef-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b8ef-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b8ef-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b8ef-125">-WhatIf</span></span>
<span data-ttu-id="0b8ef-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0b8ef-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b8ef-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0b8ef-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b8ef-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b8ef-128">CommonParameters</span></span>
<span data-ttu-id="0b8ef-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b8ef-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b8ef-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b8ef-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b8ef-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b8ef-131">INPUTS</span></span>

### <span data-ttu-id="0b8ef-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0b8ef-132">System.String</span></span>

### <span data-ttu-id="0b8ef-133">Microsoft. Azure. Commands. imfabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="0b8ef-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="0b8ef-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b8ef-134">OUTPUTS</span></span>

### <span data-ttu-id="0b8ef-135">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="0b8ef-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="0b8ef-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b8ef-136">NOTES</span></span>

## <span data-ttu-id="0b8ef-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b8ef-137">RELATED LINKS</span></span>
