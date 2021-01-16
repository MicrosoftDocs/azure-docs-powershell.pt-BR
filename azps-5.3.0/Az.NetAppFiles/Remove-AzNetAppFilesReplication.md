---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
ms.openlocfilehash: 04ad7f188a2280dcdf84e8b5c1f45e20edf4d07b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271952"
---
# <span data-ttu-id="c57fd-101">Remove-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="c57fd-101">Remove-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="c57fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c57fd-102">SYNOPSIS</span></span>
<span data-ttu-id="c57fd-103">Remover/excluir a conexão de replicação no volume de destino e enviar a liberação para a replicação de origem</span><span class="sxs-lookup"><span data-stu-id="c57fd-103">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="c57fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c57fd-104">SYNTAX</span></span>

### <span data-ttu-id="c57fd-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c57fd-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c57fd-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c57fd-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c57fd-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c57fd-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c57fd-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c57fd-108">DESCRIPTION</span></span>
<span data-ttu-id="c57fd-109">Remover/excluir a conexão de replicação no volume de destino e enviar a liberação para a replicação de origem</span><span class="sxs-lookup"><span data-stu-id="c57fd-109">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="c57fd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c57fd-110">EXAMPLES</span></span>

### <span data-ttu-id="c57fd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c57fd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="c57fd-112">Esse comando Remove a conexão de replicação do ANF no volume "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="c57fd-112">This command removes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="c57fd-113">OS</span><span class="sxs-lookup"><span data-stu-id="c57fd-113">PARAMETERS</span></span>

### <span data-ttu-id="c57fd-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c57fd-114">-AccountName</span></span>
<span data-ttu-id="c57fd-115">O nome da conta ANF do volume de replicação</span><span class="sxs-lookup"><span data-stu-id="c57fd-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="c57fd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c57fd-116">-DefaultProfile</span></span>
<span data-ttu-id="c57fd-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c57fd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c57fd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c57fd-118">-InputObject</span></span>
<span data-ttu-id="c57fd-119">O volume de destino do ANF com a replicação a ser removida</span><span class="sxs-lookup"><span data-stu-id="c57fd-119">The ANF destination volume with the replication to remove</span></span>

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

### <span data-ttu-id="c57fd-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c57fd-120">-Name</span></span>
<span data-ttu-id="c57fd-121">O nome do volume de destino de replicação do ANF</span><span class="sxs-lookup"><span data-stu-id="c57fd-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="c57fd-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c57fd-122">-PassThru</span></span>
<span data-ttu-id="c57fd-123">Retorna se a replicação de ANF especificada foi removida com êxito</span><span class="sxs-lookup"><span data-stu-id="c57fd-123">Return whether the specified ANF replication was successfully removed</span></span>

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

### <span data-ttu-id="c57fd-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="c57fd-124">-PoolName</span></span>
<span data-ttu-id="c57fd-125">O nome do pool ANF do volume de replicação</span><span class="sxs-lookup"><span data-stu-id="c57fd-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="c57fd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c57fd-126">-ResourceGroupName</span></span>
<span data-ttu-id="c57fd-127">O grupo de recursos do volume de destino de replicação do ANF</span><span class="sxs-lookup"><span data-stu-id="c57fd-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="c57fd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c57fd-128">-ResourceId</span></span>
<span data-ttu-id="c57fd-129">A ID do recurso do volume de destino de replicação do ANF</span><span class="sxs-lookup"><span data-stu-id="c57fd-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="c57fd-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c57fd-130">-Confirm</span></span>
<span data-ttu-id="c57fd-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c57fd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c57fd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c57fd-132">-WhatIf</span></span>
<span data-ttu-id="c57fd-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c57fd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c57fd-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c57fd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c57fd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c57fd-135">CommonParameters</span></span>
<span data-ttu-id="c57fd-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c57fd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c57fd-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c57fd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c57fd-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c57fd-138">INPUTS</span></span>

### <span data-ttu-id="c57fd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c57fd-139">System.String</span></span>

### <span data-ttu-id="c57fd-140">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c57fd-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="c57fd-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c57fd-141">OUTPUTS</span></span>

### <span data-ttu-id="c57fd-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c57fd-142">System.Boolean</span></span>

## <span data-ttu-id="c57fd-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c57fd-143">NOTES</span></span>

## <span data-ttu-id="c57fd-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c57fd-144">RELATED LINKS</span></span>
