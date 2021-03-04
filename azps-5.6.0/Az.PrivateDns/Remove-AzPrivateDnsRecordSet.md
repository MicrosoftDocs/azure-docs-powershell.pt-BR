---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
ms.openlocfilehash: d54b2952c617782ec30193372b430785c0a8b79d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887083"
---
# <span data-ttu-id="2d883-101">Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2d883-101">Remove-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="2d883-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d883-102">SYNOPSIS</span></span>
<span data-ttu-id="2d883-103">Exclui um conjunto de registros de uma zona DNS privada.</span><span class="sxs-lookup"><span data-stu-id="2d883-103">Deletes a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="2d883-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2d883-104">SYNTAX</span></span>

### <span data-ttu-id="2d883-105">Campos (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2d883-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d883-106">Mixed</span><span class="sxs-lookup"><span data-stu-id="2d883-106">Mixed</span></span>
```
Remove-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d883-107">Objeto</span><span class="sxs-lookup"><span data-stu-id="2d883-107">Object</span></span>
```
Remove-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d883-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d883-108">ResourceId</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d883-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2d883-109">DESCRIPTION</span></span>
<span data-ttu-id="2d883-110">O Remove-AzPrivateDnsRecordSet cmdlet exclui o conjunto de registros especificado da zona especificada.</span><span class="sxs-lookup"><span data-stu-id="2d883-110">The Remove-AzPrivateDnsRecordSet cmdlet deletes the specified record set from the specified zone.</span></span> <span data-ttu-id="2d883-111">Não é possível excluir registros SOA que são criados automaticamente no véreo de zona privada.</span><span class="sxs-lookup"><span data-stu-id="2d883-111">You cannot delete SOA records that are automatically created at the private zone apex.</span></span> <span data-ttu-id="2d883-112">Você pode passar um objeto RecordSet para esse cmdlet usando o operador de pipeline ou como parâmetro ou como ResourceId.</span><span class="sxs-lookup"><span data-stu-id="2d883-112">You can pass a RecordSet object to this cmdlet by using the pipeline operator or as a parameter or as a ResourceId.</span></span> <span data-ttu-id="2d883-113">Para identificar um registro definido por nome e tipo sem usar um objeto RecordSet, você deve passar a zona como um objeto PSPrivateDnsZone para esse cmdlet usando o operador de pipeline ou como parâmetro ou, como alternativa, você pode especificar os parâmetros ZoneName e ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="2d883-113">To identify a record set by name and type without using a RecordSet object, you must pass the zone as a PSPrivateDnsZone object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the ZoneName and ResourceGroupName parameters.</span></span> <span data-ttu-id="2d883-114">Você pode usar o parâmetro Confirm e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="2d883-114">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="2d883-115">Ao especificar o conjunto de registros usando um objeto RecordSet, o conjunto de registros não será excluído se tiver sido alterado no DNS privado do Azure desde que o objeto RecordSet local foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="2d883-115">When specifying the record set using a RecordSet object, the record set is not deleted if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="2d883-116">Isso fornece proteção para alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="2d883-116">This provides protection for concurrent changes.</span></span> <span data-ttu-id="2d883-117">Você pode suprimir isso usando o parâmetro Overwrite, que exclui o conjunto de registros independentemente de alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="2d883-117">You can suppress this by using the Overwrite parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="2d883-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d883-118">EXAMPLES</span></span>

### <span data-ttu-id="2d883-119">Exemplo 1: Remover um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="2d883-119">Example 1: Remove a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="2d883-120">O primeiro comando obtém o conjunto de registros especificado e o armazena na variável $RecordSet. O segundo comando remove o conjunto de registros em $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="2d883-120">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="2d883-121">Exemplo 2: remover um conjunto de registros e suprimir toda a confirmação</span><span class="sxs-lookup"><span data-stu-id="2d883-121">Example 2: Remove a record set and suppress all confirmation</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="2d883-122">O primeiro comando obtém o conjunto de registros especificado.</span><span class="sxs-lookup"><span data-stu-id="2d883-122">The first command gets the specified record set.</span></span> <span data-ttu-id="2d883-123">O segundo comando exclui o conjunto de registros, mesmo que tenha sido alterado enquanto isso.</span><span class="sxs-lookup"><span data-stu-id="2d883-123">The second command deletes the record set, even if it has changed in the meantime.</span></span> <span data-ttu-id="2d883-124">Os prompts de confirmação são suprimidos.</span><span class="sxs-lookup"><span data-stu-id="2d883-124">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="2d883-125">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2d883-125">PARAMETERS</span></span>

