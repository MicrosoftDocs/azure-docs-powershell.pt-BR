---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: 06b8a8bd7027b95d7f51e186b0184707ffd296a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948077"
---
# <span data-ttu-id="d147f-101">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="d147f-101">Set-AzPrivateDnsZone</span></span>

## <span data-ttu-id="d147f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d147f-102">SYNOPSIS</span></span>
<span data-ttu-id="d147f-103">Atualiza uma zona DNS privada de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d147f-103">Updates a Private DNS zone from a resource group.</span></span>

## <span data-ttu-id="d147f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d147f-104">SYNTAX</span></span>

### <span data-ttu-id="d147f-105">Campos (padrão)</span><span class="sxs-lookup"><span data-stu-id="d147f-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d147f-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="d147f-106">ResourceId</span></span>
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d147f-107">Objeto</span><span class="sxs-lookup"><span data-stu-id="d147f-107">Object</span></span>
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d147f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d147f-108">DESCRIPTION</span></span>
<span data-ttu-id="d147f-109">O cmdlet **set-AzPrivateDnsZone** atualiza permanentemente uma zona de sistema de nome de domínio (DNS) privada de um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="d147f-109">The **Set-AzPrivateDnsZone** cmdlet permanently updates a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="d147f-110">Você pode passar um objeto **PrivateDnsZone** usando o parâmetro *PrivateZone* ou usando o operador pipeline ou, como alternativa, pode especificar o *nome* e os parâmetros de *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="d147f-110">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="d147f-111">Você pode usar o parâmetro Confirm e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="d147f-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="d147f-112">Ao especificar a zona usando um objeto **PrivateDnsZone** (passado por meio do parâmetro pipeline ou *Zone* ), a zona não será atualizada se ela tiver sido alterada no Azure DNS desde que o objeto **PrivateDnsZone** local tenha sido recuperado (somente operações diretamente na contagem de recursos de zona DNS como alterações, operações em conjuntos de registros dentro da zona não).</span><span class="sxs-lookup"><span data-stu-id="d147f-112">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="d147f-113">Isso fornece proteção para alterações de zona simultâneas.</span><span class="sxs-lookup"><span data-stu-id="d147f-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="d147f-114">Isso pode ser suprimido usando o parâmetro *overwrite* , que atualiza a zona independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="d147f-114">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="d147f-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d147f-115">EXAMPLES</span></span>

### <span data-ttu-id="d147f-116">Exemplo 1: atualiza uma zona privada</span><span class="sxs-lookup"><span data-stu-id="d147f-116">Example 1: Updates a private zone</span></span>
```
PS C:\>Set-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup" -Tag @{tag1="value1";tag2="value2"}


This command updates the zone named myzone.com from the resource group named MyResourceGroup with the tags provided. Use Get-AzPrivateDnsZone to retrieve the updated zone. Updated zone would look something like this:

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {tag1="value1";tag2="value2"}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="d147f-117">OS</span><span class="sxs-lookup"><span data-stu-id="d147f-117">PARAMETERS</span></span>

### <span data-ttu-id="d147f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d147f-118">-DefaultProfile</span></span>
<span data-ttu-id="d147f-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d147f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d147f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d147f-120">-Name</span></span>
<span data-ttu-id="d147f-121">Especifica o nome da zona DNS privada que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="d147f-121">Specifies the name of the Private DNS zone that this cmdlet updates.</span></span>
<span data-ttu-id="d147f-122">Você também deve especificar o parâmetro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="d147f-122">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="d147f-123">Você também pode especificar a zona DNS privada usando o parâmetro *Zone* .</span><span class="sxs-lookup"><span data-stu-id="d147f-123">Alternatively, you can specify the private DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="d147f-124">-Substituir</span><span class="sxs-lookup"><span data-stu-id="d147f-124">-Overwrite</span></span>
<span data-ttu-id="d147f-125">Ao especificar a zona usando um objeto **PrivateDnsZone** (passado por meio do parâmetro pipeline ou *Zone* ), a zona não será atualizada se ela tiver sido alterada no Azure DNS, pois o objeto **dnsZone** local foi recuperado (somente operações diretamente na contagem de recursos de zona DNS como alterações, operações em conjuntos de registros dentro da zona não).</span><span class="sxs-lookup"><span data-stu-id="d147f-125">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="d147f-126">Isso fornece proteção para alterações de zona simultâneas.</span><span class="sxs-lookup"><span data-stu-id="d147f-126">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="d147f-127">Isso pode ser suprimido usando o parâmetro *overwrite* , que atualiza a zona independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="d147f-127">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="d147f-128">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="d147f-128">-PrivateZone</span></span>
<span data-ttu-id="d147f-129">O objeto de zona a ser definido.</span><span class="sxs-lookup"><span data-stu-id="d147f-129">The zone object to set.</span></span>

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

### <span data-ttu-id="d147f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d147f-130">-ResourceGroupName</span></span>
<span data-ttu-id="d147f-131">Especifica o nome do grupo de recursos que contém a zona a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="d147f-131">Specifies the name of the resource group that contains the zone to be updated.</span></span>
<span data-ttu-id="d147f-132">Você também deve especificar o parâmetro *zonename* .</span><span class="sxs-lookup"><span data-stu-id="d147f-132">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="d147f-133">Você também pode especificar a zona DNS privada usando um objeto **dnsZone** , passado por meio do parâmetro pipeline ou *Zone* .</span><span class="sxs-lookup"><span data-stu-id="d147f-133">Alternatively, you can specify the private DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="d147f-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d147f-134">-ResourceId</span></span>
<span data-ttu-id="d147f-135">ResourceId de zona DNS particular.</span><span class="sxs-lookup"><span data-stu-id="d147f-135">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="d147f-136">-Marca</span><span class="sxs-lookup"><span data-stu-id="d147f-136">-Tag</span></span>
<span data-ttu-id="d147f-137">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="d147f-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="d147f-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d147f-138">-Confirm</span></span>
<span data-ttu-id="d147f-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d147f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d147f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d147f-140">-WhatIf</span></span>
<span data-ttu-id="d147f-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d147f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d147f-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d147f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d147f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d147f-143">CommonParameters</span></span>
<span data-ttu-id="d147f-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d147f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d147f-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d147f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d147f-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d147f-146">INPUTS</span></span>

### <span data-ttu-id="d147f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="d147f-147">System.String</span></span>

### <span data-ttu-id="d147f-148">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="d147f-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="d147f-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d147f-149">OUTPUTS</span></span>

### <span data-ttu-id="d147f-150">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="d147f-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="d147f-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d147f-151">NOTES</span></span>

## <span data-ttu-id="d147f-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d147f-152">RELATED LINKS</span></span>

[<span data-ttu-id="d147f-153">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="d147f-153">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="d147f-154">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="d147f-154">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="d147f-155">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="d147f-155">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
