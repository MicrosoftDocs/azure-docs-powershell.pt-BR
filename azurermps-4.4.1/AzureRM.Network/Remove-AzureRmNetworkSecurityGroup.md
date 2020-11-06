---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: fd6d9a09bd2c4fa597d2c384d3ba8e730b3f1102
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602563"
---
# <span data-ttu-id="c9b03-101">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c9b03-101">Remove-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="c9b03-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9b03-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b03-103">Remove um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="c9b03-103">Removes a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9b03-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9b03-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9b03-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c9b03-105">DESCRIPTION</span></span>
<span data-ttu-id="c9b03-106">O cmdlet **Remove-AzureRmNetworkSecurityGroup** remove um grupo de segurança de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="c9b03-106">The **Remove-AzureRmNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="c9b03-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9b03-107">EXAMPLES</span></span>

### <span data-ttu-id="c9b03-108">Exemplo 1: remover um grupo de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="c9b03-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="c9b03-109">Esse comando Remove o grupo de segurança chamado NSG-FrontEnd no grupo de recursos chamado TestRG.</span><span class="sxs-lookup"><span data-stu-id="c9b03-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="c9b03-110">OS</span><span class="sxs-lookup"><span data-stu-id="c9b03-110">PARAMETERS</span></span>

### <span data-ttu-id="c9b03-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c9b03-111">-Force</span></span>
<span data-ttu-id="c9b03-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c9b03-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c9b03-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9b03-113">-Name</span></span>
<span data-ttu-id="c9b03-114">Especifica o nome do grupo de segurança de rede que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="c9b03-114">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c9b03-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9b03-115">-PassThru</span></span>
<span data-ttu-id="c9b03-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="c9b03-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c9b03-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="c9b03-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c9b03-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9b03-118">-ResourceGroupName</span></span>
<span data-ttu-id="c9b03-119">Especifica o nome de um grupo de recursos do qual este cmdlet Remove um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="c9b03-119">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="c9b03-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c9b03-120">-Confirm</span></span>
<span data-ttu-id="c9b03-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9b03-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9b03-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9b03-122">-WhatIf</span></span>
<span data-ttu-id="c9b03-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c9b03-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9b03-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c9b03-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9b03-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9b03-125">-DefaultProfile</span></span>
<span data-ttu-id="c9b03-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c9b03-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9b03-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b03-127">CommonParameters</span></span>
<span data-ttu-id="c9b03-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9b03-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b03-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9b03-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b03-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c9b03-130">INPUTS</span></span>

## <span data-ttu-id="c9b03-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c9b03-131">OUTPUTS</span></span>

## <span data-ttu-id="c9b03-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c9b03-132">NOTES</span></span>

## <span data-ttu-id="c9b03-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9b03-133">RELATED LINKS</span></span>

[<span data-ttu-id="c9b03-134">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c9b03-134">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="c9b03-135">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c9b03-135">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="c9b03-136">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c9b03-136">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


