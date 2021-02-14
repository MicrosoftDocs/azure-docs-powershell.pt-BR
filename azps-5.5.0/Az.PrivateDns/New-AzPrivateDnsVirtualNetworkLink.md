---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/New-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: be1480b68c4b0fd66328a7ff417517ee86cb88df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117245"
---
# <span data-ttu-id="df308-101">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="df308-101">New-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="df308-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df308-102">SYNOPSIS</span></span>
<span data-ttu-id="df308-103">Cria um novo link de rede virtual DNS particular.</span><span class="sxs-lookup"><span data-stu-id="df308-103">Creates a new private DNS virtual network link.</span></span>

## <span data-ttu-id="df308-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df308-104">SYNTAX</span></span>

### <span data-ttu-id="df308-105">VirtualNetworkId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="df308-105">VirtualNetworkId (Default)</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df308-106">VirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="df308-106">VirtualNetworkObject</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetwork <VirtualNetwork> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df308-107">RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="df308-107">RemoteVirtualNetworkId</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df308-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="df308-108">DESCRIPTION</span></span>
<span data-ttu-id="df308-109">O cmdlet **New-AzPrivateDnsVirtualNetworkLink** cria um novo link de rede virtual DNS (Sistema de Nomes de Domínio) particular no grupo de recursos especificado e na zona privada.</span><span class="sxs-lookup"><span data-stu-id="df308-109">The **New-AzPrivateDnsVirtualNetworkLink** cmdlet creates a new private Domain Name System (DNS) virtual network link in the specified resource group and private zone.</span></span> <span data-ttu-id="df308-110">Você deve especificar um nome de link exclusivo para *o* parâmetro Nome ou o cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="df308-110">You must specify a unique link name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="df308-111">Você pode usar o *parâmetro Confirmar* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="df308-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="df308-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="df308-112">EXAMPLES</span></span>

### <span data-ttu-id="df308-113">Exemplo 1: Criar um link de rede virtual DNS particular</span><span class="sxs-lookup"><span data-stu-id="df308-113">Example 1: Create a Private DNS virtual network link</span></span>
```
PS C:\>$Link = New-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -VirtualNetworkId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork" -EnableRegistration

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="df308-114">Esse comando cria um novo link de rede virtual associado à zona DNS privada chamada myzone.com e à rede virtual "myvirtualnetwork" (que já foi criada no grupo de recursos) no grupo de recursos especificado e a armazena na variável $Link.</span><span class="sxs-lookup"><span data-stu-id="df308-114">This command creates a new virtual network link associated with the private DNS zone named myzone.com and virtual network "myvirtualnetwork" (which has already been created in the resource group) in the specified resource group, and then stores it in the $Link variable.</span></span>

## <span data-ttu-id="df308-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df308-115">PARAMETERS</span></span>

### <span data-ttu-id="df308-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df308-116">-DefaultProfile</span></span>
<span data-ttu-id="df308-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="df308-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df308-118">-EnableRegistration</span><span class="sxs-lookup"><span data-stu-id="df308-118">-EnableRegistration</span></span>
<span data-ttu-id="df308-119">Alternar parâmetro que representa se o link está habilitado ou não para registro.</span><span class="sxs-lookup"><span data-stu-id="df308-119">Switch parameter that represents if the link is registration enabled or not.</span></span>

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

### <span data-ttu-id="df308-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="df308-120">-Name</span></span>
<span data-ttu-id="df308-121">Especifica o nome do link de rede virtual a ser criado.</span><span class="sxs-lookup"><span data-stu-id="df308-121">Specifies the name of the virtual network link to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df308-122">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="df308-122">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="df308-123">A ID do recurso da rede virtual em outro locatário.</span><span class="sxs-lookup"><span data-stu-id="df308-123">The resource id of the virtual network in another tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoteVirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df308-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df308-124">-ResourceGroupName</span></span>
<span data-ttu-id="df308-125">Especifica o grupo de recursos no qual criar o link.</span><span class="sxs-lookup"><span data-stu-id="df308-125">Specifies the resource group in which to create the link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df308-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="df308-126">-Tag</span></span>
<span data-ttu-id="df308-127">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="df308-127">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df308-128">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df308-128">-VirtualNetwork</span></span>
<span data-ttu-id="df308-129">O objeto de rede virtual associado ao link.</span><span class="sxs-lookup"><span data-stu-id="df308-129">The virtual network object associated with the link.</span></span>

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IVirtualNetwork
Parameter Sets: VirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df308-130">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="df308-130">-VirtualNetworkId</span></span>
<span data-ttu-id="df308-131">A ID do recurso da rede virtual associada ao link.</span><span class="sxs-lookup"><span data-stu-id="df308-131">The resource id of the virtual network associated with the link.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df308-132">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="df308-132">-ZoneName</span></span>
<span data-ttu-id="df308-133">Especifica o nome da zona que será vinculada ao link de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="df308-133">Specifies the name of the zone which will be linked to the virtual network link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df308-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="df308-134">-Confirm</span></span>
<span data-ttu-id="df308-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df308-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df308-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df308-136">-WhatIf</span></span>
<span data-ttu-id="df308-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="df308-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df308-138">O cmdlet não é executado. Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="df308-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df308-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="df308-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df308-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df308-140">CommonParameters</span></span>
<span data-ttu-id="df308-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df308-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df308-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df308-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df308-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="df308-143">INPUTS</span></span>

### <span data-ttu-id="df308-144">Nenhum</span><span class="sxs-lookup"><span data-stu-id="df308-144">None</span></span>

## <span data-ttu-id="df308-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="df308-145">OUTPUTS</span></span>

### <span data-ttu-id="df308-146">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="df308-146">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="df308-147">Notas</span><span class="sxs-lookup"><span data-stu-id="df308-147">NOTES</span></span>

## <span data-ttu-id="df308-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df308-148">RELATED LINKS</span></span>

[<span data-ttu-id="df308-149">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="df308-149">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="df308-150">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="df308-150">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="df308-151">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="df308-151">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)
