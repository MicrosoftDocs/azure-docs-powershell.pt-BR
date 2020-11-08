---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: fe19aba38402519a77185062ac6192d6ff9915eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117237"
---
# <span data-ttu-id="602f4-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="602f4-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="602f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="602f4-102">SYNOPSIS</span></span>
<span data-ttu-id="602f4-103">Atualize o recurso de gateway NAT com endereço IP público, prefixo de IP público e IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="602f4-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="602f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="602f4-104">SYNTAX</span></span>

### <span data-ttu-id="602f4-105">SetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="602f4-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="602f4-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="602f4-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="602f4-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="602f4-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="602f4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="602f4-108">DESCRIPTION</span></span>
<span data-ttu-id="602f4-109">Atualize o recurso de gateway NAT com endereço IP público, prefixo de IP público e IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="602f4-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="602f4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="602f4-110">EXAMPLES</span></span>

### <span data-ttu-id="602f4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="602f4-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="602f4-112">OS</span><span class="sxs-lookup"><span data-stu-id="602f4-112">PARAMETERS</span></span>

### <span data-ttu-id="602f4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="602f4-113">-AsJob</span></span>
<span data-ttu-id="602f4-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="602f4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="602f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="602f4-115">-DefaultProfile</span></span>
<span data-ttu-id="602f4-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="602f4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="602f4-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="602f4-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="602f4-118">O tempo limite ocioso do gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="602f4-118">The idle timeout of the nat gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="602f4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="602f4-119">-InputObject</span></span>
<span data-ttu-id="602f4-120">Especifica o recurso de gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="602f4-120">Specifies Nat Gateway Resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="602f4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="602f4-121">-Name</span></span>
<span data-ttu-id="602f4-122">Nome do recurso de gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="602f4-122">Name of the Nat Gateway Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="602f4-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="602f4-123">-PublicIpAddress</span></span>
<span data-ttu-id="602f4-124">Uma matriz de endereços IP públicos associados ao recurso de gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="602f4-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="602f4-125">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="602f4-125">-PublicIpPrefix</span></span>
<span data-ttu-id="602f4-126">Uma matriz de prefixos IP públicos associados ao recurso de gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="602f4-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="602f4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="602f4-127">-ResourceGroupName</span></span>
<span data-ttu-id="602f4-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="602f4-128">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="602f4-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="602f4-129">-ResourceId</span></span>
<span data-ttu-id="602f4-130">Especifica a ID do recurso de gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="602f4-130">Specifies the Id of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="602f4-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="602f4-131">-Confirm</span></span>
<span data-ttu-id="602f4-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="602f4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="602f4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="602f4-133">-WhatIf</span></span>
<span data-ttu-id="602f4-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="602f4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="602f4-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="602f4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="602f4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="602f4-136">CommonParameters</span></span>
<span data-ttu-id="602f4-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="602f4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="602f4-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="602f4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="602f4-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="602f4-139">INPUTS</span></span>

### <span data-ttu-id="602f4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="602f4-140">System.String</span></span>

### <span data-ttu-id="602f4-141">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="602f4-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="602f4-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="602f4-142">OUTPUTS</span></span>

### <span data-ttu-id="602f4-143">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="602f4-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="602f4-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="602f4-144">NOTES</span></span>

## <span data-ttu-id="602f4-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="602f4-145">RELATED LINKS</span></span>
