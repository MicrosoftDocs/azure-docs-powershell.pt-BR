---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
ms.openlocfilehash: c5a5cbbbc46106fe6c388ee8f16117411f03fe0c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260409"
---
# <span data-ttu-id="3c8fe-101">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3c8fe-101">Remove-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="3c8fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3c8fe-102">SYNOPSIS</span></span>
<span data-ttu-id="3c8fe-103">Remove um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-103">Removes a network security group.</span></span>

## <span data-ttu-id="3c8fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c8fe-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c8fe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3c8fe-105">DESCRIPTION</span></span>
<span data-ttu-id="3c8fe-106">O cmdlet **Remove-AzNetworkSecurityGroup** remove um grupo de segurança de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-106">The **Remove-AzNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="3c8fe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c8fe-107">EXAMPLES</span></span>

### <span data-ttu-id="3c8fe-108">Exemplo 1: remover um grupo de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="3c8fe-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="3c8fe-109">Esse comando Remove o grupo de segurança chamado NSG-FrontEnd no grupo de recursos chamado TestRG.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="3c8fe-110">OS</span><span class="sxs-lookup"><span data-stu-id="3c8fe-110">PARAMETERS</span></span>

### <span data-ttu-id="3c8fe-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c8fe-111">-AsJob</span></span>
<span data-ttu-id="3c8fe-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3c8fe-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c8fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c8fe-113">-DefaultProfile</span></span>
<span data-ttu-id="3c8fe-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c8fe-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3c8fe-115">-Force</span></span>
<span data-ttu-id="3c8fe-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3c8fe-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c8fe-117">-Name</span></span>
<span data-ttu-id="3c8fe-118">Especifica o nome do grupo de segurança de rede que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3c8fe-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c8fe-119">-PassThru</span></span>
<span data-ttu-id="3c8fe-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3c8fe-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3c8fe-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c8fe-122">-ResourceGroupName</span></span>
<span data-ttu-id="3c8fe-123">Especifica o nome de um grupo de recursos do qual este cmdlet Remove um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="3c8fe-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3c8fe-124">-Confirm</span></span>
<span data-ttu-id="3c8fe-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c8fe-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c8fe-126">-WhatIf</span></span>
<span data-ttu-id="3c8fe-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c8fe-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c8fe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c8fe-129">CommonParameters</span></span>
<span data-ttu-id="3c8fe-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c8fe-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c8fe-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c8fe-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3c8fe-132">INPUTS</span></span>

### <span data-ttu-id="3c8fe-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3c8fe-133">System.String</span></span>

## <span data-ttu-id="3c8fe-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3c8fe-134">OUTPUTS</span></span>

### <span data-ttu-id="3c8fe-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c8fe-135">System.Boolean</span></span>

## <span data-ttu-id="3c8fe-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3c8fe-136">NOTES</span></span>

## <span data-ttu-id="3c8fe-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c8fe-137">RELATED LINKS</span></span>

[<span data-ttu-id="3c8fe-138">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3c8fe-138">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="3c8fe-139">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3c8fe-139">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="3c8fe-140">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3c8fe-140">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


