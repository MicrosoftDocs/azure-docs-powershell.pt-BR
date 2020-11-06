---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 401fcbd5fca9fc0251e4de0fb7843fb95c1c122d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439905"
---
# <span data-ttu-id="46315-101">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="46315-101">Remove-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="46315-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46315-102">SYNOPSIS</span></span>
<span data-ttu-id="46315-103">Exclui um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="46315-103">Deletes a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46315-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46315-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46315-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="46315-105">DESCRIPTION</span></span>
<span data-ttu-id="46315-106">O gateway de rede virtual é o objeto que representa o gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="46315-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="46315-107">O cmdlet **Get-AzureRmVirtualNetworkGateway** retorna o objeto do seu gateway no Azure com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="46315-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="46315-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46315-108">EXAMPLES</span></span>

### <span data-ttu-id="46315-109">1: excluir um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="46315-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="46315-110">Exclui o objeto do gateway de rede virtual com o nome "mygateway" no grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="46315-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

<span data-ttu-id="46315-111">Observação: você deve primeiro excluir todas as conexões com o gateway de rede virtual usando o cmdlet **Remove-AzureRmVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="46315-111">Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="46315-112">OS</span><span class="sxs-lookup"><span data-stu-id="46315-112">PARAMETERS</span></span>

### <span data-ttu-id="46315-113">-Force</span><span class="sxs-lookup"><span data-stu-id="46315-113">-Force</span></span>
<span data-ttu-id="46315-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="46315-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="46315-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="46315-115">-Name</span></span>
<span data-ttu-id="46315-116">Especifica o nome do gateway de rede virtual que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="46315-116">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="46315-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46315-117">-PassThru</span></span>
<span data-ttu-id="46315-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="46315-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="46315-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="46315-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="46315-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46315-120">-ResourceGroupName</span></span>
<span data-ttu-id="46315-121">Especifica o nome do grupo de recursos que contém o gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="46315-121">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="46315-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="46315-122">-Confirm</span></span>
<span data-ttu-id="46315-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46315-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46315-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46315-124">-WhatIf</span></span>
<span data-ttu-id="46315-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="46315-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46315-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="46315-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46315-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46315-127">-DefaultProfile</span></span>
<span data-ttu-id="46315-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46315-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46315-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46315-129">CommonParameters</span></span>
<span data-ttu-id="46315-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46315-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46315-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46315-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46315-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="46315-132">INPUTS</span></span>

## <span data-ttu-id="46315-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="46315-133">OUTPUTS</span></span>

## <span data-ttu-id="46315-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="46315-134">NOTES</span></span>

## <span data-ttu-id="46315-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46315-135">RELATED LINKS</span></span>

