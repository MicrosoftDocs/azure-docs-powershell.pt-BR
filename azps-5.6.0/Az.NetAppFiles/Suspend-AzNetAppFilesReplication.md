---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: 198ec8c67939c3ae01a52f2a9b06982ce8ee8d93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887407"
---
# <span data-ttu-id="23b31-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="23b31-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="23b31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23b31-102">SYNOPSIS</span></span>
<span data-ttu-id="23b31-103">Suspender/quebrar a conexão de replicação no volume de destino</span><span class="sxs-lookup"><span data-stu-id="23b31-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="23b31-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="23b31-104">SYNTAX</span></span>

### <span data-ttu-id="23b31-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="23b31-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-ForceBreak] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23b31-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23b31-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23b31-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23b31-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23b31-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="23b31-108">DESCRIPTION</span></span>
<span data-ttu-id="23b31-109">Suspender/quebrar a conexão de replicação no volume de destino</span><span class="sxs-lookup"><span data-stu-id="23b31-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="23b31-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23b31-110">EXAMPLES</span></span>

### <span data-ttu-id="23b31-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="23b31-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="23b31-112">Este comando suspende a conexão de Replicação ANF no volume "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="23b31-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="23b31-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="23b31-113">PARAMETERS</span></span>

### <span data-ttu-id="23b31-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="23b31-114">-AccountName</span></span>
<span data-ttu-id="23b31-115">O nome da conta ANF do volume de replicação</span><span class="sxs-lookup"><span data-stu-id="23b31-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="23b31-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23b31-116">-DefaultProfile</span></span>
<span data-ttu-id="23b31-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23b31-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23b31-118">-ForceBreak</span><span class="sxs-lookup"><span data-stu-id="23b31-118">-ForceBreak</span></span>
<span data-ttu-id="23b31-119">Se a replicação estiver em transferência de status e você quiser forçar a quebra da replicação, de definida como true</span><span class="sxs-lookup"><span data-stu-id="23b31-119">If replication is in status transferring and you want to force break the replication, set to true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b31-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23b31-120">-InputObject</span></span>
<span data-ttu-id="23b31-121">O objeto de volume de destino da ANF com a replicação para quebrar</span><span class="sxs-lookup"><span data-stu-id="23b31-121">The ANF destination volume object with the replication to break</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23b31-122">-Name</span><span class="sxs-lookup"><span data-stu-id="23b31-122">-Name</span></span>
<span data-ttu-id="23b31-123">O nome do volume de destino de replicação ANF</span><span class="sxs-lookup"><span data-stu-id="23b31-123">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b31-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23b31-124">-PassThru</span></span>
<span data-ttu-id="23b31-125">Retornar se a quebra da replicação de volume especificada foi executada</span><span class="sxs-lookup"><span data-stu-id="23b31-125">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="23b31-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="23b31-126">-PoolName</span></span>
<span data-ttu-id="23b31-127">O nome do pool ANF do volume de replicação</span><span class="sxs-lookup"><span data-stu-id="23b31-127">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="23b31-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23b31-128">-ResourceGroupName</span></span>
<span data-ttu-id="23b31-129">O grupo de recursos do volume de destino de replicação ANF</span><span class="sxs-lookup"><span data-stu-id="23b31-129">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="23b31-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23b31-130">-ResourceId</span></span>
<span data-ttu-id="23b31-131">A id de recurso do volume de destino de replicação ANF</span><span class="sxs-lookup"><span data-stu-id="23b31-131">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="23b31-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23b31-132">-Confirm</span></span>
<span data-ttu-id="23b31-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23b31-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23b31-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23b31-134">-WhatIf</span></span>
<span data-ttu-id="23b31-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="23b31-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23b31-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23b31-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23b31-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23b31-137">CommonParameters</span></span>
<span data-ttu-id="23b31-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23b31-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23b31-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23b31-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23b31-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23b31-140">INPUTS</span></span>

### <span data-ttu-id="23b31-141">System.String</span><span class="sxs-lookup"><span data-stu-id="23b31-141">System.String</span></span>

### <span data-ttu-id="23b31-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="23b31-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="23b31-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="23b31-143">OUTPUTS</span></span>

### <span data-ttu-id="23b31-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="23b31-144">System.Boolean</span></span>

## <span data-ttu-id="23b31-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="23b31-145">NOTES</span></span>

## <span data-ttu-id="23b31-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23b31-146">RELATED LINKS</span></span>
