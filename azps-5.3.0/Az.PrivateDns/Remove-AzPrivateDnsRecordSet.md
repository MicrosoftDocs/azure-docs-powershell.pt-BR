---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 865ab4ab3cca9d921fc8c40e9c6ae5cd03eaf00a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427483"
---
# <span data-ttu-id="28b38-101">Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="28b38-101">Remove-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="28b38-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28b38-102">SYNOPSIS</span></span>
<span data-ttu-id="28b38-103">Exclui um conjunto de registros de uma zona DNS privada.</span><span class="sxs-lookup"><span data-stu-id="28b38-103">Deletes a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="28b38-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28b38-104">SYNTAX</span></span>

### <span data-ttu-id="28b38-105">Campos (padrão)</span><span class="sxs-lookup"><span data-stu-id="28b38-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28b38-106">Misto</span><span class="sxs-lookup"><span data-stu-id="28b38-106">Mixed</span></span>
```
Remove-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28b38-107">Objeto</span><span class="sxs-lookup"><span data-stu-id="28b38-107">Object</span></span>
```
Remove-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28b38-108">Identificação</span><span class="sxs-lookup"><span data-stu-id="28b38-108">ResourceId</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28b38-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="28b38-109">DESCRIPTION</span></span>
<span data-ttu-id="28b38-110">O cmdlet Remove-AzPrivateDnsRecordSet exclui o conjunto de registros especificado da zona especificada.</span><span class="sxs-lookup"><span data-stu-id="28b38-110">The Remove-AzPrivateDnsRecordSet cmdlet deletes the specified record set from the specified zone.</span></span> <span data-ttu-id="28b38-111">Não é possível excluir registros SOA criados automaticamente na zona privada Apex.</span><span class="sxs-lookup"><span data-stu-id="28b38-111">You cannot delete SOA records that are automatically created at the private zone apex.</span></span> <span data-ttu-id="28b38-112">Você pode passar um objeto RecordSet para esse cmdlet usando o operador pipeline ou como um parâmetro ou como um ResourceId.</span><span class="sxs-lookup"><span data-stu-id="28b38-112">You can pass a RecordSet object to this cmdlet by using the pipeline operator or as a parameter or as a ResourceId.</span></span> <span data-ttu-id="28b38-113">Para identificar um registro definido por nome e tipo sem usar um objeto RecordSet, você deve passar a zona como um objeto PSPrivateDnsZone para esse cmdlet usando o operador pipeline ou como um parâmetro ou, como alternativa, você pode especificar os parâmetros zonename e ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="28b38-113">To identify a record set by name and type without using a RecordSet object, you must pass the zone as a PSPrivateDnsZone object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the ZoneName and ResourceGroupName parameters.</span></span> <span data-ttu-id="28b38-114">Você pode usar o parâmetro Confirm e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="28b38-114">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="28b38-115">Ao especificar o conjunto de registros usando um objeto RecordSet, o conjunto de registros não será excluído se tiver sido alterado no DNS privado do Azure, pois o objeto RecordSet local foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="28b38-115">When specifying the record set using a RecordSet object, the record set is not deleted if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="28b38-116">Isso fornece proteção para alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="28b38-116">This provides protection for concurrent changes.</span></span> <span data-ttu-id="28b38-117">Você pode suprimir isso usando o parâmetro overwrite, que exclui o conjunto de registros independentemente de alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="28b38-117">You can suppress this by using the Overwrite parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="28b38-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28b38-118">EXAMPLES</span></span>

### <span data-ttu-id="28b38-119">Exemplo 1: remover um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="28b38-119">Example 1: Remove a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="28b38-120">O primeiro comando obtém o conjunto de registros especificado e, em seguida, armazena-o na variável $RecordSet. O segundo comando Remove o conjunto de registros no $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="28b38-120">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="28b38-121">Exemplo 2: remover um conjunto de registros e suprimir todas as confirmações</span><span class="sxs-lookup"><span data-stu-id="28b38-121">Example 2: Remove a record set and suppress all confirmation</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="28b38-122">O primeiro comando obtém o conjunto de registros especificado.</span><span class="sxs-lookup"><span data-stu-id="28b38-122">The first command gets the specified record set.</span></span> <span data-ttu-id="28b38-123">O segundo comando exclui o conjunto de registros, mesmo que ele tenha sido alterado enquanto isso.</span><span class="sxs-lookup"><span data-stu-id="28b38-123">The second command deletes the record set, even if it has changed in the meantime.</span></span> <span data-ttu-id="28b38-124">As solicitações de confirmação são suprimidas.</span><span class="sxs-lookup"><span data-stu-id="28b38-124">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="28b38-125">OS</span><span class="sxs-lookup"><span data-stu-id="28b38-125">PARAMETERS</span></span>

