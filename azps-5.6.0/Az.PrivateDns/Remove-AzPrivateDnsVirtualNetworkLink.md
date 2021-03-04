---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 8de4922b5d71902fe22a17a6c02f21a40e35ddc7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887080"
---
# <span data-ttu-id="669a3-101">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="669a3-101">Remove-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="669a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="669a3-102">SYNOPSIS</span></span>
<span data-ttu-id="669a3-103">Remove um link de rede virtual de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="669a3-103">Removes a virtual network link from a resource group.</span></span>

## <span data-ttu-id="669a3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="669a3-104">SYNTAX</span></span>

### <span data-ttu-id="669a3-105">Campos (Padrão)</span><span class="sxs-lookup"><span data-stu-id="669a3-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="669a3-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="669a3-106">Object</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="669a3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="669a3-107">ResourceId</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="669a3-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="669a3-108">DESCRIPTION</span></span>
<span data-ttu-id="669a3-109">O cmdlet **Remove-AzPrivateDnsVirtualNetworkLink** exclui permanentemente um link DNS de um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="669a3-109">The **Remove-AzPrivateDnsVirtualNetworkLink** cmdlet permanently deletes a private Domain Name System (DNS) link from a specified resource group.</span></span>
<span data-ttu-id="669a3-110">Você pode passar um **objeto PSPrivateDnsVirtualNetworkLink** usando o parâmetro *Link* ou usando o operador de pipeline ou, como alternativa, pode especificar os parâmetros *Name* *ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="669a3-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="669a3-111">Você pode usar o parâmetro Confirm e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="669a3-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="669a3-112">Ao especificar o link usando um objeto **PSPrivateDnsVirtualNetworkLink** (passado pelo pipeline ou pelo parâmetro *Link),* o link não será excluído se tiver sido alterado no DNS privado do Azure desde que o objeto **PSPrivateDnsVirtualNetworkLink** local foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="669a3-112">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure Private DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="669a3-113">Isso fornece proteção para alterações de zona simultâneas.</span><span class="sxs-lookup"><span data-stu-id="669a3-113">This provides protection for concurrent zone changes.</span></span> <span data-ttu-id="669a3-114">Isso pode ser suprimido usando o parâmetro *Overwrite,* que exclui a zona independentemente de alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="669a3-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="669a3-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="669a3-115">EXAMPLES</span></span>

### <span data-ttu-id="669a3-116">Exemplo 1: Remover um link</span><span class="sxs-lookup"><span data-stu-id="669a3-116">Example 1: Remove a link</span></span>
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

<span data-ttu-id="669a3-117">Este comando remove o link chamado mylink vinculado ao myzone.com de zona do grupo de recursos chamado MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="669a3-117">This command removes the link named mylink linked to zone myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="669a3-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="669a3-118">PARAMETERS</span></span>

### <span data-ttu-id="669a3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="669a3-119">-DefaultProfile</span></span>
<span data-ttu-id="669a3-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="669a3-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="669a3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="669a3-121">-InputObject</span></span>
<span data-ttu-id="669a3-122">O objeto de link de rede virtual a ser removido.</span><span class="sxs-lookup"><span data-stu-id="669a3-122">The virtual network link object to remove.</span></span>

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

