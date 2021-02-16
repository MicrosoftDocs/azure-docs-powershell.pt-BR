---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 865ab4ab3cca9d921fc8c40e9c6ae5cd03eaf00a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113375"
---
# <span data-ttu-id="90d46-101">Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="90d46-101">Remove-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="90d46-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="90d46-102">SYNOPSIS</span></span>
<span data-ttu-id="90d46-103">Exclui um conjunto de registros de uma zona DNS particular.</span><span class="sxs-lookup"><span data-stu-id="90d46-103">Deletes a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="90d46-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90d46-104">SYNTAX</span></span>

### <span data-ttu-id="90d46-105">Campos (Padrão)</span><span class="sxs-lookup"><span data-stu-id="90d46-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90d46-106">Misto</span><span class="sxs-lookup"><span data-stu-id="90d46-106">Mixed</span></span>
```
Remove-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90d46-107">Objeto</span><span class="sxs-lookup"><span data-stu-id="90d46-107">Object</span></span>
```
Remove-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90d46-108">Resourceid</span><span class="sxs-lookup"><span data-stu-id="90d46-108">ResourceId</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90d46-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="90d46-109">DESCRIPTION</span></span>
<span data-ttu-id="90d46-110">O Remove-AzPrivateDnsRecordSet cmdlet exclui o conjunto de registros especificado da zona especificada.</span><span class="sxs-lookup"><span data-stu-id="90d46-110">The Remove-AzPrivateDnsRecordSet cmdlet deletes the specified record set from the specified zone.</span></span> <span data-ttu-id="90d46-111">Não é possível excluir registros SOA criados automaticamente no apex de zona particular.</span><span class="sxs-lookup"><span data-stu-id="90d46-111">You cannot delete SOA records that are automatically created at the private zone apex.</span></span> <span data-ttu-id="90d46-112">Você pode passar um objeto RecordSet para esse cmdlet usando o operador de pipeline ou como parâmetro ou como Um ResourceId.</span><span class="sxs-lookup"><span data-stu-id="90d46-112">You can pass a RecordSet object to this cmdlet by using the pipeline operator or as a parameter or as a ResourceId.</span></span> <span data-ttu-id="90d46-113">Para identificar um conjunto de registros por nome e tipo sem usar um objeto RecordSet, você deve passar a zona como um objeto PSPrivateDnsZone para esse cmdlet usando o operador de pipeline ou como parâmetro ou, alternativamente, você pode especificar os parâmetros ZoneName e ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="90d46-113">To identify a record set by name and type without using a RecordSet object, you must pass the zone as a PSPrivateDnsZone object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the ZoneName and ResourceGroupName parameters.</span></span> <span data-ttu-id="90d46-114">Você pode usar o parâmetro Confirmar e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="90d46-114">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="90d46-115">Ao especificar o conjunto de registros usando um objeto RecordSet, o conjunto de registros não será excluído se tiver sido alterado no DNS particular do Azure desde que o objeto Local RecordSet foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="90d46-115">When specifying the record set using a RecordSet object, the record set is not deleted if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="90d46-116">Isso fornece proteção para alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="90d46-116">This provides protection for concurrent changes.</span></span> <span data-ttu-id="90d46-117">Você pode suprimir isso usando o parâmetro Substituir, que exclui o conjunto de registros independentemente de alterações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="90d46-117">You can suppress this by using the Overwrite parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="90d46-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="90d46-118">EXAMPLES</span></span>

### <span data-ttu-id="90d46-119">Exemplo 1: Remover um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="90d46-119">Example 1: Remove a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="90d46-120">O primeiro comando obtém o conjunto de registros especificado e o armazena na variável $RecordSet dados. O segundo comando remove o conjunto de registros $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="90d46-120">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="90d46-121">Exemplo 2: remover um conjunto de registros e suprimir toda a confirmação</span><span class="sxs-lookup"><span data-stu-id="90d46-121">Example 2: Remove a record set and suppress all confirmation</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="90d46-122">O primeiro comando obtém o conjunto de registros especificado.</span><span class="sxs-lookup"><span data-stu-id="90d46-122">The first command gets the specified record set.</span></span> <span data-ttu-id="90d46-123">O segundo comando exclui o conjunto de registros, mesmo que tenha sido alterado enquanto isso.</span><span class="sxs-lookup"><span data-stu-id="90d46-123">The second command deletes the record set, even if it has changed in the meantime.</span></span> <span data-ttu-id="90d46-124">Os prompts de confirmação são suprimidos.</span><span class="sxs-lookup"><span data-stu-id="90d46-124">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="90d46-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90d46-125">PARAMETERS</span></span>

