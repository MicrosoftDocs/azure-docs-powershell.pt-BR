---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 63fbe26fa0a9ac7ca5eb985a3806886adeb2a2f8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260831"
---
# <span data-ttu-id="f4a19-101">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f4a19-101">Remove-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="f4a19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f4a19-102">SYNOPSIS</span></span>
<span data-ttu-id="f4a19-103">Remove um link de rede virtual de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f4a19-103">Removes a virtual network link from a resource group.</span></span>

## <span data-ttu-id="f4a19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4a19-104">SYNTAX</span></span>

### <span data-ttu-id="f4a19-105">Campos (padrão)</span><span class="sxs-lookup"><span data-stu-id="f4a19-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4a19-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="f4a19-106">Object</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4a19-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="f4a19-107">ResourceId</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4a19-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f4a19-108">DESCRIPTION</span></span>
<span data-ttu-id="f4a19-109">O cmdlet **Remove-AzPrivateDnsVirtualNetworkLink** exclui permanentemente um link DNS (sistema de nomes de domínio) privado de um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="f4a19-109">The **Remove-AzPrivateDnsVirtualNetworkLink** cmdlet permanently deletes a private Domain Name System (DNS) link from a specified resource group.</span></span>
<span data-ttu-id="f4a19-110">Você pode passar um objeto **PSPrivateDnsVirtualNetworkLink** usando o parâmetro de *link* ou usando o operador de pipeline ou, como alternativa, pode especificar o *nome* *zonename* e os parâmetros *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="f4a19-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="f4a19-111">Você pode usar o parâmetro Confirm e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="f4a19-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="f4a19-112">Ao especificar o link usando um objeto **PSPrivateDnsVirtualNetworkLink** (passado pelo pipeline ou pelo parâmetro do *link* ), o link não será excluído se tiver sido alterado no DNS privado do Azure desde que o objeto **PSPrivateDnsVirtualNetworkLink** local foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="f4a19-112">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure Private DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="f4a19-113">Isso fornece proteção para alterações de zona simultâneas.</span><span class="sxs-lookup"><span data-stu-id="f4a19-113">This provides protection for concurrent zone changes.</span></span> <span data-ttu-id="f4a19-114">Isso pode ser suprimido usando o parâmetro *overwrite* , que exclui a zona independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="f4a19-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="f4a19-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4a19-115">EXAMPLES</span></span>

### <span data-ttu-id="f4a19-116">Exemplo 1: remover um link</span><span class="sxs-lookup"><span data-stu-id="f4a19-116">Example 1: Remove a link</span></span>
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

<span data-ttu-id="f4a19-117">Esse comando Remove o link nomeado MyLink vinculado à Zone myzone.com do grupo de recursos chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="f4a19-117">This command removes the link named mylink linked to zone myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="f4a19-118">OS</span><span class="sxs-lookup"><span data-stu-id="f4a19-118">PARAMETERS</span></span>

### <span data-ttu-id="f4a19-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4a19-119">-DefaultProfile</span></span>
<span data-ttu-id="f4a19-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f4a19-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4a19-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4a19-121">-InputObject</span></span>
<span data-ttu-id="f4a19-122">O objeto de conexão de rede virtual a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f4a19-122">The virtual network link object to remove.</span></span>

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

