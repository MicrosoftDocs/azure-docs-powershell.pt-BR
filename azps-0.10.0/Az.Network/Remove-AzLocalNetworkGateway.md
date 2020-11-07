---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: 0589fa3f5dd806149c243557b547455af35178b2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775286"
---
# <span data-ttu-id="f3854-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f3854-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="f3854-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f3854-102">SYNOPSIS</span></span>
<span data-ttu-id="f3854-103">Exclui um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="f3854-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="f3854-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3854-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3854-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f3854-105">DESCRIPTION</span></span>
<span data-ttu-id="f3854-106">O gateway de rede local é o objeto que representa o seu dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="f3854-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="f3854-107">O cmdlet **Remove-AzLocalNetworkGateway** exclui o objeto que representa o gateway local com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f3854-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="f3854-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f3854-108">EXAMPLES</span></span>

### <span data-ttu-id="f3854-109">1: excluir um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="f3854-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="f3854-110">Exclui o objeto do gateway de rede local com o nome "myLocalGW" no grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="f3854-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

<span data-ttu-id="f3854-111">Observação: você deve primeiro excluir todas as conexões com o gateway de rede local usando o cmdlet **Remove-AzVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="f3854-111">Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="f3854-112">OS</span><span class="sxs-lookup"><span data-stu-id="f3854-112">PARAMETERS</span></span>

### <span data-ttu-id="f3854-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3854-113">-AsJob</span></span>
<span data-ttu-id="f3854-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f3854-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3854-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3854-115">-DefaultProfile</span></span>
<span data-ttu-id="f3854-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f3854-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3854-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f3854-117">-Force</span></span>
<span data-ttu-id="f3854-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f3854-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3854-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3854-119">-Name</span></span>
<span data-ttu-id="f3854-120">Especifica o nome do gateway de rede local que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="f3854-120">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3854-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3854-121">-PassThru</span></span>
<span data-ttu-id="f3854-122">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="f3854-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f3854-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f3854-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3854-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3854-124">-ResourceGroupName</span></span>
<span data-ttu-id="f3854-125">Especifica o nome do grupo de recursos que contém o gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="f3854-125">Specifies the name of the resource group that contains the local network gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3854-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f3854-126">-Confirm</span></span>
<span data-ttu-id="f3854-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3854-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3854-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3854-128">-WhatIf</span></span>
<span data-ttu-id="f3854-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f3854-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3854-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f3854-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3854-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3854-131">CommonParameters</span></span>
<span data-ttu-id="f3854-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3854-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3854-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3854-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3854-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f3854-134">INPUTS</span></span>

## <span data-ttu-id="f3854-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f3854-135">OUTPUTS</span></span>

## <span data-ttu-id="f3854-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f3854-136">NOTES</span></span>

## <span data-ttu-id="f3854-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3854-137">RELATED LINKS</span></span>

[<span data-ttu-id="f3854-138">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f3854-138">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="f3854-139">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f3854-139">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="f3854-140">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f3854-140">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)


