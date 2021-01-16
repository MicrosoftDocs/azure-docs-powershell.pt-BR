---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: 8d3c71d1cf4df9483f379d8a689597a1a10c7ce7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261439"
---
# <span data-ttu-id="c7142-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c7142-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="c7142-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7142-102">SYNOPSIS</span></span>
<span data-ttu-id="c7142-103">Remove um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="c7142-103">Removes a public IP address.</span></span>

## <span data-ttu-id="c7142-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7142-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7142-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7142-105">DESCRIPTION</span></span>
<span data-ttu-id="c7142-106">O cmdlet **Remove-AzPublicIpAddress** remove um endereço IP público do Azure.</span><span class="sxs-lookup"><span data-stu-id="c7142-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="c7142-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7142-107">EXAMPLES</span></span>

### <span data-ttu-id="c7142-108">1: remover um recurso de endereço IP público</span><span class="sxs-lookup"><span data-stu-id="c7142-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="c7142-109">Este comando Remove o recurso de endereço IP público chamado $publicIpName no $rgName do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c7142-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="c7142-110">OS</span><span class="sxs-lookup"><span data-stu-id="c7142-110">PARAMETERS</span></span>

### <span data-ttu-id="c7142-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7142-111">-AsJob</span></span>
<span data-ttu-id="c7142-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c7142-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7142-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7142-113">-DefaultProfile</span></span>
<span data-ttu-id="c7142-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c7142-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7142-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c7142-115">-Force</span></span>
<span data-ttu-id="c7142-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c7142-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c7142-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7142-117">-Name</span></span>
<span data-ttu-id="c7142-118">Especifica o nome do endereço IP público que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="c7142-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c7142-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7142-119">-PassThru</span></span>
<span data-ttu-id="c7142-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="c7142-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c7142-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="c7142-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c7142-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7142-122">-ResourceGroupName</span></span>
<span data-ttu-id="c7142-123">Especifica o nome do grupo de recursos que contém o endereço IP público que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="c7142-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c7142-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c7142-124">-Confirm</span></span>
<span data-ttu-id="c7142-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7142-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7142-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7142-126">-WhatIf</span></span>
<span data-ttu-id="c7142-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c7142-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7142-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c7142-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7142-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7142-129">CommonParameters</span></span>
<span data-ttu-id="c7142-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7142-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7142-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7142-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7142-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7142-132">INPUTS</span></span>

### <span data-ttu-id="c7142-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c7142-133">System.String</span></span>

## <span data-ttu-id="c7142-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7142-134">OUTPUTS</span></span>

### <span data-ttu-id="c7142-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c7142-135">System.Boolean</span></span>

## <span data-ttu-id="c7142-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7142-136">NOTES</span></span>

## <span data-ttu-id="c7142-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7142-137">RELATED LINKS</span></span>

[<span data-ttu-id="c7142-138">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c7142-138">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="c7142-139">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c7142-139">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="c7142-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c7142-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


