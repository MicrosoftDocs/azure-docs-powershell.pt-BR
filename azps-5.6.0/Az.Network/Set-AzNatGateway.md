---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: e0c8b550b6d9571c3dd55552bab101441085f3ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892074"
---
# <span data-ttu-id="ca199-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ca199-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="ca199-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca199-102">SYNOPSIS</span></span>
<span data-ttu-id="ca199-103">Atualizar o recurso nat gateway com endereço IP público, prefixo ip público e IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="ca199-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="ca199-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ca199-104">SYNTAX</span></span>

### <span data-ttu-id="ca199-105">SetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ca199-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca199-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca199-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca199-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca199-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca199-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ca199-108">DESCRIPTION</span></span>
<span data-ttu-id="ca199-109">Atualizar o recurso nat gateway com endereço IP público, prefixo ip público e IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="ca199-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="ca199-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca199-110">EXAMPLES</span></span>

### <span data-ttu-id="ca199-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ca199-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="ca199-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ca199-112">PARAMETERS</span></span>

### <span data-ttu-id="ca199-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca199-113">-AsJob</span></span>
<span data-ttu-id="ca199-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ca199-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca199-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca199-115">-DefaultProfile</span></span>
<span data-ttu-id="ca199-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca199-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca199-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ca199-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ca199-118">O tempo de ocioso do gateway nat.</span><span class="sxs-lookup"><span data-stu-id="ca199-118">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="ca199-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca199-119">-InputObject</span></span>
<span data-ttu-id="ca199-120">Especifica o Recurso nat gateway.</span><span class="sxs-lookup"><span data-stu-id="ca199-120">Specifies Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="ca199-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ca199-121">-Name</span></span>
<span data-ttu-id="ca199-122">Nome do Recurso de Gateway Nat.</span><span class="sxs-lookup"><span data-stu-id="ca199-122">Name of the Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="ca199-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca199-123">-PublicIpAddress</span></span>
<span data-ttu-id="ca199-124">Uma matriz de endereços IP públicos associados ao recurso de gateway nat.</span><span class="sxs-lookup"><span data-stu-id="ca199-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="ca199-125">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ca199-125">-PublicIpPrefix</span></span>
<span data-ttu-id="ca199-126">Uma matriz de prefixos ip públicos associados ao recurso de gateway nat.</span><span class="sxs-lookup"><span data-stu-id="ca199-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="ca199-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca199-127">-ResourceGroupName</span></span>
<span data-ttu-id="ca199-128">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="ca199-128">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="ca199-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca199-129">-ResourceId</span></span>
<span data-ttu-id="ca199-130">Especifica a ID do recurso Nat Gateway.</span><span class="sxs-lookup"><span data-stu-id="ca199-130">Specifies the Id of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="ca199-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca199-131">-Confirm</span></span>
<span data-ttu-id="ca199-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca199-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca199-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca199-133">-WhatIf</span></span>
<span data-ttu-id="ca199-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ca199-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca199-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca199-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca199-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca199-136">CommonParameters</span></span>
<span data-ttu-id="ca199-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca199-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca199-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca199-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca199-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca199-139">INPUTS</span></span>

### <span data-ttu-id="ca199-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ca199-140">System.String</span></span>

### <span data-ttu-id="ca199-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="ca199-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="ca199-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ca199-142">OUTPUTS</span></span>

### <span data-ttu-id="ca199-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="ca199-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="ca199-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="ca199-144">NOTES</span></span>

## <span data-ttu-id="ca199-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca199-145">RELATED LINKS</span></span>
