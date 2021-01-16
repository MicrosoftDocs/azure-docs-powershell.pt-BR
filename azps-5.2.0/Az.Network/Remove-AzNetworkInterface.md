---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: f4de49bb2e35bf3d392fba06d663800a5bdc44a6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258291"
---
# <span data-ttu-id="cd1c8-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cd1c8-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="cd1c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd1c8-102">SYNOPSIS</span></span>
<span data-ttu-id="cd1c8-103">Remove uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="cd1c8-103">Removes a network interface.</span></span>

## <span data-ttu-id="cd1c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd1c8-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd1c8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd1c8-105">DESCRIPTION</span></span>
<span data-ttu-id="cd1c8-106">O cmdlet **Remove-AzNetworkInterface** remove uma interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="cd1c8-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="cd1c8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd1c8-107">EXAMPLES</span></span>

### <span data-ttu-id="cd1c8-108">Exemplo 1: remover uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="cd1c8-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="cd1c8-109">Esse comando Remove a interface de NetworkInterface1 na ResourceGroup1 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cd1c8-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="cd1c8-110">Como o parâmetro *Force* não é usado, o usuário será solicitado a confirmar essa ação.</span><span class="sxs-lookup"><span data-stu-id="cd1c8-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="cd1c8-111">Exemplo 2: remover uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="cd1c8-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="cd1c8-112">Esse comando Remove todas as interfaces de rede na ResourceGroup1 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cd1c8-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="cd1c8-113">Como o parâmetro *Force* é usado, o usuário não será solicitado a confirmar a confirmação.</span><span class="sxs-lookup"><span data-stu-id="cd1c8-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="cd1c8-114">OS</span><span class="sxs-lookup"><span data-stu-id="cd1c8-114">PARAMETERS</span></span>

### <span data-ttu-id="cd1c8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd1c8-115">-AsJob</span></span>
<span data-ttu-id="cd1c8-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cd1c8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd1c8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd1c8-117">-DefaultProfile</span></span>
<span data-ttu-id="cd1c8-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd1c8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd1c8-119">-Force</span><span class="sxs-lookup"><span data-stu-id="cd1c8-119">-Force</span></span>
<span data-ttu-id="cd1c8-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="cd1c8-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cd1c8-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd1c8-121">-Name</span></span>
<span data-ttu-id="cd1c8-122">Especifica o nome da interface de rede que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="cd1c8-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cd1c8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd1c8-123">-PassThru</span></span>
<span data-ttu-id="cd1c8-124">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="cd1c8-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cd1c8-125">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="cd1c8-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cd1c8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd1c8-126">-ResourceGroupName</span></span>
<span data-ttu-id="cd1c8-127">Especifica o nome de um grupo de recursos que contém a interface de rede que esse cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="cd1c8-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cd1c8-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cd1c8-128">-Confirm</span></span>
<span data-ttu-id="cd1c8-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd1c8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd1c8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd1c8-130">-WhatIf</span></span>
<span data-ttu-id="cd1c8-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cd1c8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd1c8-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cd1c8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd1c8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd1c8-133">CommonParameters</span></span>
<span data-ttu-id="cd1c8-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd1c8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd1c8-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd1c8-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd1c8-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd1c8-136">INPUTS</span></span>

### <span data-ttu-id="cd1c8-137">System. String</span><span class="sxs-lookup"><span data-stu-id="cd1c8-137">System.String</span></span>

## <span data-ttu-id="cd1c8-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd1c8-138">OUTPUTS</span></span>

### <span data-ttu-id="cd1c8-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd1c8-139">System.Boolean</span></span>

## <span data-ttu-id="cd1c8-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd1c8-140">NOTES</span></span>

## <span data-ttu-id="cd1c8-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd1c8-141">RELATED LINKS</span></span>

[<span data-ttu-id="cd1c8-142">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cd1c8-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="cd1c8-143">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cd1c8-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="cd1c8-144">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cd1c8-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