### <span data-ttu-id="2d883-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d883-126">-DefaultProfile</span></span>
<span data-ttu-id="2d883-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d883-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d883-128">-Name</span><span class="sxs-lookup"><span data-stu-id="2d883-128">-Name</span></span>
<span data-ttu-id="2d883-129">O nome dos registros no conjunto de registros (em relação ao nome da zona e sem um ponto final).</span><span class="sxs-lookup"><span data-stu-id="2d883-129">The name of the records in the record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="2d883-130">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="2d883-130">-Overwrite</span></span>
<span data-ttu-id="2d883-131">Não use o campo ETag do parâmetro RecordSet para verificações otimistas de simulta.</span><span class="sxs-lookup"><span data-stu-id="2d883-131">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="2d883-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d883-132">-PassThru</span></span>
<span data-ttu-id="2d883-133">Usado para passar o resultado (booleano) da operação excluir zona privada mais abaixo do pipeline.</span><span class="sxs-lookup"><span data-stu-id="2d883-133">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="2d883-134">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="2d883-134">-RecordSet</span></span>
<span data-ttu-id="2d883-135">O conjunto de registros no qual adicionar o registro.</span><span class="sxs-lookup"><span data-stu-id="2d883-135">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="2d883-136">-RecordType</span><span class="sxs-lookup"><span data-stu-id="2d883-136">-RecordType</span></span>
<span data-ttu-id="2d883-137">O tipo de registros DNS privados no conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="2d883-137">The type of Private DNS records in the record set.</span></span>

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

### <span data-ttu-id="2d883-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d883-138">-ResourceGroupName</span></span>
<span data-ttu-id="2d883-139">O grupo de recursos ao qual a zona pertence.</span><span class="sxs-lookup"><span data-stu-id="2d883-139">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="2d883-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d883-140">-ResourceId</span></span>
<span data-ttu-id="2d883-141">Private DNS RecordSet ResourceID.</span><span class="sxs-lookup"><span data-stu-id="2d883-141">Private DNS RecordSet ResourceID.</span></span>

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

### <span data-ttu-id="2d883-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="2d883-142">-Zone</span></span>
<span data-ttu-id="2d883-143">O objeto PrivateDnsZone que representa a zona na qual o conjunto de registros será criado.</span><span class="sxs-lookup"><span data-stu-id="2d883-143">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="2d883-144">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="2d883-144">-ZoneName</span></span>
<span data-ttu-id="2d883-145">A zona na qual o conjunto de registros existe (sem um ponto final).</span><span class="sxs-lookup"><span data-stu-id="2d883-145">The zone in which the record set exists (without a terminating dot).</span></span>

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

### <span data-ttu-id="2d883-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d883-146">-Confirm</span></span>
<span data-ttu-id="2d883-147">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d883-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d883-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d883-148">-WhatIf</span></span>
<span data-ttu-id="2d883-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2d883-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d883-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2d883-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d883-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d883-151">CommonParameters</span></span>
<span data-ttu-id="2d883-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d883-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d883-153">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d883-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d883-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d883-154">INPUTS</span></span>

### <span data-ttu-id="2d883-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="2d883-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="2d883-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2d883-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

### <span data-ttu-id="2d883-157">System.String</span><span class="sxs-lookup"><span data-stu-id="2d883-157">System.String</span></span>

## <span data-ttu-id="2d883-158">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2d883-158">OUTPUTS</span></span>

### <span data-ttu-id="2d883-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2d883-159">System.Boolean</span></span>

## <span data-ttu-id="2d883-160">NOTES</span><span class="sxs-lookup"><span data-stu-id="2d883-160">NOTES</span></span>

## <span data-ttu-id="2d883-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d883-161">RELATED LINKS</span></span>
