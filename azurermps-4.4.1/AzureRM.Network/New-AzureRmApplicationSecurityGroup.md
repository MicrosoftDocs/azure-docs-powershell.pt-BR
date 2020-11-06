---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 97a49535ab02b2ccd75a1f7520bcd8a1e3e6264f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609986"
---
# <span data-ttu-id="bc62a-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bc62a-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="bc62a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc62a-102">SYNOPSIS</span></span>
<span data-ttu-id="bc62a-103">Cria um grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bc62a-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc62a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc62a-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc62a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc62a-105">DESCRIPTION</span></span>
<span data-ttu-id="bc62a-106">O cmdlet **New-AzureRmApplicationSecurityGroup** cria um grupo de segurança de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bc62a-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="bc62a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc62a-107">EXAMPLES</span></span>

### <span data-ttu-id="bc62a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bc62a-108">Example 1</span></span>
```
PS C:\> New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="bc62a-109">Este exemplo cria um grupo de segurança de aplicativo sem associações.</span><span class="sxs-lookup"><span data-stu-id="bc62a-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="bc62a-110">Após a criação, as configurações de IP na interface de rede podem ser incluídas no grupo.</span><span class="sxs-lookup"><span data-stu-id="bc62a-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="bc62a-111">As regras de segurança também podem se referir ao grupo como suas origens ou destinos.</span><span class="sxs-lookup"><span data-stu-id="bc62a-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="bc62a-112">OS</span><span class="sxs-lookup"><span data-stu-id="bc62a-112">PARAMETERS</span></span>

### <span data-ttu-id="bc62a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc62a-113">-DefaultProfile</span></span>
<span data-ttu-id="bc62a-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc62a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc62a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bc62a-115">-Force</span></span>
<span data-ttu-id="bc62a-116">Não peça confirmação se quiser substituir um recurso.</span><span class="sxs-lookup"><span data-stu-id="bc62a-116">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="bc62a-117">-Local</span><span class="sxs-lookup"><span data-stu-id="bc62a-117">-Location</span></span>
<span data-ttu-id="bc62a-118">O local.</span><span class="sxs-lookup"><span data-stu-id="bc62a-118">The location.</span></span>

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

### <span data-ttu-id="bc62a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc62a-119">-Name</span></span>
<span data-ttu-id="bc62a-120">O nome do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bc62a-120">The name of the application security group.</span></span>

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

### <span data-ttu-id="bc62a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc62a-121">-ResourceGroupName</span></span>
<span data-ttu-id="bc62a-122">O nome do grupo de recursos do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bc62a-122">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="bc62a-123">-Marca</span><span class="sxs-lookup"><span data-stu-id="bc62a-123">-Tag</span></span>
<span data-ttu-id="bc62a-124">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="bc62a-124">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc62a-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bc62a-125">-Confirm</span></span>
<span data-ttu-id="bc62a-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc62a-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc62a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc62a-127">-WhatIf</span></span>
<span data-ttu-id="bc62a-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bc62a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc62a-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bc62a-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc62a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc62a-130">CommonParameters</span></span>
<span data-ttu-id="bc62a-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc62a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc62a-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc62a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc62a-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc62a-133">INPUTS</span></span>

### <span data-ttu-id="bc62a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bc62a-134">System.String</span></span>
<span data-ttu-id="bc62a-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bc62a-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bc62a-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc62a-136">OUTPUTS</span></span>

### <span data-ttu-id="bc62a-137">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bc62a-137">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="bc62a-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc62a-138">NOTES</span></span>

## <span data-ttu-id="bc62a-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc62a-139">RELATED LINKS</span></span>

[<span data-ttu-id="bc62a-140">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bc62a-140">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="bc62a-141">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bc62a-141">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="bc62a-142">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bc62a-142">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="bc62a-143">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bc62a-143">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="bc62a-144">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bc62a-144">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="bc62a-145">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bc62a-145">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bc62a-146">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bc62a-146">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bc62a-147">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bc62a-147">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
