---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: ab4d79b4770f438b233e5bfcc740e79364955ea6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259610"
---
# <span data-ttu-id="afaf6-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="afaf6-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="afaf6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="afaf6-102">SYNOPSIS</span></span>
<span data-ttu-id="afaf6-103">Suspender/interromper a conexão de replicação no volume de destino</span><span class="sxs-lookup"><span data-stu-id="afaf6-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="afaf6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afaf6-104">SYNTAX</span></span>

### <span data-ttu-id="afaf6-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="afaf6-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-ForceBreak] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afaf6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="afaf6-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afaf6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="afaf6-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afaf6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="afaf6-108">DESCRIPTION</span></span>
<span data-ttu-id="afaf6-109">Suspender/interromper a conexão de replicação no volume de destino</span><span class="sxs-lookup"><span data-stu-id="afaf6-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="afaf6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="afaf6-110">EXAMPLES</span></span>

### <span data-ttu-id="afaf6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="afaf6-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="afaf6-112">Esse comando suspende a conexão de replicação do ANF no volume "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="afaf6-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="afaf6-113">OS</span><span class="sxs-lookup"><span data-stu-id="afaf6-113">PARAMETERS</span></span>

### <span data-ttu-id="afaf6-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="afaf6-114">-AccountName</span></span>
<span data-ttu-id="afaf6-115">O nome da conta ANF do volume de replicação</span><span class="sxs-lookup"><span data-stu-id="afaf6-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="afaf6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afaf6-116">-DefaultProfile</span></span>
<span data-ttu-id="afaf6-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="afaf6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afaf6-118">-ForceBreak</span><span class="sxs-lookup"><span data-stu-id="afaf6-118">-ForceBreak</span></span>
<span data-ttu-id="afaf6-119">Se a replicação estiver em transferência de status e você quiser forçar a interrupção da replicação, defina como verdadeiro</span><span class="sxs-lookup"><span data-stu-id="afaf6-119">If replication is in status transferring and you want to force break the replication, set to true</span></span>

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

### <span data-ttu-id="afaf6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afaf6-120">-InputObject</span></span>
<span data-ttu-id="afaf6-121">O objeto de volume de destino ANF com a replicação a ser interrompida</span><span class="sxs-lookup"><span data-stu-id="afaf6-121">The ANF destination volume object with the replication to break</span></span>

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

### <span data-ttu-id="afaf6-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="afaf6-122">-Name</span></span>
<span data-ttu-id="afaf6-123">O nome do volume de destino de replicação do ANF</span><span class="sxs-lookup"><span data-stu-id="afaf6-123">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="afaf6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afaf6-124">-PassThru</span></span>
<span data-ttu-id="afaf6-125">Retorna se a interrupção da replicação do volume especificado foi realizada</span><span class="sxs-lookup"><span data-stu-id="afaf6-125">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="afaf6-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="afaf6-126">-PoolName</span></span>
<span data-ttu-id="afaf6-127">O nome do pool ANF do volume de replicação</span><span class="sxs-lookup"><span data-stu-id="afaf6-127">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="afaf6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afaf6-128">-ResourceGroupName</span></span>
<span data-ttu-id="afaf6-129">O grupo de recursos do volume de destino de replicação do ANF</span><span class="sxs-lookup"><span data-stu-id="afaf6-129">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="afaf6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afaf6-130">-ResourceId</span></span>
<span data-ttu-id="afaf6-131">A ID do recurso do volume de destino de replicação do ANF</span><span class="sxs-lookup"><span data-stu-id="afaf6-131">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="afaf6-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="afaf6-132">-Confirm</span></span>
<span data-ttu-id="afaf6-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afaf6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afaf6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afaf6-134">-WhatIf</span></span>
<span data-ttu-id="afaf6-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="afaf6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afaf6-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="afaf6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afaf6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afaf6-137">CommonParameters</span></span>
<span data-ttu-id="afaf6-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afaf6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afaf6-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afaf6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afaf6-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="afaf6-140">INPUTS</span></span>

### <span data-ttu-id="afaf6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="afaf6-141">System.String</span></span>

### <span data-ttu-id="afaf6-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="afaf6-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="afaf6-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="afaf6-143">OUTPUTS</span></span>

### <span data-ttu-id="afaf6-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="afaf6-144">System.Boolean</span></span>

## <span data-ttu-id="afaf6-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="afaf6-145">NOTES</span></span>

## <span data-ttu-id="afaf6-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="afaf6-146">RELATED LINKS</span></span>
