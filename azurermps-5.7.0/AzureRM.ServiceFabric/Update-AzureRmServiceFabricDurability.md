---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: 9c82f0aab38fb5479f5344166a409b9b32f7447c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432395"
---
# <span data-ttu-id="59e54-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="59e54-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="59e54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59e54-102">SYNOPSIS</span></span>
<span data-ttu-id="59e54-103">Atualize a camada de durabilidade ou o VmSku de um tipo de nó no cluster.</span><span class="sxs-lookup"><span data-stu-id="59e54-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59e54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59e54-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59e54-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59e54-105">DESCRIPTION</span></span>
<span data-ttu-id="59e54-106">Use **Update-AzureRmServiceFabricDurability** para atualizar a durabilidade ou a SKU do cluster.</span><span class="sxs-lookup"><span data-stu-id="59e54-106">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="59e54-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59e54-107">EXAMPLES</span></span>

### <span data-ttu-id="59e54-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="59e54-108">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="59e54-109">Esse comando altera o nível de durabilidade do NodeType ' NT1 ' para prata.</span><span class="sxs-lookup"><span data-stu-id="59e54-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="59e54-110">OS</span><span class="sxs-lookup"><span data-stu-id="59e54-110">PARAMETERS</span></span>

### <span data-ttu-id="59e54-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59e54-111">-DefaultProfile</span></span>
<span data-ttu-id="59e54-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="59e54-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59e54-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="59e54-113">-DurabilityLevel</span></span>
<span data-ttu-id="59e54-114">Especifique o nível de durabilidade.</span><span class="sxs-lookup"><span data-stu-id="59e54-114">Specify durability level.</span></span>

```yaml
Type: DurabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: Bronze, Silver, Gold

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59e54-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="59e54-115">-Name</span></span>
<span data-ttu-id="59e54-116">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="59e54-116">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59e54-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="59e54-117">-NodeType</span></span>
<span data-ttu-id="59e54-118">Especifique o nome do tipo de nó do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="59e54-118">Specify Service Fabric node type name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59e54-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59e54-119">-ResourceGroupName</span></span>
<span data-ttu-id="59e54-120">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="59e54-120">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59e54-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="59e54-121">-Sku</span></span>
<span data-ttu-id="59e54-122">Especifique a SKU do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="59e54-122">Specify the SKU of the node type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59e54-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="59e54-123">-Confirm</span></span>
<span data-ttu-id="59e54-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59e54-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59e54-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59e54-125">-WhatIf</span></span>
<span data-ttu-id="59e54-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="59e54-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59e54-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="59e54-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59e54-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59e54-128">CommonParameters</span></span>
<span data-ttu-id="59e54-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59e54-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59e54-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59e54-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59e54-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59e54-131">INPUTS</span></span>

### <span data-ttu-id="59e54-132">Microsoft. Azure. Commands. imfabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="59e54-132">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="59e54-133">System. String</span><span class="sxs-lookup"><span data-stu-id="59e54-133">System.String</span></span>

## <span data-ttu-id="59e54-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59e54-134">OUTPUTS</span></span>

### <span data-ttu-id="59e54-135">Microsoft. Azure. Commands. imfabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="59e54-135">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="59e54-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59e54-136">NOTES</span></span>

## <span data-ttu-id="59e54-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59e54-137">RELATED LINKS</span></span>

