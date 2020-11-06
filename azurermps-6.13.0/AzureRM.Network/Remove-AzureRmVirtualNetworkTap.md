---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: 59e3b7f233077c8ed7064bcb1757634fe08c262b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429427"
---
# <span data-ttu-id="48247-101">Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="48247-101">Remove-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="48247-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48247-102">SYNOPSIS</span></span>
<span data-ttu-id="48247-103">Remove um toque de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="48247-103">Removes a virtual network tap.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48247-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48247-104">SYNTAX</span></span>

### <span data-ttu-id="48247-105">RemoveByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="48247-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzureRmVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48247-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48247-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzureRmVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48247-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48247-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzureRmVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48247-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48247-108">DESCRIPTION</span></span>
<span data-ttu-id="48247-109">O cmdlet **Remove-AzureRmVirtualNetworkTap** remove um toque de rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="48247-109">The **Remove-AzureRmVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="48247-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48247-110">EXAMPLES</span></span>

### <span data-ttu-id="48247-111">Exemplo 1: remover um toque de rede virtuak</span><span class="sxs-lookup"><span data-stu-id="48247-111">Example 1: Remove a virtuak network tap</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="48247-112">Esse comando Remove a VirtualNetworkTap1 na ResourceGroup1 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="48247-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="48247-113">Como o parâmetro *Force* não é usado, o usuário será solicitado a confirmar essa ação.</span><span class="sxs-lookup"><span data-stu-id="48247-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="48247-114">OS</span><span class="sxs-lookup"><span data-stu-id="48247-114">PARAMETERS</span></span>

### <span data-ttu-id="48247-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48247-115">-AsJob</span></span>
<span data-ttu-id="48247-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="48247-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48247-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48247-117">-DefaultProfile</span></span>
<span data-ttu-id="48247-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48247-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48247-119">-Force</span><span class="sxs-lookup"><span data-stu-id="48247-119">-Force</span></span>
<span data-ttu-id="48247-120">Não pedir confirmação se quiser excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="48247-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="48247-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48247-121">-InputObject</span></span>
<span data-ttu-id="48247-122">Referência ao recurso VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="48247-122">Reference to VirtualNetworkTap resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48247-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="48247-123">-Name</span></span>
<span data-ttu-id="48247-124">O nome do toque.</span><span class="sxs-lookup"><span data-stu-id="48247-124">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48247-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48247-125">-PassThru</span></span>
<span data-ttu-id="48247-126">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="48247-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="48247-127">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="48247-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="48247-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48247-128">-ResourceGroupName</span></span>
<span data-ttu-id="48247-129">O nome do grupo de recursos da rede virtual toque.</span><span class="sxs-lookup"><span data-stu-id="48247-129">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48247-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48247-130">-ResourceId</span></span>
<span data-ttu-id="48247-131">ResourceId VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="48247-131">VirtualNetworkTap resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48247-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="48247-132">-Confirm</span></span>
<span data-ttu-id="48247-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48247-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48247-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48247-134">-WhatIf</span></span>
<span data-ttu-id="48247-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="48247-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48247-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="48247-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48247-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48247-137">CommonParameters</span></span>
<span data-ttu-id="48247-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48247-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48247-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48247-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48247-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48247-140">INPUTS</span></span>

### <span data-ttu-id="48247-141">System. String</span><span class="sxs-lookup"><span data-stu-id="48247-141">System.String</span></span>

## <span data-ttu-id="48247-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48247-142">OUTPUTS</span></span>

### <span data-ttu-id="48247-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="48247-143">System.Boolean</span></span>

## <span data-ttu-id="48247-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48247-144">NOTES</span></span>

## <span data-ttu-id="48247-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48247-145">RELATED LINKS</span></span>
