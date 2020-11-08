---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: eb695da1dc1fea238a57ea1c98bec42899e8f28f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111615"
---
# <span data-ttu-id="2dcf6-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="2dcf6-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="2dcf6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2dcf6-102">SYNOPSIS</span></span>
<span data-ttu-id="2dcf6-103">Suspender/interromper a conexão de replicação no volume de destino</span><span class="sxs-lookup"><span data-stu-id="2dcf6-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="2dcf6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2dcf6-104">SYNTAX</span></span>

### <span data-ttu-id="2dcf6-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2dcf6-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2dcf6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dcf6-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dcf6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dcf6-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dcf6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2dcf6-108">DESCRIPTION</span></span>
<span data-ttu-id="2dcf6-109">Suspender/interromper a conexão de replicação no volume de destino</span><span class="sxs-lookup"><span data-stu-id="2dcf6-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="2dcf6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2dcf6-110">EXAMPLES</span></span>

### <span data-ttu-id="2dcf6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2dcf6-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="2dcf6-112">Esse comando suspende a conexão de replicação do ANF no volume "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="2dcf6-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="2dcf6-113">OS</span><span class="sxs-lookup"><span data-stu-id="2dcf6-113">PARAMETERS</span></span>

### <span data-ttu-id="2dcf6-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2dcf6-114">-AccountName</span></span>
<span data-ttu-id="2dcf6-115">O nome da conta ANF do volume de replicação</span><span class="sxs-lookup"><span data-stu-id="2dcf6-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="2dcf6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dcf6-116">-DefaultProfile</span></span>
<span data-ttu-id="2dcf6-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2dcf6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dcf6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2dcf6-118">-InputObject</span></span>
<span data-ttu-id="2dcf6-119">O objeto de volume de destino ANF com a replicação a ser interrompida</span><span class="sxs-lookup"><span data-stu-id="2dcf6-119">The ANF destination volume object with the replication to break</span></span>

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

### <span data-ttu-id="2dcf6-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="2dcf6-120">-Name</span></span>
<span data-ttu-id="2dcf6-121">O nome do volume de destino de replicação do ANF</span><span class="sxs-lookup"><span data-stu-id="2dcf6-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="2dcf6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2dcf6-122">-PassThru</span></span>
<span data-ttu-id="2dcf6-123">Retorna se a interrupção da replicação do volume especificado foi realizada</span><span class="sxs-lookup"><span data-stu-id="2dcf6-123">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="2dcf6-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="2dcf6-124">-PoolName</span></span>
<span data-ttu-id="2dcf6-125">O nome do pool ANF do volume de replicação</span><span class="sxs-lookup"><span data-stu-id="2dcf6-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="2dcf6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dcf6-126">-ResourceGroupName</span></span>
<span data-ttu-id="2dcf6-127">O grupo de recursos do volume de destino de replicação do ANF</span><span class="sxs-lookup"><span data-stu-id="2dcf6-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="2dcf6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2dcf6-128">-ResourceId</span></span>
<span data-ttu-id="2dcf6-129">A ID do recurso do volume de destino de replicação do ANF</span><span class="sxs-lookup"><span data-stu-id="2dcf6-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="2dcf6-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2dcf6-130">-Confirm</span></span>
<span data-ttu-id="2dcf6-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dcf6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dcf6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dcf6-132">-WhatIf</span></span>
<span data-ttu-id="2dcf6-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2dcf6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dcf6-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2dcf6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dcf6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dcf6-135">CommonParameters</span></span>
<span data-ttu-id="2dcf6-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dcf6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dcf6-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2dcf6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dcf6-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2dcf6-138">INPUTS</span></span>

### <span data-ttu-id="2dcf6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2dcf6-139">System.String</span></span>

### <span data-ttu-id="2dcf6-140">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="2dcf6-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="2dcf6-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2dcf6-141">OUTPUTS</span></span>

### <span data-ttu-id="2dcf6-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2dcf6-142">System.Boolean</span></span>

## <span data-ttu-id="2dcf6-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2dcf6-143">NOTES</span></span>

## <span data-ttu-id="2dcf6-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2dcf6-144">RELATED LINKS</span></span>
