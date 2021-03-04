---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: 30a569c16a2f3da135f77061e8ff5373c45b2598
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887442"
---
# <span data-ttu-id="13289-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="13289-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="13289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13289-102">SYNOPSIS</span></span>
<span data-ttu-id="13289-103">Cria um novo pool de Arquivos do Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="13289-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="13289-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="13289-104">SYNTAX</span></span>

### <span data-ttu-id="13289-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="13289-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13289-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13289-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13289-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="13289-107">DESCRIPTION</span></span>
<span data-ttu-id="13289-108">O cmdlet **New-AzNetAppFilesPool** cria um pool ANF.</span><span class="sxs-lookup"><span data-stu-id="13289-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="13289-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13289-109">EXAMPLES</span></span>

### <span data-ttu-id="13289-110">Exemplo 1: Criar um pool ANF</span><span class="sxs-lookup"><span data-stu-id="13289-110">Example 1: Create an ANF pool</span></span>
```
PS C:\>New-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool" -l "westus2" -PoolSize 4398046511104 -ServiceLevel "Premium" -QosType "Auto"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
TotalThroughputMibps: 262.144
UtilizedThroughputMibps: 164.221
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="13289-111">Este comando cria o novo pool ANF "MyAnfPool" na conta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="13289-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="13289-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="13289-112">PARAMETERS</span></span>

### <span data-ttu-id="13289-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="13289-113">-AccountName</span></span>
<span data-ttu-id="13289-114">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="13289-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="13289-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="13289-115">-AccountObject</span></span>
<span data-ttu-id="13289-116">A conta do novo objeto pool</span><span class="sxs-lookup"><span data-stu-id="13289-116">The account for the new pool object</span></span>

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

### <span data-ttu-id="13289-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13289-117">-DefaultProfile</span></span>
<span data-ttu-id="13289-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="13289-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13289-119">-Location</span><span class="sxs-lookup"><span data-stu-id="13289-119">-Location</span></span>
<span data-ttu-id="13289-120">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="13289-120">The location of the resource</span></span>

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

### <span data-ttu-id="13289-121">-Name</span><span class="sxs-lookup"><span data-stu-id="13289-121">-Name</span></span>
<span data-ttu-id="13289-122">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="13289-122">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13289-123">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="13289-123">-PoolSize</span></span>
<span data-ttu-id="13289-124">O tamanho do pool ANF</span><span class="sxs-lookup"><span data-stu-id="13289-124">The size of the ANF pool</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13289-125">-QosType</span><span class="sxs-lookup"><span data-stu-id="13289-125">-QosType</span></span>
<span data-ttu-id="13289-126">O tipo qos do pool.</span><span class="sxs-lookup"><span data-stu-id="13289-126">The qos type of the pool.</span></span> <span data-ttu-id="13289-127">Os valores possíveis incluem: 'Auto', 'Manual'</span><span class="sxs-lookup"><span data-stu-id="13289-127">Possible values include: 'Auto', 'Manual'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Auto
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13289-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13289-128">-ResourceGroupName</span></span>
<span data-ttu-id="13289-129">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="13289-129">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="13289-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="13289-130">-ServiceLevel</span></span>
<span data-ttu-id="13289-131">O nível de serviço do pool ANF</span><span class="sxs-lookup"><span data-stu-id="13289-131">The service level of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13289-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="13289-132">-Tag</span></span>
<span data-ttu-id="13289-133">Uma hashtable que representa marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="13289-133">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="13289-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13289-134">-Confirm</span></span>
<span data-ttu-id="13289-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13289-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13289-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13289-136">-WhatIf</span></span>
<span data-ttu-id="13289-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="13289-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13289-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="13289-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13289-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13289-139">CommonParameters</span></span>
<span data-ttu-id="13289-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13289-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13289-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13289-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13289-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13289-142">INPUTS</span></span>

### <span data-ttu-id="13289-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="13289-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="13289-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="13289-144">OUTPUTS</span></span>

### <span data-ttu-id="13289-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="13289-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="13289-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="13289-146">NOTES</span></span>

## <span data-ttu-id="13289-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13289-147">RELATED LINKS</span></span>
