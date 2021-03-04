---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: 54bc4a3b9875f68df8a7c824c7e4f754e6f35a4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890758"
---
# <span data-ttu-id="f84b3-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f84b3-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="f84b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f84b3-102">SYNOPSIS</span></span>
<span data-ttu-id="f84b3-103">Remove uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="f84b3-103">Removes a network interface.</span></span>

## <span data-ttu-id="f84b3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f84b3-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f84b3-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f84b3-105">DESCRIPTION</span></span>
<span data-ttu-id="f84b3-106">O cmdlet **Remove-AzNetworkInterface** remove uma interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="f84b3-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="f84b3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f84b3-107">EXAMPLES</span></span>

### <span data-ttu-id="f84b3-108">Exemplo 1: Remover uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="f84b3-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="f84b3-109">Este comando remove a interface de rede NetworkInterface1 no grupo de recursos ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="f84b3-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="f84b3-110">Como o *parâmetro Force* não é usado, o usuário será solicitado a confirmar essa ação.</span><span class="sxs-lookup"><span data-stu-id="f84b3-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="f84b3-111">Exemplo 2: Remover uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="f84b3-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="f84b3-112">Este comando remove todas as interfaces de rede no grupo de recursos ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="f84b3-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="f84b3-113">Como o *parâmetro Force* é usado, o usuário não é solicitado a confirmar.</span><span class="sxs-lookup"><span data-stu-id="f84b3-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="f84b3-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f84b3-114">PARAMETERS</span></span>

### <span data-ttu-id="f84b3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f84b3-115">-AsJob</span></span>
<span data-ttu-id="f84b3-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f84b3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f84b3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f84b3-117">-DefaultProfile</span></span>
<span data-ttu-id="f84b3-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f84b3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f84b3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f84b3-119">-Force</span></span>
<span data-ttu-id="f84b3-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f84b3-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f84b3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f84b3-121">-Name</span></span>
<span data-ttu-id="f84b3-122">Especifica o nome da interface de rede que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="f84b3-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f84b3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f84b3-123">-PassThru</span></span>
<span data-ttu-id="f84b3-124">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="f84b3-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f84b3-125">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f84b3-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f84b3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f84b3-126">-ResourceGroupName</span></span>
<span data-ttu-id="f84b3-127">Especifica o nome de um grupo de recursos que contém a interface de rede que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="f84b3-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f84b3-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f84b3-128">-Confirm</span></span>
<span data-ttu-id="f84b3-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f84b3-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f84b3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f84b3-130">-WhatIf</span></span>
<span data-ttu-id="f84b3-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f84b3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f84b3-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f84b3-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f84b3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f84b3-133">CommonParameters</span></span>
<span data-ttu-id="f84b3-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f84b3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f84b3-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f84b3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f84b3-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f84b3-136">INPUTS</span></span>

### <span data-ttu-id="f84b3-137">System.String</span><span class="sxs-lookup"><span data-stu-id="f84b3-137">System.String</span></span>

## <span data-ttu-id="f84b3-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f84b3-138">OUTPUTS</span></span>

### <span data-ttu-id="f84b3-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f84b3-139">System.Boolean</span></span>

## <span data-ttu-id="f84b3-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="f84b3-140">NOTES</span></span>

## <span data-ttu-id="f84b3-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f84b3-141">RELATED LINKS</span></span>

[<span data-ttu-id="f84b3-142">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f84b3-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="f84b3-143">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f84b3-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="f84b3-144">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f84b3-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


