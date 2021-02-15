---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: ab4d79b4770f438b233e5bfcc740e79364955ea6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112922"
---
# <span data-ttu-id="bd7b1-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="bd7b1-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="bd7b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bd7b1-102">SYNOPSIS</span></span>
<span data-ttu-id="bd7b1-103">Suspender/quebrar a conexão de replicação no volume de destino</span><span class="sxs-lookup"><span data-stu-id="bd7b1-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="bd7b1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd7b1-104">SYNTAX</span></span>

### <span data-ttu-id="bd7b1-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bd7b1-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-ForceBreak] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd7b1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd7b1-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd7b1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd7b1-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd7b1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="bd7b1-108">DESCRIPTION</span></span>
<span data-ttu-id="bd7b1-109">Suspender/quebrar a conexão de replicação no volume de destino</span><span class="sxs-lookup"><span data-stu-id="bd7b1-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="bd7b1-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bd7b1-110">EXAMPLES</span></span>

### <span data-ttu-id="bd7b1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bd7b1-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="bd7b1-112">Este comando suspende a conexão de Replicação ANF no volume "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="bd7b1-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="bd7b1-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd7b1-113">PARAMETERS</span></span>

### <span data-ttu-id="bd7b1-114">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="bd7b1-114">-AccountName</span></span>
<span data-ttu-id="bd7b1-115">O nome da conta ANF do volume de replicação</span><span class="sxs-lookup"><span data-stu-id="bd7b1-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="bd7b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd7b1-116">-DefaultProfile</span></span>
<span data-ttu-id="bd7b1-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bd7b1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd7b1-118">-ForceBreak</span><span class="sxs-lookup"><span data-stu-id="bd7b1-118">-ForceBreak</span></span>
<span data-ttu-id="bd7b1-119">Se a replicação estiver em transferência de status e você quiser forçar a quebra da replicação, definida como verdadeira</span><span class="sxs-lookup"><span data-stu-id="bd7b1-119">If replication is in status transferring and you want to force break the replication, set to true</span></span>

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

### <span data-ttu-id="bd7b1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd7b1-120">-InputObject</span></span>
<span data-ttu-id="bd7b1-121">O objeto de volume de destino da ANF com a replicação para quebra</span><span class="sxs-lookup"><span data-stu-id="bd7b1-121">The ANF destination volume object with the replication to break</span></span>

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

### <span data-ttu-id="bd7b1-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="bd7b1-122">-Name</span></span>
<span data-ttu-id="bd7b1-123">O nome do volume de destino de replicação da ANF</span><span class="sxs-lookup"><span data-stu-id="bd7b1-123">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="bd7b1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd7b1-124">-PassThru</span></span>
<span data-ttu-id="bd7b1-125">Retornar se a quebra da replicação de volume especificada foi executada</span><span class="sxs-lookup"><span data-stu-id="bd7b1-125">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="bd7b1-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="bd7b1-126">-PoolName</span></span>
<span data-ttu-id="bd7b1-127">O nome do pool de ANF do volume de replicação</span><span class="sxs-lookup"><span data-stu-id="bd7b1-127">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="bd7b1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd7b1-128">-ResourceGroupName</span></span>
<span data-ttu-id="bd7b1-129">O grupo de recursos do volume de destino de replicação da ANF</span><span class="sxs-lookup"><span data-stu-id="bd7b1-129">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="bd7b1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd7b1-130">-ResourceId</span></span>
<span data-ttu-id="bd7b1-131">A ID do recurso do volume de destino de replicação da ANF</span><span class="sxs-lookup"><span data-stu-id="bd7b1-131">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="bd7b1-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bd7b1-132">-Confirm</span></span>
<span data-ttu-id="bd7b1-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd7b1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd7b1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd7b1-134">-WhatIf</span></span>
<span data-ttu-id="bd7b1-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bd7b1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd7b1-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bd7b1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd7b1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd7b1-137">CommonParameters</span></span>
<span data-ttu-id="bd7b1-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd7b1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd7b1-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd7b1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd7b1-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="bd7b1-140">INPUTS</span></span>

### <span data-ttu-id="bd7b1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="bd7b1-141">System.String</span></span>

### <span data-ttu-id="bd7b1-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="bd7b1-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="bd7b1-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="bd7b1-143">OUTPUTS</span></span>

### <span data-ttu-id="bd7b1-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bd7b1-144">System.Boolean</span></span>

## <span data-ttu-id="bd7b1-145">Notas</span><span class="sxs-lookup"><span data-stu-id="bd7b1-145">NOTES</span></span>

## <span data-ttu-id="bd7b1-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd7b1-146">RELATED LINKS</span></span>
