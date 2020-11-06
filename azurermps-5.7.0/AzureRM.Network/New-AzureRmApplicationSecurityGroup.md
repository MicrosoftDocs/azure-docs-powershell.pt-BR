---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 82fdec48f2e021e33490f84a05a064fb007ac8d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428159"
---
# <span data-ttu-id="e07ab-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e07ab-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="e07ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e07ab-102">SYNOPSIS</span></span>
<span data-ttu-id="e07ab-103">Cria um grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e07ab-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e07ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e07ab-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e07ab-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e07ab-105">DESCRIPTION</span></span>
<span data-ttu-id="e07ab-106">O cmdlet **New-AzureRmApplicationSecurityGroup** cria um grupo de segurança de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e07ab-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="e07ab-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e07ab-107">EXAMPLES</span></span>

### <span data-ttu-id="e07ab-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e07ab-108">Example 1</span></span>
```
PS C:\> New-AzureRmApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="e07ab-109">Este exemplo cria um grupo de segurança de aplicativo sem associações.</span><span class="sxs-lookup"><span data-stu-id="e07ab-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="e07ab-110">Após a criação, as configurações de IP na interface de rede podem ser incluídas no grupo.</span><span class="sxs-lookup"><span data-stu-id="e07ab-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="e07ab-111">As regras de segurança também podem se referir ao grupo como suas origens ou destinos.</span><span class="sxs-lookup"><span data-stu-id="e07ab-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="e07ab-112">OS</span><span class="sxs-lookup"><span data-stu-id="e07ab-112">PARAMETERS</span></span>

### <span data-ttu-id="e07ab-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e07ab-113">-AsJob</span></span>
<span data-ttu-id="e07ab-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e07ab-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e07ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e07ab-115">-DefaultProfile</span></span>
<span data-ttu-id="e07ab-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e07ab-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e07ab-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e07ab-117">-Force</span></span>
<span data-ttu-id="e07ab-118">Não peça confirmação se quiser substituir um recurso.</span><span class="sxs-lookup"><span data-stu-id="e07ab-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="e07ab-119">-Local</span><span class="sxs-lookup"><span data-stu-id="e07ab-119">-Location</span></span>
<span data-ttu-id="e07ab-120">O local.</span><span class="sxs-lookup"><span data-stu-id="e07ab-120">The location.</span></span>

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

### <span data-ttu-id="e07ab-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e07ab-121">-Name</span></span>
<span data-ttu-id="e07ab-122">O nome do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e07ab-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="e07ab-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e07ab-123">-ResourceGroupName</span></span>
<span data-ttu-id="e07ab-124">O nome do grupo de recursos do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e07ab-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="e07ab-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="e07ab-125">-Tag</span></span>
<span data-ttu-id="e07ab-126">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="e07ab-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e07ab-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e07ab-127">-Confirm</span></span>
<span data-ttu-id="e07ab-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e07ab-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07ab-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e07ab-129">-WhatIf</span></span>
<span data-ttu-id="e07ab-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e07ab-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e07ab-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e07ab-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07ab-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e07ab-132">CommonParameters</span></span>
<span data-ttu-id="e07ab-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e07ab-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e07ab-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e07ab-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e07ab-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e07ab-135">INPUTS</span></span>

### <span data-ttu-id="e07ab-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e07ab-136">System.String</span></span>
<span data-ttu-id="e07ab-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e07ab-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e07ab-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e07ab-138">OUTPUTS</span></span>

### <span data-ttu-id="e07ab-139">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e07ab-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="e07ab-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e07ab-140">NOTES</span></span>

## <span data-ttu-id="e07ab-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e07ab-141">RELATED LINKS</span></span>

[<span data-ttu-id="e07ab-142">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e07ab-142">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="e07ab-143">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e07ab-143">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="e07ab-144">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e07ab-144">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e07ab-145">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e07ab-145">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e07ab-146">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e07ab-146">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e07ab-147">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e07ab-147">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e07ab-148">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e07ab-148">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e07ab-149">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e07ab-149">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
