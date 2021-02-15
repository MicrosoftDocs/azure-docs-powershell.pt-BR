---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: 8d3c71d1cf4df9483f379d8a689597a1a10c7ce7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115084"
---
# <span data-ttu-id="bbf0a-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bbf0a-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="bbf0a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bbf0a-102">SYNOPSIS</span></span>
<span data-ttu-id="bbf0a-103">Remove um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="bbf0a-103">Removes a public IP address.</span></span>

## <span data-ttu-id="bbf0a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbf0a-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbf0a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="bbf0a-105">DESCRIPTION</span></span>
<span data-ttu-id="bbf0a-106">O cmdlet **Remove-AzPublicIpAddress** remove um endereço IP público do Azure.</span><span class="sxs-lookup"><span data-stu-id="bbf0a-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="bbf0a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bbf0a-107">EXAMPLES</span></span>

### <span data-ttu-id="bbf0a-108">1: Remover um recurso de endereço IP público</span><span class="sxs-lookup"><span data-stu-id="bbf0a-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="bbf0a-109">Esse comando remove o recurso de endereço IP público chamado $publicIpName no grupo de recursos $rgName.</span><span class="sxs-lookup"><span data-stu-id="bbf0a-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="bbf0a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbf0a-110">PARAMETERS</span></span>

### <span data-ttu-id="bbf0a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bbf0a-111">-AsJob</span></span>
<span data-ttu-id="bbf0a-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bbf0a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bbf0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbf0a-113">-DefaultProfile</span></span>
<span data-ttu-id="bbf0a-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="bbf0a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbf0a-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="bbf0a-115">-Force</span></span>
<span data-ttu-id="bbf0a-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="bbf0a-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bbf0a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="bbf0a-117">-Name</span></span>
<span data-ttu-id="bbf0a-118">Especifica o nome do endereço IP público que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="bbf0a-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bbf0a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbf0a-119">-PassThru</span></span>
<span data-ttu-id="bbf0a-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="bbf0a-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bbf0a-121">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="bbf0a-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bbf0a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbf0a-122">-ResourceGroupName</span></span>
<span data-ttu-id="bbf0a-123">Especifica o nome do grupo de recursos que contém o endereço IP público que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="bbf0a-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bbf0a-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bbf0a-124">-Confirm</span></span>
<span data-ttu-id="bbf0a-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbf0a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbf0a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbf0a-126">-WhatIf</span></span>
<span data-ttu-id="bbf0a-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bbf0a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbf0a-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bbf0a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbf0a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbf0a-129">CommonParameters</span></span>
<span data-ttu-id="bbf0a-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbf0a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbf0a-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbf0a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbf0a-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="bbf0a-132">INPUTS</span></span>

### <span data-ttu-id="bbf0a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="bbf0a-133">System.String</span></span>

## <span data-ttu-id="bbf0a-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="bbf0a-134">OUTPUTS</span></span>

### <span data-ttu-id="bbf0a-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bbf0a-135">System.Boolean</span></span>

## <span data-ttu-id="bbf0a-136">Notas</span><span class="sxs-lookup"><span data-stu-id="bbf0a-136">NOTES</span></span>

## <span data-ttu-id="bbf0a-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bbf0a-137">RELATED LINKS</span></span>

[<span data-ttu-id="bbf0a-138">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bbf0a-138">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="bbf0a-139">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bbf0a-139">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="bbf0a-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bbf0a-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


