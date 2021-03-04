---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: f8a509fc73387361de5bd191ee9eefc61c33a5f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891112"
---
# <span data-ttu-id="18ee9-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="18ee9-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="18ee9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18ee9-102">SYNOPSIS</span></span>
<span data-ttu-id="18ee9-103">Remove um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="18ee9-103">Removes a public IP address.</span></span>

## <span data-ttu-id="18ee9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="18ee9-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18ee9-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="18ee9-105">DESCRIPTION</span></span>
<span data-ttu-id="18ee9-106">O cmdlet **Remove-AzPublicIpAddress** remove um endereço IP público do Azure.</span><span class="sxs-lookup"><span data-stu-id="18ee9-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="18ee9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18ee9-107">EXAMPLES</span></span>

### <span data-ttu-id="18ee9-108">1: Remover um recurso de endereço IP público</span><span class="sxs-lookup"><span data-stu-id="18ee9-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="18ee9-109">Este comando remove o recurso de endereço IP público chamado $publicIpName no grupo de recursos $rgName.</span><span class="sxs-lookup"><span data-stu-id="18ee9-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="18ee9-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="18ee9-110">PARAMETERS</span></span>

### <span data-ttu-id="18ee9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18ee9-111">-AsJob</span></span>
<span data-ttu-id="18ee9-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="18ee9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18ee9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18ee9-113">-DefaultProfile</span></span>
<span data-ttu-id="18ee9-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="18ee9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18ee9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="18ee9-115">-Force</span></span>
<span data-ttu-id="18ee9-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="18ee9-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="18ee9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="18ee9-117">-Name</span></span>
<span data-ttu-id="18ee9-118">Especifica o nome do endereço IP público que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="18ee9-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="18ee9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18ee9-119">-PassThru</span></span>
<span data-ttu-id="18ee9-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="18ee9-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="18ee9-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="18ee9-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="18ee9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18ee9-122">-ResourceGroupName</span></span>
<span data-ttu-id="18ee9-123">Especifica o nome do grupo de recursos que contém o endereço IP público que esse cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="18ee9-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="18ee9-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18ee9-124">-Confirm</span></span>
<span data-ttu-id="18ee9-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18ee9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18ee9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18ee9-126">-WhatIf</span></span>
<span data-ttu-id="18ee9-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="18ee9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18ee9-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18ee9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18ee9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18ee9-129">CommonParameters</span></span>
<span data-ttu-id="18ee9-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18ee9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18ee9-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18ee9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18ee9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18ee9-132">INPUTS</span></span>

### <span data-ttu-id="18ee9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="18ee9-133">System.String</span></span>

## <span data-ttu-id="18ee9-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="18ee9-134">OUTPUTS</span></span>

### <span data-ttu-id="18ee9-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="18ee9-135">System.Boolean</span></span>

## <span data-ttu-id="18ee9-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="18ee9-136">NOTES</span></span>

## <span data-ttu-id="18ee9-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18ee9-137">RELATED LINKS</span></span>

[<span data-ttu-id="18ee9-138">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="18ee9-138">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="18ee9-139">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="18ee9-139">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="18ee9-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="18ee9-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


