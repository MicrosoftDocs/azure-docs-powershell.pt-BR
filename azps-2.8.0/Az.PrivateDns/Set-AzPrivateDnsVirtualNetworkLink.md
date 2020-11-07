---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: d2d00df48cbaf4bff1d6e9dac648004d73e65f2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773071"
---
# <span data-ttu-id="375c2-101">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="375c2-101">Set-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="375c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="375c2-102">SYNOPSIS</span></span>
<span data-ttu-id="375c2-103">Atualiza/define um link de rede virtual associado a uma zona privada e um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="375c2-103">Updates/Sets a virtual network link associated with a private zone and a resource group.</span></span>

## <span data-ttu-id="375c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="375c2-104">SYNTAX</span></span>

### <span data-ttu-id="375c2-105">Campos (padrão)</span><span class="sxs-lookup"><span data-stu-id="375c2-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="375c2-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="375c2-106">Object</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="375c2-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="375c2-107">ResourceId</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="375c2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="375c2-108">DESCRIPTION</span></span>
<span data-ttu-id="375c2-109">O cmdlet **set-AzPrivateDnsVirtualNetworkLink** atualiza um link associado a uma zona de um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="375c2-109">The **Set-AzPrivateDnsVirtualNetworkLink** cmdlet updates a link associated with a zone from a specified resource group.</span></span>
<span data-ttu-id="375c2-110">Você pode passar um objeto **PSPrivateDnsVirtualNetworkLink** usando o parâmetro de *link* ou usando o operador de pipeline ou, como alternativa, pode especificar o *nome* *zonename* e os parâmetros *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="375c2-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="375c2-111">Você pode usar o parâmetro Confirm e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="375c2-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="375c2-112">Ao especificar a zona usando um objeto **PSPrivateDnsVirtualNetworkLink** (passado pelo pipeline ou pelo parâmetro do *link* ), o link não será atualizado se ele tiver sido alterado no Azure DNS desde que o objeto **PSPrivateDnsVirtualNetworkLink** local tenha sido recuperado.</span><span class="sxs-lookup"><span data-stu-id="375c2-112">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not updated if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="375c2-113">Isso fornece proteção para alterações de links simultâneas.</span><span class="sxs-lookup"><span data-stu-id="375c2-113">This provides protection for concurrent link changes.</span></span> <span data-ttu-id="375c2-114">Isso pode ser suprimido usando o parâmetro *overwrite* , que atualiza o link independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="375c2-114">This can be suppressed using the *Overwrite* parameter, which updates the link regardless of concurrent changes.</span></span>

## <span data-ttu-id="375c2-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="375c2-115">EXAMPLES</span></span>

