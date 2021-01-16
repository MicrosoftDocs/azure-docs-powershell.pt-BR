---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 95ed2dc354f32229727a3d1b13dbfdfb95fe001a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271940"
---
# <span data-ttu-id="435b2-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="435b2-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="435b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="435b2-102">SYNOPSIS</span></span>
<span data-ttu-id="435b2-103">Retome/sincronize novamente a conexão no volume de destino.</span><span class="sxs-lookup"><span data-stu-id="435b2-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="435b2-104">Se a operação for executada no volume de origem, será revertida-sincronizar novamente a conexão e sincronizar da origem para o destino.</span><span class="sxs-lookup"><span data-stu-id="435b2-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="435b2-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="435b2-105">SYNTAX</span></span>

### <span data-ttu-id="435b2-106">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="435b2-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="435b2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="435b2-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="435b2-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="435b2-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="435b2-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="435b2-109">DESCRIPTION</span></span>
<span data-ttu-id="435b2-110">Retomar/ressincronizar a conexão no volume de destino</span><span class="sxs-lookup"><span data-stu-id="435b2-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="435b2-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="435b2-111">EXAMPLES</span></span>

### <span data-ttu-id="435b2-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="435b2-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="435b2-113">Esse comando retoma a conexão de replicação do ANF no volume "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="435b2-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="435b2-114">OS</span><span class="sxs-lookup"><span data-stu-id="435b2-114">PARAMETERS</span></span>

### <span data-ttu-id="435b2-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="435b2-115">-AccountName</span></span>
<span data-ttu-id="435b2-116">O nome da conta ANF do volume de replicação</span><span class="sxs-lookup"><span data-stu-id="435b2-116">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="435b2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="435b2-117">-DefaultProfile</span></span>
<span data-ttu-id="435b2-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="435b2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="435b2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="435b2-119">-InputObject</span></span>
<span data-ttu-id="435b2-120">O objeto de volume de destino de replicação do ANF para ressincronização</span><span class="sxs-lookup"><span data-stu-id="435b2-120">The ANF replication destination volume object to resync</span></span>

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

### <span data-ttu-id="435b2-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="435b2-121">-Name</span></span>
<span data-ttu-id="435b2-122">O nome do volume de destino de replicação do ANF</span><span class="sxs-lookup"><span data-stu-id="435b2-122">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="435b2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="435b2-123">-PassThru</span></span>
<span data-ttu-id="435b2-124">Retornar se a ressincronização do volume de replicação especificado foi realizada</span><span class="sxs-lookup"><span data-stu-id="435b2-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="435b2-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="435b2-125">-PoolName</span></span>
<span data-ttu-id="435b2-126">O nome do pool ANF do volume de replicação</span><span class="sxs-lookup"><span data-stu-id="435b2-126">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="435b2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="435b2-127">-ResourceGroupName</span></span>
<span data-ttu-id="435b2-128">O grupo de recursos do volume de destino de replicação do ANF</span><span class="sxs-lookup"><span data-stu-id="435b2-128">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="435b2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="435b2-129">-ResourceId</span></span>
<span data-ttu-id="435b2-130">A ID do recurso do volume de destino de replicação do ANF</span><span class="sxs-lookup"><span data-stu-id="435b2-130">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="435b2-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="435b2-131">-Confirm</span></span>
<span data-ttu-id="435b2-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="435b2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="435b2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="435b2-133">-WhatIf</span></span>
<span data-ttu-id="435b2-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="435b2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="435b2-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="435b2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="435b2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="435b2-136">CommonParameters</span></span>
<span data-ttu-id="435b2-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="435b2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="435b2-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="435b2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="435b2-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="435b2-139">INPUTS</span></span>

### <span data-ttu-id="435b2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="435b2-140">System.String</span></span>

### <span data-ttu-id="435b2-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="435b2-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="435b2-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="435b2-142">OUTPUTS</span></span>

### <span data-ttu-id="435b2-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="435b2-143">System.Boolean</span></span>

## <span data-ttu-id="435b2-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="435b2-144">NOTES</span></span>

## <span data-ttu-id="435b2-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="435b2-145">RELATED LINKS</span></span>
