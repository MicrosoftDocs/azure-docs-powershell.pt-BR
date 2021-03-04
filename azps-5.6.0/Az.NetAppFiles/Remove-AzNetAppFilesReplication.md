---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
ms.openlocfilehash: 4087725afbf845e42c2a00952a818f5eb356d421
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887423"
---
# <span data-ttu-id="dd872-101">Remove-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="dd872-101">Remove-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="dd872-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd872-102">SYNOPSIS</span></span>
<span data-ttu-id="dd872-103">Remover/excluir a conexão de replicação no volume de destino e enviar a versão para a replicação de origem</span><span class="sxs-lookup"><span data-stu-id="dd872-103">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="dd872-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dd872-104">SYNTAX</span></span>

### <span data-ttu-id="dd872-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dd872-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd872-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd872-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd872-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd872-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd872-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dd872-108">DESCRIPTION</span></span>
<span data-ttu-id="dd872-109">Remover/excluir a conexão de replicação no volume de destino e enviar a versão para a replicação de origem</span><span class="sxs-lookup"><span data-stu-id="dd872-109">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="dd872-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd872-110">EXAMPLES</span></span>

### <span data-ttu-id="dd872-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dd872-111">Example 1</span></span>
```powershell
PS C:\> Remove-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="dd872-112">Este comando remove a conexão de Replicação ANF no volume "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="dd872-112">This command removes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="dd872-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dd872-113">PARAMETERS</span></span>

### <span data-ttu-id="dd872-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dd872-114">-AccountName</span></span>
<span data-ttu-id="dd872-115">O nome da conta ANF do volume de replicação</span><span class="sxs-lookup"><span data-stu-id="dd872-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="dd872-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd872-116">-DefaultProfile</span></span>
<span data-ttu-id="dd872-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd872-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd872-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd872-118">-InputObject</span></span>
<span data-ttu-id="dd872-119">O volume de destino da ANF com a replicação a ser removido</span><span class="sxs-lookup"><span data-stu-id="dd872-119">The ANF destination volume with the replication to remove</span></span>

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

### <span data-ttu-id="dd872-120">-Name</span><span class="sxs-lookup"><span data-stu-id="dd872-120">-Name</span></span>
<span data-ttu-id="dd872-121">O nome do volume de destino de replicação ANF</span><span class="sxs-lookup"><span data-stu-id="dd872-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="dd872-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd872-122">-PassThru</span></span>
<span data-ttu-id="dd872-123">Retornar se a replicação ANF especificada foi removida com êxito</span><span class="sxs-lookup"><span data-stu-id="dd872-123">Return whether the specified ANF replication was successfully removed</span></span>

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

### <span data-ttu-id="dd872-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="dd872-124">-PoolName</span></span>
<span data-ttu-id="dd872-125">O nome do pool ANF do volume de replicação</span><span class="sxs-lookup"><span data-stu-id="dd872-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="dd872-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd872-126">-ResourceGroupName</span></span>
<span data-ttu-id="dd872-127">O grupo de recursos do volume de destino de replicação ANF</span><span class="sxs-lookup"><span data-stu-id="dd872-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="dd872-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd872-128">-ResourceId</span></span>
<span data-ttu-id="dd872-129">A id de recurso do volume de destino de replicação ANF</span><span class="sxs-lookup"><span data-stu-id="dd872-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="dd872-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd872-130">-Confirm</span></span>
<span data-ttu-id="dd872-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd872-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd872-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd872-132">-WhatIf</span></span>
<span data-ttu-id="dd872-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dd872-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd872-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dd872-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd872-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd872-135">CommonParameters</span></span>
<span data-ttu-id="dd872-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd872-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd872-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd872-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd872-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd872-138">INPUTS</span></span>

### <span data-ttu-id="dd872-139">System.String</span><span class="sxs-lookup"><span data-stu-id="dd872-139">System.String</span></span>

### <span data-ttu-id="dd872-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="dd872-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="dd872-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dd872-141">OUTPUTS</span></span>

### <span data-ttu-id="dd872-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dd872-142">System.Boolean</span></span>

## <span data-ttu-id="dd872-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="dd872-143">NOTES</span></span>

## <span data-ttu-id="dd872-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd872-144">RELATED LINKS</span></span>
