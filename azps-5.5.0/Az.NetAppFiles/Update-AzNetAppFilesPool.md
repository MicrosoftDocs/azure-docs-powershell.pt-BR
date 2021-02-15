---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: 8f26023224e0f6d4a035f4671db7b45be57a3177
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111706"
---
# <span data-ttu-id="7373c-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="7373c-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="7373c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7373c-102">SYNOPSIS</span></span>
<span data-ttu-id="7373c-103">Atualiza um pool de Arquivos Azure NetApp (ANF) de acordo com os modificadores opcionais fornecidos.</span><span class="sxs-lookup"><span data-stu-id="7373c-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="7373c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7373c-104">SYNTAX</span></span>

### <span data-ttu-id="7373c-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7373c-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7373c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7373c-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7373c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7373c-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7373c-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7373c-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7373c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="7373c-109">DESCRIPTION</span></span>
<span data-ttu-id="7373c-110">O **cmdlet Update-AzNetAppFilesPool** modifica um pool ANF.</span><span class="sxs-lookup"><span data-stu-id="7373c-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="7373c-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7373c-111">EXAMPLES</span></span>

### <span data-ttu-id="7373c-112">Exemplo 1: Modificar um pool de ANF</span><span class="sxs-lookup"><span data-stu-id="7373c-112">Example 1: Modify an ANF pool</span></span>
```
PS C:\>Update-AzNetAppFilesPool -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolSize 4398046511104 -QosType "Auto"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
Size              : 4398046511104
ServiceLevel      : Standard
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="7373c-113">Esse comando altera o pool de ANF "MyAnfPool" para ter o tamanho determinado e o QosType.</span><span class="sxs-lookup"><span data-stu-id="7373c-113">This command changes the ANF pool "MyAnfPool" to have the given size and QosType.</span></span>

## <span data-ttu-id="7373c-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7373c-114">PARAMETERS</span></span>

### <span data-ttu-id="7373c-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="7373c-115">-AccountName</span></span>
<span data-ttu-id="7373c-116">O nome da conta da ANF</span><span class="sxs-lookup"><span data-stu-id="7373c-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7373c-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="7373c-117">-AccountObject</span></span>
<span data-ttu-id="7373c-118">O objeto da conta que contém o pool de atualizações</span><span class="sxs-lookup"><span data-stu-id="7373c-118">The account object containing the pool to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7373c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7373c-119">-DefaultProfile</span></span>
<span data-ttu-id="7373c-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7373c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7373c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7373c-121">-InputObject</span></span>
<span data-ttu-id="7373c-122">O objeto de pool a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="7373c-122">The pool object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7373c-123">-Local</span><span class="sxs-lookup"><span data-stu-id="7373c-123">-Location</span></span>
<span data-ttu-id="7373c-124">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="7373c-124">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7373c-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="7373c-125">-Name</span></span>
<span data-ttu-id="7373c-126">O nome do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="7373c-126">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7373c-127">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="7373c-127">-PoolSize</span></span>
<span data-ttu-id="7373c-128">O tamanho do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="7373c-128">The size of the ANF pool</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7373c-129">-QosType</span><span class="sxs-lookup"><span data-stu-id="7373c-129">-QosType</span></span>
<span data-ttu-id="7373c-130">O tipo de qos do pool.</span><span class="sxs-lookup"><span data-stu-id="7373c-130">The qos type of the pool.</span></span> <span data-ttu-id="7373c-131">Os valores possíveis incluem: 'Automático', 'Manual'</span><span class="sxs-lookup"><span data-stu-id="7373c-131">Possible values include: 'Auto', 'Manual'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7373c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7373c-132">-ResourceGroupName</span></span>
<span data-ttu-id="7373c-133">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="7373c-133">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7373c-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7373c-134">-ResourceId</span></span>
<span data-ttu-id="7373c-135">A ID do recurso do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="7373c-135">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7373c-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="7373c-136">-Tag</span></span>
<span data-ttu-id="7373c-137">Uma tabela hash que representa marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="7373c-137">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7373c-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7373c-138">-Confirm</span></span>
<span data-ttu-id="7373c-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7373c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7373c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7373c-140">-WhatIf</span></span>
<span data-ttu-id="7373c-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7373c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7373c-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7373c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7373c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7373c-143">CommonParameters</span></span>
<span data-ttu-id="7373c-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7373c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7373c-145">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7373c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7373c-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="7373c-146">INPUTS</span></span>

### <span data-ttu-id="7373c-147">System.String</span><span class="sxs-lookup"><span data-stu-id="7373c-147">System.String</span></span>

### <span data-ttu-id="7373c-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="7373c-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="7373c-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="7373c-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="7373c-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="7373c-150">OUTPUTS</span></span>

### <span data-ttu-id="7373c-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="7373c-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="7373c-152">Notas</span><span class="sxs-lookup"><span data-stu-id="7373c-152">NOTES</span></span>

## <span data-ttu-id="7373c-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7373c-153">RELATED LINKS</span></span>