### <span data-ttu-id="f4a19-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4a19-123">-Name</span></span>
<span data-ttu-id="f4a19-124">Especifica o nome do link a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="f4a19-124">Specifies the name of the link to be deleted.</span></span>
<span data-ttu-id="f4a19-125">Você também deve especificar o parâmetro *ResourceGroupName* e *zonename* .</span><span class="sxs-lookup"><span data-stu-id="f4a19-125">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="f4a19-126">Ou, se preferir, você pode especificar o link usando o parâmetro de *link* .</span><span class="sxs-lookup"><span data-stu-id="f4a19-126">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="f4a19-127">-Substituir</span><span class="sxs-lookup"><span data-stu-id="f4a19-127">-Overwrite</span></span>
<span data-ttu-id="f4a19-128">Ao especificar a zona usando um objeto **PSPrivateDnsVirtualNetworkLink** (passado pelo pipeline ou pelo parâmetro do *link* ), a zona não é excluída se foi alterada no Azure DNS desde que o objeto **PSPrivateDnsVirtualNetworkLink** local foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="f4a19-128">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="f4a19-129">Isso fornece proteção para alterações de zona simultâneas.</span><span class="sxs-lookup"><span data-stu-id="f4a19-129">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="f4a19-130">Isso pode ser suprimido usando o parâmetro *overwrite* , que exclui a zona independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="f4a19-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="f4a19-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4a19-131">-PassThru</span></span>
<span data-ttu-id="f4a19-132">Usado para passar o resultado (booliano) da operação excluir o link de rede virtual mais adiante no pipeline.</span><span class="sxs-lookup"><span data-stu-id="f4a19-132">Used for passing the result (boolean) of the operation delete virtual network link further down the pipeline.</span></span>

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

### <span data-ttu-id="f4a19-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4a19-133">-ResourceGroupName</span></span>
<span data-ttu-id="f4a19-134">Especifica o nome do grupo de recursos que contém o link a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f4a19-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="f4a19-135">Você também deve especificar *zonename* e o parâmetro *Name* .</span><span class="sxs-lookup"><span data-stu-id="f4a19-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="f4a19-136">Como alternativa, você pode especificar a zona DNS usando um objeto **PSPrivateDnsVirtualNetworkLink** , passado pelo pipeline ou pelo parâmetro de *link* .</span><span class="sxs-lookup"><span data-stu-id="f4a19-136">Alternatively, you can specify the DNS zone using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="f4a19-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4a19-137">-ResourceId</span></span>
<span data-ttu-id="f4a19-138">Especifica a ID do recurso ARM do link.</span><span class="sxs-lookup"><span data-stu-id="f4a19-138">Specifies the ARM resource ID of the link.</span></span>

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

### <span data-ttu-id="f4a19-139">-Zonename</span><span class="sxs-lookup"><span data-stu-id="f4a19-139">-ZoneName</span></span>
<span data-ttu-id="f4a19-140">Especifica o nome da zona DNS privada à qual o link está associado.</span><span class="sxs-lookup"><span data-stu-id="f4a19-140">Specifies the name of the private DNS zone that the link is associated with.</span></span>
<span data-ttu-id="f4a19-141">Você também deve especificar o parâmetro *ResourceGroupName* e *Name* .</span><span class="sxs-lookup"><span data-stu-id="f4a19-141">You must also specify the *ResourceGroupName* and *Name* parameter.</span></span>
<span data-ttu-id="f4a19-142">Ou, se preferir, você pode especificar o link usando o parâmetro de *link* .</span><span class="sxs-lookup"><span data-stu-id="f4a19-142">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="f4a19-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f4a19-143">-Confirm</span></span>
<span data-ttu-id="f4a19-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4a19-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4a19-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4a19-145">-WhatIf</span></span>
<span data-ttu-id="f4a19-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f4a19-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4a19-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f4a19-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4a19-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4a19-148">CommonParameters</span></span>
<span data-ttu-id="f4a19-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4a19-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4a19-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4a19-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4a19-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f4a19-151">INPUTS</span></span>

### <span data-ttu-id="f4a19-152">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f4a19-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="f4a19-153">System. String</span><span class="sxs-lookup"><span data-stu-id="f4a19-153">System.String</span></span>

## <span data-ttu-id="f4a19-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f4a19-154">OUTPUTS</span></span>

### <span data-ttu-id="f4a19-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4a19-155">System.Boolean</span></span>

## <span data-ttu-id="f4a19-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f4a19-156">NOTES</span></span>

## <span data-ttu-id="f4a19-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4a19-157">RELATED LINKS</span></span>

[<span data-ttu-id="f4a19-158">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f4a19-158">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="f4a19-159">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f4a19-159">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="f4a19-160">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f4a19-160">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
