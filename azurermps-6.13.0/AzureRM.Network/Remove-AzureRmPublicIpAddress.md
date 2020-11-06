---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
ms.openlocfilehash: 6d294bd4b6f016ed1731a71528b39adc3bbe8e70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440341"
---
# <span data-ttu-id="db3de-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="db3de-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="db3de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db3de-102">SYNOPSIS</span></span>
<span data-ttu-id="db3de-103">Remove um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="db3de-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db3de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db3de-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db3de-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db3de-105">DESCRIPTION</span></span>
<span data-ttu-id="db3de-106">O cmdlet **Remove-AzureRmPublicIpAddress** remove um endereço IP público do Azure.</span><span class="sxs-lookup"><span data-stu-id="db3de-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="db3de-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db3de-107">EXAMPLES</span></span>

### <span data-ttu-id="db3de-108">1: remover um recurso de endereço IP público</span><span class="sxs-lookup"><span data-stu-id="db3de-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="db3de-109">Este comando Remove o recurso de endereço IP público chamado $publicIpName no $rgName do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="db3de-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="db3de-110">OS</span><span class="sxs-lookup"><span data-stu-id="db3de-110">PARAMETERS</span></span>

### <span data-ttu-id="db3de-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db3de-111">-AsJob</span></span>
<span data-ttu-id="db3de-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="db3de-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db3de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db3de-113">-DefaultProfile</span></span>
<span data-ttu-id="db3de-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db3de-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db3de-115">-Force</span><span class="sxs-lookup"><span data-stu-id="db3de-115">-Force</span></span>
<span data-ttu-id="db3de-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="db3de-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="db3de-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="db3de-117">-Name</span></span>
<span data-ttu-id="db3de-118">Especifica o nome do endereço IP público que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="db3de-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="db3de-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db3de-119">-PassThru</span></span>
<span data-ttu-id="db3de-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="db3de-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="db3de-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="db3de-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="db3de-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db3de-122">-ResourceGroupName</span></span>
<span data-ttu-id="db3de-123">Especifica o nome do grupo de recursos que contém o endereço IP público que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="db3de-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="db3de-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="db3de-124">-Confirm</span></span>
<span data-ttu-id="db3de-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db3de-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db3de-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db3de-126">-WhatIf</span></span>
<span data-ttu-id="db3de-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="db3de-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db3de-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db3de-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db3de-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db3de-129">CommonParameters</span></span>
<span data-ttu-id="db3de-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db3de-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db3de-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db3de-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db3de-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db3de-132">INPUTS</span></span>

### <span data-ttu-id="db3de-133">System. String</span><span class="sxs-lookup"><span data-stu-id="db3de-133">System.String</span></span>

## <span data-ttu-id="db3de-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db3de-134">OUTPUTS</span></span>

### <span data-ttu-id="db3de-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="db3de-135">System.Boolean</span></span>

## <span data-ttu-id="db3de-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db3de-136">NOTES</span></span>

## <span data-ttu-id="db3de-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db3de-137">RELATED LINKS</span></span>

[<span data-ttu-id="db3de-138">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="db3de-138">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="db3de-139">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="db3de-139">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="db3de-140">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="db3de-140">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


