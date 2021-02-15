---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: 06b8a8bd7027b95d7f51e186b0184707ffd296a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111470"
---
# <span data-ttu-id="451a1-101">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="451a1-101">Set-AzPrivateDnsZone</span></span>

## <span data-ttu-id="451a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="451a1-102">SYNOPSIS</span></span>
<span data-ttu-id="451a1-103">Atualiza uma zona DNS particular de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="451a1-103">Updates a Private DNS zone from a resource group.</span></span>

## <span data-ttu-id="451a1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="451a1-104">SYNTAX</span></span>

### <span data-ttu-id="451a1-105">Campos (Padrão)</span><span class="sxs-lookup"><span data-stu-id="451a1-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="451a1-106">Resourceid</span><span class="sxs-lookup"><span data-stu-id="451a1-106">ResourceId</span></span>
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="451a1-107">Objeto</span><span class="sxs-lookup"><span data-stu-id="451a1-107">Object</span></span>
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="451a1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="451a1-108">DESCRIPTION</span></span>
<span data-ttu-id="451a1-109">O cmdlet **Set-AzPrivateDnsZone** atualiza permanentemente uma zona DNS (Sistema de Nomes de Domínio) particular de um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="451a1-109">The **Set-AzPrivateDnsZone** cmdlet permanently updates a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="451a1-110">Você pode passar um objeto **PrivateDnsZone** usando o parâmetro *PrivateZone* ou usando o operador de pipeline ou, como alternativa, pode especificar os parâmetros *Nome* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="451a1-110">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="451a1-111">Você pode usar o parâmetro Confirmar e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="451a1-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="451a1-112">Ao especificar a zona usando um objeto **PrivateDnsZone** (passado pelo parâmetro pipeline ou Zona), a zona não será atualizada se tiver sido alterada no DNS do Azure, uma vez que o objeto **local PrivateDnsZone** foi recuperado (somente operações diretamente na contagem de recursos de zona DNS como alterações, as operações em conjuntos de registros dentro da zona não o fazem). </span><span class="sxs-lookup"><span data-stu-id="451a1-112">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="451a1-113">Isso fornece proteção para alterações de zona simultâneas.</span><span class="sxs-lookup"><span data-stu-id="451a1-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="451a1-114">Isso pode ser suprimido usando o parâmetro *Substituir,* que atualiza a zona independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="451a1-114">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="451a1-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="451a1-115">EXAMPLES</span></span>

### <span data-ttu-id="451a1-116">Exemplo 1: atualiza uma zona privada</span><span class="sxs-lookup"><span data-stu-id="451a1-116">Example 1: Updates a private zone</span></span>
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

## <span data-ttu-id="451a1-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="451a1-117">PARAMETERS</span></span>

### <span data-ttu-id="451a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="451a1-118">-DefaultProfile</span></span>
<span data-ttu-id="451a1-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="451a1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="451a1-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="451a1-120">-Name</span></span>
<span data-ttu-id="451a1-121">Especifica o nome da zona DNS particular que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="451a1-121">Specifies the name of the Private DNS zone that this cmdlet updates.</span></span>
<span data-ttu-id="451a1-122">Você também deve especificar o parâmetro *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="451a1-122">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="451a1-123">Como alternativa, você pode especificar a zona DNS privada usando o *parâmetro* Zona.</span><span class="sxs-lookup"><span data-stu-id="451a1-123">Alternatively, you can specify the private DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="451a1-124">-Substituir</span><span class="sxs-lookup"><span data-stu-id="451a1-124">-Overwrite</span></span>
<span data-ttu-id="451a1-125">Ao especificar a zona usando um objeto **PrivateDnsZone** (passado pelo parâmetro pipeline ou Zona), a zona não será atualizada se tiver sido alterada no DNS do Azure, uma vez que o objeto **DnsZone** local foi recuperado (somente as operações diretamente na contagem de recursos de zona DNS como alterações, as operações nos conjuntos de registros dentro da zona não o fazem). </span><span class="sxs-lookup"><span data-stu-id="451a1-125">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="451a1-126">Isso fornece proteção para alterações de zona simultâneas.</span><span class="sxs-lookup"><span data-stu-id="451a1-126">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="451a1-127">Isso pode ser suprimido usando o parâmetro *Substituir,* que atualiza a zona independentemente das alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="451a1-127">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="451a1-128">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="451a1-128">-PrivateZone</span></span>
<span data-ttu-id="451a1-129">O objeto de zona a ser definido.</span><span class="sxs-lookup"><span data-stu-id="451a1-129">The zone object to set.</span></span>

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

### <span data-ttu-id="451a1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="451a1-130">-ResourceGroupName</span></span>
<span data-ttu-id="451a1-131">Especifica o nome do grupo de recursos que contém a zona a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="451a1-131">Specifies the name of the resource group that contains the zone to be updated.</span></span>
<span data-ttu-id="451a1-132">Você também deve especificar o parâmetro *ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="451a1-132">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="451a1-133">Como alternativa, você pode especificar a zona DNS privada usando um objeto **DnsZone,** passado pelo pipeline ou pelo parâmetro *Zona.*</span><span class="sxs-lookup"><span data-stu-id="451a1-133">Alternatively, you can specify the private DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="451a1-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="451a1-134">-ResourceId</span></span>
<span data-ttu-id="451a1-135">ID de Recurso de Zona DNS Particular.</span><span class="sxs-lookup"><span data-stu-id="451a1-135">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="451a1-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="451a1-136">-Tag</span></span>
<span data-ttu-id="451a1-137">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="451a1-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="451a1-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="451a1-138">-Confirm</span></span>
<span data-ttu-id="451a1-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="451a1-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="451a1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="451a1-140">-WhatIf</span></span>
<span data-ttu-id="451a1-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="451a1-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="451a1-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="451a1-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="451a1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="451a1-143">CommonParameters</span></span>
<span data-ttu-id="451a1-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="451a1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="451a1-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="451a1-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="451a1-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="451a1-146">INPUTS</span></span>

### <span data-ttu-id="451a1-147">System.String</span><span class="sxs-lookup"><span data-stu-id="451a1-147">System.String</span></span>

### <span data-ttu-id="451a1-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="451a1-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="451a1-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="451a1-149">OUTPUTS</span></span>

### <span data-ttu-id="451a1-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="451a1-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="451a1-151">Notas</span><span class="sxs-lookup"><span data-stu-id="451a1-151">NOTES</span></span>

## <span data-ttu-id="451a1-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="451a1-152">RELATED LINKS</span></span>

[<span data-ttu-id="451a1-153">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="451a1-153">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="451a1-154">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="451a1-154">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="451a1-155">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="451a1-155">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
