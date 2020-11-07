---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d54dac2689fd751663ebf0046288c4d4ceeae928
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773081"
---
# <span data-ttu-id="2635d-101">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="2635d-101">Remove-AzPrivateDnsZone</span></span>

## <span data-ttu-id="2635d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2635d-102">SYNOPSIS</span></span>
<span data-ttu-id="2635d-103">Remove uma zona DNS privada de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2635d-103">Removes a private DNS zone from a resource group.</span></span>

## <span data-ttu-id="2635d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2635d-104">SYNTAX</span></span>

### <span data-ttu-id="2635d-105">Campos (padrão)</span><span class="sxs-lookup"><span data-stu-id="2635d-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2635d-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="2635d-106">Object</span></span>
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2635d-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="2635d-107">ResourceId</span></span>
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2635d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2635d-108">DESCRIPTION</span></span>
<span data-ttu-id="2635d-109">O cmdlet **Remove-AzPrivateDnsZone** exclui permanentemente uma zona de sistema de nome de domínio (DNS) privada de um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="2635d-109">The **Remove-AzPrivateDnsZone** cmdlet permanently deletes a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="2635d-110">Todos os conjuntos de registros contidos na zona também são excluídos.</span><span class="sxs-lookup"><span data-stu-id="2635d-110">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="2635d-111">Você pode passar um objeto **PrivateDnsZone** usando o parâmetro *PrivateZone* ou usando o operador pipeline ou, como alternativa, pode especificar o *nome* e os parâmetros de *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="2635d-111">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="2635d-112">Você pode usar o parâmetro Confirm e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="2635d-112">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="2635d-113">Ao especificar a zona usando um objeto **PrivateDnsZone** (passado por meio do parâmetro pipeline ou *Zone* ), a zona não será excluída se ela tiver sido alterada no Azure DNS desde que o objeto **PrivateDnsZone** local tenha sido recuperado (somente operações diretamente na contagem de recursos de zona DNS como alterações, operações em conjuntos de registros dentro da zona não).</span><span class="sxs-lookup"><span data-stu-id="2635d-113">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="2635d-114">Isso fornece proteção para alterações de zona simultâneas.</span><span class="sxs-lookup"><span data-stu-id="2635d-114">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="2635d-115">Isso pode ser suprimido usando o parâmetro *overwrite* , que exclui a zona independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="2635d-115">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="2635d-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2635d-116">EXAMPLES</span></span>

### <span data-ttu-id="2635d-117">Exemplo 1: remover uma zona privada</span><span class="sxs-lookup"><span data-stu-id="2635d-117">Example 1: Remove a private zone</span></span>
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="2635d-118">Esse comando Remove a zona chamada myzone.com do grupo de recursos chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="2635d-118">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="2635d-119">OS</span><span class="sxs-lookup"><span data-stu-id="2635d-119">PARAMETERS</span></span>

### <span data-ttu-id="2635d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2635d-120">-DefaultProfile</span></span>
<span data-ttu-id="2635d-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2635d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2635d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2635d-122">-Name</span></span>
<span data-ttu-id="2635d-123">Especifica o nome da zona DNS privada que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="2635d-123">Specifies the name of the private DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="2635d-124">Você também deve especificar o parâmetro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="2635d-124">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="2635d-125">Você também pode especificar a zona DNS usando o parâmetro *Zone* .</span><span class="sxs-lookup"><span data-stu-id="2635d-125">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="2635d-126">-Substituir</span><span class="sxs-lookup"><span data-stu-id="2635d-126">-Overwrite</span></span>
<span data-ttu-id="2635d-127">Ao especificar a zona usando um objeto **PrivateDnsZone** (passado por meio do parâmetro pipeline ou *Zone* ), a zona não será excluída se ela tiver sido alterada no Azure DNS desde que o objeto **PrivateDnsZone** local tenha sido recuperado (somente operações diretamente na contagem de recursos de zona DNS como alterações, operações em conjuntos de registros dentro da zona não).</span><span class="sxs-lookup"><span data-stu-id="2635d-127">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="2635d-128">Isso fornece proteção para alterações de zona simultâneas.</span><span class="sxs-lookup"><span data-stu-id="2635d-128">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="2635d-129">Isso pode ser suprimido usando o parâmetro *overwrite* , que exclui a zona independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="2635d-129">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="2635d-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2635d-130">-PassThru</span></span>
<span data-ttu-id="2635d-131">Usado para passar o resultado (booliano) da operação excluir zona privada mais adiante no pipeline.</span><span class="sxs-lookup"><span data-stu-id="2635d-131">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="2635d-132">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="2635d-132">-PrivateZone</span></span>
<span data-ttu-id="2635d-133">O objeto de zona particular a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="2635d-133">The private zone object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2635d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2635d-134">-ResourceGroupName</span></span>
<span data-ttu-id="2635d-135">Especifica o nome do grupo de recursos que contém a zona a ser removida.</span><span class="sxs-lookup"><span data-stu-id="2635d-135">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="2635d-136">Você também deve especificar o parâmetro *zonename* .</span><span class="sxs-lookup"><span data-stu-id="2635d-136">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="2635d-137">Como alternativa, você pode especificar a zona DNS usando um objeto **PrivateDnsZone** , transmitido via o pipeline ou o parâmetro *Zone* .</span><span class="sxs-lookup"><span data-stu-id="2635d-137">Alternatively, you can specify the DNS zone using a **PrivateDnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="2635d-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2635d-138">-ResourceId</span></span>
<span data-ttu-id="2635d-139">ResourceId de zona DNS particular.</span><span class="sxs-lookup"><span data-stu-id="2635d-139">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="2635d-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2635d-140">-Confirm</span></span>
<span data-ttu-id="2635d-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2635d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2635d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2635d-142">-WhatIf</span></span>
<span data-ttu-id="2635d-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2635d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2635d-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2635d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2635d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2635d-145">CommonParameters</span></span>
<span data-ttu-id="2635d-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2635d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2635d-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2635d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2635d-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2635d-148">INPUTS</span></span>

### <span data-ttu-id="2635d-149">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="2635d-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="2635d-150">System. String</span><span class="sxs-lookup"><span data-stu-id="2635d-150">System.String</span></span>

## <span data-ttu-id="2635d-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2635d-151">OUTPUTS</span></span>

### <span data-ttu-id="2635d-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2635d-152">System.Boolean</span></span>

## <span data-ttu-id="2635d-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2635d-153">NOTES</span></span>

## <span data-ttu-id="2635d-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2635d-154">RELATED LINKS</span></span>

[<span data-ttu-id="2635d-155">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="2635d-155">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="2635d-156">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="2635d-156">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="2635d-157">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="2635d-157">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