### <span data-ttu-id="375c2-116">Exemplo 1: definir um link</span><span class="sxs-lookup"><span data-stu-id="375c2-116">Example 1: Set a link</span></span>
```
PS C:\>Set-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -Tag @{} -IsRegistrationEnabled $true

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

<span data-ttu-id="375c2-117">Esse comando define IsRegistrationEnabled como true para o link chamado MyLink, vinculado ao Zone chamado myzone.com do grupo de recursos chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="375c2-117">This command sets IsRegistrationEnabled to True for the link named mylink, linked to zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="375c2-118">OS</span><span class="sxs-lookup"><span data-stu-id="375c2-118">PARAMETERS</span></span>

### <span data-ttu-id="375c2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="375c2-119">-DefaultProfile</span></span>
<span data-ttu-id="375c2-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="375c2-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="375c2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="375c2-121">-InputObject</span></span>
<span data-ttu-id="375c2-122">O objeto de conexão de rede virtual a ser definido.</span><span class="sxs-lookup"><span data-stu-id="375c2-122">The virtual network link object to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="375c2-123">-IsRegistrationEnabled</span><span class="sxs-lookup"><span data-stu-id="375c2-123">-IsRegistrationEnabled</span></span>
<span data-ttu-id="375c2-124">Booliano que representa se o registro está habilitado no link de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="375c2-124">Boolean that represents if registration is enabled on the virtual network link.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="375c2-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="375c2-125">-Name</span></span>
<span data-ttu-id="375c2-126">Especifica o nome do link que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="375c2-126">Specifies the name of the link that this cmdlet removes.</span></span>
<span data-ttu-id="375c2-127">Você também deve especificar o parâmetro *ResourceGroupName* e *zonename* .</span><span class="sxs-lookup"><span data-stu-id="375c2-127">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="375c2-128">Você também pode especificar o link DNS privado usando o parâmetro de *link* .</span><span class="sxs-lookup"><span data-stu-id="375c2-128">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="375c2-129">-Substituir</span><span class="sxs-lookup"><span data-stu-id="375c2-129">-Overwrite</span></span>
<span data-ttu-id="375c2-130">Ao especificar o link usando um objeto **PSPrivateDnsVirtualNetworkLink** (passado pelo pipeline ou pelo parâmetro do *link* ), o link não será excluído se ele tiver sido alterado no Azure DNS desde que o objeto **PSPrivateDnsVirtualNetworkLink** local tenha sido recuperado.</span><span class="sxs-lookup"><span data-stu-id="375c2-130">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="375c2-131">Isso fornece proteção para alterações de links simultâneas.</span><span class="sxs-lookup"><span data-stu-id="375c2-131">This provides protection for concurrent link changes.</span></span>
<span data-ttu-id="375c2-132">Isso pode ser suprimido usando o parâmetro *overwrite* , que exclui o link independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="375c2-132">This can be suppressed using the *Overwrite* parameter, which deletes the link regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="375c2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="375c2-133">-ResourceGroupName</span></span>
<span data-ttu-id="375c2-134">Especifica o nome do grupo de recursos que contém o link a ser removido.</span><span class="sxs-lookup"><span data-stu-id="375c2-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="375c2-135">Você também deve especificar *zonename* e o parâmetro *Name* .</span><span class="sxs-lookup"><span data-stu-id="375c2-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="375c2-136">Como alternativa, você pode especificar o link de rede virtual usando um objeto **PSPrivateDnsVirtualNetworkLink** , passado pelo pipeline ou pelo parâmetro de *link* .</span><span class="sxs-lookup"><span data-stu-id="375c2-136">Alternatively, you can specify the virtual network link using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="375c2-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="375c2-137">-ResourceId</span></span>
<span data-ttu-id="375c2-138">ResourceId de zona DNS particular.</span><span class="sxs-lookup"><span data-stu-id="375c2-138">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="375c2-139">-Marca</span><span class="sxs-lookup"><span data-stu-id="375c2-139">-Tag</span></span>
<span data-ttu-id="375c2-140">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="375c2-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="375c2-141">-Zonename</span><span class="sxs-lookup"><span data-stu-id="375c2-141">-ZoneName</span></span>
<span data-ttu-id="375c2-142">Especifica o nome da zona DNS que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="375c2-142">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="375c2-143">Você também deve especificar o *nome* e o parâmetro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="375c2-143">You must also specify the *Name* and *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="375c2-144">Você também pode especificar o link DNS privado usando o parâmetro de *link* .</span><span class="sxs-lookup"><span data-stu-id="375c2-144">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="375c2-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="375c2-145">-Confirm</span></span>
<span data-ttu-id="375c2-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="375c2-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="375c2-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="375c2-147">-WhatIf</span></span>
<span data-ttu-id="375c2-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="375c2-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="375c2-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="375c2-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="375c2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="375c2-150">CommonParameters</span></span>
<span data-ttu-id="375c2-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="375c2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="375c2-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="375c2-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="375c2-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="375c2-153">INPUTS</span></span>

### <span data-ttu-id="375c2-154">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="375c2-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="375c2-155">System. String</span><span class="sxs-lookup"><span data-stu-id="375c2-155">System.String</span></span>

## <span data-ttu-id="375c2-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="375c2-156">OUTPUTS</span></span>

### <span data-ttu-id="375c2-157">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="375c2-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="375c2-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="375c2-158">NOTES</span></span>

## <span data-ttu-id="375c2-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="375c2-159">RELATED LINKS</span></span>

[<span data-ttu-id="375c2-160">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="375c2-160">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="375c2-161">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="375c2-161">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="375c2-162">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="375c2-162">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