### <span data-ttu-id="28b38-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28b38-126">-DefaultProfile</span></span>
<span data-ttu-id="28b38-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28b38-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28b38-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="28b38-128">-Name</span></span>
<span data-ttu-id="28b38-129">O nome dos registros no conjunto de registros (relativo ao nome da zona e sem um ponto final).</span><span class="sxs-lookup"><span data-stu-id="28b38-129">The name of the records in the record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b38-130">-Substituir</span><span class="sxs-lookup"><span data-stu-id="28b38-130">-Overwrite</span></span>
<span data-ttu-id="28b38-131">Não use o campo ETag do parâmetro RecordSet para verificações de simultaneidade otimistas.</span><span class="sxs-lookup"><span data-stu-id="28b38-131">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="28b38-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28b38-132">-PassThru</span></span>
<span data-ttu-id="28b38-133">Usado para passar o resultado (booliano) da operação excluir zona privada mais adiante no pipeline.</span><span class="sxs-lookup"><span data-stu-id="28b38-133">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="28b38-134">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="28b38-134">-RecordSet</span></span>
<span data-ttu-id="28b38-135">O conjunto de registros no qual adicionar o registro.</span><span class="sxs-lookup"><span data-stu-id="28b38-135">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28b38-136">-RecordType</span><span class="sxs-lookup"><span data-stu-id="28b38-136">-RecordType</span></span>
<span data-ttu-id="28b38-137">O tipo de registro DNS privado no conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="28b38-137">The type of Private DNS records in the record set.</span></span>

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b38-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28b38-138">-ResourceGroupName</span></span>
<span data-ttu-id="28b38-139">O grupo de recursos ao qual a zona pertence.</span><span class="sxs-lookup"><span data-stu-id="28b38-139">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="28b38-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28b38-140">-ResourceId</span></span>
<span data-ttu-id="28b38-141">ResourceSet do conjunto de registros DNS privado.</span><span class="sxs-lookup"><span data-stu-id="28b38-141">Private DNS RecordSet ResourceID.</span></span>

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

### <span data-ttu-id="28b38-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="28b38-142">-Zone</span></span>
<span data-ttu-id="28b38-143">O objeto PrivateDnsZone que representa a zona na qual criar o conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="28b38-143">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28b38-144">-Zonename</span><span class="sxs-lookup"><span data-stu-id="28b38-144">-ZoneName</span></span>
<span data-ttu-id="28b38-145">A zona na qual o conjunto de registros existe (sem um ponto de terminação).</span><span class="sxs-lookup"><span data-stu-id="28b38-145">The zone in which the record set exists (without a terminating dot).</span></span>

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

### <span data-ttu-id="28b38-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="28b38-146">-Confirm</span></span>
<span data-ttu-id="28b38-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28b38-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28b38-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28b38-148">-WhatIf</span></span>
<span data-ttu-id="28b38-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="28b38-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28b38-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="28b38-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28b38-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28b38-151">CommonParameters</span></span>
<span data-ttu-id="28b38-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28b38-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28b38-153">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28b38-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28b38-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="28b38-154">INPUTS</span></span>

### <span data-ttu-id="28b38-155">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="28b38-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="28b38-156">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="28b38-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

### <span data-ttu-id="28b38-157">System. String</span><span class="sxs-lookup"><span data-stu-id="28b38-157">System.String</span></span>

## <span data-ttu-id="28b38-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="28b38-158">OUTPUTS</span></span>

### <span data-ttu-id="28b38-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="28b38-159">System.Boolean</span></span>

## <span data-ttu-id="28b38-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="28b38-160">NOTES</span></span>

## <span data-ttu-id="28b38-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28b38-161">RELATED LINKS</span></span>
