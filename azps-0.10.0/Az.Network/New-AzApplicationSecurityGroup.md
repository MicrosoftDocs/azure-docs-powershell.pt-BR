---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 81eaa1f5c6e44586ae6ac9e5b6838f00063a9211
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775408"
---
# <span data-ttu-id="9ef66-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9ef66-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="9ef66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ef66-102">SYNOPSIS</span></span>
<span data-ttu-id="9ef66-103">Cria um grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9ef66-103">Creates an application security group.</span></span>

## <span data-ttu-id="9ef66-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ef66-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ef66-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ef66-105">DESCRIPTION</span></span>
<span data-ttu-id="9ef66-106">O cmdlet **New-AzApplicationSecurityGroup** cria um grupo de segurança de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9ef66-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="9ef66-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ef66-107">EXAMPLES</span></span>

### <span data-ttu-id="9ef66-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9ef66-108">Example 1</span></span>
```
PS C:\> New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="9ef66-109">Este exemplo cria um grupo de segurança de aplicativo sem associações.</span><span class="sxs-lookup"><span data-stu-id="9ef66-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="9ef66-110">Após a criação, as configurações de IP na interface de rede podem ser incluídas no grupo.</span><span class="sxs-lookup"><span data-stu-id="9ef66-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="9ef66-111">As regras de segurança também podem se referir ao grupo como suas origens ou destinos.</span><span class="sxs-lookup"><span data-stu-id="9ef66-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="9ef66-112">OS</span><span class="sxs-lookup"><span data-stu-id="9ef66-112">PARAMETERS</span></span>

### <span data-ttu-id="9ef66-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ef66-113">-AsJob</span></span>
<span data-ttu-id="9ef66-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9ef66-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ef66-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ef66-115">-DefaultProfile</span></span>
<span data-ttu-id="9ef66-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ef66-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ef66-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9ef66-117">-Force</span></span>
<span data-ttu-id="9ef66-118">Não peça confirmação se quiser substituir um recurso.</span><span class="sxs-lookup"><span data-stu-id="9ef66-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="9ef66-119">-Local</span><span class="sxs-lookup"><span data-stu-id="9ef66-119">-Location</span></span>
<span data-ttu-id="9ef66-120">O local.</span><span class="sxs-lookup"><span data-stu-id="9ef66-120">The location.</span></span>

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

### <span data-ttu-id="9ef66-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ef66-121">-Name</span></span>
<span data-ttu-id="9ef66-122">O nome do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9ef66-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="9ef66-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ef66-123">-ResourceGroupName</span></span>
<span data-ttu-id="9ef66-124">O nome do grupo de recursos do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9ef66-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="9ef66-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="9ef66-125">-Tag</span></span>
<span data-ttu-id="9ef66-126">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="9ef66-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="9ef66-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9ef66-127">-Confirm</span></span>
<span data-ttu-id="9ef66-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ef66-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ef66-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ef66-129">-WhatIf</span></span>
<span data-ttu-id="9ef66-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9ef66-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ef66-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9ef66-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ef66-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ef66-132">CommonParameters</span></span>
<span data-ttu-id="9ef66-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ef66-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ef66-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ef66-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ef66-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ef66-135">INPUTS</span></span>

### <span data-ttu-id="9ef66-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9ef66-136">System.String</span></span>
<span data-ttu-id="9ef66-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9ef66-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9ef66-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ef66-138">OUTPUTS</span></span>

### <span data-ttu-id="9ef66-139">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9ef66-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="9ef66-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ef66-140">NOTES</span></span>

## <span data-ttu-id="9ef66-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ef66-141">RELATED LINKS</span></span>

[<span data-ttu-id="9ef66-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9ef66-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="9ef66-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9ef66-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="9ef66-144">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9ef66-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9ef66-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9ef66-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9ef66-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9ef66-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9ef66-147">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9ef66-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="9ef66-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9ef66-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="9ef66-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9ef66-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