### <span data-ttu-id="669a3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="669a3-123">-Name</span></span>
<span data-ttu-id="669a3-124">Especifica o nome do link a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="669a3-124">Specifies the name of the link to be deleted.</span></span>
<span data-ttu-id="669a3-125">Você também deve especificar o *parâmetro ResourceGroupName* e *ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="669a3-125">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="669a3-126">Como alternativa, você pode especificar o link usando o *parâmetro Link.*</span><span class="sxs-lookup"><span data-stu-id="669a3-126">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="669a3-127">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="669a3-127">-Overwrite</span></span>
<span data-ttu-id="669a3-128">Ao especificar a zona usando um **objeto PSPrivateDnsVirtualNetworkLink** (passado pelo pipeline ou pelo parâmetro *Link),* a zona não será excluída se tiver sido alterada no DNS do Azure desde que o objeto **PSPrivateDnsVirtualNetworkLink** local foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="669a3-128">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="669a3-129">Isso fornece proteção para alterações de zona simultâneas.</span><span class="sxs-lookup"><span data-stu-id="669a3-129">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="669a3-130">Isso pode ser suprimido usando o parâmetro *Overwrite,* que exclui a zona independentemente de alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="669a3-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="669a3-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="669a3-131">-PassThru</span></span>
<span data-ttu-id="669a3-132">Usado para passar o resultado (booleano) da operação excluir link de rede virtual mais abaixo do pipeline.</span><span class="sxs-lookup"><span data-stu-id="669a3-132">Used for passing the result (boolean) of the operation delete virtual network link further down the pipeline.</span></span>

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

### <span data-ttu-id="669a3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="669a3-133">-ResourceGroupName</span></span>
<span data-ttu-id="669a3-134">Especifica o nome do grupo de recursos que contém o link a ser removido.</span><span class="sxs-lookup"><span data-stu-id="669a3-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="669a3-135">Você também deve especificar o parâmetro *ZoneName* e *Name.*</span><span class="sxs-lookup"><span data-stu-id="669a3-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="669a3-136">Como alternativa, você pode especificar a zona DNS usando um **objeto PSPrivateDnsVirtualNetworkLink,** passado pelo pipeline ou pelo *parâmetro Link.*</span><span class="sxs-lookup"><span data-stu-id="669a3-136">Alternatively, you can specify the DNS zone using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="669a3-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="669a3-137">-ResourceId</span></span>
<span data-ttu-id="669a3-138">Especifica a ARM de recurso do link.</span><span class="sxs-lookup"><span data-stu-id="669a3-138">Specifies the ARM resource ID of the link.</span></span>

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

### <span data-ttu-id="669a3-139">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="669a3-139">-ZoneName</span></span>
<span data-ttu-id="669a3-140">Especifica o nome da zona DNS privada à que o link está associado.</span><span class="sxs-lookup"><span data-stu-id="669a3-140">Specifies the name of the private DNS zone that the link is associated with.</span></span>
<span data-ttu-id="669a3-141">Você também deve especificar o *parâmetro ResourceGroupName* e *Name.*</span><span class="sxs-lookup"><span data-stu-id="669a3-141">You must also specify the *ResourceGroupName* and *Name* parameter.</span></span>
<span data-ttu-id="669a3-142">Como alternativa, você pode especificar o link usando o *parâmetro Link.*</span><span class="sxs-lookup"><span data-stu-id="669a3-142">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="669a3-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="669a3-143">-Confirm</span></span>
<span data-ttu-id="669a3-144">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="669a3-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="669a3-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="669a3-145">-WhatIf</span></span>
<span data-ttu-id="669a3-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="669a3-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="669a3-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="669a3-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="669a3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="669a3-148">CommonParameters</span></span>
<span data-ttu-id="669a3-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="669a3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="669a3-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="669a3-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="669a3-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="669a3-151">INPUTS</span></span>

### <span data-ttu-id="669a3-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="669a3-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="669a3-153">System.String</span><span class="sxs-lookup"><span data-stu-id="669a3-153">System.String</span></span>

## <span data-ttu-id="669a3-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="669a3-154">OUTPUTS</span></span>

### <span data-ttu-id="669a3-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="669a3-155">System.Boolean</span></span>

## <span data-ttu-id="669a3-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="669a3-156">NOTES</span></span>

## <span data-ttu-id="669a3-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="669a3-157">RELATED LINKS</span></span>

[<span data-ttu-id="669a3-158">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="669a3-158">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="669a3-159">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="669a3-159">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="669a3-160">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="669a3-160">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