### <span data-ttu-id="90d46-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90d46-126">-DefaultProfile</span></span>
<span data-ttu-id="90d46-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="90d46-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90d46-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="90d46-128">-Name</span></span>
<span data-ttu-id="90d46-129">O nome dos registros no conjunto de registros (em relação ao nome da zona e sem um ponto de término).</span><span class="sxs-lookup"><span data-stu-id="90d46-129">The name of the records in the record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="90d46-130">-Substituir</span><span class="sxs-lookup"><span data-stu-id="90d46-130">-Overwrite</span></span>
<span data-ttu-id="90d46-131">Não use o campo ETag do parâmetro RecordSet para verificações otimistas de simulta.</span><span class="sxs-lookup"><span data-stu-id="90d46-131">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="90d46-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90d46-132">-PassThru</span></span>
<span data-ttu-id="90d46-133">Usado para passar o resultado (boolano) da operação, exclua a zona privada mais abaixo do pipeline.</span><span class="sxs-lookup"><span data-stu-id="90d46-133">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="90d46-134">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="90d46-134">-RecordSet</span></span>
<span data-ttu-id="90d46-135">O conjunto de registros no qual adicionar o registro.</span><span class="sxs-lookup"><span data-stu-id="90d46-135">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="90d46-136">-RecordType</span><span class="sxs-lookup"><span data-stu-id="90d46-136">-RecordType</span></span>
<span data-ttu-id="90d46-137">O tipo de registros DNS particulares no conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="90d46-137">The type of Private DNS records in the record set.</span></span>

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

### <span data-ttu-id="90d46-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90d46-138">-ResourceGroupName</span></span>
<span data-ttu-id="90d46-139">O grupo de recursos ao qual a zona pertence.</span><span class="sxs-lookup"><span data-stu-id="90d46-139">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="90d46-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90d46-140">-ResourceId</span></span>
<span data-ttu-id="90d46-141">Private DNS RecordSet ResourceID.</span><span class="sxs-lookup"><span data-stu-id="90d46-141">Private DNS RecordSet ResourceID.</span></span>

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

### <span data-ttu-id="90d46-142">-Zona</span><span class="sxs-lookup"><span data-stu-id="90d46-142">-Zone</span></span>
<span data-ttu-id="90d46-143">O objeto PrivateDnsZone representando a zona na qual criar o conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="90d46-143">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="90d46-144">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="90d46-144">-ZoneName</span></span>
<span data-ttu-id="90d46-145">A zona na qual o conjunto de registros existe (sem um ponto de término).</span><span class="sxs-lookup"><span data-stu-id="90d46-145">The zone in which the record set exists (without a terminating dot).</span></span>

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

### <span data-ttu-id="90d46-146">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="90d46-146">-Confirm</span></span>
<span data-ttu-id="90d46-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90d46-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90d46-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90d46-148">-WhatIf</span></span>
<span data-ttu-id="90d46-149">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="90d46-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90d46-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="90d46-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90d46-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90d46-151">CommonParameters</span></span>
<span data-ttu-id="90d46-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90d46-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90d46-153">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90d46-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90d46-154">Entradas</span><span class="sxs-lookup"><span data-stu-id="90d46-154">INPUTS</span></span>

### <span data-ttu-id="90d46-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="90d46-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="90d46-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="90d46-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

### <span data-ttu-id="90d46-157">System.String</span><span class="sxs-lookup"><span data-stu-id="90d46-157">System.String</span></span>

## <span data-ttu-id="90d46-158">Saídas</span><span class="sxs-lookup"><span data-stu-id="90d46-158">OUTPUTS</span></span>

### <span data-ttu-id="90d46-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="90d46-159">System.Boolean</span></span>

## <span data-ttu-id="90d46-160">Notas</span><span class="sxs-lookup"><span data-stu-id="90d46-160">NOTES</span></span>

## <span data-ttu-id="90d46-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90d46-161">RELATED LINKS</span></span>
