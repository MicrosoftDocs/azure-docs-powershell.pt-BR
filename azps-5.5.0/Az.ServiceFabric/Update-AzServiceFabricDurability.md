---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 1a406ad937a545c9b2599966909809c7552ad7db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113983"
---
# <span data-ttu-id="a7d94-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="a7d94-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="a7d94-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7d94-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d94-103">Atualize o nível de durabilidade ou vmSku de um tipo de nó no cluster.</span><span class="sxs-lookup"><span data-stu-id="a7d94-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="a7d94-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7d94-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7d94-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7d94-105">DESCRIPTION</span></span>
<span data-ttu-id="a7d94-106">Use **Update-AzServiceFabric Rastreaability** para atualizar a durabilidade ou a SKU do cluster.</span><span class="sxs-lookup"><span data-stu-id="a7d94-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="a7d94-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a7d94-107">EXAMPLES</span></span>

### <span data-ttu-id="a7d94-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a7d94-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="a7d94-109">Esse comando altera o nível de durabilidade do NodeType 'nt1' para prata.</span><span class="sxs-lookup"><span data-stu-id="a7d94-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="a7d94-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7d94-110">PARAMETERS</span></span>

### <span data-ttu-id="a7d94-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d94-111">-DefaultProfile</span></span>
<span data-ttu-id="a7d94-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a7d94-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7d94-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="a7d94-113">-DurabilityLevel</span></span>
<span data-ttu-id="a7d94-114">Especifique o nível de durabilidade.</span><span class="sxs-lookup"><span data-stu-id="a7d94-114">Specify durability level.</span></span>

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

### <span data-ttu-id="a7d94-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7d94-115">-Name</span></span>
<span data-ttu-id="a7d94-116">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="a7d94-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a7d94-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="a7d94-117">-NodeType</span></span>
<span data-ttu-id="a7d94-118">Especifique o nome do tipo de nó de Malha de Serviço.</span><span class="sxs-lookup"><span data-stu-id="a7d94-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="a7d94-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7d94-119">-ResourceGroupName</span></span>
<span data-ttu-id="a7d94-120">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a7d94-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a7d94-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="a7d94-121">-Sku</span></span>
<span data-ttu-id="a7d94-122">Especifique a SKU do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="a7d94-122">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="a7d94-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a7d94-123">-Confirm</span></span>
<span data-ttu-id="a7d94-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7d94-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7d94-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7d94-125">-WhatIf</span></span>
<span data-ttu-id="a7d94-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a7d94-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7d94-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a7d94-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7d94-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d94-128">CommonParameters</span></span>
<span data-ttu-id="a7d94-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7d94-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d94-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7d94-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d94-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="a7d94-131">INPUTS</span></span>

### <span data-ttu-id="a7d94-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a7d94-132">System.String</span></span>

### <span data-ttu-id="a7d94-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="a7d94-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="a7d94-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="a7d94-134">OUTPUTS</span></span>

### <span data-ttu-id="a7d94-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="a7d94-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a7d94-136">Notas</span><span class="sxs-lookup"><span data-stu-id="a7d94-136">NOTES</span></span>

## <span data-ttu-id="a7d94-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7d94-137">RELATED LINKS</span></span>
