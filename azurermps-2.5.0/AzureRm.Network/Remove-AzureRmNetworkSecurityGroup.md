---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 32709a1a0280604b784c9f094478858f8c4bc4ab
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785468"
---
# <span data-ttu-id="ab1fe-101">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ab1fe-101">Remove-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="ab1fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab1fe-102">SYNOPSIS</span></span>
<span data-ttu-id="ab1fe-103">Remove um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="ab1fe-103">Removes a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab1fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab1fe-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab1fe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ab1fe-105">DESCRIPTION</span></span>
<span data-ttu-id="ab1fe-106">O cmdlet **Remove-AzureRmNetworkSecurityGroup** remove um grupo de segurança de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="ab1fe-106">The **Remove-AzureRmNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="ab1fe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab1fe-107">EXAMPLES</span></span>

### <span data-ttu-id="ab1fe-108">Exemplo 1: remover um grupo de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="ab1fe-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="ab1fe-109">Esse comando Remove o grupo de segurança chamado NSG-FrontEnd no grupo de recursos chamado TestRG.</span><span class="sxs-lookup"><span data-stu-id="ab1fe-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="ab1fe-110">OS</span><span class="sxs-lookup"><span data-stu-id="ab1fe-110">PARAMETERS</span></span>

### <span data-ttu-id="ab1fe-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab1fe-111">-AsJob</span></span>
<span data-ttu-id="ab1fe-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ab1fe-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab1fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab1fe-113">-DefaultProfile</span></span>
<span data-ttu-id="ab1fe-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab1fe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab1fe-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ab1fe-115">-Force</span></span>
<span data-ttu-id="ab1fe-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="ab1fe-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ab1fe-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab1fe-117">-Name</span></span>
<span data-ttu-id="ab1fe-118">Especifica o nome do grupo de segurança de rede que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="ab1fe-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ab1fe-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab1fe-119">-PassThru</span></span>
<span data-ttu-id="ab1fe-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="ab1fe-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ab1fe-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="ab1fe-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ab1fe-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab1fe-122">-ResourceGroupName</span></span>
<span data-ttu-id="ab1fe-123">Especifica o nome de um grupo de recursos do qual este cmdlet Remove um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="ab1fe-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="ab1fe-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ab1fe-124">-Confirm</span></span>
<span data-ttu-id="ab1fe-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab1fe-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab1fe-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab1fe-126">-WhatIf</span></span>
<span data-ttu-id="ab1fe-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ab1fe-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab1fe-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ab1fe-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab1fe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab1fe-129">CommonParameters</span></span>
<span data-ttu-id="ab1fe-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab1fe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab1fe-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab1fe-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab1fe-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ab1fe-132">INPUTS</span></span>

## <span data-ttu-id="ab1fe-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ab1fe-133">OUTPUTS</span></span>

## <span data-ttu-id="ab1fe-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ab1fe-134">NOTES</span></span>

## <span data-ttu-id="ab1fe-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab1fe-135">RELATED LINKS</span></span>

[<span data-ttu-id="ab1fe-136">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ab1fe-136">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="ab1fe-137">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ab1fe-137">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="ab1fe-138">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ab1fe-138">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


